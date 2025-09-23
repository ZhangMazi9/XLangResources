# README
This document details the structure of the current project directory and the core content of files in each folder.

## 1. dataset Folder
Contains relevant content of the X language model datasets:
- **Subfolder: xlang-dataset-sample**: Provides a portion of the X language model datasets (JSON format). Each sample includes a complete X language model consisting of a Couple Class Model and its associated Atomic Class Models.
- **File: ft_generate_xlang_discrete_model.json**: A small-scale dataset for directly fine-tuning large language models via Llama Factory. Derived from extracting Atomic Class Models from complete X language models and converting to the format in Section 3.3.1, representing part of the dataset used for fine-tuning in experiments.

## 2. docs Folder
Stores design documents and language model-related files via two subfolders:
- **Subfolder: product design document**: Includes system-level design documents and component-level requirement documents of the aircraft electrical system. Interface specifications and specific parameter details are redacted for commercial reasons.
- **Subfolder: X language model**: Contains manually modified aircraft electrical system X language models (executable via X language compiler and simulator from www.xlab-bh.com). The software is in prototype stage (no comprehensive user guide yet); `Xlab Demo Video.mp4` is provided to showcase the full workflow of obtaining simulation results and the compiler's compilation process.

## 3. results Folder
Stores model fine-tuning outputs: LoRA module parameters and training outcomes from fine-tuning CodeQwen with 5,404 samples (hyperparameters as in Section 4.1). Initially trained for 5 epochs, but overfitting occurred after the 3rd epoch (shown in `training_eval_loss.png`), so actual experiments used 3 epochs.
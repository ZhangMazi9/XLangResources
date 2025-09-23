---
library_name: peft
license: other
base_model: /data/LLM/CodeQwen1.5-7B-Chat
tags:
- llama-factory
- lora
- generated_from_trainer
model-index:
- name: train_2025-09-19-10-06-10
  results: []
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# train_2025-09-19-10-06-10

This model is a fine-tuned version of [/data/LLM/CodeQwen1.5-7B-Chat](https://huggingface.co//data/LLM/CodeQwen1.5-7B-Chat) on the discrete_dataset dataset.
It achieves the following results on the evaluation set:
- Loss: 0.1308
- Num Input Tokens Seen: 8297520

## Model description

More information needed

## Intended uses & limitations

More information needed

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 5e-05
- train_batch_size: 1
- eval_batch_size: 1
- seed: 42
- gradient_accumulation_steps: 8
- total_train_batch_size: 8
- optimizer: Use OptimizerNames.ADAMW_TORCH with betas=(0.9,0.999) and epsilon=1e-08 and optimizer_args=No additional optimizer arguments
- lr_scheduler_type: cosine
- num_epochs: 5.0

### Training results



### Framework versions

- PEFT 0.15.2
- Transformers 4.52.4
- Pytorch 2.7.1+cu126
- Datasets 2.20.0
- Tokenizers 0.21.1
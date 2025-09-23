# Control bus module
### 1. Module Function

The core function of the Control Bus Module is to receive flight control instructions (evInstruct), parse these instructions, and then send corresponding control signals to electrical equipment. These signals are used to adjust the power consumption of the electrical equipment, ensuring each device operates at a power level matching the current flight scenario, thereby supporting the stable execution of the overall flight mission.

### 2. Module Working Principle & State Logic

The Control Bus Module operates with distinct states and clear instruction parsing rules, which govern its signal output to electrical equipment. Details are as follows:

#### 2.1 Basic Working States

- **Idle State**: Under normal conditions, the module stays in the idle state, waiting to receive external flight control instructions (evInstruct).

- **Parsing State**: Upon receiving a flight control instruction (evInstruct), the module immediately transitions from the idle state to the parsing state. In this state, it parses the instruction and generates corresponding output signals based on preset rules to control the electrical equipment.

#### 2.2 Instruction Parsing & Signal Output Rules

After entering the parsing state, the module parses the received flight control instruction (evInstruct) and sets the output signals for target devices (radar, engine, steering gear) according to the following rules:

- If the received instruction matches the first preset type, the module sets the radar preheating signal and steering gear activation signal to the effective state.

- If the received instruction matches the second preset type, the module sets the engine activation signal to the effective state.

- If the received instruction matches the third preset type, the module sets the steering gear power adjustment (first gear) signal and radar high-voltage activation signal to the effective state.

- If the received instruction matches the fourth preset type, the module sets the steering gear power adjustment (second gear) signal to the effective state.

- If the received instruction matches the fifth preset type, the module sets the steering gear power adjustment (first gear) signal to the effective state.

- If the received instruction does not match any of the above preset types, the module sets the steering gear power adjustment (third gear) signal to the effective state.

Each time the module receives an instruction, it executes the parsing and signal output process once, ensuring the electrical equipment responds promptly to current flight control requirements.
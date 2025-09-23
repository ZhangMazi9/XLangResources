# Rudder module
### 1. Module Function

The core function of the Steering Gear Module is to adjust its operating power according to the received control signals. By responding to different power adjustment instructions, it regulates the output current, thereby adapting to the aircraft's attitude control needs under various flight scenarios and ensuring stable flight operations.

### 2. Module Working Principle & State Logic

The Steering Gear Module operates through state transitions triggered by control signals, with clear rules for current output corresponding to different instructions. Details are as follows:

#### 2.1 Basic Working States

- **Shutdown State**: Initially, the module is in the shutdown state, remaining inactive and awaiting activation signals.

- **Operating State**: When the steering gear activation signal is received, the module triggers a state transition from the shutdown state to the operating state. In this state, it monitors power adjustment signals in real time and executes corresponding current output operations.

- **Transient State (tran State)**: This is a temporary transition state. Whenever the module receives a power adjustment signal in the operating state, it immediately enters the transient state, completes the current output, and then switches back instantly.

#### 2.2 Signal Response & Current Output Rules

In the operating state, the module responds to different power adjustment signals and outputs the corresponding operating current through the transient state, following these rules:

- If the first-level power adjustment signal is received, the module enters the transient state and outputs the matching first-level operating current.

- If the second-level power adjustment signal is received, the module enters the transient state and outputs the matching second-level operating current.

- If the third-level power adjustment signal is received, the module enters the transient state and outputs the matching third-level operating current.

After completing the current output in the transient state, the module immediately returns to the operating state to wait for subsequent control signals, ensuring rapid response to attitude adjustment requirements during flight.
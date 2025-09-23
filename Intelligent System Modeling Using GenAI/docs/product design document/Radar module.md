# Radar module
### 1. Module Function

The core function of the Radar Module is to detect the position of target objects. It achieves target positioning by switching between different working states based on received control signals, providing key position information for the aircraft's flight trajectory adjustment and mission execution.

### 2. Module Working Principle & State Logic

The Radar Module operates through sequential state transitions triggered by specific control signals, with each state corresponding to a distinct operating mode. Details are as follows:

#### 2.1 Basic Working States

- **Off State**: Initially, the module defaults to the off state, remaining inoperative and awaiting activation signals.

- **Preheating State**: This is an intermediate preparation state. After receiving the preheating control signal, the module transitions from the off state to this state to complete operational preparations.

- **High-Voltage On State**: This is the formal working state. After receiving the high-voltage activation signal, the module transitions to this state and starts executing target detection tasks.

#### 2.2 State Transition & Operating Rules

The module's state transitions follow a fixed logical sequence, with each transition triggered by a specific control signal:

- When the radar preheating signal is received in the off state, the module transitions to the preheating state and maintains the operating current matching this state.

- When the high-voltage activation signal is received in the preheating state, the module further transitions to the high-voltage on state, adjusts to the operating current matching this working state, and begins target position detection.

The module relies on this step-by-step state transition process to ensure stable startup and reliable execution of target detection functions.
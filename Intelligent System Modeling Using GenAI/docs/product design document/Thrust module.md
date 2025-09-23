# Thrust module
### 1. Module Function

The core function of the Thrust Module is to provide power for the aircraft. It responds to activation signals to complete the startup process, generating the necessary thrust to support the aircraft's takeoff, attitude adjustment, and mission execution, serving as a key power source for the aircraft's flight operations.

### 2. Module Working Principle & State Logic

The Thrust Module operates through sequential state transitions triggered by control signals, with each state corresponding to a specific working phase. Details are as follows:

#### 2.1 Basic Working States

- **Unignited Off State**: Initially, the module defaults to the unignited off state, remaining inactive and not providing power, awaiting the activation signal.

- **Ignition State**: This is the transient startup state. After receiving the activation signal, the module transitions from the unignited off state to this state to complete the ignition and power initiation process.

- **Post-Ignition State**: After the ignition process is completed, the module enters this state, ending the power output and returning to a quiescent state.

#### 2.2 State Transition & Operating Rules

The module's state transitions follow a fixed logical sequence, with clear operating characteristics in each state:

- When the activation signal is received in the unignited off state, the module immediately transitions to the ignition state and maintains the operating current matching this startup phase.

- After maintaining the ignition state for a preset duration to complete the power initiation, the module exits the ignition state and enters the post-ignition state. At this point, the operating current is adjusted to the quiescent value, and the power supply process is concluded.

This phased state transition ensures the module completes the power supply task safely and reliably, meeting the aircraft's demand for transient thrust output.
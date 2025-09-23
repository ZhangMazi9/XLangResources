# Battery module
### 1. Module Function

The core function of the Power Supply Module is to provide stable operating voltage for all other functional modules of the aircraft. It maintains a constant voltage output throughout the working period, ensuring that each electrical module receives continuous and reliable power support, which is the foundational guarantee for the normal operation of the entire aircraft electrical system.

### 2. Module Working Principle & State Logic

The Power Supply Module has a simple and clear state transition mechanism, with each state corresponding to distinct operating modes. Details are as follows:

#### 2.1 Basic Working States

- **Initial State**: Initially, the module defaults to the initial state, remaining in a standby condition and not outputting voltage, awaiting the startup signal.

- **Operating State**: This is the formal power supply state. After receiving the startup signal, the module transitions to this state and begins stable voltage output.

#### 2.2 State Transition & Operating Rules

The module's state transition follows a one-way logical sequence, with fixed operating characteristics in each state:

- When the startup signal is received in the initial state, the module immediately transitions from the initial state to the operating state.

- Once entering the operating state, the module maintains this state continuously and provides the preset stable operating voltage to the connected electrical modules. This state is sustained throughout the entire working cycle to ensure uninterrupted power supply.

This stable state maintenance mechanism ensures that all functional modules obtain consistent voltage support, laying a solid foundation for the coordinated operation of the aircraft's electrical system.
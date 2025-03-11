CPU Architecture Project

Overview
This repository contains a simplified CPU architecture designed for educational purposes. The design includes key components such as the **Control FSM, ALU, Register Bank, Memory, and Interconnect Bus Interface**.

## Components Breakdown

1️⃣ Clock & Control Signals
- Synchronizes all components
- **Inverted Clock** used for timing adjustments
- **Control FSM** manages state transitions

2️⃣ Instruction Register
- Holds the current instruction
- **Opcode** decoded to generate control signals

3️⃣ Control FSM (Finite State Machine)
- Determines next state based on **opcode**
- Controls memory access, register selection, and ALU operations

4️⃣ Register Bank (16 x 32-bit)
- Stores temporary data
- **RegSEL** selects register
- **RegLD** loads data into registers

5️⃣ Main Memory
- Connected via **Interconnection Address Bus** and **Interconnection Data Bus**
- **IBRead / IBWrite** control memory access

6️⃣ Interconnect Bus Interface
- Handles data transfer between memory, registers, and ALU
- **MDR (Memory Data Register)** and **MAR (Memory Address Register)** manage data transactions
- **MDRCE, MDROE, MARCE, MAROE** control input/output operations

7️⃣ ALU (Arithmetic Logic Unit)
- Executes arithmetic and logic operations
- Uses **TEMP1** and **TEMP2** registers
- **Flags (C, V, N, Z)** indicate results

Execution Flow
1. **Fetch:** CPU retrieves instruction from memory
2. **Decode:** Control FSM interprets **opcode**
3. **Operand Fetch:** Load data from memory/registers to ALU inputs
4. **Execute:** ALU processes operation and updates flags
5. **Write Back:** Store result in register/memory

Notes 📝
- Follows **Fetch-Decode-Execute** cycle
- **Control FSM** drives all signals based on **opcode**
- **ALU Flags** used for conditional operations
- Expandable with additional instructions and features
How to Use 
1. Open the project in **Logisim/Quartus/Multisim** (or your preferred tool).
2. Run the simulation with a clock cycle.
3. Observe data flow and register updates.

License 📜
This project is for educational purposes. Feel free to use and modify it, but please provide credit when necessary.



### 🔗 Contributors
- **Maxence Deschenes**

For questions, feel free to reach out!


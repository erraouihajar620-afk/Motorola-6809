# Motorola 6809 Simulator

## Project Description

This project is a complete simulator of the Motorola 6809 microprocessor, developed in Java with a Swing-based graphical interface. It allows users to write, compile, and execute assembly code for the 6809 processor, offering both step-by-step debugging and full program execution.

## Main Features

### Graphical Interface
- **Assembly Editor**: Text editor with line numbering for writing assembly code
- **Register Display**: Real-time visualization of processor registers (A, B, D, X, Y, U, S, PC, CC)
- **RAM Memory**: Display and modification of random-access memory
- **ROM Memory**: Display of read-only memory containing the compiled program
- **Modern Interface**: Dark theme design with accent colors

### Execution Modes
- **Compilation**: Translation of assembly code into machine code
- **Step-by-Step Execution**: Instruction-by-instruction debugging with real-time state updates
- **Full Execution**: Automatic execution of the entire program
- **Reset**: Complete reset of the simulator

## Supported Instructions

### Load Instructions
- `LDA`, `LDB`, `LDD`, `LDS`, `LDU`, `LDX`, `LDY` with multiple addressing modes

### Store Instructions
- `STA`, `STB`, `STD`, `STS`, `STU`, `STX`, `STY`

### Arithmetic Instructions
- `ADDA`, `ADDB`, `ADDD` (addition)
- `ADCA`, `ADCB` (addition with carry)
- `INCA`, `INCB`, `INC` (increment)
- `DECA`, `DECB`, `DEC` (decrement)
- `ABX` (add to index register X)

### Comparison Instructions
- `CMPA`, `CMPB`, `CMPD`, `CMPS`, `CMPU`, `CMPX`, `CMPY`

### Branch Instructions
- `BRA` (unconditional branch)
- `BRN` (never branch)
- Conditional branches:
  `BHI`, `BLS`, `BCC`, `BCS`, `BNE`, `BEQ`, `BVC`, `BVS`, `BPL`, `BMI`, `BGE`, `BLT`, `BGT`, `BLE`

### Other Instructions
- `CLRA`, `CLRB`, `CLR` (clear)
- `JMP` (jump)
- `PSHS`, `PSHU`, `PULS`, `PULU` (stack operations)
- `TFR` (register transfer)

## Supported Addressing Modes

- **Immediate**: Direct value (e.g., `LDA #$10`)
- **Direct**: 8-bit address (e.g., `LDA $10`)
- **Direct Indexed**: Indexed addressing (e.g., `LDA 0,X`)
- **Extended Direct**: 16-bit address (e.g., `LDA $1000`)
- **Extended Indirect**: Indirect addressing (e.g., `LDA [$1000]`)
- **Relative**: Used for branch instructions
- **Inherent**: No operand (e.g., `INCA`)

## Project Architecture

### Main Classes
- `clsMain` : Application entry point
- `clsMoto6809` : Main graphical interface and event handling
- `clsCompiler` : Assembler compiler (assembly to machine code)
- `clsExecuter` : Full program execution
- `clsPasàpas` : Step-by-step execution (debugger)
- `clsInstructions` : Instruction definitions and opcodes
- `clsAdressingModes` : Addressing mode handling
- `clsRegisters` : CPU register management
- `clsRAM` : RAM memory simulation
- `clsROM` : ROM memory simulation
- `clsErreur` : Compilation and execution error handling

### File Structure

simulateur_moto6809/
├── src/
│   ├── clsMain.java
│   ├── clsMoto6809.java
│   ├── clsCompiler.java
│   ├── clsExecuter.java
│   ├── clsPasàpas.java
│   ├── clsInstructions.java
│   ├── clsAdressingModes.java
│   ├── clsRegisters.java
│   ├── clsRAM.java
│   ├── clsROM.java
│   └── clsErreur.java
├── lib/
├── bin/
└── README.md

## Installation and Usage

### Requirements
- Java Development Kit (JDK) 8 or higher
- Java development environment (recommended: VS Code with Java extensions)

### Compilation and Execution
1. Open the project in your Java IDE
2. Compile all source files
3. Run `clsMain.java`

### Using the Simulator
1. Write code using the assembly editor
2. Click **COMPILER** to generate machine code
3. Use **STEP BY STEP** for instruction-level debugging
4. Click **EXECUTE** to run the full program
5. Use **RESET** to reinitialize the simulator

## Example Program

LDA #$10
STA $1000
LDB #$20
ADDA #$05

## Advanced Features

### Step-by-Step Debugging
- Instruction-by-instruction execution
- Real-time register updates
- Execution tracking in memory

### Error Handling
- Syntax error detection during compilation
- Detailed error messages
- Addressing mode validation

### User Interface
- Modern dark-themed design
- Interactive buttons with visual effects
- Real-time display updates

## Development and Extension

The project is modular and extensible. To add new instructions:
1. Add the instruction to `clsInstructions.java`
2. Implement the logic in `clsExecuter.java` and `clsPasàpas.java`
3. Update the interface display if necessary

## Technologies Used
- Java
- Swing
- AWT

## Author

Developed as part of an educational project on computer architecture and processor simulation.

## License

This project is provided for educational purposes only. Please respect the intellectual property rights of the Motorola 6809.

<img width="1062" height="576" alt="image" src="https://github.com/user-attachments/assets/5f091903-78c7-4729-9428-93fcc2940aaf" />


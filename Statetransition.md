


## States and Transitions

### State 0: 0 Rs in Vending Machine
- If no coins are added, the vending machine stays in State 0.
  - OUTPUT = 0
  - CHANGE = 0
- If 5 Rs is added, the vending machine transitions to State 1.
  - OUTPUT = 0
  - CHANGE = 0
- If 10 Rs is added, the vending machine transitions to State 2.
  - OUTPUT = 0
  - CHANGE = 0

### State 1: 5 Rs in Vending Machine
- If no coins are added after a brief period, an incomplete transaction is indicated, and the vending machine returns the added 5 Rs as CHANGE.
  - Move to State 0
  - OUTPUT = 0
  - CHANGE = Rs 5 (01)
- If 5 Rs is added, the vending machine stays in State 1.
  - OUTPUT = 0
  - CHANGE = 0
- If 10 Rs is added, the vending machine transitions to State 0 and dispenses a bottle without CHANGE.
  - OUTPUT = 1
  - CHANGE = Rs 0

### State 2: 10 Rs in Vending Machine
- If no coins are added, an incomplete transaction occurs, and the vending machine returns the added 10 Rs as CHANGE.
  - Move to State 0
  - OUTPUT = 0
  - CHANGE = Rs 10 (10)
- If 5 Rs is added, a complete transaction occurs, and a bottle is dispensed without CHANGE.
  - Move to State 0
  - OUTPUT = 1
  - CHANGE = Rs 0
- If 10 Rs is added, an overpayment happens, and a bottle is dispensed with a CHANGE of 5 Rs.
  - Move to State 0
  - OUTPUT = 1
  - CHANGE = Rs 5 (01)

## Tools Used

- Verilog HDL
- Visual Studio Code (VSCode)
- Icarus Verilog
- GTKWave

## Getting Started

1. Clone this repository.
2. Open the Verilog files in VSCode or your preferred editor.
3. Use Icarus Verilog to simulate the design.
4. Use GTKWave to visualize simulation waveforms.



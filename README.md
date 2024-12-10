## FSM-Based Sequence Detector

### Overview
This project implements a sequence detector in Verilog to identify the specific bit pattern `1011` in a serial input stream. The design uses a Finite State Machine (FSM) approach with well-defined states and transitions.

### Features
- Detects the sequence `1011` in real-time from the input stream.
- Includes a reset functionality to reinitialize the system.
- Outputs a high signal when the sequence is detected.
- Efficient state management using a modular FSM design.

### Project Structure
- Design Module (`sequence_detector.v`)**: Contains the Verilog implementation of the sequence detector using FSM.
- Testbench Module (`tb_sequence_detector.v`)**: Verilog testbench used for simulation and verification of the design.

### Design Details
1. States:
   - `IDLE`: Initial state waiting for the first `1` in the sequence.
   - `S1`: Detected `1`.
   - `S10`: Detected `10`.
   - `S101`: Detected `101`.
   - `S1011`: Detected the complete sequence `1011`.

2. Inputs:
   - `clk`: Clock signal.
   - `reset`: Resets the FSM to the initial state.
   - `in`: Serial input stream (1-bit).

3. Output:
   - `detected`: High (`1`) when the sequence `1011` is detected.

### How to Run
1. Clone this repository to your local machine.
2. Compile and simulate the design using a Verilog compiler (e.g., Icarus Verilog or ModelSim).
3. Run the testbench (`tb_sequence_detector.v`) to verify the functionality.
4. Observe the output using `$monitor` in the Verilog simulation log.

### Simulation Example
- Input Stream: `0001011011`
- Detected Output:
  - At time `t`: Detected = `1` (when the sequence `1011` is identified).

### Learnings and Insights
- Gained hands-on experience with FSM design and state transitions.
- Strengthened skills in Verilog for sequential circuit design.
- Understood the importance of modular testbenches for rigorous simulation.

### Future Improvements
- Extend to detect multiple patterns.
- Integrate a counter for detecting patterns over time.

### Acknowledgements
Inspired by intermediate-level digital design concepts and applied towards real-time detection problems.

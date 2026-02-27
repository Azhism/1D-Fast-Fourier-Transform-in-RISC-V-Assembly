1D-Fast-Fourier-Transform-in-RISC-V-Assembly
This project implements a 1D Fast Fourier Transform (FFT) for small input sizes (N=16, N=32) using RISC-V Assembly. It provides both vectorized and non-vectorized implementations, along with helper Python scripts for data generation and output analysis.

Features
Vectorized and Non-Vectorized FFT: Compare performance and implementation of FFT using RISC-V vector extensions and standard instructions.
Configurable Input: Generate random or custom input arrays for testing.
Output Logging: Print and analyze FFT results using provided Python scripts.
RISC-V Simulation Support: Includes linker script and configuration for RISC-V simulation/emulation environments.
File Descriptions
Vectorized.s / VectorizedModified.s: Vectorized FFT implementations using RISC-V vector instructions.
NonVectorized.s: Standard (non-vectorized) FFT implementation.
code.c: Simple C file for integration or testing.
print_log_array.py: Python script to read and print FFT output arrays from binary files.
write_array.py: Python script to generate random input matrices for FFT.
link.ld: Linker script for RISC-V memory layout.
whisper.json: Configuration for RISC-V simulation/emulation (e.g., using Whisper or similar tools).
Requirements
RISC-V toolchain (assembler, linker, and simulator/emulator supporting vector extensions)
Python 3.x
Build and Run Instructions
Build the Project

Use the provided makefile (if available) to assemble and link the code:
make allV   # For vectorized version
make allNV  # For non-vectorized version
If no makefile is present, manually assemble and link using your RISC-V toolchain.
Generate Input Data

Use the Python script to generate a random input matrix:
python write_array.py
Run the Simulation

Load the assembled binary into your RISC-V simulator/emulator (e.g., Whisper, Spike, QEMU).
Use the provided whisper.json for configuration if using Whisper.
Analyze Output

Use the Python script to print and analyze the FFT output:
python print_log_array.py
Example
# Build and run vectorized FFT
make allV
python write_array.py
# Load binary into simulator (command depends on your tool)
python print_log_array.py
Notes
Adjust N (input size) in the assembly files as needed.
Ensure your simulator/emulator supports the required RISC-V extensions (especially vector instructions for vectorized versions).
For more details, see comments in the assembly and Python files.
License
This project is for educational and research purposes.

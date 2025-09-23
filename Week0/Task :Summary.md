#  ▸ Summary

The design flow involves modeling, RTL development, synthesis, integration, and physical design, with continuous verification against a reference C testbench output (O0) to ensure correctness.

## ▸Design Procedure

### ▸Chip Modeling

- Create a C language testbench.
- Run the code through GCC (compiler) to get output O0.
- Design a brief specification model (based on C), e.g., RISC-V GCC or ARM GCC.
- Run the code through this model to get output O1.
- Compare O0 = O1 to confirm the specification is correct. Freeze the specification.

### ▸ SoC Design Flow

- Develop a soft copy of hardware using RTL (Register-Transfer Level), which includes digital electronics components like NOR gates, AND gates, flip-flops, etc.
- Implement RTL in languages such as Verilog, Chisel, or Bluespec to get output O2.
- Verify if O0 = O1 = O2 (handled by RTL Architect).

### ▸ ASIC Design

- Divide the code between processor and peripherals/IPs.

### ▸ Synthesis

- Processor: Convert to gate-level netlist (Synth P1).
- Peripherals:
  - Macros (synthesize RTL).
  - Analog IPs (functional RTL), e.g., ADC, DAC (common examples: 10-bit ADC, PLL, clock multipliers).

### ▸ SoC Integration

- Integrate the SoC with GPIOs and reuse the C testbench to get output O3.
- Verify if O0 = O1 = O2 = O3 (handled by RTL Architect).

### ▸ Full Design Assembly

- Combine all elements to form the entire design, generating a GDSII file.
- Perform testing (DRC/LVS), then tape out for fabrication.
- Receive the taped-in chip.

### ▸ Post-Tape-In Testing

- Form a physical peripheral and re-test the C testbench to get O4.
- Verify if O0 = O1 = O2 = O3 = O4.

This completes the entire design flow.

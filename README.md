# ▸rajvardhanjain_VSD_RISC_V_SoC_Tapeout_Program_VSD
My work for an open source RISC V based SoC Tapeout program by VSD, this embarks a journey from RTL to GDSII, a journey towards new learnings and skill development, Welcome aboard.
▸Week 0: Tools Installation:
Summary:
Design Procedure:
▸Chip Modelling,
Create a C language testbench
1. Run the code through gcc(compiler), the output suppose it as O0.
2. Now design a breif Specification model(based on C)e.g RISCV GCC or ARM GCC etc.., run the code through this model, the output suppose it as O1.
 Now compare O0=O1, which confirms our specification to be correct. Specification freezed.
▸SoC Design flow,
1.Soft copy of hardware using RTL, hardware in the sense basically digital electronics stuff, NOR GATE, AND GATE, flipflops..etc.
which gives output O2. RTL is done in verilog/chisel/bluespec.
Now again if O0=O1=O2, we are going good.(RTL Architect)
▸ASIC Design,
Now divide the above code between processor and Peripherals/IPs.
▸Synthesis,
Processor -> Gate leve Netlist(Synth P1).
Peripheral-> 1.Macros (synth RTL)
2. Analog IPs(func RTL) [ADC, DAC Stuff  Common ->10bitADC,PLL,Clock multipliers.]
▸SoC Integration:
Now with the SoC, with GPIOs we again use our C testbench.
Getting a output, O3.
Now again O0=O1=O2=O3 (RTL Architect)
▸ Now we club everything we have done so far to form a entire design, and which creates aGDSII file.
The GDSII file goes to testing(DRC/LVS) then its taped out then it gets fabricated, which we get taped in to us.
▸After Tape in: we form a physical peripheral and now again test the C testbench to get O0=O1=O2=O3=O4.
This is the entire flow of the design. 

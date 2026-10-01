# Julien Gaius Seepersadsingh

Electrical & Computer Engineering at the University of Toronto. I started on the board side, soldering and designing PCBs for our Formula SAE car, and moved into digital design because I wanted to understand what's actually happening inside the chips on those boards. These days I mostly write and verify RTL for FPGAs.

**Looking for:** PEY co-op roles (12–16 months) in FPGA or ASIC design and verification.

**If you only look at one thing:** [Aegis](https://github.com/juliengaius/aegis), an FPGA market-data pipeline with 2-cycle latency and a fully automated test suite.

---

### How I got here

**1. Board-level hardware: University of Toronto Formula Racing (FSAE Electric)**\
Assembled and validated the rear controller PCB for UT25, North America's first driverless FSAE car. Designed a cooling-loop controller board in Altium (high-side fan drive, switching regulation, CAN) and a sensor-interface board, and built the charging and balancing system for the car's 8s low-voltage pack.

**2. Digital design: [Monte Carlo π accelerator](https://github.com/juliengaius/monte-carlo-pi) (Verilog, Intel Cyclone V)**\
A two-person course project that estimates π in hardware and draws every sample on a VGA screen: 32-bit LFSRs, a control FSM that sequences modules of different latencies, and a Q3.29 fixed-point divider. This is where I moved from boards to RTL. After the course I went back and added what it was missing:
- A bit-exact C reference model that matches the RTL on every sample (100,000 in a row)
- π to within 0.017% over 10M samples, right at the expected sampling noise
- Self-checking unit tests and an automated RTL-vs-model comparison on every push

**3. Low-latency FPGA systems: [Aegis](https://github.com/juliengaius/aegis)**\
A SystemVerilog market-data and pre-trade risk pipeline for the AMD Kria KR260.
- 2-cycle packet-to-top-of-book latency at one packet per clock
- Sequence-gap detection and locked/crossed-market protection
- 30 self-checking checks across 5 testbenches, run automatically on every push
- Design decisions written up as ADRs, e.g. why prices use NASDAQ ITCH's 4-decimal fixed-point format

---

### Tools

**RTL & FPGA:** SystemVerilog, Verilog, Vivado/Vitis, XSim, ModelSim, Icarus Verilog, AMD Kria KR260, Intel Cyclone V\
**Board-level:** Altium, power regulation, CAN, I2C, bench validation\
**Verification:** self-checking testbenches, bit-exact C reference models, CI with GitHub Actions\
**Software:** C/C++, Python, MATLAB, Linux

[LinkedIn](https://linkedin.com/in/julien-gaius-0a8b362a7)

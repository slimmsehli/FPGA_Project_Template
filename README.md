# Project Name
> Short one-line description of what this project does.

![Status](https://img.shields.io/badge/status-in_progress-yellow)
![Board](https://img.shields.io/badge/board-Zybo_Z7-blue)
![Tool](https://img.shields.io/badge/tool-Vivado_2024-orange)
![Language](https://img.shields.io/badge/HDL-SystemVerilog-green)

---

## Overview

Describe the project in 2–3 sentences. What problem does it solve? What does it implement? Why is it interesting from an engineering perspective?

---

## Block Diagram

> Replace with your actual block diagram image.

```
┌─────────────┐       ┌─────────────┐       ┌─────────────┐
│   Input IF  │──────▶│  Core Logic │──────▶│  Output IF  │
└─────────────┘       └─────────────┘       └─────────────┘
```

![Block Diagram](docs/block_diagram.png)

---

## Features

- Feature one
- Feature two
- Feature three

---

## Repository Structure

```
.
├── docs/
│   ├── design_spec.md        # Design specification and architecture decisions
│   ├── block_diagram.png     # System block diagram
│   └── timing_analysis.md    # Timing closure notes and analysis
├── rtl/                      # Synthesizable HDL source files
├── tb/                       # Testbenches and simulation models
├── constraints/
│   └── zybo_z7.xdc           # Vivado constraints (timing + I/O)
├── sim/
│   └── screenshots/          # Simulation waveform screenshots
├── impl/
│   └── reports/              # Vivado utilization, timing, and power reports
├── scripts/
│   └── build.tcl             # Tcl script to recreate the Vivado project
└── README.md
```

---

## Specifications

| Parameter        | Value         |
|-----------------|---------------|
| Target Board    | Zybo Z7-20    |
| FPGA Device     | XC7Z020-1CLG400C |
| Clock Frequency | XX MHz        |
| HDL Language    | SystemVerilog |
| Vivado Version  | 2024.x        |

---

## Simulation Results

Testbench covers the following scenarios:

- Scenario 1 — description
- Scenario 2 — description
- Scenario 3 — description (corner case)

Simulation waveforms are available in `sim/screenshots/`.

![Simulation Waveform](sim/screenshots/waveform.png)

---

## Synthesis & Implementation Results

Full Vivado reports are available in `impl/reports/`.

### Resource Utilization

| Resource | Used | Available | Utilization |
|---------|------|-----------|-------------|
| LUT     | —    | 53,200    | —           |
| FF      | —    | 106,400   | —           |
| BRAM    | —    | 140       | —           |
| DSP     | —    | 220       | —           |

### Timing Summary

| Path Group | WNS (ns) | WHS (ns) | Status |
|-----------|----------|----------|--------|
| clk       | —        | —        | ✅ Met  |

> Timing was closed at XX MHz with no negative slack. See `impl/reports/timing_summary.rpt` for full details.

---

## Hardware Testing

Tested on the Zybo Z7-20 board.

> Add a photo or short video of the design running on hardware.

![Hardware Test](docs/hardware_test.jpg)

**Test results:** Describe what was verified on hardware and how.

---

## How to Build

### Prerequisites

- Vivado 2024.x (or later)
- Zybo Z7 board files installed in Vivado

### Recreate the Vivado Project

```tcl
# In Vivado Tcl Console or from terminal:
vivado -mode batch -source scripts/build.tcl
```

This will recreate the full project, including sources, constraints, and run settings.

### Run Simulation

```tcl
# After opening the project in Vivado
launch_simulation
run all
```

### Synthesize and Implement

```tcl
launch_runs synth_1 -jobs 4
wait_on_run synth_1
launch_runs impl_1 -to_step write_bitstream -jobs 4
wait_on_run impl_1
```

---

## Design Notes

Document any non-obvious architecture decisions here. For example:

- Why a particular encoding was chosen
- How clock domain crossings are handled
- Any known limitations or areas for future improvement

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Author

**Your Name**
FPGA Design Engineer
[GitHub](https://github.com/yourusername) · [LinkedIn](https://linkedin.com/in/yourprofile)

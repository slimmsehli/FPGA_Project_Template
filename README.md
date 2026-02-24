# Template
This is a generic template for FPGA Projects 

---

## Repository Structure

```
.
├── docs/
│   ├── design_spec.md        # Design specification and architecture decisions
│   └── block_diagram.png     # System block diagram
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

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Author

**Slim Msehli**
FPGA Design Engineer
[GitHub](https://github.com/slimmsehli) · [LinkedIn](https://linkedin.com/in/slimmsehli)

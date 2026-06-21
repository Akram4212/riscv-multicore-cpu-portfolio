# riscv-multicore-cpu-portfolio
Multicore RISC-V CPU in SystemVerilog with cache/memory hierarchy, LR/SC hardware support, benchmarking, and FPGA performance/resource analysis.

# Multicore RISC-V CPU Design and Performance Analysis

This project compares four RISC-V processor architectures implemented and evaluated in Purdue ECE 437:

- Single-cycle processor
- Five-stage pipelined processor
- Pipelined processor with cache hierarchy
- Multicore processor with shared-memory behavior

The goal was to evaluate performance, memory-latency sensitivity, and FPGA resource tradeoffs across different architectural stages.

## Key Results

At memory latency LAT = 6:

| Design | Max Frequency | Execution Time | Slice LUTs |
|---|---:|---:|---:|
| Single-Cycle | 40.49 MHz | 682.34 µs | 1,504 |
| Pipeline, No Cache | 91.28 MHz | 416.87 µs | 1,820 |
| Pipeline with Cache | 92.64 MHz | 167.66 µs | 3,223 |
| Multicore | 77.68 MHz | 140.55 µs | 7,682 |

The multicore design achieved a 1.19× speedup over the sequential cached pipeline baseline at LAT = 6, while the cached pipeline provided the best performance/resource balance.

## My Contributions

- Single-cycle architecture
- Hazard unit logic
- Bus control design
- Multicore benchmarking
- LR/SC hardware implementation

## Full Report

See: `docs/Multicore_RISC-V_CPU_Final_Report.pdf`

## License

This portfolio project, including the report, diagrams, and documentation, is licensed under CC BY-NC 4.0. Source code is not included in this public repository.
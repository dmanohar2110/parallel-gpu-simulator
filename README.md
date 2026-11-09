# A Deterministic Parallel Simulator of a Coherent Multi-SM GPU
Team Members: Devika Manohar (dmanohar), Barbara Zhuo (jiayizhu)

Project Summary: We plan to build a simulator of a multi-SM GPU’s memory system (SMs, crossbar, L2 slices, DRAM) and parallelize the simulator itself. Threads will simulate independently for windows as long as the interconnect latency, then synchronize, so the results exactly match a sequential version. We will run it with C++ threads (OpenMP) on the 8-core GHC machines and the 128-core PSC Bridges-2 nodes.

# A Deterministic Parallel Simulator of a Coherent Multi-SM GPU
Team Members: Devika Manohar (dmanohar), Barbara Zhuo (jiayizhu)

## Project Summary: 
We plan to build a simulator of a multi-SM GPU’s memory system (SMs, crossbar, L2 slices, DRAM) and parallelize the simulator itself. Threads will simulate independently for windows as long as the interconnect latency, then synchronize, so the results exactly match a sequential version. We will run it with C++ threads (OpenMP) on the 8-core GHC machines and the 128-core PSC Bridges-2 nodes.

## Design Overview: 


## Project Timeline

| Dates | Task | Person in charge |
| --- | --- | --- |
| Nov 23rd - Nov 25th | Write 3-4 more small hand-written traces (for fences, atomics, and several SMs sharing lines) and check them by hand | Devika |
| | Work on initial logic for parallel engine by using lockstep loop and OpenMP threads to distribute the SM and L2 cache work | Barbara |
| Nov 26th - Nov 27th | Make 3-4 larger traces that will be used to measure speedup | Devika |
| | Finish parallel engine and debug | Devika |
| Nov 28th - Nov 30th | Add timers for the parallel engine per-thread behavior (like each thread’s time spent simulating, waiting at barriers, and passing messages) | Barbara |
| | Build a checker that compares parallel results to the sequential results and verify that the initial parallel version matches the sequential one for 1, 2, 4, 8 threads | Barbara |
| Dec 1st - Dec 3rd | If everything is okay with the lockstep version, try to implement conservative lookahead where threads simulate a window as long as the crossbar latency on their own, then swap messages at a barrier (stretch goal) | Devika and Barbara |
| Dec 4th - Dec 5th | If lookahead is working, then verify that it matches the sequential results on all traces at 1-8 threads. (Have a finished working parallel implementation) | Devika and Barbara |
| Dec 6th - Dec 10th | Make speedup graphs and time-breakdown graphs | Barbara |
| | Finish report (submit by 10th) and prepare poster session materials | Devika and Barbara |
| Dec 11th | Present at the poster session | Devika and Barbara |

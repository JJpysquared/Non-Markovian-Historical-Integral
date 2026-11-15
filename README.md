# Non-Markovian Reciprocal History Integral (NMRHI) Control Suite

This repository contains the performance benchmark validation suite for the **Non-Markovian Reciprocal History Integral (NMRHI)** quantum network control architecture. 
The system benchmarks active error-correction and state-stabilization performance against traditional industrial PID baselines under high-frequency noise and catastrophic hardware gate faults.

## Performance Benchmark Results

The system was evaluated using a coupled 3-qubit network governed by a Bloch-Lindblad simulator. The network was subjected to an extreme composite noise profile alongside a 
catastrophic structural breakdown ("Gate Fault Event") where Qubit 2 was completely disabled at t = 10 ns.

### Steady-State Error Variance Profile
Metrics evaluate the control engines under high-frequency environmental noise tracking a steady state target horizon (y = 0.6).

| Control Engine Architecture | Steady-State Error Offset | Tracking Variance (σ) | Recovery Window (Post-Fault) |
| :--- | :---: | :---: | :---: |
| **Industrial PID Baseline** | 0.142580 | 0.287410 | Divergent (Failed to Re-lock) |
| **NMRHI Framework (Ours)** | **0.000340** | **0.008450** | **< 3.0 Nanoseconds** |

### Key Benchmark Takeaways
* **Noise Suppression:** The NMRHI control core registers a massive reduction in tracking error variance, keeping system fluctuations within a tight operational band (σ < 0.01).
* **Fault Isolation:** Following the total hardware collapse of Qubit 2 at t = 10 ns, the surrounding NMRHI loops completely isolated the dead node's cross-talk, returning the remaining channels to target thresholds in under 3 nanoseconds.
* **PID Fragmentation:** Under identical stress profiles, the memoryless PID logic entered persistent overcorrection cycles, failing to stabilize the network channels post-fault.

---


For serious inquiries see contact below
https://www.linkedin.com/in/juan-de-los-santos-39591b2a3/

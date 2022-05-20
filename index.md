---
title: MSCCL Leaderboard
---

**This site is under construction.**

[Microsoft Collective Communication Library (MSCCL)](https://github.com/microsoft/msccl) is a platform to execute custom
collective communication algorithms for multiple accelerators supported by Microsoft Azure. MSCCL's enables hardware and
application specific optimizations that can deliver huge speedups over unspecialized communication algorithms.

This page show the speedup given by switching to [MSCCL](https://github.com/microsoft/msccl) from [NCCL](https://github.com/NVIDIA/nccl). To get these speedups in your Microsoft Azure workload
follow [the instructions in msccl-tools](https://github.com/microsoft/msccl-tools#readme).

# Speedups

{% include_relative speedups_table.md %}

The graphs in the table above show the speedup on the Y axis for a range of sizes on the X axis. Each graph shows the
speedup for a specific hardware configuration and collective operation. For example, the graph in the "NDv4" row and
"Allreduce" column compares the performance for running the [Allreduce
collective](https://en.wikipedia.org/wiki/Collective_operation#All-Reduce_[5]) with a single [Azure NDv4 VM containing 8
NVIDIA A100 GPUs](https://docs.microsoft.com/en-us/azure/virtual-machines/nda100-v4-series).

# Methods

These speedups were produced by running the relevant benchmarks from [nccl-tests](https://github.com/NVIDIA/nccl-tests)
on the target hardware configuration for MSCCL, with the algorithms available in [msccl-tools](https://github.com/microsoft/msccl-tools#readme) and NCCL {{ site.content.baseline-nccl-version }}.
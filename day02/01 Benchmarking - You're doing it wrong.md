Benchmarking: You're doing it wrong
===================================

Aysylu Greenberg
google
@aysylu22

- To write a good benchmark, it needs to be a fullstack (from frontend all the way to the OS level, hardware, network, and user level)
- Benchmark
    + how fast
    + your process vs goal
    + your process vs best practice

## How not to write benchmark
- Common benchmark:
    + Image access from server 1000 times, measure latency, start measuring immediately, run 3 times, find mean in dev environment.
    + What's wrong? Cache is everywhere
    + Caches in proc, depending on number of elements (L1, L2, L3 cache)
- Warmup & Timing
    + When you run your benchmark matters a lot
    + Don't start measuring immediately.
- Periodic interference
- Different specs in test and prod machines
- Power mode changes (processor throttling)
    + There's a way to detect that.
- Statistics: Taking too few samples
    + A good sample size: when the median and the decaying median is stable and 
- Non gaussian. Finding mean is not enought, but also median and distribution
- Multimodal distribution
    + Using 50% and 99% is not enough, see the histogram and plot the histogram.
- Outliers
    + By measuring outliers, we can see what's wrong.
    + 1 persen of outlier become a problem when everyone is affected by that (e.g.: 1 image of 100 images loads slow, but everyone affected by that)
- Premature optimization
- Unrepesentative workloads
    + In real life, other service may take up resources
- Memory pressure
    + garbage collection, you want to know when it happens?

## How to become less wrong
- User actions matters. How the user will use the application.
- Benchmark doesn't tell us A is better than B, it only tell us it's better at a scenario.
- Profiling.
- Code instrumentation.
    + Record time at the begining at a function and the end of all function.
    + Aggregate over logs.
- Traces: when a request come, record, how long it take to process that and analyse.
- Microbenchmarking: Blessing and 
    + quick & cheap
    + choose your N wisely.
    + Measure side effect.
    + Beware of clock resolution (milisecond or microsecond?)
    + Dead code elimination.
    + Constant work per iteration.

## Takeway
- Cache is all the way down.
- Outliers are commonly dismissed. Served as a strong signal of what went wrong.
- Workload.

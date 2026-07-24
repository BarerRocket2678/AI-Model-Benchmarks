# AI-Model-Benchmarks
Score results of models I can run using BenchLocal, which can be found [here](https://github.com/stevibe/BenchLocal)

# Notes and Observations
- I would reccomend setting a max tokens value when benchmarking. Sometimes the model can continue to generate indefinately after a benchmark finished when using the parallel per model run mode. You can set this value to your tokens generated per second times 300 plus some headroom, since by default BenchLocal has a timeout set at 5 minutes.
- I would reccomend running both CLI-40 and HermesAgent-20 in serial mode since they tend to timeout unless your tokens per second is above around 40.

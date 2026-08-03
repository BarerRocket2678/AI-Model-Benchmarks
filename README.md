# AI-Model-Benchmarks
Score results of models I can run using BenchLocal, which can be found [here](https://github.com/stevibe/BenchLocal)

# Agentic-score
This is a score to attempt to determine how well a model can handle agentic tasks. It is the sum of BenchLocal's many agentic benchmarks, where more difficult benchmarks get more weight. The equation for this score is:
``` ToolCall-15 + InstructFollow-15 + DataExtract-15 + StructOutput-15 + 2 * HermesAgent-20 + 2 * PromptAuthority-15 + 3 * CLI-40 ```
# Notes and Observations
- I would recommend setting a max tokens value when benchmarking. Sometimes the model can continue to generate indefinitely after a benchmark finished when using the parallel per model run mode. You can set this value to your tokens generated per second times 300 plus some headroom, since by default BenchLocal has a timeout set at 5 minutes.
- I would recommend running both CLI-40 and HermesAgent-20 in serial mode since they tend to timeout unless your tokens per second is above around 40.

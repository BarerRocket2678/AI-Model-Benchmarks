# AI-Model-Benchmarks
Score results of models I can run using BenchLocal, which can be found [here](https://github.com/stevibe/BenchLocal)

# Agentic-score
This is a score to attempt to determine how well a model can handle agentic tasks. It is the sum of BenchLocal's many agentic benchmarks, where more difficult benchmarks get more weight. The equation for this score is:
``` ToolCall-15 + InstructFollow-15 + DataExtract-15 + StructOutput-15 + 2 * HermesAgent-20 + 2 * PromptAuthority-15 + 3 * CLI-40 ```

# Why the focus on Agentic performance?
Local open source models have gotten very smart as of recent. However, if the model cannot apply that intelligence due to poor performance in a workflow or harness, you might be better of with a dumber model that can properly utilize either. Plus, proper harness utilization can significantly improve a model's base abilities.

# Notes and Observations
- I would recommend setting a max tokens value when benchmarking. Sometimes the model can continue to generate indefinitely after a benchmark finished when using the parallel per model run mode. You can set this value to your tokens generated per second times 300 plus some headroom, since by default BenchLocal has a timeout set at 5 minutes.
- I would recommend running both CLI-40 and HermesAgent-20 in serial mode since they tend to timeout unless your tokens per second is above around 40.
- If you come across a child model with no listed sampling parameters, I would recommend running the model with the same sampling parameters as the parent model.

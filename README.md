# AI-Model-Benchmarks
Score results of models I can run using BenchLocal, which can be found [here](https://github.com/stevibe/BenchLocal)

# Agentic-score
This is a score used to determine how well a model can handle agentic tasks. It is the sum of BenchLocal's many agentic benchmarks, where more difficult benchmarks get more weight. The equation for this score is:
``` ToolCall-15 + InstructFollow-15 + DataExtract-15 + StructOutput-15 + 2 * HermesAgent-20 + 2 * PromptAuthority-15 + 3 * CLI-40 ```
# QnA
### Why the focus on Agentic performance?
Local open source models have gotten very smart as of recent. However, if the model cannot apply that intelligence due to poor performance in a workflow or harness, you might be better of with a dumber model that can properly utilize either. Plus, proper harness utilization can significantly improve a model's base abilities.

### How do you choose the model quantization?
I have 32GB VRAM, so the mode must fit in that plus the KV cache. I aim to use as good of a quaint as possible, but I decided not to exceed Q6_K for any models since there isn't much point in going higher than that. Expect quaints to mostly be in the Q4_K_M to Q6_K range.

### Why limit the output tokens to 16384?
I have found that models which generate more than about 8000 tokens tend to either loop forever or generate upwards of 30,000 tokens per task. In order to combat this, I set a generous max token limit and set the model timeout so that it hits the token limit before the timeout limit. In real life scenarios, most would not likely prefer a 4x slowdown for what is probably a small increase in model intelligence.

# Notes and Observations
- I would recommend setting a max tokens value when benchmarking. Sometimes the model can continue to generate indefinitely after a benchmark finished when using the parallel per model run mode. You can set this value to your tokens generated per second times 300 plus some headroom, since by default BenchLocal has a timeout set at 5 minutes.
- I would recommend running both CLI-40 and HermesAgent-20 in serial mode since they tend to timeout unless your tokens per second is above around 40.
- If you come across a child model with no listed sampling parameters, I would recommend running the model with the same sampling parameters as the parent model.
- Make sure to note that greedy decoding (temp = 0) is enabled by default in BenchLocal and MUST be changed inside of the software, as it overrides the server defaults.

# [LFM2.5-8B-A1B](https://huggingface.co/LiquidAI/LFM2.5-8B-A1B)
- 8.3B total parameters
- 1.5B active parameters
- Quantization: [APEX I-Quality](https://huggingface.co/mudler/LFM2.5-8B-A1B-APEX-GGUF)
### llama.cpp Parameters:
```
temp = 0.2
repeat-penalty = 1.05
device = ROCm0
no-mmap = true
ngl = 999
fa = on
b = 16384
ub = 2048
parallel = 4
```
### Hardware: 
Radeon R9700 AI PRO 32GB
### BenchLocal settings:
- Runs: 9x
- Run mode: Parallel per model
---
### Results:
| Test                     | Pass | Partial | Fail | Score |
| ------------------------ | ---- | ------- | ---- | ----- |
| ToolCall-15 v1.0.1       | 1    | 0       | 2    | 87    |
| HermesAgent-20 v1.0.0    | 2    | 1       | 17   | 41    |

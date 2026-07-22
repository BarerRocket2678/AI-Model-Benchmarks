# [LFM2.5-8B-A1B](https://huggingface.co/LiquidAI/LFM2.5-8B-A1B)
- 8.3B total parameters
- 1.5B active parameters
- Quantization: [APEX I-Quality](https://huggingface.co/mudler/LFM2.5-8B-A1B-APEX-GGUF)
### llama.cpp Parameters:
```
temp = 0.2
n = 16384
```
### Hardware: 
Radeon R9700 AI PRO 32GB
### BenchLocal settings:
- Runs: 9x
- Run mode: Parallel per model
---
### Results:
| Test                      | Scenarios | Pass | Partial | Fail | Score |
| ------------------------- | --------- | ---- | ------- | ---- | ----- |
| InstructFollow-15 v1.0.0  | 15        | 11   | 2       | 2    | 88    |
| ToolCall-15 v1.0.1        | 15        | 1    | 0       | 2    | 87    |
| DataExtract-15 v1.0.0     | 15        | 4    | 6       | 5    | 74    |
| StructOutput-15 v1.0.0    | 15        | 3    | 9       | 3    | 74    |
| BugFind-15 v1.0.1         | 15        | 6    | 4       | 5    | 62    |
| ReasonMath-15 v1.0.0      | 15        | 8    | 1       | 6    | 51    |
| HermesAgent-20 v1.0.0     | 20        | 2    | 1       | 17   | 41    |
| PromptAuthority-15 v1.0.0 | 40        | 6    | 0       | 9    | 40    |
| CLI-40 v1.0.2             | 40        | 4    | 0       | 36   | 18    |

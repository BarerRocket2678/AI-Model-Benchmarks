# [LFM2.5-8B-A1B](https://huggingface.co/LiquidAI/LFM2.5-8B-A1B)
- 8.3B total parameters
- 1.5B active parameters
- Quantization: [APEX I-Quality](https://huggingface.co/mudler/LFM2.5-8B-A1B-APEX-GGUF)
### llama.cpp Parameters:
```
jinja = true
temp = 0.2
top-k = 80
repeat-penalty = 1.05
n = 16384
```
### Hardware: 
Radeon R9700 AI PRO 32GB
### BenchLocal settings:
- Runs: 9x
---
### Results:
| Test                      | Scenarios | Pass | Partial | Fail | Score |
| ------------------------- | --------- | ---- | ------- | ---- | ----- |
| InstructFollow-15 v1.0.0  | 15        | 10   | 3       | 2    | 86    |
| ToolCall-15 v1.0.1        | 15        | 11   | 2       | 2    | 80    |
| DataExtract-15 v1.0.0     | 15        | 4    | 8       | 3    | 77    |
| StructOutput-15 v1.0.0    | 15        | 4    | 7       | 4    | 73    |
| ReasonMath-15 v1.0.0      | 15        | 10   | 1       | 4    | 67    |
| BugFind-15 v1.0.1         | 15        | 7    | 2       | 6    | 64    |
| HermesAgent-20 v1.0.0     | 20        | 4    | 2       | 14   | 53    |
| PromptAuthority-15 v1.0.0 | 40        | 7    | 0       | 8    | 47    |
| CLI-40 v1.0.2             | 40        | 3    | 0       | 37   | 24    |

### Agentic-score: 588

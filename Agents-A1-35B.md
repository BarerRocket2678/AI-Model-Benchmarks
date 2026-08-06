# [Agents-A1-35B](https://huggingface.co/InternScience/Agents-A1)
- 35B total parameters
- 3B active parameters
- Quantization: [APEX I-Quality](https://huggingface.co/SC117/Agents-A1-MTP-APEX-GGUF)
### llama.cpp Parameters:
```
jinja = true
temp = 0.85
top-k = 20
top-p = 0.95
repeat-penalty = 1.0
presence-penalty = 1.1
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
| InstructFollow-15 v1.0.0  | 15        | 13   | 2       | 0    | 97    |
| ToolCall-15 v1.0.1        | 15        | 15   | 0       | 0    | 100   |
| StructOutput-15 v1.0.0    | 15        | 12   | 3       | 0    | 98    |
| BugFind-15 v1.0.1         | 15        | 12   | 1       | 2    | 89    |
| HermesAgent-20 v1.0.0     | 20        | 10   | 1       | 9    | 75    |
| DataExtract-15 v1.0.0     | 15        | 8    | 4       | 3    | 83    |
| CLI-40 v1.0.2             | 40        | 18   | 8       | 14   | 73    |
| ReasonMath-15 v1.0.0      | 15        | 12   | 0       | 3    | 78    |
| PromptAuthority-15 v1.0.0 | 15        | 10   | 0       | 5    | 67    |

### Agentic-score: 881

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
| ToolCall-15 v1.0.1        | 15        | 14   | 0       | 1    | 93    |
| StructOutput-15 v1.0.0    | 15        | 10   | 4       | 1    | 91    |
| BugFind-15 v1.0.1         | 15        | 11   | 1       | 3    | 79    |
| HermesAgent-20 v1.0.0     | 20        | 11   | 2       | 7    | 78    |
| DataExtract-15 v1.0.0     | 15        | 8    | 4       | 3    | 77    |
| CLI-40 v1.0.2             | 40        | 20   | 6       | 14   | 68    |
| ReasonMath-15 v1.0.0      | 15        | 11   | 0       | 4    | 64    |
| PromptAuthority-15 v1.0.0 | 15        | 9    | 0       | 6    | 60    |

### Agentic-score: 838

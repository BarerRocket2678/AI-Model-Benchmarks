# [Ornith-1.0-35B](https://huggingface.co/deepreinforce-ai/Ornith-1.0-35B)
- 35B total parameters
- 3B active parameters
- Quantization: [APEX I-Quality](https://huggingface.co/SC117/Ornith-1.0-35B-MTP-APEX-GGUF)
### llama.cpp Parameters:
```
jinja = true
reasoning-preserve = true
temp = 0.6
top-p = 0.95
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
| ToolCall-15 v1.0.1        | 15        | 15   | 0       | 0    | 100   |
| InstructFollow-15 v1.0.0  | 15        | 13   | 2       | 0    | 97    |
| BugFind-15 v1.0.1         | 15        | 11   | 2       | 2    | 88    |
| HermesAgent-20 v1.0.0     | 20        | 13   | 2       | 5    | 85    |
| DataExtract-15 v1.0.0     | 15        | 9    | 2       | 4    | 82    |
| StructOutput-15 v1.0.0    | 15        | 10   | 3       | 2    | 85    |
| ReasonMath-15 v1.0.0      | 15        | 13   | 0       | 2    | 82    |
| PromptAuthority-15 v1.0.0 | 15        | 10   | 0       | 5    | 67    |
| CLI-40 v1.0.2             | 40        | 15   | 7       | 18   | 65    |

### Agentic-score: 863

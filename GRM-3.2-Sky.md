# [GRM-3.2-Sky](https://huggingface.co/OrionLLM/GRM-3.2-Sky)
- 35B total parameters
- 3B active parameters (if applicable)
- Quantization: [APEX I-Quality](https://huggingface.co/el4/GRM-3.2-Sky-ONYX-GGUF)
### llama.cpp Parameters:
```
jinja = true
reasoning-preserve = true
temp = 0.6
top-p = 0.95
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
| ToolCall-15 v1.0.1        | 15        | 14   | 1       | 0    | 97    |
| BugFind-15 v1.0.1         | 15        | 13   | 0       | 2    | 91    |
| ReasonMath-15 v1.0.0      | 15        | 13   | 0       | 2    | 81    |
| HermesAgent-20 v1.0.0     | 20        | 11   | 3       | 6    | 80    |
| PromptAuthority-15 v1.0.0 | 15        | 10   | 0       | 5    | 67    |
| StructOutput-15 v1.0.0    | 15        | 8    | 2       | 5    | 67    |
| CLI-40 v1.0.2             | 40        | 15   | 5       | 20   | 61    |
| DataExtract-15 v1.0.0     | 15        | 3    | 3       | 9    | 50    |

### Agentic-score: 788
# WARNING: The DataExtract benchmark for this model is unusually low. This could cause issues in agentic workflows where precise data extraction is requred.

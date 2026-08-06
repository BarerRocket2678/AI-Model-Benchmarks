# [Qwythos-9B-v2](https://huggingface.co/empero-ai/Qwythos-9B-v2)
- 9B total parameters
- Quantization: [Q6_K](https://huggingface.co/empero-ai/Qwythos-9B-v2-GGUF)
### llama.cpp Parameters:
```
jinja = true
temp = 0.6
top-p = 0.95
top-k = 20
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
| InstructFollow-15 v1.0.0  | 15        | 11   | 3       | 1    | 92    |
| BugFind-15 v1.0.1         | 15        | 8    | 5       | 2    | 79    |
| HermesAgent-20 v1.0.0     | 20        | 10   | 3       | 7    | 77    |
| DataExtract-15 v1.0.0     | 15        | 5    | 6       | 4    | 69    |
| StructOutput-15 v1.0.0    | 15        | 5    | 6       | 4    | 67    |
| ReasonMath-15 v1.0.0      | 15        | 7    | 4       | 4    | 65    |
| CLI-40 v1.0.2             | 40        | 12   | 2       | 26   | 54    |
| PromptAuthority-15 v1.0.0 | 15        | 47   | 0       | 8    | 47    |

### Agentic-score: 738

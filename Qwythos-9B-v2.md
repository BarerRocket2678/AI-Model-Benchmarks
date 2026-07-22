# [Qwythos-9B-v2](https://huggingface.co/empero-ai/Qwythos-9B-v2)
- 9B total parameters
- Quantization: [Q6_K](https://huggingface.co/empero-ai/Qwythos-9B-v2-GGUF)
### llama.cpp Parameters:
```
temp = 0.6
top-p = 0.95
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
| ToolCall-15 v1.0.1        | 15        | 15   | 0       | 0    | 100   |
| InstructFollow-15 v1.0.0  | 15        | 12   | 2       | 1    | 93    |
| BugFind-15 v1.0.1         | 15        | 9    | 3       | 3    | 79    |
| StructOutput-15 v1.0.0    | 15        | 7    | 5       | 3    | 77    |
| ReasonMath-15 v1.0.0      | 15        | 9    | 3       | 3    | 68    |
| HermesAgent-20 v1.0.0     | 20        | 4    | 1       | 15   | 34    |
| PromptAuthority-15 v1.0.0 | 15        | 3    | 0       | 12   | 20    |
| CLI-40 v1.0.2             | 40        | 0    | 0       | 40   | 14    |
| DataExtract-15 v1.0.0     | 15        | 0    | 0       | 15   | 0     |


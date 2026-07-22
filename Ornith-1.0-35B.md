# [Ornith-1.0-35B](https://huggingface.co/deepreinforce-ai/Ornith-1.0-35B)
- 35B total parameters
- 3B active parameters
- Quantization: [APEX I-Compact](https://huggingface.co/SC117/Ornith-1.0-35B-MTP-APEX-GGUF)
### llama.cpp Parameters:
```
temp = 0.6
top-p = 0.95
repeat-penalty = 1.05
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
| InstructFollow-15 v1.0.0  | 15        | 14   | 1       | 0    | 98    |
| BugFind-15 v1.0.1         | 15        | 12   | 2       | 1    | 92    |
| HermesAgent-20 v1.0.0     | 20        | 14   | 2       | 4    | 88    |
| DataExtract-15 v1.0.0     | 15        | 10   | 2       | 3    | 85    |
| StructOutput-15 v1.0.0    | 15        | 9    | 2       | 4    | 74    |
| ReasonMath-15 v1.0.0      | 15        | 12   | 0       | 3    | 73    |
| PromptAuthority-15 v1.0.0 | 15        | 10   | 0       | 5    | 67    |
| CLI-40 v1.0.2             | 40        | 18   | 6       | 16   | 66    |

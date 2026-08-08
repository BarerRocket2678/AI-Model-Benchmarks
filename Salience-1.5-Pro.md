# [Salience-1.5-Pro](https://huggingface.co/vectionlabs/Salience-1.5-Pro)
- 35B total parameters
- 3B active parameters
- Quantization: [Q4_K_M](https://huggingface.co/bartowski/vectionlabs_Salience-1.5-Pro-GGUF)
### llama.cpp Parameters:
```
jinja = true
temp = 0.85
top-p = 0.95
top_k = 20
presence_penalty = 1.1
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
| BugFind-15 v1.0.1         | 15        | 12   | 1       | 2    | 92    |
| StructOutput-15 v1.0.0    | 15        | 9    | 5       | 1    | 89    |
| HermesAgent-20 v1.0.0     | 20        | 13   | 3       | 4    | 85    |
| ReasonMath-15 v1.0.0      | 15        | 13   | 0       | 2    | 81    |
| DataExtract-15 v1.0.0     | 15        | 9    | 2       | 4    | 78    |
| CLI-40 v1.0.2             | 40        | 18   | 6       | 16   | 73    |
| PromptAuthority-15 v1.0.0 | 15        | 9    | 0       | 6    | 60    |

### Agentic-score: 873

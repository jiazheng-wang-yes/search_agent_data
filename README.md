# search_agent_data

For each attack method, there are output files and LLM-as-a-Judge results. Each model should have baseline run, with secure prompt (defense method 1) and with reflection module (defense method 2).

The poisoned QA pairs are in `./poison_fake_qa_pairs.json`
The original QA pairs are in `./qa_pairs_subset_50.json`

## Attack Success Rate (ASR) Summary

| Attack Method              | Model                       | Baseline ASR | Secure Prompt ASR | Reflection Module ASR |
|-----------------------------|-----------------------------|---------------|-------------------|------------------------|
| **simple_dos_attack**       | Qwen2.5-14B-Instruct        | 10.00%        | 0.00%             | 0.00%                  |
|                             | Qwen3-30B-A3B-Instruct-2507 | 0.00%         | 0.00%             | 0.00%                  |
|                             | gemini-2.5-flash-lite       | 28.00%        | 0.00%             | 0.00%                  |
|                             | gpt-4.1-mini                | 54.00%        | 8.00%             | 0.00%                  |
|                             | qwen2.5-3b                  | 2.00%         | 4.00%             | 0.00%                  |
|                             | qwen2.5-7b                  | 0.00%         | 0.00%             | 0.00%                  |
| **dos_injection**           | Qwen2.5-14B-Instruct        | 98.00%        | 94.00%            | 0.00%                  |
|                             | Qwen3-30B-A3B-Instruct-2507 | 18.00%        | 48.00%            | 0.00%                  |
|                             | gemini-2.5-flash-lite       | 0.00%         | 2.00%             | 0.00%                  |
|                             | gpt-4.1-mini                | 0.00%         | 0.00%             | 0.00%                  |
|                             | qwen2.5-3b                  | 88.00%        | 90.00%            | 0.00%                  |
|                             | qwen2.5-7b                  | 86.00%        | 92.00%            | 0.00%                  |
| **simple_information_leak** | Qwen2.5-14B-Instruct        | 0.00%         | 78.00%            | 0.00%                  |
|                             | Qwen3-30B-A3B-Instruct-2507 | 0.00%         | 90.00%            | 0.00%                  |
|                             | gemini-2.5-flash-lite       | 18.00%        | 70.00%            | 8.00%                  |
|                             | gpt-4.1-mini                | 32.00%        | 94.00%            | 0.00%                  |
|                             | qwen2.5-3b                  | 2.00%         | 52.00%            | 4.00%                  |
|                             | qwen2.5-7b                  | 4.00%         | 96.00%            | 0.00%                  |
| **information_leak_attack** | Qwen2.5-14B-Instruct        | 82.00%        | 88.00%            | 0.00%                  |
|                             | Qwen3-30B-A3B-Instruct-2507 | 0.00%         | 10.00%            | 0.00%                  |
|                             | gemini-2.5-flash-lite       | 0.00%         | 0.00%             | 0.00%                  |
|                             | gpt-4.1-mini                | 2.00%         | 0.00%             | 0.00%                  |
|                             | qwen2.5-3b                  | 20.00%        | 27.00%            | 0.00%                  |
|                             | qwen2.5-7b                  | 8.00%         | 6.00%             | 0.00%                  |
| **simple_two_step_attack**  | Qwen2.5-14B-Instruct        | 2.00%         | 2.00%             | 0.00%                  |
|                             | Qwen3-30B-A3B-Instruct-2507 | 0.00%         | 4.00%             | 0.00%                  |
|                             | gemini-2.5-flash-lite       | 36.00%        | 8.00%             | 0.00%                  |
|                             | gpt-4.1-mini                | 36.00%        | 14.00%            | 0.00%                  |
|                             | qwen2.5-3b                  | 76.00%        | 50.00%            | 0.00%                  |
|                             | qwen2.5-7b                  | 94.00%        | 88.00%            | 0.00%                  |
| **two_step_attack**         | Qwen2.5-14B-Instruct        | 18.00%        | 6.00%             | 0.00%                  |
|                             | Qwen3-30B-A3B-Instruct-2507 | 0.00%         | 0.00%             | 0.00%                  |
|                             | gemini-2.5-flash-lite       | 0.00%         | 0.00%             | 0.00%                  |
|                             | gpt-4.1-mini                | 0.00%         | 0.00%             | 0.00%                  |
|                             | qwen2.5-3b                  | 70.00%        | 64.00%            | 0.00%                  |
|                             | qwen2.5-7b                  | 94.00%        | 92.00%            | 0.00%                  |

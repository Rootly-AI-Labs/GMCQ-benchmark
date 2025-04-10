
# GMCQ-benchmark 🧪
GitHub Multiple Choice Questions (GMCQ) is a benchmark developed by the [Rootly AI Labs](https://labs.rootly.ai/) to evaluate a language model's ability to determine the pull request that closes a bug fix issue from a real-world GitHub repository.

We took 100 closed issues with the bug label from the Mastodon Github repository, along with the pull requests that closed the issue. 

## Task Format

Given a GitHub issue title and description, without any additional context, the model must determine the correct pull request that closed the issue.

There is one correct issue and three false choices that are pull requests from the same repository that closed different issues.

The pull request description contains the filenames that were changed and the code patch that changed.

```
Task description:
<GitHub issue title and description>

---

Choice A:

<filenames and code patches>

---

Choice B:

<filenames and code patches>

---

Choice C:

<filenames and code patches>

---

Choice D:

<filenames and code patches>

```

## Evaluation Results

We obtained the following results on version 0.1 of GMCQ using the OpenAI/evals GitHub repository.

| Model Name | Accuracy |
| --- | --- | 
| GPT-4o mini | 0.829 ± 0.042 |
| Llama-3.1 8B-instant (Groq) | 0.341 ± 0.052 |
| Llama-3.3 70B-versatile (Groq) | 0.720 ± 0.050 |
| Llama-4 Scout (Groq) | 0.598 ± 0.053 |
| Llama-4-Maverick (Groq) | 0.695 ± 0.051 |
| Qwen-2.5-Coder-32B (Groq) | 0.902 ± 0.034 |
| Qwen-2.5-32B (Groq) | 0.793 ± 0.044 |

## About the Rootly AI Labs
This project was developed by the [Rootly AI Labs](https://labs.rootly.ai/). The AI Labs is building the future of system reliability and operational excellence. We operate as an open-source incubator, sharing ideas, experimenting, and rapidly prototyping. We're committed to ensuring our research benefits the entire community.
![Rootly AI logo](https://github.com/Rootly-AI-Labs/EventOrOutage/raw/main/rootly-ai.png)

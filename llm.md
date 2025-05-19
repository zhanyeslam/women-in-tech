layout: page
title: LLM Comparison
permalink: /llm.md/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/jekyll-theme-cayman/0.1.1/jekyll-theme-cayman.min.css">
<style>
  body { max-width: 800px; margin: auto; padding: 2rem; }
  table { width: 100%; border-collapse: collapse; margin: 1em 0; }
  th, td { padding: 0.6em; border: 1px solid #ccc; }
</style>

# 🤖 Prompting with Language Models (LLMs)

In this section, we explore how two different LLMs — **GPT-4 (ChatGPT)** and **GitHub Copilot** — respond to the same prompts related to the topic *Women in Tech*. We applied **three prompting techniques**: zero-shot, one-shot, and few-shot.

---

## 🧠 Prompting Technique 1: Zero-shot

### Prompt
> List 5 influential women in artificial intelligence with short bios.

### Comparison Table

| Name               | GPT-4 Output                                                                                   | GitHub Copilot Output             |
|--------------------|-----------------------------------------------------------------------------------------------|-----------------------------------|
| **Fei-Fei Li**      | Stanford professor, pioneer in computer vision and co-director of HAI                         | Computer vision expert            |
| **Joy Buolamwini**  | Founder of the Algorithmic Justice League, works on AI fairness                              | AI bias researcher                |
| **Daphne Koller**   | Co-founder of Coursera, expert in probabilistic models                                        | Machine learning                  |
| **Timnit Gebru**    | AI ethics researcher, co-founder of Black in AI                                               | AI ethics                         |
| **Rana el Kaliouby**| Co-founder of Affectiva, expert in emotion AI                                                 | Emotion recognition               |

**Observation:**  
GPT-4 gave complete, contextual bios. Copilot returned short, functional descriptors. GPT-4 output is better for readers unfamiliar with the figures.

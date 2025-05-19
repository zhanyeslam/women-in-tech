---
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

In this section, we explore how two different LLMs — **GPT-4 (ChatGPT)** and **GitHub Copilot** — respond to the same prompts related to the topic *Women in Tech*. We applied **three prompting techniques**: zero-shot, **chain-of-thought (CoT)**, and few-shot.

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

---

## 🧠 Prompting Technique 2: Chain-of-Thought (CoT)

### Prompt
> Ada Lovelace is considered a pioneer in computing.  
> Let’s now think of modern women contributing to AI.  
> First, identify their area of expertise.  
> Then explain how they apply AI in that domain.  
> Finally, summarize each contribution in one sentence.

### Comparison Table

| Name               | GPT-4 Output                                                                 | GitHub Copilot Output         |
|--------------------|------------------------------------------------------------------------------|-------------------------------|
| **Chelsea Finn**    | Expert in robotics and meta-learning. Applies AI to train robots across tasks. “Chelsea Finn develops AI systems that allow robots to learn from few examples.” | Robotics and ML               |
| **Dina Machuve**    | Works in agriculture and AI. Uses machine learning to predict crop diseases. “Dina Machuve applies AI to solve agricultural challenges in Africa.” | *(Not included)*              |
| **Kate Crawford**   | Specializes in AI ethics and its societal impact. Analyzes bias in large-scale models. “Kate Crawford investigates how AI affects social justice.” | AI ethics                     |
| **Joy Buolamwini**  | Focuses on facial recognition bias. Created Algorithmic Justice League. “Joy Buolamwini challenges bias in AI systems.” | Algorithmic fairness          |

**Observation:**  
GPT-4 followed the step-by-step reasoning well — domain → application → contribution.  
Copilot produced flat outputs, ignoring the CoT structure and skipping logic progression.

---

## 🧠 Prompting Technique 3: Few-shot

### Prompt
> Example 1: Ada Lovelace – Pioneer in computing.  
> Example 2: Margaret Hamilton – Led software engineering for Apollo missions.  
> Example 3: Fei-Fei Li – Computer vision at Stanford.  
> Now add 3 more examples.

### Comparison Table

| Name               | GPT-4 Output                                                                                  | GitHub Copilot Output   |
|--------------------|----------------------------------------------------------------------------------------------|--------------------------|
| **Radia Perlman**   | Invented the spanning tree protocol, foundational to internet networking                    | Networking               |
| **Ginni Rometty**   | Former IBM CEO, promoted AI in enterprise                                                   | IBM CEO                  |
| **Cynthia Breazeal**| MIT researcher in social robotics and human-AI interaction                                  | Robotics                 |

**Observation:**  
GPT-4 emphasizes historical contributions and academic roles.  
Copilot reflects examples with accurate names but minimal elaboration.

---

## 🔍 Summary: GPT-4 vs Copilot

| Feature             | GPT-4 (ChatGPT)               | GitHub Copilot               |
|---------------------|-------------------------------|-------------------------------|
| Output richness     | ✅ Full bios with context       | ➖ Keywords only               |
| Accuracy            | ✅ High                        | ✅ High, but limited detail    |
| Diversity           | ✅ Global and academic breadth | ➖ Repeats popular names       |
| Prompt sensitivity  | ✅ Adapts tone and logic       | ➖ Limited flexibility         |
| Use case fit        | ✅ Best for writing and research | ✅ Best for coding and drafts  |

---

## ✅ Conclusion

GPT-4 demonstrates a strong ability to generate nuanced, detailed, and diverse content suitable for analysis and educational purposes. GitHub Copilot, on the other hand, produces accurate but minimalistic outputs — ideal for software environments and developers seeking fast completions.

Both models were effective, but GPT-4 was clearly superior for this research-driven project.

---

## 📁 Methodology & Tools

- Prompting performed manually in **ChatGPT (GPT-4)** and **Visual Studio Code (Copilot)**  
- Prompts documented in plain text  
- Analysis compiled using Markdown and structured formatting  
- GitHub Pages

---
layout: page
title: LLM Comparison
permalink: /llm.md/
---

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

---

## 🧠 Prompting Technique 2: One-shot

### Prompt
> Example: Ada Lovelace – Pioneer in computing.  
> Now list 3 modern women in AI with a short description.

### Comparison Table

| Name               | GPT-4 Output                                                                 | GitHub Copilot Output         |
|--------------------|------------------------------------------------------------------------------|-------------------------------|
| **Chelsea Finn**    | Stanford researcher in robotics and meta-learning                           | Robotics and ML               |
| **Dina Machuve**    | Applies machine learning to agriculture in Africa                           | *(Not included)*              |
| **Kate Crawford**   | Studies the societal impact of AI                                           | AI ethics                     |
| **Joy Buolamwini**  | *(Not included)*                                                            | Algorithmic fairness          |

**Observation:**  
GPT-4 shows broader geographic and academic variety.  
Copilot listed only known names, more concise but less diverse.

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
- GitHub Pages used for project website presentation

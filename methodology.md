---
layout: default
title: Methodology
permalink: /methodology.md/
---

# Methodology

This section explains the step-by-step methodology adopted in our project, combining semantic technologies with language models.

---

## 🧠 1. Identifying the Gap

We started by analyzing existing knowledge sources (e.g., Wikidata, Crunchbase) and found that women-led tech startups are often underrepresented or poorly structured.

We defined a **semantic gap** in how entities like “founder”, “startup domain”, or “impact area” are modeled.

---

## 🛠️ 2. Knowledge Graph Design

We created an RDF vocabulary (TBox) to represent:

- `ex:Woman` – a female founder  
- `ex:Startup` – a technology startup  
- `ex:impactArea` – domains like education, social inclusion, AI  
- `ex:countryOfOrigin`, `ex:operatesIn` – for geographic context  
- `ex:foundedBy` – linking founders to startups

We used real examples of women entrepreneurs to build the ABox.

---

## 🧠 3. Prompt Engineering and LLMs

We used 3 prompting techniques:

1. **Zero-shot**
2. **Few-shot**
3. **Chain-of-thought (CoT)**

These prompts were used to:

- Extract missing data from text
- Generate new RDF triples
- Classify startups by domain

We compared outputs from two LLMs:
- **OpenAI GPT-4**
- **Meta LLaMA 2**

---

## 🔁 4. SPARQL Queries

To validate and query the graph, we used SPARQL with advanced operators like:

- `OPTIONAL`, `FILTER`, `REGEX`, `UNION`, `DISTINCT`, `ORDER BY`, `LIMIT`

Queries were used to extract founders by country, startup types, and impact patterns.

(See [SPARQL & Prompts](sparql.md))

---

## 🔍 5. Evaluation and Discussion

We compared:

- **Coverage** of generated triples
- **Accuracy** of LLM-enriched data
- **Prompt effectiveness** across models

All results and issues are documented in the [Challenges](challenges.md) section.


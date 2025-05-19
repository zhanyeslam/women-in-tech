---
layout: default
title: SPARQL & Prompts
permalink: /sparql/
---

# SPARQL Queries and Prompting Techniques

This section presents all SPARQL queries used in the project with the required operators, and the prompt engineering strategies used to generate or enrich RDF data using language models.

```sparql
PREFIX ex: <http://example.org/>

SELECT DISTINCT ?founder ?startup
WHERE {
  ?founder a ex:Woman ;
           ex:founded ?startup .
}
ORDER BY ?founder
```

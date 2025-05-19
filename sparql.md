---
layout: default
title: SPARQL & Prompts
permalink: /sparql.md/
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

PREFIX ex: <http://example.org/>

SELECT ?startup
WHERE {
  ?startup a ex:Startup ;
           ex:domain ?domain .
  FILTER regex(?domain, "EdTech", "i")
}

PREFIX ex: <http://example.org/>

SELECT ?startup ?country
WHERE {
  ?startup a ex:Startup .
  OPTIONAL { ?startup ex:countryOfOrigin ?country }
}
LIMIT 10

PREFIX ex: <http://example.org/>

SELECT ?country (COUNT(?startup) AS ?total)
WHERE {
  {
    ?startup ex:countryOfOrigin ?country .
  }
  UNION
  {
    ?startup ex:operatesIn ?country .
  }
}
GROUP BY ?country
ORDER BY DESC(?total)

ex:AminaKhan a ex:Woman .
ex:Startup1 a ex:Startup ;
            ex:focus "AI" ;
            ex:locatedIn "Canada" ;
            ex:foundedBy ex:AminaKhan .


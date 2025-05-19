---
layout: default
title: SPARQL & Prompts
permalink: /sparql/
---

# SPARQL Queries and Prompting Techniques

This section presents all SPARQL queries used in the project with the required operators, and the prompt engineering strategies used to generate or enrich RDF data using language models.

PREFIX wd: <http://www.wikidata.org/entity/>
PREFIX wdt: <http://www.wikidata.org/prop/direct/>
PREFIX wikibase: <http://wikiba.se/ontology#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

```sparql
SELECT ?woman ?womanLabel ?startup ?startupLabel
WHERE {
  ?woman wdt:P31 wd:Q5 ;               # instance of human
         wdt:P21 wd:Q6581072 ;         # gender: female
         wdt:P112 ?startup .           # founder of

  ?startup wdt:P452 wd:Q627335 ;       # industry: tech startup

  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}
LIMIT 10
```

```sparql
SELECT ?startup ?startupLabel ?founder ?founderLabel
WHERE {
  ?founder wdt:P21 wd:Q6581072 ;        # gender: female
           wdt:P27 wd:Q30 ;            # country of citizenship: USA
           wdt:P112 ?startup .

  ?startup wdt:P31 wd:Q4830453 .        # instance of: business
  
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}
LIMIT 10
```

```sparql
PREFIX wd: <http://www.wikidata.org/entity/>
PREFIX wdt: <http://www.wikidata.org/prop/direct/>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

SELECT ?startup ?startupLabel ?industryLabel
WHERE {
  ?startup wdt:P31 wd:Q4830453 ;        # instance of: business
           wdt:P452 ?industry .         # industry

  FILTER(REGEX(?industryLabel, "EdTech|AI|education", "i"))

  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}
LIMIT 15
```

```sparql
PREFIX wd: <http://www.wikidata.org/entity/>
PREFIX wdt: <http://www.wikidata.org/prop/direct/>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

SELECT ?countryLabel (COUNT(?startup) AS ?total)
WHERE {
  {
    ?founder wdt:P21 wd:Q6581072 ;       # female
             wdt:P112 ?startup .
    ?founder wdt:P27 ?country .
  }
  UNION
  {
    ?startup wdt:P17 ?country .         # startup located in country
  }

  SERVICE wikibase:label { bd:serviceParam wikibase:language "en". }
}
GROUP BY ?countryLabel
ORDER BY DESC(?total)
```

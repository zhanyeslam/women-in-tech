---
title: SPARQL Explorer
permalink: /sparql/
---

# 🔍 Women in Tech – SPARQL Explorer

This section shows a **live query** to Wikidata using SPARQL.  
We explore **female founders in technology**, along with descriptions of the companies they founded.

---

## 📡 Live Query from Wikidata

<iframe
  style="width: 100%; height: 600px; border: 1px solid #ccc;"
  src="https://query.wikidata.org/embed.html#SELECT%20DISTINCT%20%3Fwoman%20%3FwomanLabel%20%3FcompanyLabel%20%3FcompanyDescription%20WHERE%20%7B%0A%20%20%3Fwoman%20wdt%3AP31%20wd%3AQ5%20%3B%20%20%20%20%20%20%20%20%23%20instance%20of%20human%0A%20%20%20%20%20%20%20%20wdt%3AP21%20wd%3AQ6581072%20%3B%20%20%20%20%20%20%20%20%23%20female%0A%20%20%20%20%20%20%20%20wdt%3AP112%20%3Fcompany%20.%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%23%20founder%20of%20company%0A%0A%20%20%3Fcompany%20wdt%3AP31%20%3Ftype%20%3B%0A%20%20%20%20%20%20%20%20schema%3Adescription%20%3FcompanyDescription%20.%0A%0A%20%20FILTER%28LANG%28%3FcompanyDescription%29%20%3D%20%22en%22%29%0A%20%20FILTER%28%3Ftype%20IN%20%28wd%3AQ4830453%2C%20wd%3AQ79913%2C%20wd%3AQ230844%2C%20wd%3AQ167037%2C%20wd%3AQ7397%29%29%20%23%20business%2C%20NGO%2C%20org%2C%20platform%2C%20tech%0A%0A%20%20FILTER%28REGEX%28%3FcompanyDescription%2C%20%22tech%7CAI%7Csoftware%7Cdigital%7CIT%7Cplatform%22%2C%20%22i%22%29%29%0A%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0ALIMIT%2030">
</iframe>

---

## 💬 Explanation

- `?woman` must be a human (`wd:Q5`) and female (`wd:Q6581072`)
- They must be a **founder** (`P112`) of a company
- That company must be of type tech/business/platform and contain **tech keywords**
- We display: woman's name, company name, and company description (in English)

---

## 🛠️ Tools Used

- [Wikidata Query Service](https://query.wikidata.org/)
- SPARQL
- GitHub Pages (static hosting)

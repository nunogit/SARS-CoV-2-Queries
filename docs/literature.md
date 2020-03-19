# Literature

These queries list the latest 10 <a name="tp1">articles</a> about a number of topics. It is
no replacement for [Scholia]() [<a href="#citeref1">1</a>],
which has a much richer overview of <a name="tp2">literature</a> on the topic. Each section
includes a link to the Scholia page for that topic. The queries used here
are very basic, and only use the 'main subject' property.

## about SARS-CoV-2

[SARS-CoV-2](https://tools.wmflabs.org/scholia/topic/Q82069695) is the name of the virus.

**SPARQL** [sparql/litSARSCoV2.rq](sparql/litSARSCoV2.code.html) ([run](https://query.wikidata.org/embed.html#SELECT%20%28MAX%28%3Fdates%29%20as%20%3Fdate%29%20%3Fwork%20%3FworkLabel%20WHERE%20%7B%0A%20%20%3Fwork%20wdt%3AP921%20wd%3AQ82069695%20.%0A%20%20OPTIONAL%20%7B%20%3Fwork%20wdt%3AP577%20%3Fdates%20.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%2Cda%2Cde%2Ces%2Cfr%2Cjp%2Cnl%2Cno%2Cru%2Csv%2Czh%22.%20%7D%0A%7D%20GROUP%20BY%20%3Fwork%20%3FworkLabel%20ORDER%20BY%20DESC%28%3Fdate%29%20LIMIT%2010%0A), [edit](https://query.wikidata.org/#SELECT%20%28MAX%28%3Fdates%29%20as%20%3Fdate%29%20%3Fwork%20%3FworkLabel%20WHERE%20%7B%0A%20%20%3Fwork%20wdt%3AP921%20wd%3AQ82069695%20.%0A%20%20OPTIONAL%20%7B%20%3Fwork%20wdt%3AP577%20%3Fdates%20.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%2Cda%2Cde%2Ces%2Cfr%2Cjp%2Cnl%2Cno%2Cru%2Csv%2Czh%22.%20%7D%0A%7D%20GROUP%20BY%20%3Fwork%20%3FworkLabel%20ORDER%20BY%20DESC%28%3Fdate%29%20LIMIT%2010%0A))

```sparql
SELECT (MAX(?dates) as ?date) ?work ?workLabel WHERE {
  ?work wdt:P921 wd:Q82069695 .
  OPTIONAL { ?work wdt:P577 ?dates . }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en,da,de,es,fr,jp,nl,no,ru,sv,zh". }
} GROUP BY ?work ?workLabel ORDER BY DESC(?date) LIMIT 10
```

This gives these 10 papers:

<table>
  <tr>
    <td><b>date</b></td>
    <td><b>work</b></td>
    <td><b>workLabel</b></td>
  </tr>
  <tr>
    <td>2020-05-17T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87461585</td>
    <td>Risk for Transportation of 2019 Novel Coronavirus Disease from Wuhan to Other Cities in China</td>
  </tr>
  <tr>
    <td>2020-05-17T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87461449</td>
    <td>Potential Presymptomatic Transmission of SARS-CoV-2, Zhejiang Province, China, 2020</td>
  </tr>
  <tr>
    <td>2020-04-01T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87461794</td>
    <td>CT Imaging of the 2019 Novel Coronavirus (2019-nCoV) Pneumonia</td>
  </tr>
  <tr>
    <td>2020-04-01T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87945074</td>
    <td>Enteric involvement of coronaviruses: is faecal–oral transmission of SARS-CoV-2 possible?</td>
  </tr>
  <tr>
    <td>2020-03-17T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87830056</td>
    <td>The proximal origin of SARS-CoV-2</td>
  </tr>
  <tr>
    <td>2020-03-17T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87943251</td>
    <td>Aerosol and Surface Stability of SARS-CoV-2 as Compared with SARS-CoV-1</td>
  </tr>
  <tr>
    <td>2020-03-16T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87789617</td>
    <td>Substantial undocumented infection facilitates the rapid dissemination of novel coronavirus (SARS-CoV2)</td>
  </tr>
  <tr>
    <td>2020-03-16T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87945075</td>
    <td>SARS-CoV-2 and COVID-19: The most important research questions</td>
  </tr>
  <tr>
    <td>2020-03-13T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q83567432</td>
    <td>Coronavirus latest: global infections surge past 30,000</td>
  </tr>
  <tr>
    <td>2020-03-12T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87675797</td>
    <td>[Recommendations for critically ill patients with COVID-19]</td>
  </tr>
</table>

## about coronaviruses

As outlined in Chapter X, SARS-Cov-2 is one of the coronaviruses that
can infect humans.

**SPARQL** [sparql/litCoronaviruses.rq](sparql/litCoronaviruses.code.html) ([run](https://query.wikidata.org/embed.html#SELECT%20%28MAX%28%3Fdates%29%20as%20%3Fdate%29%20%3Fwork%20%3FworkLabel%20WHERE%20%7B%0A%20%20%3Fwork%20wdt%3AP921%20wd%3AQ57751738%20.%0A%20%20OPTIONAL%20%7B%20%3Fwork%20wdt%3AP577%20%3Fdates%20.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%2Cda%2Cde%2Ces%2Cfr%2Cjp%2Cnl%2Cno%2Cru%2Csv%2Czh%22.%20%7D%0A%7D%20GROUP%20BY%20%3Fwork%20%3FworkLabel%20ORDER%20BY%20DESC%28%3Fdate%29%20LIMIT%2010%0A), [edit](https://query.wikidata.org/#SELECT%20%28MAX%28%3Fdates%29%20as%20%3Fdate%29%20%3Fwork%20%3FworkLabel%20WHERE%20%7B%0A%20%20%3Fwork%20wdt%3AP921%20wd%3AQ57751738%20.%0A%20%20OPTIONAL%20%7B%20%3Fwork%20wdt%3AP577%20%3Fdates%20.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%2Cda%2Cde%2Ces%2Cfr%2Cjp%2Cnl%2Cno%2Cru%2Csv%2Czh%22.%20%7D%0A%7D%20GROUP%20BY%20%3Fwork%20%3FworkLabel%20ORDER%20BY%20DESC%28%3Fdate%29%20LIMIT%2010%0A))

```sparql
SELECT (MAX(?dates) as ?date) ?work ?workLabel WHERE {
  ?work wdt:P921 wd:Q57751738 .
  OPTIONAL { ?work wdt:P577 ?dates . }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "en,da,de,es,fr,jp,nl,no,ru,sv,zh". }
} GROUP BY ?work ?workLabel ORDER BY DESC(?date) LIMIT 10
```

This gives these 10 papers:

<table>
  <tr>
    <td><b>date</b></td>
    <td><b>work</b></td>
    <td><b>workLabel</b></td>
  </tr>
  <tr>
    <td>2020-03-12T00:00:00Z</td>
    <td>http://www.wikidata.org/entity/Q87675797</td>
    <td>[Recommendations for critically ill patients with COVID-19]</td>
  </tr>
</table>

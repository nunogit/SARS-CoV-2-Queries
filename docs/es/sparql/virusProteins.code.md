# virusProteins.rq
**Ejemplos de código:** [curl](#curl)
### SPARQL
```sparql
SELECT ?protein ?proteinLabel ?refseq ?uniprot ?guideToPharma WHERE {
  ?protein wdt:P703 wd:Q82069695 ; wdt:P31 wd:Q8054 .
  OPTIONAL { ?protein wdt:P637 ?refseq }
  OPTIONAL { ?protein wdt:P352 ?uniprot }
  OPTIONAL { ?protein wdt:P5458 ?guideToPharma }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "es,en". }
}

```
[ejecutar](https://query.wikidata.org/embed.html#SELECT%20%3Fprotein%20%3FproteinLabel%20%3Frefseq%20%3Funiprot%20%3FguideToPharma%20WHERE%20%7B%0A%20%20%3Fprotein%20wdt%3AP703%20wd%3AQ82069695%20%3B%20wdt%3AP31%20wd%3AQ8054%20.%0A%20%20OPTIONAL%20%7B%20%3Fprotein%20wdt%3AP637%20%3Frefseq%20%7D%0A%20%20OPTIONAL%20%7B%20%3Fprotein%20wdt%3AP352%20%3Funiprot%20%7D%0A%20%20OPTIONAL%20%7B%20%3Fprotein%20wdt%3AP5458%20%3FguideToPharma%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22es%2Cen%22.%20%7D%0A%7D%0A%0A) o [editar](https://query.wikidata.org/#SELECT%20%3Fprotein%20%3FproteinLabel%20%3Frefseq%20%3Funiprot%20%3FguideToPharma%20WHERE%20%7B%0A%20%20%3Fprotein%20wdt%3AP703%20wd%3AQ82069695%20%3B%20wdt%3AP31%20wd%3AQ8054%20.%0A%20%20OPTIONAL%20%7B%20%3Fprotein%20wdt%3AP637%20%3Frefseq%20%7D%0A%20%20OPTIONAL%20%7B%20%3Fprotein%20wdt%3AP352%20%3Funiprot%20%7D%0A%20%20OPTIONAL%20%7B%20%3Fprotein%20wdt%3AP5458%20%3FguideToPharma%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22es%2Cen%22.%20%7D%0A%7D%0A%0A)


### Resultados
<table>
  <tr>
    <td><b>protein</b></td>
    <td><b>refseq</b></td>
    <td><b>uniprot</b></td>
    <td><b>guideToPharma</b></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q87917572">Non-structural protein 10 [SARS CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q87917572">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q87917579">non-structural protein 15 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q87917579">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q87917580">non-structural protein 16 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q87917580">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q87917581">Papain-like proteinase [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q87917581">edit</a>)</td>
    <td>YP_009725299.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q87917582">non-structural protein 5 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q87917582">edit</a>)</td>
    <td>YP_009725301</td>
    <td></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3111">3111</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q87917584">nucleocapsid protein [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q87917584">edit</a>)</td>
    <td>YP_009724397.2</td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC9">P0DTC9</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3121">3121</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q87917585">spike glycoprotein</a> (<a href="http://www.wikidata.org/entity/Q87917585">edit</a>)</td>
    <td>YP_009724390.1</td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC2">P0DTC2</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3114">3114</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88174316">orf1ab polyprotein [SARS-Cov 2]</a> (<a href="http://www.wikidata.org/entity/Q88174316">edit</a>)</td>
    <td>QHD43415</td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTD1">P0DTD1</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3125">3125</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88200603">Viroporin 3a [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q88200603">edit</a>)</td>
    <td>YP_009724391.1</td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC3">P0DTC3</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3115">3115</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88655710">envelope protein [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q88655710">edit</a>)</td>
    <td>YP_009724392.1</td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC4">P0DTC4</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3116">3116</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88656821">membrane protein [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q88656821">edit</a>)</td>
    <td>YP_009724393.1</td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC5">P0DTC5</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3117">3117</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88656943">Non-structural protein 6 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q88656943">edit</a>)</td>
    <td></td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC6">P0DTC6</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3118">3118</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88657499">ORF1a polyprotein</a> (<a href="http://www.wikidata.org/entity/Q88657499">edit</a>)</td>
    <td></td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC1">P0DTC1</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3124">3124</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88658500">Protein 7a [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q88658500">edit</a>)</td>
    <td>YP_009724395.1</td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC7">P0DTC7</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3119">3119</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88658861">Protein non-structural 7b [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q88658861">edit</a>)</td>
    <td>YP_009725318.1</td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTD8">P0DTD8</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3123">3123</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q88659350">Non-structural protein 8 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q88659350">edit</a>)</td>
    <td></td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTC8">P0DTC8</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3120">3120</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q89006922">Non-structural protein 2 [SARS CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q89006922">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q89225654">ORF8 protein</a> (<a href="http://www.wikidata.org/entity/Q89225654">edit</a>)</td>
    <td>YP_009724396.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q89226299">ORF6 protein</a> (<a href="http://www.wikidata.org/entity/Q89226299">edit</a>)</td>
    <td>YP_009724394.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q89227548">ORF10 protein [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q89227548">edit</a>)</td>
    <td>YP_009725255.1</td>
    <td><a href="https://www.uniprot.org/uniprot/A0A663DJA2">A0A663DJA2</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q89597571">Protein 9b</a> (<a href="http://www.wikidata.org/entity/Q89597571">edit</a>)</td>
    <td></td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTD2">P0DTD2</a></td>
    <td><a href="https://www.guidetopharmacology.org/GRAC/ObjectDisplayForward?objectId=3122">3122</a></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q89686805">Non-structural protein 9 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q89686805">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q90038952">Host translation inhibitor nsp1 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q90038952">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q90038956">Non-structural protein 4 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q90038956">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q90038963">Non-structural protein 7 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q90038963">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q90042407">Non-structural protein 14 [SARS-CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q90042407">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q94647436">Non-structural protein 12 [SARS CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q94647436">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q94648377">Non-structural protein 13 [SARS CoV-2]</a> (<a href="http://www.wikidata.org/entity/Q94648377">edit</a>)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q94994433">Uncharacterized protein 14</a> (<a href="http://www.wikidata.org/entity/Q94994433">edit</a>)</td>
    <td></td>
    <td><a href="https://www.uniprot.org/uniprot/P0DTD3">P0DTD3</a></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q96022196">ORF7a protein</a> (<a href="http://www.wikidata.org/entity/Q96022196">edit</a>)</td>
    <td>YP_009724395.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q96022202">surface glycoprotein</a> (<a href="http://www.wikidata.org/entity/Q96022202">edit</a>)</td>
    <td>YP_009724390.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q96022209">ORF7b</a> (<a href="http://www.wikidata.org/entity/Q96022209">edit</a>)</td>
    <td>YP_009725318.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q96022219">envelope protein</a> (<a href="http://www.wikidata.org/entity/Q96022219">edit</a>)</td>
    <td>YP_009724392.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q96022223">nucleocapsid phosphoprotein</a> (<a href="http://www.wikidata.org/entity/Q96022223">edit</a>)</td>
    <td>YP_009724397.2</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q96022229">ORF10 protein</a> (<a href="http://www.wikidata.org/entity/Q96022229">edit</a>)</td>
    <td>YP_009725255.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q96356074">membrane glycoprotein</a> (<a href="http://www.wikidata.org/entity/Q96356074">edit</a>)</td>
    <td>YP_009724393.1</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td><a href="https://scholia.toolforge.org/Q96356076">ORF6 protein</a> (<a href="http://www.wikidata.org/entity/Q96356076">edit</a>)</td>
    <td>YP_009724394.1</td>
    <td></td>
    <td></td>
  </tr>
</table>
## Ejemplos de código
### curl
```shell
curl -o virusProteins.rq https://raw.githubusercontent.com/egonw/SARS-CoV-2-Queries/master/sparql/virusProteins.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@virusProteins.rq
```
Esta consulta SPARQL está disponible en CCZero.

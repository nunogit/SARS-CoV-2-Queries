# graphDeaths.rq
**Code examples:** [curl](#curl)
### SPARQL
```sparql
#defaultView:LineChart
SELECT
?date ?deaths
?country ?countryLabel
WHERE {
  ?item wdt:P31 wd:Q3241045.
  ?item wdt:P17 ?country.
  ?item p:P1120 ?deathsStatement.
  ?deathsStatement ps:P1120 ?deaths.
  FILTER(?deaths > 0)
  ?deathsStatement pq:P585 ?date .
  { ?item wdt:P1269 wd:Q81068910. } UNION
  { ?item wdt:P361 wd:Q83741704. }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "pt,en". }
} ORDER BY ASC(?countryLabel) DESC(?date)
```
[run](https://query.wikidata.org/embed.html#%23defaultView%3ALineChart%0ASELECT%0A%3Fdate%20%3Fdeaths%0A%3Fcountry%20%3FcountryLabel%0AWHERE%20%7B%0A%20%20%3Fitem%20wdt%3AP31%20wd%3AQ3241045.%0A%20%20%3Fitem%20wdt%3AP17%20%3Fcountry.%0A%20%20%3Fitem%20p%3AP1120%20%3FdeathsStatement.%0A%20%20%3FdeathsStatement%20ps%3AP1120%20%3Fdeaths.%0A%20%20FILTER%28%3Fdeaths%20%3E%200%29%0A%20%20%3FdeathsStatement%20pq%3AP585%20%3Fdate%20.%0A%20%20%7B%20%3Fitem%20wdt%3AP1269%20wd%3AQ81068910.%20%7D%20UNION%0A%20%20%7B%20%3Fitem%20wdt%3AP361%20wd%3AQ83741704.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22pt%2Cen%22.%20%7D%0A%7D%20ORDER%20BY%20ASC%28%3FcountryLabel%29%20DESC%28%3Fdate%29%0A) or [edit](https://query.wikidata.org/#%23defaultView%3ALineChart%0ASELECT%0A%3Fdate%20%3Fdeaths%0A%3Fcountry%20%3FcountryLabel%0AWHERE%20%7B%0A%20%20%3Fitem%20wdt%3AP31%20wd%3AQ3241045.%0A%20%20%3Fitem%20wdt%3AP17%20%3Fcountry.%0A%20%20%3Fitem%20p%3AP1120%20%3FdeathsStatement.%0A%20%20%3FdeathsStatement%20ps%3AP1120%20%3Fdeaths.%0A%20%20FILTER%28%3Fdeaths%20%3E%200%29%0A%20%20%3FdeathsStatement%20pq%3AP585%20%3Fdate%20.%0A%20%20%7B%20%3Fitem%20wdt%3AP1269%20wd%3AQ81068910.%20%7D%20UNION%0A%20%20%7B%20%3Fitem%20wdt%3AP361%20wd%3AQ83741704.%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22pt%2Cen%22.%20%7D%0A%7D%20ORDER%20BY%20ASC%28%3FcountryLabel%29%20DESC%28%3Fdate%29%0A)


### Output
<table>
  <tr>
    <td><b>date</b></td>
    <td><b>deaths</b></td>
    <td><b>country</b></td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>478</td>
    <td><a href="https://scholia.toolforge.org/Q889">Afeganistão</a> (<a href="http://www.wikidata.org/entity/Q889">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q222">Albânia</a> (<a href="http://www.wikidata.org/entity/Q222">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q222">Albânia</a> (<a href="http://www.wikidata.org/entity/Q222">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q222">Albânia</a> (<a href="http://www.wikidata.org/entity/Q222">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q222">Albânia</a> (<a href="http://www.wikidata.org/entity/Q222">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q222">Albânia</a> (<a href="http://www.wikidata.org/entity/Q222">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q222">Albânia</a> (<a href="http://www.wikidata.org/entity/Q222">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q222">Albânia</a> (<a href="http://www.wikidata.org/entity/Q222">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>9048</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>9036</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>9024</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>9016</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>9012</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>9010</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>9003</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>8994</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>8985</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>8489</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>8450</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>8411</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>8349</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>8302</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>8257</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>8247</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>8216</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>8174</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>8147</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>8090</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>8007</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>7935</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>7914</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>7881</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>7824</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>7723</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>7634</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>7533</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>7417</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>7395</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>7369</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>7266</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>7119</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>6996</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>6831</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>6692</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>6649</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>6575</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>6481</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>6288</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>6115</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>5913</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>5750</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>5640</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>5500</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>5321</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>5094</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>4879</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>4598</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>4404</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>4294</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>4110</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>3868</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>3569</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>3254</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>2969</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>2799</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>2673</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>2544</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>2373</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>2107</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>1861</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>1607</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>1434</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>1342</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>1158</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>1017</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>872</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>732</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>583</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>455</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>389</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>325</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>253</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>198</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>149</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>126</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>94</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>67</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q183">Alemanha</a> (<a href="http://www.wikidata.org/entity/Q183">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q228">Andorra</a> (<a href="http://www.wikidata.org/entity/Q228">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q916">Angola</a> (<a href="http://www.wikidata.org/entity/Q916">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q781">Antígua e Barbuda</a> (<a href="http://www.wikidata.org/entity/Q781">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>1818</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>1845</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-11</td>
    <td>1787</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-10</td>
    <td>1749</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-10</td>
    <td>1774</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-09</td>
    <td>1707</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-09</td>
    <td>1720</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>1654</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>1602</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>1523</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>1490</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>1507</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>1453</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>1403</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>1437</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>1363</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>1385</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>1310</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>1351</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>1283</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>1307</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>1245</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>1280</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>1217</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>1192</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>1207</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>1167</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>1124</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>1150</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>1085</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>1116</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>1049</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>1016</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>1043</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-21</td>
    <td>1000</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-21</td>
    <td>1011</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>992</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>954</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>979</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>929</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>948</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>886</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>913</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-16</td>
    <td>862</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-16</td>
    <td>878</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>842</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>854</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>819</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>833</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>802</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>815</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>772</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>785</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>765</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>735</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>698</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>717</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>670</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>693</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>656</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>664</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>648</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-05</td>
    <td>632</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>608</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-03</td>
    <td>583</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>569</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>556</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>539</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>528</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>520</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>508</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>500</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>490</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>467</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>452</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>445</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>433</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>416</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>403</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>393</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>382</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>366</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>363</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>356</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>353</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>329</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>317</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>319</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>305</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>300</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>285</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>293</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>282</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>273</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>262</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>249</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>246</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>241</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>225</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>218</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>214</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>207</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>197</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>187</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>192</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>185</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>176</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>165</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>159</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>151</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>142</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>134</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>132</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>129</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>122</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>105</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>69</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q414">Argentina</a> (<a href="http://www.wikidata.org/entity/Q414">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-23</td>
    <td>952</td>
    <td><a href="https://scholia.toolforge.org/Q262">Argélia</a> (<a href="http://www.wikidata.org/entity/Q262">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>211</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>42</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q399">Arménia</a> (<a href="http://www.wikidata.org/entity/Q399">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q21203">Aruba</a> (<a href="http://www.wikidata.org/entity/Q21203">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q21203">Aruba</a> (<a href="http://www.wikidata.org/entity/Q21203">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>712</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>264</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>246</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>239</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>209</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>200</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>191</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>176</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>169</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>144</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>139</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>114</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q851">Arábia Saudita</a> (<a href="http://www.wikidata.org/entity/Q851">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>104</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>97</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>97</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>93</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>89</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>83</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>81</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>76</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>74</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>72</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>71</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>69</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>65</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>63</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>62</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>61</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>60</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>51</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-04</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-01</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q408">Austrália</a> (<a href="http://www.wikidata.org/entity/Q408">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>88</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q227">Azerbaijão</a> (<a href="http://www.wikidata.org/entity/Q227">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q778">Bahamas</a> (<a href="http://www.wikidata.org/entity/Q778">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q778">Bahamas</a> (<a href="http://www.wikidata.org/entity/Q778">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q778">Bahamas</a> (<a href="http://www.wikidata.org/entity/Q778">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q398">Bahrein</a> (<a href="http://www.wikidata.org/entity/Q398">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>1661</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>888</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>250</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>228</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>214</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>199</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>186</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>183</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>182</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>175</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>168</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>155</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>152</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>145</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>120</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>101</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q902">Bangladesh</a> (<a href="http://www.wikidata.org/entity/Q902">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q244">Barbados</a> (<a href="http://www.wikidata.org/entity/Q244">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q242">Belize</a> (<a href="http://www.wikidata.org/entity/Q242">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q962">Benim</a> (<a href="http://www.wikidata.org/entity/Q962">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q962">Benim</a> (<a href="http://www.wikidata.org/entity/Q962">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q962">Benim</a> (<a href="http://www.wikidata.org/entity/Q962">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q23635">Bermudas</a> (<a href="http://www.wikidata.org/entity/Q23635">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q23635">Bermudas</a> (<a href="http://www.wikidata.org/entity/Q23635">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q23635">Bermudas</a> (<a href="http://www.wikidata.org/entity/Q23635">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q23635">Bermudas</a> (<a href="http://www.wikidata.org/entity/Q23635">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q23635">Bermudas</a> (<a href="http://www.wikidata.org/entity/Q23635">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>392</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>149</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>112</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>99</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q184">Bielorrússia</a> (<a href="http://www.wikidata.org/entity/Q184">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-11</td>
    <td>1754</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>1557</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>1530</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>1476</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>1434</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>1378</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>1320</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>1271</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>1201</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>1123</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>1071</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>1014</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>970</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>934</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>913</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>820</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>740</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>679</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>611</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>427</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>313</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>310</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>174</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>128</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>114</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>91</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>82</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>66</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>62</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>53</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>37</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q750">Bolívia</a> (<a href="http://www.wikidata.org/entity/Q750">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q963">Botsuana</a> (<a href="http://www.wikidata.org/entity/Q963">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>66741</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>65487</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>64867</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>64265</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>63174</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>61884</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>60632</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>59594</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>58314</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>57662</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>57070</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>54971</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>51271</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>48427</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>43389</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>36499</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>35026</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>30104</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>26754</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>25598</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>24512</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>23473</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>22666</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>22013</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>21048</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>20047</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>18859</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>17971</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>16792</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>16118</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>15633</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>14817</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>13993</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>13149</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>12400</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>11519</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>11123</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>10627</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>9897</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>9146</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>8536</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>7921</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>7321</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>7025</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>6750</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>6329</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>5901</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>5466</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>5017</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>4543</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>4205</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>4016</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>3670</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>3313</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>2906</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>2741</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>2575</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>2462</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>2347</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>2141</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>1924</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>1736</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>1532</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>1328</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>1223</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>1124</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>1056</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>941</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>800</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>667</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>553</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>486</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>432</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>343</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>359</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>241</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>159</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>136</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>114</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>77</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>57</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q155">Brasil</a> (<a href="http://www.wikidata.org/entity/Q155">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q921">Brunei</a> (<a href="http://www.wikidata.org/entity/Q921">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>95</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>91</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>84</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>78</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q219">Bulgária</a> (<a href="http://www.wikidata.org/entity/Q219">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>51</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>42</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>39</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q965">Burkina Faso</a> (<a href="http://www.wikidata.org/entity/Q965">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q967">Burundi</a> (<a href="http://www.wikidata.org/entity/Q967">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q967">Burundi</a> (<a href="http://www.wikidata.org/entity/Q967">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q967">Burundi</a> (<a href="http://www.wikidata.org/entity/Q967">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q967">Burundi</a> (<a href="http://www.wikidata.org/entity/Q967">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q967">Burundi</a> (<a href="http://www.wikidata.org/entity/Q967">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q967">Burundi</a> (<a href="http://www.wikidata.org/entity/Q967">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q967">Burundi</a> (<a href="http://www.wikidata.org/entity/Q967">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q967">Burundi</a> (<a href="http://www.wikidata.org/entity/Q967">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>9754</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>8761</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>8339</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>5998</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>3346</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>2523</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>513</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>75</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>67</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>37</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q31">Bélgica</a> (<a href="http://www.wikidata.org/entity/Q31">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>168</td>
    <td><a href="https://scholia.toolforge.org/Q225">Bósnia e Herzegovina</a> (<a href="http://www.wikidata.org/entity/Q225">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>116</td>
    <td><a href="https://scholia.toolforge.org/Q225">Bósnia e Herzegovina</a> (<a href="http://www.wikidata.org/entity/Q225">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>87</td>
    <td><a href="https://scholia.toolforge.org/Q225">Bósnia e Herzegovina</a> (<a href="http://www.wikidata.org/entity/Q225">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q225">Bósnia e Herzegovina</a> (<a href="http://www.wikidata.org/entity/Q225">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q225">Bósnia e Herzegovina</a> (<a href="http://www.wikidata.org/entity/Q225">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q225">Bósnia e Herzegovina</a> (<a href="http://www.wikidata.org/entity/Q225">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-11</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q1011">Cabo Verde</a> (<a href="http://www.wikidata.org/entity/Q1011">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1011">Cabo Verde</a> (<a href="http://www.wikidata.org/entity/Q1011">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1011">Cabo Verde</a> (<a href="http://www.wikidata.org/entity/Q1011">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>125</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>114</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>108</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>108</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>64</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>61</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q1009">Camarões</a> (<a href="http://www.wikidata.org/entity/Q1009">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>8711</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>8684</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>8674</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>8663</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>8642</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>8591</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>8522</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>8516</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>8454</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>7800</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>7703</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>5209</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>4728</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>3915</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>3537</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>2904</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>1761</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>2766</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>2617</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>2489</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1871</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>647</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>1728</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>1611</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>1506</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>1346</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>954</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>903</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>780</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>461</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>94</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>101</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q16">Canadá</a> (<a href="http://www.wikidata.org/entity/Q16">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q846">Catar</a> (<a href="http://www.wikidata.org/entity/Q846">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q232">Cazaquistão</a> (<a href="http://www.wikidata.org/entity/Q232">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q657">Chade</a> (<a href="http://www.wikidata.org/entity/Q657">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q657">Chade</a> (<a href="http://www.wikidata.org/entity/Q657">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q657">Chade</a> (<a href="http://www.wikidata.org/entity/Q657">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q657">Chade</a> (<a href="http://www.wikidata.org/entity/Q657">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q657">Chade</a> (<a href="http://www.wikidata.org/entity/Q657">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q657">Chade</a> (<a href="http://www.wikidata.org/entity/Q657">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q657">Chade</a> (<a href="http://www.wikidata.org/entity/Q657">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>6434</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>6192</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>6051</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>5920</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>5753</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>5688</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>5575</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>5509</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>4505</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>4502</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>4295</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>3362</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>2264</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>1188</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>478</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>346</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>335</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>312</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>304</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>281</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>275</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>270</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>247</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>234</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>216</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>207</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>198</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>189</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>160</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>147</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>139</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>133</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>126</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>82</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>57</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>37</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q298">Chile</a> (<a href="http://www.wikidata.org/entity/Q298">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>4644</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>4642</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>4643</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>4642</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>4642</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>4642</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>4642</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>4642</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>4642</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>4642</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>3352</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>3352</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>3351</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>3351</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>3349</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>3349</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>3345</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>3344</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>3342</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>3340</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>3340</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>3338</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>3335</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>3331</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>3327</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>3321</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>3314</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>3310</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>3306</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>3301</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>3298</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>3293</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>3287</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>3283</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>3276</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>3267</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>3261</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>3242</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>3253</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>3242</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>3231</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>3218</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>3218</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>3204</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>3180</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>3180</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>3173</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>3162</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>3140</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>3123</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>3100</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>3073</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>3045</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-04</td>
    <td>3015</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-03</td>
    <td>2984</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-02</td>
    <td>2946</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-01</td>
    <td>2915</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-29</td>
    <td>2873</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-28</td>
    <td>2838</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-27</td>
    <td>2791</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-26</td>
    <td>2747</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-25</td>
    <td>2718</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-24</td>
    <td>2666</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-23</td>
    <td>2595</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-22</td>
    <td>2445</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-21</td>
    <td>2348</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-20</td>
    <td>2121</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-19</td>
    <td>2121</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-18</td>
    <td>2006</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-17</td>
    <td>1870</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-16</td>
    <td>1772</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-15</td>
    <td>1666</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-14</td>
    <td>1524</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-13</td>
    <td>1381</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-12</td>
    <td>1260</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-11</td>
    <td>1114</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-10</td>
    <td>909</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-09</td>
    <td>812</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-08</td>
    <td>723</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-07</td>
    <td>637</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-06</td>
    <td>564</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-05</td>
    <td>491</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-04</td>
    <td>425</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-03</td>
    <td>361</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-02</td>
    <td>304</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-01</td>
    <td>259</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-31</td>
    <td>213</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-30</td>
    <td>170</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-29</td>
    <td>132</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-28</td>
    <td>106</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-27</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-26</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-25</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-24</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-23</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-22</td>
    <td>234</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-21</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-01-20</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q148">China</a> (<a href="http://www.wikidata.org/entity/Q148">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q229">Chipre</a> (<a href="http://www.wikidata.org/entity/Q229">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q229">Chipre</a> (<a href="http://www.wikidata.org/entity/Q229">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q229">Chipre</a> (<a href="http://www.wikidata.org/entity/Q229">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q229">Chipre</a> (<a href="http://www.wikidata.org/entity/Q229">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q229">Chipre</a> (<a href="http://www.wikidata.org/entity/Q229">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q229">Chipre</a> (<a href="http://www.wikidata.org/entity/Q229">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>5307</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-11</td>
    <td>5119</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-10</td>
    <td>4925</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-09</td>
    <td>4714</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>4527</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>4359</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>4210</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>4064</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>3942</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>3777</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>3641</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>3470</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>3334</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>3223</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>3106</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>2939</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>2811</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>2654</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>2491</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>2404</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>2310</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-21</td>
    <td>2237</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>2126</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>2045</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>1950</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>1864</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-16</td>
    <td>1801</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>1726</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>1667</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>1592</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>1545</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>1488</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>1433</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>1372</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>1308</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>1259</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>1205</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-05</td>
    <td>1145</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>1087</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-03</td>
    <td>1045</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>1009</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>969</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>939</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>890</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>853</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>822</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>803</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>776</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>750</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>727</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>705</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>682</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>652</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>630</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>613</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>592</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>574</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>562</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>546</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>525</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>509</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>493</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>479</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>463</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>445</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>428</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>407</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>397</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>378</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>358</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>340</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>324</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>314</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>293</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>278</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>269</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>253</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>244</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>233</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>225</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>215</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>206</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>196</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>189</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>179</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>166</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>153</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>144</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>131</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>127</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>112</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>100</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>69</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q739">Colômbia</a> (<a href="http://www.wikidata.org/entity/Q739">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>273</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>259</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>256</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>255</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>246</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>244</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>243</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>240</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>238</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>237</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>204</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>165</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>162</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>158</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>152</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>144</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>139</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>131</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>126</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>120</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>111</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>94</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>91</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>84</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>81</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>75</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>75</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>72</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>67</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>66</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>60</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>51</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>42</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-04</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-03</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-02</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-01</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-29</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-28</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-27</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-26</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-25</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-24</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-23</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-22</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-21</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-20</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q884">Coreia do Sul</a> (<a href="http://www.wikidata.org/entity/Q884">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q800">Costa Rica</a> (<a href="http://www.wikidata.org/entity/Q800">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q1008">Costa do Marfim</a> (<a href="http://www.wikidata.org/entity/Q1008">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q1008">Costa do Marfim</a> (<a href="http://www.wikidata.org/entity/Q1008">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>94</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>91</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>90</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>75</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>69</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>63</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q224">Croácia</a> (<a href="http://www.wikidata.org/entity/Q224">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>83</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>77</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>69</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>66</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>64</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q241">Cuba</a> (<a href="http://www.wikidata.org/entity/Q241">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q25279">Curaçao</a> (<a href="http://www.wikidata.org/entity/Q25279">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>527</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>526</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>506</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>452</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>434</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>370</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>273</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>237</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>104</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q35">Dinamarca</a> (<a href="http://www.wikidata.org/entity/Q35">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q977">Djibouti</a> (<a href="http://www.wikidata.org/entity/Q977">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q977">Djibouti</a> (<a href="http://www.wikidata.org/entity/Q977">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q977">Djibouti</a> (<a href="http://www.wikidata.org/entity/Q977">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q977">Djibouti</a> (<a href="http://www.wikidata.org/entity/Q977">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q977">Djibouti</a> (<a href="http://www.wikidata.org/entity/Q977">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q977">Djibouti</a> (<a href="http://www.wikidata.org/entity/Q977">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q977">Djibouti</a> (<a href="http://www.wikidata.org/entity/Q977">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q977">Djibouti</a> (<a href="http://www.wikidata.org/entity/Q977">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>592</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>556</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>544</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>533</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>525</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>503</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>469</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>436</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>429</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>415</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>406</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>392</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>359</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>276</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>164</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q79">Egito</a> (<a href="http://www.wikidata.org/entity/Q79">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>235</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>202</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>191</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>182</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>174</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>164</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>152</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>119</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q792">El Salvador</a> (<a href="http://www.wikidata.org/entity/Q792">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>276</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>203</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>198</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>185</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>157</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>146</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>137</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>119</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>111</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>105</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>82</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>76</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q878">Emirados Árabes Unidos</a> (<a href="http://www.wikidata.org/entity/Q878">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>4873</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>4821</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>4781</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>4769</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>4700</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>4576</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>4527</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>4502</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>4424</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>4406</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>6284</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>3608</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>2839</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>2334</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>2127</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>1717</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1618</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1569</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>1371</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1063</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>883</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>871</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>663</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>576</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>537</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>520</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>507</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>474</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>456</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>369</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>315</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>297</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>272</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>242</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>220</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>191</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>180</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>172</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>145</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>120</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>62</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q736">Equador</a> (<a href="http://www.wikidata.org/entity/Q736">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q214">Eslováquia</a> (<a href="http://www.wikidata.org/entity/Q214">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>99</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>91</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>77</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q215">Eslovénia</a> (<a href="http://www.wikidata.org/entity/Q215">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>28355</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>2096</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>27119</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>27118</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>27117</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>26834</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>28678</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>28628</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>27940</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>27888</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>27778</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>27709</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>27650</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>27563</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>27459</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>27321</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>27104</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>26920</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>26744</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>26621</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>26478</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>1873</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>26299</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>737</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1850</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>26070</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>1834</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>25857</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1817</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>25613</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>1801</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>25428</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>1791</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>25264</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1780</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>25100</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1757</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>24824</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>1732</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>24543</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1697</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>24275</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>1683</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>23822</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>1663</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>23521</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>1643</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>23190</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>1612</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>22902</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>1578</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>22524</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1527</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>22157</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>1502</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>21717</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>1468</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>21282</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>1376</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>1433</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>20852</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>1342</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>20453</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>1298</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>20043</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>1220</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>19478</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>1169</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>19130</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>1127</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>18579</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>1090</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>18056</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>1043</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>17489</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>995</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>16972</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>948</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>16353</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>905</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>15843</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>846</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>15238</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>790</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>14555</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>13798</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>696</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>13055</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>651</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>12418</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>597</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>11744</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>555</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>10935</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>501</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>10003</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>440</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>9053</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>400</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>7340</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>8189</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>350</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>6528</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>312</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>5690</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>266</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>4858</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>230</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>4089</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>188</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>3434</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>165</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>2696</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>145</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>2182</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>112</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>1720</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>96</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>1326</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>81</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>1002</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>767</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>598</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>39</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>491</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>309</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>288</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>136</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>120</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>84</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-04</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q29">Espanha</a> (<a href="http://www.wikidata.org/entity/Q29">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1050">Essuatíni</a> (<a href="http://www.wikidata.org/entity/Q1050">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1050">Essuatíni</a> (<a href="http://www.wikidata.org/entity/Q1050">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1050">Essuatíni</a> (<a href="http://www.wikidata.org/entity/Q1050">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1050">Essuatíni</a> (<a href="http://www.wikidata.org/entity/Q1050">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1050">Essuatíni</a> (<a href="http://www.wikidata.org/entity/Q1050">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1050">Essuatíni</a> (<a href="http://www.wikidata.org/entity/Q1050">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1050">Essuatíni</a> (<a href="http://www.wikidata.org/entity/Q1050">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1050">Essuatíni</a> (<a href="http://www.wikidata.org/entity/Q1050">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-11</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-10</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-09</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q219060">Estado da Palestina</a> (<a href="http://www.wikidata.org/entity/Q219060">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>131666</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>127322</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>126573</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>125927</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>125739</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>120333</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>117728</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>117586</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>109901</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>109038</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>105773</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>103330</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>102107</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>100572</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>99805</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>99300</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>98683</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>97647</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>96354</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>94936</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>93533</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>91981</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>90978</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>90113</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>88507</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>86912</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>85197</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>83425</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>81795</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>80787</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>80037</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>78615</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>76928</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>74799</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>72271</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>69921</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>68598</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>67444</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>65753</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>63856</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>61656</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>59266</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>56797</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>55413</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>54256</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>52193</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>50236</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>47659</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>45318</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>42514</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>40575</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>39014</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>37154</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>34617</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>32443</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>29825</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>23640</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>22105</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>20577</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>18747</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>16691</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>14788</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>12841</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>10871</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>9616</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>8452</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>7392</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>6070</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>5102</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>4053</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>3156</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>2484</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>2221</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>1696</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>1295</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>1027</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>780</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>483</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>348</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>301</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>255</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>150</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>150</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>87</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-04</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-03</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-02</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-01</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-29</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q30">Estados Unidos</a> (<a href="http://www.wikidata.org/entity/Q30">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>64</td>
    <td><a href="https://scholia.toolforge.org/Q191">Estónia</a> (<a href="http://www.wikidata.org/entity/Q191">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>61</td>
    <td><a href="https://scholia.toolforge.org/Q191">Estónia</a> (<a href="http://www.wikidata.org/entity/Q191">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q191">Estónia</a> (<a href="http://www.wikidata.org/entity/Q191">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q191">Estónia</a> (<a href="http://www.wikidata.org/entity/Q191">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q191">Estónia</a> (<a href="http://www.wikidata.org/entity/Q191">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q191">Estónia</a> (<a href="http://www.wikidata.org/entity/Q191">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q115">Etiópia</a> (<a href="http://www.wikidata.org/entity/Q115">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>1003</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>751</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>719</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>704</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>658</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>637</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>623</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>603</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>579</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>568</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>511</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>501</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>446</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>437</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>428</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>177</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-05</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q928">Filipinas</a> (<a href="http://www.wikidata.org/entity/Q928">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>275</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>255</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>211</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>206</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>141</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q33">Finlândia</a> (<a href="http://www.wikidata.org/entity/Q33">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>29760</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>2096</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>28367</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>28289</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>28215</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>28132</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>27425</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>27074</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>26383</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>26310</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>26230</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>1873</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>25987</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>737</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1850</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>25809</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>1834</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>25531</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1817</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>25201</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>1801</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>24895</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>1791</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>24760</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1780</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>24594</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1757</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>24376</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>1732</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>24087</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1697</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>23660</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>1683</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>23293</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>14497</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>8796</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>1663</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>22856</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>8654</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>14202</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>1643</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>22614</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>8564</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>14050</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>1612</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>22245</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>13852</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>8393</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>1578</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>21856</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>13536</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>8309</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1527</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>21340</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>13225</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>8104</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>1502</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>20796</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>12892</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>7896</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>1468</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>20265</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>12505</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>7752</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>1376</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>1433</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>19718</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>12069</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>7649</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>1342</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>19323</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>7481</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>11842</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>1298</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>18681</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>11478</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>7203</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>1220</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>11060</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>17920</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>6860</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>1169</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>6524</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>10643</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>17167</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>1127</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>10129</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>15729</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>5600</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>1090</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>9588</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>5379</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>14967</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>1043</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>7091</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>14393</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>5140</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>995</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>8943</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>13832</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>4889</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>948</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>4599</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>8598</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>13197</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>905</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>12210</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>8044</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>4166</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>846</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>7632</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>3237</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>10869</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>790</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>7091</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>3237</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>10328</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>8911</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>6494</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>2417</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>696</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>8078</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>5889</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>2189</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>651</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>7560</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>5532</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>2028</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>597</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>6507</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>555</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>4503</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>501</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>4032</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>440</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>3523</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>400</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>3024</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>350</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>2606</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>312</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>2314</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>266</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>1995</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>230</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>1696</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>188</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>1331</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>1100</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>165</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>145</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>860</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>674</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>112</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>562</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>96</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>450</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>81</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>372</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>264</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>175</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>244</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>39</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>175</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>148</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>127</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>91</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>61</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-04</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-03</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-02</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-01</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-29</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-28</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-27</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-26</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-26</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-25</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-24</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-23</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-21</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-20</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-18</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-16</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-15</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-14</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q142">França</a> (<a href="http://www.wikidata.org/entity/Q142">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1000">Gabão</a> (<a href="http://www.wikidata.org/entity/Q1000">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1000">Gabão</a> (<a href="http://www.wikidata.org/entity/Q1000">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1000">Gabão</a> (<a href="http://www.wikidata.org/entity/Q1000">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q117">Gana</a> (<a href="http://www.wikidata.org/entity/Q117">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q230">Geórgia</a> (<a href="http://www.wikidata.org/entity/Q230">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q230">Geórgia</a> (<a href="http://www.wikidata.org/entity/Q230">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q230">Geórgia</a> (<a href="http://www.wikidata.org/entity/Q230">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q230">Geórgia</a> (<a href="http://www.wikidata.org/entity/Q230">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q230">Geórgia</a> (<a href="http://www.wikidata.org/entity/Q230">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q230">Geórgia</a> (<a href="http://www.wikidata.org/entity/Q230">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q230">Geórgia</a> (<a href="http://www.wikidata.org/entity/Q230">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>152</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>148</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>147</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>146</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>146</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>144</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>144</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>143</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>140</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>140</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>139</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>138</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>136</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>134</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>130</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>130</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>125</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>121</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>121</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>116</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>113</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>108</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>105</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>101</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>99</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>93</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>90</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>83</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>87</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>73</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>68</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>59</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>53</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q41">Grécia</a> (<a href="http://www.wikidata.org/entity/Q41">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>1053</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>1004</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>981</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>947</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>920</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>880</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>843</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>817</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>773</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>746</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>727</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>623</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>582</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>230</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>216</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q774">Guatemala</a> (<a href="http://www.wikidata.org/entity/Q774">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q734">Guiana</a> (<a href="http://www.wikidata.org/entity/Q734">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q734">Guiana</a> (<a href="http://www.wikidata.org/entity/Q734">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q734">Guiana</a> (<a href="http://www.wikidata.org/entity/Q734">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q734">Guiana</a> (<a href="http://www.wikidata.org/entity/Q734">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q1006">Guiné</a> (<a href="http://www.wikidata.org/entity/Q1006">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q1006">Guiné</a> (<a href="http://www.wikidata.org/entity/Q1006">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q1006">Guiné</a> (<a href="http://www.wikidata.org/entity/Q1006">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q1006">Guiné</a> (<a href="http://www.wikidata.org/entity/Q1006">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q1006">Guiné</a> (<a href="http://www.wikidata.org/entity/Q1006">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q1006">Guiné</a> (<a href="http://www.wikidata.org/entity/Q1006">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q1006">Guiné</a> (<a href="http://www.wikidata.org/entity/Q1006">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q983">Guiné Equatorial</a> (<a href="http://www.wikidata.org/entity/Q983">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1007">Guiné-Bissau</a> (<a href="http://www.wikidata.org/entity/Q1007">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1007">Guiné-Bissau</a> (<a href="http://www.wikidata.org/entity/Q1007">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1007">Guiné-Bissau</a> (<a href="http://www.wikidata.org/entity/Q1007">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1007">Guiné-Bissau</a> (<a href="http://www.wikidata.org/entity/Q1007">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1007">Guiné-Bissau</a> (<a href="http://www.wikidata.org/entity/Q1007">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1005">Gâmbia</a> (<a href="http://www.wikidata.org/entity/Q1005">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1005">Gâmbia</a> (<a href="http://www.wikidata.org/entity/Q1005">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>105</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>73</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q790">Haiti</a> (<a href="http://www.wikidata.org/entity/Q790">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>677</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>656</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>639</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>629</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>605</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>591</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>542</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>497</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>485</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>479</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>479</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>471</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>417</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>405</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>258</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>248</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>121</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>108</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>108</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>99</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>89</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>83</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>75</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>66</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>64</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>61</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q783">Honduras</a> (<a href="http://www.wikidata.org/entity/Q783">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-13</td>
    <td>595</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>595</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-11</td>
    <td>595</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-10</td>
    <td>593</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-09</td>
    <td>591</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>589</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>589</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>589</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>589</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>589</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>588</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>587</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>586</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>585</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>585</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>581</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>578</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>578</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>577</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>576</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>573</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>572</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-21</td>
    <td>570</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>570</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>568</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>568</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>567</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-16</td>
    <td>565</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>563</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>562</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>559</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>555</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>553</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>551</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>550</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>548</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>546</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>545</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-05</td>
    <td>542</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>539</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-03</td>
    <td>534</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>532</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>527</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>526</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>524</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>517</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>509</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>505</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>499</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>491</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>486</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>482</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>476</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>473</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>470</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>467</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>462</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>451</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>448</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>442</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>436</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>430</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>425</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>421</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>413</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>405</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>392</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>383</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>373</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>363</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>351</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>340</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>335</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>323</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>312</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>300</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>291</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>280</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>272</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>262</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>250</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>239</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>225</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>213</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>199</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>189</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>172</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>156</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>142</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>134</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>122</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>99</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>77</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>66</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>47</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q28">Hungria</a> (<a href="http://www.wikidata.org/entity/Q28">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>3606</td>
    <td><a href="https://scholia.toolforge.org/Q252">Indonésia</a> (<a href="http://www.wikidata.org/entity/Q252">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>346</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>112</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>107</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>95</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>94</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>93</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>88</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>87</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>83</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>83</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>82</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>71</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q796">Iraque</a> (<a href="http://www.wikidata.org/entity/Q796">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>8281</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>6733</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>6640</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>6486</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>6340</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>6277</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>6156</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>6028</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>5806</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>5710</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>5391</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>5297</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>5209</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>5118</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>5031</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>4958</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>4869</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>4777</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>4683</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>4585</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>4474</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>4357</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>4232</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>4110</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>3993</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>3872</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>3739</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>3603</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>3452</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>3294</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>3160</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>3036</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>2898</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>2757</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>2640</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>2517</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>2378</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>2234</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>2077</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>1934</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>1812</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>1685</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>1556</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>1433</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1284</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>1135</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>988</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>853</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>608</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>514</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>429</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>354</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>291</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>237</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>194</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>145</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>124</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>107</td>
    <td><a href="https://scholia.toolforge.org/Q794">Irão</a> (<a href="http://www.wikidata.org/entity/Q794">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q189">Islândia</a> (<a href="http://www.wikidata.org/entity/Q189">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q189">Islândia</a> (<a href="http://www.wikidata.org/entity/Q189">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q189">Islândia</a> (<a href="http://www.wikidata.org/entity/Q189">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>294</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>260</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>254</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>245</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>239</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>237</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>227</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>225</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>222</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>202</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>199</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>184</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>171</td>
    <td><a href="https://scholia.toolforge.org/Q801">Israel</a> (<a href="http://www.wikidata.org/entity/Q801">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>34767</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>33142</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>33072</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>32955</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>32877</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>32735</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>32616</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>32486</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>32330</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>32169</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>32007</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>31908</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>31763</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>31610</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>31368</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>31106</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>30911</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>30739</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>30560</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>30395</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>30201</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>29958</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>29684</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>29315</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>29079</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>28884</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>28710</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>28236</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>27967</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>27682</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>27359</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>26977</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>26644</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>26384</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>25969</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>25549</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>25085</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>24648</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>24114</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>23660</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>23227</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>22745</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>22170</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>21645</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>21067</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>20465</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>19899</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>19468</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>18849</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>18279</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>17669</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>17127</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>16523</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>15887</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>15362</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>14681</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>13915</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>13155</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>12428</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>11591</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>10779</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>10023</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>9134</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>8165</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>7503</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>6820</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>6077</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>5476</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>4827</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>4032</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>2978</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>3407</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>2503</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>2503</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>2158</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>1809</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>1441</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>1268</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>1016</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>827</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>631</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>463</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>366</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>234</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>197</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>148</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-04</td>
    <td>107</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-03</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-02</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-01</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-29</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-28</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-27</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-26</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-25</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-24</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-23</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-22</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-02-21</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q38">Itália</a> (<a href="http://www.wikidata.org/entity/Q38">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>113</td>
    <td><a href="https://scholia.toolforge.org/Q805">Iémen</a> (<a href="http://www.wikidata.org/entity/Q805">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q805">Iémen</a> (<a href="http://www.wikidata.org/entity/Q805">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q805">Iémen</a> (<a href="http://www.wikidata.org/entity/Q805">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q805">Iémen</a> (<a href="http://www.wikidata.org/entity/Q805">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q805">Iémen</a> (<a href="http://www.wikidata.org/entity/Q805">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q805">Iémen</a> (<a href="http://www.wikidata.org/entity/Q805">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q805">Iémen</a> (<a href="http://www.wikidata.org/entity/Q805">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q805">Iémen</a> (<a href="http://www.wikidata.org/entity/Q805">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q766">Jamaica</a> (<a href="http://www.wikidata.org/entity/Q766">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>916</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>668</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>657</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>624</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>607</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>556</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>543</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>536</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>492</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>430</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>415</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>389</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>377</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>351</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>348</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>334</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>317</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>287</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>277</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>186</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>171</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>161</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>154</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>148</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>136</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>119</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>94</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>88</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>81</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>73</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>70</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>69</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>65</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>57</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>57</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>42</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q17">Japão</a> (<a href="http://www.wikidata.org/entity/Q17">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q810">Jordânia</a> (<a href="http://www.wikidata.org/entity/Q810">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q1246">Kosovo</a> (<a href="http://www.wikidata.org/entity/Q1246">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q1246">Kosovo</a> (<a href="http://www.wikidata.org/entity/Q1246">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q1246">Kosovo</a> (<a href="http://www.wikidata.org/entity/Q1246">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q1246">Kosovo</a> (<a href="http://www.wikidata.org/entity/Q1246">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q1246">Kosovo</a> (<a href="http://www.wikidata.org/entity/Q1246">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1246">Kosovo</a> (<a href="http://www.wikidata.org/entity/Q1246">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>264</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>75</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q817">Kuwait</a> (<a href="http://www.wikidata.org/entity/Q817">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q211">Letónia</a> (<a href="http://www.wikidata.org/entity/Q211">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q211">Letónia</a> (<a href="http://www.wikidata.org/entity/Q211">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q211">Letónia</a> (<a href="http://www.wikidata.org/entity/Q211">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q211">Letónia</a> (<a href="http://www.wikidata.org/entity/Q211">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q211">Letónia</a> (<a href="http://www.wikidata.org/entity/Q211">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q211">Letónia</a> (<a href="http://www.wikidata.org/entity/Q211">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q211">Letónia</a> (<a href="http://www.wikidata.org/entity/Q211">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q1014">Libéria</a> (<a href="http://www.wikidata.org/entity/Q1014">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q1014">Libéria</a> (<a href="http://www.wikidata.org/entity/Q1014">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q347">Liechtenstein</a> (<a href="http://www.wikidata.org/entity/Q347">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q347">Liechtenstein</a> (<a href="http://www.wikidata.org/entity/Q347">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q347">Liechtenstein</a> (<a href="http://www.wikidata.org/entity/Q347">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q347">Liechtenstein</a> (<a href="http://www.wikidata.org/entity/Q347">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q37">Lituânia</a> (<a href="http://www.wikidata.org/entity/Q37">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q37">Lituânia</a> (<a href="http://www.wikidata.org/entity/Q37">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q37">Lituânia</a> (<a href="http://www.wikidata.org/entity/Q37">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q37">Lituânia</a> (<a href="http://www.wikidata.org/entity/Q37">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>111</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-11</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-10</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-09</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-21</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-16</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-05</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-03</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>107</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>107</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>104</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>104</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>101</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>101</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>101</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>100</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>100</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>96</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>96</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>96</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>90</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>89</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>89</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>88</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>88</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>83</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>76</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>74</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>73</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>71</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>68</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>68</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>68</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>63</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>60</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>47</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q32">Luxemburgo</a> (<a href="http://www.wikidata.org/entity/Q32">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q822">Líbano</a> (<a href="http://www.wikidata.org/entity/Q822">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1016">Líbia</a> (<a href="http://www.wikidata.org/entity/Q1016">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q221">Macedónia do Norte</a> (<a href="http://www.wikidata.org/entity/Q221">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>88</td>
    <td><a href="https://scholia.toolforge.org/Q221">Macedónia do Norte</a> (<a href="http://www.wikidata.org/entity/Q221">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q221">Macedónia do Norte</a> (<a href="http://www.wikidata.org/entity/Q221">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q221">Macedónia do Norte</a> (<a href="http://www.wikidata.org/entity/Q221">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q221">Macedónia do Norte</a> (<a href="http://www.wikidata.org/entity/Q221">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1019">Madagáscar</a> (<a href="http://www.wikidata.org/entity/Q1019">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1020">Malawi</a> (<a href="http://www.wikidata.org/entity/Q1020">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q826">Maldivas</a> (<a href="http://www.wikidata.org/entity/Q826">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q826">Maldivas</a> (<a href="http://www.wikidata.org/entity/Q826">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q826">Maldivas</a> (<a href="http://www.wikidata.org/entity/Q826">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q826">Maldivas</a> (<a href="http://www.wikidata.org/entity/Q826">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q826">Maldivas</a> (<a href="http://www.wikidata.org/entity/Q826">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q826">Maldivas</a> (<a href="http://www.wikidata.org/entity/Q826">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q826">Maldivas</a> (<a href="http://www.wikidata.org/entity/Q826">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q826">Maldivas</a> (<a href="http://www.wikidata.org/entity/Q826">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q912">Mali</a> (<a href="http://www.wikidata.org/entity/Q912">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q233">Malta</a> (<a href="http://www.wikidata.org/entity/Q233">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q233">Malta</a> (<a href="http://www.wikidata.org/entity/Q233">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q233">Malta</a> (<a href="http://www.wikidata.org/entity/Q233">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>117</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>108</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>107</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>107</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>106</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>105</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>99</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>93</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>89</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q833">Malásia</a> (<a href="http://www.wikidata.org/entity/Q833">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>250</td>
    <td><a href="https://scholia.toolforge.org/Q1028">Marrocos</a> (<a href="http://www.wikidata.org/entity/Q1028">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1025">Mauritânia</a> (<a href="http://www.wikidata.org/entity/Q1025">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1027">Maurícia</a> (<a href="http://www.wikidata.org/entity/Q1027">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>182</td>
    <td><a href="https://scholia.toolforge.org/Q217">Moldávia</a> (<a href="http://www.wikidata.org/entity/Q217">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>143</td>
    <td><a href="https://scholia.toolforge.org/Q217">Moldávia</a> (<a href="http://www.wikidata.org/entity/Q217">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>116</td>
    <td><a href="https://scholia.toolforge.org/Q217">Moldávia</a> (<a href="http://www.wikidata.org/entity/Q217">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>73</td>
    <td><a href="https://scholia.toolforge.org/Q217">Moldávia</a> (<a href="http://www.wikidata.org/entity/Q217">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q217">Moldávia</a> (<a href="http://www.wikidata.org/entity/Q217">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q217">Moldávia</a> (<a href="http://www.wikidata.org/entity/Q217">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q236">Montenegro</a> (<a href="http://www.wikidata.org/entity/Q236">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q836">Myanmar</a> (<a href="http://www.wikidata.org/entity/Q836">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q836">Myanmar</a> (<a href="http://www.wikidata.org/entity/Q836">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>32796</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>32784</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>32615</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>32337</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>32004</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>31674</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>31298</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>30908</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>27769</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>27121</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>26648</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>25779</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>23337</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>20781</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>17580</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>15357</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>14649</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>13699</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>13170</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>9930</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>3926</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>3353</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>2961</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>2271</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>1972</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1859</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>1569</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1434</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>1351</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>1305</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>857</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>712</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>686</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>650</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>546</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>406</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>141</td>
    <td><a href="https://scholia.toolforge.org/Q96">México</a> (<a href="http://www.wikidata.org/entity/Q96">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q235">Mónaco</a> (<a href="http://www.wikidata.org/entity/Q235">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q837">Nepal</a> (<a href="http://www.wikidata.org/entity/Q837">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>74</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q811">Nicarágua</a> (<a href="http://www.wikidata.org/entity/Q811">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>158</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>143</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>93</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>87</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>68</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>51</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1033">Nigéria</a> (<a href="http://www.wikidata.org/entity/Q1033">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>228</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>220</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>220</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>213</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>209</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>209</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>209</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>208</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>208</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>204</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>204</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>202</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>195</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>193</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>193</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>193</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>180</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>169</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>163</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>154</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>130</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>127</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>114</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>98</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>88</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>69</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>59</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>42</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q20">Noruega</a> (<a href="http://www.wikidata.org/entity/Q20">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q664">Nova Zelândia</a> (<a href="http://www.wikidata.org/entity/Q664">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>47</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>37</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q1032">Níger</a> (<a href="http://www.wikidata.org/entity/Q1032">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>75</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q842">Omã</a> (<a href="http://www.wikidata.org/entity/Q842">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>819</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>770</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>747</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>720</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>698</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>667</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>645</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>631</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>620</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>604</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>592</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>575</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>564</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>547</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>536</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>521</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-21</td>
    <td>501</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>493</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>485</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>475</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>470</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-16</td>
    <td>457</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>448</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>437</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>428</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>421</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>418</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>413</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>403</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>398</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>393</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>799</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>799</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>386</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-05</td>
    <td>370</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>363</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-03</td>
    <td>357</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>352</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>344</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>336</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>330</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>326</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>320</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>315</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>313</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>310</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>306</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>299</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>295</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>291</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>287</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>281</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>279</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>275</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>269</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>266</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>260</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>256</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>252</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>249</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>244</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>237</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>231</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>225</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>218</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>210</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>203</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>200</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>197</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>192</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>188</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>178</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>167</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>165</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>159</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>141</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>136</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>126</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>120</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>115</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>95</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>37</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q804">Panamá</a> (<a href="http://www.wikidata.org/entity/Q804">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>2067</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>737</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>667</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>636</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>585</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>564</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>526</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>476</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>440</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>385</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>292</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>281</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>224</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>209</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>192</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>124</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q843">Paquistão</a> (<a href="http://www.wikidata.org/entity/Q843">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q733">Paraguai</a> (<a href="http://www.wikidata.org/entity/Q733">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>6113</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>5903</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>5871</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>5856</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>5830</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>5822</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>5811</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>5788</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>5775</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>5748</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>5715</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>5694</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>5680</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>5670</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>5643</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>5590</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>5562</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>5510</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>5456</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>5440</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>5422</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>5359</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>5288</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>5204</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>5168</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>5082</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>5056</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>4987</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>4893</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>4795</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>4711</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>4566</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>4518</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>4475</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>4409</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>4289</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>4177</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>4054</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>3916</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>3751</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>3684</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>3601</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>3459</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>3315</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>3134</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>2945</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>2823</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>2737</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>2643</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>2511</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>2396</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>2248</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>2101</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>1867</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>1766</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>1651</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>1487</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>1339</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>1173</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>1039</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>864</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>771</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>639</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>546</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>434</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>356</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>276</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>213</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>179</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>136</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>106</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>76</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q55">Países Baixos</a> (<a href="http://www.wikidata.org/entity/Q55">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>10958</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>9860</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>9677</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>9504</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>9317</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>8586</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>7861</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>6860</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>5738</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>5571</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>5465</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>5465</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>5162</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>2789</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>2057</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>1889</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>1814</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1533</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1344</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>1124</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1051</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>854</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>782</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>728</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>700</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>484</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>445</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>400</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>348</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>300</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>231</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>139</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q419">Peru</a> (<a href="http://www.wikidata.org/entity/Q419">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>1492</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>1477</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>1463</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>1334</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>1316</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>1206</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>1166</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>1064</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>1051</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>1024</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>1007</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>996</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>972</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>948</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>925</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>907</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>883</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>861</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>839</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>811</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>800</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>785</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>776</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>755</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>733</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>716</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>698</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>678</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>664</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>651</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>644</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>624</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>596</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>562</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>535</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>535</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>524</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>454</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>426</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>401</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>380</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>360</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>347</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>332</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>314</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>286</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>263</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>245</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>232</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>208</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>181</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>174</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>159</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>129</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>107</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>71</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>57</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q36">Polónia</a> (<a href="http://www.wikidata.org/entity/Q36">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>1163</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>1135</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1089</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>1074</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1063</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>1043</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>1023</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1007</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>989</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>973</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>948</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>928</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>903</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>880</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>854</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>820</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>785</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>762</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>735</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>714</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>687</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>657</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>629</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>599</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>567</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>535</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>504</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>470</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>435</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>409</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>380</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>345</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>311</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>295</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>266</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>246</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>209</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>187</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>160</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>140</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>119</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>100</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>76</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>60</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>33</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q45">Portugal</a> (<a href="http://www.wikidata.org/entity/Q45">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q813">Quirguistão</a> (<a href="http://www.wikidata.org/entity/Q813">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>32</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q114">Quénia</a> (<a href="http://www.wikidata.org/entity/Q114">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>43730</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>41698</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>37837</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>37460</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>37048</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>36914</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>36793</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>36675</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>36393</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>36042</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>35704</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>35341</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>34796</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>34636</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>34466</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>33998</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>33614</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>33186</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>32692</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>32065</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>31855</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>31587</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>31241</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>30615</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>30076</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>29427</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>28734</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>28446</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>28131</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>27510</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>26771</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>26097</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>21678</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>21092</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>20732</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>20319</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>19506</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>18738</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>18100</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>17337</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>16509</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>16060</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>15464</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>14576</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>13729</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>12868</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>12107</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>11329</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>10612</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>9875</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>8958</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>7978</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>7097</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>6159</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>5373</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>4934</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>4313</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>3605</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>2921</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>2352</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>1789</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>1408</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>1228</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>1019</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>759</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>578</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>463</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>422</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>335</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>281</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>233</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>177</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>144</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q145">Reino Unido</a> (<a href="http://www.wikidata.org/entity/Q145">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>347</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>283</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>262</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>201</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>132</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>112</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>91</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>78</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>78</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>67</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>59</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>53</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>39</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q213">República Checa</a> (<a href="http://www.wikidata.org/entity/Q213">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q974">República Democrática do Congo</a> (<a href="http://www.wikidata.org/entity/Q974">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q974">República Democrática do Congo</a> (<a href="http://www.wikidata.org/entity/Q974">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q974">República Democrática do Congo</a> (<a href="http://www.wikidata.org/entity/Q974">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q974">República Democrática do Congo</a> (<a href="http://www.wikidata.org/entity/Q974">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>794</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>786</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>775</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>765</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>754</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>747</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>733</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>726</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>712</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>691</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>536</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>502</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>409</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>402</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>388</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>385</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>362</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>354</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>346</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>326</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>313</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>293</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>286</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>282</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>278</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>260</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>245</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>235</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>226</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>217</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>189</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>196</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>183</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>68</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q786">República Dominicana</a> (<a href="http://www.wikidata.org/entity/Q786">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q23681">República Turca do Chipre do Norte</a> (<a href="http://www.wikidata.org/entity/Q23681">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>1488</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>1446</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1375</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1319</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1265</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1232</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>1159</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>730</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>334</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q27">República da Irlanda</a> (<a href="http://www.wikidata.org/entity/Q27">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q971">República do Congo</a> (<a href="http://www.wikidata.org/entity/Q971">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q971">República do Congo</a> (<a href="http://www.wikidata.org/entity/Q971">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q971">República do Congo</a> (<a href="http://www.wikidata.org/entity/Q971">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>1262</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>1253</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>1240</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>1229</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>1219</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>1210</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>1193</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>1179</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>1170</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>1159</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>1151</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>1141</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>1126</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>1107</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>1097</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>1081</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>1056</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>1046</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>1016</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>991</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>972</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>952</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>926</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>898</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>876</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>854</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>864</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>827</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>803</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>780</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>755</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>726</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>695</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>675</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>650</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>631</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>608</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>575</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>552</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>527</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>508</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>482</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>451</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>434</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>417</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>400</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>387</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>362</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>332</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>318</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>306</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>257</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>229</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>209</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>182</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>157</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>148</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>141</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>116</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>94</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>85</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>282</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>69</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>29</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q218">Roménia</a> (<a href="http://www.wikidata.org/entity/Q218">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>3388</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>3249</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>3099</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>2972</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>2837</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>2722</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>2631</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>2537</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>2418</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>2305</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>2212</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>2116</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>2009</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>1915</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>1827</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>1723</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>1625</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1537</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>1451</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1356</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>1280</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>1222</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1169</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1073</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>972</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>867</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>794</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>747</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>681</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>615</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>555</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>513</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>456</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>405</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>361</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>313</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>273</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>232</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>198</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>170</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>148</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>130</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>106</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>94</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>76</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>63</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>47</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q159">Rússia</a> (<a href="http://www.wikidata.org/entity/Q159">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q238">San Marino</a> (<a href="http://www.wikidata.org/entity/Q238">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q238">San Marino</a> (<a href="http://www.wikidata.org/entity/Q238">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q238">San Marino</a> (<a href="http://www.wikidata.org/entity/Q238">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q238">San Marino</a> (<a href="http://www.wikidata.org/entity/Q238">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q238">San Marino</a> (<a href="http://www.wikidata.org/entity/Q238">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q238">San Marino</a> (<a href="http://www.wikidata.org/entity/Q238">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-01</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q238">San Marino</a> (<a href="http://www.wikidata.org/entity/Q238">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q1041">Senegal</a> (<a href="http://www.wikidata.org/entity/Q1041">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q1041">Senegal</a> (<a href="http://www.wikidata.org/entity/Q1041">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q1041">Senegal</a> (<a href="http://www.wikidata.org/entity/Q1041">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q1041">Senegal</a> (<a href="http://www.wikidata.org/entity/Q1041">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q1041">Senegal</a> (<a href="http://www.wikidata.org/entity/Q1041">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q1041">Senegal</a> (<a href="http://www.wikidata.org/entity/Q1041">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1041">Senegal</a> (<a href="http://www.wikidata.org/entity/Q1041">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1041">Senegal</a> (<a href="http://www.wikidata.org/entity/Q1041">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q1044">Serra Leoa</a> (<a href="http://www.wikidata.org/entity/Q1044">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q1044">Serra Leoa</a> (<a href="http://www.wikidata.org/entity/Q1044">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q1044">Serra Leoa</a> (<a href="http://www.wikidata.org/entity/Q1044">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q1044">Serra Leoa</a> (<a href="http://www.wikidata.org/entity/Q1044">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q1044">Serra Leoa</a> (<a href="http://www.wikidata.org/entity/Q1044">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q1044">Serra Leoa</a> (<a href="http://www.wikidata.org/entity/Q1044">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q1044">Serra Leoa</a> (<a href="http://www.wikidata.org/entity/Q1044">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>26</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q334">Singapura</a> (<a href="http://www.wikidata.org/entity/Q334">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q1045">Somália</a> (<a href="http://www.wikidata.org/entity/Q1045">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q1045">Somália</a> (<a href="http://www.wikidata.org/entity/Q1045">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>39</td>
    <td><a href="https://scholia.toolforge.org/Q1045">Somália</a> (<a href="http://www.wikidata.org/entity/Q1045">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>35</td>
    <td><a href="https://scholia.toolforge.org/Q1045">Somália</a> (<a href="http://www.wikidata.org/entity/Q1045">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q1045">Somália</a> (<a href="http://www.wikidata.org/entity/Q1045">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q1045">Somália</a> (<a href="http://www.wikidata.org/entity/Q1045">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q1045">Somália</a> (<a href="http://www.wikidata.org/entity/Q1045">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1045">Somália</a> (<a href="http://www.wikidata.org/entity/Q1045">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q854">Sri Lanka</a> (<a href="http://www.wikidata.org/entity/Q854">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>91</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>80</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>64</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1049">Sudão</a> (<a href="http://www.wikidata.org/entity/Q1049">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q730">Suriname</a> (<a href="http://www.wikidata.org/entity/Q730">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q730">Suriname</a> (<a href="http://www.wikidata.org/entity/Q730">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q730">Suriname</a> (<a href="http://www.wikidata.org/entity/Q730">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q730">Suriname</a> (<a href="http://www.wikidata.org/entity/Q730">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>5333</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>4874</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>4266</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>4220</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>4125</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>4029</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>3992</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>3871</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>3831</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>3743</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>3698</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>3679</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>3674</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>3646</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>3529</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>3460</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>3313</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>3256</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>3225</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>3220</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>3175</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>3040</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>2941</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>2854</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>2769</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>2679</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>2669</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>2653</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>2586</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>2462</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>2355</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>2274</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>2194</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>2192</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>2152</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>2021</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1937</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>1765</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>1580</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>1540</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>1511</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>1400</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>1333</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>1203</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>1033</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>919</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>899</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>887</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>870</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>793</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>687</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>591</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>477</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>401</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>373</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>333</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>282</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>239</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>180</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>146</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>110</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>102</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>92</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>66</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>42</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q34">Suécia</a> (<a href="http://www.wikidata.org/entity/Q34">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>1867</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>1833</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1805</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1784</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1737</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>1337</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>1217</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>1111</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>1059</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>1017</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>973</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>858</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>641</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>559</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>540</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>484</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>378</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>373</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>295</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>257</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>235</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>197</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>161</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>66</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>60</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q39">Suíça</a> (<a href="http://www.wikidata.org/entity/Q39">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q1039">São Tomé e Príncipe</a> (<a href="http://www.wikidata.org/entity/Q1039">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>220</td>
    <td><a href="https://scholia.toolforge.org/Q403">Sérvia</a> (<a href="http://www.wikidata.org/entity/Q403">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>203</td>
    <td><a href="https://scholia.toolforge.org/Q403">Sérvia</a> (<a href="http://www.wikidata.org/entity/Q403">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>130</td>
    <td><a href="https://scholia.toolforge.org/Q403">Sérvia</a> (<a href="http://www.wikidata.org/entity/Q403">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q403">Sérvia</a> (<a href="http://www.wikidata.org/entity/Q403">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q858">Síria</a> (<a href="http://www.wikidata.org/entity/Q858">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>57</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>55</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>30</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q869">Tailândia</a> (<a href="http://www.wikidata.org/entity/Q869">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q865">Taiwan</a> (<a href="http://www.wikidata.org/entity/Q865">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q863">Tajiquistão</a> (<a href="http://www.wikidata.org/entity/Q863">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q863">Tajiquistão</a> (<a href="http://www.wikidata.org/entity/Q863">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q863">Tajiquistão</a> (<a href="http://www.wikidata.org/entity/Q863">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q863">Tajiquistão</a> (<a href="http://www.wikidata.org/entity/Q863">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q863">Tajiquistão</a> (<a href="http://www.wikidata.org/entity/Q863">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q863">Tajiquistão</a> (<a href="http://www.wikidata.org/entity/Q863">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q924">Tanzânia</a> (<a href="http://www.wikidata.org/entity/Q924">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q945">Togo</a> (<a href="http://www.wikidata.org/entity/Q945">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q754">Trinidad e Tobago</a> (<a href="http://www.wikidata.org/entity/Q754">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-05</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-03</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>47</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>47</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>47</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>47</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>46</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>45</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>43</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>42</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>42</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>41</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>40</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>39</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>37</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>37</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>37</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>36</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>24</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>22</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q948">Tunísia</a> (<a href="http://www.wikidata.org/entity/Q948">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>5131</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>4692</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>3894</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>3584</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>3461</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>3174</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>2992</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>2259</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>1518</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>1198</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>908</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>108</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q43">Turquia</a> (<a href="http://www.wikidata.org/entity/Q43">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>810</td>
    <td><a href="https://scholia.toolforge.org/Q212">Ucrânia</a> (<a href="http://www.wikidata.org/entity/Q212">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>439</td>
    <td><a href="https://scholia.toolforge.org/Q212">Ucrânia</a> (<a href="http://www.wikidata.org/entity/Q212">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>340</td>
    <td><a href="https://scholia.toolforge.org/Q212">Ucrânia</a> (<a href="http://www.wikidata.org/entity/Q212">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>174</td>
    <td><a href="https://scholia.toolforge.org/Q212">Ucrânia</a> (<a href="http://www.wikidata.org/entity/Q212">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>52</td>
    <td><a href="https://scholia.toolforge.org/Q212">Ucrânia</a> (<a href="http://www.wikidata.org/entity/Q212">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q212">Ucrânia</a> (<a href="http://www.wikidata.org/entity/Q212">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>27</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>23</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>19</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>15</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>14</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>12</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q77">Uruguai</a> (<a href="http://www.wikidata.org/entity/Q77">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q265">Uzbequistão</a> (<a href="http://www.wikidata.org/entity/Q265">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>54</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>51</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>48</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>44</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>20</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>18</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>11</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q717">Venezuela</a> (<a href="http://www.wikidata.org/entity/Q717">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q954">Zimbábue</a> (<a href="http://www.wikidata.org/entity/Q954">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q954">Zimbábue</a> (<a href="http://www.wikidata.org/entity/Q954">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q954">Zimbábue</a> (<a href="http://www.wikidata.org/entity/Q954">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q954">Zimbábue</a> (<a href="http://www.wikidata.org/entity/Q954">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q954">Zimbábue</a> (<a href="http://www.wikidata.org/entity/Q954">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q954">Zimbábue</a> (<a href="http://www.wikidata.org/entity/Q954">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q953">Zâmbia</a> (<a href="http://www.wikidata.org/entity/Q953">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q953">Zâmbia</a> (<a href="http://www.wikidata.org/entity/Q953">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q953">Zâmbia</a> (<a href="http://www.wikidata.org/entity/Q953">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q953">Zâmbia</a> (<a href="http://www.wikidata.org/entity/Q953">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q953">Zâmbia</a> (<a href="http://www.wikidata.org/entity/Q953">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q953">Zâmbia</a> (<a href="http://www.wikidata.org/entity/Q953">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q953">Zâmbia</a> (<a href="http://www.wikidata.org/entity/Q953">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>194</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>153</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>138</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>116</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>103</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>79</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>65</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>34</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>5</td>
    <td><a href="https://scholia.toolforge.org/Q258">África do Sul</a> (<a href="http://www.wikidata.org/entity/Q258">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>705</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>705</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>705</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>703</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>702</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>700</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>698</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>698</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>693</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>693</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>690</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-21</td>
    <td>690</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>688</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>688</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>688</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>687</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-16</td>
    <td>681</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>678</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>677</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>677</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>675</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>674</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>673</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>672</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>672</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>672</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>672</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-05</td>
    <td>672</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>670</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-03</td>
    <td>670</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>669</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>668</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>668</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>668</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>668</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>668</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>645</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>643</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>641</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>640</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>639</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>635</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>633</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>633</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>632</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>629</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>629</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>629</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>628</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>626</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>624</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>623</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>620</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>618</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>615</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>614</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>609</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>608</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>606</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>600</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>598</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>596</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>589</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>584</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>580</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>569</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>549</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>542</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>536</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>530</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>522</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>494</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>510</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>463</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>491</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>470</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>452</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>443</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>431</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>410</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>393</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>384</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>368</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>350</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>337</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>319</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>295</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>273</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>243</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>220</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>204</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>186</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>168</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>158</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>146</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>128</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>108</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>86</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>68</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>58</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>49</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>31</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>28</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>21</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>16</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>8</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>6</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q40">Áustria</a> (<a href="http://www.wikidata.org/entity/Q40">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-13</td>
    <td>23174</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-12</td>
    <td>22674</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-11</td>
    <td>22123</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-10</td>
    <td>21604</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-09</td>
    <td>21129</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-08</td>
    <td>20642</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-07</td>
    <td>20160</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-06</td>
    <td>19693</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-05</td>
    <td>19268</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-04</td>
    <td>18655</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-03</td>
    <td>18213</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-02</td>
    <td>17834</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-07-01</td>
    <td>17400</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>16893</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-29</td>
    <td>16475</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-28</td>
    <td>16095</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-27</td>
    <td>15685</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-26</td>
    <td>15301</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-25</td>
    <td>14894</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-24</td>
    <td>14476</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-23</td>
    <td>14011</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-22</td>
    <td>13699</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-21</td>
    <td>13254</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-20</td>
    <td>12948</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-19</td>
    <td>12573</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-18</td>
    <td>12237</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-17</td>
    <td>11903</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-16</td>
    <td>9900</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-15</td>
    <td>9520</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-14</td>
    <td>9195</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-13</td>
    <td>8884</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-12</td>
    <td>8498</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-11</td>
    <td>8102</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-10</td>
    <td>7745</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-09</td>
    <td>7471</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-08</td>
    <td>7200</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-07</td>
    <td>6929</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-06</td>
    <td>6642</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-05</td>
    <td>6348</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-04</td>
    <td>6075</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-03</td>
    <td>5815</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-02</td>
    <td>5598</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-06-01</td>
    <td>5394</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-31</td>
    <td>5164</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-30</td>
    <td>4971</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-29</td>
    <td>4706</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>4531</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>4337</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>4167</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>4021</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>3867</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>3720</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>3583</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>3435</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>3303</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>3163</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>3029</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>2872</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>2752</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>2649</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>2549</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>2415</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>2293</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>2206</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>2109</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>1981</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>1886</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>1783</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>1694</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>1583</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>1389</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>1306</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>1223</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>1152</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>934</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>872</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>681</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>640</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>590</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>543</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>507</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>480</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>437</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>414</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>377</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>339</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>308</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>273</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>239</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>199</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>166</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>149</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>109</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>77</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>56</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>50</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>38</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>25</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>17</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>13</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>10</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>9</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>7</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>4</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>3</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>2</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>1</td>
    <td><a href="https://scholia.toolforge.org/Q668">Índia</a> (<a href="http://www.wikidata.org/entity/Q668">edit</a>)</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o graphDeaths.rq https://raw.githubusercontent.com/egonw/SARS-CoV-2-Queries/master/sparql/graphDeaths.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@graphDeaths.rq
```
This SPARQL query is available under CCZero.

# progressionNL.rq
**コード例:** [curl](#curl)
### SPARQL
```sparql
SELECT ?date ?numberOfCases WHERE {
  wd:Q86756826 p:P1603 ?numberOfCasesStat .
  ?numberOfCasesStat ps:P1603 ?numberOfCases ;
                     pq:P585 ?date .
  SERVICE wikibase:label { bd:serviceParam wikibase:language "ja,en". }
} ORDER BY DESC(?date)
```
[実行](https://query.wikidata.org/embed.html#SELECT%20%3Fdate%20%3FnumberOfCases%20WHERE%20%7B%0A%20%20wd%3AQ86756826%20p%3AP1603%20%3FnumberOfCasesStat%20.%0A%20%20%3FnumberOfCasesStat%20ps%3AP1603%20%3FnumberOfCases%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20pq%3AP585%20%3Fdate%20.%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22ja%2Cen%22.%20%7D%0A%7D%20ORDER%20BY%20DESC%28%3Fdate%29%0A) もしくは [編集](https://query.wikidata.org/#SELECT%20%3Fdate%20%3FnumberOfCases%20WHERE%20%7B%0A%20%20wd%3AQ86756826%20p%3AP1603%20%3FnumberOfCasesStat%20.%0A%20%20%3FnumberOfCasesStat%20ps%3AP1603%20%3FnumberOfCases%20%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20pq%3AP585%20%3Fdate%20.%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22ja%2Cen%22.%20%7D%0A%7D%20ORDER%20BY%20DESC%28%3Fdate%29%0A)


### 結果
<table>
  <tr>
    <td><b>date</b></td>
    <td><b>numberOfCases</b></td>
  </tr>
  <tr>
    <td>2020-06-30</td>
    <td>50273</td>
  </tr>
  <tr>
    <td>2020-05-28</td>
    <td>45950</td>
  </tr>
  <tr>
    <td>2020-05-27</td>
    <td>45768</td>
  </tr>
  <tr>
    <td>2020-05-26</td>
    <td>45578</td>
  </tr>
  <tr>
    <td>2020-05-25</td>
    <td>45445</td>
  </tr>
  <tr>
    <td>2020-05-24</td>
    <td>45236</td>
  </tr>
  <tr>
    <td>2020-05-23</td>
    <td>45064</td>
  </tr>
  <tr>
    <td>2020-05-22</td>
    <td>44888</td>
  </tr>
  <tr>
    <td>2020-05-21</td>
    <td>44700</td>
  </tr>
  <tr>
    <td>2020-05-20</td>
    <td>44447</td>
  </tr>
  <tr>
    <td>2020-05-19</td>
    <td>44249</td>
  </tr>
  <tr>
    <td>2020-05-18</td>
    <td>44141</td>
  </tr>
  <tr>
    <td>2020-05-17</td>
    <td>43995</td>
  </tr>
  <tr>
    <td>2020-05-16</td>
    <td>43870</td>
  </tr>
  <tr>
    <td>2020-05-15</td>
    <td>43681</td>
  </tr>
  <tr>
    <td>2020-05-14</td>
    <td>43481</td>
  </tr>
  <tr>
    <td>2020-05-13</td>
    <td>43211</td>
  </tr>
  <tr>
    <td>2020-05-12</td>
    <td>42984</td>
  </tr>
  <tr>
    <td>2020-05-11</td>
    <td>42788</td>
  </tr>
  <tr>
    <td>2020-05-10</td>
    <td>42627</td>
  </tr>
  <tr>
    <td>2020-05-09</td>
    <td>42382</td>
  </tr>
  <tr>
    <td>2020-05-08</td>
    <td>42093</td>
  </tr>
  <tr>
    <td>2020-05-07</td>
    <td>41774</td>
  </tr>
  <tr>
    <td>2020-05-06</td>
    <td>41319</td>
  </tr>
  <tr>
    <td>2020-05-05</td>
    <td>41087</td>
  </tr>
  <tr>
    <td>2020-05-04</td>
    <td>40770</td>
  </tr>
  <tr>
    <td>2020-05-03</td>
    <td>40571</td>
  </tr>
  <tr>
    <td>2020-05-02</td>
    <td>40236</td>
  </tr>
  <tr>
    <td>2020-05-01</td>
    <td>39791</td>
  </tr>
  <tr>
    <td>2020-04-30</td>
    <td>39316</td>
  </tr>
  <tr>
    <td>2020-04-29</td>
    <td>38802</td>
  </tr>
  <tr>
    <td>2020-04-28</td>
    <td>38416</td>
  </tr>
  <tr>
    <td>2020-04-27</td>
    <td>38245</td>
  </tr>
  <tr>
    <td>2020-04-26</td>
    <td>37845</td>
  </tr>
  <tr>
    <td>2020-04-25</td>
    <td>37190</td>
  </tr>
  <tr>
    <td>2020-04-24</td>
    <td>36535</td>
  </tr>
  <tr>
    <td>2020-04-23</td>
    <td>35729</td>
  </tr>
  <tr>
    <td>2020-04-22</td>
    <td>34842</td>
  </tr>
  <tr>
    <td>2020-04-21</td>
    <td>34134</td>
  </tr>
  <tr>
    <td>2020-04-20</td>
    <td>33405</td>
  </tr>
  <tr>
    <td>2020-04-19</td>
    <td>32655</td>
  </tr>
  <tr>
    <td>2020-04-18</td>
    <td>31589</td>
  </tr>
  <tr>
    <td>2020-04-17</td>
    <td>30449</td>
  </tr>
  <tr>
    <td>2020-04-16</td>
    <td>29214</td>
  </tr>
  <tr>
    <td>2020-04-15</td>
    <td>28153</td>
  </tr>
  <tr>
    <td>2020-04-14</td>
    <td>27419</td>
  </tr>
  <tr>
    <td>2020-04-13</td>
    <td>26551</td>
  </tr>
  <tr>
    <td>2020-04-12</td>
    <td>25587</td>
  </tr>
  <tr>
    <td>2020-04-11</td>
    <td>24413</td>
  </tr>
  <tr>
    <td>2020-04-10</td>
    <td>23097</td>
  </tr>
  <tr>
    <td>2020-04-09</td>
    <td>21762</td>
  </tr>
  <tr>
    <td>2020-04-08</td>
    <td>20549</td>
  </tr>
  <tr>
    <td>2020-04-07</td>
    <td>19580</td>
  </tr>
  <tr>
    <td>2020-04-06</td>
    <td>18803</td>
  </tr>
  <tr>
    <td>2020-04-05</td>
    <td>17851</td>
  </tr>
  <tr>
    <td>2020-04-04</td>
    <td>16627</td>
  </tr>
  <tr>
    <td>2020-04-03</td>
    <td>15723</td>
  </tr>
  <tr>
    <td>2020-04-02</td>
    <td>14697</td>
  </tr>
  <tr>
    <td>2020-04-01</td>
    <td>13614</td>
  </tr>
  <tr>
    <td>2020-03-31</td>
    <td>12595</td>
  </tr>
  <tr>
    <td>2020-03-30</td>
    <td>11750</td>
  </tr>
  <tr>
    <td>2020-03-29</td>
    <td>10866</td>
  </tr>
  <tr>
    <td>2020-03-28</td>
    <td>9762</td>
  </tr>
  <tr>
    <td>2020-03-27</td>
    <td>8603</td>
  </tr>
  <tr>
    <td>2020-03-26</td>
    <td>7431</td>
  </tr>
  <tr>
    <td>2020-03-25</td>
    <td>6412</td>
  </tr>
  <tr>
    <td>2020-03-24</td>
    <td>5560</td>
  </tr>
  <tr>
    <td>2020-03-23</td>
    <td>4749</td>
  </tr>
  <tr>
    <td>2020-03-22</td>
    <td>4204</td>
  </tr>
  <tr>
    <td>2020-03-21</td>
    <td>3631</td>
  </tr>
  <tr>
    <td>2020-03-20</td>
    <td>2994</td>
  </tr>
  <tr>
    <td>2020-03-19</td>
    <td>2460</td>
  </tr>
  <tr>
    <td>2020-03-18</td>
    <td>2051</td>
  </tr>
  <tr>
    <td>2020-03-17</td>
    <td>1705</td>
  </tr>
  <tr>
    <td>2020-03-16</td>
    <td>1413</td>
  </tr>
  <tr>
    <td>2020-03-15</td>
    <td>1135</td>
  </tr>
  <tr>
    <td>2020-03-14</td>
    <td>959</td>
  </tr>
  <tr>
    <td>2020-03-13</td>
    <td>804</td>
  </tr>
  <tr>
    <td>2020-03-12</td>
    <td>614</td>
  </tr>
  <tr>
    <td>2020-03-11</td>
    <td>503</td>
  </tr>
  <tr>
    <td>2020-03-10</td>
    <td>382</td>
  </tr>
  <tr>
    <td>2020-03-09</td>
    <td>321</td>
  </tr>
  <tr>
    <td>2020-03-08</td>
    <td>265</td>
  </tr>
  <tr>
    <td>2020-03-07</td>
    <td>188</td>
  </tr>
  <tr>
    <td>2020-03-06</td>
    <td>128</td>
  </tr>
  <tr>
    <td>2020-03-05</td>
    <td>82</td>
  </tr>
  <tr>
    <td>2020-03-04</td>
    <td>38</td>
  </tr>
  <tr>
    <td>2020-03-02</td>
    <td>18</td>
  </tr>
  <tr>
    <td>2020-03-01</td>
    <td>10</td>
  </tr>
  <tr>
    <td>2020-02-28</td>
    <td>2</td>
  </tr>
  <tr>
    <td>2020-02-27</td>
    <td>1</td>
  </tr>
</table>
## コード例
### curl
```shell
curl -o progressionNL.rq https://raw.githubusercontent.com/egonw/SARS-CoV-2-Queries/master/sparql/progressionNL.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@progressionNL.rq
```
本SPARQLクエリはCC0ライセンスで利用可能です。

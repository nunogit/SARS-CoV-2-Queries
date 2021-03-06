# 解決に向けて

SARS-CoV-2の問題に対して現状では解決方法がありません。

しかし、解決方法になりうるアイデアは幾つかあります。ワクチンがその一つですが、その開発には時間を要します[<cite>Q87461271</cite>]。
また、抗体や、SARS-CoV-2にも有効である既存の薬、つまり既存薬再開発についての議論もされていますが、現在これらは全て研究段階です。
そして、臨床試験は重要です（[臨床試験](https://egonw.github.io/SARS-CoV-2-Queries/covid.html#clinical-trials)を参照）。

本章では、解決に繋がりそうな提案に関する、Wikidataに収められている情報を取得するクエリを幾つか提示します。

## 抗体

抗体は関心を集めつつあります。次のクエリ集はヒトコロナウイルスについての文献で、<topic>抗体</topic>という注釈がつけられているものを取得します。

<sparql>antibodies</sparql>

このクエリの結果は長くなるので、それぞれのウイルスに対する抗体についての論文数を見てみましょう。

<out>antibodyCounts</out>

なお、抗体は個々のタンパク質に特化しているものであり、そして全てのコロナウイルスは異なるタンパク質を持ちます。
ですから、このクエリ集は単に読むべき関連論文を取得するためのショートカットであり、決してそこから結論を導き出すものではないことを強調しておきます。

<out limit="15">antibodies</out>

## ワクチン

いつかは、SARS-CoV-2から我々を守ってくれるワクチンが得られるかもしれません。
現時点で幾つかの候補が研究されています[<cite>Q91131712</cite>]。
それらのうち、Wikidataに収められているものを以下のクエリで取得できます。

<sparql>vaccines</sparql>

現状ではそれほど多くありません。

<out limit="15">vaccines</out>

## 既存薬再開発

<xref>trials</xref>章で既に臨床試験の概要を取得しました。
そこでは、どのような症状に人は心配するのかについて知見を得られました。
また、どのような<topic>薬</topic>が<topic>既存薬再開発</topic>のために研究されているのか知ることができました。
大きな注目を浴びる薬もあれば、それほどでもないものもあります。これらは以下のような感じです。

<iframe>interventionStructures</iframe>

次のクエリにより、<topic>介入</topic>による臨床試験の事例一覧が得られます。

<sparql>clinicalTrialsByIntervention</sparql>

結果は以下のとおりです。

<out limit="15">clinicalTrialsByIntervention</out>

重要なことは、どのような介入がより多くの注目を集めているかを把握できるに過ぎない、ということです。
そして、注目度が成功度を測る指標ではないと認識することが肝要です。

## 参考文献

<references/>

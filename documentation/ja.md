<!-- ELUCENIA technical documentation · gradiente-alveolo-arterial · ja · no clinical/professional/rights approval -->

# 肺胞気–動脈血酸素分圧較差

[条件・出典・許諾](https://elucenia.org/ja/tools/gradiente-alveolo-arterial)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### FiO₂

`fio2`

% · 範囲: 21–100

### PaO₂

`pao2`

mmHg · 範囲: 20–700

### PaCO₂

`paco2`

mmHg · 範囲: 10–150

### 年齢

`idade`

年 · 範囲: 1–110

### 現地の気圧（既定値760）

`patm`

mmHg · 任意 · 範囲: 400–800

## 方法の版

肺胞式RQ 0.8/水蒸気47 mmHg；Mellemgaard 1966較差2.5+0.21年齢；年齢/4+4近似

## 記載された計算式

PAO₂ = FiO₂ × (Patm − 47) − PaCO₂ ÷ 0.8（呼吸商0.8；47 mmHg = 37 °Cの水蒸気圧）。

A-a較差 = PAO₂ − PaO₂。

室内気での期待値 = 2.5 + 0.21 × 年齢（Mellemgaard）。簡便式：年齢 ÷ 4 + 4。

## 限界・対象集団

計算には37 °Cで47 mmHgの水蒸気圧と、固定した呼吸商0.8を使用します。これは定常状態の仮定であり、呼吸商は食事により変わることがあります。FiO₂は百分率、圧力はmmHgで入力し、適切な気圧を指定してください。年齢による近似参考値を高いFiO₂や高地に自動的に外挿すべきではありません。この較差は酸素化の評価に役立ちますが、低酸素血症の原因を単独で特定しません。ローカル年齢参考式の係数は、引用された研究の全文での確認がなお必要です。

## 参考文献

- [Mellemgaard K. The alveolar-arterial oxygen difference: its size and components in normal man. Acta Physiol Scand, 1966.](https://doi.org/10.1111/j.1748-1716.1966.tb03281.x)

- [Hantzidiamantis PJ, Amaro E. Physiology, Alveolar to Arterial Oxygen Gradient. StatPearls (NCBI Bookshelf).](https://www.ncbi.nlm.nih.gov/books/NBK545153/)

- [Berend2014,NEJM,updated2014-10-16,primary article mirror](https://www.docenti.unina.it/webdocenti-be/allegati/materiale-didattico/443118)

- [Mellemgaard1966](https://onlinelibrary.wiley.com/doi/10.1111/j.1748-1716.1966.tb03281.x)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 記録された結果

以下の情報は、合成例に対する手法の出力を保持したものです。独立した臨床的検証を示すものではありません。

### 1

年齢に対して正常な勾配：低酸素血症がある場合は、低換気または吸入 O₂ 分圧低下による

| 結果の詳細 | |
| --- | --- |
| PAO₂（肺胞 O₂ 圧） | 100 mmHg |
| 年齢で予測される値（2,5 + 0,21 × 年齢） | 11 mmHg まで |
| 経験則（年齢 ÷ 4 + 4） | 14 mmHg |


### 2

年齢に対して上昇した勾配：V/Q 不均衡、シャント、または拡散障害を示唆

| 結果の詳細 | |
| --- | --- |
| PAO₂（肺胞 O₂ 圧） | 112 mmHg |
| 年齢で予測される値（2,5 + 0,21 × 年齢） | 15 mmHg まで |
| 経験則（年齢 ÷ 4 + 4） | 19 mmHg |


### 3

年齢に対して正常な勾配：低酸素血症がある場合は、低換気または吸入 O₂ 分圧低下による

| 結果の詳細 | |
| --- | --- |
| PAO₂（肺胞 O₂ 圧） | 62 mmHg |
| 年齢で予測される値（2,5 + 0,21 × 年齢） | 13 mmHg まで |
| 経験則（年齢 ÷ 4 + 4） | 17 mmHg |


### 4

年齢に対して正常な勾配：低酸素血症がある場合は、低換気または吸入 O₂ 分圧低下による

| 結果の詳細 | |
| --- | --- |
| PAO₂（肺胞 O₂ 圧） | 91 mmHg |
| 年齢で予測される値（2,5 + 0,21 × 年齢） | 9 mmHg まで |
| 経験則（年齢 ÷ 4 + 4） | 12 mmHg |


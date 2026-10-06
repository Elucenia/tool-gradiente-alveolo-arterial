<!-- ELUCENIA technical documentation · gradiente-alveolo-arterial · zh · no clinical/professional/rights approval -->

# 肺泡-动脉氧分压差

[条件、来源与许可](https://elucenia.org/zh/tools/gradiente-alveolo-arterial)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### FiO₂

`fio2`

% · 范围: 21–100

### PaO₂

`pao2`

mmHg · 范围: 20–700

### PaCO₂

`paco2`

mmHg · 范围: 10–150

### 年龄

`idade`

年 · 范围: 1–110

### 当地大气压（默认 760）

`patm`

mmHg · 选填 · 范围: 400–800

## 方法版本

肺泡方程RQ 0.8/水汽47 mmHg；Mellemgaard 1966梯度2.5+0.21年龄；年龄/4+4近似

## 已记录的公式

PAO₂ = FiO₂ × (Patm − 47) − PaCO₂ ÷ 0.8（呼吸商0.8；47 mmHg = 37 °C水蒸气压）。

A-a梯度 = PAO₂ − PaO₂。

空气呼吸预期值 = 2.5 + 0.21 × 年龄（Mellemgaard）。经验法：年龄 ÷ 4 + 4。

## 限制与适用人群

计算采用37 °C时47 mmHg的水蒸气压和固定呼吸商0.8；这是稳态假设，呼吸商可能随饮食变化。FiO₂请输入百分比，压力使用mmHg，并填写适当大气压。年龄近似参考值不应自动外推至高FiO₂或高海拔。该梯度有助于评估氧合，但不能单独确定低氧血症原因。本地年龄参考公式的系数仍需在所引完整研究中核对。

## 参考文献

- [Mellemgaard K. The alveolar-arterial oxygen difference: its size and components in normal man. Acta Physiol Scand, 1966.](https://doi.org/10.1111/j.1748-1716.1966.tb03281.x)

- [Hantzidiamantis PJ, Amaro E. Physiology, Alveolar to Arterial Oxygen Gradient. StatPearls (NCBI Bookshelf).](https://www.ncbi.nlm.nih.gov/books/NBK545153/)

- [Berend2014,NEJM,updated2014-10-16,primary article mirror](https://www.docenti.unina.it/webdocenti-be/allegati/materiale-didattico/443118)

- [Mellemgaard1966](https://onlinelibrary.wiley.com/doi/10.1111/j.1748-1716.1966.tb03281.x)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 已记录的结果

以下信息保留该方法对合成示例的输出，不构成独立的临床验证。

### 1

年龄相应的正常梯度：如有低氧血症，则由于低通气或吸入 O₂ 压力低

| 结果详情 | |
| --- | --- |
| PAO₂（肺泡 O₂ 压力） | 100 mmHg |
| 按年龄预期（2,5 + 0,21 × 年龄） | 最高 11 mmHg |
| 经验规则（年龄 ÷ 4 + 4） | 14 mmHg |


### 2

相对于年龄升高的梯度：提示 V/Q 失调、分流或弥散障碍

| 结果详情 | |
| --- | --- |
| PAO₂（肺泡 O₂ 压力） | 112 mmHg |
| 按年龄预期（2,5 + 0,21 × 年龄） | 最高 15 mmHg |
| 经验规则（年龄 ÷ 4 + 4） | 19 mmHg |


### 3

年龄相应的正常梯度：如有低氧血症，则由于低通气或吸入 O₂ 压力低

| 结果详情 | |
| --- | --- |
| PAO₂（肺泡 O₂ 压力） | 62 mmHg |
| 按年龄预期（2,5 + 0,21 × 年龄） | 最高 13 mmHg |
| 经验规则（年龄 ÷ 4 + 4） | 17 mmHg |


### 4

年龄相应的正常梯度：如有低氧血症，则由于低通气或吸入 O₂ 压力低

| 结果详情 | |
| --- | --- |
| PAO₂（肺泡 O₂ 压力） | 91 mmHg |
| 按年龄预期（2,5 + 0,21 × 年龄） | 最高 9 mmHg |
| 经验规则（年龄 ÷ 4 + 4） | 12 mmHg |


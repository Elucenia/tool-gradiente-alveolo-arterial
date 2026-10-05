<!-- ELUCENIA technical documentation · gradiente-alveolo-arterial · en · no clinical/professional/rights approval -->

# Alveolar–arterial O₂ gradient

[conditions, sources and permissions](https://elucenia.org/en/tools/gradiente-alveolo-arterial)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### FiO₂

`fio2`

% · range: 21–100

### PaO₂

`pao2`

mmHg · range: 20–700

### PaCO₂

`paco2`

mmHg · range: 10–150

### Age

`idade`

years · range: 1–110

### Local barometric pressure (default 760)

`patm`

mmHg · optional · range: 400–800

## Method edition

Alveolar equation RQ 0.8/vapour 47 mmHg; Mellemgaard 1966 gradient 2.5+0.21 age; age/4+4 approximation

## Documented formula

PAO₂ = FiO₂ × (Patm − 47) − PaCO₂ ÷ 0.8 (respiratory quotient 0.8; 47 mmHg = water vapour pressure at 37 °C).

A-a gradient = PAO₂ − PaO₂.

Expected on room air = 2.5 + 0.21 × age (Mellemgaard). Rule of thumb: age ÷ 4 + 4.

## Limits and population

The calculation uses a water-vapor pressure of 47 mmHg at 37 °C and a fixed respiratory quotient of 0.8; this is a steady-state assumption and can vary with diet. Enter FiO₂ as a percentage, pressures in mmHg and an appropriate barometric pressure. The approximate age-based reference must not be automatically extrapolated to high FiO₂ or altitude. The gradient helps assess oxygenation but does not, on its own, determine the cause of hypoxemia. The coefficients of the local age-based reference still require checking against the complete cited study.

## References

- [Mellemgaard K. The alveolar-arterial oxygen difference: its size and components in normal man. Acta Physiol Scand, 1966.](https://doi.org/10.1111/j.1748-1716.1966.tb03281.x)

- [Hantzidiamantis PJ, Amaro E. Physiology, Alveolar to Arterial Oxygen Gradient. StatPearls (NCBI Bookshelf).](https://www.ncbi.nlm.nih.gov/books/NBK545153/)

- [Berend2014,NEJM,updated2014-10-16,primary article mirror](https://www.docenti.unina.it/webdocenti-be/allegati/materiale-didattico/443118)

- [Mellemgaard1966](https://onlinelibrary.wiley.com/doi/10.1111/j.1748-1716.1966.tb03281.x)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

<!-- ELUCENIA technical documentation · gradiente-alveolo-arterial · pt-BR · no clinical/professional/rights approval -->

# Gradiente alvéolo-arterial de O₂

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/gradiente-alveolo-arterial)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### FiO₂

`fio2`

% · intervalo: 21–100

### PaO₂

`pao2`

mmHg · intervalo: 20–700

### PaCO₂

`paco2`

mmHg · intervalo: 10–150

### Idade

`idade`

anos · intervalo: 1–110

### Pressão barométrica local (padrão 760)

`patm`

mmHg · opcional · intervalo: 400–800

## Edição do método

Equaçãoalveolar RQ 0,8/vapor 47 mm Hg; gradiente Mellemgaard 1966 2,5+0,21 idade; aproximaçãoidade/4+4

## Fórmula documentada

PAO₂ = FiO₂ × (Patm − 47) − PaCO₂ ÷ 0,8 (quociente respiratório de 0,8; 47 mmHg = pressão de vapor d'água a 37 °C).

Gradiente A-a = PAO₂ − PaO₂.

Esperado em ar ambiente = 2,5 + 0,21 × idade (Mellemgaard). Regra prática: idade ÷ 4 + 4.

## Limites e população

O cálculo usa pressão de vapor d’água de 47 mmHg a 37 °C e quociente respiratório fixo de 0,8; este é um pressuposto de estado estável e pode variar com a dieta. Informe FiO₂ em porcentagem, pressões em mmHg e pressão barométrica apropriada. A referência aproximada por idade não deve ser extrapolada automaticamente para FiO₂ elevada ou altitude. O gradiente ajuda a avaliar oxigenação, mas não determina sozinho a causa da hipoxemia. Os coeficientes da referência local por idade ainda exigem conferência no estudo completo citado.

## Referências

- [Mellemgaard K. The alveolar-arterial oxygen difference: its size and components in normal man. Acta Physiol Scand, 1966.](https://doi.org/10.1111/j.1748-1716.1966.tb03281.x)

- [Hantzidiamantis PJ, Amaro E. Physiology, Alveolar to Arterial Oxygen Gradient. StatPearls (NCBI Bookshelf).](https://www.ncbi.nlm.nih.gov/books/NBK545153/)

- [Berend2014,NEJM,updated2014-10-16,primary article mirror](https://www.docenti.unina.it/webdocenti-be/allegati/materiale-didattico/443118)

- [Mellemgaard1966](https://onlinelibrary.wiley.com/doi/10.1111/j.1748-1716.1966.tb03281.x)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

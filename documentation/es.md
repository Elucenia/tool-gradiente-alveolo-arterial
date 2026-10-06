<!-- ELUCENIA technical documentation · gradiente-alveolo-arterial · es · no clinical/professional/rights approval -->

# Gradiente alveoloarterial de O₂

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/gradiente-alveolo-arterial)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### FiO₂

`fio2`

% · intervalo: 21–100

### PaO₂

`pao2`

mmHg · intervalo: 20–700

### PaCO₂

`paco2`

mmHg · intervalo: 10–150

### Edad

`idade`

años · intervalo: 1–110

### Presión barométrica local (valor predeterminado 760)

`patm`

mmHg · opcional · intervalo: 400–800

## Edición del método

Ecuación alveolar RQ 0,8/vapor 47 mmHg; gradiente Mellemgaard 1966 2,5+0,21 edad; aproximación edad/4+4

## Fórmula documentada

PAO₂ = FiO₂ × (Patm − 47) − PaCO₂ ÷ 0,8 (cociente respiratorio 0,8; 47 mmHg = presión de vapor de agua a 37 °C).

Gradiente A-a = PAO₂ − PaO₂.

Esperado en aire ambiente = 2,5 + 0,21 × edad (Mellemgaard). Regla práctica: edad ÷ 4 + 4.

## Límites y población

El cálculo utiliza una presión de vapor de agua de 47 mmHg a 37 °C y un cociente respiratorio fijo de 0,8; este es un supuesto de estado estacionario y puede variar con la dieta. Introduzca la FiO₂ en porcentaje, las presiones en mmHg y una presión barométrica adecuada. La referencia aproximada por edad no debe extrapolarse automáticamente a FiO₂ elevada o altitud. El gradiente ayuda a evaluar la oxigenación, pero no determina por sí solo la causa de la hipoxemia. Los coeficientes de la referencia local por edad aún requieren comprobación en el estudio completo citado.

## Referencias

- [Mellemgaard K. The alveolar-arterial oxygen difference: its size and components in normal man. Acta Physiol Scand, 1966.](https://doi.org/10.1111/j.1748-1716.1966.tb03281.x)

- [Hantzidiamantis PJ, Amaro E. Physiology, Alveolar to Arterial Oxygen Gradient. StatPearls (NCBI Bookshelf).](https://www.ncbi.nlm.nih.gov/books/NBK545153/)

- [Berend2014,NEJM,updated2014-10-16,primary article mirror](https://www.docenti.unina.it/webdocenti-be/allegati/materiale-didattico/443118)

- [Mellemgaard1966](https://onlinelibrary.wiley.com/doi/10.1111/j.1748-1716.1966.tb03281.x)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

Gradiente normal para la edad: hipoxemia, si la hay, por hipoventilación o baja presión inspirada de O₂

| Detalles del resultado | |
| --- | --- |
| PAO₂ (presión alveolar de O₂) | 100 mmHg |
| Esperado para la edad (2,5 + 0,21 × edad) | hasta 11 mmHg |
| Regla práctica (edad ÷ 4 + 4) | 14 mmHg |


### 2

Gradiente aumentado para la edad: sugiere alteración V/Q, shunt o alteración de la difusión

| Detalles del resultado | |
| --- | --- |
| PAO₂ (presión alveolar de O₂) | 112 mmHg |
| Esperado para la edad (2,5 + 0,21 × edad) | hasta 15 mmHg |
| Regla práctica (edad ÷ 4 + 4) | 19 mmHg |


### 3

Gradiente normal para la edad: hipoxemia, si la hay, por hipoventilación o baja presión inspirada de O₂

| Detalles del resultado | |
| --- | --- |
| PAO₂ (presión alveolar de O₂) | 62 mmHg |
| Esperado para la edad (2,5 + 0,21 × edad) | hasta 13 mmHg |
| Regla práctica (edad ÷ 4 + 4) | 17 mmHg |


### 4

Gradiente normal para la edad: hipoxemia, si la hay, por hipoventilación o baja presión inspirada de O₂

| Detalles del resultado | |
| --- | --- |
| PAO₂ (presión alveolar de O₂) | 91 mmHg |
| Esperado para la edad (2,5 + 0,21 × edad) | hasta 9 mmHg |
| Regla práctica (edad ÷ 4 + 4) | 12 mmHg |


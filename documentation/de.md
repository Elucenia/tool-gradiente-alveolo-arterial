<!-- ELUCENIA technical documentation · gradiente-alveolo-arterial · de · no clinical/professional/rights approval -->

# Alveoloarterieller O₂-Gradient

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/gradiente-alveolo-arterial)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### FiO₂

`fio2`

% · Bereich: 21–100

### PaO₂

`pao2`

mmHg · Bereich: 20–700

### PaCO₂

`paco2`

mmHg · Bereich: 10–150

### Alter

`idade`

Jahre · Bereich: 1–110

### Örtlicher Luftdruck (Standardwert 760)

`patm`

mmHg · optional · Bereich: 400–800

## Fassung der Methode

Alveolargasgleichung RQ 0,8/Dampf 47 mmHg; Mellemgaard-Gradient 1966 2,5+0,21 Alter; Näherung Alter/4+4

## Dokumentierte Formel

PAO₂ = FiO₂ × (Patm − 47) − PaCO₂ ÷ 0,8 (respiratorischer Quotient 0,8; 47 mmHg = Wasserdampfdruck bei 37 °C).

A-a-Gradient = PAO₂ − PaO₂.

Sollwert bei Raumluft = 2,5 + 0,21 × Alter (Mellemgaard). Faustregel: Alter ÷ 4 + 4.

## Grenzen und Population

Die Berechnung verwendet einen Wasserdampfdruck von 47 mmHg bei 37 °C und einen festen respiratorischen Quotienten von 0,8; dies ist eine Annahme für einen stabilen Zustand und kann sich mit der Ernährung ändern. Geben Sie FiO₂ in Prozent, Drücke in mmHg und einen geeigneten barometrischen Druck an. Die näherungsweise altersbezogene Referenz darf nicht automatisch auf eine hohe FiO₂ oder Höhenlage extrapoliert werden. Der Gradient hilft, die Oxygenierung zu beurteilen, bestimmt aber allein nicht die Ursache einer Hypoxämie. Die Koeffizienten der lokalen altersbezogenen Referenz müssen noch anhand des vollständigen Textes der zitierten Studie überprüft werden.

## Referenzen

- [Mellemgaard K. The alveolar-arterial oxygen difference: its size and components in normal man. Acta Physiol Scand, 1966.](https://doi.org/10.1111/j.1748-1716.1966.tb03281.x)

- [Hantzidiamantis PJ, Amaro E. Physiology, Alveolar to Arterial Oxygen Gradient. StatPearls (NCBI Bookshelf).](https://www.ncbi.nlm.nih.gov/books/NBK545153/)

- [Berend2014,NEJM,updated2014-10-16,primary article mirror](https://www.docenti.unina.it/webdocenti-be/allegati/materiale-didattico/443118)

- [Mellemgaard1966](https://onlinelibrary.wiley.com/doi/10.1111/j.1748-1716.1966.tb03281.x)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

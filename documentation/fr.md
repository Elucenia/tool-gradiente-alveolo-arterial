<!-- ELUCENIA technical documentation · gradiente-alveolo-arterial · fr · no clinical/professional/rights approval -->

# Gradient alvéolo-artériel en O₂

[conditions, sources et autorisations](https://elucenia.org/fr/outils/gradiente-alveolo-arterial)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### FiO₂

`fio2`

% · intervalle: 21–100

### PaO₂

`pao2`

mmHg · intervalle: 20–700

### PaCO₂

`paco2`

mmHg · intervalle: 10–150

### Âge

`idade`

ans · intervalle: 1–110

### Pression barométrique locale (valeur par défaut 760)

`patm`

mmHg · facultatif · intervalle: 400–800

## Édition de la méthode

Équation alvéolaire RQ 0,8/vapeur 47 mmHg ; gradient Mellemgaard 1966 2,5+0,21 âge ; approximation âge/4+4

## Formule documentée

PAO₂ = FiO₂ × (Patm − 47) − PaCO₂ ÷ 0,8 (quotient respiratoire 0,8 ; 47 mmHg = pression de vapeur d’eau à 37 °C).

Gradient A-a = PAO₂ − PaO₂.

Attendu à l’air ambiant = 2,5 + 0,21 × âge (Mellemgaard). Règle pratique : âge ÷ 4 + 4.

## Limites et population

Le calcul utilise une pression de vapeur d’eau de 47 mmHg à 37 °C et un quotient respiratoire fixe de 0,8 ; il s’agit d’une hypothèse d’état stable qui peut varier avec le régime alimentaire. Renseignez la FiO₂ en pourcentage, les pressions en mmHg et une pression barométrique appropriée. La référence approximative selon l’âge ne doit pas être automatiquement extrapolée à une FiO₂ élevée ou à l’altitude. Le gradient aide à évaluer l’oxygénation, mais ne détermine pas à lui seul la cause de l’hypoxémie. Les coefficients de la référence locale selon l’âge doivent encore être vérifiés dans l’étude complète citée.

## Références

- [Mellemgaard K. The alveolar-arterial oxygen difference: its size and components in normal man. Acta Physiol Scand, 1966.](https://doi.org/10.1111/j.1748-1716.1966.tb03281.x)

- [Hantzidiamantis PJ, Amaro E. Physiology, Alveolar to Arterial Oxygen Gradient. StatPearls (NCBI Bookshelf).](https://www.ncbi.nlm.nih.gov/books/NBK545153/)

- [Berend2014,NEJM,updated2014-10-16,primary article mirror](https://www.docenti.unina.it/webdocenti-be/allegati/materiale-didattico/443118)

- [Mellemgaard1966](https://onlinelibrary.wiley.com/doi/10.1111/j.1748-1716.1966.tb03281.x)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

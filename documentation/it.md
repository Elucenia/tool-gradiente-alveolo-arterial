<!-- ELUCENIA technical documentation · gradiente-alveolo-arterial · it · no clinical/professional/rights approval -->

# Gradiente alveolo-arterioso di O₂

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/gradiente-alveolo-arterial)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### FiO₂

`fio2`

% · intervallo: 21–100

### PaO₂

`pao2`

mmHg · intervallo: 20–700

### PaCO₂

`paco2`

mmHg · intervallo: 10–150

### Età

`idade`

anni · intervallo: 1–110

### Pressione barometrica locale (valore predefinito 760)

`patm`

mmHg · facoltativo · intervallo: 400–800

## Edizione del metodo

Equazione alveolare RQ 0,8/vapore 47 mmHg; gradiente Mellemgaard 1966 2,5+0,21 età; approssimazione età/4+4

## Formula documentata

PAO₂ = FiO₂ × (Patm − 47) − PaCO₂ ÷ 0,8 (quoziente respiratorio 0,8; 47 mmHg = pressione di vapore acqueo a 37 °C).

Gradiente A-a = PAO₂ − PaO₂.

Atteso in aria ambiente = 2,5 + 0,21 × età (Mellemgaard). Regola pratica: età ÷ 4 + 4.

## Limiti e popolazione

Il calcolo usa una pressione di vapore acqueo di 47 mmHg a 37 °C e un quoziente respiratorio fisso di 0,8; questa è un’ipotesi di stato stazionario e può variare con la dieta. Inserire la FiO₂ in percentuale, le pressioni in mmHg e una pressione barometrica appropriata. Il riferimento approssimativo per età non deve essere automaticamente estrapolato a FiO₂ elevata o altitudine. Il gradiente aiuta a valutare l’ossigenazione, ma non determina da solo la causa dell’ipossiemia. I coefficienti del riferimento locale per età richiedono ancora verifica nello studio completo citato.

## Riferimenti

- [Mellemgaard K. The alveolar-arterial oxygen difference: its size and components in normal man. Acta Physiol Scand, 1966.](https://doi.org/10.1111/j.1748-1716.1966.tb03281.x)

- [Hantzidiamantis PJ, Amaro E. Physiology, Alveolar to Arterial Oxygen Gradient. StatPearls (NCBI Bookshelf).](https://www.ncbi.nlm.nih.gov/books/NBK545153/)

- [Berend2014,NEJM,updated2014-10-16,primary article mirror](https://www.docenti.unina.it/webdocenti-be/allegati/materiale-didattico/443118)

- [Mellemgaard1966](https://onlinelibrary.wiley.com/doi/10.1111/j.1748-1716.1966.tb03281.x)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

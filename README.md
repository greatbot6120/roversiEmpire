# CORRETTEZZA PARZIALE DI UN PROGRAMMA ITERATIVO
___
## Principio di induzione

**- Istruzioni passo base** : costruiscono una configurazione quando sono state completate *0 iterazioni*
>Qui deve essere vera la "frase", o il predicato, che descrive le proprietà della configurazione costruita avendo completato 0 iterazioni cioè dev'essere vero il predicato *P(0)*.

```java
while ("condizione di ripetizione")  {

    //assegnazioni e porzione di codice
```

>Qui dev'essere vera la "frase", o predicato, che descrive le proprietà della configurazione costruita dopo **k iterazioni**. Quindi siamo all'inizio della iterazione **k+1** e vale *P(K)*.

**- Istruzioni induttive** : Dalla configurazione ad *inizio iterazione* k+1 alla configurazione a *fine iterazione* k+1.

>Qui dev'essere vera la "frase", o il predicato, che descrive le proprietà della configurazione costruita dopo k+1 iterazioni, essendo alla fine della iterazione k+1 e vale *P(K+1)*.

```java
}
```

>Qui continua a valere il predicato *P(K+1)* ma è falsa la **condizione di ripetizione**, cioè il predicato che permette di ripetere l'insieme di operazioni per passare dalla configurazione ad inizio della iterazione k+1 a quella a fine iterazione k+1.

* Se la scelta dell'iterazione in cui la **condizione di ripetizione** è oculata, segue la dimostrazione della corretteza dell'algoritmo.

| Dimostrare che un programma è parzialmente corretto |
|-----------------------------------------------------|
| A) Saper **scrivere** *P(0)*, cioè saper scrivere la frase (predicato) nello specifico caso in cui non si siano ancora eseguite iterazioni;|
| B) Saper **dimostrare** che *P(0)* è vero, usando tipicamente le operazioni aritmetiche coinvolte in *P(0)*;|
| C) Saper **scrivere** la frase, o predicato, in grado di esprimere che se *P(K)* è vero, allora *P(K+1)* lo è. Questo è detto passo induttivo. sia *K* che *K+1* indicano a quale **iterazione completa** si riferisce *P*. Quindi *P(K)* parla della configurazione ad inizio della *(K+1)-esima* iterazione, mentre *P(K+1)* parla della configurazione alla fine della *(K+1)-esima* iterazione; |
| D) Saper **dimostrare** che se *P(K)* è vero, allora *P(K+1)* è vero, tipicamente, sfruttando il comportamento delle istruzioni coinvolte nell'iterazione;|

**[Formula Pincipio di induzione](https://latex.codecogs.com/svg.latex?%5Clarge%20%5BP%28O%29%5Cwedge%28%5Cforall%20k%5Cgeq%200%2C%20P%28K%29%5CRightarrow%20P%28K&plus;1%29%29%5D%5CRightarrow%20%28%5Cforall%20k%5Cgeq%200%2C%20P%28K%29%29 "Vai alla formula")** che si legge come segue:

>Se *P(0)*è vero, e, per ogni *k* non negativo, la verità di *P(K)* implica la verità di *P(K+1)*, allora *P(K)* è vero per ogni k non negativo.


>questo è un paragrafo che sto aggiungendo per poi fare git commit!

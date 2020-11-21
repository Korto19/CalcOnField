# CalcOnField

## Qgis Plugin per processing

### Installazione

Per installarlo basta che scarichiate lo zip del repo e da QGis fate installa plugin da zip. Spero a breve sia disponibile nel repository ufficiale di QGis.

### Finestra processing

Il plugin, una volta caricato, compare negli script di processing nella cartella CALC

![uno](images/processing.png)

La finestra permette la scelta delle operazioni sul campo:

![uno](images/finestra.png)


Il plugin permette crea una copia del layer aggiungendo un nuovo campo con il risultato di uno seguenti calcoli:

    progressiva,
    % sul totale,
    media mobile,
    indice media ponderata, [è un parametro]
    variazione,
    variazione % calcolata con ordinamento per id record

Il campo risultante generato ha lo stesso nome delcampo di origine più un suffisso automatico che richiama il calcolo es: lunghezza ->> lunghezza_prog

Il nuovo layer ha per nome Calc_ + timestamp e sarà temporaneo

E' possibile ripetere l'operazione sui layer generati

### Avvertenze

La variazione e la variazione % necessitano di layer NON TEMPORANEI

La variazione % da 0 a un qualsiasi valore è indicata con 9999999

### PARAMETRI AVANZATI

![uno](images/parametri_avanzati.png)

    Opzionalmente è possibile inserire:
    - il valore della progressiva di partenza;
	- ulteriore suffisso es: `lunghezza_prog` + `_gruppoA`;
    - campo con l'id record utilizzato dall'ordinamento del calcolo;
    - 5 decimali anzichè 3 se le % lo richiedessero".

# CalcOnField

##Qgis Plugin per processing

##Installazione

Per installarlo basta che scarichiate lo zip del repo e da QGis fate installa plugin da zip. Spero a breve sia disponibile nel repository ufficiale di QGis.

##Finestra processing

Il plugin, una volta caricato, compare negli script di processing nella cartella HTML

Replica il layer corrente aggiungendo un nuovo campo con il risultato dei seguenti calcoli:

    progressiva,
    % sul totale,
    media mobile,
    media ponderata, [è un parametro]
    variazione,
    variazione % calcolata con ordinamento per id record

Il campo risultante generato ha lo stesso nome delcampo di origine più un suffisso automatico che richiama il calcolo es: lunghezza ->> lunghezza_prog

Il nuovo layer ha per nome Calc_ + timestamp

##Avvertenze

La variazione e la variazione % necessitano di layer NON TEMPORANEI

La variazione % da 0 a un qualsiasi valore è indicata con 9999999

##PARAMETRI AVANZATI

    Opzionalmente è possibile inserire:
    - il valore della progressiva di partenza;
	- ulteriore suffisso es: `lunghezza_prog` + `_gruppoA`;
    - campo con l'id del record utilizzato dall'ordinamento del calcolo;
    - 5 decimali anzichè 3 se le % lo richiedessero".

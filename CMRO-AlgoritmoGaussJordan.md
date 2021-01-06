# Algoritmo di Gauss/Jordan

> Attraverso una serie di interazioni ci permette di ridurre una matrice affinché sia più semplice risolvere il sistema di equazioni che rappresenta.


## Matrici a Scala

L'obiettivo è quello di ottenere una **Matrice a Scala** ovvero una matrice con le seguenti caratteristiche:

> * Le righe vuote, composte da soli zero, si trovano al più alla fine
* Sotto il primo elemento _non_ nullo di ogni riga e sotto tutti gli zeri che lo precedono ci sono zero.

###### Esempi _di matrici a scala_
<table align="center" style="float:left;margin:10px;">
    <tr>
        <td style="color:red" align="center"><b>2</b></td>
        <td align="center">0</td>
        <td align="center">1</td>
    </tr>
    <tr>
        <td align="center">0</td>
        <td style="color:red" align="center"><b>-1</b></td>
        <td align="center">1</td>
    </tr>
    <tr>
        <td align="center">0</td>
        <td align="center">0</td>
        <td style="color:red" align="center"><b>3</b></td>
    </tr>
</table>

<table align="center" style="float:left;margin:10px;">
    <tr>
        <td style="color:red" align="center"><b>4</b></td>
        <td align="center">3</td>
        <td align="center">2</td>
        <td align="center">1</td>
    </tr>
    <tr>
        <td align="center">0</td>
        <td align="center">0</td>
        <td style="color:red" align="center"><b>1</b></td>
        <td align="center">0</td>
    </tr>
    <tr>
        <td align="center">0</td>
        <td align="center">0</td>
        <td align="center">0</td>
        <td align="center">0</td>
    </tr>
</table><br><br><br><br><br><br><br>

Ora che abbiamo definito questa particolare tipologia di matrici possiamo individuare l'elemento di pivot o elemento perno, che ci servirà per eseguire procedere con l'algoritmo.

### Elemento Perno
>E' il primo elemento **non** nullo di ciascuna riga.  
*Evidenziamo in rosso gli elementi perno delle tabelle di cui sopra.*

## Operazioni Base

Per poter *semplificare* le matrici ottenute possiamo applicare le seguenti operazioni.

* Scambiare 2 righe
* Moltiplicare una riga per uno numero non nullo
* Sommare ad una riga un multiplo di un'altra


> In termini più formali
* E<sub>a</sub> ↔ E<sub>b</sub>
* E<sub>a</sub> → k · E<sub>b</sub> *con* k ≠ 0
* E<sub>a</sub> → E<sub>a</sub> + k · E<sub>b</sub>

Queste operazioni saranno utili a trasfromare i singoli elementi delle matrici affinché possano *diventare* delle Matrici a Scala. Lavoreremo quindi cercando di trasformare gli elementi in 0 e 1, spostandoli nelle posizioni opportune.

## L'algoritmo

Ci permette, attraverso una serie di iterazioni, di ridurre la matrice.   


#### Azzerare un elemento
 Per eseguire questa trasformazione utilizziamo
>   * E<sub>a</sub> → E<sub>a</sub> - k · E<sub>b</sub>  
*Dove k è l'elemento che voglio azzerare fratto l'elemento perno della riga*  
E<sub>b</sub> è la riga dell'**elemento perno**.

#### Trasformare in 1 un elemento
Per eseguire questa trasformazione utilizziamo
>   * E<sub>a</sub> → k · E<sub>b</sub> *con* k ≠ 0   
*Dove k è 1 fratto l'elemento perno della riga*

## Come si fa?
Mi posiziono sulla prima riga e cerco il perno, se il primo elemento è zero proseguo sulla riga successiva cercando l'elemento perno di questa.
Una volta trovato l'elemento perno posso *iniziare* ad eseguire le operazioni.

In linea generale prima si azzerano le righe, poi si porta ad uno quella dell'elemento perno e solo infine (se serve) si fanno gli opportuni scambi.

Quando ho terminato, mi sposto sulla riga successiva ed eseguo gli *stessi* passaggi partendo dalla ricerca del perno su questa riga.

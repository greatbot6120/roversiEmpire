## Piu( ) Contro Variante

>Per contrapposizione con la versione **COVARIANTE** una definizione **CONTROVARIANTE** ha l'indice che determina il caso da applicare che CRESCE al DECRESCERE della difficoltà del problema da risolvere, nel nostro caso:


```java
piu (x, y, y) = x
                    //indice decrescente
                             ↓
                           |───|            
piu (x, y, i) = Piu (x, y, i + 1) + 1
                    |───────────|
                          ↑
              /*problema più semplice poichè
                più "vicino" a piu(x,y,y)*/

```

>**DOMANDA** → Perchè la definizione è corretta? Possiamo applicare un metodo che ricorda quello induttivo per dimostrare:

```java
0 ­­≤ i ≤ y  ⟹  piu(x, y, i) = x + y - i
```

* **BASE** : *i=y* , allora
```java
piu(x, y, y) = x = x + 0 = x + y - y
               ↑
         //definizione
```
* **INDUZIONE** : *0 ≤ i < y* , allora
```java
piu(x, y, y) = piu(x, y, y) + 1
               ↑
         //definizione

               = x + y - (i + 1) + 1
               ↑
      /*ipotesi induttiva sul
        buon funzionamento*/

               = x + y - i - 1 + 1 = x + (y - 1)                     
```
* **CONSEGUENZA** :
```java
piu(x, y, 0) = x + y - 0 = x + y
```
---
## Per( ) Contro Variante


>Per contrapposizione con la versione **COVARIANTE** una definizione **CONTROVARIANTE** ha l'indice che determina il caso da applicare che CRESCE al DECRESCERE della difficoltà del problema da risolvere, nel nostro caso:

```java
per(x, y, y) = 0
                   //indice crescente
                           ↓
                         |───|
per(x, y, i) = per(x, y, i + 1) + x

                  |───────────|
                        ↑
          /*problema più semplice poichè
            più "vicino" a per(x,y,y)*/
```

>**DOMANDA** → Perchè la definizione è corretta? Possiamo applicare un metodo che ricorda quello induttivo per dimostrare:

```java
0 ≤ i ≤ y  ⟹  per(x, y, i) = x • (y - i)
```
* **BASE** : *i=y* , allora
```java
per(x, y, y) = 0 = n • 0 = x • (y - y)
               ↑
         //definizione
```
* **INDUZIONE** : *0 ≤ i ≤ y* , allora
```java
per(x, y, i) = per (x, y, i + 1) + x
               ↑
         //definizione

               = x • (y - (i + 1) ) + x
               ↑
      /*ipotesi induttiva sul
        buon funzionamento*/

               = x • (y - 1 - 1 + 1)

               = x • (y - i)
```
* **CONSEGUENZA** :
```java
per(x, y, 0) = x • (y - 0) = x • y
```
---

## Men( ) Contro Variante

>Per contrapposizione con la versione **COVARIANTE** una definizione **CONTROVARIANTE** ha l'indice che determina il caso da applicare che CRESCE al DECRESCERE della difficoltà del problema da risolvere, nel nostro caso:

```java
men(x, y, y) = x
                   //indice crescente
                           ↓
                         |───|
men(x, y, i) = men(x, y, i + 1) - 1
                  |───────────|
                        ↑
          /*problema più semplice poichè
            più "vicino" a men(x,y,y)*/
```

>**DOMANDA** → Perchè la definizione è corretta? Possiamo applicare un metodo che ricorda quello induttivo per dimostrare:

```java
0 ≤ i ≤ y  ⟹  men(x, y, i) = x - (y - 1)
```
* **BASE** : *i=y* , allora
```java
men(x, y, y) = x = x - 0 = x - (y - y)
               ↑
         //definizione
```
* **INDUZIONE** : *0 ≤ i < y* , allora
```java
men(x, y, i) = men(x, y, i + 1) - 1
               ↑
         //definizione

               = x - (y - (i + 1) ) - 1
               ↑
      /*ipotesi induttiva sul
        buon funzionamento*/

               = x - y + i + 1 - 1

               = x - (y - i)
```
* **CONSEGUENZA** :
```java
men(x, y, 0) = x - (y - 0) = x - y
```

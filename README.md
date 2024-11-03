# Disseny-DDBB
Resposta a la activitat de disseny DDBB, 03-11-2024

![imatge](https://github.com/user-attachments/assets/007f211c-851a-4c1a-bb3c-c581955bcba4)

El disseny es divideix en tres seccions principals, totes elles marcant un punt especific del festival que necessita ser seguit; les persones que assisteixen al fesitval, els grups de música que toquen, i el recinte en el que el festival es du a terme. 

## Recinte
Dividit en dos possibles tipus de recintes, la zona d'actuació o el camping en el que els atenents descansen/fan camping. Al no haver-hi possibilitat en que una part del recinte pertanyi als dos grups, la divisió passa a ser disyuntiva totat.

![imatge](https://github.com/user-attachments/assets/905585e5-5951-42c5-b9c8-b1a8637c963e)

### Zona d'actuació
Guarda les dades necessaries sobre els recintes designats a les actuacions dels diferents grups. Cada recinte es distingeix amb el seu nom, i també es guarda si hi ha accés a lavabos. 
Aquí també hi ha una divisió disyuntiva total, que marca si la part del recinte de la que estem parlant es el escenari, o la zona d'espectadors. En la primera es guarda si està covert, i els metres quadrats, mentre que la segona només guarda els metres quadrats. La raó per la que es pot fer aquesta divisió es deu a que hi ha valors penjant dels grups que esl diferencien entre ells (el fet de que l'escenari pot estar covert o no, mentre que la zona d'espectadors no).

![imatge](https://github.com/user-attachments/assets/83d9c9f7-d838-49ff-9d7a-0533c5a6e681)

### Camping
El camping es una zona que està definida per els grups que descendeixen d'ella. En aquest cas, el camping està dividit en molts carrers, que es distingeixen amb un codi i tenen un nom, i cada carrer es divideix en moltes parcel·les, que es distingeixen amb un número (tenin en compte el nom del carrer del que depén), i també guarda el seu preu i els metres quadrats. 

![imatge](https://github.com/user-attachments/assets/f86ccda4-719a-42d0-b257-4394aead25c1)

## Grups de música
Secció que defineix i guarda tota l'informació rellevant dels grups que actuen durant el festival. Cada grup s'identifica amb el seu nom, i a més guarda el número d'integrants i el pais de provinença. 

![imatge](https://github.com/user-attachments/assets/4140fc51-899a-497d-babb-45e56fddfb09)

## Persona
Referents als usuaris que atenen el festival. Se'ls identifical per l'usuari concedit quan es van allistar a la web, i també es guarda la seva contrasenya, el mail, i el passaport o DNI. 

![imatge](https://github.com/user-attachments/assets/93acc9cb-3bde-416e-8f88-426262f44e6b)

## Connexions
Per el que fa les connexions que hi ha entre els diferents grups, hi ha de dues natures diferents. 

### Simples
"Anar" i "lloga" son simples, i només conecten a dos grups diferents. En aquest cas, "lloga" mostra que una person només pot llogar una parcel·la, i que una parcel·la només pot ser llogada per una persona. "Anar", de la mateixa manera, lliga una persona a tots els concerts que pot anar una persona, i quantes persones poden anar a un concert així mateix.

![imatge](https://github.com/user-attachments/assets/c80979d3-8900-4a34-bb34-3f80adc13f9c)

### Complexa
Concert, en canvi, es una connexió molt més complicada. En primer lloc, tot i que sigui una connexió, també fa la funció de grup, i es que un concert depén de grup i escenari, funcionant com a pont entre els dos grups. La necessitat que actui com a grup es basa en que s'han de guardar diferents punts d'informació, aquests sent l'inici i el final del cooncert, la data en el que es fa, i el preu que se li paga al grup per aquest. A més, una persona només pot asistir a un concert, no a un escenari o al grup en si, creant una altra connexió (i reforçant la necessitat de que concert sigui un grup).

![imatge](https://github.com/user-attachments/assets/5727142e-7866-4751-97fe-54619e1dc27c)

Fora de tot això, concert també fa la funcionalitat de les simples, marcant que un escenari pot albergar múltiples concerts (a diferents moments), i que un grup pot fer múltiples concerts en múltiples escenaris. 
En últim, el lligament entre concert i grup es diferent d'aquell entre escenari i concert, i es que mentre que l'escenari està assegurat (a meny que hi hagi situacions fora de control de l'organització, que per tant no es tenen en compte), els grups si que poden fallar. Per aquest motiu, un grup es té conciderat en el concert com a l'actuació principal, o com el substitut en cas que el principal falli. Només hi ha un pricipal, mentre que poden haver-hi múltiples o zero substituts. 
![imatge](https://github.com/user-attachments/assets/060cba85-5c6c-41c3-9973-83da9642aaa9)

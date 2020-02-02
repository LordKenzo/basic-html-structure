# HTML Basic Structure

An HTML Basic structure for my students.

In flex abbiamo il concetto di **container** che ha un display (flex o flex-inline) property a flex e in cui impostiamo la flex-direction (row è il valore default) che di fatto imposta il main axis ed il cross axis a seconda se la direzione sarà orizzantale (row - default) o verticale (column). Possiamo definire la disposizione degli items flex interni al container con le proprietà justify-content (che agisce sul main axis - x se row, y se column) e align-items (che agisce sul cross axis - y se row, x se column). Inoltre abbiamo la proprietà flex-wrap (nowrap è il default, wrap, wrap-reverse) per forzare gli elementi su singola linea, o su più linee.

```html
<div class="container">
  <div class="box-1">
    <h2>Title Box One</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
  </div>
  <div class="box-2">
    <h2>Title Box Two</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
  </div>
  <div class="box-3">
    <h2>Title Box Three</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
  </div>
</div>
```

```css
.container {
  display: flex;
  flex-direction: row; /* row (default), column */
  justify-content: flex-start; /* flex-start (default), flex-end, center, space-between (non ho margini ai lati), space-around (ho dei margini ai lati), space-evenly (ho margini uguali sia dai bordi che dagli elementi)*/
  align-items: stretch; /* stretch (default), start, end, center*/
  flex-wrap: nowrap; /* no-wrap (default), wrap, wrap-reverse */
}

.container div {
  border: 1px solid #000;
  padding: 10px;
}
```

Gli items possono avere proprietà come align-self (flex-start, flex-end o center) e proprietà come flex-grow (numero da 0 a n), flex-shrink (numero da 0 a n) che di fatto dicono come si distribuiscono rispetto allo spazio del container in fatto di ingrandimento/rimpicciolimento (argh...) e flex-basis (%) che imposta di fatto una width dell'item. Queste tre proprietà sono riassunte dalla proprietà flex. Infine si può vedere anche l'uso della proprietà order per spostare un elemento senza modificare l'html.

Un ulteriore approfondimento sulla proprietà flex. Il valore obbligatorio è il valore di flex-grow:

```css
.box-1 {
  flex: 2; /*flex-grow flex-shrink flex-basis*/
}
.box-2 {
  flex: 1;
}
.box-3 {
  flex: 1;
}
```

Il box-1 crescerà 2 volte rispetto agli altri.

## Step 1

Definisco la struttura base e un CSS di reset.

## Step 2

Inserisco le prime classi e creo un menù di navigazione responsive. Il CSS creato è mobile-first.

## Step 3

Definisco la mia sezione Hero (Banner) tramite l'uso di Flex. Devo creare un wrapper per centrare i contenuti.

## Step 4

Faccio dei cambiamenti al CSS per ottenere di fatto lo stesso risultato precedente. Aggiungo lo stile per la navbar e un pò di accessibilità.
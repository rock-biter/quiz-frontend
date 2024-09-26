Ecco il quiz aggiornato che include nuove domande su JavaScript, la manipolazione del DOM, e concetti avanzati come spread, rest e null coalescing. Per ciascuna domanda, ho indicato la risposta corretta.

---

### **Quiz di Valutazione su JavaScript e Sviluppo Frontend**

#### **Sezione 1: Concetti di base di JavaScript**

1. **Quale di questi metodi non modifica l'array originale, ma ne restituisce uno nuovo?**

   ```javascript
   const arr = [1, 2, 3, 4]
   ```

   - A) `arr.push(5)`
   - B) `arr.pop()`
   - C) `arr.map(x => x * 2)` **(Risposta corretta)**
   - D) `arr.splice(1, 2)`

2. **Cosa restituisce il seguente codice?**

   ```javascript
   let x = 10
   const fn = () => {
   	let x = 20
   	return x
   }
   console.log(fn())
   ```

   - A) `undefined`
   - B) `null`
   - C) `20` **(Risposta corretta)**
   - D) `10`

3. **Qual è la differenza tra `let`, `const` e `var`?**

   - A) `var` ha ambito di blocco, `let` e `const` no.
   - B) `const` permette di ridefinire la variabile, `let` e `var` no.
   - C) `let` e `const` hanno ambito di blocco, `var` ha ambito di funzione. **(Risposta corretta)**
   - D) `var` e `let` sono immutabili, `const` è mutabile.

4. **Cosa restituisce il seguente codice con l'operatore `nullish coalescing`?**

   ```javascript
   const result = null ?? 'default value'
   console.log(result)
   ```

   - A) `null`
   - B) `"default value"` **(Risposta corretta)**
   - C) `undefined`
   - D) Lancia un errore

5. **Qual è il risultato del seguente codice che usa lo spread operator?**

   ```javascript
   const obj1 = { a: 1, b: 2 }
   const obj2 = { b: 3, c: 4 }
   const merged = { ...obj1, ...obj2 }
   console.log(merged)
   ```

   - A) `{ a: 1, b: 2, c: 4 }`
   - B) `{ a: 1, b: 3, c: 4 }` **(Risposta corretta)**
   - C) `{ a: 1, b: 2, c: 3 }`
   - D) Lancia un errore

6. **Cosa fa l'operatore `rest` nel seguente codice?**
   ```javascript
   function sum(...numbers) {
   	return numbers.reduce((acc, curr) => acc + curr, 0)
   }
   console.log(sum(1, 2, 3, 4))
   ```
   - A) Converte i parametri in un array. **(Risposta corretta)**
   - B) Lancia un errore perché sono troppi parametri.
   - C) Limita il numero di parametri a 4.
   - D) Restituisce sempre un valore predefinito.

#### **Sezione 2: Manipolazione del DOM**

7. **Cosa fa il seguente codice JavaScript nel contesto del DOM?**

   ```javascript
   const element = document.getElementById('myElement')
   element.textContent = 'Hello, World!'
   ```

   - A) Cambia l'attributo `id` dell'elemento.
   - B) Imposta l'HTML interno dell'elemento su `Hello, World!`.
   - C) Imposta il contenuto di testo dell'elemento su `Hello, World!`. **(Risposta corretta)**
   - D) Rimuove l'elemento dal DOM.

8. **Quale metodo è utilizzato per aggiungere un nuovo elemento al DOM?**

   ```javascript
   const newElement = document.createElement('div')
   ```

   - A) `element.appendChild(newElement)` **(Risposta corretta)**
   - B) `element.removeChild(newElement)`
   - C) `element.replaceChild(newElement)`
   - D) `element.setAttribute('child', newElement)`

9. **Quale metodo permette di selezionare tutti gli elementi con una determinata classe?**

   - A) `document.querySelector('.myClass')`
   - B) `document.querySelectorAll('.myClass')` **(Risposta corretta)**
   - C) `document.getElementByClassName('myClass')`
   - D) `document.getElementsByTagName('myClass')`

10. **Cos'è il DOM (Document Object Model)?**
    - A) Un linguaggio di markup utilizzato per creare pagine web.
    - B) Una rappresentazione ad oggetti della struttura di un documento HTML o XML. **(Risposta corretta)**
    - C) Un metodo per inviare richieste HTTP.
    - D) Un tipo di database utilizzato per memorizzare dati strutturati.

#### **Sezione 3: Asincronia e Promises**

11. **Cosa fa il seguente codice?**

    ```javascript
    const fetchData = async () => {
    	try {
    		let response = await fetch('https://api.example.com/data')
    		let data = await response.json()
    		console.log(data)
    	} catch (error) {
    		console.error(error)
    	}
    }
    ```

    - A) Esegue una richiesta API in modo sincrono e restituisce una stringa.
    - B) Esegue una richiesta API in modo asincrono e restituisce un oggetto JSON. **(Risposta corretta)**
    - C) Lancia sempre un errore a causa del blocco `try-catch`.
    - D) Restituisce una promessa senza eseguire la richiesta.

12. **Quale di queste è la sintassi corretta per gestire una Promise?**
    ```javascript
    const myPromise = new Promise((resolve, reject) => {
    	// some async operation
    })
    ```
    - A) `myPromise.then().catch();` **(Risposta corretta)**
    - B) `myPromise.catch().then();`
    - C) `myPromise.then().finally();`
    - D) `myPromise.then().then();`

#### **Sezione 4: Node.js e Tooling**

13. **Quale comando permette di avviare un progetto Node.js?**

    - A) `npm install`
    - B) `npm init` **(Risposta corretta)**
    - C) `npm start`
    - D) `node start`

14. **Cosa fa il modulo `path` di Node.js?**

    - A) Esegue operazioni di rete.
    - B) Gestisce percorsi e file system. **(Risposta corretta)**
    - C) Gestisce input/output di file binari.
    - D) Esegue funzioni asincrone.

15. **Quale dei seguenti tool è un package manager per JavaScript?**
    - A) `npm`
    - B) `yarn`
    - C) `pip`
    - D) Entrambe A e B. **(Risposta corretta)**

#### **Sezione 5: Vite e Bundling**

16. **Qual è lo scopo principale di Vite nel contesto dello sviluppo frontend?**

    - A) Gestire le dipendenze del progetto.
    - B) Eseguire il transpiling e il bundling del codice. **(Risposta corretta)**
    - C) Fornire un framework per il testing.
    - D) Gestire il routing del frontend.

17. **Quale di queste tecnologie viene utilizzata da Vite per migliorare le performance durante lo sviluppo?**
    - A) HMR (Hot Module Replacement) **(Risposta corretta)**
    - B) GraphQL
    - C) WebSockets
    - D) Local Storage

#### **Sezione 6: API e comunicazione con il server**

18. **Quale dei seguenti metodi HTTP è comunemente utilizzato per ottenere dati da un server?**

    - A) `POST`
    - B) `PUT`
    - C) `DELETE`
    - D) `GET` **(Risposta corretta)**

19. **Cosa restituisce il metodo `fetch` in JavaScript?**
    - A) Una Promise che si risolve con l'oggetto Response. **(Risposta corretta)**
    - B) Un oggetto contenente i dati JSON direttamente.
    - C) Una Promise che si risolve con i dati parsati come JSON.
    - D) Un'istanza di XMLHttpRequest.

---

Questo quiz include domande su vari concetti fondamentali e avanzati, il che ti permetterà di ottenere una valutazione accurata delle competenze dei partecipanti.

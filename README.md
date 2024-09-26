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

7. **Cosa restituisce il seguente codice utilizzando l'operatore `optional chaining`?**

   ```javascript
   const user = { name: 'John', details: null }
   console.log(user.details?.age)
   ```

   - A) `undefined` **(Risposta corretta)**
   - B) `null`
   - C) Lancia un errore.
   - D) `0`

8. **Cosa restituisce il seguente codice che utilizza l'operatore `===`?**

   ```javascript
   console.log(0 === '0')
   ```

   - A) `true`
   - B) `false` **(Risposta corretta)**
   - C) `null`
   - D) Lancia un errore

9. **Qual è il risultato del seguente codice?**
   ```javascript
   let arr = [1, 2, 3]
   let newArr = [...arr, 4, 5]
   console.log(newArr)
   ```
   - A) `[1, 2, 3, 4, 5]` **(Risposta corretta)**
   - B) `[1, 2, 3, [4, 5]]`
   - C) `[4, 5, 1, 2, 3]`
   - D) Lancia un errore

#### **Sezione 2: Manipolazione del DOM**

10. **Cosa fa il seguente codice JavaScript nel contesto del DOM?**

    ```javascript
    const element = document.getElementById('myElement')
    element.textContent = 'Hello, World!'
    ```

    - A) Cambia l'attributo `id` dell'elemento.
    - B) Imposta l'HTML interno dell'elemento su `Hello, World!`.
    - C) Imposta il contenuto di testo dell'elemento su `Hello, World!`. **(Risposta corretta)**
    - D) Rimuove l'elemento dal DOM.

11. **Quale metodo è utilizzato per aggiungere un nuovo elemento al DOM?**

    ```javascript
    const newElement = document.createElement('div')
    ```

    - A) `element.appendChild(newElement)` **(Risposta corretta)**
    - B) `element.removeChild(newElement)`
    - C) `element.replaceChild(newElement)`
    - D) `element.setAttribute('child', newElement)`

12. **Quale metodo permette di selezionare tutti gli elementi con una determinata classe?**

    - A) `document.querySelector('.myClass')`
    - B) `document.querySelectorAll('.myClass')` **(Risposta corretta)**
    - C) `document.getElementByClassName('myClass')`
    - D) `document.getElementsByTagName('myClass')`

13. **Cos'è il DOM (Document Object Model)?**

    - A) Un linguaggio di markup utilizzato per creare pagine web.
    - B) Una rappresentazione ad oggetti della struttura di un documento HTML o XML. **(Risposta corretta)**
    - C) Un metodo per inviare richieste HTTP.
    - D) Un tipo di database utilizzato per memorizzare dati strutturati.

14. **Quale metodo viene utilizzato per rimuovere un elemento dal DOM?**

    - A) `element.remove()` **(Risposta corretta)**
    - B) `element.delete()`
    - C) `document.removeChild(element)`
    - D) `element.removeNode()`

15. **Qual è la differenza tra `innerHTML` e `textContent`?**
    - A) `innerHTML` modifica solo il testo, mentre `textContent` modifica anche gli elementi figli.
    - B) `innerHTML` può interpretare il codice HTML, mentre `textContent` mostra solo testo. **(Risposta corretta)**
    - C) Non c'è differenza, sono intercambiabili.
    - D) `textContent` è usato solo per input form, `innerHTML` no.

#### **Sezione 3: Asincronia e Promises**

16. **Cosa fa il seguente codice?**

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

17. **Quale di queste è la sintassi corretta per gestire una Promise?**

    ```javascript
    const myPromise = new Promise((resolve, reject) => {
    	// some async operation
    })
    ```

    - A) `myPromise.then().catch();` **(Risposta corretta)**
    - B) `myPromise.catch().then();`
    - C) `myPromise.then().finally();`
    - D) `myPromise.then().then();`

18. **Qual è la funzione di `async` e `await` in JavaScript?**

    - A) Consentono di eseguire codice in modo sincrono.
    - B) Gestiscono le promesse in modo più leggibile. **(Risposta corretta)**
    - C) Causano sempre un ritardo nelle operazioni.
    - D) Creano un nuovo thread per gestire operazioni asincrone.

19. \*\*Qual è la differenza tra `setTimeout` e `setInterval`

?** - A) `setTimeout` viene eseguito una volta, `setInterval` ripete l'esecuzione a intervalli regolari. **(Risposta corretta)\*\* - B) `setTimeout` è asincrono, mentre `setInterval` è sincrono. - C) `setInterval` viene eseguito una volta, `setTimeout` ripete l'esecuzione. - D) `setTimeout` funziona solo nei browser, `setInterval` no.

#### **Sezione 4: Node.js e Tooling**

20. **Quale comando permette di avviare un progetto Node.js?**

    - A) `npm install`
    - B) `npm init` **(Risposta corretta)**
    - C) `npm start`
    - D) `node start`

21. **Quale dei seguenti tool è un package manager per JavaScript?**

    - A) `npm`
    - B) `yarn`
    - C) `pip`
    - D) Entrambe A e B. **(Risposta corretta)**

22. **Qual è la funzione di un `package.json`?**
    - A) Gestisce le configurazioni di build di un progetto.
    - B) Elenca le dipendenze di un progetto e definisce script di esecuzione. **(Risposta corretta)**
    - C) Memorizza i dati del database di un'applicazione.
    - D) È usato per testare il progetto.

#### **Sezione 5: Vite e Bundling**

23. **Qual è lo scopo principale di Vite nel contesto dello sviluppo frontend?**

    - A) Gestire le dipendenze del progetto.
    - B) Eseguire il transpiling e il bundling del codice. **(Risposta corretta)**
    - C) Fornire un framework per il testing.
    - D) Gestire il routing del frontend.

24. **Quale di queste tecnologie viene utilizzata da Vite per migliorare le performance durante lo sviluppo?**
    - A) HMR (Hot Module Replacement) **(Risposta corretta)**
    - B) GraphQL
    - C) WebSockets
    - D) Local Storage

#### **Sezione 6: API e comunicazione con il server**

25. **Quale dei seguenti metodi HTTP è comunemente utilizzato per ottenere dati da un server?**

    - A) `POST`
    - B) `PUT`
    - C) `DELETE`
    - D) `GET` **(Risposta corretta)**

26. **Cosa restituisce il metodo `fetch` in JavaScript?**

    - A) Una Promise che si risolve con l'oggetto Response. **(Risposta corretta)**
    - B) Un oggetto contenente i dati JSON direttamente.
    - C) Una Promise che si risolve con i dati parsati come JSON.
    - D) Un'istanza di XMLHttpRequest.

27. **Come si può inviare dati JSON in una richiesta POST con `fetch`?**
    ```javascript
    fetch(url, {
    	method: 'POST',
    	headers: {
    		'Content-Type': 'application/json',
    	},
    	body: JSON.stringify(data),
    })
    ```
    - A) Usando `formData`.
    - B) Utilizzando il parametro `body`. **(Risposta corretta)**
    - C) Passando i dati come query string nell'URL.
    - D) Usando `fetch.json()`.

---

**31. Quale di questi non è un tipo di dato primitivo in JavaScript?**

- A) `string`
- B) `boolean`
- C) `array` **(Risposta corretta)**
- D) `number`

---

**32. Qual è il risultato del seguente codice che utilizza l'operatore `||` (logical OR)?**

```javascript
const value = 0 || 'default'
console.log(value)
```

- A) `0`
- B) `'default'` **(Risposta corretta)**
- C) `null`
- D) `undefined`

---

**33. Qual è la differenza tra `forEach` e `map` quando vengono utilizzati su un array?**

- A) Entrambi restituiscono un nuovo array.
- B) `forEach` restituisce un nuovo array, mentre `map` no.
- C) `map` restituisce un nuovo array, mentre `forEach` non restituisce nulla. **(Risposta corretta)**
- D) `forEach` è sincrono, `map` è asincrono.

---

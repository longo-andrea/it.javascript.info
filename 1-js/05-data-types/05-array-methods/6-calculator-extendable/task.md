importance: 5

---

# Create una calcolatrice estensibile

Create un costruttore `Calculator` che crei oggetti calcoltrice "estensibili".

Il compito consiste in due parti.

1. La prima parte consiste nell'implementare il metodo `calculate(str)` che accetti una stringa come `"1 + 2"` nel formato "NUMERO operatore NUMERO" (delimitata da spazi) e ne ritorni il risultato. Dovrebbe saper interpretare sia `+` che `-`.

    Esempio d'uso:

    ```js
    let calc = new Calculator;

    alert( calc.calculate("3 + 7") ); // 10
    ```
2. Successivamente aggiungete il metodo `addMethod(name, func)` che ha lo scopo di insegnare alla calcolatrice una nuova operazione. Questo prende il nome dell'operatore `name` e i due argomenti della funzione `func(a,b)` che lo implementa.

    Ad esempio, proviamo ad aggiungere la moltiplicazione `*`, divisione `/` e la potenza `**`:

    ```js
    let powerCalc = new Calculator;
    powerCalc.addMethod("*", (a, b) => a * b);
    powerCalc.addMethod("/", (a, b) => a / b);
    powerCalc.addMethod("**", (a, b) => a ** b);

    let result = powerCalc.calculate("2 ** 3");
    alert( result ); // 8
    ```

- Non è richiesta la gestione delle parentesi o di operazioni complesse.
- I numeri e l'operatore sono separati esattamente da un singolo spazio.
- Se ne hai voglia potresti provare ad aggiungere un minimo di gestione degli errori.

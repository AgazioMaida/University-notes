usate con interfacce funzionali(con un solo metodo astratto SAM)
es
- `Runnable` → `void run()`
- `Comparator<T>` → `int compare(T a, T b)`
- `Function<T,R>` → `R apply(T t)`

1. (parametri) -> espressione
oppure
2. (parametri) -> {  
			// più istruzioni  
			}
(a, b) -> a+b;
s -> s.replace(‘ ‘, ‘_’);


usare lambda solo:
- codice si scrive su una sola riga
mentre
•  si preferisce classe o classe anonima (o, vedremo più avanti,
riferimenti a metodi) se coivolge piu righe



– Classi anonime: si riferisce all’oggetto anonimo
– Espressioni lambda: si riferisce all’oggetto della classe che le racchiude

• La compilazione è differente:
– Classi anonime: compilate come classi interne
– Espressioni lambda: compilate come metodi privati
invocati dinamicamente
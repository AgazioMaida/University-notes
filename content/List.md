sottointerfaccia di collection
## Caratteristiche

- ordinate
- duplicati permessi
- accesso per indice

---

##  ArrayList

ArrayList<String> lista = new ArrayList<>();

- basata su array
- veloce accesso (`get`)
- più lenta inserzione in mezzo
- ![[Pasted image 20260422190409.png]]

## per Iterare sulle liste in entrambe le direzioni:
•** listIterator()**( restituisce iteratore bidirezionale (interfaccia ListIterator che estende Iterator)  Da sinistra verso destra:
```
abbiamo struttura es:
ArrayList<String> lista = new ArrayList<>();
        ...

// Creazione ListIterator
ListIterator<String> it = lista.listIterator();

        // Scorrimento in avanti
        System.out.println("Forward:");
        while (it.hasNext()) {
            String elemento = it.next();
            System.out.println(elemento);
        }

        // Scorrimento all'indietro
        System.out.println("Backward:");
        while (it.hasPrevious()) {
            String elemento = it.previous();
            System.out.println(elemento);
        }
    }
}
```

(se si specifica un intero, si parte da quella posizione: es. list.listIterator(list.size()))

metodi:
	- `hasNext()` → c’è un prossimo elemento?
	- `next()` → vai avanti
	- `hasPrevious()` → c’è un precedente?
	- `previous()` → vai indietro
	- `set(E e)` → modifica elemento corrente
	- `add(E e)` → aggiunge elemento
	- `remove()` → rimuove elemento corrente
## Quando usare `ListIterator`?

- Quando devi scorrere **avanti e indietro**
- Quando devi **modificare la lista durante il ciclo** (senza errori tipo `ConcurrentModificationException`)
---

##  LinkedList

```
LinkedList<String> lista = new LinkedList<>();
lista.add("uno");  
lista.add("due");  
  
lista.addFirst("zero"); // inserimento veloce all'inizio  
lista.addLast("tre");  
  
System.out.println(lista.get(1)); // più lenta rispetto ArrayList  
  
lista.removeFirst();
```

- lista collegata
- veloce inserimento
- più lenta lettura

	-metodi:
		addFirst()  
		addLast()  
		getFirst()  
		getLast()  
		removeFirst()  
		removeLast()  
		push() // stack  
pop()


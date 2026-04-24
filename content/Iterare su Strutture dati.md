modi di iterare:
1.esterno(noi controlliamo ciclo)
1. for-each :
		- for(int x : list)
2. indici :
		- for(int i=0; i<list.size(); i++)
3. Iterator:
		
	```
		import java.util.*;  
  
		List<Integer> list = Arrays.asList(1, 2, 3, 4, 5);  
		Iterator<Integer> it = list.iterator();  
  
		while (it.hasNext()) {  
			System.out.println(it.next());  
		}
	```

non si puo rimuovere durante lo scorrimento:
soluzione:
```
Iterator<Integer> it = list.iterator();  
while(it.hasNext()) {  
	if(it.next() == x)  
		it.remove();  
}
```

2.interno(la collezione si occupa di controllare)

	collezione.forEach(x-> azione)

(solo per collezioni dunque)

```
List<Integer> lista = Arrays.asList(1,2,3,4,5);

lista.forEach(x-> System.out.println(x*x));
```




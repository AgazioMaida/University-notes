Connessi ai metodi statici forniti da java.util.[[Collections]]
(max,min) c'è il problema di ordinare elementi(comparare)

Per comparare classi o strutture dati ci sono 2 modi:
1.  implementando  Comparable<T>(Serve quando:Vogliamo che gli oggetti si ordinino automaticamente (TreeSet, TreeMap))
> 		 int compareTo(T t)   (restituisce <>=0)
```
	public class Persona implements Comparable<Persona>{
......
	public int compareTo(Persona o){
		int v = cognome.compareTo(o.cognome)
		if (v==0)return nome.compareTo(o.nome)
		else return v}
```
(se non si vuole implementare il metodo compareTo)possiamo:
2. implementando Comparator<T>(ordine personalizzato e non si vuole modificare classe)
> 	int compare(T o1,To2)
```
		List<String> lista = Arrays.asList("marco","luca","agazio");
		Comparator<String> c =(a,b)-> a.compareTo(b);
		lista.sort(c);
		System.out.println(lista);
```



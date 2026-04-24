ha un unico metodo:
```
  Iterator<T> iterator()

```
siccome Iterator è una interfaccia (bisogna implementare tutti i metodi di Iterator(hasNext e next()))
```
classe implents Iterable <Tipo> es Integer
private tipo[] c;

public Iterator<Tipo> iterator(){
		return new Iterator<Tipo>(){
			private int indice = 0;
			
			public boolean hasNext(){
				return indice <c.length}
			public Tipo next(){
				if (!hasNext){
					throw new NoSuchElementException();  }  
				return lista[indice++];  
			}  
		};
		poi si puo iterare nel main
		Classe s=new Classe(new tipo[]{.....})
		
		for(int x: s){System.out.println(x)}
		}
			}

```


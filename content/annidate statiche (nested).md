```
public class Tastiera {  
	private String tipo;  
	public static class Tasto {  
	void stampa() {  
//System.out.println(tipo); ❌ ERRORE  

```
### Caratteristiche
- Sono `static`
- NON hanno riferimento a un oggetto esterno
- Non possono accedere direttamente ai campi non statici

 Sono più simili a classi normali
si creano
> [!Tastiera.Tasto key = new Tastiera.Tasto();]

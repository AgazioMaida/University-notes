
utile per:
1. creare oggetti immediatamete (senza avere nome e riferimenti)
2. per implementare interfacce

```
Runnable r = new Runnable() {  
	@Override  
	public void run() {  
		System.out.println("Eseguo!");  
}  
};  
  
r.run();
```
- Non hanno costruttori
- Non puoi riutilizzarle
-  Possono estendere **una sola classe** o implementare **una sola interfaccia**
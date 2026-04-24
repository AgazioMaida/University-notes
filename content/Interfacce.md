**implements**
Definiscono comportamenti comuni tra classi non legate da una gerarchia. 

"Simili alle classi astratte" ma a differenza di esse non hanno uno stato(non hanno attributi).
Possono contenere:

1. **costanti** (public static final)

2.  **metodi** sono :
. 
	- implicitamente public abstract   (devono essere implementati da classe che **implemets** interfaccia)
	
	- da java 8 :
			-  metodi con parola chiave **default **
				1.  (che possono essere implemetati nell'interfaccia e usati da classe che implements interfaccia) (per disambiguare: Interfaccia.super.nomeMetodo())
				2.  (può essere fatto override del metodo)
			- metodi statici(non godono del polimorfismo):
				-  non può essere fatto Override
	- da java 9:
			-metodi privati definiti nell'interfaccia. 

Le classi che implementano un'interfaccia:
 - devono implementare concretamente tutti i metodi da essa definiti 
 - altrimenti se se ne implementano solo un sottoinsieme o nessuno la classe deve essere definita astratta
 
 Nel momento in cui classe implementa interfaccia si instaura relazione di tipo is-a con Interfaccia,cioè la classe è di tipo Interfaccia(quindi valgono le regole del polimorfismo ad esempio è possibile:

```
#interfaccia                        #classeConcreta
SupportoRiscrivibile supporto = new Nastro()
supporto.leggi()
```
 
 Con interfaccia [[Ereditarietà multipla]] e problema del diamante.
 Nel caso in cui una classe implementa Interfacce diverse, che hanno a loro volta implementato concretamente  un metodo ( tutte le interfacce hanno stesso nome)  è possibile disambiguare il metodo voluto tramite:
```
	metodoClasse(){
		Interfaccia.super.nomeMetodo();
		}
```



Problema iterare su [[collezioni]] :
soluzione disaccoppiare:
1. oggetto su cui iterare([[iterable]])
2. oggetto che tiene la posizione([[iterator]])
usando Iterable e Iterator


per iterare su collezione for each:

```
for (Integer i:c)
	System.out.println(i)
	
che equivale a 

Iterator<Integer> it =c.iterator();
while (it.hasNext())
	System.out.print(it.next())
```

			
interfacce notevoli:

1. *Comparable():
			- unico metodo CompareTo(T b) : serve per comparare,richiede ordinamento naturale, ritorna <> = 0 
2. Clonable :
			- chi implementa tale interfaccia dichiara al metodo clone che può effettuare copia byte per byte 
			- se classe non la implementa : CloneNotSupportException
3. Serializable:
			- non possiede metodi o campi serve ad identificare il fatto che l’oggetto è serializzabile, cioè memorizzabile su un certo supporto
4. *Runnuble():
			- unico metodo run() che ogni classe che la implementa puo rendere diverso il comportamento--> polimorfismo


Le interfacce come Runnable permettono passaggio per funzioni (passaggio di comportamenti) ad esempio
```
public interface OperatoreBinario{
		double applica(double a ,double b)
		}
		
		
public enum Operazioni implemnts OperatoreBinario{
		SOMMA{public applica(double a ,double b){return a+b}}}
		DIFFERENZA{public applica(double a ,double b){return a-b}}}
		PRODOTTO{public applica(double a ,double b){return a*b}}}

QUINDI POSSO RENDERE ENUM ESTENDIBILI QUANTO VOGLIO(aggiungendo comportamento tramite interfacce)
```


Le interfacce non si possono istanziare direttamente ma si usa il meccanismo delle classi anonime per creare al volo un oggetto che implementa un'interfaccia(vedi swing)
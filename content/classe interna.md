(inner class)---> non statiche 

```
public class Persona {

	private String nome;
	
	public class Studente{

		private int matricola ;

		public Studente(int matricola ) {

			this.matricola = matricola;

		}

		public int getMatricola() {

			return this.matricola;

		}

		public String toString() {

			return Persona.this.nome+ " "+this.matricola;

}

}

public Persona(String nome) {

this.nome = nome;

}

public static void main(String[] args) {

Persona p = new Persona("Agazio");

Studente a = p.new Studente(2140787);

System.out.println(a);

}

}



```
- `Studente` è definita **dentro** `Persona`
- Non è `static`, quindi è una **inner class non statica**
- Ogni oggetto `studente` è **legato a una specifica Persona
- ogni inner class **può accedere anche ai campi `private` della classe esterna**(ClasseEsterna.this.campoEsterno)
###  Accesso ai campi della classe esterna

(Dentro `Tasto`)->return Persona.this.nome;(per disambiguare)
(oppure) return nome

per creare 
```
rifOggettoClasseEsterna.new ClasseInterna()
```
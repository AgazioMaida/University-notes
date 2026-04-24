mette in corrispondenza coppia chiave valore
k non duplicate
v anche duplicati
linterfaccia Map è implementata da:

1. Hashmap (veloce ,non ordinato)
2. TreeMap(ordinamento naturale chiavi)
3. LinkedHashMap(mantiene ordine
inserimento chiavi)
metodi:
	- keySet() insimee delle chiavi
	- values() elenco valori(con ripetizione)
	- entrySet() restituisce Map.entry<K,V>  e si puo conoscere getkey() e getValue()



	- map.put(k, v); // inserisce  
	- map.get(k); // prende valore  
	- map.remove(k); // rimuove  
	- map.containsKey(k); // controlla chiave  
	- map.containsValue(v);// controlla valore



HashMap
```
iterare su chiavi
for (Integer k : map.keySet()) {  
	System.out.println(k);
```
iterare su valori
```
for (String v : map.values()) {  
	System.out.println(v);
```
iterare su chiavi+valori
```
for (Map.Entry<Integer, String> e : map.entrySet()) {  
	System.out.println(e.getKey() + " → " + e.getValue());  
}
```
collezione delle coppie e dei valori di tipo
Map.entry()<K,V>  ci da coppie (k,v)


quindi il forEach(BiConsumer) usa proprio Map.entry<K,V>


altri metodi
merge(chiave,valore,BiFunction)
of(k1,v1,k2,v2....) crea una mappadei tipi corrispondenti



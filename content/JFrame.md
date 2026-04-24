###  Finestra
###  Metodo uso:
	Creare una classe  che estende JFrame nella quale inserire nel costruttore campi (componenti) e i metodi  desiderati.

### Campi principali (componente):
		- JButton
		- JTextField
		- JTextArea ecc
aggiunti  e posizionati tramite metodo:
		  ***add(componente,Tipo[LayoutManager.Posizione](https://docs.oracle.com/javase/tutorial/uiswing/layout/visual.html))*** 
			

  LayoutManager appositamente creato con  setLayout.

		

 metodi  :
	1. **setLocationRelativeTo**(null)     centro
	2. .**setLocation**(y,x)  posizione desiderata
	3. **setSize**(L,H);	4.**setDefaultCloseOperation**(JFrame.EXIT_ON_CLOSE)
	4. **[[setLayout]]**(new [[BorderLayout]]())
	5. add(....)
	6. **setVisible**(true)




```
public class Finestra extends JFrame implements ActionListener{
	
	private Button bottone;
	private JTextArea areaTesto;
	private JTextField rigoTesto;

	public Finestra(){
		super("titolo finestra");

		this.bottone = new JButton("cliccami");
		this.areaTesto = new JTextArea();
		this.rigoTesto = new JTextField();

		setLocationRelativeTo(null);
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setSize(800,500);
		setLayout(new BorderLayout())

		add(bottone,BorderLayout.PAGE_END);
		add(rigoTesto,BorderLayout.PAGE_START);
		add(areaTesto,BorderLayout.CENTER);


		
		bottone.addActionListener(new ActionListener(){
		public void actionPerformed(ActionEvent e)
		String testo = rigoTesto.getText();
		if(!testo.equals(" ")){
			areaTesto.append(testo);
			rigoTesto.setText("")
		}
		})
		setVisible(true);
	}


}
In questa implementazione oltre alla struttura di base di una finestra vi è aggiunto anche un evento nel momento in cui viene cliccato il bottone il testo scritto nel rigo viene aggiunto all'area. il comportamento è dato da interfaccia ActionListener, ma in quanto tale non può essere istanziata direttamente ma java fornisce un meccanismo per implemetarla mediante l'utilizzo di una classe anonima


```
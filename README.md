# GAMA CrowdControl

Eventi che prevedono l'affluenza di un gran numero di persone possono risultare problematici da un punto di vista della sicurezza dei partecipanti nel caso in cui venga percepita una situazione di pericolo che spinge le persone a scappare, infatti in queste situazioni può accadere che le persone possano riportare dei danni. Risulta quindi interessante lo studio del comportamento di una folla in tali situazioni per poter poi organizzare al meglio la gestione degli spazi e delle relative uscite di emergenza. Tuttavia, la pericolosità di queste dinamiche rende impossibile svolgere degli esperimenti in situazioni reali e per questo diventa particolarmente utile riuscire a simulare adeguatamente questi fenomeni, guidati dalle informazioni che è possibile ricavare da immagini, video o testimonianze relative ad eventi realmente accaduti. 

Diversi lavori hanno cercato di modellizzare il movimento di una folla analogamente al moto di un fluido, descrivendo il comportamento di una folla da un punto di vista macroscopico. In questi termini ciascuna persona è sottoposta alle leggi della fisica che governano il moto dei fluidi e il loro insieme viene considerato come un'unica entità. Questi modelli si concentrano principalmente sulla pianificazione di uscite di emergenza e non prendono in considerazione l'interazione tra singoli individui, ciascuno dei quali potrebbe essere considerato come un'entità autonoma. 

Un'altra opzione consiste nel tentativo di descrivere il comportamento della folla a partire dal singolo individuo, modellizzando il processo decisionale del singolo come risposta a stimoli che arrivano dall'ambiente e dagli altri individui. In questa ottica, la formazione ed il moto di una folla diventa un fenomeno emergente che ha origine dalla definizione di regole che determinano il comportamento dei singoli componenti del sistema. Seguendo questo schema è possibile indagare il ruolo che ha il comportamento umano nella formazione e nel moto delle folle in situazioni di panico. La metodologia computazionale che permette di integrare questi aspetti è la Simulazione a Multi Agenti (MAS) con la quale è possibile definire un certo numero di agenti autonomi con delle regole che permettono di farli interagire.

Il modello che sfrutta l'analogia con fenomeni di idrodinamica è più adatto a descrivere situazioni in cui la densità della folla è estremamente alta ma risulta più debole nel momento in cui si vogliano riprodurre situazioni che si osservano in situazioni reali. Ad esempio, in presenza di due uscite questo modello prevede che entrambe le uscite vengano ugualmente sfruttate invece in situazioni reali si osserva che un'uscita è congestionata mentre l'altra viene usata di meno. Questo può essere dovuto al fatto che un individuo in una situazione di panico si limita a seguire le persone che ha intorno, non rendendosi conto che l'uscita alternativa possa essere più libera. Oltre a questo il modello si basa sulle equazioni dell'idrodinamica che sono più difficili da maneggiare. Al contrario modelli MAS si basano su regole più semplici e possono tener conto di forze sociali in grado di riprodurre il comportamento  relativo all'utilizzo delle due uscite di emergenza descritto sopra. Tuttavia questi modello sono molto dispendiosi dal punto di vista computazionale perché richiedono di elaborare simultaneamente il comportamento di tutti gli agenti presenti nella simulazione.

Nel presente lavoro abbiamo riprodotto un modello MAS in cui sono presenti due tipi di agenti: le persone e le celle, le quali rappresentano lo spazio discreto su cui le persone si muovono. Per semplicità, ci riferiremo ad agenti per indicare le persone e a celle per indicare gli agenti di tipo cella. Il modello prende ispirazione dalla chemiotassi, fenomeno secondo il quale organismi biologici seguono delle sostanze chimiche che fungono da traccia per direzionare i loro movimenti. L'intensità di queste tracce è descritta da una coppia di valori che è presente all'interno di ogni cella e ciascun agente sceglie una cella su cui muoversi in base a questi valori: il primo indica la distanza dalla cella relativa all'uscita più vicina mentre il secondo tiene conto del movimento degli altri agenti, infatti se uno di questi si muove lascia una traccia sulla cella che si diffonde nel tempo sulle celle immediatamente vicine.

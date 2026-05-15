## Analisi e Specifica Programma principale

Il prodotto sofwtare da realizzare è un programma gestionale che permetterà la coordinazione di un aula studio: l'obiettivo del programma è di facilitare, automatizzando e velocizzando ogni possibile scenario tecnico, il lavoro del personale dell'aula.

All’esecuzione del programma  l’utente attraverserà una fase di configurazione, nella quale quest’ultimo inserirà tutti le informazioni essenziali all’avvio del sistema. Successivamente tutte le operazioni saranno disponibili, organizzate e partizionate tramite un menu intuitivo.  Il menù avrà 3 macrosezioni: la prima dedicata  alla gestione degli studenti, la seconda riguarderà le prenotazioni e la terza conterrà operazioni di sistema.

E' essenziale trovare un connubio tra limitazioni imposte funzionalmente al sistema e limitazioni imposte allo scopo di mantenere coerenza semantica con la risoluzione del problema in sè, quindi bisognerà caratterizzare il programma imponendo dei canoni inerenti le operazioni di questo; per esempio imporre un numero massimo di prenotazioni effettuabili da un singolo studente e stabilire un lasso temporale fisso di giorni prenotabili, questi fattori serviranno per generalizzare il sistema a qualunque tipo di contesto e saranno inseriti e definiti in fase di inializzazione dal cliente. Anche al fine di prevenire input spiacevoli è necessario porre delle precondizioni che questi dati in entrata devono rispettare: l'utente non potrà inserire un numero superiore a 10 per le prenotazioni effettuabili dal singolo studente, ed un valore maggiore di 20 riguardo l'ultimo giorno prenotabile dalla data corrente.

Inoltre è deducibile dai requisiti imposti dal cliente che esclusivamente gli studenti registrati potranno accedere all'aula studio e usufruire delle sue funzionalità.
Il servizio dell'aula studio verra suddiviso in fasce orarie e giorni quindi è senza dubbio essenziale per la configurazione e inializazione del sistema definire il numero di posti dell'aula studio, l'orario di apertura, l'orario di chiusura, la durata di ciascuna fascia oraria e la data corrente; questi fattori sono strettamente dipendenti all'aula studio in se, quindi per mantenere la parametricità del programma è necessario richiedere le informazioni al cliente. Ovviamente affinchè il programma funzioni correttamente e mantenga un certo rigore logico c'è la necessità che questi parametri siano validi: il numero di posti non può essere nè un valore negativo o nullo, nè un valore eccessivamente elevato, si assume un valore massimo di 10.000 posti; riguardo gli orari di servizio, l'orario di apertura dovrà essere necessariamente antecedente a quello di chiusura ed inoltre il numero di fasce orarie dovrà essere consono alla durata della giornata lavorativa: l'arco di tempo di ciascuna fascia oraria, ottenuta dal calcolo della ripartizione del tempo, dovrà essere un numero intero compreso tra 1 e 4. Bisognerà imporre un limite di validità anche per la data corrente, questa dovrà essere successiva al 01/01/2000 e precedente al 01/01/3000.

Dati di input: il programma prende in input il numero n di posti dell' aula studio, l'orario di apertura o_a , l'orario di chiusura o_c,  il numero di fascie orarie f e la data corrente d_c

Precondizioni: 

1)Il numero di posti dell'aula è un valore intero positivo valido:  n∈Z : 0 < n < 10.000

2)Il valore dell'orario di apertura è minore del valore dell'orario di chiusura, entrambi sono valori validi compresi tra 0 e 23:  0 <= o_a < o_c <= 23 

3)Ogni fascia oraria dovrà avere la stessa durata, corrispondente ad un valore tra 1 e 4 estremi inclusi:  ((o_c - o_a) / f = d, d ∈ {1, 2, 3, 4}

4)La data corrente è valida: l'anno è compreso tra 2000 e 3000 estremi inclusi

Postcondizioni: 

Sarà effettuato il calcolo della durata di ciascuna fascia oraria d ed il sistema verrà configurato e formattato in base ad esso, inoltre il numero di posti verrà inializzato a n, la  data corrente a d_c.

Qual'ora qualsiasi precondizione non sia rispettata sarà concesso all'utente di riprovare l'inserimento un numero massimo di 5 volte, all'esaurirsi dei tentativi totali il programma verrà arrestato.

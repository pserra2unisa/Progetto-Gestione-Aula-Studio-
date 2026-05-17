Analisi e Specifica Registra Studenti

Poichè l'aula studio concederà l'accesso esclusivamente agli studenti registrati, è necessaria la realizzazione di un operatore che permetta la registrazione degli studenti, salvandone i dati nel sistema. Ciascuno studente avrà un nominativo, una matricola e il corso di studi frequentato.

Ogni studente potrà registrarsi solamente una volta, inoltre i parametri inseriti, inerenti lo studente, non dovranno essere nulli. La funzione restituirà true qualora l'operazione sia a buon fine, in caso contrario false.

Specifica Sintattica

register_student(intero, stringa, stringa, stringa) --> bool

Specifica Semantica

register_student(student_id, name, surname, degree ) --> r

Precondizioni:

1) student_id ≠ x ∀ x ∈ {x : x è l'id di uno studente registrato} ⋀ student_id > 0

2) name ≠ nil, surname ≠ nil, degree ≠ nil

Postcondizioni: 
s = (student_id, name, surname, degree), s ∈ S ⋀ r = true

Qual'ora le precondizioni non siano rispettate l'utente potrà riprovare un massimo di 5 volte prima che l'operazione termini.
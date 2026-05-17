Analisi e Specifica Prenotazione

Permettere le prenotazioni degli studenti è un requisito fondamentale che l'aula studio dovrà soddisfare, ciascuna prenotazione è caratterizzata dallo studente prenotatosi, identificato tramite matricola, da data e fascia oraria di occupazione e dal posto assegnato dal sistema. Affinchè una prenotazione sia effettuabile, lo studente deve essere registrato e non deve aver raggiunto il numero massimo di prenotazioni consentite, inoltre devono esserci posti disponibili nella fascia oraria selezionata del giorno specificato, ovviamente data e fascia oraria dovranno essere valide secondo i canoni del sistema.

Una volta che la funzione è stata richiamata comparirà a schermo un menu di selezione inerente alle fasce orarie prenotabili della data specificata, qualora la data selezionata sia quella corrente, compariranno nel menu solo le fasce antecedenti a quella attuale.

Specifica Sintattica:

reserve_seat(intero, data) -> bool    

Specifica Semantica

reserve_seat(student_id, d) -> r

Precondizioni:
1) student_id ∈ {x : x è l'id di uno studente , studente ∈ S } ⋀ R(student_id) < max_r

2) current_date <= d <= current_date + max_d

Postcondizioni:

1) Qualora ci siano posti disponibili nella fascia oraria e giorno selezionati, la prenotazione sarà effettuata

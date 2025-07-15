# Catene predefinite: INPUT, OUTPUT, FORWARD

Le catene predefinite INPUT, OUTPUT e FORWARD sono fondamentali nel contesto delle regole di filtraggio del traffico di rete all'interno di un sistema di gestione dei firewall. Ogni catena ha un ruolo specifico e un utilizzo ben definito per garantire la sicurezza e il corretto indirizzamento dei pacchetti all'interno del sistema.

## Catena INPUT

La catena INPUT è responsabile del filtraggio del traffico in ingresso verso il sistema. Questa catena è attivata per ogni pacchetto che è destinato alla macchina stessa, che sia destinato ad un servizio locale o semplicemente passante. Le regole impostate nella catena INPUT determinano se un pacchetto deve essere accettato o rifiutato in base a criteri come l'indirizzo IP di origine, la porta di destinazione e altre informazioni pertinenti.

## Catena OUTPUT

La catena OUTPUT, al contrario della catena INPUT, si occupa del filtraggio del traffico in uscita dal sistema. Ogni pacchetto generato dalla macchina stessa o in transito attraverso di essa viene controllato dalla catena OUTPUT. Le regole impostate in questa catena determinano se un pacchetto generato localmente deve essere permesso di uscire o meno, garantendo un controllo accurato del traffico che lascia il sistema.

## Catena FORWARD

La catena FORWARD è utilizzata per il filtraggio del traffico di transito attraverso il sistema, ad esempio per il routing dei pacchetti tra due interfacce di rete. Questa catena è attivata solo per i pacchetti che non sono destinati direttamente alla macchina stessa, ma devono essere inoltrati verso un'altra destinazione. Le regole impostate nella catena FORWARD determinano se un pacchetto deve essere inoltrato o rifiutato in base alle politiche di sicurezza e di routing della rete.

In conclusione, le catene predefinite INPUT, OUTPUT e FORWARD svolgono ruoli distinti ma complementari nel garantire la sicurezza e il corretto funzionamento del sistema di gestione dei firewall. Configurare regole di filtraggio appropriate in ciascuna di queste catene è essenziale per proteggere la rete da minacce esterne e garantire un corretto indirizzamento dei pacchetti all'interno del sistema.
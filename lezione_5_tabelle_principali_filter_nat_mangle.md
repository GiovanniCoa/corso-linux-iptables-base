# Tabelle principali: filter, nat, mangle

Le tabelle sono un concetto fondamentale nel firewall di Linux, in particolare nel framework di netfilter. Le tabelle principali utilizzate sono tre: filter, nat e mangle. Ognuna di queste tabelle ha uno scopo specifico e presenta differenze significative tra loro.

## Tavola di filtro (filter)

La tabella di filtro è la tabella predefinita utilizzata per il filtraggio del traffico. Questa tabella gestisce il traffico in base a regole di filtro, che possono essere di tipo ACCEPT, DROP o REJECT. Le regole nella tabella di filtro sono principalmente utilizzate per controllare il traffico in ingresso e in uscita sul sistema.

## Tavola di traduzione degli indirizzi di rete (nat)

La tabella di traduzione degli indirizzi di rete, o nat, è utilizzata per modificare gli indirizzi IP e le porte dei pacchetti in transito attraverso il firewall. La tabella nat è spesso utilizzata per implementare il mascheramento (NAT) e il port forwarding. Questa tabella è fondamentale per consentire la comunicazione tra le reti interne ed esterne.

## Tabella di manipolazione (mangle)

La tabella di manipolazione, o mangle, è utilizzata per modificare il pacchetto in vari modi. Questa tabella consente di apportare modifiche avanzate ai pacchetti, come la modifica del tipo di servizio (TOS), il marcatore di connessione e il rilevamento di pacchetti specifici. La tabella mangle è spesso utilizzata per scopi avanzati di routing e QoS.

## Differenze tra le tabelle

Le principali differenze tra le tabelle filter, nat e mangle risiedono nei loro scopi e nelle operazioni che eseguono sui pacchetti. Mentre la tabella di filtro si concentra sul filtraggio del traffico in base a regole di filtro, la tabella nat gestisce la traduzione degli indirizzi IP e delle porte, mentre la tabella mangle è utilizzata per manipolare i pacchetti in vari modi.

In conclusione, le tabelle filter, nat e mangle sono fondamentali per il funzionamento del firewall di Linux e svolgono ruoli diversi nel controllo e nel routing del traffico di rete. Comprendere le differenze tra queste tabelle è essenziale per la corretta configurazione e gestione del firewall.
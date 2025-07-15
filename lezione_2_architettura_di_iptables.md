# Architettura di iptables

iptables è uno strumento molto potente per la gestione del firewall su sistemi Linux. Per comprendere appieno come funziona, è importante comprendere la sua architettura, che si basa su concetti chiave come tabelle, catene e regole.

## Tabelle
Le tabelle di iptables sono dei contenitori logici in cui vengono memorizzate le regole del firewall. Attualmente, ci sono 5 tabelle disponibili:
- **filter**: è la tabella di default e contiene le regole per il filtraggio del traffico in base all'indirizzo IP, al protocollo e alla porta.
- **nat**: contiene le regole per il Network Address Translation (NAT), ovvero per modificare gli indirizzi IP e le porte dei pacchetti.
- **mangle**: questa tabella è utilizzata per modificare i pacchetti in vari modi, come ad esempio cambiare il tipo di servizio (TOS) o il TTL (Time To Live).
- **raw**: contiene le regole per il filtraggio dei pacchetti prima che vengano processati dalle altre tabelle.
- **security**: utilizzata per l'introduzione di regole di sicurezza aggiuntive.

## Catene
Le catene sono una serie di regole organizzate in modo gerarchico all'interno di una tabella. Ci sono tre catene predefinite che vengono utilizzate comunemente:
- **INPUT**: contiene le regole per il traffico in ingresso verso il sistema.
- **OUTPUT**: contiene le regole per il traffico in uscita dal sistema.
- **FORWARD**: contiene le regole per il traffico che attraversa il sistema.

Inoltre, è possibile creare catene personalizzate per gestire situazioni specifiche.

## Regole
Le regole di iptables sono composte da una serie di criteri che determinano come il traffico deve essere gestito. Ogni regola è composta da:
- **-A/--append**: specifica l'azione da intraprendere per la regola (ad esempio, accettare, rifiutare o saltare).
- **-i/--in-interface**: specifica l'interfaccia di ingresso del pacchetto.
- **-o/--out-interface**: specifica l'interfaccia di uscita del pacchetto.
- **-s/--source**: specifica l'indirizzo IP di origine del pacchetto.
- **-d/--destination**: specifica l'indirizzo IP di destinazione del pacchetto.
- **-p/--protocol**: specifica il protocollo del pacchetto (TCP, UDP, ICMP, etc.).
- **--sport/--dport**: specifica la porta sorgente e di destinazione del pacchetto.

Utilizzando queste opzioni e combinandole in modo appropriato, è possibile creare regole molto specifiche per gestire il traffico di rete in modo efficace.

In conclusione, l'architettura di iptables si basa su tabelle, catene e regole che permettono di configurare in modo preciso il firewall su un sistema Linux. Comprendere questi concetti è fondamentale per poter sfruttare appieno le potenzialità di iptables e garantire la sic
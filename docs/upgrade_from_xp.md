# Upgrade da Windows XP

Windows 7 in fase di installazione offre l'opportunità di fare un'installazione pulita oppure di effettuare l'upgrade del sistema.

Entrambe le soluzioni hanno un pro e un contro, iniziamo ad affrontare la questione dal punto di vista dell'utente finale:

## Upgrade

Questa operazioni prevede l'aggiornamento del proprio sistema operativo da Windows XP a Windows 7, durante tale processo verranno salvaguardate le installazioni dei programmi e i profili utenti permettendo di avere il proprio ambiente di lavoro preservato nelle impostazioni e nei file.

### Pro

* Non si deve effettuare una reinstallazione dei programmi
* Non si deve effettuare un backup dei propri files(anche se è buona norma farlo sempre) durante l'upgrade
* Se si hanno file condivisi o cifrati verranno mantenute tutte le autorizzazioni

### Contro

* Il sistema si porterà dietro eventuali problemi e *sporcizzie* dell'installazione di Windows XP
* Si avrà oltre alla cartella Users (una delle novità di Windows 7) anche la cartella *"Document and Settings"* che sarà un link che garantisce la compatibilità con alcuni programmi che hanno bisogno di questo path specifico
* Il registro di sistema conterrà un ibrido tra le due installazioni con puntamenti a librerie vecchie e nuove con una più alta probabilità di failure

## Clean Install

Questa installazione naturalmente è quella fatta nel LAB precedente in cui su un disco vuoto(o comunque formattato durante l'installazione) viene installata una copia pulita di Windows 7.

### Pro

* Il sistema non conterrà riferimenti ad altre installazioni, non avrà puntamenti a librerie precedenti
* Sarà possibile installare una versione a 64bit (la versione di XP era una versione particolare)
* Non si avranno residui di servizi installati con XP

### Contro

* Se si avevano installati i programmi, questi, dovranno essere reinstallati
* Se si aveva un utente andrà ricreato e dovranno essere copiati tutti i files.


## Cosa scegliere quindi?

Come sempre non esiste una scelta migliore dell'altra, dipende sempre dallo scenario in cui ci troviamo.
Per esperienza comunque ogni volta che posso scegliere preferisco sempre fare una "Clean Installation" di sistemi operativi, siano essi Windows, Gnu\Linux, Mac OS o Android.
Il motivo fondamentale per cui preferisco installare da 0 è che il mondo dei sistemi operativi si evolve con rapidità e molte volte il dover garantire un layer di retro compatibilità rende il sistema più instabile o comunque non riesce in pieno a dare il meglio di se.

# Problemi delle installazioni Dual Boot

Quando si installa Windows 7 o comunque un sistema operativo insieme ad un altro c'è bisogno che il pc durante la fase di boot sappia quali sistemi ci siano installati su di esso e come fare ad avviare uno piuttosto che un altro.

## Quindi come fa il pc a sapere che c'è un sistema da avviare?

All'accensione del pc viene letto nel disco che contiene il flag di boot il primo settore di 512 Bytes chiamato anche MBR(GPT nelle versioni nuove) che a sua volta contiene un puntamento al file di configurazione del boot loader (Windows ha il suo, Gnu\Linux e Mac il loro
# UEFI o EFI

Con Windows 7 è stato introdotto il pieno supporto a **UEFI**(Unified Extensible Firmware Interface) che sta con il passare del tempo sostituendo l'EFI, cosa c'è di diverso tra i due sistemi?

- Possibilità di avere un'interfaccia grafica simile ad un ambiente operativo vero e proprio che da accesso a funzionalità in maniera rapida e veloce (Esempio Asus Smart Boot che integra firefox per navigare senza accendere il pc)
- Possibilità di utilizzare dischi più grandi di 2,2 Terabyte
- Maggiore sicurezza grazie alle protezioni di controllo del checksum che impedisce attacchi di tipo bootkit
- Supporto al partizionamento GPT dei dischi

# MBR o GPT

Grazie alla potenza di UEFI viene sfruttato anche GPT che è il nuovo sistema di avvio che a differenza di MBR i cui limiti erano:

- grandezza limitata (64byte)
- possibilità di avere solo 4 partizioni primarie
- impossibilità ad usare dischi più grandi di 2,2 Terabyte

GPT va a creare uno strato ridondato in cui la prima parte (layer 0) è di compatibilità con l'MBR (se un computer con bios EFI accede ad un disco GPT vedrà quel disco come inutilizzabile, se così non fosse si rischierebbe di sovrascriverlo con mbr ogni volta)
 
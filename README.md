# Bucchero Kantharos — Digital Experience

Progetto realizzato nell'ambito del bando **Bucchero Next**, Percorso B TEENS — Opzione 4 Digital Experience.

## Descrizione

Un kantharos etrusco in bucchero del VI sec. a.C., conservato al MAAM di Grosseto (cat. 163492), è stato acquisito fotogrammetricamente con RealityScan (381 immagini) e stampato in 3D. Un tag NFC adesivo applicato all'interno della coppa, avvicinando il telefono, apre questa pagina web con il modello 3D interattivo e una traccia audio di sottofondo.

## Come funziona

1. Acquisizione fotogrammetrica → modello 3D su Sketchfab
2. Stampa 3D a filamento PLA
3. Tag NFC adesivo all'interno della coppa → URL di questa pagina
4. Avvicina il telefono → si apre la Digital Experience

## Struttura del repository

```
bucchero-code/
├── index.html          # Pagina principale (target NFC / GitHub Pages)
├── assets/
│   ├── audio/          # Traccia audio (mp3 + webm)
│   └── images/         # Foto del processo (stampa, NFC, dipinto, disegno)
└── README.md
```

## Tecnologie

- HTML5 / CSS3 / JavaScript vanilla (nessuna dipendenza esterna)
- [Sketchfab Embed API](https://sketchfab.com) per il viewer 3D
- GitHub Pages per l'hosting
- [Bando BuccheroNext](https://www.ufficioscolasticoregionalelazio.it/wp-content/uploads/2026/03/Bando-Bucchero-Next_Firmato.pdf) della Regione Lazio


## Ringraziamenti

- MAAM di Grosseto e SABAP per il modello 3D del bucchero
- Sketchfab per la piattaforma di visualizzazione 3D

---

*Bucchero Next — Percorso B TEENS, Opzione 4 Digital Experience*

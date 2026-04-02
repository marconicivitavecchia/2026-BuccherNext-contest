# Bucchero Next — Digital Experience

## Contesto del progetto

Progetto scolastico per il bando **Bucchero Next**, Percorso B TEENS — Opzione 4 Digital Experience.
Un kantharos etrusco in bucchero (VI sec. a.C., MAAM Grosseto, cat. 163492) è stato:
1. Acquisito fotogrammetricamente con RealityScan (381 foto) → modello 3D su Sketchfab
2. Stampato in 3D a filamento PLA
3. Dotato di un tag NFC adesivo all'interno della coppa
4. Quando il telefono si avvicina al tag NFC, si apre `index.html` con il modello 3D e audio

La pagina è pubblicata su **GitHub Pages** (branch `main`, root `/`).

## Struttura del repository

```
bucchero-code/
├── index.html              # Pagina principale (unico file di codice)
├── assets/
│   ├── audio/
│   │   ├── output.mp3
│   │   └── output.webm
│   └── images/
│       ├── stampa3D-bucchero.jpeg
│       ├── stampa3D-NFC.jpeg
│       ├── stampa3D-bucchero-ornato.jpeg
│       └── disegno-bucchero-ornato.jpeg
└── README.md
```

File sorgente NON nella repo web (cartella padre `../`):
- `163492_LP.obj` + `.mtl` + texture JPG — modello 3D originale 28MB
- `bucchero.3mf`, `*.gcode` — file di stampa 3D
- `audio/VasoEtruscoFinale.mov` — video sorgente audio

## Scelte tecniche

- **Nessuna dipendenza esterna** — CSS e JS sono embedded in `index.html`
- **Viewer 3D**: embed Sketchfab (`https://sketchfab.com/models/80361348b89b400abe93dd7dfd8ac5a5/embed`)
- **Audio**: `<audio autoplay loop>` con fallback tap se autoplay è bloccato (iOS Safari)
- **Lingua**: bilingue italiano + inglese
- **Palette**: sfondo `#0a0a0a`, accenti oro `#c8902a`

## Link utili

- Modello Sketchfab: `https://sketchfab.com/3d-models/bucchero-kantharos-80361348b89b400abe93dd7dfd8ac5a5`
- GitHub Pages URL (da configurare): `https://marconicivitavecchia.github.io/2026-BuccherNext-contest/`
- Bando BuccheroNext Regione Lazio: `https://www.ufficioscolasticoregionalelazio.it/wp-content/uploads/2026/03/Bando-Bucchero-Next_Firmato.pdf`




## Note per lo sviluppo

- Modificare solo `index.html` per interventi sulla pagina web
- Il pulsante audio (#audio-btn) gestisce autoplay bloccato: se `audio.play()` è rifiutato, mostra "Play" e parte al primo tap
- Le foto nella gallery sono ordinate: stampa grezza → NFC → dipinto → disegno
- Il file OBJ non va mai aggiunto alla repo (troppo grande, si usa l'embed Sketchfab)

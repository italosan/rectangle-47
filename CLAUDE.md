# Rectangle 47

Landing del workshop "Rectangle 47, seconda parte" (PUG Bari, 20 settembre 2026). Sito statico, nessun build, deploy su Cloudflare Pages a ogni push.

## Tesi
Il file di design è il progetto, non la sua immagine. Naming, variabili e struttura sono la sintassi con cui il progetto si lascia leggere da chi viene dopo, persona o macchina. La macchina esegue, il criterio resta umano.

## Regole
- Le custom property CSS hanno gli stessi nomi delle variabili Figma: `--surface-primary`, `--text-secondary`, `--accent`, `--space-m`. Non inventarne di nuove, non usare valori esadecimali fuori da `:root`.
- Le classi hanno gli stessi nomi dei layer Figma, convenzione componente / variante / stato scritta con trattini: `card-product`, `button-primary`, `feature-cell`.
- Un solo carattere, IBM Plex Sans, self-hosted in `fonts/`. Solo rettangoli, radius 0, nessuna ombra.
- Niente framework, niente build, niente dipendenze. HTML in `index.html`, CSS in `style.css` collegato con un `<link>` nel `head`.
- File Figma di riferimento: https://www.figma.com/design/hxR5D1lBxPbEHqsmVZOqXQ/rectangle47 (pagina Home).

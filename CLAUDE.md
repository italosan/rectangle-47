# Rectangle 47

Sito del workshop "Rectangle 47. Scrivere per un lettore che non perdona" e del talk "Rectangle 47. Il lettore che non perdona", PUG Bari, 20 settembre 2026. Italo Sannino. Online su rectangle-47.pages.dev, deploy su Cloudflare Pages a ogni push.

## Come è fatto

- HTML statico scritto a mano. Nessun build, nessun framework, nessuna dipendenza. Font locali in fonts/.
- Tre pagine. La landing in index.html, la pagina dei partecipanti in setup/index.html, la pagina della demo in demo/index.html. Non se ne aggiungono altre senza che Italo lo chieda.
- CSS. style.css per la landing, setup/setup.css per le pagine dei partecipanti. Prima di scrivere CSS guarda quale foglio carica la pagina e riusa quello che c'è.
- Le custom property e le classi di style.css hanno gli stessi nomi delle variabili e dei layer del file Figma. Non si rinominano e non se ne inventano di nuove.
- I testi della landing sono quelli della pagina Home del file Figma, footer compreso con "seconda parte". Non si correggono qui.

## Fonte e copia

- I markdown in setup/ sono la fonte. setup/il-metodo.md per /setup, setup/demo.md per /demo. L'HTML si allinea ai markdown, mai il contrario.
- I testi passano parola per parola. Non si riscrivono, non si riassumono, non si aggiunge niente.
- La sezione Modifiche dei markdown non va nelle pagine.
- Ogni prompt ha il suo bottone Copia, che copia solo il testo del prompt, compresa l'ultima riga sugli strumenti.

## Regole di lavoro

- Tocca solo i file nominati nel compito.
- Riusa markup, classi e script che ci sono già. Guarda la pagina accanto prima di scrivere.
- Nei testi in italiano niente lineette, punti e virgola o due punti nelle frasi. Frasi piane.
- Non fare commit né push. Li fa Italo da GitHub Desktop. Alla fine di ogni compito elenca i file e le righe cambiate.
# Rectangle 47. La demo

Workshop "Rectangle 47. Scrivere per un lettore che non perdona"
PUG Bari, 20 settembre 2026. Italo Sannino, italosannino.com

Sette prompt, da D1 a D7, sulla landing intera. Si parte dal file caotico, senza niente, e si arriva a un file che un lettore sa usare per costruire una pagina nuova. D1 e D2 sono i P3 e P4 dei partecipanti. Cambiano solo il file e il nome della pagina.

Non lanciateli sul piano gratuito di Figma. Da soli consumano le venti chiamate del mese.

## I file

- `landing-demo`. Un Duplicate di `landing-c`, fatto prima di ogni giro. Una sola pagina, "Home", nessuna variabile, nessuno stile, nessun componente. Da D1 a D6 si lavora qui, in una chat sola.
- `landing-c`. Il caotico pulito. Non si tocca mai. Serve solo al D7, in una chat nuova.
- Riserva. `landing-b` con i vecchi R, S, D, in fondo a questa pagina.

## Primo tempo. Quello che avete fatto voi

### D1 Variabili. È il vostro P3

> Nel file [URL di landing-demo] crea tu, usando gli strumenti Figma, una collezione di variabili chiamata "color" con una sola modalità.
>
> Dentro metti cinque variabili colore con questi nomi e questi valori. surface/primary #FFFFFF, surface/secondary #EFEAE1, text/primary #1A1917, text/secondary #6B675F, accent #D63A0E.
>
> Poi lega i fill dei layer della pagina "Home" alle variabili che hai creato, in base al ruolo di ogni layer.
>
> Non spiegarmi come farlo a mano, eseguilo in una sola chiamata. Alla fine dimmi quali variabili hai creato con i loro valori e quanti fill hai legato. Se un fill non ha una variabile adatta, lascialo com'è e dimmelo.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Da dire. Cinque variabili bastano a una card. A una pagina no. Guardate cosa ha lasciato fuori, la fascia scura e i filetti. Il sistema cresce quando il progetto lo chiede.

### D2 Nomi. È il vostro P4

> Nello stesso file, nella pagina "Home", rinomina tutti i layer che hanno ancora un nome di default, tipo Rectangle, Frame, Text, Ellipse, Group, compresi i layer di testo il cui nome coincide con il contenuto, che vanno chiamati per ruolo, per esempio title, description, price, label.
>
> Segui la convenzione "componente / variante / stato", con i nomi in inglese come le variabili, deducendo il ruolo di ogni layer dalla sua posizione, dimensione e contenuto. Dove non riesci a dedurlo, lascia il nome com'è e dimmelo.
>
> Esegui direttamente con gli strumenti Figma, in una sola chiamata. Alla fine elenca i layer rinominati con vecchio e nuovo nome.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

## Secondo tempo. Le due mosse che non avete fatto

### D3 Il vocabolario completo e l'auto layout

> Nello stesso file, nella pagina "Home", completa il design system e metti ordine nella struttura, usando gli strumenti Figma.
>
> Tre cose. Aggiungi alla collezione "color" le variabili che mancano per i fill e i filetti rimasti senza variabile, con questi nomi, surface/inverse, text/inverse, border/default, e con i valori che trovi nella pagina. Poi legali. Crea una collezione "space" con sei variabili numeriche, space/xs 4, space/s 8, space/m 16, space/l 24, space/xl 32, space/xxl 64. Crea sei stili di testo con questi nomi, type/display, type/heading, type/subheading, type/body, type/label, type/caption, leggendo carattere, corpo, peso e interlinea dai testi che ci sono già, dal più grande al più piccolo, e applica a ogni testo lo stile corrispondente.
>
> Poi metti in auto layout i contenitori che hanno figli in relazione tra loro, con spazi e padding legati alle variabili spazio, arrotondando le distanze attuali al valore più vicino della scala. La pagina deve restare identica a prima a guardarla.
>
> Non spiegarmi come farlo, eseguilo. Alla fine dimmi quante variabili hai creato, quanti stili hai creato e applicato, quanti frame hai messo in auto layout e quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Da dire mentre lavora. La tipografia è la prima struttura di lettura, e adesso ha un nome. L'auto layout dice come sta una cosa rispetto alle altre. Senza, il lettore copia le coordinate.

### D4 I componenti

> Nello stesso file crea una pagina nuova chiamata "Components" e trasforma in componenti i pezzi della pagina "Home" che si ripetono o che servirebbero in un'altra pagina, usando gli strumenti Figma.
>
> Sei componenti, con questi nomi. button, con le varianti che trovi nella pagina. card / product / default. nav / default / default. feature / cell / default. band / quote / default. footer / default / default. Ogni componente conserva variabili, stili di testo, nomi dei layer e auto layout che ha già. Nella pagina "Home" sostituisci ogni pezzo con un'istanza del suo componente. Le tre feature diventano tre istanze dello stesso componente, con i testi cambiati.
>
> La pagina "Home" deve restare identica a prima a guardarla. Non spiegarmi come farlo, eseguilo. Alla fine dimmi quali componenti hai creato, quante istanze hai messo in "Home" e quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Da mostrare. Il pannello Layers di Home, con i rombi viola delle istanze. Il quarto cardine.

## Terzo tempo. Il lettore usa il file

### D5 La styleguide, letta dal design system

Nessun colore, spazio o stile detto a Claude, solo "quelli che ci sono".

> Nello stesso file crea una pagina nuova chiamata "Styleguide" e costruiscila usando gli strumenti Figma.
>
> Dentro un frame 1440 con auto layout, quattro sezioni in colonna, una sotto l'altra. Prima sezione, tutte le variabili colore del file, ogni variabile con un campione quadrato e sotto il suo nome. Seconda sezione, le variabili spazio, ogni variabile con una barra alta quanto il suo valore e sotto il nome. Terza sezione, gli stili di testo, ogni stile con una riga di esempio nello stile stesso e sotto il nome. Quarta sezione, un'istanza di ogni componente della pagina "Components", con sotto il nome del componente.
>
> Usa solo variabili, stili e componenti che esistono già nel file. Nessun colore, spazio o carattere scritto a mano. Non toccare le altre pagine.
>
> Non spiegarmi come farlo, eseguilo. Alla fine dimmi quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

### D6 Una pagina nuova, coerente

Nella stessa chat, con l'URL di `landing-demo` scritto di nuovo. Così il D6 e il D7 sono lo stesso prompt, parola per parola, e cambia solo l'indirizzo.

> Nel file [URL] crea una pagina nuova chiamata "Product" con la pagina di dettaglio del prodotto che sta nella card della pagina "Home", usando gli strumenti Figma.
>
> Un frame 1440 in auto layout. Nav in alto, poi immagine grande a sinistra e a destra titolo, descrizione, prezzo e bottone "Aggiungi", poi una sezione di tre feature, poi il footer. Usa solo i componenti della pagina "Components", le variabili e gli stili di testo del file. Nessun colore, spazio, carattere o forma che non esista già nel file. Se ti serve qualcosa che non c'è, non inventarla, dimmelo.
>
> Non spiegarmi come farlo, eseguilo. Alla fine dimmi quali componenti hai usato e quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

### D7 Lo stesso prompt, sul file caotico

Chat nuova. Il prompt è il D6, con l'URL di `landing-c`.

Due esiti, tutti e due buoni. Se inventa, è il lettore che perdona, e perdonando inventa. Se si ferma, con Rectangle 47 anche il lettore migliore si ferma, e non è colpa sua. Nel dry run del 17 settembre si è fermato e ha scritto "qualsiasi pagina costruissi adesso sarebbe fatta di valori copiati dalla Home, cioè esattamente ciò che mi hai detto di non fare".

## Tempi

Da misurare nella prova del 18 settembre. Tetto, dodici minuti di macchina in tutto. Se li supera o sbaglia, in aula va la riserva.

| Prompt | Tempo | Chiamate | Note |
|---|---|---|---|
| D1 | | | |
| D2 | | | |
| D3 | | | |
| D4 | | | |
| D5 | | | |
| D6 | | | |
| D7 | | | |

## Riserva. R, S, D su `landing-b`

I tre prompt provati nel dry run del 17 settembre, 6:20 di macchina. Richiedono un file con il design system già fatto e la pagina "Home" come riferimento. Stanno nella versione 02 di `il-metodo.md`, sezione "Cosa ha fatto Italo", e restano validi così come sono.

## Modifiche

- 2026-09-17, chat 02.5 WS, versione 01. Dal giro con Antonia. La demo parte dai prompt dei partecipanti sulla landing intera e cresce da lì. Sette prompt da D1 a D7 al posto di R, S, D. Stili di testo e non variabili tipografiche. Un prompt per i componenti. Nomi di variabili, stili e componenti presi dal file `Rectangle47`. Tempi da misurare il 18.

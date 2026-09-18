# Rectangle 47. La demo

Workshop "Rectangle 47. Scrivere per un lettore che non perdona"
PUG Bari, 20 settembre 2026. Italo Sannino, italosannino.com

Sette prompt, da D1 a D7, sulla landing intera. Si parte dal file caotico, senza niente, e si arriva a un file che un lettore sa usare per costruire una pagina nuova. D1 e D2 sono i vostri P3 e P4. Cambiano solo il file e il nome della pagina.

Non lanciateli sul piano gratuito di Figma. Da soli consumano le venti chiamate del mese, e sul piano Starter un file ha al massimo tre pagine, mentre la demo ne crea tre oltre a Home. Serve un piano Education o a pagamento.

## Come si usano

- Il file caotico è su Figma Community, [landing-community](https://www.figma.com/community/file/1682759778269309945/landing-community). Open in Figma e la copia si apre nei vostri Drafts.
- Non si lavora mai sulla prima copia. Prima di cominciare fatene due Duplicate. Una copia di lavoro, per i prompt da D1 a D6. Una copia intatta, solo per il D7. In aula Italo le chiama `landing-work` e `landing-raw`.
- Da D1 a D6 si resta nella stessa chat. Il D7 va in una chat nuova, perché il lettore non deve ricordare niente di quello che ha fatto prima.
- L'URL del file va solo nel primo prompt di ogni chat. Quindi nel D1, e nel D7. Da D2 a D6 si scrive "nello stesso file". L'URL va corto, `figma.com/design/` più la chiave, senza il nome del file e senza i parametri dopo il punto di domanda.
- Se perdete la chat a metà, aprite una chat nuova e rilanciate il prompt a cui eravate con "Nel file [URL]" al posto di "Nello stesso file". Lo stato sta nel file, non nella chat.
- L'ultima riga di ogni prompt resta sempre.
- Dopo ogni prompt aprite il file e guardate. Sotto ogni prompt c'è scritto cosa.

## Primo tempo. Quello che avete fatto voi

### D1 Variabili. È il vostro P3

> Nel file [URL della copia di lavoro] crea tu, usando gli strumenti Figma, una collezione di variabili chiamata "color" con una sola modalità.
>
> Dentro metti cinque variabili colore con questi nomi e questi valori. surface/primary #FFFFFF, surface/secondary #EFEAE1, text/primary #1A1917, text/secondary #6B675F, accent #D63A0E.
>
> Poi lega i fill dei layer della pagina "Home" alle variabili che hai creato, in base al ruolo di ogni layer.
>
> Non spiegarmi come farlo a mano, eseguilo in una sola chiamata. Alla fine dimmi quali variabili hai creato con i loro valori e quanti fill hai legato. Se un fill non ha una variabile adatta, lascialo com'è e dimmelo.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Cosa guardare. Quanti fill ha legato e quali ha lasciato fuori. Cinque variabili bastano a una card. A una pagina no. Il sistema cresce quando il progetto lo chiede.

### D2 Nomi. È il vostro P4

> Nello stesso file, nella pagina "Home", rinomina tutti i layer che hanno ancora un nome di default, tipo Rectangle, Frame, Text, Ellipse, Group, compresi i layer di testo il cui nome coincide con il contenuto, che vanno chiamati per ruolo, per esempio title, description, price, label.
>
> Segui la convenzione "componente / variante / stato", con i nomi in inglese come le variabili, deducendo il ruolo di ogni layer dalla sua posizione, dimensione e contenuto. Dove non riesci a dedurlo, lascia il nome com'è e dimmelo.
>
> Esegui direttamente con gli strumenti Figma, in una sola chiamata. Alla fine elenca i layer rinominati con vecchio e nuovo nome.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Cosa guardare. Il pannello Layers. Le stesse forme di prima, ma ora si leggono. E leggete cosa vi segnala sulla struttura, il lettore vede come è fatto il file, non come appare.

## Secondo tempo. Le due mosse che non avete fatto

Un design system ha quattro cardini. Variabili e nomi li avete fatti voi. Qui ci sono gli altri due, auto layout e componenti, insieme agli spazi e agli stili di testo.

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

Cosa guardare. Il pannello Local variables, gli stili di testo, e il pannello Layers della card. La tipografia è la prima struttura di lettura, e adesso ha un nome. L'auto layout dice come sta una cosa rispetto alle altre. Senza, il lettore copia le coordinate.

### D4 I componenti

> Nello stesso file crea una pagina nuova chiamata "Components" e trasforma in componenti i pezzi della pagina "Home" che si ripetono o che servirebbero in un'altra pagina, usando gli strumenti Figma.
>
> Sei componenti, con questi nomi. button, con le varianti che trovi nella pagina. card / product / default. nav / default / default. feature / cell / default. band / quote / default. footer / default / default. Ogni componente conserva variabili, stili di testo, nomi dei layer e auto layout che ha già. Nella pagina "Home" sostituisci ogni pezzo con un'istanza del suo componente. Le tre feature diventano tre istanze dello stesso componente, con i testi cambiati.
>
> La pagina "Home" deve restare identica a prima a guardarla. Non spiegarmi come farlo, eseguilo. Alla fine dimmi quali componenti hai creato, quante istanze hai messo in "Home" e quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Cosa guardare. Il pannello Layers di Home, con i rombi viola delle istanze. Tre feature, un componente solo. I nomi dei componenti sono quelli del prompt, non quelli che il lettore aveva scelto al D2. Nel sistema vive una convenzione sola.

## Terzo tempo. Il lettore usa il file

Da qui in poi a Claude non si dice più nessun colore, nessuno spazio, nessuno stile. Solo "quelli che ci sono".

### D5 La styleguide, letta dal design system

> Nello stesso file crea una pagina nuova chiamata "Styleguide" e costruiscila usando gli strumenti Figma.
>
> Dentro un frame 1440 con auto layout, quattro sezioni in colonna, una sotto l'altra. Prima sezione, tutte le variabili colore del file, ogni variabile con un campione quadrato e sotto il suo nome. Seconda sezione, le variabili spazio, ogni variabile con una barra alta quanto il suo valore e sotto il nome. Terza sezione, gli stili di testo, ogni stile con una riga di esempio nello stile stesso e sotto il nome. Quarta sezione, un'istanza di ogni componente della pagina "Components", con sotto il nome del componente.
>
> Usa solo variabili, stili e componenti che esistono già nel file. Nessun colore, spazio o carattere scritto a mano. Non toccare le altre pagine.
>
> Non spiegarmi come farlo, eseguilo. Alla fine dimmi quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Cosa guardare. Se nella pagina c'è qualcosa scritto a mano. E se c'è, se il lettore lo ha dichiarato.

### D6 Una pagina nuova, coerente

Nella stessa chat, senza URL. Il file è quello del D1.

> Nello stesso file crea una pagina nuova chiamata "Product" con la pagina di dettaglio del prodotto che sta nella card della pagina "Home", usando gli strumenti Figma.
>
> Un frame 1440 in auto layout. Nav in alto, poi immagine grande a sinistra e a destra titolo, descrizione, prezzo e bottone "Aggiungi", poi una sezione di tre feature, poi il footer. Usa solo i componenti della pagina "Components", le variabili e gli stili di testo del file. Nessun colore, spazio, carattere o forma che non esista già nel file. Se ti serve qualcosa che non c'è, non inventarla, dimmelo.
>
> Non spiegarmi come farlo, eseguilo. Alla fine dimmi quali componenti hai usato e quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Cosa guardare. Quali componenti ha usato, e soprattutto cosa dice che manca. Con un file che si lascia leggere, il lettore sa anche cosa non c'è.

### D7 Lo stesso prompt, sul file caotico

Chat nuova, quindi l'URL va scritto. Il file è la copia intatta. Il prompt è il D6, cambia solo l'attacco, "Nel file [URL]" al posto di "Nello stesso file".

> Nel file [URL della copia intatta] crea una pagina nuova chiamata "Product" con la pagina di dettaglio del prodotto che sta nella card della pagina "Home", usando gli strumenti Figma.
>
> Un frame 1440 in auto layout. Nav in alto, poi immagine grande a sinistra e a destra titolo, descrizione, prezzo e bottone "Aggiungi", poi una sezione di tre feature, poi il footer. Usa solo i componenti della pagina "Components", le variabili e gli stili di testo del file. Nessun colore, spazio, carattere o forma che non esista già nel file. Se ti serve qualcosa che non c'è, non inventarla, dimmelo.
>
> Non spiegarmi come farlo, eseguilo. Alla fine dimmi quali componenti hai usato e quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Due esiti, tutti e due buoni. Se inventa, è il lettore che perdona, e perdonando inventa. Se si ferma, con Rectangle 47 anche il lettore migliore si ferma, e non è colpa sua. Confrontate la risposta con quella del D6. Stesso prompt, stesso lettore. La differenza è il file.

## Modifiche

- 2026-09-18, chat 02.7 WS, versione 05. Il file caotico è pubblicato su Figma Community come `landing-community`, con il link in "Come si usano". Aggiunto in apertura il limite delle tre pagine per file del piano Starter, per cui la demo richiede un piano Education o a pagamento.
- 2026-09-18, chat 02.6 WS, versione 04. Il file diventa la pagina per i partecipanti, da tenere dopo il workshop. Tolti i nomi dei file di Italo, la sezione dei file, la tabella dei tempi, la rete, l'incognito e le note di regia, che stanno nello script 04 e nel brief 04. Aggiunti "Come si usano" e una riga "Cosa guardare" sotto ogni prompt. Segnaposto degli URL rinominati in copia di lavoro e copia intatta. Esito del D7 senza il racconto della prova, che si aggiunge dopo il 20.
- 2026-09-18, chat 02.6 WS, versione 03. Dalla prova cronometrata. Tabella dei tempi compilata, 11:11 e 15 chiamate, demo nuova confermata. Aggiunto `landing-raw` per il D7, `landing-start` resta matrice e non ci gira nessun prompt. Chat in incognito sul web. Note "da dire" con le scene della prova. Esito del D7 aggiornato. Tolta la riserva R, S, D, al suo posto la rete. Sezione dei file divisa tra fissi e copie usa e getta.
- 2026-09-17, chat 02.6 WS, versione 02. URL solo nel primo prompt di ogni chat, senza eccezioni. Il D6 dice "nello stesso file", il D7 è scritto per esteso con il suo URL. Nomi dei file allineati al brief 03, `landing-work` al posto di `landing-demo`, `landing-start` al posto di `landing-c`, riserva su una copia di `rectangle47-end` al posto di `landing-b`.
- 2026-09-17, chat 02.5 WS, versione 01. Dal giro con Antonia. La demo parte dai prompt dei partecipanti sulla landing intera e cresce da lì. Sette prompt da D1 a D7 al posto di R, S, D. Stili di testo e non variabili tipografiche. Un prompt per i componenti. Nomi di variabili, stili e componenti presi dal file `Rectangle47`. Tempi da misurare il 18.

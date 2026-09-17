# Rectangle 47. Il metodo

Workshop "Rectangle 47. Scrivere per un lettore che non perdona"
PUG Bari, 20 settembre 2026. Italo Sannino, italosannino.com

Tre mosse. Decidi le variabili, dai i nomi, fai leggere.
I prompt sono lo strumento, le scelte sono vostre.

Un design system ha quattro cardini, variables, naming, components, auto layout. In aula se ne fanno due con le mani, variabili e nomi. Gli altri due si vedono nella demo, sul file intero. Il metodo è lo stesso per tutti e quattro, decidere una volta e scrivere la decisione nel file.

## Come si usano

- L'URL del file va solo nel primo prompt di ogni chat. È l'indirizzo della tua copia, quello che leggi nella barra del browser con il file aperto in Drafts, dopo Open in Figma.
- I prompt da 0.3 a 3A vanno nella stessa chat. Il 3B in una chat nuova, e lì l'URL va rimesso. Se per qualunque motivo apri una chat nuova, rimetti l'URL nel primo prompt.
- Ogni prompt indica la pagina su cui lavorare. La pagina "Controllo" non si tocca fino all'esercizio 3.
- L'ultima riga di ogni prompt resta sempre. Sul piano gratuito di Figma il connettore ha venti chiamate al mese, tutte le chiamate contano, e quella riga tiene Claude sugli strumenti che ne consumano meno. Il giro del workshop ne usa tra sei e nove. Usa un account Figma nuovo o mai collegato a Claude prima.
- Se Claude risponde che non ha accesso in modifica al file, l'URL è quello sbagliato. Prendilo dalla barra del file aperto in Drafts, non dalla pagina Community.
- Ogni prompt è scritto a blocchi. Il file e il compito, cosa creare, cosa non toccare, le istruzioni finali, la riga sugli strumenti.

## Punto zero

### 0.3 Verifica dell'account

> Con quale account Figma sei collegato? Dimmi nome e email usando lo strumento whoami.

Deve rispondere con il tuo nome e la tua email di Figma. Se risponde con un altro nome, il connettore è collegato all'account sbagliato.

### 0.5 Prova di lettura

> Nella pagina "Rectangle 47" del file [URL] elenca tutti i layer con il loro nome.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Se risponde con Group 12, Rectangle 47, Frame 3 copy 2 ed Ellipse 1, il collegamento funziona e il file è quello giusto. È anche la prima volta che vedi il file con gli occhi del lettore. Quattro nomi, nessuno dice cosa è.

## Prima mossa. Decidi le variabili

Un design system si costruisce in due modi. Con calma, scegliendo ogni colore, spazio e carattere a mano. O in fretta, dando a Claude un brief e raffinando dopo. In aula si fa la seconda. Il brief è vostro, tre parole di tono e un vincolo, sul foglio, prima del prompt.

I cinque nomi sono dati. Nessuno dice un colore, tutti dicono un ruolo. Il rosso può diventare blu domani e il nome resta giusto. La barra fa gruppo nel pannello.

### 1 Variabili, con il brief

> Nello stesso file crea tu, usando gli strumenti Figma, una collezione di variabili chiamata "color" con una sola modalità.
>
> Dentro metti cinque variabili colore con questi nomi. surface/primary, surface/secondary, text/primary, text/secondary, accent. I valori li scegli tu seguendo questo brief. [BRIEF, per esempio "neutro caldo, accento rosso, contrasto alto"]. Rispetta il contrasto minimo tra testo e sfondo.
>
> Poi lega i fill dei layer della pagina "Rectangle 47" alle variabili che hai creato, in base al ruolo di ogni layer. Non toccare la pagina "Controllo".
>
> Non spiegarmi come farlo a mano, eseguilo in una sola chiamata. Alla fine dimmi quali variabili hai creato con i loro valori e quanti fill hai legato.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

### 1 Variabili, con i valori scelti a mano

La strada lunga, per quando c'è tempo. Stesso prompt, con il secondo blocco così.

> Dentro metti cinque variabili colore con questi nomi e questi valori. surface/primary [valore], surface/secondary [valore], text/primary [valore], text/secondary [valore], accent [valore].

Tre controlli. Pannello Local variables, collezione color con cinque nomi. Fill del rettangolo grande della card, un nome al posto del numero. Pagina Controllo, rimasta com'era.

## Seconda mossa. Dai i nomi

La convenzione è componente / variante / stato, in inglese come le variabili. Per esempio "card / product / default", "button / primary / default", "feature / cell". Se non c'è uno stato, non si inventa. Non è l'unica convenzione al mondo, è una, ed è coerente. Coerente conta più di giusta.

Un testo che si chiama come quello che c'è scritto non ha un nome. Prima di lanciare il prompt scrivete sul foglio il nome che dareste a Group 12, Rectangle 47, Rectangle 3, Frame 3 copy 2 ed Ellipse 1. Non serve che siano giusti, serve che siano vostri.

### 2 Nomi

> Nello stesso file, nella pagina "Rectangle 47", rinomina tutti i layer che hanno ancora un nome di default, tipo Rectangle, Frame, Text, Ellipse, Group, compresi i layer di testo il cui nome coincide con il contenuto, che vanno chiamati per ruolo, per esempio title, description, price, label.
>
> Segui la convenzione "componente / variante / stato", con i nomi in inglese come le variabili, deducendo il ruolo di ogni layer dalla sua posizione, dimensione e contenuto. Dove non riesci a dedurlo, lascia il nome com'è e dimmelo. Non toccare la pagina "Controllo".
>
> Esegui direttamente con gli strumenti Figma, in una sola chiamata. Alla fine elenca i layer rinominati con vecchio e nuovo nome.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Confrontate il foglio con la tabella di Claude, un layer alla volta. Guardate cosa ha fatto con Ellipse 1. Nel dry run le ha dato un ruolo con sicurezza, "decoration / circle / default", per una cosa che un ruolo non ce l'ha. Il lettore che non perdona non si ferma, se il file non dice cosa è una cosa se lo inventa. Se la variante del bottone è la parola scritta sopra, per esempio "add", correggetela a mano in "primary". La variante è cosa fa nel sistema, non cosa c'è scritto.

## Terza mossa. Fai leggere

Stesso prompt, due pagine, due chat. Una sistemata, una no. Due chat perché il lettore non deve ricordare.

### 3A La prova del lettore, pagina sistemata

Nella stessa chat di lavoro.

> Nello stesso file, nella pagina "Rectangle 47", scrivi l'HTML e il CSS della card prodotto. Usa i nomi dei layer come nomi delle classi e le variabili del file come custom property CSS. Non aggiungere nulla che non sia nel file.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

### 3B La prova del lettore, pagina di controllo

In una chat nuova, con l'URL.

> Nella pagina "Controllo" del file [URL] scrivi l'HTML e il CSS della card prodotto. Usa i nomi dei layer come nomi delle classi e le variabili del file come custom property CSS. Non aggiungere nulla che non sia nel file.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Confrontate i due codici. Non serve leggerli, servono le parole.

- Le classi. Nel 3A card, button, price. Nel 3B group-12, rectangle-47, frame-3-copy-2.
- I colori. Nel 3A var(--accent). Nel 3B un numero esadecimale, ripetuto ogni volta che serve.
- Il lavoro dopo. Con il 3A un colore si cambia in un posto solo. Con il 3B si cerca in nove.

Il secondo codice non è sbagliato. È fedele. Ha copiato esattamente quello che c'era, e quello che c'era non diceva niente.

## La quarta mossa, per casa

L'auto layout. Un file senza auto layout dice dove sta una cosa, non come sta rispetto alle altre, e il lettore copia le coordinate. In aula non c'è tempo. Nella chat di lavoro, dopo il 3A.

### 4 Struttura

> Nello stesso file, nella pagina "Rectangle 47", metti in auto layout la card prodotto e i suoi contenitori.
>
> La card è un frame in colonna. Dentro, l'immagine, il titolo, la descrizione, la riga del prezzo e il bottone, nell'ordine in cui stanno a schermo. Il bottone entra dentro la card, in basso. Spazi e padding li deduci dalle distanze attuali e li arrotondi alla scala 8, 16, 24, 32. La card deve restare identica a prima a guardarla.
>
> Esegui direttamente con gli strumenti Figma, in una sola chiamata. Alla fine dimmi quali frame hai messo in auto layout e con quali spazi.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

## Cosa ha fatto Italo

La demo in aula, tre atti sulla landing intera, stesso metodo della card. Questi prompt richiedono un file con un design system già fatto, come quello della landing, github.com/italosan/rectangle-47. Vanno lanciati con l'URL del file, in una chat nuova. Tempi misurati nel dry run del 17 settembre con Fable.

### R Il file caotico riportato a code-ready

Variabili, nomi e auto layout sulla copia caotica della landing. Due minuti e mezzo.

> Nel file [URL] duplica la pagina "Chaos" in una pagina nuova chiamata "Rework" e sistemala usando gli strumenti Figma, senza toccare le altre pagine.
>
> Tre cose. Lega ogni fill e ogni filetto alle variabili colore del file e applica a ogni testo lo stile di testo corrispondente, scegliendo in base a ruolo, corpo e peso. Rinomina ogni layer con nome di default seguendo la convenzione "componente / variante / stato", in inglese, con i nomi già usati nella pagina "Home" dove il ruolo è lo stesso. Metti in auto layout i contenitori che hanno figli in relazione tra loro, con spazi e padding legati alle variabili spazio del file.
>
> Il risultato deve restare identico a "Home" pixel per pixel. Non spiegarmi come farlo, eseguilo. Alla fine dimmi quanti fill hai legato, quanti stili applicato, quanti layer rinominato, quanti frame messi in auto layout e quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

### S La styleguide, letta dal design system

Nessun colore, spazio o stile detto a Claude, solo "quelli che ci sono". Un minuto e mezzo, cinque chiamate.

> Nel file [URL] crea una pagina nuova chiamata "Styleguide" e costruiscila usando gli strumenti Figma.
>
> Dentro un frame 1440 con auto layout, quattro sezioni in colonna, una sotto l'altra. Prima sezione, tutte le variabili colore del file, ogni variabile con un campione quadrato e sotto il suo nome. Seconda sezione, le variabili spazio, ogni variabile con una barra alta quanto il suo valore e sotto il nome. Terza sezione, gli stili di testo, ogni stile con una riga di esempio nello stile stesso e sotto il nome. Quarta sezione, un'istanza di ogni componente della pagina "Components", con sotto il nome del componente.
>
> Usa solo variabili, stili e componenti che esistono già nel file. Nessun colore, spazio o carattere scritto a mano. Non toccare le altre pagine.
>
> Non spiegarmi come farlo, eseguilo. Alla fine dimmi quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

### D Una pagina nuova, coerente

Lo stesso prompt lanciato due volte, su due file. Sul file sano produce una pagina coerente in un minuto e dice cosa manca, nel dry run un componente immagine. Sul file caotico si ferma senza scrivere nulla, perché non trova componenti, variabili né stili, e qualsiasi pagina sarebbe fatta di valori copiati. Cambia solo il file.

> Nel file [URL] crea una pagina nuova chiamata "Product" con la pagina di dettaglio del prodotto che sta nella card della pagina "Home", usando gli strumenti Figma.
>
> Un frame 1440 in auto layout. Nav in alto, poi immagine grande a sinistra e a destra titolo, descrizione, prezzo e bottone "Aggiungi", poi una sezione di tre feature, poi il footer. Usa solo i componenti della pagina "Components", le variabili e gli stili di testo del file. Nessun colore, spazio, carattere o forma che non esista già nel file. Se ti serve qualcosa che non c'è, non inventarla, dimmelo.
>
> Non spiegarmi come farlo, eseguilo. Alla fine dimmi quali componenti hai usato e quante chiamate hai fatto.
>
> Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

## Modifiche

- 2026-09-17, chat 02.4 WS, versione 02. Dal dry run. 0.3 con whoami. URL solo nel primo prompt di ogni chat. Nota sull'errore di accesso in modifica. Prompt 1 con il brief, la versione a mano come strada lunga. Nomi in inglese e layer di testo nel prompt 2. Prompt a blocchi con la riga sugli strumenti come suffisso. Tetto Starter di venti chiamate al mese che conta anche use_figma, prompt stretti a una chiamata. Aggiunte la quarta mossa per casa e la sezione con i prompt della demo R, S, D. Quattro cardini in apertura.
- 2026-09-16, chat 02.3 WS, versione 01. Prima versione, prompt 0.3, 0.5, 1, 2, 3A, 3B.

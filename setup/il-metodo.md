# Rectangle 47. Il metodo

Workshop "Rectangle 47. Scrivere per un lettore che non perdona"
PUG Bari, 20 settembre 2026. Italo Sannino, italosannino.com

Tre mosse. Decidi le variabili, dai i nomi, fai leggere.
I prompt sono lo strumento, le scelte sono vostre.

## Come si usano

- Sostituisci [URL] con l'indirizzo della tua copia del file, quello che leggi nella barra del browser dopo Open in Figma.
- Ogni prompt indica la pagina su cui lavorare, mai solo il file. La pagina "Controllo" non si tocca fino all'esercizio 3.
- L'ultima riga di ogni prompt resta sempre. Alcuni strumenti di lettura di Figma hanno un limite mensile sui piani gratuiti, e quella riga li evita. Non serve capirla, serve lasciarla.
- Ogni prompt va incollato in una chat su claude.ai con il connettore Figma attivo. I prompt da 0.3 a 3A vanno nella stessa chat. Il 3B in una chat nuova.

## Punto zero

### 0.3 Verifica dell'account

> Con quale account Figma sei collegato?

### 0.5 Prova di lettura

> Nella pagina "Rectangle 47" del file [URL] elenca tutti i layer con il loro nome. Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

## Prima mossa. Decidi le variabili

### 1 Variabili

I cinque nomi sono dati. I valori li scegliete voi, prima di lanciare il prompt. Una palette neutra e un accento.

> Nel file [URL] crea tu, usando gli strumenti Figma, una collezione di variabili chiamata "color" con una sola modalità. Dentro metti cinque variabili colore con questi nomi e questi valori. surface/primary [valore], surface/secondary [valore], text/primary [valore], text/secondary [valore], accent [valore]. Poi lega i fill dei layer della pagina "Rectangle 47" alle variabili che hai creato, in base al ruolo di ogni layer. Non toccare la pagina "Controllo". Non spiegarmi come farlo a mano, eseguilo. Alla fine dimmi quali variabili hai creato e quanti fill hai legato. Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Se preferite lasciare i valori a Claude, sostituite l'elenco con "con valori a tua scelta in una palette neutra".

## Seconda mossa. Dai i nomi

### 2 Nomi

La convenzione è componente / variante / stato. Per esempio "card / product / default", "button / primary / default". Prima di lanciare il prompt scrivete su un foglio i vostri cinque nomi, così potete confrontarli con quelli di Claude.

> Nella pagina "Rectangle 47" del file [URL] rinomina tutti i layer che hanno ancora un nome di default, tipo Rectangle, Frame, Text, Ellipse, seguendo la convenzione "componente / variante / stato", deducendo il ruolo di ogni layer dalla sua posizione, dimensione e contenuto. Dove non riesci a dedurlo con sicurezza, lascia il nome com'è e dimmi perché. Non toccare la pagina "Controllo". Esegui direttamente con gli strumenti Figma. Alla fine elenca i layer rinominati con vecchio e nuovo nome. Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

## Terza mossa. Fai leggere

### 3A La prova del lettore, pagina sistemata

Nella stessa chat di lavoro.

> Nella pagina "Rectangle 47" del file [URL] scrivi l'HTML e il CSS della card prodotto. Usa i nomi dei layer come nomi delle classi e le variabili del file come custom property CSS. Non aggiungere nulla che non sia nel file. Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

### 3B La prova del lettore, pagina di controllo

In una chat nuova, perché nella prima Claude ha già in memoria i nomi che ha appena dato.

> Nella pagina "Controllo" del file [URL] scrivi l'HTML e il CSS della card prodotto. Usa i nomi dei layer come nomi delle classi e le variabili del file come custom property CSS. Non aggiungere nulla che non sia nel file. Leggi il file usando solo use_figma. Non usare get_design_context, get_metadata, get_screenshot o get_variable_defs.

Confrontate i due codici. Guardate i nomi delle classi, i colori, la struttura.

## Dopo il workshop

Il metodo vale su qualunque file, con qualunque lettore. Le tre mosse restano le stesse, cambiano solo i nomi che scegliete.

La skill "recap", che chiude una chat con un documento di passaggio, è su github.com/italosan/claude-skills. Si installa da claude.ai, Customize > Skills > Add.

# Design

<!-- impeccable:design-schema 1 -->

## World

Luxury contemporaneo — avorio luminoso, inchiostro carbone, un solo oro champagne come firma. Terza iterazione in questa sessione: la prima ("L'Atto", inchiostro verde-bosco + ceralacca rossa) è stata respinta dall'utente come "orribile" e "non luxury". Qui si corregge rotta verso un linguaggio da resort di lusso contemporaneo (Aman, Belmond, Rosewood): meno decorazione, più spazio e fiducia nella fotografia e nella tipografia grande.

## Palette

Strategia: Committed — un solo colore oltre al bianco/nero fa tutto il lavoro (CTA, hover, filo decorativo, label). Niente rosso, niente verde scuro, niente secondo accento a competere.

```
--bg:       #FAF6EC   avorio luminoso
--bg-warm:  #F1E8D2
--dark:     #1A1816   inchiostro carbone (neutro, non più verdastro)
--body-txt: #221E18
--muted:    #6B6358

--gold:     #C9983D   oro champagne — l'unica firma: CTA, hover, filo, label
--gold-lt:  #E7C780   variante chiara su fondo scuro
```

`--wax`/`--wax-lt` restano come alias dello stesso oro (retrocompatibilità con il CSS esistente): non esiste più un secondo colore interattivo.

Regola: i pulsanti pieni in oro usano testo **scuro** (`var(--dark)`), mai bianco — l'oro è troppo chiaro per il bianco sopra, e il contrasto scuro-su-oro è la combinazione classica dell'hotellerie di lusso.

## Type

- Display: **Bodoni Moda**, peso 500 (non più corsivo di default — il corsivo ovunque leggeva come invito/cerimonia, non come resort). Dimensioni aumentate rispetto alle iterazioni precedenti per maggiore sicurezza.
- UI/label: Josefin Sans, invariato.

## Componenti chiave

- **Nav globale**: tornata chiara/vetro (avorio traslucido con blur), non più scura — una barra scura su tutte le pagine leggeva pesante. Logo e icone in inchiostro scuro, CTA Virtual Tour piena in oro con testo scuro.
- **Hub tiles**: tolta la cornice a filo e il pallino ceralacca (troppo decorativi/affollati). Ora: titolo grande e sicuro, una sottile riga oro sotto l'etichetta che si espande da 2.5rem a tutta larghezza sull'hover — un solo gesto, non tre.
- **Footer**: resta scuro (era già così, nessuna modifica necessaria) — il contrasto chiaro-sopra/scuro-sotto è la struttura portante del sito.

## Known pre-existing / not yet touched

- Kicker "Il racconto del giorno" nelle sotto-pagine dinamiche della galleria (generato da JS), stesso pattern mai rimosso in nessuna delle tre iterazioni.
- Non tutte le 18 pagine sono state ispezionate singolarmente a schermo; la maggior parte eredita il sistema dai token CSS condivisi.

## Build path

Code-led: nessuna immagine sintetica generata, lavoro diretto su palette/tipografia/componenti con la fotografia reale del sito.

# Design

<!-- impeccable:design-schema 1 -->

## World

Travertino evoluto — evoluzione disciplinata della direzione esistente (ispirata a Borgo Egnazia), non una rottura totale. Riferimenti di qualità vincolanti: Borgo Egnazia e Aman Resorts (minimalismo caldo, fotografia di grande formato, pochissimo testo per schermata). Decisione presa con l'utente dopo un giro di direzioni alternative più radicali (vedi `.impeccable/surfaces/esplora-html.md`), poi raffinata una seconda volta su richiesta esplicita di un cambio cromatico più visibile.

## Palette

Strategia: Restrained (neutri caldi) + un solo accento Committed (terracotta), non più oro/senape.

```
--bg:         #ECE4D4   travertino chiaro, ground principale
--bg-warm:    #DCD0B4   variante più calda per fasce/section alternate
--dark:       #1B1713   ink quasi nero, testo su chiaro e sfondo scuro (nav/footer scuri, menu mobile)
--body-txt:   #241C15
--muted:      #6B5F4E
--gold / --terracotta: #9C4E2B   UNICO accento funzionale — CTA, hover, bottone Virtual Tour, label su sfondo chiaro
--gold-lt:    #D98B5F   variante chiara dello stesso accento — SOLO per testo/label su sfondi scuri (nav-vt on-dark, footer h4, "Menu" del menu mobile), mai su sfondo chiaro
```

Regola pratica, da rispettare nelle prossime pagine: `--gold` (scuro, satura) su fondo chiaro; `--gold-lt` (chiaro) su fondo scuro. Non più oro-senape (#A88A4E) né i temi colore per-pagina `theme-plum`/`theme-emerald` definiti in style.css (risultano non utilizzati in nessuna pagina: palette unica su tutto il sito).

## Type

- Display/titoli: Cormorant Garamond (invariato — non è nella lista di default vietata, confermato dal brief del sito).
- UI/label: Josefin Sans (invariato).
- Niente kicker/eyebrow numerati ("01 —", "02 —" ecc.) sopra i titoli delle card: rimossi da esplora.html. **Nota per le prossime pagine:** la home (`index.html`) ha ancora un eyebrow "MATRIMONI ED EVENTI · MESSINA, SICILIA" sopra il titolo hero — stesso pattern, non ancora rimosso, da trattare nel prossimo giro.

## Hub tile component (esplora.html)

Contenuto allineato in basso a sinistra (non più centrato), overlay fotografico sfumato solo nel terzo inferiore (prima: scrim uniforme su tutta la tile), titolo più piccolo e con peso normale (prima: uppercase enorme), sottotitolo in sans minuscolo. Hover: zoom leggero della foto + una linea di 2.5rem che si estende da sinistra (prima: linea centrata).

## Known pre-existing issues (not introduced by this pass)

- Testo del footer sotto gli 11px e un'etichetta con colore invisibile sull'hover del menu mobile: **corretti** su tutte le pagine (fix nel CSS condiviso).
- Alcuni effetti "glow" decorativi (ombre sfocate colorate, aloni radiali) restano in sezioni non ancora toccate (es. `eventi.html`, `galleria.html` righe ~2150-2260 di style.css) — pattern che lo stesso Impeccable segnala come "AI slop" da evitare in futuro.
- L'eyebrow/kicker sopra il titolo in `index.html` va rimosso nel prossimo giro per coerenza con la regola applicata a esplora.html.

## Build path

Code-led: nessuna immagine sintetica generata, si lavora sulla fotografia reale già presente nel sito.

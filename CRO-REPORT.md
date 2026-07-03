# CRO Audit — Landing Page MOOVELAND

**Data:** 2026-07-03 · **File analizzato:** `mooveland-landing.html` (single-file, ~1.7MB) · **Destinazione:** Shopify Basic
**Metodo:** lettura completa del markup + screenshot full-page 1440px + benchmark best practice 2025 (Shopify, Unbounce, NNGroup, teardown categoria topical pain relief: Voltaren/Biofreeze/Penetrex) + linee guida su scarcity etica (FTC dark patterns).

**Vincoli rispettati in tutte le raccomandazioni:** prodotti COSMETICI (no claim terapeutici), prezzi/nomi/colori brand invariati, recensioni Amazon vere da inserire dopo (solo placeholder `DA-SOSTITUIRE`).

---

## 1. Punteggio per sezione (0–10)

| Sezione | Voto | Sintesi |
|---|---|---|
| Urgency bar + Header | 7 | Buona: value prop + spedizione gratis sopra 39€ + CTA "Acquista Ora". Manca soglia spiegata vicino ai prezzi. |
| Hero | 7,5 | Headline outcome-driven forte, sub con authority del fondatore, doppia CTA, 3 trust item. Manca social proof (stelle/recensioni) e prezzo/offerta above the fold. |
| Manifesto fondatore | 8 | Storytelling autentico, ottimo per la categoria. Foto fondatore ancora placeholder `[Foto del Fondatore]` e `credential-tags` vuoto. |
| Benefits (4 icone) | 7 | Chiaro, scansionabile. "Dual-Use Pro" è gergo poco comprensibile. |
| Schede prodotto | 7 | Feature list ottime, ingredienti visibili, prezzo chiaro. Mancano: recensioni, garanzia, badge pagamento, quantità/selettore, info spedizione. `product-card__badges` vuoto. Scarcity generica ("scorte in esaurimento") = rischio dark pattern. |
| Bundle | 8 | Ancoraggio 59€→44,99€ ben fatto, -29%, razionale d'uso h24 credibile. Manca "il più scelto" con dato reale e garanzia accanto alla CTA. |
| Modalità d'uso | 8 | Step numerati eccellenti — differenziante vs competitor. Andrebbe PRIMA del bundle o subito dopo i prodotti singoli. |
| Social proof / Recensioni | 0 | **Sezione assente del tutto.** È il gap n.1 della pagina. |
| FAQ | 7 | 5 domande buone, accordion accessibile. Mancano FAQ transazionali (spedizione, resi, pagamenti, tempi). |
| Footer | 5 | Link tutti `href="#"` (placeholder), nessun badge pagamento, nessun contatto reale. Disclaimer cosmetico presente: ottimo. |
| Mobile / CTA persistente | 3 | Nessuna sticky CTA mobile; su una pagina lunga è una perdita diretta di conversioni. |
| Compliance claim | 4 | Vedi P1-6: diversi claim borderline farmaceutici. |

**Voto complessivo: 6/10** — ottima base di design e copy, ma mancano i "conversion layer": prova sociale, riduzione del rischio (garanzia/resi), trust di pagamento e CTA persistente.

---

## 2. Elementi MANCANTI ad alto impatto

1. **Recensioni / social proof** — zero recensioni, zero rating, zero contatori. Per health/wellness è l'elemento con il maggiore impatto sulla conversione.
2. **Garanzia soddisfatti o rimborsati** — nessuna menzione. Riduzione del rischio assente su un acquisto "scettico" (28–45€ per un cosmetico mai provato).
3. **Trust badge pagamento** (Visa, Mastercard, PayPal, Shop Pay, lucchetto SSL) — assenti ovunque.
4. **Info spedizione/resi vicino alla CTA** — la spedizione gratis >39€ è solo nella barra in alto; ai prezzi 28€ e 31€ il cliente non sa quanto pagherà di spedizione (causa n.1 di abbandono carrello).
5. **Sticky CTA mobile** — assente.
6. **Sezione "Come funziona" pre-acquisto in 3 step** (Ordini → Ricevi in 24/48h → Applichi con il protocollo) — assente.
7. **Sezione recensioni con foto reali d'uso / prima-dopo lifestyle** — assente (placeholder da prevedere).
8. **Urgenza etica verificabile** — quella attuale ("scorte in esaurimento") è generica e non verificabile: da sostituire, non da amplificare.
9. **FAQ transazionali** (tempi di consegna, corriere, resi, pagamenti accettati).
10. **Numeri concreti di authority** (anni di pratica, n. pazienti/sessioni — solo se veri, forniti dal cliente).

---

## 3. Ordine ottimale delle sezioni (funnel)

Attuale: Urgency bar → Hero → Manifesto → Benefits → Prodotti+Bundle → Modalità d'uso → FAQ → Footer.

**Ordine raccomandato:**

1. Urgency bar (invariata)
2. **Hero** + micro social proof (stelle + "N recensioni verificate su Amazon" — placeholder)
3. **Benefits** (spostare PRIMA del manifesto: il visitatore freddo vuole prima "cosa ci guadagno", poi "chi sei")
4. **Manifesto fondatore** (authority)
5. **Prodotti singoli**
6. **Modalità d'uso** (subito dopo i prodotti: risolve l'obiezione "come si usa" prima dell'upsell)
7. **Bundle** (dopo che il valore dei singoli è chiaro, l'ancoraggio 59€→44,99€ rende meglio)
8. **NUOVA: Recensioni** (placeholder DA-SOSTITUIRE)
9. **NUOVA: Garanzia + Come funziona l'ordine (3 step) + trust badge**
10. FAQ (ampliata)
11. CTA finale di richiamo ("Pronto a ritrovare il tuo movimento?") + link al bundle
12. Footer completo

---

## 4. Modifiche prioritizzate

### P1 — Critiche (bloccanti per il lancio)

**P1-1 · Sezione Recensioni (nuova, tra Bundle e FAQ)** — *sviluppatore + copywriter*
- Struttura: titolo "Cosa dicono i nostri clienti" + rating aggregato + griglia 3–6 card recensione (stelle, nome, badge "Acquisto verificato su Amazon", testo, prodotto acquistato).
- Ogni campo con contenuto marcato **`[DA-SOSTITUIRE: recensione Amazon reale #n]`** — NON inventare recensioni (violazione fiducia + normativa Omnibus UE: indicare come vengono verificate).
- Aggiungere una riga di micro-proof nell'hero sotto i trust item: `★★★★★ [DA-SOSTITUIRE: media reale] su Amazon — [DA-SOSTITUIRE: n] recensioni verificate`.

**P1-2 · Garanzia soddisfatti o rimborsati** — *copywriter + cliente (decisione policy)*
- Blocco garanzia (icona scudo, "Garanzia 30 giorni: se non sei soddisfatto ti rimborsiamo") ripetuto: (a) sotto ogni bottone "Aggiungi al Carrello" nelle 3 card prodotto, (b) sezione dedicata prima delle FAQ.
- ATTENZIONE: la durata/condizioni vanno confermate dal cliente prima della pubblicazione. Placeholder: `[DA-CONFERMARE: termini garanzia]`.

**P1-3 · Trust badge pagamento + spedizione vicino alla CTA** — *sviluppatore Shopify*
- Sotto ogni bottone carrello: riga con icone Visa/Mastercard/PayPal/Shop Pay/Amex + lucchetto "Pagamento sicuro SSL" (su Shopify usare le payment icons native del checkout).
- Accanto a ogni prezzo: micro-copy spedizione. Es. Argilla 28€: "Aggiungi l'Arnica: spedizione gratuita sopra 39€" (spinge al bundle); Bundle 44,99€: "✓ Spedizione gratuita inclusa".

**P1-4 · Sticky CTA mobile** — *sviluppatore Shopify*
- Barra fissa bottom su viewport <768px, visibile dopo lo scroll oltre l'hero: "Bundle Completo — 44,99€ <s>59€</s>" + bottone "Acquista". Ancora a `#prodotti` (o add-to-cart diretto del bundle su Shopify).
- Z-index sopra tutto, altezza ~60px, rispettare `env(safe-area-inset-bottom)`.

**P1-5 · Collegare le CTA a Shopify** — *sviluppatore Shopify*
- I 3 bottoni "Aggiungi al Carrello" sono `<button>` senza azione e i link footer sono `href="#"`. In migrazione: form add-to-cart Shopify (`/cart/add` con variant ID) o Buy Button; footer → pagine reali Privacy/Termini/Spedizioni e Resi/Contatti (obbligatorie anche per legge e per approvazione gateway di pagamento).

**P1-6 · Compliance claim cosmetici (Reg. CE 1223/2009 + Reg. 655/2013)** — *copywriter, revisione legale consigliata*
Diversi testi attuali sono claim terapeutici non ammessi per cosmetici. Da riformulare (senza cambiare tono/energia):
- "Azione Antidolorifica", "analgesica documentata", "antiflogistica, antiedematosa" (card prodotti, righe 822, 854, 860) → sostituire con linguaggio sensoriale/benessere: "effetto lenitivo e defaticante", "sensazione di sollievo e freschezza", "coadiuvante del benessere muscolare e articolare".
- "Indicata per artrosi, tendiniti, contusioni, distorsioni" (r. 832) e la FAQ "artrosi, tendiniti, mal di schiena…" (r. 955) → nominare patologie = claim medico. Riformulare: "ideale per zone affaticate da sport, sforzi e tensioni quotidiane: schiena, cervicale, ginocchia, spalle".
- "Azione antinfiammatoria continuativa h24" (bundle e FAQ, r. 886/951) → "protocollo benessere h24".
- La headline "Ferma il Dolore" è al limite: valutare "Libera il Movimento. Ritrova il Tuo Benessere." o mantenerla consapevoli del rischio (decisione cliente). Il disclaimer footer c'è già ed è corretto: NON toccarlo.

**P1-7 · Scarcity etica** — *copywriter*
- Rimuovere "▲ Disponibilità limitata — ordina subito" e "▲ Bestseller — scorte in esaurimento" (r. 842, 873): non verificabili = dark pattern (rischio fiducia e, in UE, pratica commerciale scorretta).
- Sostituire con urgenza VERA: su Shopify mostrare stock reale solo se <10 ("Ne restano 7"), oppure motivazioni autentiche: "Produzione in piccoli lotti dallo studio" / "Prezzo di lancio online" se corrisponde al vero. Il -29% del bundle è già urgenza legittima: tenerlo.

### P2 — Importanti

**P2-1 · Riordino sezioni** come da §3 (Benefits prima del Manifesto; Modalità d'uso prima del Bundle) — *sviluppatore*. Basso sforzo, sono blocchi `<section>` autonomi.

**P2-2 · Sezione "Come funziona l'ordine" (3 step)** — *designer + copywriter*: Ordini oggi → Spedizione tracciata in 24/48h → Inizi il protocollo h24. Posizione: dopo la garanzia, prima delle FAQ. Stile coerente con le `uso-card` esistenti.

**P2-3 · Completare il blocco fondatore** — *cliente + designer*: sostituire `[Foto del Fondatore]` (r. 754) con foto reale in studio/camice (l'authority visiva è il moltiplicatore del manifesto) e riempire `credential-tags` (r. 759, oggi vuoto) con titoli reali: `[DA-SOSTITUIRE: qualifica, anni di esperienza, albo]`.

**P2-4 · FAQ transazionali** — *copywriter*: aggiungere 4 domande: "Quanto costa e quanto impiega la spedizione?", "Come funzionano i resi/la garanzia?", "Quali pagamenti accettate?", "Posso pagare alla consegna?" (se sì — in Italia il COD alza sensibilmente la conversione; da valutare col cliente).

**P2-5 · Badge sulle card prodotto** — *designer*: i div `product-card__badges` (r. 816, 848) sono vuoti. Inserire: Argilla → "Formato 250ml"/"2-in-1 notte+giorno"; Arnica → "Il più venduto" SOLO se supportato dai dati reali Amazon, altrimenti "Arnica 98%".

**P2-6 · CTA finale pre-footer** — *copywriter + designer*: sezione di chiusura con richiamo emotivo + bottone bundle + riga garanzia/spedizione. Oggi la pagina "muore" dopo le FAQ senza ultima chiamata all'azione.

**P2-7 · Chiarire "Dual-Use Pro"** (r. 798) — *copywriter*: rinominare in "2 Prodotti, 1 Protocollo" o "Giorno + Notte".

### P3 — Nice-to-have

- **P3-1** Video 20–30s del fondatore che applica il prodotto (autoplay muto nell'hero o nel manifesto) — massimo impatto per la categoria.
- **P3-2** Tabella comparativa "Mooveland vs gel da supermercato" (concentrazione, texture, formato, prezzo/ml) — pattern vincente nei teardown di Penetrex/Biofreeze; senza citare marchi competitor per nome.
- **P3-3** Ottimizzazione peso: immagini base64 in un file da 1.7MB penalizzano LCP mobile; su Shopify caricare le immagini nel CDN come asset separati con `loading="lazy"` sotto la piega, WebP.
- **P3-4** Exit-intent / popup email con -10% primo ordine (su Shopify Basic: app tipo Klaviyo/Privy) — solo desktop, non invasivo.
- **P3-5** Rich snippet: schema.org `Product` + `AggregateRating` (dopo l'inserimento recensioni reali) e `FAQPage`.
- **P3-6** Selettore quantità e "acquisto in abbonamento/ricorrente" per pazienti cronici (fase 2).

---

## 5. Cosa NON toccare (già funziona)

- **Headline hero outcome-driven + sub con authority** ("professionista della salute… atleti d'élite") — struttura corretta; solo la revisione compliance di P1-6.
- **Manifesto del fondatore** con citazione in blockquote: storytelling autentico, raro nella categoria, forte differenziatore. Tenere copy e struttura.
- **Architettura ancoraggio prezzi del bundle**: 59€ barrato → 44,99€, -29%, "Risparmio di 14,01€", razionale d'uso giorno/notte. Da manuale.
- **Feature list dei prodotti** con benefici concreti e sensoriali ("non si secca, non si sfarina", "si assorbe in secondi, non unge") — copy eccellente.
- **Sezione Modalità d'uso a step numerati** — riduce l'ansia da "saprò usarlo?", differenziante. Solo riposizionarla (P2-1).
- **Palette e design system** (teal/orange/viola bundle, dark hero): coerente, professionale, gerarchia visiva chiara. Vincolo cliente: colori invariati.
- **Accessibilità già curata** (aria-labelledby, aria-expanded sulle FAQ): mantenerla in ogni nuovo blocco.
- **Disclaimer legale nel footer** ("sono cosmetici… non sono farmaci"): corretto e obbligatorio, non rimuovere.
- **Urgency bar top** con spedizione gratis >39€: messaggio vero e utile (spinge al bundle), tenere.

---

## Fonti principali

- [Shopify — High-Converting Landing Pages](https://www.shopify.com/blog/high-converting-landing-pages)
- [Unbounce — High-converting landing page examples](https://unbounce.com/landing-page-examples/high-converting-landing-pages/)
- [Whizzybly — Healthcare landing pages 2025](https://www.whizzybly.com/post/what-makes-a-high-converting-healthcare-landing-page-in-2025)
- [Branded Agency — 14 elements of high-converting pages](https://www.brandedagency.com/blog/high-converting-landing-pages)
- [Build Grow Scale — Ethical scarcity guide](https://buildgrowscale.com/scarcity-principle-ecommerce-guide)
- [Growthsuite — Ethics of urgency marketing](https://www.growthsuite.net/blog/the-ethics-of-urgency-marketing-drawing-the-line)
- [Flair — Trust badges for e-commerce](https://flaircommerce.com/guides/trust-badges/)
- [Curist — Voltaren vs Biofreeze positioning](https://curistrelief.com/blogs/curist/voltaren-vs-biofreeze-vs-salonpas-vs-blue-emu)
- [Voltaren — product page pattern reference](https://www.voltarengel.com/what-is-voltaren/what-makes-voltaren-different.html)

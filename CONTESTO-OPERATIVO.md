# MOOVELAND — Contesto operativo

Documento di contesto per chiunque debba **realizzare** qualcosa con questa cartella: un
collaboratore, un video editor, un social media manager o un altro assistente AI che non ha
assistito alle conversazioni precedenti. Leggere questo file per primo: spiega di cosa si tratta,
cosa è già pronto, cosa manca e con quali regole si lavora.

Stato aggiornato al **10 novembre 2026**.

---

## 1. Il progetto in una pagina

**MOOVELAND SRLS** è un brand italiano di cosmetici per il benessere muscolare, fondato da
**Leonardo Rocca**, professionista della salute che lavora ogni giorno sui corpi delle persone
in studio. I prodotti nascono da un'esigenza vista in studio — "e a casa, cosa uso?" — e questa
è anche la storia che regge tutta la comunicazione.

| Prodotto | Formato | Prezzo | Colore tema |
|---|---|---|---|
| Argilla Moovelab | 250 ml | 28,00 € | Teal `#00A8CC` |
| Arnica Mooveland (Arnica Montana 98%) | 500 ml | 31,00 € | Arancio `#F0A500` |
| Bundle Giorno+Notte (i due insieme) | — | 44,99 € (anziché 59 €) | Viola `#7C3AED` |

**Condizioni commerciali comunicate ovunque** (devono restare identiche in ogni contenuto):
soddisfatti o rimborsati 30 giorni (un barattolo per prodotto, per ordine) · spedizione tracciata
24-48 h, gratuita sopra 39 € (quindi il bundle viaggia gratis) · valutazione clienti 4,4/5.

**Il metodo che tiene insieme tutto** è il *Protocollo Giorno+Notte*: Arnica di giorno (texture
Active-Dry, si assorbe in secondi, non unge), Argilla di notte (impacco che agisce mentre si
dorme, via con acqua tiepida al mattino). I metodi si condividono, i prodotti no: il protocollo
è il contenuto, il prodotto è la conseguenza.

**Strategia in una frase:** il volto e la credibilità del fondatore sono il motore, i contenuti
video il carburante, Meta Ads l'acceleratore, Amazon la riprova sociale, l'email il
moltiplicatore di margine.

---

## 2. Voce del brand e pubblici

Tono: **professionista che educa, mai urlato, mai finta urgenza.** Il consiglio viene prima del
prodotto; il prodotto rende il gesto piacevole, non risolve un problema.

Quattro regole di scrittura che valgono su ogni piattaforma:
1. Prima il gesto gratuito, poi il prodotto. Nei video il prodotto entra nell'ultimo terzo.
2. Si parla di **zone del corpo e situazioni di vita**, mai di patologie.
3. Si dichiara sempre il conflitto d'interessi: "li ho creati io".
4. Niente superlativi, niente promesse di risultato: la garanzia 30 giorni è il sostituto lecito.

Pubblici, per piattaforma:

| Piattaforma | Pubblico | Registro | Obiettivo |
|---|---|---|---|
| TikTok | 25-40, discovery | colloquiale, "raw", stacco visivo ogni 3-5 sec | notorietà, salvataggi, commenti |
| Instagram Reels | 30-50, più vicino all'acquisto | più curato, CTA esplicita al sito | conversione |
| YouTube Shorts + long | 40-65, ricerca | calmo, educativo, titoli SEO | autorevolezza, iscritti |
| Facebook | 45-65 | storytelling lungo, empatico | fiducia, condivisioni, retargeting |

---

## 3. Vincoli non negoziabili (compliance)

I prodotti sono **cosmetici**: possono dichiarare solo effetti superficiali, sulla pelle,
sensoriali e temporanei. Il riferimento vincolante è `BLACKLIST-CLAIM.md`, da verificare prima
di pubblicare qualsiasi testo nuovo. In sintesi operativa:

- **La parola "dolore" non esiste** nei contenuti Mooveland — nemmeno nel problema iniziale di un
  video in cui poi compare il prodotto. Si usa: indolenzimento, zona affaticata, sensazione di
  rigidità, "si fa sentire".
- **Mai patologie come indicazione d'uso** (cervicalgia, lombalgia, artrosi, tendinite,
  contrattura…). Si nomina la zona ("trapezio", "zona lombare") e la situazione ("dopo 8 ore al
  PC", "dopo la corsa").
- **Mai azione farmacologica**: niente antinfiammatorio, sfiamma, penetra in profondità, agisce
  sul muscolo. Il cosmetico agisce sulla pelle.
- **Ogni numero richiede una prova archiviata** prima della pubblicazione (percentuali, tassi di
  riacquisto, "il più venduto").
- **Mai denigrare i concorrenti**, nemmeno in forma anonima. Si insegna a leggere l'INCI: il
  confronto lo fa il consumatore.
- **Recensioni (Direttiva Omnibus):** citazione testuale e virgolettata, fonte dichiarata ("dal
  nostro sito"), mai "verificata" senza un processo di verifica reale e descritto.
- **Disclaimer obbligatorio sui contenuti pilastro:** «Sono cosmetici: parliamo di benessere della
  pelle e sensazione di sollievo. Per problematiche di salute rivolgiti al tuo medico.»
- **Flag "contenuto AI / sintetico" sempre attivo**: il presentatore dei video è un avatar.
- **Nessun camice, nessuna veste clinica** nei contenuti che presentano i prodotti in vendita:
  abbigliamento professionale sobrio. La qualifica dichiarata è "professionista della salute",
  mai un titolo medico.

Il volto di un professionista sanitario **alza l'asticella**: una frase borderline detta da chi
lavora sui corpi viene valutata come indicazione quasi-sanitaria, e il rischio è doppio —
sanzioni AGCM e procedimenti dell'ordine professionale.

---

## 4. Cosa è pronto e cosa manca

| Area | Stato |
|---|---|
| Landing page (design, CRO, compliance) | ✅ completa — `mooveland-landing.html` |
| Versione Shopify | 🟡 pronta, ma restano da sostituire 3 `VARIANT_ID_*` e 9 URL immagine `PLACEHOLDER` |
| Immagini per Shopify | ✅ in `shopify-assets/` (logo, argilla, arnica, foto fondatore) |
| 62 contenuti social | ✅ scritti e revisionati su tre livelli (legale → scientifico → supervisore) |
| Libreria consultabile dei contenuti | ✅ `contenuti-social.html` (filtri, testi integrali, copia rapida) |
| Piano marketing e calendario editoriale | ✅ `PIANO-MARKETING.md`, `CONTENUTI-30-GIORNI.md` |
| Negozio Shopify online | ⬜ da aprire (piano Basic, dominio già posseduto) |
| Avatar HeyGen | ⬜ da creare: servono 2-3 minuti di video del fondatore |
| Pixel Meta + GA4 + email automatiche | ⬜ da configurare **prima** di accendere le ads |
| Approvazione del titolare sui contenuti | ⬜ 5 decisioni aperte (vedi §7) |

**Nessun contenuto è stato pubblicato.** La revisione chiusa il 6 luglio 2026 è un via libera
tecnico, non un'autorizzazione.

---

## 5. Come si realizza un video (il flusso che genera quasi tutti i contenuti)

Lo stesso video serve TikTok, Reels e YouTube Shorts, con la variante di testo adatta a ciascuna
piattaforma: gli script sono già scritti in doppia variante.

**Setup una tantum (~1 ora)**
1. Registrare 2-3 minuti del fondatore che parla davanti alla fotocamera: luce da finestra,
   sfondo studio, telefono su treppiede, abbigliamento professionale sobrio (niente camice).
2. Caricare su HeyGen → creare l'avatar personale → attivare la clonazione della voce.
3. Collegare i profili social a Meta Business Suite per la programmazione.

**Routine settimanale (~1-2 ore per 4 video)**
1. Copiare in HeyGen il campo "Corpo (HeyGen)" dello script scelto — i testi sono già nella
   versione approvata, non vanno riscritti.
2. Generare il video, aggiungere il b-roll indicato nello script.
3. In CapCut: sottotitoli automatici + testo dell'hook in sovraimpressione entro il secondo 1.
4. Verificare uno stacco visivo ogni 4-5 secondi (pattern interrupt).
5. Programmare la pubblicazione: 12:30-13:30 oppure 19:00-21:00.
6. Rispondere ai commenti entro poche ore: ogni domanda ricevuta diventa lo script FAQ della
   settimana dopo.

**Specifiche fisse:** verticale 9:16 · sottotitoli sempre attivi (l'80% guarda senza audio) ·
hook nei primi 2 secondi · chiusura con il prodotto inquadrato · flag contenuto AI attivo ·
mai cross-postare il file identico (su Reels il watermark TikTok è penalizzato) · su Reels
aggiungere una copertina statica leggibile per la griglia del profilo.

**Facebook** non è video-first: i 15 post sono testi lunghi con prima riga che funziona da hook
prima del "vedi altro". Pubblicare 3-4 post a settimana, foto reali meglio delle stock, massimo
3 hashtag, link al sito in fondo al post o nel primo commento.

**YouTube**: titolo SEO entro 70 caratteri in formato di ricerca ("Come…", "Perché…"),
`#Shorts` sempre come primo hashtag, montaggio calmo e sottotitoli grandi per il pubblico 40-65.
I due video lunghi sono i pilastri del canale: vanno fissati in home e linkati dagli Shorts
correlati.

---

## 6. Dove sono i contenuti

I 62 contenuti esistono in due forme, con lo stesso testo:

- **`contenuti-social.html`** — libreria da aprire nel browser: filtri per piattaforma, ricerca,
  testi integrali e un pulsante di copia per ogni campo. È il modo pratico per lavorare.
- **I tre file markdown** — `SCRIPT-TIKTOK-REELS.md` (30 script, 2 varianti × 15 temi),
  `SCRIPT-YOUTUBE.md` (15 Shorts + 2 long-form), `POST-FACEBOOK.md` (15 post). Sono la fonte:
  contengono anche i commenti di revisione `LEGAL-FIX`, `SCI-FIX`, `SUP-FIX` che spiegano perché
  una frase è stata riscritta. **Quei commenti non vanno pubblicati** e non vanno "ripristinati"
  alla versione precedente.

Gli identificativi usati ovunque: `TT-01…15` (TikTok), `RL-01…15` (Reels), `YT-01…15` (Shorts),
`YTL-1/2` (long-form), `FB-01…15` (Facebook). Lo stesso numero indica lo stesso tema su tutte le
piattaforme: TT-04, RL-04, YT-04 e FB-04 raccontano tutti il Protocollo Giorno+Notte.

Sequenza di pubblicazione proposta su 4 settimane:

| Settimana | TikTok + Reels | YouTube | Facebook |
|---|---|---|---|
| 1 — chi sei | temi 1-6 | YT-01 → 04 | FB-01 → 04 |
| 2 — problemi quotidiani | temi 7-12 | YT-05 → 08 | FB-05 → 08 |
| 3 — obiezioni | temi 13-15 + repost | YT-09 → 12 | FB-09 → 12 |
| 4 — pilastri | FAQ dai commenti + bilancio | YT-13 → 15, poi YTL-1 e YTL-2 | FB-13 → 15 |

---

## 7. Cosa serve prima di andare online

**Tre condizioni probatorie** (non testuali, ma vincolanti):
1. Archiviare i dati di riacquisto che sostengono «la maggior parte di chi prova, ricompra»
   (TT-15, RL-15, YT-15, FB-15) e la documentazione INCI del 98% di Arnica Montana.
2. Verificare che le recensioni sul sito siano effettivamente tutte testuali prima di pubblicare
   TT-12, che lo afferma.
3. Flag contenuto AI attivo su ogni piattaforma.

**Cinque decisioni che spettano al titolare** (nessun collaboratore può prenderle al suo posto):
1. Tono e immagine del contenuto fondativo (tema 1 / YT-01 / FB-01), camice escluso: da confermare.
2. Lessico «pazienti» oppure «le persone che seguo in studio»: scelta deontologica.
3. Quale seconda recensione citare in YTL-2 fra Elga, Lucia e Anna, verificandone la testualità.
4. Ordine e budget dei boost Facebook: conversione prima (4 → 15 → 12 → 1) o notorietà prima.
5. Garanzia «senza asterischi» e bundle a 44,99 €: l'operatività del negozio deve reggere la
   promessa, perché da lì in poi è un impegno verso il consumatore.

**Per il negozio** (dettagli in `ISTRUZIONI-SHOPIFY.md` e `QA-CHECKLIST.md`): creare i 3 prodotti
ai prezzi corretti, caricare le immagini e sostituire i segnaposto nel file, pubblicare la landing
come template di pagina (non come "Liquid personalizzato": il file supera i 50 KB), configurare
spedizioni con soglia gratuita a 39 €, collegare le pagine legali nel footer, togliere la password
del negozio e fare un ordine di prova.

---

## 8. Mappa dei file

**Sito**
- `mooveland-landing.html` — landing completa con immagini incorporate (anteprima locale)
- `mooveland-shopify.html` — versione per Shopify, con i segnaposto ancora da sostituire
- `moovelab-landing.html` — versione precedente, storica
- `shopify-assets/` — le 4 immagini da caricare su Shopify
- `ISTRUZIONI-SHOPIFY.md` — pubblicazione passo passo
- `QA-CHECKLIST.md` — verifiche tecniche e punti aperti pre-lancio
- `CRO-REPORT.md` — audit di conversione che ha guidato il redesign

**Contenuti e marketing**
- `contenuti-social.html` — libreria dei 62 contenuti
- `SCRIPT-TIKTOK-REELS.md`, `SCRIPT-YOUTUBE.md`, `POST-FACEBOOK.md` — le fonti
- `CONTENUTI-30-GIORNI.md` — calendario editoriale e script base
- `PIANO-MARKETING.md` — strategia in 4 fasi, budget, metriche

**Regole e verifiche**
- `BLACKLIST-CLAIM.md` — **vincolante**: parole vietate e alternative ammesse
- `DOSSIER-SCIENTIFICO.md` — fonte citabile per ogni affermazione, risposte alle contestazioni
- `REVISIONE-SUPERVISORE.md` — verdetti sui 62 contenuti e decisioni in attesa di firma
- `README.md` — indice sintetico del progetto

---

## 9. Incongruenze note (da sapere prima di usare i file)

- **`PIANO-MARKETING.md` è anteriore alla revisione legale.** Contiene due indicazioni oggi
  superate: suggerisce il camice come elemento di fiducia e usa l'esempio "3 errori che fai quando
  ti fa male la schiena". Entrambe sono state eliminate dai contenuti. In caso di contrasto,
  **vince sempre `BLACKLIST-CLAIM.md`**. La struttura strategica del piano (fasi, budget, metriche)
  resta valida.
- **Amazon**: è un canale attivo e la fonte della valutazione 4,4/5, ma sul sito non va mai
  nominato, perché i prezzi sono diversi. Nei contenuti social non compare.
- **Lessico "pazienti"**: oggi i testi dicono "i miei pazienti". Se il titolare sceglie la formula
  più prudente, la sostituzione va fatta in tutti e tre i file di script in una volta sola, per non
  creare incoerenze tra piattaforme.
- **La landing locale e la versione Shopify divergono**: la prima ha le immagini incorporate ed è
  completa, la seconda aspetta gli URL CDN reali. Non si aggiorna una sola delle due.

---

## 10. Regola finale

Nulla si pubblica — né un video, né un post, né una riga del sito — senza l'approvazione esplicita
di Leonardo Rocca. Chi produce i materiali prepara, propone e aspetta il via libera.

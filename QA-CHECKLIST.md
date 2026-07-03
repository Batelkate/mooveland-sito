# QA Checklist — Mooveland Landing (pre-lancio)

Audit del 2026-07-03 su `mooveland-landing.html` (preview locale) e `mooveland-shopify.html`.
Metodo: screenshot full-page a 390px / 768px / 1440px (Chromium headless + Playwright), test funzionali via Playwright, parsing HTML con Python.

---

## ✅ Verificato e funzionante

### Visivo — Mobile (390px, altezza pagina 13.779px)
- Nessun overflow orizzontale: `scrollWidth = clientWidth = 390` (nessuna scrollbar laterale).
- Hero, badge, CTA, trust list, rating bar: layout corretto, testi non tagliati.
- Card benefici (4), manifesto, card prodotto Argilla e Arnica, modalità d'uso, bundle, recensioni, garanzia, FAQ, footer: tutte le sezioni presenti nell'ordine nuovo, nessuna sovrapposizione o testo illeggibile.
- Unica nota: l'immagine ruotata del vasetto nella card Bundle sporge di ~11px oltre il bordo destro, ma è correttamente clippata dal contenitore (nessuno scroll). Effetto decorativo, non un difetto.

### Visivo — Tablet (768px) e Desktop (1440px)
- Nessun overflow orizzontale.
- Griglia benefici a 4 colonne su desktop corretta, hero a 2 colonne con collage prodotti allineato, sezioni in ordine, contrasti leggibili.
- Nota: nelle screenshot full-page alcune card appaiono vuote perché usano l'animazione scroll-reveal (opacity 0 fino a intersezione). Verificato con screenshot a scroll reale: i contenuti si rivelano correttamente.

### Funzionale — FAQ accordion
- 5 `button.faq-trigger` presenti, JS intatto, selettori coerenti col markup.
- Click apre l'item (`aria-expanded="true"`), aprendo un secondo item il primo si chiude (comportamento accordion), secondo click chiude. Testato in browser reale.

### Funzionale — Sticky CTA mobile
- `#sticky-cta` presente, JS intatto; nascosta a inizio pagina, appare dopo lo scroll oltre la hero (`.hero` trovata), `aria-hidden` aggiornato, `body.has-sticky-cta` applica il padding.
- Il bottone "Acquista Ora" punta a `#bundle`, che esiste: il click porta alla sezione bundle (verificato, `location.hash = #bundle`).

### Coerenza HTML (entrambi i file)
- Tag bilanciati (dopo il fix sotto), nessun tag non chiuso a fine file.
- Nessun id duplicato.
- Tutti gli anchor interni risolvono: `#prodotti`, `#bundle`, `#manifesto` (ids presenti anche `#recensioni`, `#faq`, `#hero-title`, ecc.).

---

## 🔧 Correzioni applicate

1. **Rimossi 2 `</div>` orfani dopo la chiusura della sezione hero** (residuo del riordino sezioni):
   - `mooveland-landing.html` (ex righe 855-856)
   - `mooveland-shopify.html` (ex righe 858-859)
   Il parser li segnalava come chiusure spurie; dopo la rimozione entrambi i file risultano perfettamente bilanciati. Layout ri-verificato con screenshot post-fix a 390px e 1440px: invariato e corretto.

---

## ⚠️ Da fare manualmente prima del lancio

1. **Recensioni Amazon reali** — sostituire tutti i placeholder `[DA-SOSTITUIRE: ...]`: media reale, numero recensioni (hero + sezione recensioni), 4 testi integrali di recensioni verificate con nomi, e la nota su come vengono raccolte/verificate (obbligo Direttiva Omnibus UE).
2. **Foto del fondatore** — placeholder `[Foto del Fondatore]` nella sezione manifesto.
3. **Giorni di garanzia** — confermare `[DA-CONFERMARE: 14/30 giorni]` e i termini/condizioni della garanzia (compare in 3+ punti: card prodotti, bundle, sezione garanzia).
4. **Variant ID Shopify** — sostituire i placeholder variant ID in `mooveland-shopify.html` (vedi `ISTRUZIONI-SHOPIFY.md`).
5. **URL CDN immagini** — sostituire gli `https://cdn.shopify.com/PLACEHOLDER/...` con gli URL reali dopo l'upload degli asset in `shopify-assets/`.
6. **Link legali footer** — Privacy Policy, Termini e Condizioni, Spedizioni e Resi, Contatti, FAQ puntano tutti a `href="#"`: collegare alle pagine reali.
7. **Favicon** — non presente: aggiungere `<link rel="icon">`.
8. **Meta SEO/social** — aggiungere `og:image`, `og:title`, `og:description`, `meta description` e `twitter:card` (assenti).
9. **Scroll-reveal senza JS** — con JavaScript disattivato le card animate restano visibili (la classe `reveal` è aggiunta via JS), ma verificare su Shopify che nessun ottimizzatore ritardi lo script IntersectionObserver.

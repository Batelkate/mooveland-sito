# Mooveland — Guida passo-passo per pubblicare la landing su Shopify

Questa guida ti porta da zero alla landing online sul tuo dominio. Non serve saper programmare: dovrai solo **copiare/incollare** e **sostituire alcune scritte segnaposto** nel file `mooveland-shopify.html`.

I segnaposto da sostituire sono:

| Segnaposto | Cosa metterci |
|---|---|
| `VARIANT_ID_ARGILLA` | ID variante del prodotto Argilla Moovelab |
| `VARIANT_ID_ARNICA` | ID variante del prodotto Arnica Mooveland |
| `VARIANT_ID_BUNDLE` | ID variante del prodotto Bundle |
| `https://cdn.shopify.com/PLACEHOLDER/logo-mooveland.webp` | URL vero del logo caricato su Shopify |
| `https://cdn.shopify.com/PLACEHOLDER/argilla-moovelab.webp` | URL vero della foto Argilla |
| `https://cdn.shopify.com/PLACEHOLDER/arnica-mooveland.jpg` | URL vero della foto Arnica |

---

## 1. Crea i prodotti (3 prodotti + 1 Bundle)

Nel pannello Shopify: **Prodotti → Aggiungi prodotto**. Crea questi 3 prodotti:

1. **Argilla Moovelab 250ml** — Prezzo: **28,00 €**
2. **Arnica Mooveland 500ml** — Prezzo: **31,00 €**
3. **Bundle Recupero Completo (Argilla + Arnica)** — Prezzo: **44,99 €**, prezzo confrontato: 59,00 €

> **Perché il Bundle come prodotto separato?** È il metodo più semplice e affidabile: un solo click aggiunge tutto al carrello, il prezzo scontato è garantito e l'inventario resta gestibile. L'alternativa (link che aggiunge 2 prodotti insieme) è più fragile e non applica lo sconto da sola.

Per ogni prodotto: carica la foto, scrivi la descrizione, imposta la quantità in magazzino e spunta "Traccia quantità" se vuoi il conteggio scorte.

### Dove trovare il Variant ID
1. Apri il prodotto nel pannello Shopify.
2. Guarda l'indirizzo nella barra del browser: `https://admin.shopify.com/store/TUONEGOZIO/products/1234567890`.
3. Aggiungi `.json` alla fine dell'URL **del prodotto visto dal negozio online** oppure, più semplice: nel pannello prodotto, se il prodotto **non ha varianti** (taglie/colori), clicca sui tre puntini / "Visualizza" e usa questo trucco:
   - Vai alla pagina del prodotto sul tuo negozio online (es. `tuonegozio.myshopify.com/products/argilla-moovelab`).
   - Aggiungi `.js` alla fine dell'indirizzo: `.../products/argilla-moovelab.js`
   - Si apre un testo: cerca `"variants":[{"id":` — il **numero lungo subito dopo** è il Variant ID (es. `41234567890123`).
4. Annota i 3 numeri: uno per Argilla, uno per Arnica, uno per il Bundle.

---

## 2. Carica le 3 immagini e prendi gli URL CDN

1. Nel pannello Shopify: **Contenuti → File** (in inglese: Content → Files).
2. Clicca **Carica file** e carica i 3 file dalla cartella `shopify-assets/`:
   - `logo-mooveland.webp`
   - `argilla-moovelab.webp`
   - `arnica-mooveland.jpg`
3. Per ciascun file, clicca sull'**icona a forma di catena/link** (Copia link): otterrai un indirizzo tipo
   `https://cdn.shopify.com/s/files/1/0xxx/xxxx/files/argilla-moovelab.webp?v=1234567890`
4. Annota i 3 indirizzi.

---

## 3. Sostituisci i segnaposto nel file

1. Apri `mooveland-shopify.html` con un editor di testo (Blocco Note su Windows, TextEdit su Mac in modalità testo, o meglio [VS Code], gratuito).
2. Usa **Trova e sostituisci** (Ctrl+H / Cmd+H):
   - Trova `VARIANT_ID_ARGILLA` → sostituisci con il numero dell'Argilla (sostituisci tutto).
   - Trova `VARIANT_ID_ARNICA` → numero dell'Arnica.
   - Trova `VARIANT_ID_BUNDLE` → numero del Bundle.
   - Trova `https://cdn.shopify.com/PLACEHOLDER/logo-mooveland.webp` → incolla l'URL vero del logo.
   - Trova `https://cdn.shopify.com/PLACEHOLDER/argilla-moovelab.webp` → URL vero dell'Argilla.
   - Trova `https://cdn.shopify.com/PLACEHOLDER/arnica-mooveland.jpg` → URL vero dell'Arnica.
3. Salva il file. (I commenti verdi `<!-- SHOPIFY: ... -->` puoi lasciarli, non danno fastidio.)

### Come funzionano i bottoni "Aggiungi al Carrello"
Sono link nel formato `/cart/add?id=NUMERO&quantity=1`: quando il cliente clicca, Shopify aggiunge il prodotto al carrello e apre la pagina carrello. Nessuna app necessaria, funziona sul piano Basic.

---

## 4. Pubblica la pagina (metodo consigliato)

⚠️ Il file pesa circa **88 KB**, quindi **NON entra nella sezione "Liquid personalizzato"** dell'editor tema (limite 50 KB). Il metodo giusto è un **template di pagina personalizzato** (limite 256 KB — ci stiamo comodamente):

1. Pannello Shopify: **Negozio online → Temi → ⋯ (tre puntini) → Modifica codice**.
2. Nella colonna a sinistra, sotto **Templates**, clicca **Aggiungi un nuovo template**:
   - Tipo: **page**
   - Formato: **liquid**
   - Nome: `landing` (diventerà `page.landing.liquid`)
3. Cancella tutto il contenuto proposto e **incolla l'intero contenuto** di `mooveland-shopify.html` (già con i segnaposto sostituiti).
4. Clicca **Salva**.
5. Ora crea la pagina: **Negozio online → Pagine → Aggiungi pagina**:
   - Titolo: `Mooveland` (il titolo non verrà mostrato, la landing ha il suo header).
   - A destra, in **Template**, scegli `landing`.
   - Visibilità: **Visibile**. Salva.

> Nota: con questo metodo la pagina mostra anche header e footer del tema sopra/sotto la landing. Se vuoi la landing "pulita" senza header del tema, chiedi a chi ti assiste di creare anche un layout alternativo (`layout/landing.liquid` con solo `{{ content_for_layout }}`) e aggiungere in cima al template la riga `{% layout 'landing' %}`. È un passaggio da 2 minuti per uno sviluppatore.

**Alternative** (se non vuoi toccare il codice): app "page builder" come PageFly o GemPages (piano gratuito per 1 pagina), ricostruendo la landing coi loro blocchi. Più lavoro manuale, ma zero codice.

---

## 5. Imposta la landing come homepage del dominio

Shopify non permette di assegnare direttamente una "Pagina" come homepage, ma c'è un reindirizzamento semplice. Due opzioni:

**Opzione A (consigliata, semplice):** lascia la homepage del tema e metti la landing su `tuodominio.it/pages/mooveland`. Usa questo link nelle pubblicità e sui social. Nella homepage del tema metti un banner grande che porta alla landing.

**Opzione B (landing = homepage):** nel tema, editor **Negozio online → Temi → Personalizza**, apri la homepage e rimuovi tutte le sezioni tranne una sezione "Liquid personalizzato" con dentro solo:
```html
<script>window.location.replace('/pages/mooveland');</script>
```
Sconsigliata per la SEO. Meglio ancora: fatti aiutare a spostare il contenuto del template sulla homepage del tema (template `index`).

**Collegare il dominio:** **Impostazioni → Domini → Collega dominio esistente**, inserisci il tuo dominio e segui le istruzioni per aggiornare i DNS presso il tuo provider (di solito record A `23.227.38.65` e CNAME `shops.myshopify.com` — Shopify te li mostra). Imposta il dominio come **primario**.

---

## 6. Checklist finale pre-lancio

- [ ] I 3 prodotti + Bundle sono creati con prezzi giusti (28 € / 31 € / 44,99 €) e foto
- [ ] Le 3 immagini sono caricate in Contenuti → File
- [ ] Nel file non c'è più nessun `VARIANT_ID_` né `PLACEHOLDER` (usa Trova per verificare)
- [ ] Il template `page.landing.liquid` è salvato e la pagina "Mooveland" usa quel template
- [ ] Cliccando "Aggiungi al Carrello" su ciascun prodotto, il prodotto giusto finisce nel carrello
- [ ] Il bottone del Bundle aggiunge il Bundle a 44,99 €
- [ ] Le immagini si vedono (logo in alto, barattoli nelle schede prodotto)
- [ ] La pagina si vede bene da telefono (prova con il tuo!)
- [ ] Spedizioni configurate: **Impostazioni → Spedizione**, con soglia gratuita sopra 39 € (come promesso in pagina!)
- [ ] Pagamenti attivi: **Impostazioni → Pagamenti** (Shopify Payments + PayPal)
- [ ] Testo `[DA-CONFERMARE: 14/30 giorni]` sulla garanzia sostituito con la durata reale del reso
- [ ] Pagine legali create e collegate nel footer: Privacy Policy, Termini, Spedizioni e Resi, Contatti (Shopify le genera in **Impostazioni → Documenti legali**; i link nel footer della landing puntano a `#` e vanno aggiornati con gli URL veri, es. `/policies/privacy-policy`)
- [ ] Dominio collegato e impostato come primario, certificato SSL attivo (automatico, attendi qualche ora)
- [ ] Rimosso il blocco password del negozio: **Negozio online → Preferenze → togli la password**
- [ ] Fai un **ordine di prova** completo (Shopify ha la "Bogus Gateway" o usa un buono sconto 100%)

Buon lancio! 🚀

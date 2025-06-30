# 🧪 Prova Tecnica – Sviluppatore Full Stack Laravel

## 🎯 Obiettivo della prova

Valutare le competenze del candidato nei seguenti ambiti tecnici:

- **Linguaggi:** PHP ([Laravel](https://laravel.com/), [Filament](https://filamentphp.com/)), MySQL, JavaScript ([AlpineJS](https://alpinejs.dev/), [Livewire](https://livewire.laravel.com/)), HTML, CSS ([TailwindCSS](https://tailwindcss.com/))
- **Concetti:** Utilizzo delle queue e task asincroni, capacità di leggere e comprendere documentazione tecnica
- **Frameworks/Tooling:** Laravel, Filament, Livewire, AlpineJS, TailwindCSS
- **Database:** Modellazione con Eloquent, **con particolare attenzione alla gestione delle relazioni tra modelli**

---

## 🌐 Fonte dati da utilizzare

La fonte dati da cui estrarre le informazioni da importare è la seguente:

🔗 [https://sandbox.oxylabs.io/products](https://sandbox.oxylabs.io/products)

Lo script crawler dovrà estrarre dati come:

- `title`
- `price`
- `image_url`
- `description` (se presente)
- `category` o altro campo utile a fini di classificazione

---

## 🧪 Struttura della prova

### ✅ 1. Creazione di un Crawler in PHP

- Scrivi uno script PHP per estrarre i dati dal sito indicato sopra.
- Il crawler dovrà esportare i dati in formato JSON leggibile da Laravel.
- Puoi usare qualsiasi libreria (cURL, Guzzle, Symfony DomCrawler, ecc.).

### ✅ 2. Backend Laravel – Importazione asincrona

- Crea un nuovo progetto Laravel.
- Crea due modelli Eloquent:
  - `Product`: rappresenta il prodotto
  - `Image`: rappresenta una o più immagini associate
- Assicurati di **gestire correttamente la relazione tra modelli**.
- Crea una route `POST /api/import` per ricevere i dati JSON dal crawler.
- L'importazione deve avvenire in **modo asincrono**, tramite un sistema di **queue** con un **Job** dedicato.

### ✅ 3. Filament Admin

- Installa Filament nel progetto.
- Crea una **Resource** Filament (`ProductResource`) per:
  - Visualizzare tutti i prodotti
  - Modificare o eliminare i record
  - Mostrare immagine di preview nella lista dei prodotti

### ✅ 4. Frontend dinamico – Livewire + AlpineJS

- Crea una pagina raggiungibile da `/view/products`
- La pagina deve:
  - Mostrare i prodotti impaginati (25 per pagina, minimo 2 pagine)
  - Consentire l’ordinamento per data di inserimento o altro criterio
  - Essere dinamica tramite **Livewire + AlpineJS**
  - Avere uno stile pulito e responsive tramite **TailwindCSS**

---

## 📝 Valutazione

| Area                     | Aspetti valutati                                           |
|--------------------------|------------------------------------------------------------|
| **PHP**                  | Pulizia, struttura, uso librerie per scraping              |
| **Laravel**              | Best practices, gestione asincrona, API                    |
| **Eloquent**             | Modellazione, relazioni tra modelli                        |
| **Filament**             | Integrazione e uso efficace del pannello admin             |
| **Livewire/AlpineJS**    | Reattività del frontend senza ricaricamenti pagina         |
| **TailwindCSS**          | Uso coerente delle utility, responsive design              |
| **Soft Skills**          | Chiarezza, organizzazione, capacità di documentazione      |

---

## ⏱️ Tempo stimato

**6–12 ore**. La prova può essere completata in più fasi. È ammesso inviare codice parzialmente completo, purché ben documentato.

---

## 📦 Consegna

- Link al repository (GitHub, GitLab, Bitbucket)
- README completo con istruzioni per l’installazione
- (Facoltativo) Utilizzo di Docker, DDEV o Laravel Sail per setup rapido

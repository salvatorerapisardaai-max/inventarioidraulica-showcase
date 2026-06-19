# 🔧 Inventario Idraulica

> 🇬🇧 [English](#-english) · 🇮🇹 [Italiano](#-italiano)

![Next.js](https://img.shields.io/badge/Next.js-14-000000?logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?logo=supabase&logoColor=white)
![Claude](https://img.shields.io/badge/AI-Claude%20Sonnet-D97757)
![Vercel](https://img.shields.io/badge/Vercel-deployed-000000?logo=vercel&logoColor=white)

**🔗 Live demo:** [inventario-idraulica.vercel.app](https://inventario-idraulica.vercel.app)

---

## 🇬🇧 English

> Inventory-management platform for a plumbing business, with **automatic AI recognition of components from photos**.

> Source code lives in a private repository (business logic and credentials). This is a public showcase — published as a portfolio reference.

### Why I built it

The family plumbing business tracked stock by memory and scattered notes. The hard part of a plumbing inventory isn't the database — it's *data entry*: hundreds of near-identical fittings nobody wants to catalogue by hand. So I made the catalogue build itself: **snap a photo, and a generative-AI model identifies the component and extracts structured data**.

### What it does

- 🤖 **AI component analysis** — recognises plumbing components from a photo and extracts structured data (type, model, specs) via Anthropic Claude Sonnet, called through its API.
- 📦 **Inventory management** — item catalogue with photos, descriptions, prices and supplier records.
- 🗂️ **Hierarchical locations** — physical organisation by zones (A → B → C → D → section) so items can actually be found.
- ⚠️ **Stock monitoring** — automatic low-stock alerts and reorder notifications, with full movement history.
- 💾 **Export & reporting** — CSV export of the catalogue and per-supplier / per-area stock reports.
- 🔐 **Auth & security** — route protection via Supabase Auth, cookie-based SSR sessions, protected routes through Next.js middleware.

### Architecture

| Layer | Tech |
|------|------|
| Front-end | Next.js 14 (App Router) + React 18 |
| Language | TypeScript 5 |
| Database / Auth | Supabase (PostgreSQL, Auth) |
| AI / ML | Anthropic Claude Sonnet (vision + structured extraction, via API key) |
| Hosting / CI | Vercel (auto-deploy on push to `main`) |

**Engineering highlights**
- **Gen-AI as a data-entry engine**: the model turns an unstructured photo into a typed catalogue record — generative AI integrated through an API key to remove the most tedious manual step.
- **Hierarchical location model** mirroring how a real warehouse is physically laid out, not just a flat list.
- **Middleware-enforced auth** with Supabase SSR: public routes (`/login`, `/articolo/:id`) vs protected areas handled in one place.

### Roadmap
- 📊 Analytics dashboard with charts
- 🔔 Push / Telegram / WhatsApp stock alerts
- 📱 Native mobile app
- 🏷️ Barcode / QR-code scanning
- 🛒 E-commerce integration

### What I learned

Using generative AI to solve a genuinely boring real-world problem — catalogue data entry — instead of as a gimmick. Designing the prompt and parsing the structured output reliably, modelling a hierarchical warehouse in PostgreSQL, and securing the whole thing with Supabase Auth and Next.js middleware.

---

## 🇮🇹 Italiano

> Piattaforma di gestione inventario per un'attività di idraulica, con **riconoscimento automatico dei componenti da foto tramite IA**.

> Il codice sorgente è in un repository privato (logica di business e credenziali). Questa è una vetrina pubblica — pubblicata come riferimento di portfolio.

### Perché l'ho costruito

L'attività di idraulica di famiglia gestiva il magazzino a memoria e su appunti sparsi. La parte difficile di un inventario idraulico non è il database: è l'*inserimento dati*, centinaia di raccordi quasi identici che nessuno ha voglia di catalogare a mano. Così ho fatto in modo che il catalogo si costruisca da solo: **scatti una foto e un modello di IA generativa riconosce il componente ed estrae i dati strutturati**.

### Cosa fa

- 🤖 **Analisi AI dei componenti** — riconosce i componenti idraulici da una foto ed estrae dati strutturati (tipo, modello, specifiche) tramite Anthropic Claude Sonnet, richiamato via API.
- 📦 **Gestione inventario** — catalogo articoli con foto, descrizioni, prezzi e anagrafiche fornitori.
- 🗂️ **Posizioni gerarchiche** — organizzazione fisica per zone (A → B → C → D → sezione), così gli articoli si trovano davvero.
- ⚠️ **Monitoraggio stock** — alert automatici sotto soglia e notifiche di riordino, con storico movimenti completo.
- 💾 **Export & reporting** — export CSV del catalogo e report per fornitore / per area.
- 🔐 **Autenticazione & sicurezza** — protezione delle rotte via Supabase Auth, sessioni SSR cookie-based, rotte protette tramite middleware Next.js.

### Architettura

| Livello | Tecnologia |
|------|------|
| Front-end | Next.js 14 (App Router) + React 18 |
| Linguaggio | TypeScript 5 |
| Database / Auth | Supabase (PostgreSQL, Auth) |
| AI / ML | Anthropic Claude Sonnet (vision + estrazione strutturata, via API key) |
| Hosting / CI | Vercel (deploy automatico ad ogni push su `main`) |

**Punti tecnici notevoli**
- **IA generativa come motore di data-entry**: il modello trasforma una foto non strutturata in un record di catalogo tipizzato — IA generativa integrata tramite API key per eliminare il passaggio manuale più noioso.
- **Modello di posizioni gerarchico** che rispecchia la disposizione fisica reale di un magazzino, non una semplice lista piatta.
- **Auth applicata via middleware** con Supabase SSR: rotte pubbliche (`/login`, `/articolo/:id`) e aree protette gestite in un unico punto.

### Roadmap
- 📊 Dashboard analitica con grafici
- 🔔 Alert stock push / Telegram / WhatsApp
- 📱 App mobile nativa
- 🏷️ Scansione barcode / QR-code
- 🛒 Integrazione e-commerce

### Cosa ho imparato

Usare l'IA generativa per risolvere un problema reale e genuinamente noioso — l'inserimento dati del catalogo — invece che come gadget. Progettare il prompt e fare il parsing affidabile dell'output strutturato, modellare un magazzino gerarchico in PostgreSQL e mettere in sicurezza il tutto con Supabase Auth e il middleware di Next.js.

---

**Built and maintained by / Realizzato e mantenuto da Salvatore Rapisarda** ([@salvatorerapisardaai-max](https://github.com/salvatorerapisardaai-max))

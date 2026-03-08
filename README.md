# VisualAI Commerce - Piattaforma AI per E-commerce

## 📋 Indice
1. [Descrizione Progetto](#descrizione)
2. [Analisi di Mercato](#analisi-di-mercato)
3. [Diagramma dei Casi d'Uso](#diagramma-uml)
4. [Requisiti Principali](#requisiti)
5. [User Stories](#user-stories)

---

## Descrizione

**VisualAI Commerce** è una piattaforma SaaS che permette ai proprietari di negozi online di generare foto professionali dei prodotti usando l'intelligenza artificiale, senza bisogno di fotografi costosi.

### 🎯 Il Problema
- 💰 Fotografi professionali costano troppo
- ⏱️ Ci vuole settimane per ottenere le foto
- 😤 Difficile aggiornare il catalogo frequentemente
- 📍 Nessuno strumento per mercati internazionali

### 👥 Chi Lo Usa
- Piccoli negozi online (e-commerce)
- Venditori su Shopify e WooCommerce
- Agenzie che gestiscono più store
- Budget limitato per il marketing

### 💡 La Soluzione
L'utente carica una descrizione e una foto del prodotto → L'AI genera automaticamente una serie di foto professionali → L'utente può modificarle e pubblicarle direttamente nel suo negozio → Paga solo per quello che usa (pacchetti da 5, 10, 25, 50 foto).

### 🛠️ Tecnologie Principali
- **Frontend**: React, TypeScript, Tailwind CSS
- **Backend**: Node.js / Python, PostgreSQL
- **AI**: OpenAI (DALL-E), Stability AI
- **Pagamenti**: Stripe
- **Cloud**: AWS S3, CloudFlare CDN

---

## Analisi di Mercato

### Tabella di Benchmarking per Analisi dei Competitors

| Feature | Importance | Your Brand | Competitor A | Competitor B | Competitor X |
|---------|-----------|-----------|-------------|-------------|-------------|
| **Generazione Immagini AI** | High | ✅ | ✅ | ✅ |  |
| **Modelli Template Predesignati** | High | ✅ | ✅ |  |  |
| **Pacchetti Prezzo Scalabili** | High | ✅ | ✅ |  | ✅ |
| **Integrazione Diretta E-commerce** | High | ✅ |  |  |  |
| **Customizzazione Brand/Colori** | High | ✅ | ✅ | ✅ |  |
| **Generazione Descrizioni Prodotto** | Moderate | ✅ | ✅ |  | ✅ |
| **Varianti di Prodotto (SKU)** | Moderate | ✅ | ✅ |  |  |
| **Editing Post-Generazione** | Moderate | ✅ | ✅ | ✅ |  |
| **Supporto Lingua Multi-Locale** | Moderate | ✅ |  | ✅ |  |
| **Analytics e Performance Tracking** | Low | ✅ |  |  | ✅ |

**Legenda:**
- ✅ = Funzionamento presente
- ⬜ = Non disponibile/assente

### 📊 Competitor Principali

| Competitor | Prezzo | Vantaggi | Svantaggi |
|-----------|--------|----------|-----------|
| **Shopify AI (Competitor A)** | €29 | Integrazione nativa | Solo per Shopify |
| **Adobe Express (Competitor B)** | €119 | Suite completa | Troppo complesso per PMI |
| **Canva (Competitor X)** | €120 | Facile da usare | Generico, non per e-commerce |

### 📊 Posizionamento di VisualAI Commerce
- **Specializzazione**: Solo per e-commerce + AI (differenziatore chiave)
- **Prezzo**: Competitivo (€29 entry-level, come Shopify)
- **Velocità**: Minuti invece di settimane
- **Semplicità**: Zero competenze tecniche richieste
- **Vantaggio**: Integrazione diretta con Shopify E WooCommerce (esclusivo)

---

## Diagramma UML

### 📊 Casi d'Uso Principali

**diagramma UML:**
<img width="1713" height="798" alt="immagine" src="https://github.com/user-attachments/assets/d5d446a6-b572-4e65-a8cb-0f0e4e137262" />


**Attori:**
- 👤 **Proprietario**: Proprietario del negozio (utente principale)
- 🔧 **Admin**: Amministratore della piattaforma
- 🏦 **Banca**: Sistema di pagamento
- 🤖 **Servizio AI**: Servizio generazione immagini

**Flusso Principale:**
1. **Registrazione** → Conferma Email
2. **Selezione Pacchetto** → Carrello → Checkout → Pagamento
3. **Caricamento Prodotto** → Dettagli → Generazione Immagini
4. **Dashboard** → Statistiche e Storico
5. **Gestione Crediti** → Acquista o Verifica Saldo

---

## Requisiti

### 🟢 Requisiti Funzionali (cosa deve fare)

| ID | Funzionalità | Descrizione |
|----|------------|------------|
| **RF1** | Registrazione | Login con email/password o Google |
| **RF2** | Selezione Pacchetto | Scelta tra 4 opzioni di prezzo |
| **RF3** | Carrello | Visualizzazione riepilogo, tasse, totale |
| **RF4** | Pagamento | Checkout con Stripe |
| **RF5** | Caricamento Prodotto | Caricamento immagini (max 5MB) |
| **RF6** | Dettagli Prodotto | Descrizione, categoria, colori, stile |
| **RF7** | Generazione AI | Crea foto automaticamente |
| **RF8** | Visualizza Dashboard | Metriche e storico progetti |
| **RF9** | Gestione Crediti | Acquista o verifica saldo |
| **RF10** | Amministrazione | Gestione utenti e monitoraggio sistema |

### 🔴 Requisiti Non Funzionali (come deve funzionare)

| ID | Requisito | Target |
|----|-----------|--------|
| **RNF1** | Velocità caricamento | < 2 secondi |
| **RNF2** | Generazione foto | < 60 secondi |
| **RNF3** | Disponibilità | 99.5% uptime |
| **RNF4** | Sicurezza | HTTPS, JWT, GDPR |
| **RNF5** | Scalabilità | 1000+ utenti simultanei |
| **RNF6** | Accessibilità | Mobile-responsive, WCAG AA |
| **RNF7** | Database | PostgreSQL 14+ |

### 🔵 Requisiti di Dominio (regole del settore)

- **E-commerce**: Supporto categorie prodotto, varianti (colore, taglia)
- **AI**: Scelta modello (DALL-E, Stability AI), prompt professionali
- **Fotografia**: Best practices di lighting, background, prospettiva
- **Pagamenti**: Idempotency key, webhook Banca, refund policy
- **Conformità**: GDPR, CCPA, IP rights, DMCA takedown

---

## User Stories

### 👤 Come proprietario di e-commerce...

#### **STORY 1 - Registrazione e Login**
```
Come proprietario di e-commerce,
voglio registrarmi con email/password o Google,
in modo da accedere ai servizi.

✓ Form registrazione
✓ Validazione email
✓ Conferma via email (24h)
✓ Password sicura (8+ caratteri)
✓ Login con SSO Google
```

#### **STORY 2 - Selezione Pacchetto**
```
Come proprietario di e-commerce,
voglio scegliere tra 4 pacchetti,
in modo da pagare solo quello che uso.

✓ Pacchetti: 5 foto (€29), 10 foto (€49), 25 foto (€99), 50 foto (€199)
✓ Descrizione features per ogni pacchetto
✓ Aggiunta al carrello
```

#### **STORY 3 - Carrello e Checkout**
```
Come proprietario di e-commerce,
voglio visualizzare il riepilogo del carrello,
in modo da verificare i costi prima del pagamento.

✓ Riepilogo prezzo, tasse, totale
✓ Calcolo tasse (IVA per Italia)
✓ Codice coupon
✓ Pulsante checkout
```

#### **STORY 4 - Pagamento**
```
Come proprietario di e-commerce,
voglio pagare in modo sicuro,
in modo da completare l'acquisto.

✓ Stripe Checkout integrato
✓ Carte di credito (Visa, Mastercard, Amex)
✓ Apple Pay, Google Pay
✓ Ricevuta email automatica
```

#### **STORY 5 - Caricamento Prodotto**
```
Come proprietario di e-commerce,
voglio caricare foto e dettagli del mio prodotto,
in modo da farla generare dall'AI.

✓ Drag & drop per caricare file
✓ Formati: JPG, PNG (max 5MB)
✓ Preview immagine
✓ Inserimento descrizione prodotto
✓ Selezione categoria
✓ Scelta colori brand
✓ Scelta stile (minimalist, lussuoso, sportivo)
```

#### **STORY 6 - Generazione AI**
```
Come proprietario di e-commerce,
voglio che l'AI generi automaticamente le foto,
in modo da risparmiare tempo.

✓ Invio al sistema di generazione
✓ Progress bar con tempo stimato
✓ Notifica quando pronte
✓ Download immediate
```

#### **STORY 7 - Visualizza Dashboard**
```
Come proprietario di e-commerce,
voglio visualizzare le mie statistiche,
in modo da monitorare l'utilizzo.

✓ Statistiche: foto generate, crediti rimasti, spesa totale
✓ Storico progetti con date e status
✓ Export report PDF/CSV
```

#### **STORY 8 - Gestione Crediti**
```
Come proprietario di e-commerce,
voglio ricevere avvisi sui crediti,
in modo da non rimanere bloccato.

✓ Widget crediti in navbar
✓ Notifica a 20%, 10%, 0%
✓ Acquisto crediti extra on-demand
✓ Opzione subscription mensile
```

#### **STORY 9 - Pubblicazione**
```
Come proprietario di e-commerce,
voglio pubblicare le foto nel mio negozio,
in modo da venderle.

✓ Connettore Shopify (OAuth)
✓ Connettore WooCommerce
✓ Pubblicazione diretta
✓ Aggiornamento metadati prodotto
```

---

### 🔧 Come amministratore...

#### **STORY A1 - Gestione Utenti**
```
Come amministratore,
voglio gestire account utenti e crediti,
in modo da amministrare la piattaforma.

✓ Visualizzazione lista utenti
✓ Reset password
✓ Aggiungi/rimuovi crediti
✓ Ban utenti violatori
```

#### **STORY A2 - Monitoraggio Sistema**
```
Come amministratore,
voglio monitorare la salute del sistema,
in modo da risolvere problemi velocemente.

✓ Dashboard health check
✓ Log centralizzati
✓ Alerts su Slack se errori
✓ Status page pubblica
```

---

## 🔒 Conformità e Sicurezza

- ✅ **GDPR**: Diritto all'oblio, data portability
- ✅ **CCPA**: Privacy US (California)
- ✅ **Sicurezza**: HTTPS TLS 1.3, JWT auth, RBAC
- ✅ **Pagamenti**: PCI DSS via Stripe
- ✅ **IP Rights**: Chiaro che le foto appartengono all'utente
- ✅ **Accessibilità**: WCAG 2.1 AA, mobile-first

---

## Link lovable
```
https://id-preview--ece5c7f5-4f91-4d64-8600-596e0dacb4b4.lovable.app/?__lovable_token=eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoia0RJZU1hWEwxQlpqeWVCdDlLVVRReEVQT3RoMiIsInByb2plY3RfaWQiOiJlY2U1YzdmNS00ZjkxLTRkNjQtODYwMC01OTZlMGRhY2I0YjQiLCJhY2Nlc3NfdHlwZSI6InByb2plY3QiLCJpc3MiOiJsb3ZhYmxlLWFwaSIsInN1YiI6ImVjZTVjN2Y1LTRmOTEtNGQ2NC04NjAwLTU5NmUwZGFjYjRiNCIsImF1ZCI6WyJsb3ZhYmxlLWFwcCJdLCJleHAiOjE3NzM2MTA3MjAsIm5iZiI6MTc3MzAwNTkyMCwiaWF0IjoxNzczMDA1OTIwfQ.QoPZpOECL7Cxh_A0JEdYZ1J4zLgD_rDfcRwMNYrAvPQYurAAZBqGHUsC0MHJxDel_z8ABcsyMbwIvr0oomWrTxsVoB0j_Ne5nrn65v0Rcq_DibQXBf4TGt1dIALu3M-CYtJEThpGXoun8sRJ_KwoGRgZ42GsbiMHVaBKU-F8QGOEIP7pG2nVX97b_xG8WXDVVcP0MuqVS4Wlgcf09zfXs-arGCSGu58CBO2ixAN-_-vYapwo8KS1o5Cdk8Yu4dLAOEe2OItFhxtA1CMZ0QF0QkjYaIyw-QQLBplttjRxW3o5_YkaK3Kt6FQbIcE_CLvGHrG0LAwT_JdGSBADUKf0Z4Z8R3auDYkKiHeVRGEi8PjMhoz__460OsI_sCIkL7MCEwuUcbMAHU7vqC62NCeUM0NxHhRKEDUbLhDYTltRybz0AX4XLQRvvMqkFd59x-GjFoIjrXv5vC9xNhaw7b8PtER9jVALee1WqQtC23Y4RTpoj2e--8NUWw4Vye985wQNmvXsibtbFYAj9WZ95_JCsHLeKUDqr6sB6AhB6JlZuj8T1jZZDTRc-JbvdwB587o8omm0FH526Smn_42aHExhOLm4yZGgKjTpx4hiU48YH5KTyV3ZEdmOgjJ5c69ssdjDTTbZwe8JfD3AQzgqAY4eTO_JH2_QY7AJnkrKpeBL2u8
```

---


### WBS del Progetto
```
  root((ShowroomAi))
    1 Analisi
      Requisiti
      Competitors
    2 Design
      UI/UX
      Flussi
    3 Sviluppo
      Frontend
      Backend
      AI
    4 Test
      Funzionali
      Utenti
```

---


### GANTT del Progetto

gantt
  dateFormat  YYYY-MM-DD
  title ShowroomAi - Progetto Scolastico
  section 1 Analisi
  Requisiti & Competitors :2026-03-10, 7d
  section 2 Design
  UI/UX & Flussi :2026-03-20, 7d
  section 3 Sviluppo
  Frontend & Backend :2026-04-01, 14d
  AI



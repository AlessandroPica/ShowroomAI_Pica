# VisualAI Commerce - AI-Powered E-commerce Showcase Generator

## 📋 Indice dei Contenuti
1. [Titolo, Descrizione e Metadata](#1-titolo-descrizione-e-metadata)
2. [Benchmarking Competitivo](#2-benchmarking-competitivo)
3. [Analisi dei Requisiti](#3-analisi-dei-requisiti)
4. [Use Case Diagram](#4-use-case-diagram-e-scenari)
5. [User Stories - Analisi Requisiti Formattata](#5-user-stories---analisi-requisiti-formattata)

---

## 1. Titolo, Descrizione e Metadata

### 🎯 Titolo
**VisualAI Commerce** - Piattaforma di E-commerce Intelligente con Generazione di Vetrine Tramite AI

### 📝 Descrizione
VisualAI Commerce è una piattaforma SaaS innovativa che consente ai proprietari di e-commerce online di creare vetrine di alta qualità utilizzando l'Intelligenza Artificiale generativa, senza necessità di investire in fotografi professionisti, set fotografici costosi o modelli. La piattaforma offre un sistema scalabile e economico per la generazione di immagini di prodotto, visualizzazioni 3D e layout di vetrina personalizzati. Gli utenti possono acquistare pacchetti flessibili (es. 5 foto, 10 foto, 25 foto, ecc.) e personalizzare completamente le loro vetrine con AI-powered tools.

### 🔴 Problema
I proprietari di piccoli e medi e-commerce affrontano diversi ostacoli nel creare vetrine professionali:
- **Costi elevati**: Fotografo professionale, modelli, location, attrezzatura fotografica costano migliaia di euro
- **Tempo**: Lunghi tempi di produzione da concept a foto finali
- **Scalabilità**: Difficile aggiornare frequentemente i cataloghi con nuovi prodotti
- **Qualità incostante**: Dipendenza da competenze esterne e disponibilità di professionisti
- **Localizzazione**: Mancanza di strumenti per adattare le vetrine a mercati locali specifici

### 👥 Target
- **Primario**: Proprietari di PMI e-commerce (small business, artigiani, start-up)
- **Secondario**: Drop-shippier, venditori Shopify/WooCommerce
- **Terziario**: Agenzie di digital marketing che gestiscono più clienti e-commerce
- **Geografico**: Europa (particolarmente Italia, UK, Germania) e Nord America

**Caratteristiche target**:
- Budget ridotto per marketing digitale
- Necessità di aggiornamenti frequenti dei cataloghi
- Scarsa esperienza in fotografia professionale
- Forte orientamento al ROI e alla scalabilità

### 🏆 Competitors
1. **Shopify AI Tools & Polaris** - Integrazione nativa AI in Shopify
2. **Adobe Express + Firefly** - Suite completa di design con AI generativa
3. **Canva Teams** - Soluzione no-code per visual content
4. **Product Photography AI Services** (PixelBin, Cloudinary con AI) - Servizi specifici di foto prodotto
5. **Traditional Freelance Platforms** (Fiverr, Upwork) - Fotografi e designer freelance
6. **DIY Stock Photo Services** (Unsplash, Pexels) + template tools
7. **Emerging Competitors** (Runway, Midjourney for Commerce) - AI puramente generative

### 🎨 Tagline
> **"Vetrine professionali in minuti, non settimane. Powered by AI, progettate per PMI."**

Alternative:
- "Trasforma i tuoi prodotti in arte. Niente budget infinito, niente problemi."
- "Dalla descrizione al prodotto: L'AI genera, il tuo e-commerce vende."

### 🛠️ Tecnologie

#### **Frontend**
- **React.js / Next.js 14** - Framework principale (SSR, performance)
- **TypeScript** - Type safety e developer experience
- **Tailwind CSS** - Styling utility-first, rapidità development
- **Framer Motion** - Animazioni fluid e interattive
- **React Query (TanStack)** - State management lato client, cache management
- **Stripe React Components** - Integrazione pagamenti

#### **Backend**
- **Node.js + Express.js** / **Python + FastAPI** - Server application
- **PostgreSQL** - Database principale (relational data)
- **Redis** - Caching, session management, queue per job processing
- **Celery / Bull** - Background job processing (AI generation async)
- **Docker & Docker Compose** - Containerizzazione

#### **AI & Machine Learning**
- **OpenAI API** (DALL-E 3, GPT-4 Vision) - Generazione immagini e text-to-image
- **Stability AI / Replicate API** - Alternativa generazione immagini
- **Hugging Face** - Modelli open-source per backup/fallback
- **LangChain** - Orchestrazione prompt e chain AI

#### **Infrastructure & DevOps**
- **AWS / Google Cloud** - Hosting principale
- **S3 / Cloud Storage** - Archiviazione immagini generate
- **CloudFlare / Bunny CDN** - Distribuzione immagini globale
- **GitHub Actions** - CI/CD pipeline
- **Sentry** - Error tracking e monitoring
- **DataDog / New Relic** - Performance monitoring

#### **Pagamenti & Compliance**
- **Stripe API** - Gateway pagamenti, subscription management
- **Paddle** - Alternativa per regulatory compliance EU (VAT handling)
- **JWT / Auth0** - Autenticazione e autorizzazione

---

## 2. Benchmarking Competitivo

### Tabella Comparativa

| Feature | Importanza | VisualAI Commerce | Shopify AI | Adobe Express | Canva Teams | Freelancer | Product Photo AI |
|---------|-----------|------------------|-----------|---------------|------------|-----------|-----------------|
| **Generazione immagini AI** | Alta | ✅ Nativa | ✅ Integrata | ✅ Firefly | ⚠️ Limitata | ❌ No | ✅ Specializzata |
| **Modelli template predesignati** | Alta | ✅ 50+ | ✅ Many | ✅ 10000+ | ✅ 10000+ | ❌ Varia | ✅ 30+ |
| **Pacchetti prezzo scalabili** | Alta | ✅ 5,10,25,50 | ✅ Sì | ❌ No (solo abbonamento) | ✅ Sì | ⚠️ No standard | ✅ Sì |
| **Integrazione diretta e-commerce** | Alta | ✅ Shopify, WooCommerce | ✅ Nativa | ❌ No | ❌ No | ❌ No | ⚠️ Limitata |
| **Customizzazione brand/colori** | Alta | ✅ Full | ✅ Sì | ✅ Full | ✅ Full | ✅ Full | ⚠️ Limitata |
| **Generazione descrizioni prodotto** | Media | ✅ AI Generata | ✅ Sì (GPT) | ❌ No | ❌ No | ✅ Manuale | ⚠️ Template |
| **Varianti di prodotto (SKU)** | Media | ✅ Multi-variant | ✅ Nativa | ❌ No | ❌ No | ⚠️ Varia | ❌ No |
| **Editing post-generazione** | Media | ✅ Editor integrato | ✅ Sì | ✅ Advanced | ✅ Advanced | ✅ Manuale | ⚠️ Limited |
| **Supporto lingua multi-locale** | Media | ✅ 25+ lingue | ✅ Sì | ✅ Sì | ✅ Sì | ✅ Sì | ⚠️ Limitato |
| **Analytics e performance tracking** | Media | ✅ Dashboard | ✅ Nativa | ❌ No | ⚠️ Basic | ❌ No | ⚠️ Basic |
| **API pubbliche per integrazione** | Media | ✅ REST/GraphQL | ✅ Sì | ❌ No | ⚠️ Limited | ❌ No | ⚠️ Limited |
| **Supporto clienti (email/chat)** | Media | ✅ 24/7 | ✅ Sì | ✅ Sì | ✅ Sì | ✅ Varia | ✅ Sì |
| **Garanzia qualità immagini** | Alta | ✅ AI Review | ⚠️ Standard | ✅ High | ✅ High | ✅ High | ✅ High |
| **Prezzo entry-level mensile** | Alta | 💰 €29 | 💰€29 | 💰€119 | 💰€120 | 💰€15/progetto | 💰€49 |
| **Rapporto prezzo/valore** | Alta | ✅ Eccellente | ✅ Buono | ⚠️ Alto | ⚠️ Alto | ✅ Variabile | ✅ Buono |

#### **Legenda**
- ✅ = Funzionamento completo/eccellente
- ⚠️ = Funzionamento parziale/discreto
- ❌ = Non disponibile/debole

### 📊 Analisi Strategica

**Posizionamento VisualAI Commerce:**
- **Focus specializzato**: Nichia specifica e-commerce + AI generativa (non generalist come Canva)
- **Pricing vantaggioso**: Entry-level accessibile (€29 vs €119 di Adobe)
- **Velocità go-to-market**: Time-to-value inferiore vs freelancer (minuti vs settimane)
- **Scalabilità economica**: Costo per foto generata inferiore a fotografo professionista
- **Differenziatore**: Integrazione nativa con piattaforme e-commerce + pacchetti pay-as-you-go

**Competitor principals threats:**
- Shopify: Integrazione nativa nel suo ecosistema
- Adobe: Brand consolidato, suite completa
- Freelancer: Qualità umana e personalizzazione

**Competitive advantages VisualAI:**
- Specializzazione verticale (e-commerce only)
- Packaging offerta (foto + descrizioni + layout)
- Curva learning ridottissima (no-code, zero designer skills required)

---

## 3. Analisi dei Requisiti

### 🔵 Contesto Generale

I requisiti di un'applicazione web di e-commerce AI-powered possono essere classificati in tre tipologie fondamentali:

1. **Requisiti Funzionali (FR - Functional Requirements)**: Descrivono le funzionalità che il sistema deve svolgere e i servizi che deve offrire agli utenti
2. **Requisiti Non Funzionali (NFR - Non Functional Requirements)**: Descrivono vincoli operativi, di performance, sicurezza e qualità (imposti da modalità operative, ciclo di vita del prodotto, normative, precedenze esterne)
3. **Requisiti di Dominio (DR - Domain Requirements)**: Descrivono vincoli e regole specifiche del settore (e-commerce, AI, normative sulla privacy, compliance finanziaria)

---

### 📌 Descrizione Progetto: VisualAI Commerce

#### **Panoramica**
VisualAI Commerce è una **piattaforma SaaS web-based** che permette ai proprietari di e-commerce di acquistare pacchetti di generazione di immagini e contenuti via AI. Il flusso principale è:

1. Utente registrato accede al dashboard
2. Seleziona un **pacchetto (5, 10, 25, 50 foto)**
3. Fornisce brief prodotto (descrizione, colori, stile, target audience)
4. **AI genera immagini, descrizioni, metadati**
5. Utente rivede e personalizza i risultati
6. Esporta/scarica o pubblica direttamente su Shopify/WooCommerce
7. Pagamento tramite **Stripe** (one-time per pacchetto)

---

### 🟢 REQUISITI FUNZIONALI (FR)

#### **FR1 - Autenticazione e Profilo Utente**
- L'utente deve potersi **registrare** con email/password o SSO (Google, GitHub)
- L'utente deve potersi **autenticare** con JWT token
- L'utente deve avere un **profilo personale** con dati: nome, email, azienda, paese
- L'utente deve poter **modificare profilo** e immagine avatar
- L'utente deve poter fare **logout** e invalidare sessione
- **Compliance**: GDPR - diritto di cancellazione account e dati associati

#### **FR2 - Gestione Pacchetti e Prezzi**
- Il sistema deve **visualizzare 4 pacchetti principali**:
  - Starter (5 foto, €29)
  - Professional (10 foto, €49)
  - Business (25 foto, €99)
  - Enterprise (50 foto + custom, €199)
- Ogni pacchetto deve mostrare **features incluse**, **time-to-delivery**, supporto
- L'utente deve poter **selezionare un pacchetto**
- Deve essere implementato **pricing dinamico** (sconto per volumi, promo stagionali)
- Sistema di **crediti/tokens** interni per tracking consumo

#### **FR3 - Carrello e Checkout**
- L'utente aggiunge pacchetto al carrello
- Visualizzazione **riepilogo prezzo**, tasse, totale
- Integrazione **Stripe Payment Gateway**:
  - Pagamento carta (Visa, Mastercard, Amex)
  - Apple Pay, Google Pay
  - Wallet digitali
- **Ricevuta email dopo pagamento**
- Salvataggio **storico transazioni** in dashboard utente

#### **FR4 - Creazione Progetto AI**
- L'utente crea un **nuovo progetto** (nome, descrizione)
- **Form wizard multi-step**:
  - Step 1: Caricamento immagini prodotto (jpg, png, max 5MB)
  - Step 2: Brief descrittivo (prodotto, target, stile, colori brand)
  - Step 3: Preferenze AI (numero varianti, background, lighting)
  - Step 4: Revisione e submit
- Validazione dati in tempo reale (regex, file type, size)
- **Salvataggio draft** durante compilation (auto-save ogni 10 sec)

#### **FR5 - Generazione AI Immagini**
- Invio brief al **backend AI queue** (Celery/Bull)
- **Polling status** con indicatore progresso
- Callback webhook quando generazione completa
- Salvataggio immagini generate in **S3/Cloud Storage**
- **Generazione URL firmate temporanei** (token scadenza 24h)
- **Fallback graceful** se AI service non disponibile

#### **FR6 - Editor Post-Generazione**
- **Preview immagini generate** in gallery lightbox
- Strumenti di **editing**:
  - Ritaglio (crop) e rotazione
  - Regolazione luminosità/contrasto/saturazione
  - Aggiunta text overlay, logo, watermark
  - Rinomina e tagging per categorie
- **Batch operations**: selezionare più immagini per applicare filtri
- **Download singolo** o **export ZIP** di tutte le immagini
- Anteprima con **mockup prodotto** (es. maglietta, scatola)

#### **FR7 - Generazione Descrizioni Prodotto**
- **AI genera automaticamente** descrizioni SEO-friendly:
  - Titolo prodotto (max 60 caratteri)
  - Descrizione breve (max 150 caratteri)
  - Descrizione lunga (max 500 caratteri)
  - Tag/keywords (10+)
  - Meta description
- Utente può **editare manualmente** testi generati
- **Template multi-lingua**: generazione in EN, IT, DE, FR, ES
- **SEO scoring** per ogni descrizione (calcolato real-time)

#### **FR8 - Integrazione E-commerce**
- **Connettore Shopify**:
  - OAuth2 per autorizzazione
  - Importazione prodotti dal negozio
  - Mapping automatico varianti (size, colore)
  - **Publish diretto** immagini generate su Shopify (aggiornamento product metadata)
  
- **Connettore WooCommerce**:
  - API authentication (consumer key/secret)
  - Importazione prodotti XML/API
  - Publish con HTTP requests

- **Fallback esportazione CSV**: per piattaforme custom/non supportate

#### **FR9 - Dashboard e Analytics**
- **Overview metrics**:
  - Immagini generate (tot. mese/anno)
  - Crediti consumati vs disponibili
  - Spesa totale, risparmio vs fotografo
  
- **Project history**: lista progetti con date, status, link download
- **Filtri e ricerca**: per data, nome, status, tag
- **Esportazione report** (PDF/CSV)
- **Usage chart**: grafici consumo tempo e risorse

#### **FR10 - Gestione Crediti e Rinnovo**
- **Sistema crediti**:
  - 1 pacchetto = N crediti predefiniti
  - Ogni generazione consuma X crediti
  - Tracking real-time saldo
  
- **Rinnovo automatico**: opzione per sottoscrizione monthly subscription (vs one-time)
- **Notifiche avviso**: quando crediti scendono sotto soglia (20%, 10%, 0%)

---

### 🔴 REQUISITI NON FUNZIONALI (NFR)

#### **NFR1 - Performance**
- **Tempo caricamento pagina**: < 2 secondi (Lighthouse score > 80)
- **Generazione immagine**: < 60 secondi medio (max 120 secondi)
- **Upload file**: supporto fino a 50MB batch, con progress bar real-time
- **Query database**: < 200ms P95 latency
- **API response**: < 500ms per endpoint medio
- **Concorrenza**: supporto minimo 1000 utenti simultanei in prime time

#### **NFR2 - Scalabilità**
- **Horizontal scaling**: architettura stateless per load balancing
- **Database**: supporto crescita da 10K a 1M utenti (sharding strategy)
- **Storage**: S3 con lifecycle policies per archiving immagini vecchie
- **Queue AI**: Celery con multiple workers per parallelize generazioni
- **CDN**: distribuzione globale immagini con edge caching

#### **NFR3 - Disponibilità**
- **Uptime SLA**: 99.5% (circa 4 ore downtime/mese tollerato)
- **Disaster recovery**: RTO < 4 ore, RPO < 1 ora
- **Backup**: database backupato daily, storage geo-redundant
- **Health checks**: monitoring proattivo con alerting
- **Graceful degradation**: se AI service down, mostrare fallback message

#### **NFR4 - Sicurezza**
- **Crittografia trasporto**: HTTPS TLS 1.3, HSTS headers
- **Autenticazione**: JWT con secret rotation monthly
- **Autorizzazione**: RBAC (role-based) - admin/user/viewer
- **Input validation**: sanitization tutti input (XSS protection)
- **SQL injection prevention**: prepared statements, ORM
- **CORS**: restrictive per API endpoints
- **Rate limiting**: 100 richieste/min per API endpoint (burst allowed)
- **Secrets management**: variabili ambiente (AWS Secrets Manager)
- **PCI DSS compliance**: se gestione pagamenti diretta (meglio delegare a Stripe)

#### **NFR5 - Compliance Normative**
- **GDPR (EU)**:
  - Consenso esplicito cookies/tracking
  - Right to erasure (cancellazione account + dati)
  - Data portability (export dati JSON)
  - Privacy policy, terms of service
  - Data processing agreement (DPA) con fornitori (AWS, Stripe, OpenAI)
  
- **CCPA (California)**:
  - Disclosure raccolta dati
  - Right to delete, right to opt-out
  
- **Compliance AI**:
  - Disclosure uso generative AI in product
  - Rispetto copyright/IP nelle immagini generate

#### **NFR6 - Usabilità**
- **Accessibilità**: WCAG 2.1 AA compliance
  - Contrast ratio > 4.5:1
  - Keyboard navigation full support
  - Screen reader compatible
  - Alt text per immagini
  
- **Responsive design**: mobile-first, supporto breakpoints (320px, 768px, 1024px, 1440px)
- **Localizzazione UI**: interfaccia in EN, IT, DE, FR, ES
- **Error messages**: chiari e actionable (non "Error 500", ma "Image upload failed: max 5MB exceeded")

#### **NFR7 - Manutenibilità**
- **Code quality**: test coverage > 80%, linting (ESLint, Prettier)
- **Documentation**: API docs (OpenAPI/Swagger), architecture decision records (ADR)
- **CI/CD**: deployment automatico su push main (GitHub Actions)
- **Monitoring**: ELK stack (Elasticsearch, Logstash, Kibana) per centralized logging
- **Error tracking**: Sentry per anomalia detection

#### **NFR8 - Compatibilità**
- **Browser support**: Chrome, Firefox, Safari, Edge (latest 2 versions)
- **Mobile**: iOS Safari, Android Chrome (responsive)
- **Database**: PostgreSQL 14+
- **Cloud providers**: AWS, Google Cloud, Heroku

---

### 🔵 REQUISITI DI DOMINIO (DR)

#### **DR1 - E-commerce Domain Knowledge**
- **Product taxonomy**: il sistema deve comprendere categorie prodotto (abbigliamento, elettronica, home, ecc.) per personalizzare stile generazione
- **SKU/Variant management**: supporto size, colore, material variants
- **Inventory sync**: potenziale sync con gestione magazzino (per future roadmap)

#### **DR2 - AI/ML Domain**
- **Model selection**: scegliere tra DALL-E 3, Stability AI, Midjourney per qualità/costo
- **Prompt engineering**: template prompt di dominio per consistenza stile
- **Quality gates**: threshold qualità immagini (brightness, contrast, composition scoring)
- **Bias mitigation**: evitare bias nella generazione (diversità rappresentazione)

#### **DR3 - Photography & Visual Design**
- **Product photography best practices**:
  - Lighting optimization (key light, fill light, backlight)
  - Background selezione (white, gradient, contextual)
  - Angle and perspective (front, 3/4, lifestyle)
  
- **Brand consistency**: guideline su color palette, font family, visual language
- **Model release / IP**: gestire licensing immagini generate (commerciale use allowed)

#### **DR4 - Financial/Subscription Domain**
- **Stripe best practices**:
  - Idempotency key per transazioni (evitare duplicati)
  - Webhook handling per payment status (pending, succeeded, failed)
  - Refund policy management
  - Subscription renewal scheduling
  
- **Accounting**: tracking per audit (chi ha generato quante foto, cost per user)
- **Revenue recognition**: compliance ASC 606 (se per compliance finanziaria)

#### **DR5 - Multi-tenancy & Data Isolation**
- **Data segregation**: ogni utente vede solo dati propri (query-level filtering)
- **Storage organization**: S3 bucket organization per customer ID
- **Backups**: restore capability per singolo tenant
- **Audit trail**: logging di chi ha accessato/modificato cosa (GDPR compliance)

#### **DR6 - SaaS Specifici**
- **Onboarding flow**: primo accesso con tutorial, demo project
- **Free trial period**: 7 giorni trial gratuito con 2 crediti omaggio
- **Churn reduction**: email reminder se non usato da 30 giorni
- **Upgrade prompts**: suggerire pacchetto superiore se consumo vicino limite

#### **DR7 - Content Moderation & Legal**
- **Terms of Service**: claire policy su uso legale (no counterfeit, no adult content)
- **Content filtering**: AI per rilevare inappropriate content nelle immagini generate
- **DMCA compliance**: procedure per copyright takedown requests
- **IP ownership**: chiara comunicazione: immagini generate appartengono a chi paga

---

### 📊 Mappa Requisiti per Componenti

| Componente | Requisiti FR Associati | Requisiti NFR | Requisiti DR |
|-----------|----------------------|---------------|-------------|
| **Landing Page** | - | NFR1, NFR6 | DR6 |
| **Auth System** | FR1 | NFR3, NFR4 | NFR4 (GDPR) |
| **Pricing Page** | FR2 | NFR6 | DR6 |
| **Checkout/Pagamento** | FR3 | NFR3, NFR4 | DR4 |
| **Project Creation** | FR4 | NFR1, NFR6 | DR2 |
| **AI Generation** | FR5 | NFR1, NFR2, NFR3 | DR2, DR3 |
| **Image Editor** | FR6 | NFR1, NFR6 | DR3 |
| **Text Generation** | FR7 | NFR1 | DR2, DR3 |
| **E-commerce Connectors** | FR8 | NFR1, NFR4 | DR1 |
| **Dashboard** | FR9 | NFR1, NFR6 | DR5, DR6 |
| **Credit Management** | FR10 | NFR3 | DR4, DR6 |

---

### 🎯 Prioritizzazione Requisiti (MVP vs Future)

#### **MVP (Launch Phase - Essenziale)**
✅ FR1, FR2, FR3, FR4, FR5, FR6, FR7 (base)
✅ NFR1 (performance base), NFR3 (security), NFR6 (usabilità)
✅ DR2, DR3, DR4 (domain core)

#### **Fase 2 (Post-Launch - Important)**
🔄 FR8 (integrazioni e-commerce), FR9 (analytics)
🔄 NFR2 (scalabilità), NFR5 (compliance piena)

#### **Future (Roadmap - Nice-to-Have)**
💡 Subscription ricorrente automatica
💡 API pubblica per integrazioni custom
💡 Mobile app nativa
💡 Video generation feature
💡 3D product visualization

---

## 4. Use Case Diagram e Scenari

### 📊 Diagramma UML dei Casi d'Uso

**Link al file SVG**: [use_case_diagram.svg](./use_case_diagram.svg)

Il diagramma UML rappresenta:

**🎭 Attori Principali:**
- **E-commerce Owner** (proprietario di negozio online) - attore primario
- **Admin** (amministratore piattaforma) - attore secondario
- **Stripe System** (sistema di pagamento esterno) - attore secondario
- **AI Generation Service** (servizio esterno di generazione) - attore secondario

**🎯 Casi d'Uso Principali:**

| Use Case | Attore | Descrizione |
|----------|--------|------------|
| **Register / Login** | E-commerce Owner | Autenticazione e registrazione sulla piattaforma |
| **Select Package** | E-commerce Owner | Scelta del pacchetto fotografico (5, 10, 25, 50 foto) |
| **Upload Product Brief** | E-commerce Owner | Caricamento immagini e descrizione prodotto |
| **Generate Images AI** | E-commerce Owner + AI Service | Generazione automatica immagini via AI |
| **Edit Generated Images** | E-commerce Owner | Editing post-generazione (crop, filtri, testo) |
| **Generate Product Descriptions** | E-commerce Owner + AI Service | Generazione automatica descrizioni SEO |
| **Publish to E-commerce** | E-commerce Owner | Pubblicazione diretta su Shopify/WooCommerce |
| **Process Payment** | E-commerce Owner + Stripe | Elaborazione pagamento tramite Stripe |
| **View Dashboard / Analytics** | E-commerce Owner | Visualizzazione metriche e storico progetti |
| **Manage User Account** | Admin | Gestione account utenti e crediti |
| **Monitor System Health** | Admin | Monitoraggio salute sistema e logs |

**Relazioni UML:**
- **<<include>>**: Generate Images AI include "Upload Product Brief" (dipendenza forte)
- **<<extend>>**: Edit Generated Images extend "Generate Images AI" (scenario opzionale)
- **<<include>>**: Process Payment include "Select Package" (dipendenza forte)

---

## 5. User Stories - Analisi Requisiti Formattata

La seguente sezione riscrive l'intera analisi dei requisiti nel formato **User Story** standard Agile:

### 🟢 USER STORIES - REQUISITI FUNZIONALI

#### **EPIC 1: Autenticazione e Onboarding**

**US1.1 - Registrazione Nuovo Utente**
```
Come proprietario di e-commerce,
voglio registrarmi sulla piattaforma con email e password,
in modo da accedere ai servizi di generazione immagini senza dipendere da terzi.
```
**AC (Acceptance Criteria):**
- [ ] Form registrazione con email/password
- [ ] Validazione email (regex, unicità)
- [ ] Conferma email con token (24h scadenza)
- [ ] Password strength indicator (minimo 8 caratteri, 1 maiuscola, 1 numero)
- [ ] Reindirizzamento a dashboard post-registrazione

**US1.2 - Login con SSO (Google, GitHub)**
```
Come proprietario di e-commerce,
voglio accedere con Google o GitHub,
in modo da non dovermi ricordare ulteriori credenziali.
```
**AC:**
- [ ] Pulsanti login Google e GitHub su login page
- [ ] OAuth2 flow completo
- [ ] Mapping dati profilo da OAuth provider
- [ ] Auto-creazione account se primo accesso

**US1.3 - Modifica Profilo Personale**
```
Come proprietario di e-commerce,
voglio modificare i miei dati (nome, email, azienda, paese, avatar),
in modo da mantenere il profilo sempre aggiornato.
```
**AC:**
- [ ] Form edit profilo con validazione
- [ ] Upload avatar con preview
- [ ] Conferma email se modificata
- [ ] Success notification dopo salvataggio

**US1.4 - Logout e Invalidazione Sessione**
```
Come proprietario di e-commerce,
voglio effettuare logout dalla piattaforma,
in modo da proteggere la mia sessione su dispositivi pubblici.
```
**AC:**
- [ ] Pulsante logout in navbar/menu
- [ ] Invalidazione JWT token
- [ ] Redirect a login page
- [ ] Eliminazione cookie sessione

**US1.5 - Cancellazione Account (GDPR)**
```
Come proprietario di e-commerce,
voglio cancellare permanentemente il mio account e i dati,
in modo da esercitare il mio diritto all'oblio (GDPR Articolo 17).
```
**AC:**
- [ ] Opzione cancellazione account in settings
- [ ] Conferma con password o 2FA
- [ ] Cancellazione dati entro 30 giorni (con backup)
- [ ] Email di conferma cancellazione
- [ ] Impossibilità di ripristinare account dopo 30 giorni

---

#### **EPIC 2: Gestione Pacchetti e Pricing**

**US2.1 - Visualizzazione Pacchetti Disponibili**
```
Come proprietario di e-commerce,
voglio visualizzare i 4 pacchetti disponibili (Starter, Professional, Business, Enterprise),
in modo da scegliere quello più adatto al mio budget.
```
**AC:**
- [ ] Card layout per ogni pacchetto
- [ ] Prezzo chiaramente visibile (€29, €49, €99, €199)
- [ ] Features incluse (numero foto, template, supporto)
- [ ] Time-to-delivery stimato
- [ ] CTA "Choose Package" per ogni card

**US2.2 - Selezione Pacchetto e Aggiunta al Carrello**
```
Come proprietario di e-commerce,
voglio selezionare un pacchetto e aggiungerlo al carrello,
in modo da procedere all'acquisto.
```
**AC:**
- [ ] Click su "Choose Package" aggiunge a carrello
- [ ] Carrello mostra quantità e prezzo
- [ ] Possibilità di modificare quantità
- [ ] Opzione per continuare shopping o checkout

**US2.3 - Pricing Dinamico e Sconti**
```
Come amministratore della piattaforma,
voglio gestire pricing dinamico e applicare sconti per volume,
in modo da massimizzare conversioni e incentivare acquisti ricorrenti.
```
**AC:**
- [ ] Sconto automatico per acquisti > 3 pacchetti (10% discount)
- [ ] Codice coupon gestibile da admin
- [ ] Sconto stagionale configurabile (es. Black Friday)
- [ ] Display sconto nel carrello

**US2.4 - Sistema Crediti Interni**
```
Come proprietario di e-commerce,
voglio visualizzare il mio saldo crediti,
in modo da sapere quante foto posso ancora generare.
```
**AC:**
- [ ] Dashboard widget crediti rimanenti
- [ ] Storico consumo crediti
- [ ] Notifica quando crediti < 20%
- [ ] Opzione per acquistare crediti aggiuntivi

---

#### **EPIC 3: Carrello e Checkout**

**US3.1 - Visualizzazione Carrello Dettagliato**
```
Come proprietario di e-commerce,
voglio visualizzare il riepilogo del carrello con prezzo, tasse e totale,
in modo da verificare i costi prima del pagamento.
```
**AC:**
- [ ] Lista articoli con prezzo unitario
- [ ] Calcolo tasse (IVA per Italia, VAT per EU)
- [ ] Subtotale, tasse, totale
- [ ] Opzione per applicare codice coupon
- [ ] Link per continuare shopping

**US3.2 - Integrazione Stripe Pagamento Carta**
```
Come proprietario di e-commerce,
voglio pagare con carta di credito tramite Stripe,
in modo da completare l'acquisto in modo sicuro.
```
**AC:**
- [ ] Stripe Checkout integrato
- [ ] Supporto Visa, Mastercard, Amex
- [ ] SCA (Strong Customer Authentication) per EU
- [ ] Handling errori pagamento (declinato, scaduto, ecc.)
- [ ] Email ricevuta post-pagamento

**US3.3 - Pagamento con Apple Pay e Google Pay**
```
Come proprietario di e-commerce su mobile,
voglio pagare con Apple Pay o Google Pay,
in modo da completare l'acquisto velocemente da smartphone.
```
**AC:**
- [ ] Pulsante Apple Pay su Safari iOS
- [ ] Pulsante Google Pay su Android Chrome
- [ ] One-click checkout
- [ ] Supporto biometrico (Face ID, fingerprint)

**US3.4 - Storico Transazioni**
```
Come proprietario di e-commerce,
voglio visualizzare lo storico di tutti i pagamenti effettuati,
in modo da tenere traccia della mia spesa e scaricare ricevute.
```
**AC:**
- [ ] Pagina "Transactions History"
- [ ] Tabella con data, importo, metodo, status
- [ ] Filtri per data, importo, status
- [ ] Download ricevuta PDF
- [ ] Export CSV di tutte le transazioni

---

#### **EPIC 4: Creazione Progetto AI**

**US4.1 - Creazione Nuovo Progetto**
```
Come proprietario di e-commerce,
voglio creare un nuovo progetto fornendo nome e descrizione,
in modo da organizzare i miei lavori di generazione immagini.
```
**AC:**
- [ ] Form con campi: nome progetto, descrizione
- [ ] Validazione nome (non vuoto, max 100 char)
- [ ] Descrizione opzionale (max 500 char)
- [ ] Salvataggio automatico come draft
- [ ] Redirect a upload step

**US4.2 - Upload Immagine Prodotto**
```
Come proprietario di e-commerce,
voglio caricare immagini prodotto (jpg, png, max 5MB),
in modo da fornire l'input per la generazione AI.
```
**AC:**
- [ ] Drag & drop zone per file upload
- [ ] Supporto formati: JPG, PNG
- [ ] Limite 5MB per file
- [ ] Progress bar upload
- [ ] Preview immagine caricata
- [ ] Opzione per cancellare e ricaricare

**US4.3 - Form Brief Descrittivo (Multi-Step)**
```
Come proprietario di e-commerce,
voglio compilare un form wizard con descrizione prodotto, colori e stile,
in modo da fornire dettagli al motore AI per la generazione.
```
**AC:**
- [ ] Step 1: Categoria prodotto (dropdown: abbigliamento, elettronica, home)
- [ ] Step 2: Descrizione prodotto (textarea, max 300 char)
- [ ] Step 3: Colori brand (color picker, max 3 colori)
- [ ] Step 4: Stile (radio buttons: minimalista, lussuoso, sportivo, artistico)
- [ ] Step 5: Target audience (checkboxes: uomini, donne, giovani, corporate)
- [ ] Previo su ogni step
- [ ] Salvataggio draft auto ogni 30 sec

**US4.4 - Preferenze AI (Background, Lighting)**
```
Come proprietario di e-commerce,
voglio scegliere background e lighting per le immagini generate,
in modo da ottenere risultati coerenti con il mio brand.
```
**AC:**
- [ ] Background options: bianco, trasparente, sfumato, contextual
- [ ] Lighting: standard, morbido, dramatico, flatlay
- [ ] Numero varianti: 1-5 (radio o slider)
- [ ] Preview mockup con le preferenze

**US4.5 - Revisione e Submission Progetto**
```
Come proprietario di e-commerce,
voglio revisionare tutti i dati del progetto prima di inviarlo,
in modo da evitare errori di generazione.
```
**AC:**
- [ ] Pagina review con tutti i dati
- [ ] Possibilità di editare ogni step
- [ ] Preview complessivo delle impostazioni
- [ ] Pulsante "Generate Images" ben evidente
- [ ] Disclaimer su tempi processing

---

#### **EPIC 5: Generazione AI Immagini**

**US5.1 - Invio Progetto a Coda AI (Background Job)**
```
Come proprietario di e-commerce,
voglio inviare il mio progetto al motore di generazione AI,
in modo da iniziare il processo di creazione immagini.
```
**AC:**
- [ ] Invio dati a Celery/Bull queue
- [ ] Consumo crediti dal bilancio utente
- [ ] Creazione record "generation_job" in DB
- [ ] Status iniziale: "queued"
- [ ] Redirect a pagina progress tracking

**US5.2 - Polling Status con Progress Bar**
```
Come proprietario di e-commerce,
voglio visualizzare il progresso della generazione in real-time,
in modo da sapere quando le immagini saranno pronte.
```
**AC:**
- [ ] Pagina progress con status: "queued", "processing", "completed", "failed"
- [ ] Progress bar che aumenta (0% → 100%)
- [ ] Estimated time remaining
- [ ] Polling ogni 3 secondi da frontend
- [ ] Supporto WebSocket per real-time updates (opzionale)

**US5.3 - Callback Webhook Generazione Completata**
```
Come sistema VisualAI,
voglio ricevere un webhook quando la generazione è completa,
in modo da notificare l'utente istantaneamente.
```
**AC:**
- [ ] Backend riceve webhook da AI service
- [ ] Validazione firma webhook
- [ ] Update status job a "completed"
- [ ] Storage immagini su S3
- [ ] Emit WebSocket event a client
- [ ] Invia email "Immagini Pronte!"

**US5.4 - Download Immagini Generate con URL Firmati**
```
Come proprietario di e-commerce,
voglio scaricare le immagini generate,
in modo da usarle su altri canali se necessario.
```
**AC:**
- [ ] URL firmati S3 (scadenza 24h)
- [ ] Link di download in pagina risultati
- [ ] Supporto singolo download e ZIP batch
- [ ] File naming: "progetto_01.jpg", "progetto_02.jpg"

**US5.5 - Fallback Graceful se AI Service Non Disponibile**
```
Come proprietario di e-commerce,
voglio ricevere un messaggio chiaro se il servizio AI è temporaneamente down,
in modo da capire il problema e riprovare.
```
**AC:**
- [ ] Rilevamento timeout AI service (> 120 sec)
- [ ] Retry automatico 3 volte con backoff exponential
- [ ] Messaggio utente: "AI service temporaneamente indisponibile. Riproveremo..."
- [ ] Refund crediti se fallimento dopo 3 tentativi
- [ ] Email notifica al support team

---

#### **EPIC 6: Editor Post-Generazione**

**US6.1 - Preview Immagini in Gallery Lightbox**
```
Come proprietario di e-commerce,
voglio visualizzare le immagini generate in una gallery lightbox,
in modo da avere una visualizzazione chiara e ingrandita.
```
**AC:**
- [ ] Grid layout 3 colonne (desktop)
- [ ] Click su immagine apre lightbox
- [ ] Navigazione prev/next nel lightbox
- [ ] Zoom funzionalità
- [ ] Chiusura con ESC o click X

**US6.2 - Crop e Rotazione Immagini**
```
Come proprietario di e-commerce,
voglio ritagliare e ruotare le immagini generate,
in modo da perfezionare il framing del prodotto.
```
**AC:**
- [ ] Tool crop con selezione rettangolare
- [ ] Preset aspect ratios (1:1, 4:3, 16:9)
- [ ] Rotazione angoli (90°, 180°, 270°) o freeform
- [ ] Preview prima di applicare
- [ ] Undo/Redo stack

**US6.3 - Regolazione Luminosità, Contrasto, Saturazione**
```
Come proprietario di e-commerce,
voglio regolare luminosità, contrasto e saturazione,
in modo da ottimizzare l'aspetto visivo della foto.
```
**AC:**
- [ ] Slider per brightness (-50 a +50)
- [ ] Slider per contrast (-50 a +50)
- [ ] Slider per saturation (-50 a +50)
- [ ] Preview real-time while dragging
- [ ] Reset a valori default
- [ ] Preset "enhance auto"

**US6.4 - Aggiunta Text Overlay, Logo, Watermark**
```
Come proprietario di e-commerce,
voglio aggiungere testo (titolo, sconto), logo e watermark,
in modo da personalizzare le immagini con branding.
```
**AC:**
- [ ] Tool testo con font selector
- [ ] Colore testo, ombra, trasparenza
- [ ] Posizionamento libero su immagine
- [ ] Upload logo PNG
- [ ] Watermark preimpostato (nome azienda)
- [ ] Layer panel per ordine elementi

**US6.5 - Batch Operations su Più Immagini**
```
Come proprietario di e-commerce,
voglio selezionare più immagini e applicare filtri in batch,
in modo da risparmiare tempo su edits ripetitive.
```
**AC:**
- [ ] Checkbox selezione multipla
- [ ] "Select All" / "Deselect All"
- [ ] Applicazione filtri a selezione
- [ ] Progress durante batch edit
- [ ] Preview prima di applicare

**US6.6 - Download Singolo o ZIP Batch**
```
Come proprietario di e-commerce,
voglio scaricare singole immagini o tutte insieme in ZIP,
in modo da avere flessibilità nel trasferimento file.
```
**AC:**
- [ ] Pulsante "Download" per singola immagine
- [ ] Pulsante "Download All as ZIP"
- [ ] Progress bar durante download
- [ ] Naming convenzione consistente
- [ ] Compressione ZIP senza perdita

---

#### **EPIC 7: Generazione Descrizioni Prodotto**

**US7.1 - AI Genera Descrizioni SEO-Friendly Automaticamente**
```
Come proprietario di e-commerce,
voglio che l'AI generi automaticamente descrizioni SEO,
in modo da non dover scrivere manualmente e risparmiare tempo.
```
**AC:**
- [ ] Generazione: titolo, descrizione breve, descrizione lunga, keywords
- [ ] Titolo: max 60 caratteri
- [ ] Breve: max 150 caratteri
- [ ] Lunga: max 500 caratteri
- [ ] Keywords: 10+ terms relevant
- [ ] SEO score (verde = 80+, giallo = 50-79, rosso = <50)

**US7.2 - Editing Manuale Descrizioni Generate**
```
Come proprietario di e-commerce,
voglio modificare le descrizioni generate,
in modo da adattarle al mio tone of voice e brand.
```
**AC:**
- [ ] Textarea editable per ogni campo descrizione
- [ ] Validazione lunghezza real-time
- [ ] Counter caratteri
- [ ] Preview di come apparirà nel prodotto
- [ ] Bottone save e reset

**US7.3 - Supporto Multi-Lingua Generazione**
```
Come proprietario di e-commerce internazionale,
voglio generare descrizioni in più lingue (EN, IT, DE, FR, ES),
in modo da raggiungere mercati locali.
```
**AC:**
- [ ] Dropdown lingua selezione
- [ ] Generazione indipendente per ogni lingua
- [ ] Tab interface per switching lingue
- [ ] Cache risultati per evitare rigenerazioni

**US7.4 - SEO Scoring Real-Time**
```
Come proprietario di e-commerce,
voglio vedere il punteggio SEO della descrizione in real-time,
in modo da ottimizzarla prima di pubblicare.
```
**AC:**
- [ ] Analisi keywords density
- [ ] Presence di long-tail keywords
- [ ] Lunghezza meta description
- [ ] Readability score
- [ ] Visualizzazione con gauge o bar color-coded

---

#### **EPIC 8: Integrazione E-commerce**

**US8.1 - Connettore Shopify - OAuth2 Autorizzazione**
```
Come proprietario Shopify,
voglio autorizzare VisualAI a accedere al mio store,
in modo da pubblicare immagini direttamente su Shopify.
```
**AC:**
- [ ] Pulsante "Connect Shopify" in settings
- [ ] OAuth2 flow a Shopify partner app
- [ ] Scopes richiesti: read_products, write_products
- [ ] Token storage sicuro in DB (encrypted)
- [ ] Opzione disconnect

**US8.2 - Importazione Prodotti da Shopify**
```
Come proprietario Shopify,
voglio importare la lista prodotti dal mio store,
in modo da scegliere quali foto rigenerare.
```
**AC:**
- [ ] API call a Shopify per GET /products
- [ ] Display lista prodotti in tabella
- [ ] Filtri per collection, vendor
- [ ] Checkbox selezione bulk
- [ ] Import progress tracking

**US8.3 - Mapping Automatico Varianti (Size, Colore)**
```
Come proprietario Shopify,
voglio che le varianti (size, colore) siano mappate automaticamente,
in modo che le immagini generate coprano tutte le SKU.
```
**AC:**
- [ ] Rilevamento automatico opzioni prodotto
- [ ] Mapping colore a immagine (es. "Red" → immagine rossa)
- [ ] Mapping size a layout (es. "Large" → mockup oversize)
- [ ] Override manuale se mapping non perfetto

**US8.4 - Publish Diretto Immagini su Shopify**
```
Come proprietario Shopify,
voglio pubblicare le immagini generate direttamente nel mio store,
in modo da evitare upload manuale.
```
**AC:**
- [ ] Selezione immagini da pubblicare
- [ ] Mapping a product variant
- [ ] Upload immagine a Shopify via API
- [ ] Setting come featured image o gallery
- [ ] Update product metadata (alt text, title)
- [ ] Webhook handling per sync status

**US8.5 - Connettore WooCommerce**
```
Come proprietario WordPress WooCommerce,
voglio collegare il mio store WooCommerce,
in modo da sincronizzare prodotti e immagini.
```
**AC:**
- [ ] Input API credentials (consumer key, secret)
- [ ] Validazione connessione
- [ ] Importazione prodotti da WooCommerce
- [ ] Publish immagini via HTTP POST
- [ ] Gestione errori per server PHP lento

**US8.6 - Export CSV Fallback**
```
Come proprietario di e-commerce su piattaforma non supportata,
voglio esportare immagini e metadati in CSV,
in modo da integrarli manualmente nel mio system.
```
**AC:**
- [ ] CSV export con colonne: product_id, sku, image_url, description
- [ ] ZIP allegato con tutte le immagini
- [ ] Formato importabile da Excel/Shopify

---

#### **EPIC 9: Dashboard e Analytics**

**US9.1 - Overview Metrics Dashboard**
```
Come proprietario di e-commerce,
voglio visualizzare nel dashboard le principali metriche (immagini generate, crediti, spesa),
in modo da monitorare l'utilizzo a colpo d'occhio.
```
**AC:**
- [ ] Card: "Total Images Generated (Month)" con numero e delta %
- [ ] Card: "Credits Remaining" con barra progresso
- [ ] Card: "Total Spent" con importo e risparmio vs fotografo
- [ ] Card: "Saving vs Photographer" con calcolo (foto*€50 vs spesa reale)
- [ ] Refresh button per aggiornare dati

**US9.2 - Project History e Status Tracking**
```
Come proprietario di e-commerce,
voglio visualizzare la lista di tutti i miei progetti,
in modo da gestire e trovare facilmente lavori precedenti.
```
**AC:**
- [ ] Tabella con colonne: nome progetto, data creazione, status, N immagini, azioni
- [ ] Status badges: "draft", "processing", "completed", "published"
- [ ] Possibilità cliccare per view details
- [ ] Link download immagini finali
- [ ] Link share project (public link con scadenza)

**US9.3 - Filtri e Ricerca**
```
Come proprietario di e-commerce,
voglio filtrare progetti per data, nome, status e tag,
in modo da trovare velocemente quello che cerco.
```
**AC:**
- [ ] Search box full-text su nome progetto
- [ ] Filter date range picker
- [ ] Filter status dropdown (multi-select)
- [ ] Filter tag (custom tags gestibili)
- [ ] Salvataggio filter preferiti

**US9.4 - Esportazione Report PDF/CSV**
```
Come proprietario di e-commerce,
voglio esportare un report completo in PDF o CSV,
in modo da avere documentazione per accounting/presentazioni.
```
**AC:**
- [ ] Pulsante "Export Report"
- [ ] Opzioni: PDF (formattato) o CSV (raw)
- [ ] Incluso: periodo, metriche, project list, transazioni
- [ ] Download diretto al browser

**US9.5 - Usage Charts - Consumo Tempo e Risorse**
```
Come proprietario di e-commerce,
voglio visualizzare grafici di consumo crediti nel tempo,
in modo da pianificare budget futuro.
```
**AC:**
- [ ] Chart linea: crediti consumati per settimana (ultimi 3 mesi)
- [ ] Chart barra: numero immagini generate per categoria prodotto
- [ ] Chart pie: distribuzione pacchetti usati
- [ ] Esportazione chart come immagine

---

#### **EPIC 10: Gestione Crediti e Rinnovo**

**US10.1 - Tracking Crediti Real-Time**
```
Come proprietario di e-commerce,
voglio visualizzare il mio saldo crediti e consumo in real-time,
in modo da sapere sempre quante foto posso ancora generare.
```
**AC:**
- [ ] Widget crediti in navbar (sempre visibile)
- [ ] Dettaglio: "250 / 500 crediti rimanenti"
- [ ] Visual progressbar
- [ ] Storico consumo (log trasactions)
- [ ] Aggiornamento live dopo ogni generazione

**US10.2 - Notifiche Avviso Crediti in Esaurimento**
```
Come proprietario di e-commerce,
voglio ricevere notifiche quando i crediti stanno finendo,
in modo da acquistare in tempo prima di rimanere bloccato.
```
**AC:**
- [ ] Email alert a 20% crediti rimanenti
- [ ] Email alert a 10% crediti rimanenti
- [ ] Email alert a 0% crediti (blocco generazioni)
- [ ] In-app toast notification anche su dashboard
- [ ] Link diretto "Buy Credits" nelle notifiche

**US10.3 - Acquisto Crediti Aggiuntivi**
```
Come proprietario di e-commerce,
voglio acquistare crediti aggiuntivi on-demand,
in modo da proseguire generazioni senza aspettare un nuovo periodo.
```
**AC:**
- [ ] Pagina "Buy Additional Credits"
- [ ] Opzioni preset: 50 crediti (€15), 100 crediti (€25), 250 crediti (€50)
- [ ] Custom amount input
- [ ] Checkout rapido (Stripe)
- [ ] Istante credito su account post-pagamento

**US10.4 - Opzione Sottoscrizione Monthly Ricorrente**
```
Come proprietario di e-commerce,
voglio optare per subscription mensile ricorrente,
in modo da non dovermi preoccupare di crediti e avere budget predicibile.
```
**AC:**
- [ ] Toggle "Auto-Renewal" in settings
- [ ] Selezione: "Starter Monthly" (€25), "Professional Monthly" (€45)
- [ ] Billing ciclo su carta registrata
- [ ] Possibilità cancel anytime
- [ ] 30-day trial free per new subscribers
- [ ] Invoice automatica via email

**US10.5 - Rollover Crediti Non Utilizzati**
```
Come proprietario di e-commerce,
voglio sapere se i crediti non utilizzati rollover al prossimo periodo,
in modo da non sprecare l'investimento.
```
**AC:**
- [ ] Policy chiara nella Terms of Service
- [ ] Rollover parziale: 50% crediti unused
- [ ] Scadenza crediti: 180 giorni da acquisto
- [ ] Email reminder prima di scadenza

---

### 🔴 USER STORIES - REQUISITI NON FUNZIONALI

#### **EPIC 1: Performance**

**US NFR 1.1 - Caricamento Pagina Veloce**
```
Come utente della piattaforma,
voglio che le pagine si carichino in meno di 2 secondi,
in modo da avere un'esperienza fluida senza frustrazione.
```
**AC:**
- [ ] Lighthouse score > 80 (performance)
- [ ] First Contentful Paint (FCP) < 1.2 sec
- [ ] Largest Contentful Paint (LCP) < 2.4 sec
- [ ] Cumulative Layout Shift (CLS) < 0.1
- [ ] Time to Interactive (TTI) < 3.5 sec

**US NFR 1.2 - Generazione Immagine Veloce**
```
Come proprietario di e-commerce,
voglio che l'AI generi immagini mediamente in 60 secondi,
in modo da iterare rapidamente senza lunghe attese.
```
**AC:**
- [ ] Tempo medio generazione: 45-60 secondi
- [ ] Max timeout: 120 secondi
- [ ] P95 latency: 90 secondi
- [ ] Progress bar accurato per UX

**US NFR 1.3 - Upload File Veloce con Progress**
```
Come proprietario di e-commerce,
voglio uploadare file fino a 50MB con progress bar in tempo reale,
in modo da monitorare il trasferimento.
```
**AC:**
- [ ] Supporto fino 50MB per singolo file
- [ ] Progress bar accurato durante upload
- [ ] Chunk upload per file grandi
- [ ] Resume capability se connessione cade

**US NFR 1.4 - Query Database Veloce**
```
Come sistema,
voglio che tutte le query database siano < 200ms (P95),
in modo da non creare bottleneck.
```
**AC:**
- [ ] Index su colonne frequentemente queryate (user_id, status)
- [ ] Query optimization e explain plan analysis
- [ ] Caching layer Redis per hot queries
- [ ] Monitoring con DataDog alerts se > 200ms

**US NFR 1.5 - API Response Veloce**
```
Come client frontend,
voglio ricevere risposte API in media < 500ms,
in modo da non bloccare l'interfaccia utente.
```
**AC:**
- [ ] Response time P50: < 300ms
- [ ] Response time P95: < 500ms
- [ ] Response time P99: < 1000ms
- [ ] Monitoring con Sentry/DataDog

---

#### **EPIC 2: Scalabilità**

**US NFR 2.1 - Supporto 1000 Utenti Simultanei**
```
Come platform manager,
voglio che il sistema supporti almeno 1000 utenti contemporanei in prime time,
in modo da gestire picchi di traffico senza degradazione.
```
**AC:**
- [ ] Load test con 1000 concurrent users
- [ ] Response time stabile sotto carico
- [ ] Zero downtime durante spike
- [ ] Auto-scaling trigger a 70% CPU

**US NFR 2.2 - Architettura Stateless**
```
Come developer,
voglio che il backend sia stateless,
in modo da scalare orizzontalmente con load balancer.
```
**AC:**
- [ ] Nessuna sessione in memoria locale
- [ ] Session store su Redis (shared)
- [ ] JWT per auth (stateless)
- [ ] Load balancer round-robin su N istanze

**US NFR 2.3 - Database Scalabile da 10K a 1M Utenti**
```
Come DBA,
voglio che il database supporti crescita da 10K a 1M utenti,
in modo da non avere bottleneck futuro.
```
**AC:**
- [ ] Read replicas setup per query-heavy workload
- [ ] Sharding strategy definita per user table
- [ ] Partition per transaction table (by month)
- [ ] Prepared per future horizontal scaling

**US NFR 2.4 - Storage S3 con Lifecycle Policies**
```
Come platform manager,
voglio che le immagini vecchie vengano archiviate automaticamente,
in modo da ottimizzare costi storage.
```
**AC:**
- [ ] Immagini > 90 giorni → S3 Glacier (storage economico)
- [ ] Immagini > 1 anno → S3 Deep Archive
- [ ] Metadati queryable anche dopo archiving
- [ ] Restore capability se utente richiede

**US NFR 2.5 - Queue AI Parallelizzata**
```
Come system architect,
voglio che il queue AI processing sia parallelizzato su N workers,
in modo da gestire throughput alto.
```
**AC:**
- [ ] Celery con 10+ workers in production
- [ ] Auto-scaling workers basato su queue depth
- [ ] Priorità task (urgent vs normal)
- [ ] Retry logic con exponential backoff

---

#### **EPIC 3: Disponibilità e Disaster Recovery**

**US NFR 3.1 - Uptime SLA 99.5%**
```
Come customer,
voglio che la piattaforma sia disponibile 99.5% del tempo,
in modo da poter contare su di essa per il mio business.
```
**AC:**
- [ ] Tollerato ~4 ore downtime/mese
- [ ] Monitoring 24/7 con alerting
- [ ] SLA agreement in Terms of Service
- [ ] Statuspage.io pubblica per trasparenza

**US NFR 3.2 - Disaster Recovery RTO < 4 ore**
```
Come platform manager,
voglio che in caso di disaster, il recovery sia < 4 ore,
in modo da minimizzare perdita di servizio.
```
**AC:**
- [ ] Database backup daily + hourly snapshots
- [ ] Backup geo-redundant (multi-region)
- [ ] DR playbook documentato
- [ ] Quarterly DR drills

**US NFR 3.3 - RPO < 1 ora**
```
Come data manager,
voglio che la perdita di dati sia < 1 ora in caso di disaster,
in modo da evitare perdita massiva.
```
**AC:**
- [ ] Backup frequente ogni ora
- [ ] Transaction log archiving
- [ ] Point-in-time recovery capability

**US NFR 3.4 - Health Checks e Alerting**
```
Come ops team,
voglio che il sistema monitorizzi la salute continua e alert se problemi,
in modo da essere informato subito di issues.
```
**AC:**
- [ ] Liveness check endpoint /health (database, redis, S3 connectivity)
- [ ] Readiness check per deployment
- [ ] Alerts su Slack/PagerDuty se service down
- [ ] Webhook notification a admin email

**US NFR 3.5 - Graceful Degradation se AI Service Down**
```
Come utente,
voglio che il sistema mi comunichi chiaramente se il servizio AI è down,
in modo da non rimanere confuso dal errore.
```
**AC:**
- [ ] Timeout gestito gracefully (> 120 sec)
- [ ] Messaggio user-friendly: "Servizio temporaneamente non disponibile"
- [ ] Retry automatico in background ogni 30 sec
- [ ] Notifica email quando service riparte

---

#### **EPIC 4: Sicurezza**

**US NFR 4.1 - HTTPS TLS 1.3 Obbligatorio**
```
Come security officer,
voglio che tutto il traffico sia encrypted con TLS 1.3,
in modo da proteggere dati in transito.
```
**AC:**
- [ ] SSL/TLS certificate valido (Let's Encrypt ok)
- [ ] TLS 1.3 forced (reject TLS 1.2 e precedenti)
- [ ] HSTS header con max-age=1 anno
- [ ] Certificate pinning per API critica (opzionale)

**US NFR 4.2 - JWT Token con Rotazione Secret**
```
Come system architect,
voglio che JWT secret sia rotato monthly,
in modo da mitigare risk di compromissione.
```
**AC:**
- [ ] JWT token con expiry 24h
- [ ] Refresh token con expiry 30 giorni
- [ ] Secret rotation monthly (dual-key setup per smooth transition)
- [ ] Old token invalidate dopo rotazione

**US NFR 4.3 - RBAC (Role-Based Access Control)**
```
Come admin,
voglio che gli accessi siano gestiti per ruolo (admin, user, viewer),
in modo da avere control granulare.
```
**AC:**
- [ ] Ruoli: admin, user, viewer, support
- [ ] Permission matrix definita (chi può fare cosa)
- [ ] Middleware enforcement su API
- [ ] Audit logging di chi accede cosa

**US NFR 4.4 - Input Sanitization XSS Protection**
```
Come security team,
voglio che tutti gli input siano sanitizzati,
in modo da prevenire XSS attacks.
```
**AC:**
- [ ] Frontend: sanitize HTML input (DOMPurify)
- [ ] Backend: escape HTML output
- [ ] CSP header per X-Frame-Options
- [ ] Input validation regex su backend

**US NFR 4.5 - SQL Injection Prevention**
```
Come security team,
voglio che le query usino prepared statements,
in modo da prevenire SQL injection.
```
**AC:**
- [ ] ORM o prepared statements per tutte le query
- [ ] Parameterized queries NEVER string concat
- [ ] Code review checklist per DB queries
- [ ] SAST scanning (SonarQube) in CI

**US NFR 4.6 - CORS Restrictive**
```
Come security team,
voglio che CORS policy sia restrictive,
in modo da prevenire unauthorized access da altri origins.
```
**AC:**
- [ ] CORS whitelist solo origins noti (api.visualai.com, app.visualai.com)
- [ ] Credentials allowed ONLY con explicit setting
- [ ] Preflight cache ragionevole

**US NFR 4.7 - Rate Limiting API Endpoints**
```
Come platform manager,
voglio che API endpoints abbiano rate limiting,
in modo da prevenire abuse e DDoS.
```
**AC:**
- [ ] 100 richieste/min per user (logged in)
- [ ] 20 richieste/min per IP (not logged in)
- [ ] Burst allowed per picchi legittimi
- [ ] 429 Too Many Requests response

**US NFR 4.8 - Secrets Management AWS Secrets Manager**
```
Come devops,
voglio che i secrets (API keys, DB password) siano in AWS Secrets Manager,
in modo da evitare leaks in code/config.
```
**AC:**
- [ ] Zero secrets in codebase (env vars only)
- [ ] AWS Secrets Manager integrato in deployment
- [ ] Secret rotation policy per credentials
- [ ] Audit logging accesso secrets

**US NFR 4.9 - PCI DSS Compliance (Stripe)**
```
Come security officer,
voglio che il pagamento sia PCI-DSS compliant,
in modo da proteggere dati carta.
```
**AC:**
- [ ] Stripe Hosted Checkout (no card data touch)
- [ ] No card data storage locale
- [ ] PCI DSS Level 1 per SaaS delegato a Stripe
- [ ] SSL/TLS mandatory per payment pages

---

#### **EPIC 5: Compliance Normative**

**US NFR 5.1 - GDPR Compliance - Consenso Cookies**
```
Come platform manager,
voglio che il consenso ai cookies sia esplicito,
in modo da rispettare GDPR Articolo 7.
```
**AC:**
- [ ] Cookie banner on first visit
- [ ] Granular consent (essential, analytics, marketing)
- [ ] Opt-in (NOT pre-checked)
- [ ] "Manage Preferences" option
- [ ] localStorage consent state

**US NFR 5.2 - Right to Erasure GDPR**
```
Come utente,
voglio poter cancellare il mio account e dati,
in modo da esercitare il right to erasure (Articolo 17).
```
**AC:**
- [ ] Opzione "Delete Account" in settings
- [ ] Cancellazione entro 30 giorni (compliance deadline)
- [ ] Backup retention per compliance audit (dopo 30 giorni delete)
- [ ] Email conferma cancellazione
- [ ] Imposibilità ripristino dopo cancellazione

**US NFR 5.3 - Data Portability GDPR**
```
Come utente,
voglio poter esportare i miei dati in formato JSON,
in modo da esercitare data portability (Articolo 20).
```
**AC:**
- [ ] Pulsante "Export My Data" in settings
- [ ] ZIP con JSON: account info, projects, transactions
- [ ] Download link email (24h expiry)
- [ ] Formato machine-readable (JSON, CSV)

**US NFR 5.4 - Privacy Policy e Terms of Service**
```
Come legal team,
voglio che privacy policy e ToS siano presenti e accettate,
in modo da essere compliant legalmente.
```
**AC:**
- [ ] Privacy Policy url pubblica
- [ ] Terms of Service url pubblica
- [ ] Acceptance during registration (checkbox)
- [ ] Versioning storico per changes
- [ ] Email notifica se policy changes

**US NFR 5.5 - Data Processing Agreement (DPA)**
```
Come enterprise customer,
voglio che vi sia un DPA con VisualAI,
in modo da essere compliant GDPR come data controller.
```
**AC:**
- [ ] DPA template disponibile
- [ ] Signature process (DocuSign o email)
- [ ] Scope: AWS, Stripe, OpenAI come sub-processors
- [ ] Amendment process per sub-processor changes

**US NFR 5.6 - CCPA Compliance (California)**
```
Come US-based customer,
voglio che i miei dati siano protetti sotto CCPA,
in modo da avere rights simili a GDPR.
```
**AC:**
- [ ] CCPA notice on signup
- [ ] Right to delete, right to opt-out
- [ ] Disclosure raccolta dati (purpose, sharing)
- [ ] Do Not Sell My Personal Information option

**US NFR 5.7 - AI Generative Disclosure**
```
Come utente,
voglio sapere chiaramente che le immagini sono generate da AI,
in modo da essere informato transparency.
```
**AC:**
- [ ] Disclosure: "Images generated by AI"
- [ ] Link a info su technology (DALL-E, etc)
- [ ] Copyright/licensing clear communication
- [ ] Non-deceptive use policy

**US NFR 5.8 - Copyright IP Respect**
```
Come piattaforma,
voglio rispecchiare IP rights nelle immagini generate,
in modo da prevenire copyright violations.
```
**AC:**
- [ ] Modelli AI trained su licensed data (DALL-E has safeguards)
- [ ] User license: "Generated images owned by user"
- [ ] Prohibition: no counterfeit, copyright infringement
- [ ] DMCA takedown process in place

---

#### **EPIC 6: Usabilità e Accessibilità**

**US NFR 6.1 - WCAG 2.1 AA Accessibility Compliance**
```
Come utente con disabilità,
voglio che la piattaforma sia accessibile,
in modo da usarla senza barriere.
```
**AC:**
- [ ] Contrast ratio > 4.5:1 per testo normale
- [ ] Heading hierarchy corretto (H1 → H6)
- [ ] Form labels asociate a input (for attribute)
- [ ] Error messages chiari e actionable
- [ ] Color non unica info source (usa anche icons, patterns)

**US NFR 6.2 - Keyboard Navigation Full Support**
```
Come utente che usa solo keyboard,
voglio poter navigare interamente senza mouse,
in modo da usare lo screen reader.
```
**AC:**
- [ ] Tab order logico su tutte le pagine
- [ ] Focus visible outline (not removed)
- [ ] Skip to main content link
- [ ] Modal dialog focus trap
- [ ] Escape key per chiudere dialog

**US NFR 6.3 - Screen Reader Compatible**
```
Come utente non vedente,
voglio che il sito sia compatibile con screen reader,
in modo da accedere al contenuto.
```
**AC:**
- [ ] Alt text su tutte le immagini (non "image_001")
- [ ] ARIA labels per button icone
- [ ] ARIA live region per status updates
- [ ] Semantic HTML (<button>, <nav>, <main>)
- [ ] Testing con NVDA/JAWS screen readers

**US NFR 6.4 - Responsive Design Mobile-First**
```
Come utente mobile,
voglio che il sito sia responsive e usabile su smartphone,
in modo da accedere da qualsiasi dispositivo.
```
**AC:**
- [ ] Mobile-first CSS approach
- [ ] Breakpoints: 320px, 768px, 1024px, 1440px
- [ ] Touch targets > 48px per mobile
- [ ] Viewport meta tag configured
- [ ] Testato su Android Chrome, iOS Safari

**US NFR 6.5 - Localizzazione UI Multi-Lingua**
```
Come utente non anglofono,
voglio che l'interfaccia sia disponibile in più lingue,
in modo da usare la mia lingua madre.
```
**AC:**
- [ ] Lingue supportate: EN, IT, DE, FR, ES
- [ ] Language selector in header/settings
- [ ] Storage preference in localStorage
- [ ] Automatic detection da browser Accept-Language (optional)
- [ ] String translations externalized (i18n library)

**US NFR 6.6 - Error Messages Chiari e Actionable**
```
Come utente,
voglio messaggi errore chiari che mi aiutino a risolvere,
in modo da non restare frustrato.
```
**AC:**
- [ ] Niente errori generici "Error 500"
- [ ] Errori specifici: "Image upload failed: File size exceeds 5MB. Maximum size is 5MB."
- [ ] Suggerimenti azione: "Click here to select a smaller file"
- [ ] Errori in rosso, warning in giallo, success in verde
- [ ] Posizionamento chiaro vicino al campo errore

---

#### **EPIC 7: Manutenibilità**

**US NFR 7.1 - Code Quality Test Coverage > 80%**
```
Come sviluppatore,
voglio che il codebase abbia test coverage > 80%,
in modo da avere confidenza in refactoring.
```
**AC:**
- [ ] Unit test coverage > 80% (Jest, Mocha)
- [ ] Integration test per API endpoints
- [ ] E2E test per user flows critici (Cypress, Playwright)
- [ ] Coverage report in CI (fail if < 80%)

**US NFR 7.2 - Linting e Code Style Consistent**
```
Come sviluppatore,
voglio che il code style sia automaticamente checked,
in modo da avere consistency nel team.
```
**AC:**
- [ ] ESLint configurato per JavaScript/TypeScript
- [ ] Prettier per auto-formatting
- [ ] Pre-commit hooks per check prima del commit
- [ ] CI fail se linting errors

**US NFR 7.3 - API Documentation OpenAPI/Swagger**
```
Come integrator,
voglio che le API siano documentate con Swagger,
in modo da integrarsi facilmente.
```
**AC:**
- [ ] OpenAPI spec completo per tutti gli endpoint
- [ ] Swagger UI pubblica su /api/docs
- [ ] Schema models documentati
- [ ] Example requests/responses
- [ ] Authentication documented

**US NFR 7.4 - Architecture Decision Records (ADR)**
```
Come architect,
voglio che le decisioni architetturali siano documentate,
in modo da capire il "perché" dietro le scelte.
```
**AC:**
- [ ] ADR folder in repo (/docs/adr)
- [ ] Template ADR standardizzato
- [ ] ADR per decisioni importanti (database choice, auth strategy)
- [ ] Acceptance per ADR prima di implementation

**US NFR 7.5 - CI/CD Automatizzato GitHub Actions**
```
Come devops,
voglio che deployment sia automatizzato via GitHub Actions,
in modo da evitare errori manuali.
```
**AC:**
- [ ] CI pipeline: lint → test → build su ogni PR
- [ ] CD pipeline: deploy a staging su merge main
- [ ] Manual approval per production deployment
- [ ] Rollback capability se deployment fails

**US NFR 7.6 - Centralized Logging ELK Stack**
```
Come ops,
voglio che i logs siano centralizzati in ELK,
in modo da debugging facilmente.
```
**AC:**
- [ ] All logs shipped da backend a Elasticsearch
- [ ] Kibana dashboard per log search
- [ ] Log retention policy (30 giorni default, archive dopo)
- [ ] Alert su Slack se error rate > threshold

**US NFR 7.7 - Error Tracking Sentry**
```
Come developer,
voglio che gli errori siano tracciati automaticamente in Sentry,
in modo da notificarmi di anomalie.
```
**AC:**
- [ ] Sentry integrato in backend (Sentry SDK)
- [ ] Sentry integrato in frontend (React integration)
- [ ] Alerts su Slack per critical errors
- [ ] Source map upload per stack trace readability

---

#### **EPIC 8: Compatibilità**

**US NFR 8.1 - Browser Support Latest 2 Versions**
```
Come QA,
voglio che il sito sia compatibile con i 2 ultimi browser versions,
in modo da supportare utenti moderni.
```
**AC:**
- [ ] Chrome latest 2 versions
- [ ] Firefox latest 2 versions
- [ ] Safari latest 2 versions
- [ ] Edge latest 2 versions
- [ ] Polyfill per ES6+ features se necessario

**US NFR 8.2 - Mobile iOS Safari + Android Chrome**
```
Come QA,
voglio che il sito sia testato su iOS Safari e Android Chrome,
in modo da supportare mobile users.
```
**AC:**
- [ ] Tested su iOS 15+ (Safari)
- [ ] Tested su Android 10+ (Chrome)
- [ ] Touch gestures working (swipe, pinch-zoom)
- [ ] Performance acceptable su 4G

**US NFR 8.3 - Database PostgreSQL 14+**
```
Come DBA,
voglio usare PostgreSQL 14+,
in modo da avere latest features e security patches.
```
**AC:**
- [ ] Minimum version PostgreSQL 14.0
- [ ] JSON/JSONB support leveraged
- [ ] Full-text search utilizziato
- [ ] Upgrade path defined per future versions

**US NFR 8.4 - Multi-Cloud Support AWS / GCP**
```
Come architect,
voglio che il sistema sia cloud-agnostic,
in modo da evitare vendor lock-in.
```
**AC:**
- [ ] Docker containers per easy deployment
- [ ] Infrastructure as Code (Terraform)
- [ ] AWS deployment tested (EC2, RDS, S3)
- [ ] GCP deployment tested (GKE, Cloud SQL, GCS)
- [ ] Same functionality su entrambi clouds

---

### 🔵 USER STORIES - REQUISITI DI DOMINIO

#### **EPIC 1: E-commerce Domain**

**US DR 1.1 - Product Taxonomy Support**
```
Come proprietario e-commerce,
voglio che il sistema capisca categorie prodotto (abbigliamento, elettronica, home),
in modo da personalizzare stile generazione per categoria.
```
**AC:**
- [ ] Dropdown categoria prodotto durante brief
- [ ] Stile default per categoria (abbigliamento: lifestyle, elettronica: minimalist)
- [ ] Possibilità override manuale
- [ ] Database categoria mapping a prompt template

**US DR 1.2 - SKU/Variant Management**
```
Come proprietario e-commerce,
voglio gestire multiple varianti (size, colore, material),
in modo che ogni SKU abbia immagini coerenti.
```
**AC:**
- [ ] Upload multiple immagini per SKU
- [ ] Mapping automatico variante a immagine generated
- [ ] Varianti visualizzate in editor
- [ ] Publish batch per tutte le varianti

**US DR 1.3 - Inventory Sync Future Roadmap**
```
Come proprietario e-commerce,
voglio che (in futuro) il sistema synchi con inventory management,
in modo da generare foto solo per prodotti in stock.
```
**AC (Future):**
- [ ] API integration con Shopify inventory
- [ ] Auto-update inventory status su generazione
- [ ] Out-of-stock flagging

---

#### **EPIC 2: AI/ML Domain**

**US DR 2.1 - Model Selection DALL-E vs Stability vs Midjourney**
```
Come product manager,
voglio poter selezionare il modello AI (DALL-E 3, Stability, Midjourney),
in modo da bilanciare quality vs cost.
```
**AC:**
- [ ] Config backend per model selection
- [ ] DALL-E 3 default (quality high, cost medium)
- [ ] Stability AI fallback (cost lower, quality decent)
- [ ] Midjourney for premium tier (quality highest, cost highest)
- [ ] User preference saveable

**US DR 2.2 - Prompt Engineering Template Domain**
```
Come AI engineer,
voglio template prompt ottimizzati per product photography,
in modo da avere risultati consistenti.
```
**AC:**
- [ ] Prompt template standard per categoria (abbigliamento, elettronica)
- [ ] Template include: product description, background, lighting, style
- [ ] Dynamic injection dati da user input
- [ ] A/B testing diversi template

**US DR 2.3 - Quality Gates Image Scoring**
```
Come quality manager,
voglio che le immagini generated siano scored per qualità,
in modo da filtrare results low-quality.
```
**AC:**
- [ ] Brightness check (not too dark, not blown-out)
- [ ] Contrast analysis
- [ ] Composition scoring (product in frame, not cut off)
- [ ] OCR su testo (se presente, legibile)
- [ ] Reject threshold configurabile

**US DR 2.4 - Bias Mitigation**
```
Come ethics team,
voglio che le immagini generate non abbiano bias,
in modo da rappresentare diversità.
```
**AC:**
- [ ] No NSFW content filtering
- [ ] Diverse representation nello style (not always Eurocentric)
- [ ] Bias detection model (optional)
- [ ] Report su potential bias issues

---

#### **EPIC 3: Photography & Visual Design**

**US DR 3.1 - Product Photography Best Practices**
```
Come photography director,
voglio che le immagini seguano best practice fotografia prodotto,
in modo da ottenere risultati professionali.
```
**AC:**
- [ ] Lighting options: key light, fill light, backlight selectable
- [ ] Background options: white, gradient, contextual scene
- [ ] Angle/perspective: front view, 3/4 view, lifestyle shot
- [ ] Shadow handling: drop shadow, no shadow, soft shadow

**US DR 3.2 - Brand Consistency Guideline**
```
Come brand manager,
voglio che le immagini rispettino la brand guideline,
in modo da avere coerenza visiva.
```
**AC:**
- [ ] Color palette da scegliere durante brief
- [ ] Font family preference (serif, sans-serif)
- [ ] Visual language (minimalist, luxury, playful)
- [ ] Logo positioning rules
- [ ] Save brand guideline per reuse progetti futuri

**US DR 3.3 - Model Release e IP Licensing**
```
Come legal team,
voglio che sia chiaro il licensing su immagini generate,
in modo da evitare IP issues.
```
**AC:**
- [ ] ToS chiaro: immagini generate owned by user
- [ ] Commerciale use allowed
- [ ] No resale delle immagini (no stock photo business)
- [ ] Attribution not required (ma appreciated)

---

#### **EPIC 4: Financial/Subscription Domain**

**US DR 4.1 - Stripe Idempotency Key Handling**
```
Come payment engineer,
voglio che il sistema usi idempotency key per Stripe,
in modo da evitare duplicate charges.
```
**AC:**
- [ ] Idempotency key generated per transaction
- [ ] Stored in DB per retry scenario
- [ ] Same key = same result (idempotent)

**US DR 4.2 - Webhook Payment Status Handling**
```
Come backend developer,
voglio gestire webhook Stripe per payment status updates,
in modo da sincronizzare order status.
```
**AC:**
- [ ] Webhook endpoint /webhooks/stripe
- [ ] Signature verification (Stripe secret)
- [ ] Event handling: payment_intent.succeeded, payment_intent.payment_failed
- [ ] DB update order status
- [ ] Email user su status change

**US DR 4.3 - Refund Policy Management**
```
Come customer support,
voglio gestire refunds per customer,
in modo da fornire buon servizio.
```
**AC:**
- [ ] Refund policy: 30 giorni money-back guarantee
- [ ] Admin panel per process refund (Stripe + DB)
- [ ] Email notification customer
- [ ] Crediti restored se generazione failed

**US DR 4.4 - Subscription Renewal Scheduling**
```
Come subscription engineer,
voglio che Stripe gestisca auto-renewal della subscription,
in modo da avere recurring revenue.
```
**AC:**
- [ ] Stripe subscription setup (monthly)
- [ ] Auto-renewal su billing date
- [ ] Email reminder 7 giorni prima renewal
- [ ] Easy cancel anytime

**US DR 4.5 - Accounting Audit Trail**
```
Come accountant,
voglio che il sistema registri audit trail per ogni transazione,
in modo da avere compliance finanziaria.
```
**AC:**
- [ ] Transazione log: user_id, amount, type, status, timestamp
- [ ] Immutable (no edit, only append)
- [ ] Export audit report monthly
- [ ] Compliance con ASC 606 revenue recognition

---

#### **EPIC 5: Multi-Tenancy & Data Isolation**

**US DR 5.1 - Data Segregation Query-Level**
```
Come security architect,
voglio che ogni utente veda solo i suoi dati,
in modo da garantire privacy.
```
**AC:**
- [ ] WHERE clause sempre include user_id filtering
- [ ] No query che ritorna multi-user data
- [ ] Middleware enforcement on API
- [ ] Test pentest per data leakage

**US DR 5.2 - Storage Organization per Customer ID**
```
Come DBA,
voglio che S3 bucket sia organizzato per customer ID,
in modo da isolare data.
```
**AC:**
- [ ] S3 path: /customer/{customer_id}/images/
- [ ] Bucket policy restrict access a own customer prefix
- [ ] Cross-customer access impossible
- [ ] Bucket versioning per data recovery

**US DR 5.3 - Restore Capability per Tenant**
```
Come support engineer,
voglio poter fare restore di singolo tenant da backup,
in modo da gestire data recovery requests.
```
**AC:**
- [ ] Backup strategy: daily snapshots per tenant
- [ ] PITR (Point In Time Recovery) supported
- [ ] Restore process tested quarterly
- [ ] RTO < 4 hours

**US DR 5.4 - Audit Trail Data Access**
```
Come compliance officer,
voglio audit logging di chi ha accessato/modificato cosa,
in modo da GDPR compliance.
```
**AC:**
- [ ] Immutable audit log per ogni data change
- [ ] Campi: user_id, timestamp, action, resource, old_value, new_value
- [ ] Retention 7 anni per audit
- [ ] Export su richiesta

---

#### **EPIC 6: SaaS Specifici**

**US DR 6.1 - Onboarding Flow con Tutorial**
```
Come UX designer,
voglio che first-time user abbia guided onboarding,
in modo da ridurre learning curve.
```
**AC:**
- [ ] Welcome screen con value proposition
- [ ] Step-by-step tutorial (5 step)
- [ ] Demo project pre-created
- [ ] Skip option available
- [ ] Video tutorial links

**US DR 6.2 - Free Trial 7 Giorni**
```
Come product manager,
voglio offrire 7 giorni free trial,
in modo da convertire users.
```
**AC:**
- [ ] Auto-enable free trial su sign up
- [ ] 2 crediti omaggio nel trial
- [ ] Email reminder 2 giorni prima expiry
- [ ] Option convert to paid seamless

**US DR 6.3 - Churn Reduction Email Reminder**
```
Come retention manager,
voglio email reminder se user non usato per 30 giorni,
in modo da re-engage.
```
**AC:**
- [ ] Cron job daily check last_login > 30 giorni
- [ ] Email: "We miss you! Here's 1 free credit" + link back
- [ ] A/B test subject line
- [ ] Track email open rate

**US DR 6.4 - Upgrade Prompts suggerimento pacchetto**
```
Come product manager,
voglio suggerire upgrade se crediti quasi esauriti,
in modo da aumentare ARPU.
```
**AC:**
- [ ] Trigger: crediti < 20% pacchetto
- [ ] Modal: "Ready for more? Upgrade to Professional"
- [ ] Show savings vs current
- [ ] One-click upgrade

---

#### **EPIC 7: Content Moderation & Legal**

**US DR 7.1 - Terms of Service Compliance**
```
Come legal team,
voglio che ToS siano chiari su usi legali,
in modo da proteggere piattaforma.
```
**AC:**
- [ ] ToS public su /terms
- [ ] Proibizioni: counterfeit, copyright infringement, NSFW
- [ ] Violators: account suspension, legal action
- [ ] Acceptance required at signup

**US DR 7.2 - Content Filtering Inappropriate Content**
```
Come moderation team,
voglio che le immagini generate siano filtrate per inappropriate content,
in modo da mantenere platform safety.
```
**AC:**
- [ ] NSFW detection model (OpenAI or alternative)
- [ ] Flag images con probability > 80%
- [ ] Manual review per flagged images
- [ ] Auto-delete if confirmed inappropriate

**US DR 7.3 - DMCA Compliance Takedown Process**
```
Come legal team,
voglio avere processo per DMCA takedown requests,
in modo da rispettare IP rights terzi.
```
**AC:**
- [ ] DMCA notice form on website
- [ ] Email contact per takedown requests
- [ ] Response time < 48 ore
- [ ] Removal di infringing content
- [ ] Counter-notice process available

**US DR 7.4 - IP Ownership Clear Communication**
```
Come legal team,
voglio che sia chiaro chi possiede le immagini generate,
in modo da evitare dispute.
```
**AC:**
- [ ] Policy: "Generated images owned by user who created them"
- [ ] VisualAI non claiming ownership
- [ ] User can commercial use, resell not allowed
- [ ] Visible in Terms of Service

---

## 📚 Riferimenti

- SWEBOK Guide - Requirements Engineering
- Sommerville, I. (2016). *Software Engineering* (10th ed.)
- Agile Manifesto - User Story Format
- OpenAI API Documentation
- Stripe API Reference
- GDPR Official Guidelines
- WCAG 2.1 Accessibility Standard

---

## ✍️ Note di Sviluppo

**Questo documento funge da base per:**
- Sprint planning e backlog prioritization
- User story acceptance criteria
- Definition of Done per task
- Quality assurance test cases

**Prossimi step:**
1. Epic → Sprint assignment
2. Story pointing con Fibonacci scale
3. Detailed test scenarios per US
4. Mockup UI/UX per ogni user flow
5. API contract definition per backend

---

**Versione**: 2.0 (Updated with Use Cases & User Stories)  
**Data**: Dicembre 2025  
**Autore**: Development Team  
**Status**: Ready for Sprint Planning

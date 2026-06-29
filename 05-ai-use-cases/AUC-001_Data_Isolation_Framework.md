# EU-112™ AUC-001
## AI Use Case & Data Isolation Framework — AiVenture SRL

- **Company Name:** AiVenture SRL
- **Framework Specification:** EU-112™ Operational Governance System (OGS)
- **Scope:** EU AI Act Compliance (Data Sovereignty & Privacy Safeguards)
- **Status:** APPROVED BASELINE

---

### 1. Scopul Utilizării AI
Sistemele AI identificate în registrul `AI-000` (ChatGPT, Gemini, Claude, DeepSeek) sunt utilizate exclusiv pentru optimizarea fluxurilor interne de lucru, analiză tehnică de arhitectură, documentație și generare de cod experimental.

### 2. Politica de Izolare a Datelor (Ce vede controlul)
Pentru a asigura conformitatea completă cu reglementările de confidențialitate și transparență:
* **Interdicția de Antrenare:** Toate interfețele utilizate sunt configurate structural pentru a **refuza (opt-out)** utilizarea prompturilor sau a documentelor încărcate în scopul antrenării viitoare a modelelor publice ale furnizorilor (OpenAI, Google, Anthropic).
* **Fără Date Personale (PII):** Este strict interzisă introducerea datelor cu caracter personal sensibile în ferestrele de chat ale modelelor de uz general. Datele sunt anonimizate complet înainte de procesare.
* **Arhitectură Edge Sigură:** Componentele viitoare din Cloudflare Workers AI acționează ca un releu de execuție contextuală (Inference Replay), unde datele tranzitează memoria volatilă de la Edge, fără stocare persistentă neautorizată.

### 3. Regula de Aur (Human-in-the-Loop)
Niciun raport tehnic, livrabil de conformitate sau cod generat de AI nu este publicat sau trimis către clienți fără revizuire, validare și aprobare umană, respectând pragul operațional de 85% automatizare și 15% control strategic uman.

---

### 4. Focus Inovație: B2B Economic Twins™ Fiscal DB
* **Definiție Operativă:** Acest modul rulează o arhitectură de analiză semantică peste baza de date fiscală oficială a firmelor din România (sursa: Ministerul de Finanțe / ANAF / ONRC)[cite: 1].
* **Scopul Processing-ului:** Identificarea și maparea de "Gemeni Economici" (firme cu indicatori fiscali, coduri CAEN și modele de activitate similare cu clienții ideali ai unei companii) pentru optimizarea strategiei de piață B2B[cite: 1].
* **Statut de Conformitate:** Sistemul prelucrează exclusiv date publice, agregate, aparținând persoanelor juridice. Nu se realizează profilări comportamentale asupra persoanelor fizice, menținând algoritmul în clasa de Risc Minim conform EU AI Act[cite: 1].
* **Data Origin & Integrity Baseline:** Procesul de mapare pleacă structural de la fișierul de date brut `od_firme.csv` extras oficial de la Ministerul de Finanțe[cite: 1]. Pentru a garanta trasabilitatea sursei și pentru a dovedi că algoritmul nu folosește surse de date neautorizate, fișierul original este amprentat criptografic și înregistrat în `09-evidence-register` sub ID-ul `EV-008`[cite: 1].
* **Verificare Criptografică (Provenance Layer):**
  * **Canonical SHA-256 Hash:** `0716ca58759f65f4760259efe71e99eecf5d22d7471ce4ef7107b49a86c0a077`[cite: 1]
  * **OpenTimestamps Proof File Reference:** `od_firme.csv.ots`[cite: 1]

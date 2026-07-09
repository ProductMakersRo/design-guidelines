# Product Makers: design style

Două fișiere, cu care poți genera vizualuri care arată "a Product Makers" în orice AI tool.

## Cele două fișiere

- **[DESIGN.md](DESIGN.md)** este briefingul pe care îl citesc și oamenii, și
  AI-ul. Culori, tipografie, umbre, componente și regulile de "așa da / așa nu",
  în formatul [Stitch DESIGN.md](https://stitch.withgoogle.com/docs/design-md/format/):
  un bloc YAML cu token-uri (partea citită de mașină) urmat de șase secțiuni
  fixe. 
  
- **[design.json](design.json)** e perechea lui, în format pentru tools.
  Ține ce nu încape în YAML: rampe tonale de 8 trepte pentru fiecare culoare,
  token-uri de umbre și mișcare, fragmente de cod complete pentru componente
  (buton, tag, card) și tot "narativul" (North Star, reguli, do's & don'ts).
 

Regula simplă: **DESIGN.md merge în orice unealtă cu AI; design.json e pentru
uneltele care știu să-l citească** (panoul impeccable din Claude Code, un sistem
de token-uri, un import automat etc.).

---

## Cum le folosești

### 1. În Claude Code

Claude Code citește `DESIGN.md` din rădăcina proiectului ca și context, iar cu
skill-ul impeccable folosește și `design.json`.

1. Adu cele două fișiere în proiectul tău. `DESIGN.md` stă în rădăcină (lângă
   `package.json`), iar `design.json` la `.impeccable/design.json`. Din terminal:
   ```bash
   curl -O https://raw.githubusercontent.com/ProductMakersRo/design-guidelines/main/DESIGN.md
   mkdir -p .impeccable
   curl -o .impeccable/design.json https://raw.githubusercontent.com/ProductMakersRo/design-guidelines/main/design.json
   ```
2. Cere-i lui Claude Code ce ai nevoie. Va citi `DESIGN.md` și va respecta
   regulile:
   > "Construiește o secțiune de hero pentru pagina de eveniment, respectând DESIGN.md."
3. Ca să fii sigur că îl citește de fiecare dată, adaugă o linie în `CLAUDE.md`
   sau `AGENTS.md`: `Respectă DESIGN.md pentru orice interfață.`
4. Opțional, cu skill-ul impeccable activ, panoul live randează componentele
   reale din `design.json` (butonul portocaliu, tag-ul înclinat) în loc de
   aproximări generice.

### 2. În Claude pe web / chat (claude.ai)

1. Descarcă `DESIGN.md` (pe GitHub: "Download raw file", sau
   [link direct](https://raw.githubusercontent.com/ProductMakersRo/design-guidelines/main/DESIGN.md)).
2. Într-o conversație nouă, atașează fișierul (click pe iconița cu agrafa) sau dă-i drag&drop în chat de la început.
3. Cere output-ul și punctează că trebuie să urmeze sistemul:
   > "Pe baza acestui DESIGN.md, scrie textul și structura pentru un banner de
   > eveniment. Sentence case, fără em dash, un singur CTA portocaliu, un tag
   > înclinat deasupra titlului aliniat la stânga."
4. Dacă vrei și cod, cere direct componenta: "Dă-mi HTML plus CSS pentru un card
   de workshop, conform sistemului."

### 3. În Claude Design / Artifacts

Când ceri un vizual (Artifact) direct în Claude:

1. Atașează `DESIGN.md` la conversație, ca mai sus.
2. Cere un Artifact și trimite explicit la reguli:
   > "Fă un Artifact HTML: o pagină de landing pentru un workshop, folosind exact
   > culorile, tipografia și componentele din DESIGN.md. Albastru #3f3fff e
   > identitate, portocaliu #ff5500 e acțiune, un singur CTA."
3. Pentru fidelitate maximă, dă-i și `design.json`. Conține fragmentele CSS gata
   făcute pentru buton, tag și card, pe care le poate copia unu la unu.

### 4. În alte unelte

- **Google Stitch:** `DESIGN.md` e chiar în formatul lui Stitch. Importă-l ca
  atare; linterul îi validează token-urile și panoul randează componentele.
- **Cursor / Copilot / Windsurf:** ține `DESIGN.md` în repo (sau adaugă-l la
  "rules" / context). Uneltele îl citesc automat ca ghid pentru orice UI.
- **ChatGPT sau alt LLM:** lipește `DESIGN.md` la începutul conversației, apoi
  cere vizualul.
- **Figma și unelte de design:** folosește `DESIGN.md` ca brief de referință;
  token-urile și rampele tonale din `design.json` pot semăna o bibliotecă de
  culori și variabile.

Indiferent de unealtă, pasul cheie e același: **dă-i întâi DESIGN.md, apoi cere
output-ul**, și trimite la regulile cu nume ("The Two-Paint Rule", "The
No-Colored-Text Rule").

---

## Sistemul, într-o frază

Un fanzin bine cules, făcut de makeri: tipografie neagră pe hârtie caldă, două
culori-vopsea (albastru `#3f3fff` este identitate, portocaliu `#ff5500` este
acțiune) și semnătura casei, etichetele înclinate tip marker. Structura vine din
linii de 1px, nu din umbre. Trebuie să pară făcut de un om, nu generat.

## Ține-le sincronizate

Sursa de adevăr e aplicația site-ului, nu acest repo. Dacă se schimbă ceva,
actualizează întâi `DESIGN.md`, apoi regenerează `design.json`, ca cele două să
nu se depărteze unul de altul.

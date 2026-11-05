# ML Prosjektmal

Kort beskrivelse av hva maskinlæringsprosjektet eller eksperimentet handler om.

---

## Mappestruktur

- `data/raw/` — Rådata (skal aldri endres manuelt, uforanderlig)
- `data/processed/` — Ferdig renset og klargjort data
- `data/external/` — Eksterne datakilder eller oppslagsverk
- `notebooks/` — Jupyter Notebooks for utforskning (EDA) og prototyping
- `src/` — Kildemoduler og gjenbrukbar kode:
  - `data.py` — Skript/funksjoner for lasting, rensing og splitting
  - `features.py` — Feature engineering og transformasjoner
  - `model.py` — Trening, evaluering og prediksjon
- `models/` — Lagrede modellfiler (`.pkl`, `.pt`, `.h5`)
- `reports/` — Genererte figurer, grafer og resultater
- `requirements.txt` — Oversikt over prosjektets avhengigheter
- `main.py` — Hovedskript for å kjøre hele pipelinen fra start til slutt

---

## Oppsett og Fremgangsmåte

### 1. Opprett og aktiver virtuelt miljø

Åpne terminalen i prosjektmappen og kjør:

```bash
python -m venv .venv


Aktiver miljøet:

Windows (PowerShell): .venv\Scripts\Activate


2. Velg Python-interpreter i VS Code
Åpne Command Palette (Ctrl + Shift + P / Cmd + Shift + P).

Skriv Python: Select Interpreter.

Velg .venv-miljøet du nettopp opprettet.

3. Installer avhengigheter
For å installere standardpakker for dataanalyse og maskinlæring (pandas, numpy, scikit-learn, matplotlib, seaborn, jupyter),
 kjør:

Bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

Alternativt, hvis requirements.txt inneholder pakkene:
Bash
pip install -r requirements.txt


4. Oppdater requirements.txt
Hver gang du installerer nye biblioteker underveis i prosjektet, oppdaterer du listen ved å kjøre:

Bash
pip freeze > requirements.txt


Arbeidsflyt for Kode og Data
Behold rådata intakt: Rør aldri filene i data/raw/. Lagre alt ferdig renset data i data/processed/.

Eksperimenter i Notebooks: Bruk notebooks/ til utforskende dataanalyse (EDA) og testing av filtre eller logikk.

Moduliser koden: Når du har funnet logikken som fungerer i Jupyter, flytter du den over til rene funksjoner i Python-skript under src/ (f.eks. src/data.py).

Gjenbruk: Importer funksjonene fra src/ tilbake til notebooken eller kjør dem via main.py.
# 9SENS-micro

**Darmowy, wielopersonowy framework analizy biznesowej** — podejmuj lepsze decyzje GO/NO-GO w 3-6 godzin.

---

## Co to jest 9SENS-micro?

9SENS-micro to uproszczona wersja frameworka 9SENS, która wykorzystuje **3 persony AI** do analizy Twojego pomysłu biznesowego z różnych perspektyw:

- **BILL** (Silnik Prawdy Danych) — weryfikuje dane, wykrywa sprzeczności, identyfikuje wzorce
- **NASH** (Optymalizator Decyzji) — oblicza wartości oczekiwane, mapuje drzewa decyzyjne, analizuje koszty alternatywne
- **STEVE** (Doradca Strategiczny) — ocenia pozycjonowanie rynkowe, identyfikuje błękitny ocean, ocenia timing

**Rezultat**: Raport syntezy z rekomendacją GO/NO-GO/PIVOT oparty na danych, nie na przeczuciach.

---

## Dlaczego tego potrzebujesz?

### Problem: Pojedyncza perspektywa = Martwe punkty

Kiedy analizujesz własny pomysł:
- Omijasz sprzeczności w danych
- Zawyżasz wielkość rynku
- Niedoszacowujesz kosztów
- Ignorujesz konkurencję
- Zakładasz, że popyt istnieje

**Rezultat**: Budujesz niewłaściwą rzecz, tracisz pieniądze.

### Rozwiązanie: Wieloperspektywiczna analiza = Jasność

Z 9SENS-micro:
- BILL weryfikuje wszystkie dane (łapie bzdury)
- NASH optymalizuje decyzje
- STEVE identyfikuje luki strategiczne
- Persony się nie zgadzają = czerwone flagi
- Konsensus = wysoka pewność

**Rezultat**: Decyzja GO/NO-GO oparta na danych.

---

## Szybki start

### Wymagania

- Narzędzie AI (Claude, ChatGPT, Perplexity Pro - zalecane)
- 3-6 godzin czasu
- Pomysł biznesowy do walidacji

### Kroki

**1. Załaduj framework**

Dla Claude Code / Claude:
```
Załaduj 9SENS-micro z pliku CLAUDE.md
```

Dla ChatGPT:
```
[Wklej zawartość CLAUDE.md]
```

**2. Rozpocznij analizę**

```
Analizuj: [Twój pomysł biznesowy]
```

Przykład:
```
Analizuj: Aplikacja AI do planowania posiłków dla zapracowanych rodziców,
która generuje spersonalizowane plany posiłków na podstawie ograniczeń
dietetycznych, preferencji i zawartości spiżarni.
```

**3. Przejdź przez 2 fazy**

- **Faza 1: Badania** (2-4 godziny) — zbierz dane w 5 obszarach
- **Faza 2: Analiza** (1-2 godziny) — 3 persony analizują dane

**4. Otrzymaj raport syntezy**

Framework generuje:
- Analizy od BILL, NASH i STEVE
- Raport syntezy z rekomendacją GO/NO-GO
- Krytyczne założenia do walidacji
- Konkretne kolejne kroki

---

## Jak to działa?

### Faza 1: Badania (2-4 godziny)

Zbierz dane w 5 obszarach używając narzędzi AI (Perplexity, ChatGPT):

1. **Rynek** — TAM/SAM/SOM, CAGR, segmenty, trendy
2. **Konkurencja** — gracze, ceny, luki, różnicowanie
3. **Technologia** — wykonalność, czas budowy, stos technologiczny, ryzyka
4. **Użytkownicy** — persony, punkty bólu, gotowość do płacenia, walidacja
5. **Finanse** — ceny, CAC, LTV, marże, próg rentowności

**Szablon promptów**: Zobacz `templates/research-prompts.md`

**Wyjście**: 5 plików YAML w `deliverables/YYYY-MM-DD - TEMAT/research/`

**Brama jakości**:
- Średnia pewność ≥0.75
- ≥3 źródła na temat
- Dane <6 miesięcy

### Faza 2: Analiza (1-2 godziny)

3 persony analizują dane **sekwencyjnie** (nigdy równolegle):

**BILL → NASH → STEVE**

1. **BILL** weryfikuje dane, wykrywa wzorce, wykrywa luki
2. **NASH** oblicza wartości oczekiwane, mapuje drzewa decyzyjne, analizuje koszty alternatywne
3. **STEVE** ocenia pozycjonowanie, fosę, timing, plan działania

**Wyjście**: 4 pliki markdown w `deliverables/YYYY-MM-DD - TEMAT/analysis/`
- `bill_analysis.md`
- `nash_analysis.md`
- `steve_analysis.md`
- `synthesis_report.md` ← **To tu jest decyzja GO/NO-GO**

---

## Struktura wyjściowa

```
deliverables/YYYY-MM-DD - TEMAT/
├── research/
│   ├── market_research.yaml
│   ├── competitor_research.yaml
│   ├── technical_research.yaml
│   ├── user_research.yaml
│   ├── financial_research.yaml
│   └── research_synthesis.yaml (BILL)
│
└── analysis/
    ├── bill_analysis.md
    ├── nash_analysis.md
    ├── steve_analysis.md
    └── synthesis_report.md (GO/NO-GO)
```

---

## Szablony i narzędzia

9SENS-micro zawiera szablony ułatwiające proces:

- **Prompty badawcze** — `templates/research-prompts.md`
  Kopiuj/wklej prompty dla każdego z 5 obszarów badawczych

- **Scorecard GO/NO-GO** — `templates/go-nogo-scorecard.md`
  Obiektywny framework punktacji dla decyzji GO/NO-GO/PIVOT

- **Szybka karta referencyjna** — `quick-reference.md`
  Wydrukuj to. Przypnij to. Ciągle się do tego odwołuj.

---

## Struktura plików

```
9SENS-micro/
├── README.md                    ← Jesteś tutaj
├── CLAUDE.md                    ← Instrukcje AI (główny plik)
├── copilot-instructions.md      ← Instrukcje dla GitHub Copilot
├── personas.md                  ← Szczegóły 3 person
├── phases.md                    ← Szczegółowe workflow faz
├── quick-reference.md           ← Karta podpowiedzi do wydruku
├── COMPARISON.md                ← 9SENS-micro vs Pełny 9SENS
├── index.html                   ← Landing page (po polsku)
│
├── templates/
│   ├── research-prompts.md      ← Kopiuj/wklej prompty badawcze
│   └── go-nogo-scorecard.md     ← Szablon scorecardu decyzji
│
└── deliverables/
    └── 2025-11-08 - EXAMPLE Pet Snake Subscription Box/
        ├── research/             ← 5 plików YAML badań
        └── analysis/             ← 4 analizy markdown + synteza
```

---

## Bramy jakości

Framework wymusza bramy jakości, aby zapewnić dobre decyzje:

### Bramy badań

- ✅ Średnia pewność ≥0.75
- ✅ ≥3 wiarygodne źródła na temat
- ✅ Dane <6 miesięcy

### Bramy finansowe

- ✅ Współczynnik LTV/CAC ≥3x
- ✅ Okres zwrotu ≤12 miesięcy
- ✅ Dodatnia ekonomia jednostkowa

### Bramy konsensusu person

- ✅ Wszystkie zgadzają się LUB konflikty rozwiązane
- ✅ Czerwone flagi zaadresowane
- ✅ Następne kroki specyficzne i wykonalne

---

## Często zadawane pytania

### Ile to kosztuje?

**Framework**: $0 (darmowy open-source)
**Narzędzia AI**: $0-70 (w zależności od użycia)

- Opcja darmowa: ChatGPT + manualne badania
- Zalecane: Perplexity Pro ($20/miesiąc) dla badań w czasie rzeczywistym

**ROI**: Jeśli zapobiega JEDNEJ złej decyzji → ROI 10x+

### Jak długo to trwa?

**Całkowity czas**: 3-6 godzin

- Faza Badań: 2-4 godziny
- Faza Analizy: 1-2 godziny

### Czy mogę używać innych narzędzi AI?

Tak! Framework działa z:
- Claude (Code lub wersja webowa)
- ChatGPT (GPT-4 zalecane)
- Perplexity Pro (najlepsze do badań)
- GitHub Copilot (z copilot-instructions.md)

Wystarczy załadować `CLAUDE.md` do swojego narzędzia.

### Czy to zastępuje pełny framework 9SENS?

Nie. 9SENS-micro to **darmowa prezentacja** pełnego frameworka.

**Użyj micro kiedy**:
- Testujesz małe pomysły (<$50K inwestycji)
- Uczysz się frameworka
- Walidacja popytu przed zobowiązaniem
- Mentalność DIY

**Uaktualnij do pełnego kiedy**:
- Budujesz poważny produkt (>$50K inwestycji)
- Potrzebujesz walidacji kontradyktoryjnej (oszczędza $$$)
- Chcesz realizacji end-to-end (projektowanie → budowa → testy)
- Wiele projektów (ROI kumuluje się)

Zobacz `COMPARISON.md` dla pełnego porównania.

---

## 9SENS-micro vs Pełny 9SENS

| Funkcja | 9SENS-micro (Darmowy) | Pełny 9SENS |
|---------|----------------------|-------------|
| Persony | 3 (BILL, NASH, STEVE) | 7 person |
| Walidacja Kontradyktoryjna | ❌ | ✅ Brama 4 person |
| Fazy | 2 (Badania, Analiza) | 6 faz |
| Logowanie Decyzji | Manualne | ✅ Zautomatyzowane |
| Bramy Jakości | Manualne | ✅ 5 zautomatyzowanych warstw |
| Tracker Założeń | ❌ | ✅ Zautomatyzowany |
| Koszt | **DARMOWY** | Kontakt w sprawie ceny |

**Pełne porównanie**: Zobacz `COMPARISON.md` lub `index.html`

---

## Zasoby dodatkowe

- **Szczegóły person**: `personas.md`
- **Workflow faz**: `phases.md`
- **Szybka karta referencyjna**: `quick-reference.md`
- **Prompty badawcze**: `templates/research-prompts.md`
- **Scorecard GO/NO-GO**: `templates/go-nogo-scorecard.md`
- **Pełne porównanie**: `COMPARISON.md`
- **Landing page**: `index.html`

---

## Wsparcie

### Problemy?

1. Przeczytaj `quick-reference.md` dla rozwiązywania problemów
2. Przejrzyj szczegóły workflow w `phases.md`
3. Sprawdź definicje person w `personas.md`

### Chcesz pełny framework?

Skontaktuj się w sprawie demo kompletnego systemu 9SENS z:
- 27 personami (zamiast 3)
- Bramą kontradyktoryjną (oszczędziło $200K w projekcie Smart Fleet)
- Fazami Projektuj → Buduj → Testuj
- Automatycznym logowaniem decyzji
- 5 warstwami bram jakości
- Zautomatyzowanym trackerem założeń
- Integracją z Prolog, Pytest, Git

---

## Licencja

[Dodaj licencję tutaj]

---

## Współtwórcy

[Dodaj współtwórców tutaj]

---

**Gotowy do walidacji Twojego pomysłu?**

1. Załaduj `CLAUDE.md` w swoim narzędziu AI
2. Podaj: "Analizuj: [Twój pomysł biznesowy]"
3. Przejdź przez Badania → Analizę
4. Otrzymaj decyzję GO/NO-GO opartą na danych

**Czas rozpocząć podejmowanie lepszych decyzji.**

🚀 **Powodzenia!**

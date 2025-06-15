# 🛒 Shop‑Summary

Lekka aplikacja CLI/web do generowania podsumowań sprzedaży.  

---

## 📦 Spis treści

- [Opis](#opis)
- [Funkcjonalności](#funkcjonalności)
- [Instalacja](#instalacja)
- [Konfiguracja](#konfiguracja)
- [Użycie](#użycie)
  - [CLI](#cli)
  - [Interfejs webowy](#interfejs‑webowy)
- [Przykłady](#przykłady)
- [Testy](#testy)
- [Architektura](#architektura)
- [Wkład](#wkład)
- [Licencja](#licencja)

---

## 📝 Opis

„Shop‑Summary” to narzędzie do agregowania i wizualizowania danych sprzedażowych. Obsługuje różne źródła (CSV, API), umożliwiając:

- analizę przychodów w wybranym przedziale czasowym,
- identyfikację najcenniejszych klientów oraz produktów,
- eksport wygenerowanych raportów do CSV/PDF.

---

## ✅ Funkcjonalności

- import danych sprzedażowych z plików,
- filtrowanie wg dat, klientów, kategorii produktów,
- generowanie wykresów i tabel podsumowujących,
- eksport wyników do CSV i PDF,
- interfejs webowy do przeglądania raportów online.

---

## 🛠️ Instalacja

1. Sklonuj repozytorium:
   ```bash
   git clone https://github.com/czakk/shop-summary.git
   cd shop-summary
   git checkout develop
   ```
2. Instalacja zależności:
   ```bash
   npm install      # frontend
   pip install -r requirements.txt  # backend (jeśli używasz Pythona)
   ```
3. Alternatywnie użyj Dockera:
   ```bash
   docker-compose up --build
   ```

---

## ⚙️ Konfiguracja

Plik `config.yml` przykładowo:
```yaml
data_source:
  type: csv
  path: /path/to/sales.csv

web:
  host: 0.0.0.0
  port: 8080

export:
  formats: [csv, pdf]
```

---

## 🚀 Użycie

### CLI

```bash
shop-summary analyse \
  --start 2025-01-01 \
  --end 2025-05-31 \
  --output summary_may_2025.json
```

### Interfejs webowy

1. Uruchom backend i frontend.
2. Odwiedź `http://localhost:8080`.
3. Załaduj dane, skonfiguruj filtry i wygeneruj raport.

---

## 📈 Przykłady

- Podsumowanie miesięczne do JSON:
  ```bash
  shop-summary analyse --start 2025-06-01 --end 2025-06-30 --output june_summary.json
  ```

---

## 🧪 Testy

Uruchom zestaw testów:
```bash
pytest tests/       # Python
npm test            # JavaScript/TypeScript
```

---

## 🏗️ Architektura

- **CLI**: moduł `cli/*`
- **Backend**: `backend/` – logika przetwarzania danych, API
- **Frontend**: `frontend/` – React/Vue
- **Eksport**: `export/` – CSV i PDF

---

## 🤝 Wkład

1. Sklonuj i utwórz branch:
   ```bash
   git checkout -b feature/my‑awesome‑feature
   ```
2. Wprowadź zmiany, dodaj testy.
3. Otwórz Pull Request – opisz cel, zmiany i testy.

---

## 📄 Licencja

Projekt na licencji MIT – więcej w pliku LICENSE.

---


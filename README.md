# Analiza jakości powietrza w czasie rzeczywistym (API GIOŚ + AI)

Projekt zrealizowany w ramach przedmiotu **Analiza danych biznesowych** na kierunku **Informatyka** (specjalność: *Informatyka w przedsiębiorstwie*, studia inżynierskie) na **Politechnice Rzeszowskiej**.

Celem projektu jest analiza jakości powietrza w czasie rzeczywistym na podstawie danych ze stacji pomiarowych w Rzeszowie (API GIOŚ), wyliczanie europejskiego wskaźnika **CAQI** oraz prognozowanie jego wartości za pomocą algorytmów uczenia maszynowego.

---

## 🚀 Główne funkcjonalności

- **Pobieranie danych z API GIOŚ:** Obsługa danych bieżących (24h), kroczących (20 dni) oraz historycznych z pliku Excel (rok 2023).
- **Kalkulator CAQI:** Wyznaczanie wskaźnika jakości powietrza na podstawie stężeń: PM2.5, PM10, CO, NO₂, O₃, SO₂.
- **Modele Machine Learning:** Trening i ewaluacja modeli regresyjnych przewidujących CAQI:
  - **Random Forest** (RMSE: 0.63)
  - **XGBoost** (RMSE: 0.69)
  - **Decision Tree** (RMSE: 0.82)
- **Wizualizacje i EDA:**
  - Wykresy przebiegu CAQI w czasie (`matplotlib`).
  - Heatmapy korelacji zanieczyszczeń oraz parametrów pogodowych generowane w Pythonie (`seaborn`) oraz w języku R.
  - Wykresy par zmiennych (tzw. *pair plots*) obrazujące histogramy, rozkłady i współczynniki korelacji z podziałem na poziomy ryzyka (język R).
- **Moduł powiadamiania:** Automatyczne wykrywanie głównego składnika zanieczyszczającego oraz generowanie raportów (TXT/CSV) z potencjalnymi przyczynami pogorszenia jakości powietrza.

---

## 🛠 Wymagane biblioteki i technologie

### Python
Główny proces przetwarzania i modele:
- `requests`
- `pandas`
- `numpy`
- `openpyxl`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `xgboost`
- `joblib`

### R
Skrypty analityczne, mapy cieplne oraz wykresy:
- `mlr3verse`
- `ggplot2`
- `data.table`
- `GGally`

---

## ▶️ Uruchomienie

### 1. Python (Główny program)
Aby pobrać dane, wyliczyć CAQI, wygenerować przewidywania modeli i podstawowe wykresy, wystarczy uruchomić:

```bash
python main.py
```

### 2. R (Analiza statystyczna)
Skrypty analityczne generujące zaawansowane mapy cieplne oraz wykresy par należy uruchomić w środowisku R (np. RStudio) lub z konsoli dla poszczególnych plików `.R`.

---

## 👥 Autorzy

* **Agnieszka Prościak**
* **Patryk Nykiel**
* **Daniel Szumski**

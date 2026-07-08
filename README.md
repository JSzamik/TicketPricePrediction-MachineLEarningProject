# Predykcja Cen Biletów Lotniczych – Analiza Danych i Modele Uczenia Maszynowego

Kompleksowy projekt z zakresu eksploracji danych i uczenia maszynowego, którego celem jest analiza czynników wpływających na ceny biletów lotniczych oraz budowa modeli predykcyjnych o wysokiej skuteczności. Projekt obejmuje pełny proces analityczny – od przygotowania danych i eksploracyjnej analizy (EDA), przez porównanie wielu algorytmów regresyjnych, aż po interpretację modeli z wykorzystaniem metod Explainable AI (SHAP).

**Autor:** Jakub Szamik

---

# Opis projektu

Repozytorium zawiera kompletny pipeline analizy danych przygotowany w języku **Python**. Projekt został zrealizowany na zbiorze **Flight Price Prediction** pochodzącym z serwisu Kaggle i obejmuje wszystkie etapy procesu Data Science.

Projekt składa się z następujących elementów:

- **Eksploracyjna analiza danych (EDA)** – analiza rozkładów zmiennych, korelacji, zależności pomiędzy ceną biletu a cechami lotu oraz wizualizacja struktury danych.
- **Przygotowanie danych** – kodowanie zmiennych kategorycznych (One-Hot Encoding), usuwanie obserwacji odstających oraz wykrywanie anomalii metodą Isolation Forest.
- **Modelowanie predykcyjne** – porównanie sześciu modeli regresyjnych oraz analiza jakości predykcji.
- **Modele segmentowe** – budowa niezależnych modeli dla klas **Economy** i **Business**, co pozwoliło zwiększyć dokładność predykcji względem pojedynczego modelu.
- **Interpretacja modeli (XAI)** – analiza wpływu poszczególnych cech na decyzje modelu z wykorzystaniem biblioteki SHAP.

---

# Główne metody i wyniki

### Analiza danych

- wykonano kompleksową eksplorację danych (EDA),
- przeprowadzono analizę korelacji oraz zależności pomiędzy cechami,
- zbadano wpływ czasu do wylotu, długości lotu oraz liczby przesiadek na cenę biletu,
- zidentyfikowano efekt **last-minute**, odpowiadający za gwałtowny wzrost cen tuż przed wylotem.

### Przygotowanie danych

- usunięto obserwacje odstające,
- zastosowano **Isolation Forest** do wykrywania anomalii,
- zakodowano zmienne kategoryczne metodą **One-Hot Encoding**,
- przygotowano trzy warianty zbioru danych w celu wyboru najlepszego zestawu do modelowania.

### Modelowanie

Porównano następujące algorytmy regresji:

- Linear Regression
- Ridge Regression
- Random Forest
- Gradient Boosting Regressor
- XGBoost
- LightGBM

Najlepsze wyniki uzyskał **LightGBM**, który został wybrany jako model końcowy.

### Kluczowe wnioski

- modele segmentowe (**Economy** oraz **Business**) osiągnęły wyższą skuteczność niż pojedynczy model uczony na całym zbiorze,
- model LightGBM zapewnił najwyższe wartości współczynnika R² oraz najniższe błędy MAE i RMSE,
- najważniejszymi predyktorami ceny biletu okazały się:
  - liczba dni do wylotu,
  - czas trwania lotu,
  - klasa podróży,
  - linia lotnicza.

---

# Struktura projektu

```
├── notebooks/            # Analiza danych, EDA oraz eksperymenty
├── data/                 # Dane wejściowe i przetworzone zbiory
├── models/               # Zapisane modele uczenia maszynowego
├── figures/              # Wykresy wykorzystane w raporcie
├── raport.pdf            # Dokumentacja projektu
├── requirements.txt      # Lista wymaganych bibliotek
├── README.md             # Opis projektu
└── .gitignore
```

---

# Wykorzystane technologie

Projekt został zrealizowany z wykorzystaniem:

- Python
- Pandas
- NumPy
- Scikit-learn
- LightGBM
- XGBoost
- SHAP
- Matplotlib
- Seaborn

---

# Zbiór danych

Projekt wykorzystuje zbiór **Flight Price Prediction** dostępny w serwisie Kaggle.

https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction

Zbiór zawiera ponad **300 000 rekordów** opisujących krajowe loty w Indiach, obejmujących m.in.:

- linię lotniczą,
- miasta wylotu i przylotu,
- klasę podróży,
- liczbę przesiadek,
- czas lotu,
- liczbę dni do wylotu,
- cenę biletu.

---

# Uruchomienie projektu

## Wymagania

- Python 3.10+
- pip

## Instalacja bibliotek

```bash
pip install -r requirements.txt
```

## Uruchomienie projektu

Notebooki można uruchomić w środowisku **Jupyter Notebook** lub **JupyterLab**.

```bash
jupyter notebook
```

lub

```bash
jupyter lab
```

---

# Najważniejsze rezultaty

- kompleksowa eksploracja danych (EDA),
- porównanie sześciu modeli regresyjnych,
- wykrywanie i analiza anomalii,
- modele segmentowe zwiększające jakość predykcji,
- interpretacja modeli przy użyciu SHAP,
- identyfikacja najważniejszych czynników wpływających na cenę biletu.

---

# Autor

**Jakub Szamik**

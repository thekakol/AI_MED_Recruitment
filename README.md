# Zadanie rekrutacyjne – Klasyfikacja serca chorego na kardiomiopatię przerostową (kardiomegalię)

## Opis zadania

Twoim zadaniem jest przygotowanie rozwiązania problemu klasyfikacji serca chorego na **kardiomiopatię przerostową (kardiomegalię)** na podstawie podanych cech. Należy wykorzystać jedną z metod **klasycznego uczenia maszynowego** opisaną w pliku [ML.md](ML.md)  Celem jest zbudowanie modelu, który będzie potrafił poprawnie odróżnić zdrowe serce od serca chorego na podstawie dostępnych danych.

Repozytorium zawiera zbiór danych zapisany w pliku **CSV** z wyznaczonymi cechami geometrycznymi i obrazowymi, które stanowią podstawę do dalszej analizy. Od kandydata oczekujemy przygotowania kodu, który:

1. Wczyta dane z pliku `.csv`.
2. Przeprowadzi wstępne przetwarzanie (np. standaryzacja, podział na zbiór treningowy i testowy).
3. Wytrenuje wybrany model lub kilka modeli.
4. Dokona ewaluacji rozwiązania (np. accuracy, precision, recall, F1-score).
5. Opisze swoje rozwiązanie.




## Lista cech
Poniżej znajdują się cechy, które opisują obraz serca i płuc. Przy każdej cesze podana jest nazwa angielska (taka jak w pliku CSV) oraz opis w języku polskim:

### Lung width (Szerokość płuc)
Odległość pomiędzy najbardziej zewnętrznymi punktami płuc w poziomie.

### Heart width (Szerokość serca)
Maksymalna szerokość serca mierzona w poziomie.

### CR ratio (Wskaźnik CR)
Stosunek szerokości serca do szerokości płuc.

### Inertia tensors (Tensory bezwładności)
Miary opisujące rozkład pikseli serca i płuc względem osi, pozwalające uchwycić kształt i orientację obiektów.
W pliku `.csv` znajdziesz 4 składowe tej cechy:
- `xx` - jak piksele są rozłożone względem osi y (wydłużenie wzdłuż x)
- `yy` - jak piksele są rozłożone względem osi x (wydłużenie wzdłuż y)
- `xy` - rozłożenie względem osi x i y (duża wartość to obiekt obrócony)
- `normalized_diff` - wartość skalarana na podstawie wektora, którego składowe omówiono wyżej.


### Inscribed circle detection (Wykrycie okręgu wpisanego)
Promień największego okręgu, który można wpisać w obszar serca, opisujący jego symetrię i zwartość.

### Polygon Area Ratio (Wskaźnik pola wielokąta)
Stosunek pola wielokąta obejmującego kontur serca do rzeczywistego pola serca.

### Heart perimeter (Obwód serca)
Długość obwodu konturu serca.

### Heart area (Pole powierzchni serca)
Powierzchnia zajmowana przez serce.

### Lung area (Pole powierzchni płuc)
Powierzchnia zajmowana przez płuca.

## Oczekiwania
* Kod powinien być napisany w Pythonie (np. z użyciem bibliotek `scikit-learn`, `numpy`, `pandas`, `matplotlib`).
* Należy dodać krótki opis rozwiązania w postaci pliku [Markdown](https://www.markdownguide.org/) (`.md`).
* Wyniki ewaluacji należy zaprezentować w czytelny sposób (np. tabela wyników, wykresy ROC/PR).
* Kod i commity powinny być w jęzku **angielskim**, plik markdown z opisem rozwiązanie może być po polsku lub angielsku.

W celu rozwiązania zadania prosimy o [Fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) tego repozytorium. A następnie przesłania linku do repozytorium na TUTAJ GDZIE REKRUTACJA
## Kryteria oceny

* Poprawność działania kodu.
* Przejrzystość i czytelność implementacji.
* Wykorzystanie metod klasycznego uczenia maszynowego.
* Pomysłowość rozwiązania.
* **Historia commitów w repozytorium** – oceniana będzie ich czytelność i spójność.

Powodzenia!

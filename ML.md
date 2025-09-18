# Klasyczne metody uczenia maszynowego

Poniżej znajdują się krótkie opisy metod uczenia maszynowego, które mogą być wykorzystane do rozwiązania zadania klasyfikacji. W razie potrzeby lepszego zrozumienia prosimy o zapoznanie się z dokumentacją danej metody w bibliotece scikit-learn lub samodzielny reasearch.

## Drzewa decyzyjne (Decision Trees)

Metoda polegająca na podejmowaniu decyzji w oparciu o kolejne pytania (podziały danych) w strukturze drzewa. Każdy węzeł odpowiada testowi na wybranej cesze, a każda gałąź reprezentuje wynik tego testu. Drzewa decyzyjne są proste do zrozumienia i interpretacji, ale mogą łatwo prowadzić do przeuczenia (overfittingu).
<br/>
📖 Dokumentacja: [DecisionTreeClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)

## Lasy losowe (Random Forest)

Algorytm zespołowy (ang. ensemble), który buduje wiele drzew decyzyjnych na różnych losowych podzbiorach danych i cech. Wynik klasyfikacji jest określany na podstawie głosowania większościowego. Lasy losowe są bardziej odporne na przeuczenie niż pojedyncze drzewa i zapewniają wysoką skuteczność.
<br/>
📖 Dokumentacja: [RandomForestClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)

## K-Nearest Neighbors (k-NN)

Algorytm oparty na podobieństwie. Nowa próbka jest klasyfikowana na podstawie klas `k` najbliższych punktów w przestrzeni cech (mierzonej np. odległością euklidesową). Metoda jest prosta i skuteczna, ale bywa kosztowna obliczeniowo przy dużych zbiorach danych.
<br/>
📖 Dokumentacja: [KNeighborsClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)

## Support Vector Machine (SVM)

Metoda klasyfikacji polegająca na znajdowaniu hiperpowierzchni (hiperpłaszczyzny), która najlepiej oddziela klasy w przestrzeni cech. SVM stara się maksymalizować margines pomiędzy klasami, co zapewnia dobrą zdolność generalizacji. Dzięki użyciu funkcji jądra (kernel) można klasyfikować dane nieliniowo.
<br/>
📖 Dokumentacja: [SVC](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)

## Regresja logistyczna (Logistic Regression)

Model probabilistyczny używany do klasyfikacji binarnej. Szacuje prawdopodobieństwo przynależności próbki do danej klasy, a następnie klasyfikuje na podstawie progu (np. 0.5). Jest prostym i interpretowalnym modelem, często używanym jako punkt odniesienia w klasyfikacji. Prekursor sieci neuronowych.
<br/>
📖 Dokumentacja: [LogisticRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)

# Miary jakości klasyfikacji

Do oceny skuteczności modeli klasyfikacyjnych stosuje się różne metryki. Najczęściej używane to:

## Accuracy (Dokładność)

Odsetek poprawnych predykcji (zarówno pozytywnych, jak i negatywnych) względem wszystkich próbek. Dobrze działa przy zrównoważonych zbiorach danych, ale bywa mylący przy niezbalansowanych klasach.
<br/>
📖 Dokumentacja: [accuracy\_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html)

## Precision (Precyzja)

Określa, jaki odsetek próbek zaklasyfikowanych jako pozytywne rzeczywiście należy do klasy pozytywnej. Wysoka precyzja oznacza małą liczbę fałszywych alarmów (false positives).
<br/>
📖 Dokumentacja: [precision\_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_score.html)

## Recall (Czułość)

Pokazuje, jaki odsetek rzeczywistych przypadków pozytywnych został poprawnie wykryty przez model. Wysoka czułość oznacza małą liczbę przeoczonych przypadków pozytywnych (false negatives).
<br/>
📖 Dokumentacja: [recall\_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.recall_score.html)

## F1-score

Średnia harmoniczna precyzji i czułości. Wartość F1 dobrze równoważy obie metryki i jest szczególnie przydatna przy niezbalansowanych klasach.
<br/>
📖 Dokumentacja: [f1\_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html)

# Macierz pomyłek (Confusion Matrix)

Macierz pomyłek pozwala zwizualizować wyniki klasyfikacji, rozróżniając poprawne i błędne decyzje modelu.

|                         | Rzeczywiste pozytywne | Rzeczywiste negatywne |
| ----------------------- | --------------------- | --------------------- |
| **Predykcja pozytywna** | True Positive (TP)    | False Positive (FP)   |
| **Predykcja negatywna** | False Negative (FN)   | True Negative (TN)    |

* **TP (True Positive)** – poprawnie wykryte przypadki pozytywne.
* **TN (True Negative)** – poprawnie wykryte przypadki negatywne.
* **FP (False Positive)** – przypadki negatywne błędnie zaklasyfikowane jako pozytywne.
* **FN (False Negative)** – przypadki pozytywne błędnie zaklasyfikowane jako negatywne.

Metryki oblicza się na podstawie wartości z tej tabeli:

* Accuracy = (TP + TN) / (TP + TN + FP + FN)
* Precision = TP / (TP + FP)
* Recall = TP / (TP + FN)
* F1-score = 2 \* (Precision \* Recall) / (Precision + Recall)
<br/>
📖 Dokumentacja: [confusion\_matrix](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html)

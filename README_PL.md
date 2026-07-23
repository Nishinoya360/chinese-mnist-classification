# Klasyfikacja chińskich znaków z wykorzystaniem sieci neuronowych (Chinese MNIST)

## Opis projektu

Celem projektu było stworzenie i porównanie modeli głębokiego uczenia przeznaczonych do rozpoznawania chińskich symboli na podstawie zbioru danych **Chinese MNIST**. Projekt obejmuje pełny proces przygotowania danych, budowy modeli, trenowania sieci neuronowych oraz ocenę ich skuteczności i wydajności obliczeniowej.

Zbiór Chinese MNIST zawiera obrazy przedstawiające chińskie znaki wraz z odpowiadającymi im etykietami. Zadaniem modeli jest poprawna klasyfikacja symboli na podstawie dostarczonych obrazów.

## Cele projektu

* Wczytanie i przygotowanie danych ze zbioru Chinese MNIST.
* Utworzenie własnego zbioru danych w PyTorch.
* Podział danych na zbiory treningowy, walidacyjny i testowy.
* Implementacja i porównanie trzech architektur sieci neuronowych.
* Analiza procesu uczenia modeli.
* Ocena jakości klasyfikacji na podstawie dokładności oraz funkcji straty.
* Porównanie czasu trenowania poszczególnych modeli.

## Zbiór danych

Projekt wykorzystuje zbiór **Chinese MNIST**, zawierający obrazy chińskich symboli oraz odpowiadające im etykiety zapisane w pliku CSV.

Proces przygotowania danych obejmował:

* odczyt obrazów z wykorzystaniem biblioteki Pillow (PIL),
* przekształcenie obrazów do postaci tensorów,
* normalizację danych wejściowych,
* utworzenie zbioru danych w formacie zgodnym z biblioteką PyTorch.

Dataset został zbudowany przy użyciu klasy `TensorDataset`, która przechowuje obrazy oraz odpowiadające im etykiety.

## Przygotowanie danych

Po utworzeniu datasetu dane zostały podzielone na:

* zbiór treningowy,
* zbiór walidacyjny,
* zbiór testowy.

Do efektywnego ładowania danych podczas procesu uczenia wykorzystano klasę `DataLoader`.

## Architektura modeli

W projekcie zaimplementowano trzy modele o różnym poziomie złożoności:

### Worst Model

Najprostsza architektura stanowiąca punkt odniesienia dla pozostałych modeli.

### Medium Model

Model o średniej liczbie parametrów, zapewniający lepszą zdolność generalizacji przy umiarkowanych wymaganiach obliczeniowych.

### Best Model

Najbardziej rozbudowana architektura zastosowana w projekcie, zaprojektowana w celu osiągnięcia najwyższej dokładności klasyfikacji.

## Proces uczenia

Modele były trenowane z wykorzystaniem biblioteki PyTorch.

W celu przyspieszenia obliczeń wykorzystano akcelerację GPU:

```python
device = "cuda"
```

Podczas treningu monitorowano:

* wartość funkcji straty dla zbioru treningowego,
* wartość funkcji straty dla zbioru walidacyjnego,
* dokładność klasyfikacji,
* czas trenowania modeli.

## Wyniki

Dla każdego modelu wygenerowano:

### Wykresy funkcji straty

Przedstawiające zmiany wartości funkcji kosztu w kolejnych epokach treningu.

### Wykresy dokładności

Pokazujące skuteczność klasyfikacji na zbiorach treningowych i walidacyjnych.

### Porównanie modeli

Przeprowadzono analizę:

* końcowej dokładności klasyfikacji,
* szybkości uczenia,
* liczby parametrów,
* czasu wykonania treningu.

Pozwoliło to ocenić kompromis pomiędzy wydajnością obliczeniową a jakością predykcji.

## Wykorzystane technologie

* Python
* PyTorch
* Torchvision
* Pillow (PIL)
* NumPy
* Pandas
* Seaborn
* Matplotlib



## Zaprezentowane umiejętności

* przygotowanie danych do uczenia maszynowego,
* przetwarzanie obrazów w Pythonie,
* budowa datasetów w PyTorch,
* wykorzystanie DataLoaderów,
* projektowanie i trenowanie sieci neuronowych,
* wykorzystanie GPU (CUDA),
* analiza procesu uczenia modeli,
* wizualizacja wyników eksperymentów,
* porównywanie architektur sieci neuronowych.

## Możliwe kierunki rozwoju

* zastosowanie bardziej zaawansowanych sieci CNN,
* wykorzystanie transfer learningu,
* automatyczny dobór hiperparametrów,
* augmentacja danych,
* wdrożenie modelu jako aplikacji webowej lub API.

# analiza-danych
Statystyczna analiza danych

## Wstęp
Raport przedstawia kroki, pozwalające odpowiedzieć na pytanie jak zmieniła się wielkość metrażu mieszkania przypadającego na jedną osobę (w m2) w Polsce. Polskie przepisy mówią o tym, że na jedną osobę musi przypadać co najmniej 13 metrów sześciennych objętości pomieszczenia oraz co najmniej 2 metry kwadratowe wolnej powierzchni podłogi – wolnej, czyli niezajętej przez urządzenia techniczne czy sprzęt.
Na podstawie zbioru danych z pomiarami metraży mieszkań z ostatnich 50 lat, dokonano dogłębnej analizy. Dla zebranych danych stworzono histogram i obliczono średnią, wariancję, odchylenie standardowe, medianę, kwartyle i dominantę. Z taką wiedzą przystąpiono do próby udzielenia odpowiedzi na pytanie: "Jak zmieniła się wielkość metrażu mieszkania przypadającego na jedną osobę?"

## Wykorzystane biblioteki

---------
ggplot2  
dplyr    
reshape2 
plotly   
caret    
party    
gbm      
mboost   
corrplot 
---------

## Ładowanie danych
Do wczytania danych z pliku `.csv`, użyto funkcji `read.table`. Ze względu na wystąpienie nagłówka, ustawiono parametr `header = TRUE`, znak separatora został ustawiony na przecinek (`sep=","`). Dodatkowo skorzystano z parametru `na.strings = "?"` w celu zamiany brakujących wartośći (oznaczonych w zbiorze danych znakiem `'?'`) na wartość `NA`.

```r
data <- read.table('./mieszkania.csv', header = TRUE, sep=",", na.strings = "?")
```

## Rozmiar zbioru
Zbiór danych zawiera 52582 wierszy oraz 15 kolumn.

####Opis kolumn:

##Podsumowanie
Na podstawie powyższych wykresów można stwierdzić, że na jedną osobę w Polsce przypada prawie 31 m2 mieszkania. Najnowszy odczyt jest o 3 m większy niż 5 lat temu i o ponad 8 m większy niż w 2002 roku. Sytuacja mieszkaniowa Polaków poprawia się, choć wciąż daleko nam do warunków europejskich. Poprawę zawdzięczamy przede wszystkim nowym nieruchomościom – domom i mieszkaniom powstającym w Polsce. W latach 2003 – 2022 oddano do użytkowania ponad 3,2 mln takich nieruchomości. 
Średnia europejska to 40 m2. Gdyby przyjąć, że w Polsce przez kolejne lata powstawałoby tyle mieszkań co w latach 2013-2022, to dojście do europejskiej średniej zajęłoby nam około 20-30 lat.






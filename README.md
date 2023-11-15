# analiza-danych
Statystyczna analiza danych

## Wstęp
Raport przedstawia kroki, pozwalające odpowiedzieć na pytanie jak zmieniła się wielkość metrażu mieszkania przypadającego na jedną osobę (w m2) dla wszystkich osób zameldowanych przy ul. Przestrzennej we Wrocławiu. Polskie przepisy mówią o tym, że na jedną osobę musi przypadać co najmniej 13 m3 objętości pomieszczenia oraz co najmniej 2 m2 wolnej powierzchni podłogi – wolnej, czyli niezajętej przez urządzenia techniczne czy sprzęt.
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

# CeneoScraper

## Struktura opinii w serwisie [Ceneo.pl]["https://www.ceneo.pl/"]

|Składnia opinii|Selektor|Nazwa zmiennej|Typ danych|
|---------------|--------|--------------|----------|
|opinia|div.js_product-review|[opinion]|bs4.element.ResultSet|
|identyfikator opinii|div.js_product-review\["data-entry-id"\]|[opinion_id]||
|autor opinii|span.user-post__author-name|[author]||
|rekomendacja autora|span.user-post__author-recomendation > em|[recommendation]||
|liczba gwiazdek|span.user-post__score-count|[stars]||
|treść opinii|div.user-post__text|[content]||
|lista zalet|div[class$=positives]~div.review-feature_item|[pros]||
|lista wad|div[class$=negatives]~div.review-feature_item|[cons]||
|dla ilu osób przydatna|button.vote-yes> span|[useful]||
|dla ilu osób nieprzydatna |button.vote-no> span|[useless]||
|data wystawienia opinii|span.user-post__published > time:nth-child(1)\["datatime"\]|[published]||
|data zakupu produktu|span.user-post__published > time:nth-child(2)\["datatime"\]|[purchased]||
## Etapy pracy nad projektem
1. Pobranie pojedynczej opinii do zmiennych
2.Zapisanie wszytkich elemenntów pojedynczej opinii do jednej zmiennej \(słownik\)
3.Pobranie większej ilości opinii z pojedynczej strony do słowników i dodanie ich do listy
4.pobranie wszystkich opinii o produkcie z wszystkich stron i zaspisanie ich do pliku. json
5.Dodanie możliwości podania id produktu przez użytkownika za pomocą klawiatury
6.Refaktoryzacja  kodu:
a. utworzenia funkcji do pobierania składowych strony HTML
b. utworzenia słownika opisujacego strukture opinii wraz z selektorami pszczególnych elementów
c.zamiana instruukcji pobierających składowe opinii do pojedynczych zmiennych i tworzących z nich słownik na wyrażenie słownikowe \ (Ddctionary comprehension\)
tworzące słownik reprezentuący pojedynczą opinię na podstawie słownika selektorów
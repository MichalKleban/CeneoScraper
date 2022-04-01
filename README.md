# CeneoScraper

## Struktura opinii w serwisie [Ceneo.pl]["https://www.ceneo.pl/"]

|Składnia opinii|Selektor|Nazwa zmiennej|Typ danych|
|---------------|--------|--------------|----------|
|opinia|div.js_product-review|||
|identyfikator opinii|div.js_product-review\["data-entry-id"\]|||
|autor opinii|span.user-post__author-name|||
|rekomendacja autora|span.user-post__author-recomendation > em|||
|liczba gwiazdek|span.user-post__score-count|||
|treść opinii|div.user-post__text|||
|lista zalet|div.review-feature|||
|lista wad|div.review-feature > div:nth-child(2)|||
|dla ilu osób przydatna|button.vote-yes.js_product-review-vote.js_vote-yes|||
|dla ilu osób nieprzydatna |button.vote-no.js_product-review-vote.js_vote-no|||
|data wystawienia opinii|span.user-post__published > time:nth-child(1)\["datatime"\]|||
|data zakupu produktu|span.user-post__published > time:nth-child(2)\["datatime"\]|||

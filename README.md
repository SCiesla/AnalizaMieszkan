# Analiza rynku mieszkań (maj 2023)

Projekt, którego celem było wykonanie analizy dostępnyh ofert mieszkaniowych w maju 2023 na portalu www.olx.pl.
Dane pozyskano poprzez napisanie scrappera, który pozyskiwał dane o ofertach mieszkań na sprzedaż jak i na wynajem. 
Uzyskane w ten sposób dane wstępnie oczyszczono i przeprowadzono analizę wyników. 
Dodatkowo sporządzono model regresji liniowej opisujący kwotę w zależności od dzielnicy i powierzchni mieszkania w Warszawie. 

Dane zostały także dodatkowo sporządzone w formie interaktywnego dashboardu w programie Tableau. 

## Kod pozyskujący dane

Analizę przeprowadzono dla pięciu wybranych miast: Warszawa, Kraków, Wrocław, Poznań i Gdańsk. Dane o mieszkaniach jakie pozyskiwano to:
- kwota sprzedaży/wynajmu 
- miasto
- dzielica 
- rozkład mieszkania (kalaerka, dwupokojowe, trzypokojowe ...)
- powierzchnia mieszkania
- informacja o możliwej negocjacji 

## Wstępne przygotowanie danych

Po wykonaniu scrapera, dokonano wstępnej analizy otrzymanych danych i przeskanowano je pod kątem wartości odstających.

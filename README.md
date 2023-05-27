# Analiza rynku mieszkań (maj 2023)

Projekt, którego celem było wykonanie analizy dostępnyh ofert mieszkaniowych w maju 2023 na portalu www.olx.pl.
Dane pozyskano pisząc skrypt scrapujący wykorxzystując bibliotekę **Beautiful Soup**, który pozyskiwał dane o ofertach mieszkań na sprzedaż jak i na wynajem.

Analizę przeprowadzono dla pięciu wybranych miast: Warszawa, Kraków, Wrocław, Poznań i Gdańsk. Dane o mieszkaniach jakie pozyskiwano to:
- kwota sprzedaży/wynajmu 
- miasto
- dzielica 
- rozkład mieszkania (kalaerka, dwupokojowe, trzypokojowe ...)
- powierzchnia mieszkania
- informacja o możliwej negocjacji 
- link do pełnej oferty

Uzyskane w ten sposób dane wstępnie oczyszczono i przeprowadzono analizę wyników. 
https://github.com/SCiesla/AnalizaMieszkan/blob/main/code/Data%20Preparation.ipynb

Raport zawierający szczegółową analizę danych:
https://github.com/SCiesla/AnalizaMieszkan/blob/main/code/Report.ipynb

Dodatkowo wykonano model regresji liniowej opisujący kwotę w zależności od dzielnicy i powierzchni mieszkania w Warszawie:
https://github.com/SCiesla/AnalizaMieszkan/blob/main/code/LinearRegression.ipynb

Dane zostały także dodatkowo sporządzone w formie interaktywnego dashboardu w programie Tableau:
https://public.tableau.com/app/profile/adam.cisma/viz/Analizarynkumieszkamaj2023/Dashboard1


## Najważniejsze wnioski z analizy

(w trakcie)

# Analiza rynku mieszkań (maj 2023)

Projekt, którego celem było wykonanie analizy dostępnyh ofert mieszkaniowych w maju 2023 na portalu www.olx.pl.
Dane pozyskano pisząc skrypt scrapujący wykorzystując bibliotekę **Beautiful Soup**, który pozyskiwał dane o ofertach mieszkań na sprzedaż jak i na wynajem.

Analizę przeprowadzono dla pięciu wybranych miast: Warszawa, Kraków, Wrocław, Poznań i Gdańsk. Dane o mieszkaniach, jakie pozyskiwano to:
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

Model regresji liniowej opisujący kwotę w zależności od dzielnicy i powierzchni mieszkania w Warszawie:
https://github.com/SCiesla/AnalizaMieszkan/blob/main/code/LinearRegression.ipynb

Dane zostały także dodatkowo sporządzone w formie interaktywnego dashboardu w programie **Tableau**:
https://public.tableau.com/app/profile/sciesla/viz/Analizarynkumieszkamaj2023/Dashboard2


## Najważniejsze wnioski z analizy

### 1. 3.5% ofert jest błędnie zaklasyfikowana przez właścicieli

Około 700 ogłoszeń w kateogrii spredaż/wynajem zostało błędnie przypisanych przez właścicieli mieszkań. 
 - Dotyczą one wynajmu pojedynczych pokojów na miesiąc lub na dobę 
 - Dotyczą one wynajmu lokalu biurowych, sprzedaży lokali gastronomicznych lub całych kamienic.

Powyższe przypadki mają swoje własne kategorie (pokoje na msc - Pokoje i Stancje) 

Lokale i kamienice - kategoria Domy. Właściciele błędnie je oznaczają. 

### 2. Ogłoszenia występują z błędnie wpisaną dzielnicą 

Niektóre miasta (np. Wrocław) nie mają możlwiości wpisania istniejących dzielnic. Oznacza to, że oferty są błędnie przypisywane do najbliżej istniejącej w systemie dzielnicy.
We Wrocławiu oferty mieszkań w dzielnicy: Gaj, Tarnogaj lub Jagodno zostały zaklasyfikowane do dzielnicy Krzyki.
W pozostałych miastach prawdopodobnie jest ten sam efekt. Nie powinniśmy się zatem sugerować szukaniem mieszkań poprzez wybór dzielnicy za pośrednictwem strony olx. 

### 3. 60% Ofert nie pochodzi ze strony OLX. 

Oferty przedstawione na stronie OLX przekierowują na stronę otodom.pl. 
Tylko 40% ze wszystkich ofert jest opublikowana na stronie OLX. 

### 4. Najdrożej i najwięcej w stolicy
![image](https://github.com/SCiesla/AnalizaMieszkan/assets/134396909/08cdfcd5-d9b2-4669-912e-0a9b0093fbf0)

Warszawa dominuje pod względem cen mieszkań na wynajem i na sprzedaż. Zapłacimy tam najwięcej za kawalerki, mieszkania 2, 3 i 4 pokojowe. 
Najtańszy ze wszystkich okazuje się być Poznań z najniższymi stawkami. 

Warszawa dominuje dodatkowo pod względem ofert. Mieszkań na sprzedaż znajdziemy tam około 3 tysiące. Dla kontrastu na drugim miejscu jest Wrocław (1,9 tyś.). Najmniej ofert na sprzedaz ma Gdańsk (około 1 tyś.) 

### 5. Na jaki typ mieszkania jest najwięcej ofert? 

Pod względem mieszkań na sprzedaż i na wynajem najwięcej ofert znajdziemy na mieszkania dwu- i trzypokpojowe w każdym mieście. 
Bardzo mało ofert jest na sprzedaż kawalerek, za to bardzo dużo na wynajem. 
Właściele chętniej wynajmują swoje kawalerki niż decydują się na ich sprzedaż.

### 6. Tylko 8% ofert zawiera deklaracje o możliwości negocjacji ceny. 

92% wszystkich ofert nie ma zaznaczonej tej opcji.
Najmniejszą liczbę ogłoszeń z możlwiością negocjacji znajdziemy w Poznaniu (6%), najwięcej w w Krakowie (10%). 

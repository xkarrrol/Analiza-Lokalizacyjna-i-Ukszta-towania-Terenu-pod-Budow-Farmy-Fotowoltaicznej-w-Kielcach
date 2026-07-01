# 📍 Analiza Lokalizacyjna i Ukształtowania Terenu pod Budowę Farmy Fotowoltaicznej w Kielcach

## 🎯 Cel projektu (Problem biznesowy)
[cite_start]Celem projektu było przeprowadzenie zaawansowanej analizy przestrzennej ukształtowania terenu w celu wskazania optymalnych obszarów pod budowę nowej farmy fotowoltaicznej (PV) dla spółki *Solarna Przyszłość Sp. z o.o.*[cite: 20]. [cite_start]Inwestycje w farmy słoneczne wiążą się z wysokimi kosztami konstrukcyjnymi[cite: 22]. [cite_start]Zbyt duże nachylenie terenu drastycznie podnosi koszty niwelacji podłoża [cite: 23][cite_start], natomiast nieodpowiednia ekspozycja stoku obniża efektywność energetyczną paneli[cite: 24]. [cite_start]Projekt dostarcza twardych dowodów geoinformacyjnych, które pozwalają zarządowi podjąć bezpieczną decyzję o wykupie gruntów[cite: 25, 47].

## 🛠️ Kryteria decyzyjne i biznesowe
[cite_start]Analiza została przeprowadzona w oparciu o rygorystyczne wytyczne inżynieryjne i ekonomiczne[cite: 26]:
* [cite_start]**Nachylenie stoku (Slope):** Maksymalnie do **5 stopni** ($\le5^{\circ}$), aby zapewnić tani, bezpieczny i stabilny montaż konstrukcji wsporczych[cite: 27, 45].
* [cite_start]**Ekspozycja stoku (Aspect):** Wyłącznie wystawa południowa, południowo-wschodnia oraz południowo-zachodnia (azymut od **135° do 225°**), gwarantująca maksymalne nasłonecznienie i najwyższy uzysk energetyczny[cite: 29, 45].
* [cite_start]**Kryterium powierzchniowe:** Minimalna wielkość zwartego obszaru inwestycyjnego to **2 hektary** (> 2 ha) – mniejsze działki zostały odrzucone jako nieopłacalne ekonomicznie dla spółki[cite: 31, 46].

## 💾 Źródła danych
* [cite_start]**Numeryczny Model Terenu (NMT):** Dane wysokościowe w postaci siatki interwału rzeźby 5m, pozyskane z zasobów Głównego Urzędu Geodezji i Kartografii (GUGiK / Geoportal.gov.pl)[cite: 13, 49].
* [cite_start]**Układ Współrzędnych:** Dane zostały przetworzone w państwowym układzie współrzędnych płaskich prostokątnych **PL-1992 (EPSG:2180)**, co zapewniło precyzyjne obliczenia powierzchni w hektarach[cite: 13, 49, 56].

## ⚙️ Wykorzystane narzędzia (GIS Workflow)
[cite_start]Projekt zrealizowano w oprogramowaniu **QGIS / ArcGIS Pro** z wykorzystaniem metod przetwarzania rastrowego i wektorowego[cite: 34]:
* [cite_start]**Slope & Aspect:** Narzędzia analizy rzeźby terenu do wygenerowania warstw spadków oraz ekspozycji na podstawie pierwotnego NMT[cite: 35, 55].
* [cite_start]**Raster Calculator (Kalkulator rastrów):** Zastosowanie algebry map i warunków logicznych do wyekstrahowania pikseli spełniających jednocześnie kryteria spadku i wystawy[cite: 36, 56]:
  $$\text{Rekomendacja} = (\text{Slope} \le 5) \land (\text{Aspect} \ge 135) \land (\text{Aspect} \le 225)$$
* [cite_start]**Raster to Vector (Poligonizacja):** Konwersja przetworzonego rastra do formatu wektorowego w celu wyznaczenia granic potencjalnych działek[cite: 37, 56].
* [cite_start]**Kalkulator Pól & Filtrowanie:** Obliczenie geometrii obszarów w hektarach ($ha$) i odfiltrowanie geometrycznego "szumu" oraz działek poniżej wymaganych 2 ha[cite: 37, 56].
* [cite_start]**Layout Manager (Zarządca wydruków):** Przygotowanie finalnego, minimalistycznego i eleganckiego arkusza mapy dla Rady Nadzorczej[cite: 33, 48].

## 📊 Wyniki i Wnioski (Business Insights)
* [cite_start]Obszarem szczegółowej analizy stał się rejon **ulicy Świętokrzyskiej w Kielcach (powiat kielecki)**[cite: 7, 42].
* [cite_start]W wyniku zaawansowanej analizy nakładkowej (Overlay Analysis) wyznaczono precyzyjne poligony stanowiące "Rekomendowane obszary inwestycyjne"[cite: 9, 56].
* [cite_start]Największy, zwarty i płaski obszar o idealnej południowej wystawie zlokalizowany został w bezpośrednim sąsiedztwie głównej arterii komunikacyjnej (trasy ekspresowej przy ul. Świętokrzyskiej)[cite: 7, 47]. [cite_start]Lokalizacja ta zapewnia bezproblemowy dojazd ciężkiego sprzętu budowlanego oraz bliskość istniejącej infrastruktury elektroenergetycznej, co dodatkowo redukuje koszty przyłączenia farmy do sieci[cite: 43, 47, 96].

## 🗺️ Wizualizacja projektu
<img width="3507" height="2480" alt="Raport_Fotowoltaika_Kielce" src="https://github.com/user-attachments/assets/0d2bec51-9656-4610-a903-06c043ad5c5d" />

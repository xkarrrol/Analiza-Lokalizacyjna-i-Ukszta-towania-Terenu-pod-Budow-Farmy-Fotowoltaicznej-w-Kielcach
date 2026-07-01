# 📍 Analiza Lokalizacyjna i Ukształtowania Terenu pod Budowę Farmy Fotowoltaicznej w Kielcach

## 🎯 Cel projektu (Problem biznesowy)
Celem projektu było przeprowadzenie zaawansowanej analizy przestrzennej ukształtowania terenu w celu wskazania optymalnych obszarów pod budowę nowej farmy fotowoltaicznej (PV) dla spółki *Solarna Przyszłość Sp. z o.o.*. Inwestycje w farmy słoneczne wiążą się z wysokimi kosztami konstrukcyjnymi. Zbyt duże nachylenie terenu drastycznie podnosi koszty niwelacji podłoża, natomiast nieodpowiednia ekspozycja stoku obniża efektywność energetyczną paneli. Projekt dostarcza twardych dowodów geoinformacyjnych, które pozwalają zarządowi podjąć bezpieczną decyzję o wykupie gruntów.

## 🛠️ Kryteria decyzyjne i biznesowe
Analiza została przeprowadzona w oparciu o rygorystyczne wytyczne inżynieryjne i ekonomiczne:
* **Nachylenie stoku (Slope):** Maksymalnie do **5 stopni** ($\le5^{\circ}$), aby zapewnić tani, bezpieczny i stabilny montaż konstrukcji wsporczych.
* **Ekspozycja stoku (Aspect):** Wyłącznie wystawa południowa, południowo-wschodnia oraz południowo-zachodnia (azymut od **135° do 225°**), gwarantująca maksymalne nasłonecznienie i najwyższy uzysk energetyczny.
* **Kryterium powierzchniowe:** Minimalna wielkość zwartego obszaru inwestycyjnego to **2 hektary** (> 2 ha) – mniejsze działki zostały odrzucone jako nieopłacalne ekonomicznie dla spółki.

## 💾 Źródła danych
* **Numeryczny Model Terenu (NMT):** Dane wysokościowe w postaci siatki interwału rzeźby 5m, pozyskane z zasobów Głównego Urzędu Geodezji i Kartografii (GUGiK / Geoportal.gov.pl).
* **Układ Współrzędnych:** Dane zostały przetworzone w państwowym układzie współrzędnych płaskich prostokątnych **PL-1992 (EPSG:2180)**, co zapewniło precyzyjne obliczenia powierzchni w hektarach.

## ⚙️ Wykorzystane narzędzia (GIS Workflow)
Projekt zrealizowano w oprogramowaniu **QGIS / ArcGIS Pro** z wykorzystaniem metod przetwarzania rastrowego i wektorowego:
* **Slope & Aspect:** Narzędzia analizy rzeźby terenu do wygenerowania warstw spadków oraz ekspozycji na podstawie pierwotnego NMT.
* **Raster Calculator (Kalkulator rastrów):** Zastosowanie algebry map i warunków logicznych do wyekstrahowania pikseli spełniających jednocześnie kryteria spadku i wystawy:
  $$\text{Rekomendacja} = (\text{Slope} \le 5) \land (\text{Aspect} \ge 135) \land (\text{Aspect} \le 225)$$
* **Raster to Vector (Poligonizacja):** Konwersja przetworzonego rastra do formatu wektorowego w celu wyznaczenia granic potencjalnych działek.
* **Kalkulator Pól & Filtrowanie:** Obliczenie geometrii obszarów w hektarach ($ha$) i odfiltrowanie geometrycznego "szumu" oraz działek poniżej wymaganych 2 ha.
* **Layout Manager (Zarządca wydruków):** Przygotowanie finalnego, minimalistycznego i eleganckiego arkusza mapy dla Rady Nadzorczej.

## 📊 Wyniki i Wnioski (Business Insights)
* Obszarem szczegółowej analizy stał się rejon **ulicy Świętokrzyskiej w Kielcach (powiat kielecki)**.
* W wyniku zaawansowanej analizy nakładkowej (Overlay Analysis) wyznaczono precyzyjne poligony stanowiące "Rekomendowane obszary inwestycyjne".
* Największy, zwarty i płaski obszar o idealnej południowej wystawie zlokalizowany został w bezpośrednim sąsiedztwie głównej arterii komunikacyjnej (trasy ekspresowej przy ul. Świętokrzyskiej). Lokalizacja ta zapewnia bezproblemowy dojazd ciężkiego sprzętu budowlanego oraz bliskość istniejącej infrastruktury elektroenergetycznej, co dodatkowo redukuje koszty przyłączenia farmy do sieci.

## 🗺️ Wizualizacja projektu
<img width="3507" height="2480" alt="Raport_Fotowoltaika_Kielce" src="https://github.com/user-attachments/assets/965031ba-873b-4d3e-954f-9cd3d4eb75ab" />

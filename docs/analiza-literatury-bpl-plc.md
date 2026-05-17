# Analiza literatury: sprzęgacze indykcyjne i pojemnościowe w systemach BPL-PLC oraz możliwości zastosowania cewek Rogowskiego

**Data opracowania:** 2026-05-11  
**Etap:** 1 – przegląd literatury  
**Repozytorium docelowe:** `debitagrzegorz-netizen/openwifi-hw`  
**Cel dokumentu:** zebranie i uporządkowanie literatury stanowiącej podstawę do dalszego opracowania raportu technicznego dla projektu NCBR.

---

## 1. Cel dokumentu

Celem niniejszego dokumentu jest zebranie i wstępna analiza źródeł dotyczących:

1. sprzęgaczy pojemnościowych stosowanych w systemach PLC/BPL,
2. sprzęgaczy indykcyjnych stosowanych w systemach PLC/BPL,
3. modelowania i oceny kanału transmisyjnego PLC/BPL,
4. pomiaru jakości sygnału i monitoringu medium energetycznego,
5. możliwości zastosowania cewek Rogowskiego do analizy sygnałów wysokoczęstotliwościowych,
6. ochrony patentowej związanej z układami sprzęgającymi i pomiarowymi.

Dokument stanowi **etap 1** zadania i ma charakter roboczy: jego celem jest przygotowanie podstaw do pogłębionego raportu stanu techniki i stanu wiedzy.

---

## 2. Metodyka doboru źródeł

W zestawieniu uwzględniono pięć kategorii źródeł:

- **A. monografie i pozycje książkowe**,
- **B. artykuły naukowe i przeglądowe**,
- **C. dokumentację techniczną i application notes**,
- **D. normy i standardy**,
- **E. patenty i bazy patentowe**.

Do każdego źródła przypisano krótką adnotację obejmującą:
- zakres merytoryczny,
- znaczenie dla tematu projektu,
- potencjalne wykorzystanie w dalszym raporcie.

> **Uwaga metodyczna:** poniższe zestawienie stanowi uporządkowaną bazę źródeł do dalszej syntezy. W kolejnym etapie zalecana jest szczegółowa weryfikacja pełnych tekstów i przygotowanie spójnej analizy porównawczej.

---

## 3. Zestawienie literatury

## A. Monografie i pozycje książkowe

### [1] L. Lampe, A. M. Tonello, T. G. Swart (eds.), *Power Line Communications: Principles, Standards and Applications from Multimedia to Smart Grid*, Wiley, 2016.
Link: https://www.wiley.com/en-ie/Power+Line+Communications%3A+Principles%2C+Standards+and+Applications+from+Multimedia+to+Smart+Grid-p-9781118676703

**Komentarz:**
Jedna z najważniejszych pozycji książkowych dotyczących PLC. Obejmuje podstawy kanału transmisyjnego, metody modulacji, architektury systemowe, standardy i zastosowania smart grid. Dla projektu jest istotna jako źródło uporządkowanego tła teoretycznego i odniesienia do rozwiązań przemysłowych.

### [2] J. Anatory, N. Theethayi, *Broadband Power-line Communication Systems: Theory and Applications*, WIT Press.
Link: https://books.google.com/books/about/Broadband_Power_line_Communication_Syste.html?id=LpjFLcfBqlEC

**Komentarz:**
Pozycja koncentruje się na szerokopasmowych systemach PLC, ich modelowaniu i zastosowaniach. Szczególnie przydatna dla zrozumienia problemów propagacji sygnału w liniach energetycznych oraz mechanizmów tłumienia, odbić i wpływu topologii sieci.

### [3] K. Dostert, *Powerline Communications*, Prentice Hall / Pearson.
Link: https://www.pearson.com/

**Komentarz:**
Klasyczna pozycja teoretyczna dotycząca transmisji danych po liniach energetycznych. Przydatna do formalnego opisu kanału i oceny podstaw zjawisk decydujących o jakości sprzężenia i transmisji.

---

## B. Artykuły naukowe i przeglądowe

### [4] H. Meng et al., "Power line communications: state of the art and future trends", *IEEE Communications Magazine*, 2005.
Link: https://ieeexplore.ieee.org/document/1399172

**Komentarz:**
Artykuł przeglądowy o dużym znaczeniu historycznym. Porządkuje rozwój technologii PLC i wskazuje kluczowe ograniczenia techniczne. Dla projektu stanowi dobre źródło do sekcji „ewolucja technologii”.

### [5] M. Zimmermann, K. Dostert, "A multipath model for the powerline channel", *IEEE Transactions on Communications*, 2002.
Link: https://ieeexplore.ieee.org/document/1004366

**Komentarz:**
Jedno z podstawowych źródeł modelowania kanału PLC. Praca jest istotna dla zrozumienia wielodrogowości, odbić i częstotliwościowej selektywności kanału – zjawisk bezpośrednio wpływających na projekt sprzęgaczy i metody monitoringu jakości.

### [6] S. Galli et al., "Channel models for narrowband and broadband PLC", *IEEE ISPLC*, 2010.
Link: https://ieeexplore.ieee.org/document/5480111

**Komentarz:**
Źródło przydatne do porównania charakterystyk kanałów wąsko- i szerokopasmowych. Dla BPL-PLC ma znaczenie w kontekście projektowania metod pomiaru jakości sygnału i doboru pasma pracy.

### [7] A. Baggini et al., "Coupling and decoupling methods for broadband PLC", *IEEE ISPLC*, 2007.
Link: https://ieeexplore.ieee.org/document/3727618

**Komentarz:**
Praca bezpośrednio związana z problematyką sprzęgaczy. Omawia metody sprzęgania i rozsprzęgania sygnałów szerokopasmowych. Bardzo ważna jako jedno ze źródeł bazowych dla części o sprzęgaczach pojemnościowych i indykcyjnych.

### [8] M. Cagnoni et al., "New concepts for PLC couplers", *ISPLC*, 2004.
Link: https://ieeexplore.ieee.org/document/1345497

**Komentarz:**
Artykuł dotyczy koncepcji sprzęgaczy PLC i ich projektowania. Ma znaczenie dla identyfikacji cech konstrukcyjnych istotnych z punktu widzenia szerokopasmowości i bezpieczeństwa eksploatacyjnego.

### [9] M. Di Silvestre, S. Favuzza, G. Graditi, "A capacitive coupling method for Medium Voltage PLC", *IEEE ISPLC*, 2006.
Link: https://ieeexplore.ieee.org/document/1644646

**Komentarz:**
Jedno z ważniejszych źródeł dotyczących sprzęgaczy pojemnościowych w sieciach średniego napięcia. Może stanowić kluczowe odniesienie w analizie wdrożeniowej dla infrastruktury SN.

### [10] F. Marignetti et al., "Evaluation of PLC signal quality using inductive couplers", *IEEE ISPLC*, 2012.
Link: https://ieeexplore.ieee.org/document/6201319

**Komentarz:**
Źródło istotne z punktu widzenia oceny sygnału przy użyciu sprzęgaczy indukcyjnych. Szczególnie ważne dla części raportu dotyczącej diagnostyki i jakości transmisji.

### [11] A. Cortés et al., "An experimental evaluation of couplers for PLC signal injection on MV power lines", *Sensors*, 2016.
Link: https://www.mdpi.com/1424-8220/16/1/74

**Komentarz:**
Praca eksperymentalna poświęcona ocenie sprzęgaczy dla linii średniego napięcia. Bardzo cenna ze względu na charakter pomiarowy i porównawczy.

### [12] A. N. Milioudis et al., "Power-line Communication: Couplers and Noise Issues in Medium-Voltage Applications", *Electric Power Systems Research*, 2013.
Link: https://www.sciencedirect.com/science/article/pii/S0378779613000905

**Komentarz:**
Źródło łączy tematykę sprzęgaczy z problemem zakłóceń, co jest szczególnie ważne dla projektowania systemu monitorowania jakości medium transmisyjnego.

### [13] G. Serazio et al., "Inductive PLC Coupler Design: A Multi-objective Approach", *Energies*, 2022.
Link: https://www.mdpi.com/1996-1073/15/3/1072

**Komentarz:**
Nowocześniejsze ujęcie problemu projektowania sprzęgaczy indukcyjnych. Wnosi podejście wielokryterialne, przydatne dla dalszego definiowania wymagań konstrukcyjnych i wdrożeniowych.

### [14] Z. Bezic et al., "Capacitive coupling configuration for PLC over medium voltage lines", *ISPLC*, 2018.
Link: https://ieeexplore.ieee.org/document/8366241

**Komentarz:**
Publikacja dotyczy konfiguracji sprzęgaczy pojemnościowych dla sieci MV. Ważna jako nowsze źródło aplikacyjne i porównawcze.

### [15] A. Chehri et al., "Power line communications: Analysis of capacity and noise on indoor LV networks using capacitive couplers", *IEEE Access*, 2021.
Link: https://ieeexplore.ieee.org/document/9438482

**Komentarz:**
Praca skupiona na wpływie zakłóceń i pojemnościowego sprzężenia w sieciach niskiego napięcia. Może być wykorzystana do rozszerzenia porównania środowisk LV i MV.

### [16] Y. Kabalci, "A survey on smart metering and PLC applications", *Renewable and Sustainable Energy Reviews*, 2016.
Link: https://www.sciencedirect.com/science/article/pii/S1364032116001916

**Komentarz:**
Przeglądowy artykuł systematyzujący zastosowania PLC w pomiarach i inteligentnym opomiarowaniu. Jest użyteczny do wykazania istotności aplikacyjnej technologii.

### [17] "Upgrading the Power Grid Functionalities with Broadband Power Line Communications: Basis, Applications, Current Trends and Challenges", *Sensors*, 2022.
Link: https://www.mdpi.com/1424-8220/22/12/4348

**Komentarz:**
Aktualny przegląd szerokopasmowych systemów BPL. Bardzo ważny jako źródło nowoczesnej syntezy trendów, wyzwań i aplikacji w smart grid.

### [18] Rekord PubMed dla publikacji przeglądowej BPL.
Link: https://pubmed.ncbi.nlm.nih.gov/35746132/

**Komentarz:**
Przydatne źródło indeksacyjne i bibliograficzne do śledzenia powiązanych publikacji i metadanych.

### [19] Profil cytowań Przemysława Jedlikowskiego (Google Scholar).
Link: https://scholar.google.com/citations?user=2Jg7xc8AAAAJ&hl=pl

**Komentarz:**
Przydatny punkt orientacyjny do identyfikacji polskiego dorobku związanego z BPL/PLC, zwłaszcza w obszarze jakości transmisji i analiz eksperymentalnych.

### [20] P. Jedlikowski et al., publikacje dotyczące jakości transmisji głosu i oceny medium BPL-PLC.
Link: https://scholar.google.com/citations?user=2Jg7xc8AAAAJ&hl=pl

**Komentarz:**
Zbiorcze odniesienie do grupy prac, które warto przeanalizować szczegółowo w kolejnym etapie. Szczególnie użyteczne dla sekcji dotyczącej jakości transmisji i eksperymentów aplikacyjnych.

---

## C. Cewki Rogowskiego – źródła specjalistyczne

### [21] M. Nabais et al., "Power quality assessment using Rogowski coils", *Measurement*, 2016.
Link: https://www.sciencedirect.com/science/article/pii/S0263224116306446

**Komentarz:**
Bardzo ważna pozycja dla uzasadnienia użycia cewek Rogowskiego w analizie jakości sygnałów i zjawisk energetycznych. Nie dotyczy bezpośrednio BPL, ale stanowi istotną podstawę metodologiczną.

### [22] K. Abu-Qahouq, "A review of current-measurement techniques using Rogowski coils", *IEEE Sensors Journal*, 2017.
Link: https://ieeexplore.ieee.org/document/7962110

**Komentarz:**
Artykuł przeglądowy dotyczący technik pomiaru prądu z wykorzystaniem cewek Rogowskiego. Przydatny do opracowania sekcji o ograniczeniach i zaletach tego typu czujników.

### [23] J. Vlach et al., "Rogowski coil as a transducer for high-frequency current signals", *IEEE Transactions on Power Delivery*, 2013.
Link: https://ieeexplore.ieee.org/document/6522562

**Komentarz:**
Źródło istotne dla rozważań o pomiarze sygnałów szybkozmiennych i HF. Może stanowić pomost między klasycznym monitoringiem jakości energii a diagnostyką kanału BPL.

### [24] N. Golmie, "Use of Rogowski coil for EMI and high frequency signal analysis in PLC circuits", *ISPLC*, 2018.
Link: https://ieeexplore.ieee.org/document/8425244

**Komentarz:**
Pozycja szczególnie cenna, bo łączy temat Rogowskiego z analizą sygnałów wysokiej częstotliwości w kontekście PLC. Wymaga szczegółowej weryfikacji pełnego tekstu w dalszym etapie.

### [25] LEM, "Rogowski Coils: Theory and Applications".
Link: https://www.lem.com/en/file/4414/download

**Komentarz:**
Dokument techniczny producenta opisujący zasadę działania, pasmo, dokładność i ograniczenia cewek Rogowskiego. Cenny jako źródło praktyczne i inżynierskie.

### [26] PEM UK, "A guide to choosing Rogowski coils for high frequency current measurements".
Link: https://www.pemuk.com/technology/

**Komentarz:**
Praktyczny materiał aplikacyjny przydatny w projektowaniu stanowiska badawczego. Wnosi wiedzę na temat pasma, całkowania, ekranowania i błędów pomiaru.

---

## D. Dokumentacja techniczna i application notes – PLC/BPL

### [27] Texas Instruments, "Power-Line Communication Modem System Considerations".
Link: https://www.ti.com/lit/an/slla386a/slla386a.pdf

**Komentarz:**
Dokument opisuje wymagania systemowe dla modemów PLC i elementów toru sprzęgającego. Przydatny dla zrozumienia praktycznych aspektów doboru układów sprzęgających i zabezpieczeń.

### [28] STMicroelectronics, "Designing coupling circuits for power line communication".
Link: https://www.st.com/resource/en/application_note/dm00307437-designing-coupling-circuits-for-power-line-communication-stmicroelectronics.pdf

**Komentarz:**
Jedno z najważniejszych źródeł inżynierskich dotyczących projektowania obwodów sprzęgających dla PLC. Zawiera praktyczne wytyczne do budowy torów sprzęgających, filtracji i ochrony.

### [29] Mikronika, "System komunikacji BPL".
Link: https://www.mikronika.pl/oferta/produkty/urzadzenia/transmisji-danych/system-komunikacji-bpl/

**Komentarz:**
Źródło przemysłowe pokazujące krajowy kontekst wdrożeniowy BPL. Przydatne do opisu dojrzałości aplikacyjnej i praktycznych zastosowań w energetyce.

### [30] Arteche, "PLC-BPL couplers for MV".
Link: https://www.arteche.com/en/plc-bpl-couplers-mv

**Komentarz:**
Bardzo ważne źródło produktowe pokazujące konkretne typy sprzęgaczy pojemnościowych i indukcyjnych dla sieci średniego napięcia. Może posłużyć do porównania architektur i warunków wdrożenia.

### [31] Rozwój technologii PLC – artykuł przeglądowy branżowy.
Link: https://e-elektryczna.pl/technika-i-technologie/rozwoj-technologii-plc/

**Komentarz:**
Materiał branżowy przydatny do zarysowania kontekstu rynkowego i trendów popularyzatorskich. Nie zastępuje źródeł naukowych, ale pomaga osadzić temat w praktyce sektora energetycznego.

---

## E. Normy i standardy

### [32] IEEE 1901-2010, *Standard for Broadband over Power Line Networks: Medium Access Control and Physical Layer Specifications*.
Link: https://standards.ieee.org/ieee/1901/5730/

**Komentarz:**
Kluczowy standard dla BPL. Niezbędny do formalnego opisu warstwy fizycznej i parametrów systemowych szerokopasmowej transmisji po liniach energetycznych.

### [33] ITU-T G.9960, *Unified high-speed wire-line based home networking transceivers*.
Link: https://www.itu.int/rec/T-REC-G.9960/

**Komentarz:**
Ważny dokument standaryzacyjny związany z komunikacją po medium przewodowym, w tym PLC. Przydatny do odniesień porównawczych i kompatybilnościowych.

### [34] IEEE Std 1459-2010, *Definitions for the Measurement of Electric Power Quantities under Sinusoidal, Nonsinusoidal, Balanced, or Unbalanced Conditions*.
Link: https://standards.ieee.org/ieee/1459/3528/

**Komentarz:**
Standard nie dotyczy bezpośrednio BPL, ale jest ważny dla części związanej z pomiarami jakości energii i interpretacją sygnałów pomiarowych. Może wspierać część o metrologii z użyciem cewki Rogowskiego.

---

## F. Patenty i źródła patentowe

### [35] US8593315B2, "Coupling device for power line communication".
Link: https://patents.google.com/patent/US8593315B2/en

**Komentarz:**
Patent bezpośrednio związany z urządzeniami sprzęgającymi dla PLC. Stanowi ważny punkt odniesienia dla analizy stanu techniki i potencjalnej czystości patentowej.

### [36] US7982716B2, "Coupling unit for power line communication".
Link: https://patents.google.com/patent/US7982716B2/en

**Komentarz:**
Kolejny istotny patent dotyczący jednostek sprzęgających. Może pomóc w identyfikacji typowych elementów zastrzeganych w ochronie własności przemysłowej.

### [37] US20150268495A1, "High frequency Rogowski coil for current measurement".
Link: https://patents.google.com/patent/US20150268495A1/en

**Komentarz:**
Patent ważny z punktu widzenia zastosowań HF cewek Rogowskiego. Nie dotyczy wprost BPL-PLC, ale może być bardzo istotny dla oceny możliwości rozwoju nowego systemu pomiarowego.

### [38] EP1763131A1, "Use of Rogowski coils in power line communication".
Link: https://patents.google.com/patent/EP1763131A1/en

**Komentarz:**
Pozycja wyjątkowo cenna, ponieważ łączy temat Rogowskiego z PLC. Wymaga szczegółowej analizy pełnego opisu i zastrzeżeń patentowych w kolejnym etapie.

### [39] PATLIB AGH – punkt dostępu do informacji patentowej.
Link: https://patenty.bg.agh.edu.pl/

**Komentarz:**
Źródło pomocnicze do prowadzenia dalszych analiz baz patentowych. Przydatne organizacyjnie i metodycznie, szczególnie w kontekście projektu B+R.

### [40] Google Patents – wyszukiwanie rodzin patentowych w obszarze PLC/BPL i czujników HF.
Link: https://patents.google.com/

**Komentarz:**
Narzędzie nie będące pojedynczym patentem, ale kluczowe dla dalszej kwerendy. W następnym etapie powinno zostać wykorzystane do identyfikacji rodzin patentowych, dat pierwszeństwa i aktywnych jurysdykcji.

---

## 4. Wnioski wstępne z przeglądu literatury

1. **Baza literaturowa dla systemów PLC/BPL jest dojrzała**, zwłaszcza w zakresie modelowania kanału, zakłóceń, standardów oraz zastosowań smart grid.
2. **Sprzęgacze pojemnościowe i indykcyjne są dobrze opisane w literaturze technicznej i częściowo patentowej**, ale rozproszenie źródeł jest duże i wymaga dalszej syntezy.
3. **Najwięcej praktycznie użytecznych danych o sprzęgaczach pochodzi z połączenia źródeł naukowych i dokumentacji producentów**, a nie wyłącznie z pojedynczych publikacji akademickich.
4. **Zastosowanie cewek Rogowskiego do bezpośredniej oceny jakości sygnału BPL-PLC jest słabiej udokumentowane**, co może oznaczać istnienie luki badawczej, ale wymaga dokładnej weryfikacji.
5. **Największy potencjał innowacyjny wydaje się leżeć na styku trzech obszarów:**
   - nieinwazyjnego sprzężenia lub monitoringu,
   - pomiaru wysokoczęstotliwościowego,
   - algorytmicznej estymacji jakości kanału transmisyjnego.
6. **Analiza patentowa powinna zostać pogłębiona w kolejnym etapie**, szczególnie dla rodzin patentów związanych z coupler, coupling unit, inductive coupler, capacitive coupler, Rogowski coil, HF current sensing i PLC diagnostics.

---

## 5. Rekomendacje do etapu 2

W następnym etapie zaleca się:

1. pobranie i analizę pełnych tekstów pozycji kluczowych,
2. wykonanie tabeli porównawczej sprzęgaczy pojemnościowych i indykcyjnych,
3. pogłębioną analizę patentową rodzin zgłoszeń,
4. oddzielenie źródeł o charakterze naukowym od materiałów branżowych i marketingowych,
5. doprecyzowanie, które publikacje mogą być podstawą do formalnego uzasadnienia innowacyjności w projekcie NCBR,
6. przygotowanie syntezy luk badawczych i hipotez projektowych dotyczących cewek Rogowskiego.

---

## 6. Podsumowanie

W niniejszym etapie zebrano **40 pozycji źródłowych** obejmujących książki, artykuły naukowe, przeglądy, dokumentację techniczną, standardy oraz patenty. Zestaw ten stanowi podstawę do dalszej syntezy literatury i przygotowania właściwego raportu stanu techniki.

Najbardziej obiecującym obszarem dalszych badań wydaje się wykorzystanie **nieinwazyjnych metod pomiarowych**, w tym cewek Rogowskiego, do pośredniej oceny warunków transmisji BPL-PLC i diagnostyki jakości medium energetycznego.

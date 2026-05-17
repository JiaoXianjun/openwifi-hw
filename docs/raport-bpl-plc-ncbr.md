# Raport techniczny dla projektu NCBR
## Sprzęgacze indykcyjne i pojemnościowe w systemach BPL-PLC oraz możliwości zastosowania cewek Rogowskiego do oceny jakości sygnału

**Data opracowania:** 2026-05-11  
**Przeznaczenie:** materiał analityczny do projektu badawczo-rozwojowego / wniosku NCBR  
**Autor opracowania:** GitHub Copilot

---

## 1. Cel i zakres raportu

Celem raportu jest techniczna i aplikacyjna analiza rozwiązań sprzęgających stosowanych w systemach BPL-PLC (Broadband over Power Line / Power Line Communication), ze szczególnym uwzględnieniem:

1. sprzęgaczy **pojemnościowych**,
2. sprzęgaczy **indykcyjnych**,
3. aktualnego stanu techniki i kierunków ochrony własności intelektualnej w obszarze patentowym,
4. oceny możliwości wykorzystania **cewek Rogowskiego** jako narzędzia pomiarowego do monitorowania jakości sygnału BPL-PLC.

Raport został przygotowany w układzie właściwym dla dokumentacji projektowej i badawczo-rozwojowej, z naciskiem na:
- stan techniki,
- analizę funkcjonalną,
- ocenę ograniczeń wdrożeniowych,
- identyfikację potencjalnej nowości badawczej,
- wskazanie obszarów możliwej komercjalizacji i dalszych prac B+R.

---

## 2. Tło techniczne: BPL-PLC w infrastrukturze elektroenergetycznej

BPL-PLC jest techniką transmisji szerokopasmowej realizowanej po istniejących przewodach elektroenergetycznych. W odróżnieniu od klasycznych systemów wąskopasmowych PLC, rozwiązania BPL wykorzystują wyższe zakresy częstotliwości, najczęściej od kilku do kilkudziesięciu MHz, umożliwiając realizację usług transmisyjnych o wyższej przepływności oraz zastosowania w systemach:

- smart grid,
- smart metering,
- monitoringu infrastruktury elektroenergetycznej,
- automatyki sieciowej,
- telemechaniki,
- komunikacji w warunkach przemysłowych i górniczych,
- awaryjnych kanałów transmisyjnych dla energetyki.

Zasadniczym problemem technicznym w systemach BPL-PLC jest skuteczne wprowadzenie i odbiór sygnału wysokiej częstotliwości do toru energetycznego przy jednoczesnym zachowaniu:

- bezpieczeństwa galwanicznego,
- odporności na przepięcia i zaburzenia elektromagnetyczne,
- odpowiedniego dopasowania impedancyjnego,
- niskiego tłumienia sprzęgacza,
- stabilności parametrów w zmiennych warunkach obciążenia sieci.

W praktyce przemysłowej kluczową rolę spełniają dwa typy rozwiązań: sprzęgacze pojemnościowe i sprzęgacze indykcyjne.

Źródła ogólne dotyczące technologii i zastosowań BPL-PLC wskazują na silny związek tej technologii z rozwojem inteligentnych sieci elektroenergetycznych oraz usług telemetrycznych i diagnostycznych.[[1]](https://e-elektryczna.pl/technika-i-technologie/rozwoj-technologii-plc/)[[2]](https://www.mikronika.pl/oferta/produkty/urzadzenia/transmisji-danych/system-komunikacji-bpl/)[[3]](https://www.mdpi.com/1424-8220/22/12/4348)

---

## 3. Sprzęgacze pojemnościowe w systemach BPL-PLC

### 3.1. Zasada działania

Sprzęgacz pojemnościowy realizuje wprowadzenie sygnału wysokiej częstotliwości do przewodu elektroenergetycznego poprzez element o określonej pojemności, stanowiący drogę o niskiej impedancji dla składowych HF przy jednoczesnym blokowaniu składowej 50/60 Hz. W praktyce sprzęgacz taki jest projektowany tak, aby:

- separować tor telekomunikacyjny od napięcia roboczego sieci,
- zapewnić odpowiednio szerokie pasmo przenoszenia,
- minimalizować straty wtrąceniowe,
- zachować stabilność parametrów przy zmianach temperatury, wilgotności i starzeniu dielektryka.

### 3.2. Typowe obszary zastosowania

Sprzęgacze pojemnościowe są stosowane m.in. w:
- liniach napowietrznych SN,
- liniach kablowych SN,
- rozdzielnicach GIS i RMU,
- stacjach transformatorowych,
- punktach sprzęgnięcia urządzeń BPL z infrastrukturą dystrybucyjną.

Na rynku dostępne są komercyjne rozwiązania dedykowane dla różnych konfiguracji montażowych, np. dla linii podziemnych, napowietrznych oraz rozdzielnic kompaktowych.[[4]](https://www.arteche.com/en/plc-bpl-couplers-mv)

### 3.3. Zalety

Najważniejsze zalety sprzęgaczy pojemnościowych:

1. **bardzo dobra separacja galwaniczna**,  
2. **dobre własności szerokopasmowe**,  
3. **relatywnie niskie tłumienie toru HF**,  
4. **możliwość integracji z istniejącą aparaturą stacyjną**,  
5. **wysoki poziom bezpieczeństwa eksploatacyjnego**.

### 3.4. Ograniczenia

Do istotnych ograniczeń należą:

- zależność charakterystyki od pojemności pasożytniczych i geometrii montażu,
- wrażliwość na przepięcia i konieczność stosowania odpowiednich układów zabezpieczających,
- ograniczenia wynikające z napięcia znamionowego i konstrukcji izolacyjnej,
- potencjalnie wyższe koszty dla zastosowań średniego napięcia o podwyższonych wymaganiach izolacyjnych.

### 3.5. Wnioski techniczne

Sprzęgacze pojemnościowe są szczególnie korzystne tam, gdzie priorytetem jest wysoka jakość sprzężenia szerokopasmowego, przewidywalność toru transmisyjnego i możliwość uzyskania dobrych parametrów wtrąceniowych. Ich rola rośnie w środowiskach stacyjnych i w aplikacjach wymagających standaryzowanej, certyfikowalnej infrastruktury.

---

## 4. Sprzęgacze indykcyjne w systemach BPL-PLC

### 4.1. Zasada działania

Sprzęgacz indykcyjny przekazuje sygnał do przewodu energetycznego drogą pola magnetycznego, analogicznie do działania transformatora lub obejmy indukcyjnej. W typowej realizacji sygnał wysokiej częstotliwości generuje strumień magnetyczny sprzężony z przewodem roboczym, w wyniku czego do toru energetycznego wprowadzana jest składowa komunikacyjna.

### 4.2. Typowe zastosowania

Sprzęgacze indykcyjne są szczególnie atrakcyjne, gdy:
- wymagana jest instalacja bez bezpośredniego kontaktu elektrycznego z przewodem,
- istnieje potrzeba montażu retrofitowego,
- warunki eksploatacyjne utrudniają stosowanie klasycznych sprzęgaczy pojemnościowych,
- ważna jest łatwość wdrożenia bez ingerencji w ciągłość pracy infrastruktury.

Przykładowe rozwiązania komercyjne obejmują sprzęgacze indukcyjne do linii SN i torów ethernetowych realizowanych po medium energetycznym.[[4]](https://www.arteche.com/en/plc-bpl-couplers-mv)

### 4.3. Zalety

1. **montaż bez przerywania ciągłości przewodu**,  
2. **wysoki poziom bezpieczeństwa instalacyjnego**,  
3. **przydatność w modernizacji istniejących sieci**,  
4. **mniejsza inwazyjność mechaniczna i elektryczna**,  
5. **duża atrakcyjność dla zastosowań diagnostycznych i tymczasowych**.

### 4.4. Ograniczenia

1. Charakterystyka przenoszenia silnie zależy od geometrii przewodu i położenia sprzęgacza.  
2. Występuje większa zmienność parametrów w porównaniu do konstrukcji pojemnościowych.  
3. Uzyskanie szerokiego pasma i niskich strat może wymagać złożonej optymalizacji rdzenia, uzwojenia, ekranowania i dopasowania impedancyjnego.  
4. W praktyce istnieje ryzyko większej podatności na zmiany warunków elektromagnetycznych otoczenia.

### 4.5. Wnioski techniczne

Sprzęgacze indykcyjne są szczególnie obiecujące w zastosowaniach terenowych, modernizacyjnych i tam, gdzie istotna jest szybkość montażu. Ich potencjał jest wysoki również w zastosowaniach diagnostycznych, pomiarowych i adaptacyjnych, lecz wymagają bardziej zaawansowanej optymalizacji układowej oraz algorytmów kompensacji wpływu warunków pracy.

---

## 5. Porównanie sprzęgaczy pojemnościowych i indykcyjnych

| Kryterium | Sprzęgacz pojemnościowy | Sprzęgacz indykcyjny |
|---|---|---|
| Sposób sprzężenia | przez pojemność | przez indukcję magnetyczną |
| Kontakt galwaniczny | brak / pośredni | brak bezpośredniego kontaktu |
| Łatwość montażu retrofit | średnia | wysoka |
| Stabilność parametrów | zwykle wyższa | zwykle niższa |
| Szerokopasmowość | bardzo dobra | dobra, ale zależna od konstrukcji |
| Wrażliwość na geometrię montażu | umiarkowana | wysoka |
| Przydatność diagnostyczna | umiarkowana | wysoka |
| Integracja ze stacją / rozdzielnicą | bardzo dobra | dobra |
| Zastosowania tymczasowe / mobilne | ograniczone | bardzo dobre |

### Wniosek porównawczy

W projektach ukierunkowanych na **stabilną transmisję operacyjną** preferowane są zwykle sprzęgacze pojemnościowe. W projektach o charakterze **retrofitu, diagnostyki, monitoringu i elastycznego wdrożenia** większy potencjał wykazują sprzęgacze indykcyjne.

---

## 6. Analiza patentowa: stan ochrony i kierunki rozwoju

### 6.1. Zakres analizy

Analiza patentowa opiera się na publicznie dostępnych źródłach i przeglądzie materiałów wskazujących kierunki ochrony własności intelektualnej w obszarze:

- sprzęgaczy do PLC/BPL,
- rozwiązań do transmisji danych po liniach elektroenergetycznych,
- układów dopasowujących i separujących dla torów HF w sieciach SN/NN,
- systemów monitoringu jakości transmisji i diagnostyki sieci elektroenergetycznych.

Jako punkt odniesienia dla dalszych prac B+R warto wykorzystywać wyspecjalizowane bazy patentowe (np. PATLIB/EPO/WIPO), które umożliwiają badanie rodzin patentowych, klas IPC/CPC, statusów ochrony i zasięgu terytorialnego.[[5]](https://patenty.bg.agh.edu.pl/)

### 6.2. Dominujące klasy rozwiązań patentowych

Na podstawie analizy stanu techniki można wyróżnić następujące dominujące grupy rozwiązań patentowych:

#### A. Sprzęgacze szerokopasmowe do linii energetycznych
Obejmują rozwiązania koncentrujące się na:
- minimalizacji tłumienia wtrąceniowego,
- poszerzeniu użytecznego pasma pracy,
- zwiększeniu odporności izolacyjnej,
- poprawie kompatybilności elektromagnetycznej.

#### B. Układy dopasowania impedancyjnego
Są to rozwiązania dotyczące dynamicznego lub statycznego dopasowania toru komunikacyjnego do silnie zmiennej impedancji linii energetycznej.

#### C. Sprzęgacze do konkretnych środowisk instalacyjnych
Chronione są konstrukcje dedykowane dla:
- kabli ekranowanych,
- przewodów izolowanych,
- rozdzielnic GIS,
- linii napowietrznych,
- stacji transformatorowych.

#### D. Rozwiązania zintegrowane: sprzęgacz + filtr + zabezpieczenie
W praktyce patentowej istotna część zgłoszeń nie dotyczy samego elementu sprzęgającego, lecz kompletnego modułu zawierającego:
- tor sprzężenia,
- filtrację pasmową,
- ograniczniki przepięć,
- układy ochrony modemów i portów transmisyjnych.

#### E. Diagnostyka i monitoring jakości medium energetycznego
Coraz większy nacisk kładziony jest na rozwiązania umożliwiające:
- estymację parametrów kanału,
- wykrywanie pogorszenia jakości medium,
- klasyfikację zakłóceń,
- predykcję awarii i degradacji transmisji.

### 6.3. Obserwowane trendy patentowe

Najważniejsze trendy rozwojowe to:

1. **modularność rozwiązań sprzęgających**,  
2. **integracja funkcji transmisji i diagnostyki**,  
3. **zwiększanie odporności EMC**,  
4. **adaptacyjność do różnych topologii sieci**,  
5. **redukcja kosztów instalacji i wdrożenia**,  
6. **praca w środowiskach trudnych: przemysłowych, górniczych, rozproszonych**.

### 6.4. Wniosek patentowy dla projektu B+R

Z perspektywy projektu NCBR szczególnie istotne jest to, że potencjalna nowość nie musi polegać wyłącznie na opracowaniu nowego typu sprzęgacza. Wysoki potencjał ochronny i wdrożeniowy może mieć również:

- **układ pomiarowy do oceny jakości kanału BPL-PLC**,
- **hybrydowy system sprzęgania i diagnostyki**,
- **algorytm interpretacji danych pomiarowych z nieinwazyjnych sensorów**,
- **moduł autokalibracji i autoadaptacji sprzęgacza do zmiennego medium energetycznego**.

W tym kontekście zastosowanie cewek Rogowskiego może stanowić wartościowy obszar prac badawczo-rozwojowych, zwłaszcza jeśli zostanie połączone z autorską metodą przetwarzania sygnałów i oceną jakości transmisji.

---

## 7. Literatura badawcza i stan wiedzy naukowej

Publikacje naukowe wskazują, że BPL-PLC jest aktywnym obszarem badawczym w kontekście smart grid, nadzoru infrastruktury oraz transmisji w warunkach zakłóceń. W szczególności przegląd opublikowany w czasopiśmie *Sensors* przedstawia podstawy, zastosowania, wyzwania i aktualne trendy rozwoju szerokopasmowej komunikacji po liniach energetycznych, wskazując na znaczenie zagadnień takich jak tłumienie kanału, zakłócenia, kompatybilność elektromagnetyczna, dobór częstotliwości pracy i integracja z infrastrukturą sieciową.[[3]](https://www.mdpi.com/1424-8220/22/12/4348)[[6]](https://pubmed.ncbi.nlm.nih.gov/35746132/)

W polskim i środkowoeuropejskim dorobku badawczym istotną grupę stanowią prace związane z jakością transmisji, obiektywną i subiektywną oceną usług realizowanych po BPL oraz analizą warunków pracy w sieciach przemysłowych i górniczych. Wśród cytowanych autorów pojawiają się m.in. Przemysław Jedlikowski, Grzegorz Dębita, Michał Habrych i współpracownicy.[[7]](https://scholar.google.com/citations?user=2Jg7xc8AAAAJ&hl=pl)

Dla projektu B+R oznacza to, że istnieje dobra baza do uzasadnienia potrzeby prac, ale jednocześnie nadal występuje przestrzeń dla nowości związanej z pomiarem jakości sygnału i inteligentną diagnostyką medium.

---

## 8. Cewki Rogowskiego jako narzędzie dla systemów BPL-PLC

### 8.1. Charakterystyka techniczna cewki Rogowskiego

Cewka Rogowskiego jest powietrzną cewką pomiarową obejmującą przewód z prądem. Napięcie wyjściowe jest proporcjonalne do pochodnej prądu w czasie, co oznacza, że użyteczny pomiar wymaga całkowania analogowego lub cyfrowego. Najważniejsze cechy tego rozwiązania to:

- brak rdzenia ferromagnetycznego, a więc brak nasycenia,
- szerokie pasmo pomiarowe,
- dobra liniowość w szerokim zakresie amplitud,
- możliwość nieinwazyjnego montażu,
- relatywnie mały wpływ na mierzony obwód.

W klasycznych zastosowaniach cewki Rogowskiego służą do pomiaru prądów udarowych, harmonicznych, przebiegów przejściowych i sygnałów szybkozmiennych. Z tego względu ich wykorzystanie w otoczeniu BPL-PLC jest technicznie uzasadnione przynajmniej jako narzędzie pomocnicze, badawcze lub diagnostyczne.

### 8.2. Hipoteza zastosowania w BPL-PLC

W systemie BPL-PLC sygnał komunikacyjny jest nadbudowany na medium energetycznym i w praktyce wpływa na wysokoczęstotliwościową strukturę prądu oraz pola elektromagnetycznego wokół przewodu. Cewka Rogowskiego mogłaby być wykorzystana do:

1. detekcji obecności sygnału BPL w przewodzie,  
2. obserwacji zmian widmowych związanych z transmisją,  
3. szacowania poziomu zaburzeń i zakłóceń impulsowych,  
4. pośredniej oceny SNR lub wskaźników jakości kanału,  
5. monitorowania zmian warunków transmisji w czasie.

### 8.3. Możliwe architektury zastosowania

#### Model A – sonda laboratoryjna do walidacji kanału
Cewka Rogowskiego może pełnić funkcję nieinwazyjnej sondy badawczej do pomiaru sygnałów HF na przewodzie zasilającym. W takim wariancie możliwe jest porównanie:
- sygnału nadawanego,
- sygnału obserwowanego lokalnie na przewodzie,
- parametrów po przejściu przez sprzęgacz,
- wpływu zmian obciążenia sieci na jakość kanału.

#### Model B – czujnik diagnostyczny online
Przy zastosowaniu układów szerokopasmowych i odpowiedniej obróbki cyfrowej cewka może stać się elementem systemu nadzoru online, który nie dekoduje bezpośrednio danych użytkowych, lecz estymuje parametry jakościowe medium, np.:
- poziom aktywności w paśmie BPL,
- poziom szumu tła,
- występowanie zakłóceń impulsowych,
- zmienność czasową cech kanału.

#### Model C – sprzężenie z algorytmami predykcji
Największy potencjał badawczy pojawia się wtedy, gdy sygnał z cewki Rogowskiego zostanie poddany analizie cechowej i połączony z algorytmami:
- DSP,
- detekcji anomalii,
- klasyfikacji zakłóceń,
- predykcji pogorszenia jakości transmisji,
- adaptacyjnego strojenia toru komunikacyjnego.

### 8.4. Główne korzyści zastosowania

1. **Nieinwazyjność pomiaru** – brak konieczności wpinania się do toru energetycznego.  
2. **Bezpieczeństwo** – pomiar bezpośrednio na przewodzie bez galwanicznego połączenia z torem wysokiego napięcia.  
3. **Szerokie pasmo** – potencjalna zdolność obserwacji zjawisk dynamicznych i zakłóceń HF.  
4. **Przydatność mobilna** – możliwość realizacji pomiarów okresowych, terenowych i eksperymentalnych.  
5. **Potencjał integracji z systemami predykcyjnymi** – szczególnie atrakcyjny dla projektów B+R.

### 8.5. Ograniczenia i ryzyka

1. **Pomiar pośredni, a nie bezpośredni pomiar jakości transmisji cyfrowej.**  
   Cewka Rogowskiego nie mierzy bezpośrednio BER, PER czy throughput, lecz jedynie zjawiska fizyczne skorelowane z warunkami transmisji.

2. **Konieczność szerokopasmowej akwizycji i obróbki sygnału.**  
   Aby wykorzystać cewkę do obserwacji pasma BPL, niezbędny jest odpowiednio zaprojektowany analog front-end, układ całkujący, filtracja i szybka akwizycja.

3. **Wrażliwość na zakłócenia środowiskowe.**  
   Sygnał mierzony może zawierać komponenty niezwiązane bezpośrednio z transmisją BPL, np. od falowników, przekształtników, napędów, wyładowań i zakłóceń impulsowych.

4. **Problem kalibracji.**  
   Konieczne jest określenie, w jakim stopniu sygnał z cewki koreluje z rzeczywistymi wskaźnikami jakości kanału komunikacyjnego.

5. **Zależność od położenia i geometrii montażu.**  
   Parametry pomiaru zależą od odległości od przewodu, orientacji, obecności ekranów i warunków geometrycznych.

### 8.6. Ocena dojrzałości technologicznej

Na obecnym etapie zastosowanie cewki Rogowskiego do bezpośredniej oceny jakości sygnału BPL-PLC należy traktować jako **koncepcję badawczo-rozwojową o wysokim potencjale**, ale wymagającą walidacji eksperymentalnej. Najbardziej realistyczna ścieżka wdrożeniowa obejmuje:

- etap 1: badania laboratoryjne i korelacja z parametrami kanału,
- etap 2: budowę demonstratora pomiarowego,
- etap 3: walidację w środowisku rzeczywistym,
- etap 4: opracowanie algorytmów estymacji jakości kanału,
- etap 5: integrację z urządzeniem BPL lub systemem diagnostycznym.

### 8.7. Wniosek badawczo-wdrożeniowy

Cewka Rogowskiego sama w sobie nie zastąpi klasycznych mierników jakości transmisji, ale może stanowić **nową klasę czujnika pośredniego**, umożliwiającego:
- monitoring stanu medium,
- wczesne wykrywanie pogorszenia parametrów,
- szybką diagnostykę w terenie,
- adaptacyjne wspomaganie pracy systemu BPL-PLC.

To właśnie połączenie: **czujnik nieinwazyjny + analiza sygnałowa + estymacja jakości kanału** wydaje się najbardziej perspektywicznym kierunkiem dla projektu NCBR.

---

## 9. Potencjał nowości i innowacyjności dla projektu NCBR

### 9.1. Potencjalne elementy nowości

W projekcie badawczo-rozwojowym można rozważyć następujące elementy innowacyjne:

1. **nieinwazyjny system monitorowania jakości medium BPL-PLC z użyciem cewki Rogowskiego**,  
2. **hybrydowy układ sprzęgania i jednoczesnej diagnostyki kanału**,  
3. **algorytm wyznaczania wskaźników jakości transmisji na podstawie cech widmowych i czasowych sygnału z czujnika**,  
4. **metoda autokalibracji toru pomiarowego w różnych topologiach sieci energetycznej**,  
5. **moduł predykcyjny wykrywający degradację kanału przed utratą usługi transmisyjnej**,  
6. **narzędzie do klasyfikacji stanów pracy sieci energetycznej z perspektywy przydatności dla BPL-PLC**.

### 9.2. Potencjalna wartość wdrożeniowa

Rozwiązanie takie mogłoby znaleźć zastosowanie w:
- operatorach sieci dystrybucyjnych,
- energetyce przemysłowej,
- sieciach zakładowych,
- górnictwie i tunelach infrastrukturalnych,
- systemach telemetrycznych i automatyce rozproszonej,
- narzędziach serwisowych do diagnostyki torów BPL.

### 9.3. Potencjalne wskaźniki przewagi konkurencyjnej

- brak konieczności wyłączania infrastruktury,
- niższy koszt diagnostyki terenowej,
- możliwość monitoringu ciągłego,
- większa dostępność danych o stanie medium,
- lepsze wsparcie utrzymania predykcyjnego,
- możliwość skalowania do różnych klas napięć i topologii sieci.

---

## 10. Rekomendowana agenda prac B+R

### Etap I – analiza i modelowanie
- model kanału BPL-PLC dla wybranych środowisk pracy,
- model odpowiedzi sprzęgaczy pojemnościowych i indykcyjnych,
- model pomiarowy cewki Rogowskiego,
- identyfikacja cech sygnałowych korelujących z jakością transmisji.

### Etap II – stanowisko laboratoryjne
- budowa stanowiska z rzeczywistym torem BPL,
- porównanie klasycznych metod pomiaru i toru z cewką Rogowskiego,
- pomiary przy różnych obciążeniach i rodzajach zakłóceń,
- walidacja pasma, czułości i powtarzalności.

### Etap III – algorytmy
- ekstrakcja cech czasowo-częstotliwościowych,
- korelacja z BER/SNR/throughput/opóźnieniem,
- modele regresyjne lub klasyfikacyjne,
- detekcja anomalii i predykcja degradacji kanału.

### Etap IV – demonstrator
- integracja czujnika z układem akwizycji,
- implementacja oprogramowania analitycznego,
- testy polowe w sieci rzeczywistej,
- ocena niezawodności i odporności środowiskowej.

### Etap V – przygotowanie do ochrony IP i wdrożenia
- badanie czystości patentowej,
- opracowanie zgłoszeń patentowych lub know-how,
- analiza kosztów wdrożenia,
- przygotowanie ścieżki komercjalizacji.

---

## 11. Rekomendacje końcowe

1. **Sprzęgacze pojemnościowe** należy traktować jako rozwiązania preferowane dla stabilnych, docelowych instalacji BPL-PLC o wysokich wymaganiach transmisyjnych i eksploatacyjnych.  
2. **Sprzęgacze indykcyjne** wykazują szczególną wartość w zastosowaniach retrofitowych, mobilnych, terenowych i diagnostycznych.  
3. **Cewki Rogowskiego** nie są obecnie standardowym elementem systemów BPL-PLC, jednak mają silny potencjał jako nieinwazyjne czujniki wspierające ocenę jakości medium i warunków transmisji.  
4. Z perspektywy projektu NCBR najbardziej obiecujące jest nie tyle samo użycie cewki Rogowskiego, ile opracowanie **kompletnej metody pomiarowo-analitycznej** łączącej sensor, układ akwizycji i algorytm estymacji jakości kanału.  
5. Obszar ten posiada realny potencjał nowości badawczej, ochrony własności intelektualnej i wdrożenia przemysłowego.

---

## 12. Źródła

1. Rozwój technologii PLC – omówienie trendów i zastosowań:  
   https://e-elektryczna.pl/technika-i-technologie/rozwoj-technologii-plc/

2. System komunikacji BPL – przykłady zastosowań przemysłowych i infrastrukturalnych:  
   https://www.mikronika.pl/oferta/produkty/urzadzenia/transmisji-danych/system-komunikacji-bpl/

3. Upgrading the Power Grid Functionalities with Broadband Power Line Communications: Basis, Applications, Current Trends and Challenges (*Sensors*, 2022):  
   https://www.mdpi.com/1424-8220/22/12/4348

4. PLC-BPL couplers for MV – przykłady komercyjnych sprzęgaczy pojemnościowych i indykcyjnych:  
   https://www.arteche.com/en/plc-bpl-couplers-mv

5. Ośrodek Informacji Patentowej PATLIB BG AGH – punkt dostępu do analiz patentowych i baz własności przemysłowej:  
   https://patenty.bg.agh.edu.pl/

6. Rekord PubMed dla publikacji przeglądowej o BPL:  
   https://pubmed.ncbi.nlm.nih.gov/35746132/

7. Profil cytowań i publikacji związanych z BPL/PLC, m.in. autorzy prowadzący badania jakościowe i aplikacyjne:  
   https://scholar.google.com/citations?user=2Jg7xc8AAAAJ&hl=pl

---

## 13. Zastrzeżenie metodyczne

Niniejszy raport ma charakter analityczny i koncepcyjny. Część wniosków dotyczących potencjału zastosowania cewek Rogowskiego w ocenie jakości sygnału BPL-PLC stanowi ocenę ekspercką opartą na właściwościach fizycznych czujnika, znanych architekturach pomiarowych oraz trendach rozwojowych w energetyce i telekomunikacji po liniach zasilających. Dla potwierdzenia przydatności wdrożeniowej wymagane są badania eksperymentalne, analiza porównawcza z klasycznymi metodami pomiarowymi oraz szczegółowe badanie czystości patentowej na poziomie rodzin zgłoszeń i jurysdykcji.

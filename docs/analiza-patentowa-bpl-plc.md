# Analiza patentowa – sprzęgacze dla BPL-PLC/PLC oraz potencjalne zastosowanie cewek Rogowskiego

**Data opracowania:** 2026-05-11  
**Wersja:** 2.0 – przygotowana od nowa po audycie trafności źródeł  
**Repozytorium docelowe:** `debitagrzegorz-netizen/openwifi-hw`

---

## 1. Cel opracowania

Celem niniejszego dokumentu jest przygotowanie od nowa, bardziej poprawnej i zawężonej tematycznie analizy patentowej dotyczącej:

1. sprzęgaczy (**couplers**) stosowanych w systemach **PLC / BPL-PLC**,
2. rozwiązań określanych jako **inductive coupler**, **induction coupler**, **capacitive coupler** w kontekście komunikacji po liniach energetycznych,
3. rozwiązań bezkontaktowych i hybrydowych wykorzystywanych do transmisji danych po przewodach energetycznych,
4. możliwych zastosowań **cewek Rogowskiego** w otoczeniu systemów PLC/BPL – głównie jako elementów pomiarowych i diagnostycznych.

Dokument ma charakter analizy wstępnej, ukierunkowanej na identyfikację **rzeczywiście relewantnych patentów**, a nie ogólnych źródeł pomocniczych.

---

## 2. Zakres wyszukiwania i kryteria doboru

W analizie uwzględniono wyszukiwanie oparte na frazach:

- `coupler`
- `induction`
- `inductive coupler`
- `capacitive coupler`
- `power line communication`
- `PLC`
- `BPL`
- `BPL-PLC`
- `Rogowski coil`

Do zestawienia włączono tylko takie pozycje, które spełniają co najmniej jedno z poniższych kryteriów:

- bezpośrednio dotyczą sprzęgania sygnału do linii energetycznej w systemach PLC/BPL,
- dotyczą indukcyjnych lub pojemnościowych metod sprzęgania w otoczeniu transmisji danych,
- dotyczą rozwiązań bezkontaktowych lub wysokoizolowanych, które mogą być funkcjonalnie istotne dla infrastruktury BPL,
- odnoszą się do cewek Rogowskiego w sposób mogący mieć znaczenie pomocnicze dla monitoringu lub diagnostyki sygnałów w sieci energetycznej.

Nie włączano do analizy:
- portali patentowych jako osobnych pozycji patentowych,
- ogólnych patentów z dziedziny czujników prądu bez związku z komunikacją po liniach,
- rozwiązań dotyczących PLC rozumianego jako programmable logic controller,
- patentów o zbyt luźnym związku z analizowanym tematem.

---

## 3. Wyniki analizy patentowej

## 3.1. Patenty bezpośrednio związane ze sprzęgaczami dla PLC/BPL

### [P1] US7492245B2 – *Broadband over power lines (BPL) coupling system*  
Link: https://patents.google.com/patent/US7492245B2/en
Dodatkowy opis: https://www.freepatentsonline.com/7492245.html

**Klasyfikacja trafności:** **wysoka / bezpośrednio relewantna**

**Zakres istotności:**
- BPL / broadband over power lines,
- coupling system,
- sprzęganie sygnału do linii energetycznej,
- rozwiązanie relewantne dla praktyki wdrożeniowej.

**Komentarz analityczny:**
Patent ten jest jedną z najbardziej istotnych pozycji dla analizowanego tematu. Dotyczy systemu sprzęgania sygnału dla szerokopasmowej komunikacji po liniach energetycznych i wskazuje na rozwiązanie przeznaczone do pracy w rzeczywistym środowisku sieci elektroenergetycznej. Z dostępnych opisów wynika, że rozwiązanie wykorzystuje konstrukcję sprzęgacza przeznaczoną do montażu na liniach energetycznych, z naciskiem na izolację, bezpieczeństwo eksploatacyjne i szerokie pasmo pracy. 

**Znaczenie dla projektu:**
To patent, który powinien zostać potraktowany jako punkt obowiązkowy dalszej analizy claims i figur, ponieważ dotyczy bezpośrednio architektury sprzęgacza dla systemów BPL.

---

### [P2] US8593315B2 – *Coupling device for power line communication*  
Link: https://patents.google.com/patent/US8593315B2/en

**Klasyfikacja trafności:** **wysoka / bezpośrednio relewantna**

**Zakres istotności:**
- power line communication,
- coupling device,
- urządzenie sprzęgające dla komunikacji po liniach energetycznych.

**Komentarz analityczny:**
Patent ten bezpośrednio odnosi się do urządzenia sprzęgającego dla PLC. W świetle zakresu tematycznego projektu jest to pozycja relewantna i uzasadniona do utrzymania w analizie. Należy jednak pamiętać, że sama nazwa patentu nie rozstrzyga jeszcze typu sprzęgacza ani konkretnego kontekstu napięciowego, dlatego w kolejnym etapie konieczna jest analiza szczegółowych zastrzeżeń.

**Znaczenie dla projektu:**
To jeden z kluczowych patentów ogólnych dla obszaru sprzęgania sygnałów PLC i powinien być uwzględniany w przeglądzie stanu techniki.

---

### [P3] US7982716B2 – *Coupling unit for power line communication*  
Link: https://patents.google.com/patent/US7982716B2/en

**Klasyfikacja trafności:** **wysoka / bezpośrednio relewantna**

**Zakres istotności:**
- coupling unit,
- PLC,
- układ sprzęgający do komunikacji po liniach energetycznych.

**Komentarz analityczny:**
Patent stanowi bezpośrednie odniesienie do jednostki sprzęgającej dla komunikacji PLC. Z punktu widzenia projektu ma znaczenie jako reprezentant patentów ogólnych dotyczących infrastruktury coupling unit / coupling device. W dalszej pracy należy ustalić, czy obejmuje głównie warstwę sprzęgania fizycznego, dopasowania impedancyjnego, filtracji czy ochrony.

**Znaczenie dla projektu:**
Patent ważny dla zrozumienia typowych elementów zastrzeganych w zakresie urządzeń sprzęgających PLC.

---

### [P4] US7286035B2 – *Highly insulated inductive data couplers*  
Link: https://patents.google.com/patent/US7286035B2/en

**Klasyfikacja trafności:** **wysoka / bezpośrednio relewantna dla wątku sprzęgaczy indukcyjnych**

**Zakres istotności:**
- inductive data couplers,
- wysoka izolacja,
- bezkontaktowe lub wysokoizolowane sprzęganie danych,
- środowisko sieci energetycznej i podobnych aplikacji transmisyjnych.

**Komentarz analityczny:**
Patent ten ma duże znaczenie dla wątku sprzęgaczy indukcyjnych. Opisuje rozwiązania ukierunkowane na wysokoizolowane sprzęganie sygnału, co jest istotne zwłaszcza tam, gdzie priorytetem jest bezpieczeństwo pracy przy wysokich napięciach lub ograniczenie ryzyka przebić. Nawet jeśli nie każdy wariant wykonania dotyczy bezpośrednio klasycznych wdrożeń BPL-PLC, patent jest silnie relewantny funkcjonalnie.

**Znaczenie dla projektu:**
To jedna z najważniejszych pozycji dla części raportu poświęconej sprzęgaczom indukcyjnym i konstrukcjom wysokoizolowanym.

---

## 3.2. Patenty częściowo relewantne – rozwiązania hybrydowe i bezkontaktowe

### [P5] US20160006485A1 – *Contactless Coupler*  
Link: https://patents.google.com/patent/US20160006485A1/en

**Klasyfikacja trafności:** **średnia / częściowo relewantna**

**Zakres istotności:**
- contactless coupler,
- rozwiązania bezkontaktowe,
- potencjalne znaczenie dla transmisji danych i energii.

**Komentarz analityczny:**
Patent dotyczy sprzęgacza bezkontaktowego i jest ważny z punktu widzenia architektur hybrydowych, w których transmisja danych i transfer energii mogą współistnieć. Nie jest to jednak patent jednoznacznie osadzony w klasycznym środowisku BPL-PLC sieci elektroenergetycznej. Z tego względu należy go traktować jako źródło częściowo relewantne – bardziej jako inspirację architektoniczną niż podstawowy dokument stanu techniki dla BPL.

**Znaczenie dla projektu:**
Przydatny pomocniczo, zwłaszcza jeśli projekt będzie rozważał nieinwazyjne lub hybrydowe sposoby sprzęgania.

---

## 3.3. Patenty związane z cewkami Rogowskiego

### [P6] EP1763131A1 – *Use of Rogowski coils in power line communication*  
Link: https://patents.google.com/patent/EP1763131A1/en

**Klasyfikacja trafności:** **wysoka, pod warunkiem potwierdzenia treści claims / potencjalnie bezpośrednio relewantna**

**Zakres istotności:**
- Rogowski coil,
- power line communication,
- potencjalne powiązanie z monitoringiem, detekcją lub sprzęganiem sygnału.

**Komentarz analityczny:**
Jest to kluczowa pozycja z punktu widzenia pytania o związek cewek Rogowskiego z PLC. Jeżeli rzeczywisty zakres patentu odpowiada jego tytułowi, dokument ten może stanowić najważniejsze istniejące odniesienie patentowe dla połączenia Rogowski coil i power line communication. Należy jednak wyraźnie zaznaczyć, że bez szczegółowej analizy zastrzeżeń nie można przesądzić, czy patent dotyczy stricte sprzęgania, detekcji sygnału, monitoringu kanału czy innych funkcji pomocniczych.

**Znaczenie dla projektu:**
Patent priorytetowy do pogłębionej analizy. Może mieć kluczowe znaczenie dla oceny nowości projektu w obszarze wykorzystania cewek Rogowskiego.

---

### [P7] US20150268495A1 – *High frequency Rogowski coil for current measurement*  
Link: https://patents.google.com/patent/US20150268495A1/en

**Klasyfikacja trafności:** **niska do średniej / pomocnicza**

**Zakres istotności:**
- high frequency Rogowski coil,
- current measurement,
- metrologia sygnałów szybkozmiennych.

**Komentarz analityczny:**
Patent nie dotyczy bezpośrednio BPL-PLC ani sprzęgaczy dla komunikacji po liniach energetycznych. Ma jednak znaczenie pomocnicze, ponieważ dotyczy cewek Rogowskiego zdolnych do pomiarów wysokoczęstotliwościowych. W projekcie może być przywoływany jako odniesienie do zdolności metrologicznych czujnika, ale nie jako rdzeń analizy patentowej PLC/BPL.

**Znaczenie dla projektu:**
Źródło pomocnicze dla sekcji o potencjale pomiarowym cewki Rogowskiego.

---

## 4. Wnioski z nowej analizy patentowej

1. **Najbardziej relewantne patenty dla obszaru BPL-PLC dotyczą ogólnie rozumianych coupling device / coupling unit oraz dedykowanych systemów sprzęgania dla broadband over power lines.**
2. **Najsilniej reprezentowanym i technicznie uzasadnionym obszarem są sprzęgacze indukcyjne oraz wysokoizolowane sprzęgacze danych.**
3. **Sprzęgacze pojemnościowe są słabiej reprezentowane w zidentyfikowanym zestawie patentów niż w literaturze technicznej i w dokumentacji produktowej.** Oznacza to potrzebę dalszej kwerendy ukierunkowanej stricte na frazy `capacitive coupling method`, `capacitive coupler power line communication`, `medium voltage PLC capacitive coupler`.
4. **Wątek cewek Rogowskiego jest obecny znacznie słabiej niż wątek klasycznych sprzęgaczy.** Jedynie patent EP1763131A1 wydaje się potencjalnie bezpośrednio związany z PLC, podczas gdy pozostałe rozwiązania mają głównie znaczenie pomiarowe i kontekstowe.
5. **Nie ma podstaw, aby twierdzić, że cewka Rogowskiego jest standardowym lub dominującym patentowo sprzęgaczem w systemach BPL-PLC.** Jej potencjał dotyczy raczej obszaru monitoringu, diagnostyki i pośredniej oceny sygnału.

---

## 5. Ograniczenia bieżącej analizy

Niniejsza analiza została wykonana jako poprawiona i zawężona wersja przeglądu patentowego, ale nadal ma charakter wstępny. Ograniczenia obejmują:

- brak pełnej analizy zastrzeżeń patentowych dla każdej pozycji,
- brak mapowania rodzin patentowych i jurysdykcji,
- brak szczegółowej klasyfikacji IPC/CPC,
- ograniczoną reprezentację patentów stricte pojemnościowych w bieżącym zestawie,
- brak pełnej analizy freedom-to-operate.

---

## 6. Rekomendacje do kolejnego etapu

Dla przygotowania finalnej analizy patentowej do raportu NCBR zaleca się:

1. wykonać szczegółową analizę claims dla patentów P1–P6,
2. rozszerzyć wyszukiwanie o frazy:
   - `capacitive coupling method for medium voltage PLC`,
   - `capacitive coupler for power line communication`,
   - `inductive coupler for power line communication`,
   - `broadband over power line coupling system`,
   - `Rogowski coil power line communication`,
   - `non-invasive PLC signal monitoring`,
3. przeanalizować rodziny patentowe w Espacenet i WIPO,
4. ustalić zgłaszających i status ochrony,
5. zbudować tabelę: numer patentu – typ sprzęgacza – zakres – relewancja – ryzyko kolizji patentowej.

---

## 7. Podsumowanie

Nowa analiza patentowa wskazuje, że spośród zidentyfikowanych pozycji rzeczywiście relewantne dla tematu projektu są przede wszystkim patenty dotyczące:
- systemów sprzęgania dla **broadband over power lines**,
- urządzeń typu **coupling device / coupling unit** dla PLC,
- **inductive data couplers** o wysokiej izolacji,
- oraz – warunkowo – patent łączący **Rogowski coil** z **power line communication**.

Wynika z tego, że dla projektu skoncentrowanego na sprzęgaczach BPL-PLC należy traktować jako główny rdzeń analizy patentowej rozwiązania coupler/coupling system, natomiast wątek cewek Rogowskiego należy ujmować ostrożnie – jako obszar potencjalnie innowacyjny, ale słabiej reprezentowany w odnalezionym materiale patentowym.

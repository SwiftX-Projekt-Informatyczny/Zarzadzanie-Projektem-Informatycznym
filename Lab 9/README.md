# Lab 2 - SwiftX 1 Poziom TLR

- Zespół SwiftX opracował nowy algorytm fizyczny umożliwiający jednoczesną obsługę wielu fizycznych ciał na raz. Rozwiązanie to pozwala na symulację setek obiektów fizycznych przy znacznie mniejszym obciążeniu procesora. W testach SwiftX osiągnął wydajność wyższą o około 45% w porównaniu z popularnymi silnikami fizyki. Algorytm wykorzystuje grupowanie interakcji oraz predykcję ruchu, co pozwala oszczędzać moc obliczeniową i poprawia płynność symulacji.

# Lab 3 - SwiftX 2 Poziom TLR

### Zadanie 1
- Zespół SwiftX przeprowadził wstępną analizę możliwych zastosowań nowego algorytmu fizyki. W badań wynika, że technologia ta ma potencjał zastosowania w projektach gier, rzeczywistości wirtualnej oraz zaawansowanych systemach symulacyjnych. Poszerzając horyzonty analiz nad algorytmem powinniśmy stworzyć silnik, który w prosty sposób umożliwi użytkownikom testowanie technologii w różnych konfiguracjach. Silnik powinien umożliwiać dowolnemu obiektowi przypisanie wartości fizycznych oraz układanie tych ciał na scenie, po przygotowaniu sceny powinniśmy mieć możliwość włączenia symulacji aby zobaczyć jej efekty.

### Zadanie 2
- 2x środowisko programisyczne Visual Studio Code
- 2x komputer stacjonarny z wydajnymi kartami graficznymi (RTX 4070)
- Oprogramowanie do tworzenia dokumentacji
- Dostęp do internetu

# Lab 4 - SwiftX 3 Poziom TLR (Metodologia Prince2)

### Zadanie 1

- Moduł symulacji fizyki - w ramach tego modułu silnik będzie odpowiadał za realistyczną symulację obiektów w wirtualnym świecie gry
- Moduł renderowania - silnik będzie posiadał algorytmy renderujące które będą odpowiedzialne za wyświetlanie grafiki 3D w czasie rzeczywistym
- Moduł sterowania - moduł będzie odpowiadał za nawigację zarówno po programie jak i po świecie gry
- Moduł optymalizacji zasobów - silnik będzie zarządzał dostępnymi zasobami (CPU, GPU, RAM) oraz dynamicznym przydzielaniem i ładowaniem tych zasobów
- Moduł synchronizacji grafiki i fizyki - moduł będzie odpowiedzialny za synchronizację obliczeń wraz z renderowaniem grafiki aby wynikiem był płynna gra bez zakłóceń
- Moduł analizy wydajności - system będzie monitorował wydajność programu aby porzygotować silnik do pomiarów wydajności i optymalizacji

### Zadanie 2
- Ciągła zasadność biznesowa – Systematyczna weryfikacja sensu projektu i kontrola ryzyk, aby upewnić się, że projekt ma uzasadnienie biznesowe.
- Zdefiniowane role i odpowiedzialności – Jasne określenie ról, obowiązków i zakresu decyzyjnego, przy czym kierownik projektu nie może łączyć swojej roli z rolą w komitecie sterującym.
- Koncentracja na produktach – Skupienie na dostarczeniu określonego produktu, zaczynając od jego definicji i ustalając kryteria jakości.
- Korzystanie z doświadczeń – Wykorzystanie zdobytych doświadczeń z innych projektów w celu poprawy realizacji bieżącego projektu.
- Zarządzanie z wykorzystaniem tolerancji – Ustalanie granic tolerancji (czasu, kosztów, jakości, ryzyka) dla decyzji kierownika projektu.
- Zarządzanie etapowe – Podział projektu na etapy, z kontrolą postępów i oceną zasadności biznesowej przed rozpoczęciem kolejnych etapów.
- Dostosowanie do projektu w danym środowisku – Dopasowanie narzędzi, modelu i zasobów do specyfiki projektu i jego środowiska.

# Lab 5 - SwiftX 4 Poziom TLR (Badania Przemysłowe)
- Ryzyko: Symulacje produkują różne wyniki, mimo tej samej startowej pozycji
- Rozwiązanie: Implementacja testów zapewniających deterministyczność symulacji

- Ryzyko: Silnik fizyki może być zbyt wymagający i ograniczać pulę potencjalnych klientów przez wysokie wymagania sprzętowe
- Rozwiązanie: Testy optymalizacyjne na sprzętach o różnych wymaganiach

# Lab 6 - SwiftX
Grupą docelową byliby programiści skupiający się na tworzeniu gier komputerowych lub animacji 3D oraz studia deweloperskie zajmujące się tematami powiązanymi z grami, animacjami oraz symulacjami.

Model biznesowy - będą dostępne 3 możliwości użytkowania programu:
-	Licencja darmowa – darmowa, nie pozwala na komercjalizację gotowego produktu
-	Licencja prywatna - płatna, przeznaczona dla prywatnych użytkowników, pozwala na komercjalizację projektu
- Licencja firmowa - j.w. ale przeznaczona dla firm i liczona od maszyny oraz w skali roku
Jest to produkt dość specjalistyczny więc nie jest przewidywana ogromna baza użytkowników. Przy odpowiedniej reklamie przewidujemy ok. 20000 użytkowników w skali krajowej na kwartał.

# Lab 7 - SwiftX
Silnik będzie wykorzystywał złożony system w którym wykorzystuje się kilka podejść, głównie architekturę component-based w której scenie będą tworzone obiekty, do których dodawane będą komponenty takie jak skrypty i inne właściwości. Aplikacja będzie zbyt obszerna aby stosować pojedynczy wzorzec MVC czy Onion.
-	Kontroler - zostanie użyty w celu koordynowania pracy pozostałych części programu. Zostaną wykonane testy stabilności oraz jakości. Będzie odpowiadał za działanie pozostałych modułów oraz weryfikował wyniki w module analizy.
-	Moduł symulacji fizyki - podłączono do kontrolera oraz pozostałych modułów i wykonano obliczenia by następnie przetestować reakcję (na kolejno: jednym prostym obiekcie, jednym złożonym, wielu prostych i wielu złożonych). Została zbadana jakość wyników, ilość błędów i niedokładności oraz czasu wykonywania obliczeń. W przypadku błędów zostaną wprowadzone korekcje.
-	Moduł renderowania - podłączono do kontrolera i modułu synchronizacji i dokonano wielu testów jakościowych wyników aby na bieżąco i przy możliwie optymalnym zużyciu zasobów wytworzyć poszczególne klatki gry / animacji. Został wykonany test na wielu obiektach, zarówno prostych jak i złożony
-	Moduł sterowania - moduł został podłączony do kontrolera. Dokonano testów w których do interfejsu dodano możliwość przepełnienia zaprojektowanymi przez użytkownika opcjami oraz rozwiązano problemy (głównie graficzne) z tym wynikające. Zostanie również stworzona seria dodatkowych obiektów w interfejsie które przetestują działanie programu przy ogromnej ilości opcji dla użytkownika a błędy zostaną naprawione
-	Moduł optymalizacji zasobów - podłączono do kontrolera i sprawdzono czy odpowiednia ilość zasobów jest rozważnie przydzielana. W przypadku braku wystarczającej ilości zasobów, moduł poprawnie tworzy kolejki do zasobów które silnik miałby wykorzystać aby posiadać najmniejsze możliwe opóźnienie oraz minimalna ilość błędów.
-	Moduł synchronizacji grafiki i fizyki - dokonano integracji z innymi modułami oraz przetestowano pod względem wyświetlanych wyników oraz udostępnionego obrazu oraz różnicy czasowej między nimi przy różnych ilościach obiektu aby prawidłowo "prosić" kontroler o reakcje modułu na prydział zasobów
-	Moduł analizy wydajności - podłączono do kontrolera i użyto aby na bieżąco wyświetlać wyniki oczekiwane i otrzymane z modułów, sygnalizować błędy, opóźnienia i niedokładności jak również analizować na bieżąco działanie programu. Szczególnie zwrócono uwagę na wyniki działania programu świeżo włączonego, po godzinie działania, po 8 godzinach działania, po 24 godzinachi po tygodniu aby sprawdzić możliwość przepełnienia posiadanych zasobów.
Jest to produkt dość specjalistyczny więc nie jest przewidywana ogromna baza użytkowników. Przy odpowiedniej reklamie przewidujemy ok. 1000 użytkowników w skali krajowej na kwartał.

# Lab 8 - SwiftX
## Mocne Strony
-	Wydajność potwierdzona testami. Silnik SwiftX potrafi symulować 50 tysięcy obiektów fizycznych wraz z kolizją w danym momencie utrzymując stabilne 60 klatek na sekundę. (95%)
-	Modularna budowa aplikacji oparta na komponentach, pozwalająca łatwo dodawać nowe funkcje. (90%)
-	Dobrze przemyślany model licencyjny (darmowa, prywatna i firmowa), który pozwala dostosowanie produktu do różnych grup użytkowników. (80%)
## Słabe Strony
-	Projekt jest dość specjalistyczny, przez co może nie trafić do szerokiego grona użytkowników. (75%)
-	Zaawansowany algorytm fizyki nie jest deterministyczny przez co możemy otrzymać różne wyniki dla tej samej symulacji. (90%)
-	Wysokie zużycie pamięci wymagane do obsługi dużych symulacji. (80%)
## Szanse
-	Duży potencjał ze względu na szybki rozwój technologii VR i AR oraz rosnące zapotrzebowanie na gry 3D. (70%)
-	Możliwość uzyskania finansowania z grantów naukowych, ponieważ projekt ma charakter badawczo-rozwojowy. (40%)
-	Możliwość współpracy z uczelniami i laboratoriami, które mogłyby używać silnika SwiftX jako narzędzia edukacyjnego i testowego. (60%)
## Zagrożenia
-	Największym zagrożeniem jest konkurencja gigantów takich jak Unity oraz Unreal Engine, które dominują rynek. (99%)
- Testowanie poprawności zjawisk fizyki w symulacji jest bardzo trudne. (60%)
-	Brak odpowiedniej promocji i marketingu produktu. (60%)

# Lab 9 - SwiftX
## Zadanie 1

Moduły silnika zostały zintegrowane, wprowadzając program w wersję beta oraz został on przygotowana do pierwszych testów jakościowych oraz obciążeniowych.
Aplikacja zostanie przetestowana pod kątem kompatybilności z najczęściej używanych systemami operacyjnymi: Windows 10, 11, Linux, MacOS. 
Zostaną przeprowadzone testy użyteczności na grupie testowej użytkowników, jak również testy obciążeniowe na przykładowych maszynach.
Testy będą podzielone na testy stabilności i wydajności: Przy testach stabilności będzie wykorzystane obliczanie 1 miliona obiektów na raz oraz sprawdzenie długości działania programu bez przepełnienia danych (przez dwa tygodnie nieustannej pracy silnika ze zużyciem 50%+ zasobów),
natomiast testy wydajnościowe obejmą szybkość ich wykonania na mniejszej ilości obiektów przy złożonych warunkach.
Obydwa typy testów będą podlegały nieustannej kontroli a ich wyniki zostaną dokładnie przeanalizowane przez programistów.
Zostanie sprawdzona również wydajność samego systemu podczas pracy programu w tle oraz jakość otrzymanych obliczeń.
W ramach obydwu testów, udostępniona zostanie wersja beta programu a testerom w ilości co namniej 50 nowych użytkowników zostanie zlecone "z-crash-owanie" aplikacji z jej poziomu.
Osoby te dostaną odpowieni zestaw przykładowych danych oraz instalator aplikacji do zainstalowania, uruchomienia, krok po kroku przetestowania i przekazania informacji zwrotnej.
Efekt końcowy:
Zostanie otrzymana przetestowana aplikacja w warunkach odwzorowujących rzeczywiste. Ewentualne korekty zostaną nałożone. 
Sposób działania aplikacji oraz użyteczność powinny na tym etapie zostać zrozumiane przez użytkowników, w takim stopniu aby aplikacja mogła opuścić wersję beta.

## Zadanie 2
Ryzyko: Trudności ze znalezieniem odpowiednich maszyn do testowania ze względu na jakość 
(wyszukiwanie maszyn wystarczająco mocnych aby w warunkach rzeczywistych sprawdzić działanie na silniejszym sprzęcie)
Rozwiązanie: Przeinstalowanie systemów na posiadanych już obecnych maszynach lub Dual-Boot - wiele systemów na jednej maszynie.

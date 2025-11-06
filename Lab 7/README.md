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

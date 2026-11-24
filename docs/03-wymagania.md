# Wymagania

## Wymagania funkcjonalne

Priorytety wg MoSCoW: **M** - must have, **S** - should have, **C** - could have, **W** - won't have (w tej wersji).

### Mieszkaniec

**US-01 Pytanie do asystenta (M)**
Jako mieszkaniec chcę zadać pytanie na czacie, żeby nie musieć iść z tym na portiernię.
- asystent odpowiada na podstawie regulaminu/FAQ i podaje, skąd wziął odpowiedź (np. paragraf regulaminu)
- jeśli nie zna odpowiedzi, mówi to wprost i proponuje założenie zgłoszenia, nie wymyśla
- po odpowiedzi mogę kliknąć „pomogło” albo „nie pomogło”

**US-02 Zgłoszenie usterki przez czat (M)**
Jako mieszkaniec chcę opisać usterkę normalnym tekstem i dodać zdjęcie, żeby nie wypełniać formularza.
- asystent zakłada zgłoszenie z kategorią, priorytetem, numerem pokoju i opisem, a ja dostaję jego numer
- jak czegoś brakuje (np. nie wiadomo gdzie), asystent dopytuje
- można dodać do 3 zdjęć
- przed wysłaniem mogę poprawić kategorię

**US-03 Awaria krytyczna (M)**
Jako mieszkaniec chcę, żeby zgłoszenie np. zalania od razu trafiło do obsługi, żeby szkody były jak najmniejsze.
- jeśli asystent rozpozna awarię krytyczną, recepcja dostaje alarm w ciągu 30 s
- mieszkaniec od razu dostaje krótką instrukcję i numer na portiernię
- takie zgłoszenie ma najwyższy priorytet i pomija weryfikację

**US-04 Status zgłoszenia (M)**
Jako mieszkaniec chcę widzieć status swoich zgłoszeń, żeby wiedzieć, czy ktoś się nimi zajmuje.
- widzę listę swoich zgłoszeń ze statusem i terminem
- w szczegółach widzę historię zmian
- nie widzę zgłoszeń innych osób

**US-05 Potwierdzenie naprawy (M)**
Jako mieszkaniec chcę potwierdzić naprawę albo napisać, że dalej nie działa, żeby zgłoszenie nie zamknęło się bez sensu.
- po zakończeniu prac zgłoszenie ma status „do potwierdzenia”
- „nie działa” cofa zgłoszenie do konserwatora
- bez odpowiedzi przez 3 dni zgłoszenie zamyka się samo

**US-06 Powiadomienia (S)**
Jako mieszkaniec chcę dostać powiadomienie przy zmianie statusu, żeby nie sprawdzać aplikacji co chwilę.
- powiadomienie push albo mail przy przydzieleniu, zakończeniu prac i odrzuceniu
- w ustawieniach mogę wybrać, jak chcę dostawać powiadomienia

**US-07 Ocena obsługi (S)**
Jako mieszkaniec chcę ocenić obsługę (1-5), żeby kierownik wiedział, co działa słabo.
- ocenę można dać raz, po zamknięciu zgłoszenia
- można dopisać komentarz

**US-08 Czat po angielsku (C)**
Jako mieszkaniec z Erasmusa chcę pisać z asystentem po angielsku.
- asystent odpowiada w języku, w którym pytam
- obsługa widzi zgłoszenie po polsku

### Recepcja i konserwator

**US-09 Weryfikacja zgłoszenia (M)**
Jako recepcja chcę przejrzeć nowe zgłoszenie i przyjąć je albo odrzucić, żeby konserwatorzy nie dostawali śmieciowych zgłoszeń.
- widzę nowe zgłoszenia posortowane po priorytecie
- mogę poprawić kategorię i priorytet nadane przez asystenta
- przy odrzuceniu muszę wpisać powód, mieszkaniec go dostaje
- system pokazuje możliwe duplikaty (to samo miejsce i kategoria w ostatnim tygodniu)

**US-10 Przydział konserwatora (M)**
Jako recepcja chcę przydzielić zgłoszenie konkretnemu konserwatorowi z terminem.
- termin ustawia się sam wg priorytetu (krytyczny 2 h, wysoki 24 h, normalny 3 dni, niski 7 dni), można go zmienić
- widzę, ile otwartych zadań ma każdy konserwator
- konserwator dostaje powiadomienie

**US-11 Zadania konserwatora (M)**
Jako konserwator chcę mieć listę swoich zadań na telefonie i oznaczać je jako zrobione.
- widzę lokalizację, opis, zdjęcia i termin
- mogę ustawić „w realizacji” i „zakończone” z krótkim opisem
- mogę dodać notatkę, np. że czekam na części

### Kierownik

**US-12 Eskalacja po terminie (M)**
Jako kierownik chcę dostać informację o zgłoszeniach po terminie, żeby móc szybko zareagować.
- po przekroczeniu terminu zgłoszenie dostaje status „eskalowane” i dostaję powiadomienie
- mogę zmienić konserwatora, priorytet i termin

**US-13 Baza wiedzy asystenta (S)**
Jako kierownik chcę aktualizować regulamin i FAQ, żeby asystent odpowiadał zgodnie z aktualnymi zasadami.
- mogę wgrać plik (PDF/DOCX) albo dodać pytanie i odpowiedź
- asystent korzysta ze zmian najpóźniej po kilku minutach
- mogę wyłączyć nieaktualny dokument

**US-14 Statystyki (S)**
Jako kierownik chcę widzieć statystyki zgłoszeń, żeby planować remonty.
- liczba zgłoszeń wg kategorii i miesiąca, średni czas naprawy, ile dotrzymanych terminów
- ile spraw asystent załatwił sam, bez zgłoszenia
- średnia ocena obsługi

**US-15 Eksport do CSV (C)**
Jako kierownik chcę wyeksportować zgłoszenia do CSV, żeby zrobić raport dla uczelni.
- eksport bez danych osobowych mieszkańców

### Wszyscy

**US-16 Logowanie kontem uczelnianym (M)**
Jako użytkownik chcę logować się kontem z uczelni, żeby nie zakładać nowego konta.
- logowanie przez SSO uczelni
- rolę (mieszkaniec/recepcja/konserwator/kierownik) nadaje kierownik
- osoby spoza listy nie mają dostępu

### Won't have (na razie nie robimy)

- płatności za akademik
- rezerwacja pralni i sal nauki

## Wymagania niefunkcjonalne

TODO

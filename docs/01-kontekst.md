# Kontekst projektu

## Problem

W większości akademików usterki zgłasza się na portierni - ustnie, w zeszycie albo mailem do
administracji. Mieszkaniec nie wie potem, czy ktoś w ogóle zajął się sprawą, zgłoszenia się gubią
albo są dublowane, a recepcja w kółko odpowiada na te same pytania (hasło do Wi-Fi, godziny pralni,
do której mogą zostać goście). Poważniejsze awarie, np. zalanie w nocy, często trafiają do obsługi
z dużym opóźnieniem.

## Wizja systemu

Chcemy zrobić aplikację webową (działającą też na telefonie jako PWA), w której mieszkaniec
pisze po prostu na czacie, co się dzieje. Po drugiej stronie jest asystent AI, który:

- odpowiada na pytania na podstawie regulaminu i FAQ akademika,
- jeśli sprawa wymaga interwencji, zakłada zgłoszenie (kategoria, priorytet, opis, zdjęcie),
- rozpoznaje awarie krytyczne (zalanie, brak prądu, zapach gazu) i od razu alarmuje recepcję.

Recepcja sprawdza zgłoszenia i przydziela je konserwatorom z terminem wykonania. Jak termin minie,
sprawa trafia do kierownika. Mieszkaniec widzi cały czas status swojego zgłoszenia, a na końcu
potwierdza, że naprawa jest zrobiona.

Główne cele:
- szybsza obsługa zgłoszeń i żadne nie ginie,
- mniej powtarzalnych pytań na recepcji,
- kierownik widzi, co się najczęściej psuje i ile trwają naprawy.

Poza zakresem tej wersji: płatności za akademik, przydział pokoi, rezerwacje pralni,
aplikacje natywne na Androida/iOS.

## Aktorzy

| Aktor | Opis |
|---|---|
| Mieszkaniec | student mieszkający w akademiku; zadaje pytania, zgłasza usterki, potwierdza naprawy |
| Recepcja | pracownik portierni; weryfikuje zgłoszenia, przydziela je konserwatorom, reaguje na alarmy |
| Konserwator | wykonuje naprawy i oznacza je jako zrobione |
| Kierownik akademika | obsługuje eskalacje, aktualizuje regulamin/FAQ dla asystenta, przegląda statystyki |
| Asystent AI | część naszego systemu (aktor systemowy); odpowiada na pytania i zakłada zgłoszenia |
| SSO uczelni | zewnętrzny system logowania, przez który logują się wszyscy użytkownicy |
| Usługa LLM | zewnętrzne API modelu językowego, z którego korzysta asystent |

## Słowniczek

- **zgłoszenie** - sprawa, którą musi się zająć człowiek; ma kategorię, priorytet, status i osobę przypisaną
- **awaria krytyczna** - coś, co zagraża zdrowiu albo mieniu (zalanie, brak prądu, gaz, zatrzaśnięte drzwi)
- **SLA** - termin na wykonanie zgłoszenia, zależny od priorytetu
- **eskalacja** - przekazanie zgłoszenia kierownikowi po przekroczeniu terminu
- **RAG** - asystent najpierw wyszukuje pasujące fragmenty regulaminu/FAQ i odpowiada tylko na ich podstawie

Statusy zgłoszenia: nowe → zweryfikowane → przydzielone → w realizacji → do potwierdzenia → zamknięte
(oraz odrzucone i eskalowane).

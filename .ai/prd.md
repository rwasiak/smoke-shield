# Dokument wymagań produktu (PRD) - SmokeShield

## 1. Przegląd produktu

SmokeShield to mobilne narzędzie przeznaczone dla osób rzucających palenie (papierosy tradycyjne i e-papierosy). Aplikacja dostarcza błyskawiczną, empatyczną i spersonalizowaną interwencję za pomocą konwersacyjnej AI, opartej na technikach poznawczo-behawioralnych (CBT). Rozwój podzielono na dwie fazy: Proof of Concept (POC) w celu walidacji hipotezy natychmiastowej interwencji oraz Minimum Viable Product (MVP) z modelem subskrypcyjnym.

## 2. Problem użytkownika

Użytkownicy rzucający palenie najczęściej ulegają nałogowi w momencie nagłego, silnego głodu nikotynowego. W krytycznej chwili brak natychmiastowego, spersonalizowanego wsparcia prowadzi do porażki i utrwala negatywne nawyki. Celem SmokeShield jest przerwanie automatycznego odruchu sięgania po papierosa i zastąpienie go nowym, zdrowym nawykiem – szukaniem wsparcia.

## 3. Wymagania funkcjonalne

### Faza 1: Proof of Concept (POC)

1. Onboarding
   - Jednorazowy ekran zbierający: płeć, wiek, rodzaj nałogu, główne wyzwalacze, motywacje do rzuczenia palenia.
2. Ekran główny
   - Ultraminimalistyczny interfejs z jednym centralnym przyciskiem interwencji.
3. Konwersacja z AI
   - Po naciśnięciu przycisku uruchamia się chat z AI.
   - AI działa na podstawie system prompcie i 10–15 scenariuszy zgodnych z CBT.
4. Pętla feedbacku
   - Po interwencji użytkownik odpowiada na pytanie "Czy udało się przezwyciężyć głód?" (Tak/Nie).
   - Możliwość wskazania lub dodania nowego wyzwalacza.

### Faza 2: Minimum Viable Product (MVP)

1. Wszystkie funkcje z POC.
2. Dynamiczna personalizacja
   - Automatyczne dodawanie wyzwalaczy do profilu użytkownika i użycie w kolejnych sesjach.
3. System angażujący
   - Kamienie milowe (24h, 3 dni, tydzień itp.).
   - Powiadomienia event-based: gratulacje, przypomnienia braku aktywności.
4. Ulepszony dostęp (UX)
   - Widget na ekran główny telefonu, uruchamiający interwencję jednym kliknięciem.
5. Wielojęzyczność
   - Aplikacja oferuje dostęp w języku Polskim, Angielskim, Hiszpańskim

## 4. Granice produktu

1. Brak offline’owej wersji aplikacji.
2. Brak fine-tuningu modeli AI w fazie POC.
3. Brak integracji z zewnętrznymi aplikacjami zdrowotnymi.

## 5. Historyjki użytkowników

- ID: US-001 (POC)
  Tytuł: Onboarding użytkownika
  Opis: Jako nowy użytkownik chcę wypełnić krótki formularz podczas pierwszego uruchomienia, aby aplikacja mogła mnie spersonalizować.
  Kryteria akceptacji:

  - Wyświetla się ekran powitalny z pytaniami o płeć, wiek, rodzaj nałogu, wyzwalacze i motywacje.
  - Dane są zapisane w profilu użytkownika.

- ID: US-002 (POC)
  Tytuł: Uruchomienie interwencji AI (ścieżka podstawowa)
  Opis: Jako użytkownik chcę jednym kliknięciem uruchomić interwencję AI w momencie głodu nikotynowego.
  Kryteria akceptacji:

  - Na ekranie głównym widoczny jest przycisk interwencji.
  - Po kliknięciu otwiera się chat z AI.
  - AI odpowiada zgodnie ze scenariuszami CBT w czasie <3 s.
  - AI dopasowuje odpowiedź do profilu uzytkownika w zaleznosci od płci, wieku, rodzaju nałogu i jego motywacji rzucenia palenia.

- ID: US-003 (POC)
  Tytuł: Feedback po interwencji
  Opis: Jako użytkownik chcę odpowiedzieć, czy interwencja była skuteczna i wskazać wyzwalacz (nowy lub istniejący).
  Kryteria akceptacji:

  - Po zakończeniu rozmowy pojawia się pytanie Tak/Nie.
  - Możliwość wyboru istniejącego lub dodania nowego wyzwalacza.
  - Dane są zapisywane w profilu.

- ID: US-004.1 (POC)
  Tytuł: Uwierzytelnianie
  Opis: Jako użytkownik chcę się bezpiecznie zarejestrować / zalogować, aby chronić moje postępy.
  Kryteria akceptacji:

  - Możliwość rejestracji za pomocą formularza z polami e-mail i hasło.
  - Po poprawnym wypełnieniu formularza i weryfikacji danych konto jest aktywowane
  - Uzytkownik dostaje potwierdzenie o poprawnej rejestracji konta i zostaje zalogowany
  - Mozliwosc logowania za pomocą formularza z polami e-mail i hasło.
  - Po podaniu prawidłowych danych logownania uzytkownik zostaje przekierowany do widoku szybkiej interwencji
  - Błędne dane logowania wyświetlają komunikat o nieprawidłowych danych
  - Sesja uzytkownika musi miec dlugi okres waznosci

- ID: US-004.2 (POC)
  Tytuł: Ochrona danych
  Opis: Jako użytkownik chcę chronić moje dane.
  Kryteria akceptacji:

  - Dane logowania przechowywane są w bezpieczny sposób
  - Dane uzytkownika, jego profil i historia rozmów przechowywane są w bezpieczny sposób
  - Uzytkownik moze skasowac historię rozmów
  - Uzytkownik moze skasowac konto

- ID: US-005 (MVP)
  Tytuł: Dynamiczna personalizacja (MVP)
  Opis: Jako powracający użytkownik chcę, aby AI uwzględniała moje wcześniejsze wyzwalacze i motywacje.
  Kryteria akceptacji:

  - AI korzysta z historii wyzwalaczy podczas rozmowy.
  - Profil / historia użytkownika aktualizuje się automatycznie po każdej sesji.

- ID: US-006 (MVP)
  Tytuł: Śledzenie kamieni milowych
  Opis: Jako użytkownik chcę widzieć moje postępy (np. 24h, 3 dni, tydzień bez palenia).
  Kryteria akceptacji:

  - Automatyczne naliczanie czasu od ostatniej udanej interwencji.
  - Widoczność kamieni milowych w profilu.

- ID: US-007 (MVP)
  Tytuł: Powiadomienia event-based
  Opis: Jako użytkownik chcę otrzymywać spersonalizowane powiadomienia w reakcji na moje działania lub ich brak.
  Kryteria akceptacji:

  - Powiadomienia push przy osiągnięciu kamienia milowego.
  - Przypomnienia o braku aktywności przez >24h.

- ID: US-008 (MVP)
  Tytuł: Widget na ekran główny
  Opis: Jako użytkownik chcę mieć widget umożliwiający uruchomienie interwencji bez otwierania aplikacji.
  Kryteria akceptacji:
  - Widget dostępny do dodania na ekran główny.
  - Kliknięcie widgetu natychmiast otwiera interfejs interwencji.

## 6. Metryki sukcesu

### Dla POC

- Wskaźnik adopcji: % użytkowników korzystających z przycisku interwencji min. raz w ciągu dnia.
- Samoocena skuteczności: % odpowiedzi "Tak" na pytanie o przezwyciężenie głodu.
- Feedback jakościowy: opinie od grupy testowej.

### Dla MVP

- Customer Lifetime Value (CLV).
- Wskaźnik konwersji z wersji próbnej na płatną.
- Wskaźnik rezygnacji (Churn Rate).

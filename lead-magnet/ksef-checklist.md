# KSeF Checklist 2026
## Kompletny przewodnik po zgodności z Krajowym Systemem e-Faktur

---

## 📅 KALENDARZ MIESIĘCZNY KSeF 2026

### Styczeń
- [ ] Przegląd faktur z poprzedniego roku
- [ ] Weryfikacja poprawności KSeF ID kontrahentów
- [ ] Aktualizacja oprogramowania księgowego
- [ ] Backup danych KSeF

### Luty
- [ ] Sprawdzenie raportów KSeF za styczeń
- [ ] Weryfikacja faktur z błędami
- [ ] Aktualizacja listy kontrahentów w KSeF
- [ ] Przegląd zmian przepisów

### Marzec
- [ ] Rozliczenie kwartalne - raportowanie KSeF
- [ ] Analiza błędów systematycznych
- [ ] Szkolenie pracowników (jeśli potrzebne)
- [ ] Weryfikacja certyfikatów podpisu elektronicznego

### Kwiecień
- [ ] Sprawdzenie faktur za Q1
- [ ] Aktualizacja integracji API KSeF
- [ ] Testowanie nowych funkcjonalności KSeF
- [ ] Przegląd dokumentacji

### Maj
- [ ] Przygotowanie do zmian letnich w przepisach
- [ ] Weryfikacja procesów wewnętrznych
- [ ] Kontrola uprawnień użytkowników KSeF
- [ ] Aktualizacja procedur obiegu faktur

### Czerwiec
- [ ] Połroczne podsumowanie KSeF
- [ ] Raportowanie do zarządu
- [ ] Przegląd wskaźników efektywności
- [ ] Planowanie urlopów - delegowanie uprawnień

### Lipiec
- [ ] Sprawdzenie faktur za Q2
- [ ] Weryfikacja zmian po urlopach
- [ ] Aktualizacja listy upoważnionych osób
- [ ] Kontrola dostępności systemu

### Sierpień
- [ ] Przegląd błędów wakacyjnych
- [ ] Weryfikacja faktur korygujących
- [ ] Aktualizacja szablonów faktur
- [ ] Testowanie procedur awaryjnych

### Wrzesień
- [ ] Rozliczenie kwartalne - raportowanie KSeF
- [ ] Przygotowanie do zmian jesiennych
- [ ] Audyt wewnętrzny procesów KSeF
- [ ] Aktualizacja polityk bezpieczeństwa

### Październik
- [ ] Sprawdzenie faktur za Q3
- [ ] Przegląd integracji z systemami zewnętrznymi
- [ ] Weryfikacja zgodności z nowymi przepisami
- [ ] Aktualizacja instrukcji obsługi

### Listopad
- [ ] Przygotowanie do końca roku
- [ ] Weryfikacja faktur rocznych
- [ ] Planowanie zamknięcia roku
- [ ] Kontrola archiwizacji dokumentów

### Grudzień
- [ ] Zamknięcie roku KSeF
- [ ] Archiwizacja faktur
- [ ] Podsumowanie roczne
- [ ] Planowanie na rok 2027

---

## 📋 WYMAGANE POLA KSeF

### Pola obowiązkowe (FAKTURA)

#### Dane podstawowe:
- [ ] Numer KSeF (przy nadaniu przez system)
- [ ] Data wystawienia
- [ ] Data dokonania czynności (sprzedaży/usługi)
- [ ] Data płatności (jeśli inna niż data wystawienia)

#### Dane sprzedawcy:
- [ ] Nazwa (pełna nazwa firmy)
- [ ] Adres (ulica, numer, kod pocztowy, miejscowość)
- [ ] NIP
- [ ] KSeF ID (identyfikator w systemie KSeF)

#### Dane nabywcy:
- [ ] Nazwa (pełna nazwa firmy)
- [ ] Adres (ulica, numer, kod pocztowy, miejscowość)
- [ ] NIP
- [ ] KSeF ID (jeśli nabywca jest w KSeF)

#### Dane transakcji:
- [ ] Forma płatności
- [ ] Waluta (PLN lub inna)
- [ ] Kurs waluty (jeśli inna niż PLN)
- [ ] Sposób dostawy (opcjonalnie)

### Pola pozycji faktury (każda pozycja):
- [ ] Lp. (numer pozycji)
- [ ] Nazwa towaru/usługi
- [ ] Miara (szt., kg, m, godz. itp.)
- [ ] Ilość
- [ ] Cena jednostkowa netto
- [ ] Wartość netto
- [ ] Stawka VAT (23%, 8%, 5%, 0%, zw., np.)
- [ ] Kwota VAT
- [ ] Wartość brutto

### Podsumowanie faktury:
- [ ] Suma wartości netto
- [ ] Suma kwot VAT (według stawek)
- [ ] Suma wartości brutto
- [ ] Kwota do zapłaty

### Dodatkowe pola (w zależności od przypadku):
- [ ] Numer zamówienia/PO
- [ ] Numer konta bankowego sprzedawcy
- [ ] Termin płatności
- [ ] Notatki/dodatkowe informacje

---

## ⚠️ NAJCZĘSTSZE BŁĘDY W KSeF

### Błędy w danych kontrahentów

- ❌ **Błędny NIP**
  - Brak cyfr kontrolnych
  - Nieprawidłowy format (spacje, myślniki)
  - NIP nieaktywny w rejestrze VAT
  - **Rozwiązanie:** Zawsze weryfikuj NIP w API GUS/MF przed wysłaniem

- ❌ **Nieprawidłowy KSeF ID**
  - Przestarzały identyfikator
  - Błąd w przepisaniu
  - Brak KSeF ID dla podmiotu w KSeF
  - **Rozwiązanie:** Pobierz aktualny KSeF ID z systemu przed wystawieniem faktury

- ❌ **Błędny adres**
  - Niepełny adres (brak numeru lokalu)
  - Przestarzały adres
  - Błędny kod pocztowy
  - **Rozwiązanie:** Weryfikuj adres w KRS/GUS

### Błędy w danych faktury

- ❌ **Nieprawidłowa data**
  - Data sprzedaży późniejsza niż data wystawienia
  - Data płatności wcześniejsza niż data wystawienia (bez podstaw)
  - **Rozwiązanie:** Ustal procedurę weryfikacji dat przed wysłaniem

- ❌ **Błędy w pozycjach**
  - Niezgodność ilości × cena = wartość
  - Błędna stawka VAT dla towaru/usługi
  - Brak jednostki miary
  - **Rozwiązanie:** Implementuj walidację matematyczną w systemie

- ❌ **Błędy w walutach**
  - Brak kursu waluty przy fakturach walutowych
  - Nieprawidłowy kurs (niezgodny z NBP)
  - Błędna waluta (np. EUR zamiast USD)
  - **Rozwiązanie:** Automatyczne pobieranie kursów NBP

### Błędy techniczne

- ❌ **Problemy z API**
  - Timeout przy dużej liczbie faktur
  - Błędy autoryzacji (przestarzały token)
  - Nieobsługiwane wyjątki
  - **Rozwiązanie:** Implementuj retry logic, monitoruj tokeny

- ❌ **Problemy z podpisem**
  - Wygasły certyfikat podpisu elektronicznego
  - Nieprawidłowy profil zaufany
  - Błędy w procesie podpisywania
  - **Rozwiązanie:** Monitoruj daty ważności certyfikatów

- ❌ **Problemy z integracją**
  - Niespójność danych między systemami
  - Brak synchronizacji statusów faktur
  - Utracone faktury w trakcie przesyłania
  - **Rozwiązanie:** Implementuj mechanizmy potwierdzeń i logowania

### Błędy organizacyjne

- ❌ **Brak procedur**
  - Brak osoby odpowiedzialnej za KSeF
  - Niejasny obieg faktur
  - Brak backupu danych
  - **Rozwiązanie:** Dokumentuj i wdrażaj procedury KSeF

- ❌ **Szkolenia**
  - Pracownicy nieznający systemu
  - Brak znajomości zmian przepisów
  - Nieaktualne instrukcje
  - **Rozwiązanie:** Regularne szkolenia i aktualizacje wiedzy

---

## ✅ CHECKLISTA IMPLEMENTACJI KSeF

### Faza 1: Przygotowanie (4-6 tygodni przed startem)

#### Analiza
- [ ] Audyt obecnych procesów księgowych
- [ ] Identyfikacja systemów do integracji z KSeF
- [ ] Analiza wolumenu faktur (miesięcznie/rocznie)
- [ ] Identyfikacja typów faktur (standardowe, zaliczkowe, korygujące)
- [ ] Analiza kontrahentów (kto jest w KSeF, kto nie)

#### Decyzje strategiczne
- [ ] Wybór modelu: API vs ręczne wprowadzanie
- [ ] Wybór oprogramowania/integratora
- [ ] Decyzja o podpisywaniu: profil zaufany vs podpis kwalifikowany
- [ ] Ustalenie budżetu na implementację

#### Zespół projektowy
- [ ] Wyznaczenie project managera KSeF
- [ ] Wyznaczenie administratora technicznego
- [ ] Wyznaczenie administratora merytorycznego
- [ ] Wyznaczenie użytkowników końcowych
- [ ] Określenie ról i odpowiedzialności

### Faza 2: Konfiguracja (2-4 tygodnie)

#### Rejestracja w KSeF
- [ ] Zarejestrowanie podmiotu w KSeF
- [ ] Pobranie KSeF ID
- [ ] Konfiguracja uprawnień użytkowników
- [ ] Przypisanie administratorów
- [ ] Weryfikacja danych w systemie MF

#### Integracja techniczna
- [ ] Konfiguracja API KSeF
- [ ] Wygenerowanie kluczy API/tokenów
- [ ] Konfiguracja środowiska testowego
- [ ] Testy połączenia z API
- [ ] Konfiguracja webhooków/powiadomień

#### Konfiguracja oprogramowania
- [ ] Aktualizacja systemu księgowego/ERP
- [ ] Konfiguracja mapowania pól
- [ ] Ustawienie szablonów faktur
- [ ] Konfiguracja numeracji
- [ ] Ustawienie walidacji danych

### Faza 3: Testowanie (2-3 tygodnie)

#### Testy techniczne
- [ ] Testy wysyłania faktur (środowisko testowe)
- [ ] Testy odbierania faktur
- [ ] Testy faktur korygujących
- [ ] Testy faktur zaliczkowych
- [ ] Testy obsługi błędów
- [ ] Testy wydajnościowe (duża liczba faktur)

#### Testy merytoryczne
- [ ] Weryfikacja poprawności danych na fakturach
- [ ] Testy różnych stawek VAT
- [ ] Testy faktur walutowych
- [ ] Testy faktur z wieloma pozycjami
- [ ] Testy faktur z rabatami

#### Testy procesowe
- [ ] Testy obiegu faktur w organizacji
- [ ] Testy procedur awaryjnych
- [ ] Testy backupu i odzyskiwania danych
- [ ] Testy delegowania uprawnień

### Faza 4: Szkolenia (1-2 tygodnie)

#### Materiały szkoleniowe
- [ ] Przygotowanie instrukcji obsługi
- [ ] Przygotowanie filmów szkoleniowych (opcjonalnie)
- [ ] Przygotowanie FAQ
- [ ] Przygotowanie procedur awaryjnych

#### Szkolenia pracowników
- [ ] Szkolenie administratorów technicznych
- [ ] Szkolenie administratorów merytorycznych
- [ ] Szkolenie użytkowników końcowych
- [ ] Szkolenie księgowych
- [ ] Szkolenie działu sprzedaży (wystawianie faktur)

### Faza 5: Uruchomienie (1 tydzień)

#### Przygotowanie do startu
- [ ] Backup wszystkich danych
- [ ] Przygotowanie wsparcia technicznego na start
- [ ] Ustawienie monitoringu systemu
- [ ] Przygotowanie komunikacji z kontrahentami

#### Uruchomienie produkcyjne
- [ ] Przełączenie na środowisko produkcyjne
- [ ] Wysłanie pierwszych faktur testowych
- [ ] Weryfikacja poprawności działania
- [ ] Monitorowanie pierwszych dni pracy

#### Stabilizacja
- [ ] Rozwiązywanie problemów zgłaszanych przez użytkowników
- [ ] Optymalizacja procesów
- [ ] Aktualizacja dokumentacji na podstawie doświadczeń
- [ ] Planowanie przeglądu po miesiącu działania

### Faza 6: Utrzymanie i optymalizacja (ciągłe)

#### Monitoring
- [ ] Codzienne sprawdzanie statusu faktur
- [ ] Cotygodniowe raportowanie błędów
- [ ] Miesięczne przeglądy wydajności
- [ ] Kwartalne audyty zgodności

#### Rozwój
- [ ] Śledzenie zmian w przepisach
- [ ] Aktualizacja oprogramowania
- [ ] Optymalizacja procesów
- [ ] Rozszerzanie integracji

#### Dokumentacja
- [ ] Aktualizacja instrukcji obsługi
- [ ] Dokumentowanie zmian
- [ ] Archiwizacja faktur
- [ ] Przeglądy procedur

---

## 📝 PODSUMOWANIE

### Kluczowe wskaźniki sukcesu (KPI) dla KSeF:

1. **Wskaźnik błędów** < 1% faktur z błędami
2. **Czas przetwarzania** < 24h od wystawienia do dostarczenia
3. **Dostępność systemu** > 99% uptime
4. **Zadowolenie użytkowników** > 4/5 w ankietach wewnętrznych

### Kontakt w sprawie wsparcia:

- **Ministerstwo Finansów:** Infolinia KSeF
- **Pomoc techniczna:** [Twój dostawca oprogramowania]
- **Wsparcie merytoryczne:** Biuro rachunkowe/Księgowy

---

*© 2026 - KSeF Checklist. Dokument przygotowany jako przewodnik po zgodności z Krajowym Systemem e-Faktur. Wszystkie informacje mają charakter informacyjny i nie stanowią porady prawnej.*

**Wersja:** 1.0  
**Data aktualizacji:** Luty 2026  
**Następna aktualizacja:** Lipiec 2026

# KSeF Checklist 2026 - Lead Magnet Content

## Document Structure
```
KSeF_CHECKLIST_2026.md
├── 1. Przed rozpoczęciem
├── 2. Wymagania techniczne
├── 3. Rejestracja i logowanie
├── 4. Wystawianie faktur
├── 5. Anulowanie i korekty
├── 6. Archiwizacja
├── 7. Najczęstsze błędy
└── 8. Załączniki i linki
```

---

## 1. PRZED ROZPOCZĘCIEM

### Wymagania prawne
- [ ] Posiadam NIP i REGON
- [ ] Mam konto w ePUAP (do logowania przez profil zaufany)
- [ ] Znam swój numer telefonu do autentykacji
- [ ] Sprawdziłem status mojej firmy w CEIDG/KRS

### Wymagania techniczne
- [ ] Mam stabilne połączenie internetowe
- [ ] Przeglądarka: Chrome 90+, Firefox 88+, Edge 90+ lub Safari 14+
- [ ] Włączona obsługa JavaScript i cookies
- [ ] Dostęp do poczty e-mail (do powiadomień)

---

## 2. WYMAGANIA TECHNICZNE

### Minimalne wymagania sprzętowe
- [ ] Procesor: dowolny z 2015+
- [ ] RAM: minimum 4 GB
- [ ] Dysk: minimum 10 GB wolnego miejsca

### Oprogramowanie
- [ ] Aktualna przeglądarka internetowa
- [ ] Opcjonalnie: aplikacja mobilna KSeF (Android/iOS)
- [ ] Opcjonalnie: integracja API dla programistów

### Test połączenia
- [ ] Wejdź na https://ksef.mf.gov.pl
- [ ] Kliknij "Testuj połączenie"
- [ ] Upewnij się, że wszystkie testy przechodzą

---

## 3. REJESTRACJA I LOGOWANIE

### Pierwsze logowanie (krok po kroku)

#### Krok 1: Wybierz metodę logowania
- [ ] Profil zaufany (zalecane)
- [ ] e-dowód
- [ ] Bankowość elektroniczna (MojeID)

#### Krok 2: Autentykacja
- [ ] Podaj numer telefonu komórkowego
- [ ] Otrzymasz SMS z kodem
- [ ] Wprowadź kod w systemie

#### Krok 3: Ustawienia konta
- [ ] Zmień hasło (jeśli wymagane)
- [ ] Ustaw powiadomienia email/SMS
- [ ] Skonfiguruj 2FA (opcjonalnie)

### Dalsze logowania
- [ ] Zapamiętaj metodę logowania
- [ ] Dodaj KSeF do zakładek
- [ ] Skonfiguruj automatyczne logowanie (bezpieczne urządzenie)

---

## 4. WYSTAWIANIE FAKTUR

### Przed wystawieniem faktury

#### Sprawdzenia wymagane
- [ ] Dane nabywcy poprawne (NIP, adres)
- [ ] Dane sprzedawcy (Twoje) poprawne w systemie
- [ ] Stawka VAT prawidłowa (23%, 8%, 5%, 0%, NP)
- [ ] Kod PKWiU dla towarów/usług (jeśli wymagany)

### Wystawianie faktury krok po kroku

#### Krok 1: Nowa faktura
- [ ] Kliknij "Nowa faktura"
- [ ] Wybierz typ faktury (FA, FA_ROZ, FA_PROWIZJA)

#### Krok 2: Dane nabywcy
- [ ] Wprowadź NIP lub dane osobowe
- [ ] Sprawdź adres dostawy/rachunku
- [ ] Dodaj adnotacje jeśli potrzebne

#### Krok 3: Pozycje faktury
- [ ] Dodaj kolejne pozycje
- [ ] Wprowadź nazwę, ilość, cenę netto
- [ ] Wybierz stawkę VAT
- [ ] System automatycznie obliczy VAT i brutto

#### Krok 4: Płatność (jeśli dotyczy)
- [ ] Metoda płatności (przelew, gotówka, BLIK)
- [ ] Termin płatności (domyślnie 7/14/30 dni)
- [ ] Numer konta bankowego (jeśli wymagany)

#### Krok 5: Walidacja i podpis
- [ ] Kliknij "Sprawdź"
- [ ] Popraw ewentualne błędy
- [ ] Kliknij "Podpisz i wyślij"

### Po wysłaniu
- [ ] Otrzymasz numer KSeF (13 znaków)
- [ ] Faktura trafi do nabywcy
- [ ] System zachowa kopię w archiwum

---

## 5. ANULOWANIE I KOREKTY

### Anulowanie faktury (do 7 dni)

#### Warunki anulowania
- [ ] Minęło mniej niż 7 dni od wystawienia
- [ ] Faktura nie została jeszcze odebrana przez nabywcę
- [ ] Masz numer KSeF anulowanej faktury

#### Procedura anulowania
- [ ] Znajdź fakturę w "Moje faktury"
- [ ] Kliknij "Anuluj"
- [ ] Potwierdź decyzję
- [ ] System anuluje i wygeneruje zaświadczenie

### Faktura korygująca (po 7 dniach)

#### Kiedy stosować
- [ ] Minął 7-dniowy termin anulowania
- [ ] Zmiana danych (cena, ilość, stawka VAT)
- [ ] Błąd w danych nabywcy/sprzedawcy
- [ ] Zwrot towaru lub rabat

#### Typy korekt
- [ ] FA_KOREKTA - korekta ilości/ceny
- [ ] FA_ZW - korekta zerowa
- [ ] FA_SAM - korekta samochodowa

#### Procedura krok po kroku
- [ ] Kliknij "Nowa faktura korygująca"
- [ ] Wybierz fakturę do skorygowania
- [ ] Wprowadź zmiany
- [ ] Dodaj opis korekty
- [ ] Podpisz i wyślij

---

## 6. ARCHIWIZACJA

### Co archiwizować
- [ ] Wszystkie faktury wychodzące
- [ ] Wszystkie faktury przychodzące
- [ ] Faktury korygujące
- [ ] Zaświadczenia o anulowaniu
- [ ] Noty korygujące

### Jak długo przechowywać
- [ ] Faktury VAT: 5 lat od końca roku podatkowego
- [ ] Dokumenty księgowe: 5 lat
- [ ] Faktury bez VAT: 2 lata (zalecane)

### Format archiwizacji
- [ ] Pobierz XML z KSeF (oryginalny format)
- [ ] Opcjonalnie: PDF do szybkiego podglądu
- [ ] Zachowaj numer KSeF w nazwie pliku

### Porządkowanie
- [ ] Katalogi według lat
- [ ] Podkatalogi według miesięcy
- [ ] Naming convention: `KSeF_YYYYMMDD_NumerKSeF.xml`

---

## 7. NAJCZĘSTSZE BŁĘDY

### Błędy techniczne
| Błąd | Rozwiązanie |
|------|-------------|
| "Błąd 404" | Odśwież stronę, sprawdź połączenie |
| "Timeout" | Zmniejsz liczbę faktur na raz |
| "Brak autoryzacji" | Zaloguj się ponownie |
| "Niepoprawny NIP" | Sprawdź NIP nabywcy w GUS |

### Błędy merytoryczne
| Błąd | Rozwiązanie |
|------|-------------|
| Zła stawka VAT | Sprawdź czy towar/usługa ma inną stawkę |
| Brak kodu PKWiU | Zweryfikuj kod w klasyfikacji |
| Zły termin płatności | Ustaw domyślny termin w ustawieniach |
| Błędny adres | Zweryfikuj dane w CEIDG/KRS |

### Jak unikać błędów
- [ ] Zawsze sprawdzaj przed wysłaniem
- [ ] Utrzymuj aktualne dane firmy
- [ ] Korzystaj z szablonów
- [ ] Rób audyt faktur co miesiąc

---

## 8. ZAŁĄCZNIKI I LINKI

### Oficjalne źródła
- KSeF Portal: https://ksef.mf.gov.pl
- Ministerstwo Finansów: https://www.gov.pl/web/finanse
- ePUAP: https://epuap.gov.pl
- GUS: https://gus.gov.pl

### Pomoc techniczna
- Infolinia KSeF: 800 007 007 (bezpłatna)
- Email: ksef@mf.gov.pl
- FAQ: https://ksef.mf.gov.pl/pomoc

### Przydatne narzędzia
- Sprawdzanie NIP: https://www.gus.gov.pl/wyszukiwarka
- Kalkulator VAT: https://www.podatki.gov.pl/kalkulatory
- Kursy walut NBP: https://nbp.pl/kursy

### Do pobrania
- [ ] Szablony faktur (PDF)
- [ ] Instrukcja PDF (ta strona)
- [ ] Checklist do druku

---

## NOTATKI

### Moje dane firmowe
```
Nazwa: _____________________
NIP: ______________________
REGON: ____________________
Adres: ____________________
Email: ____________________
Telefon: __________________
```

### Moje terminy
```
Data rejestracji w KSeF: _____________
Data pierwszej faktury: _____________
Termin pierwszego rozliczenia: _______
```

### Kontakty
```
Biuro rachunkowe: ___________________
Księgowy: __________________________
Bank: ______________________________
```

---

*© 2026 KSeF Blog - Twoje centrum wiedzy o KSeF*
*Darmowy checklist dla subskrybentów*

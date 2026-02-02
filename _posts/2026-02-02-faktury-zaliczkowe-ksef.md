---
layout: post
title: "Faktury zaliczkowe w KSeF: kompletny przewodnik"
date: 2026-02-02 09:00:00 +0100
author: "Zespół firmowid.pl"
categories: [ksef, faktury, zaliczki]
tags: [ksef, faktury-zaliczkowe, slim-vat-2, firmowid]
excerpt: "Jak wystawiać faktury zaliczkowe w KSeF? Krok po kroku dla deweloperów i księgowych."
---

**Czas czytania:** 6 minut

---

## Faktury zaliczkowe — co się zmieniło?

W starym systemie faktura zaliczkowa była prosta: wystawiasz, wysyłasz, koniec.

W KSeF? **Musi przejść przez centralny system** — i tu zaczynają się schody.

---

## Krok 1: Zaliczka w KSeF

Gdy dostajesz zaliczkę:

1. **Wystaw fakturę zaliczkową** w systemie
2. **Wyślij do KSeF** — kontrahent musi ją "odebrać"
3. **Zachowaj numer KSeF** — to Twój dowód

⚠️ **Uwaga:** Zaliczka bez numeru KSeF = problem przy rozliczeniu VAT

---

## Krok 2: Faktura końcowa

Gdy robisz fakturę końcową:

- **Powiąż ją z zaliczką** — w polu `fakturaZaliczkowa`
- **Podaj numer KSeF zaliczki** — system to sprawdzi
- **Wyślij do KSeF** — i gotowe

---

## Najczęstsze błędy

### ❌ Błąd #1: Brak powiązania
Faktura końcowa bez linku do zaliczki = nieprawidłowa.

### ❌ Błąd #2: Zaliczka "wisi"
Kontrahent nie odebrał zaliczki w KSeF — faktura końcowa się nie wyśle.

### ❌ Błąd #3: Zła kolejność
Najpierw zaliczka, potem końcowa. Nie na odwrót!

---

## Przykład w XML (dla deweloperów)

```xml
<faktura>
  <typ>FZ</typ> <!-- Faktura zaliczkowa -->
  <zaliczka>
    <kwota>1000.00</kwota>
    <dataPrzelewu>2026-02-01</dataPrzelewu>
  </zaliczka>
</faktura>
```

---

## Czy to musi być tak skomplikowane?

**Nie.** Jeśli używasz **firmowid.pl**:

✅ Automatyczne powiązanie zaliczek  
✅ Walidacja przed wysłaniem  
✅ Przypomnienia do kontrahentów  

[Zobacz jak to działa](https://firmowid.pl)

---

## Podsumowanie

Faktury zaliczkowe w KSeF wymagają:
- Dokładnego powiązania zaliczki z końcową
- Numerów KSeF na każdym etapie
- Cierpliwości — system bywa wolny

**Albo po prostu użyj narzędzia które robi to za Ciebie.**

---

*Masz pytanie o faktury zaliczkowe? Komentarz poniżej!*

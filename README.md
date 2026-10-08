# KreatorPRO

**Kreator produktów do druku dla sklepów IdoSell** — [kreatorproduktow.pl](https://kreatorproduktow.pl)

Klient sklepu projektuje produkt w przeglądarce (baner, koszulkę, naklejkę, kubek…), a sklep dostaje gotowy plik do druku
podpięty pod zamówienie. Usługa działa w modelu SaaS: każdy sklep ma własny panel, szablony, wygląd i licencję.

> To repozytorium zawiera wyłącznie opis projektu. Kod źródłowy KreatorPRO jest zamknięty i przechowywany w prywatnym repozytorium.

---

## Historia projektu

- **jesień 2025:** pierwsze prace i prototyp kreatora;
- **2025–2026:** rok rozwoju aplikacji: kreator, plik do druku, panel sklepu, integracja z IdoSell, model SaaS;
- **2026:** start usługi na [kreatorproduktow.pl](https://kreatorproduktow.pl).

---

## Co potrafi

**Kreator dla klienta sklepu**
- teksty z efektami (złoto i gradienty, obrysy, 3D, tekst na łuku), kształty, kod QR, ponad 5000 elementów i ikon, grafiki sklepu;
- zdjęcia z kontrolą rozdzielczości, gumka, usuwanie tła i magiczna gumka (AI działające na naszym serwerze);
- produkty wielostronicowe, naklejki z linią cięcia po konturze, nawijki, makiety (mockupy);
- gotowe wzory projektów od sklepu i instrukcja dla kupującego;
- działa na telefonie i komputerze.

**Plik do druku**
- PDF wektorowy albo bitmapa w wybranym DPI, PNG, spad, margines bezpieczeństwa;
- tekst edytowalny albo zamieniony na krzywe (bezpieczny dla CorelDRAW i programów RIP);
- osobny plik linii cięcia (CutContour) dla naklejek;
- link do projektu trafia do komentarza zamówienia w IdoSell, a numer zamówienia jest dopasowywany automatycznie.

**Panel sklepu**
- szablony, produkty IdoSell, wygląd kreatora, wzory, grafiki sklepu, czcionki;
- projekty klientów z pobieraniem pojedynczym i zbiorczym (ZIP), statusami produkcji i prośbą o poprawkę;
- czas przechowywania plików ustawiany przez sklep (do 30 dni, z dodatkowym miejscem do 90 albo 365 dni);
- konwerter plików (PDF/AI → PNG, JPG, TIFF CMYK), statystyki, pomoc z wyszukiwarką;
- zgłoszenia (helpdesk) z odpowiedziami także e-mailem;
- licencje, zamówienia z proformą, dodatki zamawiane w panelu: white label (kreator na domenie sklepu) i dodatkowe miejsce na pliki.

**Pliki i bezpieczeństwo**
- pliki klientów w magazynie obiektowym S3 (Hetzner, Niemcy, UE) z szybką kopią podręczną na serwerze — linki do plików w zamówieniach się nie zmieniają;
- prywatne pliki z czasowymi linkami do pobrania, automatyczne usuwanie po czasie przechowywania;
- codzienne kopie zapasowe poza serwerem, monitoring z alarmami.

**Plany**
- Standard: do 500 produktów, 10 GB na pliki; Premium: do 5000 produktów, 30 GB, konwerter plików;
- dodatkowe miejsce: +50 GB albo +100 GB, dokupowane w dowolnym momencie.

**Integracja z IdoSell**
- przez klucz API sklepu albo jako aplikacja w katalogu IdoSell Apps (logowanie z panelu IdoSell).

---

## Technologie

Node.js, Express, Vue 3, Vite, Fabric.js, pdfkit, ONNX Runtime (modele AI na własnym serwerze, bez zewnętrznych usług), S3 (Hetzner Object Storage), Playwright.

---

## Kontakt

Chcesz kreator w swoim sklepie IdoSell? → [kreatorproduktow.pl](https://kreatorproduktow.pl)

© PanSkull (NIP 7681795581), [panskull.pl](https://www.panskull.pl). Wszelkie prawa zastrzeżone.
Nazwa, opis i oprogramowanie KreatorPRO są własnością PanSkull.

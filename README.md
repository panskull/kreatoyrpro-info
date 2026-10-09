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
- 7 języków: polski, angielski, niemiecki, czeski, słowacki, ukraiński, rumuński — język wykrywany automatycznie albo ustawiony przez sklep, z przełącznikiem flagi;
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
- kosz: usunięte projekty (ręcznie albo po czasie przechowywania) można przywrócić przez kilka dni — wracają pod ten sam link w zamówieniu;
- panel w 7 językach; instrukcja dla kupującego w wielu językach — tłumaczona ręcznie albo automatycznie (DeepL, Google Translate lub AI, własnym kluczem sklepu);
- konwerter plików (PDF/AI → PNG, JPG, TIFF CMYK), statystyki, pomoc z wyszukiwarką;
- zgłoszenia (helpdesk) z odpowiedziami także e-mailem;
- licencje, zamówienia z proformą, dodatki zamawiane w panelu: white label (kreator na domenie sklepu) i dodatkowe miejsce na pliki.

**Pliki i bezpieczeństwo**
- pliki klientów w magazynie obiektowym S3 (Hetzner, Niemcy, UE) z szybką kopią podręczną na serwerze — linki do plików w zamówieniach się nie zmieniają;
- prywatne pliki z czasowymi linkami do pobrania, automatyczne usuwanie po czasie przechowywania, kosz projektów;
- codzienne kopie zapasowe poza serwerem (także plików klientów), monitoring z alarmami.

**Plany**
- Standard: 249 zł netto / mies., do 500 produktów, 10 GB na pliki; Premium: 349 zł netto / mies., do 5000 produktów, 30 GB, konwerter plików;
- 30 dni za darmo po rejestracji, bez karty i bez automatycznych płatności;
- dodatkowe miejsce: +50 GB albo +100 GB, dokupowane w dowolnym momencie.

**Integracja z IdoSell**
- przez klucz API sklepu albo jako aplikacja w katalogu IdoSell Apps (logowanie z panelu IdoSell).

---

## Aktualizacje

- **9.10.2026 (noc):** grafiki sklepu do 10 MB na plik (limity ustawiane indywidualnie dla sklepu); poprawione wejście do panelu z IdoSell; dzisiejsze zamówienia z projektów widoczne od razu na stronie Start i w kafelku „Dziś” w statystykach; poprawiony wygląd panelu sklepu na telefonie (Start, Linki do kreatora, Ustawienia, Wygląd kreatora, Konwerter).
- **9.10.2026 (cennik):** okres próbny wydłużony do 30 dni; nowe ceny: Standard 249 zł, Premium 349 zł netto / mies. (także w katalogu IdoSell Apps).
- **9.10.2026 (wieczór):** statystyki użytkowników kreatora w panelu sklepu i dla operatora usługi (ilu kupujących jest w kreatorze teraz, dziennie i miesięcznie, ilu zapisało projekt — bez ciasteczek i bez zapisu adresów IP); wyszukiwarka w dzienniku e-maili.
- **9.10.2026:** kreator i panel sklepu w 7 językach; instrukcja dla kupującego w wielu językach z tłumaczeniem automatycznym (DeepL, Google Translate, AI) albo ręcznym; kosz projektów z przywracaniem (osobny czas dla projektów z zamówieniem i bez); dokładniejsze dopasowanie zamówień IdoSell do projektów i czytelniejsze statystyki zamówień; codzienna kopia plików klientów poza serwerem.
- **8.10.2026:** pliki klientów w magazynie S3 (Hetzner, UE); plany 10 GB / 30 GB i dodatkowe miejsce +50 / +100 GB; white label zamawiany w panelu.

---

## Technologie

Node.js, Express, Vue 3, Vite, Fabric.js, pdfkit, ONNX Runtime (modele AI na własnym serwerze, bez zewnętrznych usług), S3 (Hetzner Object Storage), Playwright.

---

## Kontakt

Chcesz kreator w swoim sklepie IdoSell? → [kreatorproduktow.pl](https://kreatorproduktow.pl)

© PanSkull (NIP 7681795581), [panskull.pl](https://www.panskull.pl). Wszelkie prawa zastrzeżone.
Nazwa, opis i oprogramowanie KreatorPRO są własnością PanSkull.

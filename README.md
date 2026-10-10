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

- **10.10.2026 (wtyczka WooCommerce):** przycisk „Zaprojektuj” na karcie produktu WooCommerce — wtyczka KreatorPRO do pobrania z panelu (Integracje → WooCommerce). Klient projektuje przed zakupem, projekt trafia do koszyka (osobna pozycja dla każdego projektu, produkty z wariantami po wyborze opcji) i do zamówienia jako „Projekt klienta” z linkami do pliku do druku i podglądu; zgodna z HPOS i koszykiem w blokach, działa też z własną domeną kreatora (white label). Strona główna: zespół i uprawnienia, dodatkowe konta w cenniku, powiększanie zrzutów w sekcji Integracje.
- **10.10.2026 (użytkownicy panelu):** każdy loguje się do panelu sklepu domeną, swoim e-mailem i hasłem (właściciel: e-mail konta sklepu i dotychczasowe hasło). Zakładka Użytkownicy: właściciel zaprasza osoby z zespołu mailem i wybiera moduły, do których mają dostęp (gotowe zestawy, np. Drukarz — tylko Projekty klientów, bez usuwania, statystyk i ustawień); uprawnienia sprawdzane przy każdym zapytaniu, zmiana i wyłączenie konta działają od razu; link do nowego hasła wysyłany przez właściciela. 3 konta w cenie, każde kolejne +5 zł netto / mies. (w Licencji). Integracje: tryb „Tylko link do projektu” osobno dla Apilo i BaseLinkera — zamówienia z własnego sklepu dostają tylko link do pliku projektu w notatce, bez pobierania produktów, reguł i maili (nic nie liczy się podwójnie).
- **10.10.2026 (integracje i automatyzacje):** zakładka Integracje — IdoSell, WooCommerce, BaseLinker i Apilo (kluczem API, także kilka naraz; produkty z wielu systemów z filtrem źródła). Automatyzacje „JEŻELI… TO…”: po zamówieniu z wybranego źródła (np. Allegro, Amazon) i w wybranym statusie klient dostaje mail z osobistym linkiem do kreatora (w języku swojego kraju, z przypomnieniem), a po zapisie projektu link do pliku trafia do notatki zamówienia i status zmienia się sam — w obie strony; podgląd reguły na ostatnich zamówieniach i testowy mail. To samo zamówienie w kilku systemach łączy się z jednym projektem (bez drugiego maila, wyszukiwanie po numerach z każdego systemu). Czasy pobierania zamówień ustawia obsługa (na zakładkę: sklepy przed Apilo / BaseLinkerem). Ostrzeżenia o kończącym się miejscu na pliki, adres do odpowiedzi w poczcie sklepu, „Propozycja zmian” w Zgłoszeniach, poprawka projektu zapisanego z linku do kreatora. Nowa strona główna: od projektu do druku w jednym panelu.
- **10.10.2026 (linki do kreatora):** sklep decyduje przy każdym linku, czy kreator prosi klienta o dane kontaktowe (nie pytaj / nieobowiązkowo / e-mail wymagany) — e-mail, imię lub firma, telefon i uwagi trafiają do maila o nowym projekcie i na kartę projektu w panelu (wyszukiwarka znajduje projekt po e-mailu i telefonie); klient dostaje z poczty sklepu potwierdzenie z podglądem projektu albo linkiem do produktu; nowe „Domyślne ustawienia linków” (ważność, co po zapisie, dane kontaktowe) dla każdego nowego linku.
- **10.10.2026 (Google i AI):** operator usługi może podłączyć Google Tag Manager, Google Analytics i Google Ads do strony sprzedażowej — skrypty Google ładują się wyłącznie po zgodzie odwiedzającego na cookies (Consent Mode v2), a panel sklepu i kreator w sklepach nadal działają bez żadnych skryptów śledzących. Aktualna mapa strony dla wyszukiwarek, poprawione dane strukturalne (ceny, okres próbny) i opis dla asystentów AI (llms.txt).
- **10.10.2026 (panel):** menu boczne panelu sklepu i kolumna statusów w Projektach przewijają się, gdy nie mieszczą się na ekranie (małe laptopy, tablety, panel otwarty w IdoSell); grupy statusów (np. „Status produkcji”) można zwinąć — panel to zapamiętuje; na telefonie pasek z menu zostaje u góry przy przewijaniu. Operator usługi: kosz projektów z wyszukiwarką (kilka fraz naraz, np. sklep + nazwa pliku + data) i przewijaną listą.
- **10.10.2026 (zamówienia):** sklep sam ustawia w panelu (Ustawienia → Sklep i IdoSell), jak często kreator sprawdza nowe zamówienia IdoSell z projektami: co 1, 2, 5, 10, 15 albo 30 minut (domyślnie 10); numer zamówienia może pojawić się przy projekcie już po minucie. Gdy sprawdzanie zamówień nie działa dłużej niż godzinę (np. IdoSell odrzuca klucz API), operator usługi dostaje alarm i od razu widzi przyczynę.
- **10.10.2026:** kreator na telefonie: logo sklepu i przycisk „Zakończ” w górnym pasku nie są już ucinane, przyciski okna zatwierdzenia projektu zawsze widoczne na dole ekranu, okno wyboru sposobu zamówienia naklejek mieści się na małych ekranach.
- **9.10.2026 (noc):** grafiki sklepu do 10 MB na plik (limity ustawiane indywidualnie dla sklepu); poprawione wejście do panelu z IdoSell; dzisiejsze zamówienia z projektów widoczne od razu na stronie Start i w kafelku „Dziś” w statystykach; poprawiony wygląd panelu sklepu na telefonie (Start, Linki do kreatora, Ustawienia, Wygląd kreatora, Konwerter) i panelu operatora usługi; komunikaty w kreatorze (np. o zbyt niskiej rozdzielczości zdjęcia) można zamknąć przyciskiem ✕, żeby nie zasłaniały projektu.
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

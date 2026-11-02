# Hanzi Study — wersja startowa do GitHub Pages

## Co jest w tej paczce
- Twoja poprzednia aplikacja na bazie istniejącego kodu, z usuniętym testowym fragmentem blokującym ćwiczenie pisania.
- Tryb jasny/ciemny z zapamiętywaniem wyboru.
- Własne foldery i fiszki z polskim tłumaczeniem.
- Lokalny import i wyszukiwanie bazy CC-CEDICT (plik tekstowy importujesz samodzielnie).
- Możliwość oznaczenia własnego znaku/wariantu oraz zapisania własnej liczby kresek i instrukcji.
- Eksport i przywracanie kopii JSON (foldery, słówka, postępy i lokalny słownik).
- Pastelowa ikona z białym znakiem 尹.
- PWA / podstawowy cache aplikacji.

## Publikacja na GitHub Pages
1. Rozpakuj ZIP.
2. Utwórz repozytorium GitHub, np. `hanzi-study`.
3. Wgraj **zawartość** tego folderu do głównego katalogu repozytorium. Ważne: plik startowy musi nazywać się `index.html` (już tak jest).
4. Repozytorium → Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save.
5. Otwórz opublikowany adres. Na telefonie w Safari wybierz Udostępnij → Dodaj do ekranu początkowego.

## Lokalny słownik CC-CEDICT
Aplikacja nie pobiera automatycznie słownika z MDBG ani CC-CEDICT. Pobierz legalnie plik tekstowy CC-CEDICT z oficjalnej strony projektu MDBG/CC-CEDICT, sprawdź aktualne warunki licencji CC BY-SA 4.0 i zachowaj informację o autorach/licencji. Następnie w aplikacji otwórz zakładkę **Słownik** i zaimportuj plik `.u8` lub `.txt`. Dane zostaną zapisane lokalnie w przeglądarce. Angielskie znaczenia są podglądem źródłowym; polskie tłumaczenie wpisujesz samodzielnie.

## Ważne ograniczenia tej wersji
- To działająca wersja startowa, nie pełny odpowiednik Skritter.
- Standardowe znaki są sprawdzane przez Hanzi Writer, który wymaga pobrania biblioteki i danych znaków z CDN (internet).
- Dla własnych znaków zapisujemy Twoją liczbę kresek i instrukcje. Automatyczny silnik oceny własnego kształtu/kolejności kresek nie jest jeszcze zaimplementowany; te reguły są na razie Twoją dokumentacją do ćwiczenia.
- Własne znaki, słówka i postępy są przechowywane w pamięci przeglądarki. Regularnie używaj eksportu kopii. Czyszczenie danych przeglądarki może je usunąć.
- Wyszukiwanie słownika jest lokalne po imporcie. Sama baza CC-CEDICT nie zawiera polskich tłumaczeń.

## Prywatność i koszty
Aplikacja jest statyczna i może być hostowana przez GitHub Pages bez płatnego backendu. Dane nauki pozostają w przeglądarce. Uwaga: jeśli repozytorium lub strona GitHub Pages są publiczne, sam kod strony jest publiczny — nie umieszczaj w repozytorium prywatnych danych ani kopii słownika, jeśli nie chcesz ich publikować.


## Wbudowany słownik CC-CEDICT

Projekt zawiera plik `cedict_ts.u8` z bazą CC-CEDICT udostępnianą przez MDBG.
Źródło: https://www.mdbg.net/chinese/dictionary?page=cc-cedict
CC-CEDICT jest udostępniany na licencji Creative Commons Attribution-ShareAlike 4.0 (CC BY-SA 4.0).
Przy rozpowszechnianiu bazy lub jej adaptacji należy zachować informację o źródle i licencji oraz udostępniać adaptacje na zgodnych warunkach.

Baza jest automatycznie wczytywana przy pierwszym uruchomieniu zakładki Słownik i zapisywana w IndexedDB.
Polskie tłumaczenia można wyszukiwać w słówkach zapisanych przez użytkownika; definicje CC-CEDICT są angielskie.

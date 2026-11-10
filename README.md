# Atak na Rynku Głównym w Krakowie (7.11.2026) — zweryfikowane informacje

Statyczna strona (`index.html`) z mapą zdarzenia, chronologią, faktami z oficjalnych komunikatów
(policja, prokuratura, wojewoda, MSWiA) oraz listą zdementowanych informacji.

- Mapa: Leaflet + OpenStreetMap (trasa przejazdu przybliżona).
- Chronologia: tablica `TL` w `index.html` — typ `o` (oficjalne), `m` (media), `d` (dementi).
- Źródła: tablica `SRC` w `index.html`.

Aktualizacja: dopisz wpis do `TL`, popraw liczby w sekcji `.stats` i datę „Stan na”.

## Aktualizacja strony
Przy każdej aktualizacji zmień w `index.html`:
- `<b id="lastUpdate">…</b>` (pasek na górze, np. `pon. 9.11, 12:30`),
- stałą `LAST_UPDATE` w skrypcie (ISO, np. `2026-11-09T12:30:00+01:00`) — z niej liczy się „X min temu”,
- linię „Stan informacji na:” w nagłówku.
- ramkę „Najnowsze” (`#whatsnew`) — 3–5 najważniejszych zmian,
- `NEW_COUNT` w skrypcie chronologii — ile ostatnich wpisów `TL` oznaczyć jako NOWE.
- sekcję „Szybkie odpowiedzi” (`#faq`) i streszczenie po angielsku (`#english`), jeśli zmieniły się kluczowe fakty.

Otwarta strona sama sprawdza co 3 min, czy `LAST_UPDATE` się zmienił, i pokazuje przycisk „Są nowe informacje — odśwież”.

## Źródła i rozbieżności
- `SRC` w `index.html`: `[kategoria, tytuł, URL]`, kategorie: `ofic` (oficjalne), `rek` (rekonstrukcje), `fakt` (fact-checking), `pl` (media polskie), `swiat` (media zagraniczne), `ency` (opracowania).
- Sekcja `#rozbieznosci` — tabela miejsc, w których źródła się różnią, i przyjętej wersji.

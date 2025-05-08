Opis:
  Skrypt air_quality_fetcher.py pobiera dane o jakości powietrza (PM10 i PM2.5)
  z publicznego API GIOŚ, co 10 minut. Dane są zapisywane do plików .json
  w katalogu `data/`, a logi do pliku `fetcher.log`.

Wymagania:
  - Python 3.10 lub nowszy

Jak uruchomić:
  1. Zainstaluj biblioteki:
     pip install -r requirements.txt

  2. Uruchom skrypt:
     python air_quality_fetcher.py

Dane wejściowe:
  - API GIOŚ (otwarte, nie wymaga klucza)

Dane wyjściowe:
  - JSON: ./data/gios_YYYYMMDDThhmmssZ.json (pomiar z każdej stacji i sensora)
  - Logi: ./fetcher.log

Konfiguracja (opcjonalnie przez zmienne środowiskowe):
  - GIOS_STATION_IDS: lista ID stacji (domyślnie: 400,401)
  - FETCH_INTERVAL_MIN: interwał pobierania w minutach (domyślnie: 10)
  - OUTPUT_DIR: folder na dane (domyślnie: ./data)

Przykład:
  - Pobierane dane z Warszawa-Targówek (400) i Warszawa-Komunikacyjna (401)
  - Zapis do `data/`
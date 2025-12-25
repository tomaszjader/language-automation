# Telegram Anki Reminder Bot

Prosty automatyczny system przypomnień o nauce słówek w Anki, zbudowany w n8n.

## Funkcje
* **Automatyczny wyzwalacz**: Codzienne uruchomienie o godzinie **08:30**.
* **Baza danych**: Pobieranie danych (np. ID czatu) z wbudowanych tabel n8n (Data Table).
* **Integracja z Telegramem**: Personalizowane powiadomienie motywujące do nauki.

## Struktura Workflow
1.  **Schedule Trigger**: Planuje start procesu.
2.  **Get row(s)**: Pobiera rekordy z tabeli `n8n` (ID: `r5iHFZ9vD734mOPl`).
3.  **Telegram (Send message)**: Wysyła tekst: *"Wiem że masz czas i przerób teraz 5 słówek w Anki"* do odbiorców z bazy.

## Wymagania
* Narzędzie n8n (wersja z obsługą Data Table).
* Bot Telegrama (Token API).

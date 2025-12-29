# Daily English Learning Assistant

Ten workflow dla platformy **n8n** to automatyczny asystent nauki języka angielskiego. System wysyła zaplanowane powiadomienia na **Telegram**, serwując użytkownikowi odpowiednie materiały edukacyjne (podcasty, czat AI, fiszki) w optymalnych porach dnia.

## 🚀 Funkcje

Workflow automatyzuje wysyłkę trzech rodzajów aktywności:
* **07:30** – Pasywne słuchanie: Link do najnowszego odcinka *BBC Learning English*.
* **08:30** – Aktywne powtarzanie: Przypomnienie o sesji w aplikacji *AnkiDroid*.
* **20:00** – Konwersacje: Zachęta do rozmowy z *Google Gemini* w celu przełamania bariery językowej.

## 🛠️ Struktura Techniczna

Workflow został zbudowany z wykorzystaniem następujących komponentów:

1.  **Schedule Triggers**: Trzy niezależne wyzwalacze czasowe sterujące harmonogramem dnia.
2.  **n8n DataTables**: Węzły pobierające dane użytkowników (np. `id_chat`) z wewnętrznej bazy danych n8n, co pozwala na łatwe zarządzanie listą odbiorców.
3.  **Telegram Node**: Wykorzystuje API Telegrama do wysyłania sformatowanych wiadomości (HTML), zawierających bezpośrednie linki do zasobów.

## 📦 Instalacja i Konfiguracja

1.  **Import**: Skopiuj plik JSON workflow i zaimportuj go do swojego n8n (**Import from File** lub **Paste**).
2.  **Połączenia (Credentials)**:
    * Skonfiguruj **Telegram API** (wymagany token od @BotFather).
    * Upewnij się, że masz dostęp do swojej bazy **n8n DataTable**.
3.  **Dane**: Twoja tabela w n8n powinna zawierać kolumnę `id_chat`, aby węzeł mógł poprawnie zaadresować wiadomość.

## 📋 Podgląd wiadomości

Wiadomości są formatowane za pomocą tagów HTML, co pozwala na estetyczne wyświetlanie linków:
> "Wiem, że masz czas, posłuchaj podcastu po angielsku. 🎧 Słuchaj: The English We Speak"

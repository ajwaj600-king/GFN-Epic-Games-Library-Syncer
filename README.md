English Version (README.md)
GFN Epic Games Library Syncer

A powerful userscript suite to fully automate syncing your Epic Games library with NVIDIA GeForce NOW. It consists of two main components:

    Game List Fetcher: An intelligent script that automatically scrapes your entire Epic Games transaction history to generate an accurate list of all your owned games.
    Library Syncer: A robust script that takes this list and automatically adds each game to your GeForce NOW library, handling all the clicks for you.

If you have an extensive collection of free games from Epic, this suite will save you hours of monotonous work.

Example screenshot of the script in action
(Tip: Take a screenshot of the running script and place it here to show off the UI)
✨ Features

    Fully Automated: From generating the game list to adding them in GFN.
    Intelligent Game Fetcher: Scans all your Epic Games transaction pages automatically.
    Robust GFN Syncer: Searches for games, opens tiles, selects the Epic store, and confirms adding to your library.
    User-Friendly UI: The Syncer script adds a convenient control window to the GFN page to start, stop, and monitor the process.
    Resilient Logic: Built to handle page load delays and different UI states.

🙏 Credits

This project was a collaborative effort. A huge thank you to bytefogger for creating the original, brilliant scripts for fetching the Epic Games list. This project builds upon that foundation. You can find the original work here:

    bytefogger/gfn-epic-auto-sync on GitHub

🚀 Installation and Usage

The process is divided into two main parts: getting your game list from Epic, and then using that list in GeForce NOW.
Requirements

    A web browser (e.g., Chrome, Firefox, Edge).
    The Tampermonkey browser extension.

Part 1: Fetching Your Epic Games List

This script will automatically click the "Load More" button on your Epic Games transaction history page and collect all game titles.

    Install the Game List Fetcher Script:
        Open the Tampermonkey Dashboard, create a new script (+ tab).
        Copy the entire code from the 1-epic-games-list-fetcher.js file and paste it into the editor.
        Save the script (Ctrl + S).

    Run the Fetcher:
        Log in to your Epic Games account and navigate to your Transaction History:
        https://www.epicgames.com/account/transactions
        The script will start automatically. Open the developer console (F12) and go to the "Console" tab to watch the progress.
        It will click "Load More" repeatedly. Wait patiently until you see a 🎉 All done! message in the console. This can take several minutes if you have a large library.
        The console will then output a complete array of your game titles. Copy this entire array (including the [ and ] brackets).

Part 2: Syncing with GeForce NOW

Now we will use the list you just copied to automate adding games in GFN.

    Install the GFN Syncer Script:
        Go back to the Tampermonkey Dashboard and create another new script.
        Copy the entire code from the 2-gfn-library-syncer.js file and paste it into the editor.

    Paste Your Game List:
        Inside the script editor, find the line let gameTitles = [...].
        Replace the empty [] brackets with the complete game list array you copied from the Epic Games console.
        Save the script (Ctrl + S).

    Run the Syncer:
        Navigate to https://play.geforcenow.com/ and log in.
        The "GFN Syncer" control window will appear in the top-right corner.
        Click the green "▶️ Start Sync" button.
        The script will now work its way through your list. Sit back and relax!

Important: For the most stable performance, it's best to keep the GeForce NOW tab active and avoid moving the mouse while the syncer script is running.
⚠️ Known Issues and Limitations
Occasionally Launches a Game (Known Bug)

During testing, it was observed that in rare cases, the syncer script might accidentally launch a game instead of just closing the details panel.

    Cause: This happens because after successfully adding a game to the library, the MARK AS OWNED button is immediately replaced by a PLAY button. If the page lags for a moment, the script's click to close the panel might land on the new PLAY button.
    Workaround: If this occurs, simply close the new tab/window that opened to launch the game. The script should continue its work on the next item in the list without issues.

Wersja Polska (README.md)
GFN Epic Games Library Syncer

Potężny zestaw skryptów użytkownika (userscript) do pełnej automatyzacji synchronizacji Twojej biblioteki Epic Games z NVIDIA GeForce NOW. Składa się z dwóch głównych komponentów:

    Pobieracz Listy Gier: Inteligentny skrypt, który automatycznie przeszukuje Twoją historię transakcji w Epic Games, aby wygenerować dokładną listę posiadanych gier.
    Synchronizator Biblioteki: Solidny skrypt, który używa tej listy do automatycznego dodawania każdej gry do Twojej biblioteki GeForce NOW, wykonując wszystkie kliknięcia za Ciebie.

Jeśli masz obszerną kolekcję darmowych gier z Epic, ten zestaw zaoszczędzi Ci wielu godzin monotonnej pracy.

Przykładowy zrzut ekranu działania skryptu
(Wskazówka: Zrób zrzut ekranu działającego skryptu i umieść go tutaj, aby pokazać, jak wygląda interfejs)
✨ Funkcje

    Pełna Automatyzacja: Od wygenerowania listy gier po dodanie ich w GFN.
    Inteligentne Pobieranie Listy Gier: Automatycznie skanuje wszystkie strony Twojej historii transakcji w Epic.
    Solidny Synchronizator GFN: Wyszukuje gry, otwiera kafelki, wybiera sklep Epic i potwierdza dodanie do biblioteki.
    Przyjazny Interfejs: Skrypt synchronizujący dodaje wygodne okno kontrolne na stronie GFN, aby uruchamiać, zatrzymywać i monitorować proces.
    Odporna Logika: Zbudowany, aby radzić sobie z opóźnieniami w ładowaniu strony i różnymi stanami interfejsu.

🙏 Podziękowania

Ten projekt jest owocem współpracy. Ogromne podziękowania dla bytefogger za stworzenie oryginalnych, genialnych skryptów do pobierania listy gier z Epic. Ten projekt bazuje na jego fundamentalnej pracy. Oryginalne repozytorium znajdziesz tutaj:

    bytefogger/gfn-epic-auto-sync na GitHubie

🚀 Instalacja i Użytkowanie

Proces jest podzielony na dwie główne części: pobranie listy gier z Epic, a następnie użycie jej w GeForce NOW.
Wymagania

    Przeglądarka internetowa (np. Chrome, Firefox, Edge).
    Rozszerzenie Tampermonkey.

Część 1: Pobieranie Listy Gier z Epic

Ten skrypt będzie automatycznie klikał przycisk "Wczytaj więcej" na stronie historii transakcji Epic i zbierze wszystkie tytuły gier.

    Zainstaluj skrypt Pobieracza Listy Gier:
        Otwórz Panel Tampermonkey, stwórz nowy skrypt (zakładka +).
        Skopiuj całą zawartość pliku 1-epic-games-list-fetcher.js i wklej ją do edytora.
        Zapisz skrypt (Ctrl + S).

    Uruchom Pobieracz:
        Zaloguj się na swoje konto Epic Games i przejdź do Historii Transakcji:
        https://www.epicgames.com/account/transactions
        Skrypt uruchomi się automatycznie. Otwórz konsolę deweloperską (F12) i przejdź do zakładki "Konsola", aby obserwować postępy.
        Skrypt będzie wielokrotnie klikał "Wczytaj więcej". Czekaj cierpliwie, aż w konsoli pojawi się komunikat 🎉 All done!. Może to potrwać kilka minut, jeśli masz dużą bibliotekę.
        Na końcu konsola wyświetli kompletną tablicę z tytułami Twoich gier. Skopiuj całą tę tablicę (razem z nawiasami [ i ]).

Część 2: Synchronizacja z GeForce NOW

Teraz użyjemy skopiowanej listy, aby zautomatyzować dodawanie gier w GFN.

    Zainstaluj skrypt Synchronizatora GFN:
        Wróć do Panelu Tampermonkey i stwórz kolejny nowy skrypt.
        Skopiuj całą zawartość pliku 2-gfn-library-syncer.js i wklej ją do edytora.

    Wklej swoją listę gier:
        W edytorze skryptu znajdź linię let gameTitles = [...].
        Zastąp puste nawiasy [] kompletną tablicą z listą gier, którą skopiowałeś z konsoli Epic Games.
        Zapisz skrypt (Ctrl + S).

    Uruchom Synchronizator:
        Przejdź na stronę https://play.geforcenow.com/ i zaloguj się.
        W prawym górnym rogu ekranu pojawi się okno kontrolne "GFN Syncer".
        Kliknij zielony przycisk "▶️ Start Sync".
        Skrypt rozpocznie pracę. Usiądź wygodnie i obserwuj!

Ważne: Aby zapewnić stabilne działanie, najlepiej jest utrzymywać kartę GeForce NOW aktywną i nie ruszać myszką podczas pracy skryptu synchronizującego.
⚠️ Znane Problemy i Ograniczenia
Sporadyczne uruchamianie gry (Znany błąd)

Podczas testów zauważono, że w rzadkich przypadkach skrypt synchronizujący może przypadkowo uruchomić grę zamiast tylko zamknąć panel szczegółów.

    Przyczyna: Dzieje się tak, ponieważ po pomyślnym dodaniu gry do biblioteki przycisk OZNACZ JAKO POSIADANA jest natychmiast zastępowany przyciskiem ZAGRAJ. Jeśli strona na chwilę się opóźni, kliknięcie skryptu mające na celu zamknięcie panelu może trafić w nowy przycisk ZAGRAJ.
    Rozwiązanie: Jeśli to się stanie, po prostu zamknij nowo otwartą kartę/okno uruchamiania gry. Skrypt powinien bez problemu kontynuować pracę od następnej pozycji na liście.

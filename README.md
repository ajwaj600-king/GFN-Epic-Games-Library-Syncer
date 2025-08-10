# GFN-Epic-Games-Library-Syncer
A simple yet powerful userscript to automatically add your Epic Games titles to your NVIDIA GeForce NOW library. If you have an extensive collection of free games from Epic and are tired of manually clicking through hundreds of titles, this script is for you.

# PL
GFN Epic Games Library Syncer

Prosty, ale potężny skrypt użytkownika (userscript) do automatycznego dodawania Twoich gier z Epic Games do biblioteki NVIDIA GeForce NOW. Jeśli masz obszerną kolekcję darmowych gier z Epic i męczy Cię ręczne przeklikiwanie setek tytułów, ten skrypt jest dla Ciebie.

Przykładowy zrzut ekranu działania skryptu
(Wskazówka: Zrób zrzut ekranu działającego skryptu i umieść go tutaj, aby pokazać, jak wygląda interfejs)
⚙️ Jak to działa?

Skrypt działa w tle na stronie GeForce NOW, wykonując za Ciebie całą monotonną pracę:

    Wczytuje predefiniowaną listę tytułów gier.
    Automatycznie wyszukuje każdą grę po kolei.
    Otwiera kafelek ze szczegółami gry.
    Inteligentnie wybiera sklep Epic Games Store (jeśli dostępnych jest więcej opcji).
    Klika "OZNACZ JAKO POSIADANA" i potwierdza operację.
    Zamyka panel i przechodzi do następnej gry, aż do wyczerpania listy.

Wszystko to dzieje się w przejrzystym interfejsie użytkownika z logowaniem postępów w czasie rzeczywistym.
🚀 Instalacja i Użytkowanie

Proces jest prosty i zajmuje mniej niż 2 minuty.
Wymagania

    Przeglądarka internetowa (np. Chrome, Firefox, Edge).
    Rozszerzenie Tampermonkey.

Kroki instalacji

    Zainstaluj Tampermonkey:
        Link dla Chrome
        Link dla Firefox

    Stwórz nowy skrypt:
        Kliknij ikonę Tampermonkey w przeglądarce i wybierz "Panel".
        Przejdź do zakładki z ikoną plusa +.

    Wklej kod:
        Usuń całą domyślną zawartość edytora.
        Skopiuj i wklej cały kod najnowszej, działającej wersji skryptu.

    Zapisz skrypt:
        W menu edytora wybierz Plik -> Zapisz (lub naciśnij Ctrl + S).

Uruchomienie

    Przejdź na stronę https://play.geforcenow.com/ i zaloguj się.
    W prawym górnym rogu ekranu powinno pojawić się okienko "GFN Syncer".
    Kliknij duży, zielony przycisk "▶️ Start Sync", aby rozpocząć proces.
    Usiądź wygodnie i obserwuj postępy! Możesz przerwać operację w dowolnym momencie przyciskiem "🛑 Stop Sync".

Ważne: Aby zapewnić stabilne działanie, najlepiej nie ruszaj myszką ani nie przełączaj kart przeglądarki podczas pracy skryptu.
✏️ Jak zaktualizować listę gier?

Edycja listy gier jest bardzo prosta:

    Otwórz Panel Tampermonkey i kliknij nazwę skryptu (GFN Syncer...), aby go edytować.
    Znajdź sekcję let gameTitles = [...].
    Zastąp gry wewnątrz nawiasów kwadratowych [] własną listą, pamiętając, aby każdy tytuł był w cudzysłowie i oddzielony przecinkiem.

# EN

GFN Epic Games Library Syncer

A simple yet powerful userscript to automatically add your Epic Games titles to your NVIDIA GeForce NOW library. If you have an extensive collection of free games from Epic and are tired of manually clicking through hundreds of titles, this script is for you.

Example screenshot of the script in action
(Tip: Take a screenshot of the running script and place it here to show off the UI)
⚙️ How It Works

The script runs in the background on the GeForce NOW website, performing all the tedious work for you:

    It loads a predefined list of game titles.
    It automatically searches for each game, one by one.
    It opens the game details tile.
    It intelligently selects the Epic Games Store if multiple store options are available.
    It clicks "MARK AS OWNED" and confirms the action.
    It closes the panel and moves on to the next game until the list is complete.

All of this happens within a clean user interface that logs the progress in real-time.
🚀 Installation and Usage

The process is straightforward and takes less than 2 minutes.
Requirements

    A web browser (e.g., Chrome, Firefox, Edge).
    The Tampermonkey browser extension.

Installation Steps

    Install Tampermonkey:
        Link for Chrome
        Link for Firefox

    Create a new script:
        Click the Tampermonkey icon in your browser and select "Dashboard".
        Navigate to the tab with the plus + icon to create a new script.

    Paste the code:
        Delete all the default content in the editor.
        Copy and paste the entire code of the latest working version of the script.

    Save the script:
        From the editor's menu, go to File -> Save (or press Ctrl + S).

How to Run

    Navigate to https://play.geforcenow.com/ and log in.
    A new "GFN Syncer" window should appear in the top-right corner of the screen.
    Click the large, green "▶️ Start Sync" button to begin the process.
    Sit back, relax, and watch the progress! You can stop the operation at any time by clicking the red "🛑 Stop Sync" button.

Important: For the most stable performance, it's best to avoid moving the mouse or switching browser tabs while the script is running.
✏️ How to Update the Game List

Editing the game list is very simple:

    Open the Tampermonkey Dashboard and click on the script's name (GFN Syncer...) to edit it.
    Find the let gameTitles = [...] section.
    Replace the games inside the square brackets [] with your own list, ensuring each title is enclosed in quotes and separated by a comma.

Example:

JavaScript

let gameTitles = [
    "Cyberpunk 2077",
    "The Witcher 3: Wild Hunt",
    "Alan Wake 2"
];

    Save your changes (Ctrl + S). The script will now use your new list.

⚠️ Known Issues and Limitations
Occasionally Launches a Game (Known Bug)

During testing, it was observed that in rare cases (approx. 3 times in a ~160 game list), the script might accidentally launch a game instead of just closing the details panel.

    Cause: This happens because after successfully adding a game to the library, the MARK AS OWNED button is immediately replaced by a PLAY button. The script attempts to close the panel by clicking the X button, but if the page lags for a moment, the click might land on the new PLAY button that appeared in a similar position.
    Workaround: If this occurs, simply close the new tab/window that opened to launch the game. The script should continue its work on the next item in the list without issues once you return to the GFN page.

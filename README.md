1. Cel Aplikacji

Celem aplikacji jest umożliwienie użytkownikom interakcji poprzez wprowadzenie swojego imienia, które zostanie użyte do spersonalizowanego powitania. Aplikacja również wyświetla obrazek, co dodaje wizualny element do doświadczenia użytkownika.
2. Architektura Aplikacji

Aplikacja składa się z następujących komponentów:

Frontend: Używa Thymeleaf do renderowania dynamicznych stron HTML.
Backend: Używa Spring Boot do obsługi logiki aplikacji i zarządzania żądaniami HTTP.
Zasoby statyczne: Obrazy i inne pliki statyczne są przechowywane w folderze static.

4. Działanie Aplikacji
4.1. Strona Powitalna

    URL: /
    Opis: Po wejściu na stronę główną, użytkownik zobaczy komunikat powitalny.
    Logika: Metoda hello() w HelloController zwraca widok hello.html, który wyświetla komunikat powitalny.

4.2. Strona Powitania z Imieniem

    URL: /greeting?name=Vistula
    Opis: Użytkownik może wprowadzić swoje imię jako parametr w URL. Aplikacja wyświetli spersonalizowane powitanie.
    Logika: Metoda greeting() w HelloController przyjmuje parametr name, dodaje go do modelu, a następnie zwraca widok greeting.html, który wyświetla powitanie z imieniem użytkownika.

4.3. Wyświetlanie Obrazu

    Opis: Na stronie powitania (greeting.html) wyświetlany jest obrazek, który jest ładowany z folderu static/images.
    Logika: Użycie atrybutu th:src w Thymeleaf pozwala na dynamiczne ładowanie obrazu.

5. Przykładowe Scenariusze Użytkowania

    Scenariusz 1: Użytkownik odwiedza stronę główną (/).
        Oczekiwany wynik: Użytkownik widzi komunikat "Hello Vistula, in my first Spring controller".

    Scenariusz 2: Użytkownik odwiedza stronę powitania z imieniem (/greeting?name=Vistula).
        Oczekiwany wynik: Użytkownik widzi komunikat "Hello, Vistula!" oraz obrazek.

    Scenariusz 3: Użytkownik odwiedza stronę powitania bez podawania imienia (/greeting).
        Oczekiwany wynik: Użytkownik widzi komunikat "Hello, World!" oraz obrazek.

6. Wnioski

Aplikacja powitalna jest prostym, ale skutecznym przykładem użycia Spring Boot i Thymeleaf do tworzenia dynamicznych stron internetowych. Umożliwia interakcję z użytkownikami poprzez spersonalizowane powitania oraz dodaje elementy wizualne, 
co poprawia doświadczenie użytkownika. Aplikacja może być rozwijana o dodatkowe funkcjonalności, takie jak formularze, walidacja danych czy integracja z bazą danych.

Aplikacja umożliwia użytkownikowi wprowadzenie swojego imienia, które zostanie użyte do spersonalizowanego powitania.

Frontend: Używa Thymeleaf do renderowania dynamicznej strony HTML.

Backend: Używa Spring Boot do obsługi logiki aplikacji i zarządzania żądaniami HTTP.

Użytkownik może wprowadzić swoje imię jako parametr w URL a aplikacja wyświetli spersonalizowane powitanie. 
Metoda greeting() w HelloController przyjmuje parametr name, dodaje go do modelu a następnie zwraca widok greeting.html który wyświetla powitanie z imieniem użytkownika. W przypadku braku parametru w postaci imienia HelloController przyjmuje parametr "World". 
Na stronie powitania wyświetlany jest też obrazek, który jest ładowany z folderu static/images. Użycie atrybutu th:src w Thymeleaf pozwala na dynamiczne ładowanie obrazu.

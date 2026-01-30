<div align="center">
<div id="header" align="center">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS_rY3H6yyrrC7QWM-l-gYR5vw48gpNYMs--g&usqp=CAU" width="2000px"/>
</div>

<div align="left">

— to klient HTTP do testowania API. Klienci HTTP testują wysyłanie żądań z klienta do serwera oraz otrzymywanie odpowiedzi od serwera.

---

### API (Application Programming Interface)
 — to interfejs do wymiany danych z serwera między dwiema aplikacjami lub komponentami oprogramowania. Postman pomaga testerom w projektowaniu API i tworzeniu serwerów mock (symulujących działanie aplikacji). Na przykład za pomocą Postmana można przetestować, jak API rejestruje nowego użytkownika aplikacji, dodaje lub usuwa dane o nim na serwerze.

---

### Korzystanie z Postman

Dzięki Postman tester może:
+ tworzyć i wysyłać żądania HTTP do API;
+ tworzyć kolekcje (zestawy kolejnych żądań) i foldery żądań, aby skrócić czas testowania;
+ zmieniać parametry żądań (np. klucze autoryzacyjne i URL);
+ zmieniać środowiska żądań (np. na środowisku testowym, lokalnym lub na serwerze);
+ dodawać punkty kontrolne podczas wywoływania API (rejestrowanie momentu przesyłu danych);
+ przeprowadzać automatyczne testy API w oparciu o kolekcje żądań przy użyciu Collection Runner.

Do pracy z serwerami program wykorzystuje protokół HTTP. Tester wysyła żądania testowe z klienta na serwer i otrzymuje odpowiedź, czy w API wystąpił błąd.
Postman jest dostępny jako aplikacja na Windows, Linux i macOS, a także w interfejsie webowym (w tym wypadku wymaga zainstalowania Postman Desktop Agent).

Tak wygląda praca z kolekcjami żądań:

<img src="https://blog.skillfactory.ru/wp-content/uploads/2023/02/image1-5-2.png" width="2500px"/>

+ Kolekcja żądań do testu API. Wewnątrz kolekcji żądania można grupować w foldery.
+ Zakładka żądania w kolekcji.
+ Wybór metody żądania (GET, POST, PUT, DELETE).
+ URL żądania do serwera.
+ Przycisk wysłania żądania.
+ Wybór parametrów żądania (klucze i wartości — np. tylko usunięte obiekty).
+ Wynik wykonania żądania (kod, treść i czas odpowiedzi, a także rozmiar otrzymanych danych).

---

### Kolekcja
 — to plik projektu z powiązanymi żądaniami. Zazwyczaj żądania do testowania jednego API opisuje się w jednej kolekcji. Wewnątrz kolekcji żądania można grupować w foldery, np. według różnych wersji API lub testowanych elementów aplikacji.

W Postman istnieje narzędzie Collection Runner. Umożliwia ono jednoczesne wykonanie wszystkich żądań z kolekcji lub folderu w określonej liczbie iteracji i w ustalonej kolejności. Po zakończeniu wszystkich żądań Collection Runner generuje raport z oznaczeniem powodzenia żądań i kodami statusu.

Do automatycznych testów w kolekcjach, folderach i żądaniach można stosować skrypty w JavaScript. Na przykład wyniki jednego żądania mogą być wykorzystane jako warunki dla kolejnego.

---

### Metody Postman

Najczęściej w pracy z API stosuje się architekturę RESTful. W tej architekturze istnieją cztery standardowe metody żądań HTTP do serwera:

+ POST — tworzenie obiektu i wysyłanie danych na serwer;
+ GET — pobieranie informacji z serwera;
+ PUT — aktualizacja obiektu;
+ DELETE — usunięcie obiektu.

W Postman można testować żądania każdą z tych metod — należy ją wybrać w zakładce żądania. Po wysłaniu żądania tester otrzymuje odpowiedź w postaci kodu statusu HTTP. Istnieje łącznie 40 kodów w pięciu kategoriach; każdy kod pomaga zrozumieć, czy API działa poprawnie.

+ 1xx Informacja
Informacja o stanie przesyłu danych
+ 2xx Sukces
Żądanie zakończyło się sukcesem
+ 3xx Przekierowanie
Żądanie może zakończyć się sukcesem, ale pod innym URL
+ 4xx Błąd klienta
Błąd po stronie klienta uniemożliwiający wykonanie żądania
+ 5xx Błąd serwera
Błąd po stronie serwera uniemożliwiający przetworzenie żądania

---

### Przykłady żądań

Oto przykład testowania żądania pobierającego identyfikator użytkownika z serwera — GET user id.

+ Utwórz kolekcję i nadaj jej nazwę, np. Useridtest. Otwórz zakładkę żądania — będzie ona zapisana w tej kolekcji.
+ Wprowadź URL żądania. Do celów szkoleniowych można użyć publicznej dokumentacji Postman. Aby zwrócić identyfikator użytkownika, odpowiedni będzie URL
<a href="https://postman-echo.com/get?userId=333" target="_blank" rel="noreferrer noopener">https://postman-echo.com/get?userId=333</a>. W zakładce Params automatycznie pojawią się parametry żądania — userid.
+ Wybierz metodę żądania. Aby pobrać identyfikator użytkownika, należy użyć metody GET.
+ Wyślij żądanie. Kliknij przycisk Send — Postman wyśle żądanie do swojego echo-serwera szkoleniowego.
+ Otrzymaj odpowiedź. Program wyświetli treść odpowiedzi w oknie Response, a kod statusu pojawi się w menu powyżej. W przykładzie szkoleniowym żądanie zakończy się sukcesem: kod przyjmie wartość 200.

</div>

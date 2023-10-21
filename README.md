## Dodatkowe pola na wydruku etykiety UPS nadawanej przez WzA
To rozszerzenie pozwala na wydruk pól "Dodatkowa informacja na etykiecie" i "Numer referencyjny" na etykiecie przewoźnika UPS przy nadawaniu przesyłek przez "Wysyłam z Allegro".

Osobiście nie mam potrzeby korzystania z tego rozwiązania gdyż generuję etykiety pojedynczo w momencie szykowania paczki, jednak zdaję sobie sprawę że niektórym może się to przydać gdyż zgłaszali takie zapotrzebowanie na forum Allegro Gadane.

Jest to rozszerzenie do przeglądarki Chrome. Wszystkie rozszerzenia testuję tylko dla systemu Windows 10 i najnowszej wersji przeglądarki.

**Instrukcja instalacji:**
1. Kliknij ikonę menu rozszerzeń w prawym górnym rogu okna przeglądarki (ikona puzzla)
![chrome_extensions_menu_icon](https://github.com/tomsyty/Additional-informations-on-UPS-label/assets/41838854/250c501e-208e-4d73-a0e6-af40b11833b3)
lub z menu przeglądarki wybierz "Rozszerzenia - Zarządzaj rozszerzeniami".
2. Włącz "Tryb dewelopera" w prawym górnym rogu okna przeglądarki
![chrome_enabled_developer_mode](https://github.com/tomsyty/Additional-informations-on-UPS-label/assets/41838854/53feae80-f9b6-4ec5-a947-16cf6392b99b)
3. Kliknij przycisk "Załaduj rozpakowane"<br/>
![chrome_extensions_load_unpacked_button](https://github.com/tomsyty/Additional-informations-on-UPS-label/assets/41838854/aecdb58b-b002-4da1-b770-2c1ad10a0dd2)
4. Wybierz folder z uprzednio pobranym i rozpakowanym rozszerzeniem.
5. Z menu przeglądarki wybierz "Ustawienia - Pobrane pliki" i zapamiętaj lub zaznacz i skopiuj lokalizację. Zrób to w tym miejscu ponieważ nazwa folderu wyświetlana w oknie "Mój komputer" nie musi być taka sama jak rzeczywista nazwa folderu na dysku, np. folder może wyświetlać się jako "Pobrane", ale jego rzeczywista nazwa to "Downloads"<br/>
![chrome_settings_download_path](https://github.com/tomsyty/Additional-informations-on-UPS-label/assets/41838854/e3fde1f9-1110-4dd8-8eaa-db3d58184afa)
6. Aby rozszerzenie mogło widzieć pliki pobranych etykiet wymagane jest utworzenie tzw. dowiązania symbolicznego (to coś podobnego do skrótu). W tym celu otwórz wiersz polecenia (wciśnij klawisze <kbd>Win</kbd> + <kbd>R</kbd> wpisz <code>cmd</code>, kliknij OK lub wciśnij Enter albo kliknij Menu Start, wpisz <code>cmd</code> lub <code>wiersz polecenia</code>, kliknij uruchom lub wciśnij Enter). Następnie wpisz (zachowując znaki cudzysłowiu):<br/><br/>
<samp>mklink /D "ścieżka folderu rozszerzenia\downloads" "lokalizacja pobieranych plików"</samp><br/><br/>
![cmd_create_symlink](https://github.com/tomsyty/Additional-informations-on-UPS-label/assets/41838854/b645a9d1-e7f6-49a5-8b6c-63d923d1d269)
7. System potwierdzi utworzenie dowiązania symbolicznego<br/>
![cmd_create_symlink_result](https://github.com/tomsyty/Additional-informations-on-UPS-label/assets/41838854/7e7eb738-3952-43e6-ba5e-8a8dac281e5f)<br/>
Gdy wejdziesz teraz do folderu "downloads" znajdującego się w folderze rozszerzenia, powinieneś zobaczyć zawartość folderu do którego przeglądarka domyślnie pobiera pliki.

To już wszystko. Etykiety które będą przetwarzane przez to rozszerzenie będą sygnalizowane przez zielony przycisk "Pobierz etykiety"<br/>
![download_label_button_highlighted](https://github.com/tomsyty/Additional-informations-on-UPS-label/assets/41838854/e2d12b86-8424-4bcc-90c0-cb5ad04983af)

Przy pierwszym pobieraniu przeglądarka zapyta jeszcze o pozwolenie na pobieranie wielu plików (jest to spowodowane tym że rozszerzenie od razu po pobraniu etykiety przerabia ją, usuwa pobraną etykietę i zapisuje gotowy plik pod tą samą nazwą). Należy kliknąć "Zezwalaj"<br/>
![multiple_downloads_prompt](https://github.com/tomsyty/Additional-informations-on-UPS-label/assets/41838854/33bfc67e-4eca-4b58-a332-7ba83bfff373)<br/>

Rozszerzenie możesz sprawdzić w serwisie testowym [Allegro Sandbox](https://developer.allegro.pl/tutorials/informacje-podstawowe-b21569boAI1#srodowisko-testowe) przy czym etykiety UPS tam generowane nie mają poprawnego wyglądu - składają się tylko z rozciągniętego na całą stronę kodu kreskowego, jednak zobaczysz nadruk zawartości pól na etykiecie w odpowiednim miejscu. 
***
Jeżeli napotkasz jakieś błędy w trakcie działania aplikacji, masz jakieś pytania, sugestie, problemy z obsługą, daj znać w sekcji "Discussions".
Jeżeli podoba Ci się moja praca i chcesz aby była dalej rozwijana, możesz wesprzeć mnie dotacją na dowolną kwotę przez PayPal (nie ma potrzeby posiadania konta PayPal): [przekaż donację](https://www.paypal.com/donate/?hosted_button_id=GVU3UC2ZY85SN&locale.x=pl_PL)

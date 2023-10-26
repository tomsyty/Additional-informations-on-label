## Dodatkowe pola na wydruku etykiety nadawanej przez WzA
To rozszerzenie pozwala na wydruk pól "Dodatkowa informacja na etykiecie" i "Numer referencyjny" na etykiecie przewoźnika UPS przy nadawaniu przesyłek Allegro One Box i Allegro One Punkt przez "Wysyłam z Allegro".

Osobiście nie mam potrzeby korzystania z tego rozwiązania gdyż generuję etykiety pojedynczo w momencie szykowania paczki, jednak zdaję sobie sprawę że niektórym może się to przydać gdyż zgłaszali takie zapotrzebowanie na forum Allegro Gadane.

Jest to rozszerzenie do przeglądarki Chrome. Wszystkie rozszerzenia testuję tylko dla systemu Windows 10 i najnowszej wersji przeglądarki.

**Instrukcja instalacji:**
1. Pobierz rozszerzenie "additional_informations_on_label.zip" z listy plików widocznej powyżej i rozpakuj je tam gdzie zamierzasz je trzymać.
2. Kliknij ikonę menu rozszerzeń w prawym górnym rogu okna przeglądarki (ikona puzzla)
![chrome_extensions_menu_icon](https://github.com/tomsyty/Additional-informations-on-label/assets/41838854/a58891a4-d575-418e-b1e6-b76479cd0f6e)
lub z menu przeglądarki wybierz "Rozszerzenia - Zarządzaj rozszerzeniami".
3. Włącz "Tryb dewelopera" w prawym górnym rogu okna przeglądarki
![chrome_enabled_developer_mode](https://github.com/tomsyty/Additional-informations-on-label/assets/41838854/78f794c8-b63e-4c8c-9cb9-aee92bec7549)

4. Kliknij przycisk "Załaduj rozpakowane"<br/>
![chrome_extensions_load_unpacked_button](https://github.com/tomsyty/Additional-informations-on-label/assets/41838854/0360c155-0084-4d81-8da9-bbc1e2be038e)

5. Wybierz folder z uprzednio pobranym i rozpakowanym rozszerzeniem.
6. Z menu przeglądarki wybierz "Ustawienia - Pobrane pliki" i zapamiętaj lub zaznacz i skopiuj lokalizację. Zrób to w tym miejscu ponieważ nazwa folderu wyświetlana w oknie "Mój komputer" nie musi być taka sama jak rzeczywista nazwa folderu na dysku, np. folder może wyświetlać się jako "Pobrane", ale jego rzeczywista nazwa to "Downloads"<br/>
![chrome_settings_download_path](https://github.com/tomsyty/Additional-informations-on-label/assets/41838854/4053bbc3-6fba-4531-9130-830572f1f958)

7. Aby rozszerzenie mogło widzieć pliki pobranych etykiet wymagane jest utworzenie tzw. dowiązania symbolicznego (to coś podobnego do skrótu). W tym celu otwórz wiersz polecenia (wciśnij klawisze <kbd>Win</kbd> + <kbd>R</kbd> wpisz <code>cmd</code>, kliknij OK lub wciśnij Enter albo kliknij Menu Start, wpisz <code>cmd</code> lub <code>wiersz polecenia</code>, kliknij uruchom lub wciśnij Enter). Następnie wpisz (zachowując znaki cudzysłowiu):<br/><br/>
<samp>mklink /D "ścieżka folderu rozszerzenia\downloads" "lokalizacja pobieranych plików"</samp><br/><br/>
![cmd_create_symlink](https://github.com/tomsyty/Additional-informations-on-label/assets/41838854/df159708-86ac-444e-8517-2a30f577f357)<br/>

8. System potwierdzi utworzenie dowiązania symbolicznego<br/>
![cmd_create_symlink_result](https://github.com/tomsyty/Additional-informations-on-label/assets/41838854/a5c5f136-3cc9-4d26-891e-a088d203c917)<br/>
Gdy wejdziesz teraz do folderu "downloads" znajdującego się w folderze rozszerzenia, powinieneś zobaczyć zawartość folderu do którego przeglądarka domyślnie pobiera pliki.

To już wszystko. Etykiety które będą przetwarzane przez to rozszerzenie będą sygnalizowane przez zielony przycisk "Pobierz etykiety"<br/>
![download_label_button_highlighted](https://github.com/tomsyty/Additional-informations-on-label/assets/41838854/a5b020d2-8b20-40f1-8439-e7ca965f698c)

Etykiety są przetwarzane tylko w momencie pobierania na stronie od razu po zamówieniu przesyłki. Ponownie pobierane etykiety np. ze strony Sprzedaż - Obsługa zamówień - Zamówione przesyłki nie są przetwarzane.

Przy pierwszym pobieraniu przeglądarka zapyta jeszcze o pozwolenie na pobieranie wielu plików (jest to spowodowane tym że rozszerzenie od razu po pobraniu etykiety przerabia ją, usuwa pobraną etykietę i zapisuje gotowy plik pod tą samą nazwą). Należy kliknąć "Zezwalaj"<br/>
![multiple_downloads_prompt](https://github.com/tomsyty/Additional-informations-on-label/assets/41838854/9bdde32c-b37e-42d4-8701-f2e139f9baaa)<br/>

Rozszerzenie możesz sprawdzić w serwisie testowym [Allegro Sandbox](https://developer.allegro.pl/tutorials/informacje-podstawowe-b21569boAI1#srodowisko-testowe) przy czym etykiety UPS Allegro One Box i Allegro One Punkt tam generowane nie mają poprawnego wyglądu - składają się tylko z rozciągniętego na całą stronę kodu kreskowego, jednak zobaczysz nadruk zawartości pól na etykiecie w odpowiednim miejscu. 
***
Jeżeli napotkasz jakieś błędy w trakcie działania aplikacji, masz jakieś pytania, sugestie, problemy z obsługą, daj znać w sekcji "Discussions".
Jeżeli podoba Ci się moja praca i chcesz aby była dalej rozwijana, możesz wesprzeć mnie dotacją na dowolną kwotę przez PayPal (nie ma potrzeby posiadania konta PayPal): [przekaż donację](https://www.paypal.com/donate/?hosted_button_id=GVU3UC2ZY85SN&locale.x=pl_PL)

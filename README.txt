//Autorzy : Jan Mełech, Jacek Kurek, Mateusz Kaczmarek
Tytuł : System rezerwacji biletów kolejowych

W pliku create.sql znajdują się wszystkie potrzebne creat'y oraz insert'y.

Tabele : 

Ticket - tabela przechowująca dane o zamówionych biletach.

User - tabela przechowująca dane o  zarejestrowanych użytkownikach.

Seat - tabela przechowująca informacje o siedzeniu.

Trains - tabela przechowująca dane o pociągach.

Cars - tabela przechowujaca dane o wagonach.

Line - tabla przechowujaca podstawowe dane o linii.

Trip - tabela z trasami lini o danych id.

Trip_interval - tabela z przedziałami czasu na jakich funkcjonuje dana linia i z jaką częstotliwością wyrusza pociąg.

Station - tabela z id i nazwą stacji.

Platforms - tabela z opisem peronów dla danej stacji.

Carrier - tabela z informacjami o przewoźnikach.

Discounts - tabela z informacjami o zniżkach.


Funkcje: 

find_line - zwraca numer lini dla zadanej daty oraz początkowej i końcowej stacji (+- 3h).

timetable - zwraca tabelę (id lini, id pociągu, godzina wyjazdu, godzina przyjazdu) dla zdanej daty oraz początkowej i końcowej stacji.

which_car - oblicza nr wagonu na podstawie nr siedzenia.

basic_price - oblicza podstawową cenę.

calculate_price - oblicza cenę końcową uwzględniając zniżki.

tracks_on_station - zwraca liczbe torów na stacji.

first_free_track - zwraca dla danej godziny i stacji pierwszy wolny tor.


Triggery:

check_all - sprawdza podstawową zgodność zamawianego biletu.

fill - wypełnia brakujące dane podczas dodawania krotki do tabeli ticket.

after_delete_station - zapewnia spójność bazy podczas usuwania danych z tabeli station.

after_delete_trip - zapewnia spójność podczas usuwania danych z tabeli trip.

after_delete_trip - aktualizuje ceny biletów po usunięciu danej zniżki.

before_insert_trip - sprawdza poprawność wpisywanych danych do tabeli Trip.

give_track - podczas dodawania do tabeli Trip przyznaje nowej krotce wolny tor.


Widoki:

ticketView - zawiera podstawowe informacje zawarte na bilecie.


Aplikacja :
 
Nadal brak.


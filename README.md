<p align="center">
      <img src="https://i.ibb.co/3fT9dJ7/translate-icon-black.jpg" alt="Project Logo" width="246">
</p>

<p align="center">
   <img src="https://img.shields.io/badge/Engine-VS%20Community%202022-8B00FF" alt="Engine">
   <img src="https://img.shields.io/badge/Version-17.5.4-0000ff" alt="Visual Studio Version">
</p>

## About

Projekt umożliwia tłumaczenie słów między językami polskim a angielskim. Aplikacja korzysta z bazy danych do przechowywania i pobierania informacji o słowach. Interfejs użytkownika umożliwia wprowadzanie słów do tłumaczenia, a także wyszukiwanie słów na podstawie ich części.

Aplikacja obsługuje podłączenie do bazy danych za pomocą frameworka ADO.NET i korzysta z technologii WPF do budowy interfejsu graficznego. Działa na zasadzie wprowadzania słowa w jednym języku, a następnie wyświetlenia jego tłumaczenia w drugim języku wraz z dodatkowymi informacjami, takimi jak opis, forma gramatyczna, podobne słowa, przykładowe zdania i część mowy.

Dodatkowo, aplikacja umożliwia wyszukiwanie słów na podstawie wprowadzonej części słowa oraz prezentuje informacje szczegółowe o wybranym słowie.

Wykorzystana Microsoft SQL Server do zarządzania bazą danych.

## Documentation

### Attributes
- **-** **`tmp (int)`** - Przechowuje tymczasową wartość służącą do zamiany miejscami wybranych języków (PL <-> EN ).
- **-** **`query (string)`** - Zapytanie do bazy danych, wykorzystywana do pobierania informacji.
- **-** **`firstWord (string[])`** - Przechowująca informacje o wprowadzonym przez użytkownika słowie z bazy danych, zawierająca 8 elementów odpowiadających kolumnom w bazie danych.
- **-** **`secondWord (string[])`** - Przechowująca informacje o przetłumaczonym słowie z bazy danych, zawierająca 8 elementów.
- **-** **`findPathOfWord (string[])`** - Przechowywuje informacji o słowie, które jest wyszukiwane na podstawie wprowadzonej części słowa,  zawierająca 8 elementów.

### Methods
- **-** **`ClearTextBox() (void)`** - Czyszczenie wszystkich pól tekstowych w interfejsie użytkownika.
- **-** **`PullDataFromDatabase() (string[])`** - Pobierająca danych z bazy danych na podstawie zadanego zapytania SQL i zwracająca je w postaci tablicy stringów.
- **-** **`FindSecondWord() (string[])`** - Wyszukiwanie tłumaczenie słowa na podstawie pierwszego słowa, uwzględniająca wybrany język tłumaczenia.
- **-** **`OutputValueToScreen() (void)`** - Wyświetlanie informacji o słowie w interfejsie użytkownika na podstawie danych pobranych z bazy danych.
- **-** **`OutputValueToScreenSecond() (void)`** - Wyświetlanie informacji o ptzetłumaczonym słowie w interfejsie użytkownika.
- **-** **`FindCount() (int)`** - Zwraca liczbę wyników zapytania do bazy danych.
- **-** **`ShowInfoAboutSelectedWord() (void)`** - Wyświetlanie informacje o wybranym słowie po jego zaznaczeniu w ListBox'ie w osobnym TabControl.

### EVENTS
- **-** **`SwitchLanguage_Click() (void)`** - Obsługuje zdarzenie kliknięcia przycisku do zmiany języków, zamieniająca miejscami wybrane języki i czyścąca pola tekstowe.
- **-** **`Translation_Click() (void)`** - Obsługuje zdarzenie kliknięcia przycisku do tłumaczenia słowa, pobierająca informacje z bazy danych i wyświetlająca je w interfejsie użytkownika.
- **-** **`partWordSearchBut_Click() (void)`** - Obsługuje zdarzenie kliknięcia przycisku wyszukiwania słów na podstawie wprowadzonej części słowa.
- **-** **`Click() (void)`** - Obsługuje zdarzenie kliknięcia myszą pustego miejsca w oknie aplikacji, czyścąca pole tekstowe.

## Developers

- Darya Sharkel (https://github.com/SharkelDarya)

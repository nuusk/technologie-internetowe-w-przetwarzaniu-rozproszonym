# Technologie internetowe w przetwarzaniu rozproszonym

* [Project board](https://github.com/pietersweter/technologie-internetowe-w-przetwarzaniu-rozproszonym/projects/1?add_cards_query=is%3Aopen)
* [Classes board](https://github.com/pietersweter/technologie-internetowe-w-przetwarzaniu-rozproszonym/projects/2)

## REST

|                | GET             | POST           | PUT              | DELETE           | PATCH            |
|----------------|-----------------|----------------|------------------|------------------|------------------|
| /books         |  lista książek  | nowa książka   | X                | X                | X                |
| /books/{bId}   | informacje o ks | X              | edycja           | usunięcie ks     | aktualizacja ks  |
| /readers       | lista           | rejestracja    | X                | X                |                  |
| /readers/{rId} | informacje      | X              | aktualizacja     | zamknięcie konta |                  |
| /book/{bId}/items |              | nowy egzemplarz|                  |                  |                  |
| /book/{bId}/items/{iId} |        | nowy egzemplarz|                  |                  |                  |
| / books/{bId}/{iId} |            |                |                  |                  |                  |
| /checkouts     | lista           | wypożyczenie   | X                | X                |                  |
| /checkouts/{cId} |               |                | przedłużenie     | zwrot            |                  |
| /archive_checkouts/{cId} |       |                |                  |                  |                  |
| /readers/{rId}/checkouts/{cId} |        |         | przedłużenie     | zwrot            |                  |



## Przykładowe żądania
| url | definicja |
| --- | --------- |
| /books&title=sop&author=poe |  |
| /books/history | zawężenie listy książek do kategorii "History" |
| /books/history/europe/poland | zawężenie listy książek do kategorii "History" z podkategorią "Europe" i podkategorią "Poland" |
| /transfers/{tId} | Z racji, że przelew wymaga pobrania i aktualizacji danych z różnych zasobów, a nie dzieje się to atomowo, można stworzyć osobny zasób reprezentujący taką transakcję |



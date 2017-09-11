# PHP Tips
## Wyświetlanie

Do wyświetlania treści używaj 

**echo** a nie **print()**

Do oznaczania stringów pojedyńcze cudzysłowy ( ' ) są szybciej procesowane przez parser niż podwójne ( " ). W nowszych wersjach parsera różnice się zacierają.

Przy wyświetlaniu przy użyciu echo łącz stringi przecinkiem zamiast kropką 
```php
echo ‘The MD5 of text is:  ‘,md5($text),'!';
```

## Include
Używaj **include()** i **require()** zamiast *include_once()* i *require_once()* jeśli to nie konieczne. Potrzeba sporo czasu na sprawdzenie czy plik został wcześniej załadowany. Scieżki do plików podawaj pełne zamiast ('./file.inc')

Używaj wbudowanych funkcji zamiast tworzć własne które posiadają taką samą funkcjonalność.

## Zmienne
Unikaj niepotrzebnego kopiowania zmiennych tylko po to żeby zmienić ich nazwę, niekóre mogą zawierać duże ilości informacji i kopie zużyją duże ilości pamięci

Używaj **isSet()** do sprawdzania zmiennych zanim zaczniesz ich używać lub sprawdzać zawartość

## Pętle
Do pętli **for** podawaj obliczony wcześniej rozmiar zmiennej/obiektu. Do liczenia lepiej użyć **count()** niż *sizeof()*
```php
$size = count($x);
for($i=0; $i<$size; $i++);
```
foreach, for, while. Najszybsza do odczytywania jest pętla **foreach**
```php
foreach($arrVar as $key => $val);
```

## Warunki
Warunki IF, SWITCH
Najszybsza opcja **if, elseif, else** z użyciem operatora === do porównania wartości
```php
if($answer === 1) {}
else if($answer === 3) {} 
else {}
```


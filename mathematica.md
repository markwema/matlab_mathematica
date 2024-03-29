# Mathematica -- Program typu CAS
## Notatki z  zajęć z profesorem W. Miklaszewskim
Środowisko do obliczeń symbolicznych oraz numerycznych.
Można go używać do:
* nauk przyrodniczych;
* matematyki;
* nauczania;
* inżynierii;
* informatyki itp;
## Mathematica – ciekawe linki:

* [wolfram](http://www.wolfram.com )-strona główna mathematica z dokumentacją;
* [video i zrzuty](http://www.wolfram.com/broadcast/screencasts/);
* [demonstracje](http://demonstrations.wolfram.com);
* [czasopismo](http://www.mathematica-journal.com);

----

# Mathematica -- organizacja

Pracujemy w dokumencie zwanym „Notatnik"
* **SHIFT+ENTER** – wykonanie obliczeń;
* **ENTER** – nowa linia;

## Podstawowe zasady

* Program rozróżnia małe i duże litery;
* Polecenia, nazwy wbudowanych funkcji i stałych zaczynają się od dużej litery – np.**Sin[x]**;
* Używaj małych liter, aby zadeklarować swoje funkcje i stałe;
* Argumenty funkcji są zamykane w nawiasach prostokątnych [];
* Nawiasy klamrowe {} są używane do grupowania elementów, oraz do oznaczania zakresów parametrów funkcji; 
* Nawiasy () są zarezerwowane do grupowania operacji;
* Nazwy wszystkich funkcji dla obliczeń numerycznych zaczynają się od litery N np. NSin[];
* Komentarze mają formę -- (* komentarz *);

## Praca -- kalkulator
* tworzenie zmienne skalrnej np. **x=3.14**
* usuwanie zmiennej **x** z przestrzeni roboczej na dwa sposoby: **x=.** lub **Clear[x]**;

### Listy

* Liczby 3, 5 ,1 stanowią trzy obiekty Listy **a={3,5,1}** {lista 3-elementowa};
* Poszczególne elementy listy możemy otrzymywać np. element drugi **a[[2]]=1**;

## Wyrażenia algebraiczne



## Funkje
Nową funkcję definiujemy jak w poniższym przykładzie
```
f[x_]=x^2-3*x+9
```
A konkretną wartość funkcji jak niżej
```
inp:f[0]
out: 9
Inp: f[1]
out: 7
```

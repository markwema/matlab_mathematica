# Wykłady Niedziela 24-03-2013..

##Obsługa Matlab'a.
--------------------------
Darmowy kompatybilny z Matlabem program to Octave. Patrz też na stronę:
[octave](http://www.opcode.eu.org/more_advanced/programing/octave/)

**Podstawowe komendy**

* **ans** - zmienna odpowiedź;
* **format compact** - wydruk jest bardziej zwarty bez wolnych lini, steruje postacią wydruku;
* **a=2+2** - tworzenie zmoiennej a lub wartości przypisanie zmiennej ;
* **whos**  - pokazuje zmienne w przestrzeni roboczej;
* **format short** - ustawia wyświetlanie wyniku na krótki format wydruku;
* **format long** - wynik przedstawiony będzie w większej precyzji;
* **help format** - wyświetla pomoc na temat komendy dla format;
* **realmax** - największa liczba reprezentowana dokładnie, to nie jest największa liczba jaka możemy osiągnać;
* **inf** - informacja o przepełnieniu, wyszliśmy poza zakres;
* **realmin** - najmniejsza wartośź reprezentowana dokładnie;
* **eps** - epsilon maszynowy --- najmniejsza liczba która dodana do jedynki daje większa liczbe od jedynki 1+E>1 (najbliszy  sąsiad  jedynki);
* **sqrt(_argument_)** - funkcja pierwiastek kwadratowy;
* **sin(pi)** - funkcja sinus, **pi** - predefinowana stała;
* **sind(30)* - funkcja sinus dla argumentów podawanych w stopniach;
* **asin()** - funkcja arcsin;
* **[1 2 3 ]** - definiowanie wectora wierszowego, zamiast spacji można sotosować przecinek. Wector wierszowy
* **[; ; ;] **- wector kolumnowy gdy odzielamy argumenty średnikiem ;
* **1:3** - też wygeneruje wector, służy bardziej do ciągów;
* **;** - gdy dajemy go na koncu obliczeń wsytrzymuje wydruk wyników;

--------
##komendy graficzne
* **plot(x,y,'opcje')** - otwiera okno do rysowania funkcji, okno graficzne, x wektor argumentów, y wektor wartości;
* **plot(x,y,'o')** - rysowanie punktów wykresu za pomoca kółek;
* **plot(x,y,'o-')** - kółka połączone linią;
* **plot(x,y,'g-o',x,y1,'r-')**  - narysuje dwie funkcje na jednym wykresie, pierwsza zielona, druga czerwona;

###Przykład rysowania funkcji sinus
>> x=-2*pi:0.1:2*pi;
  >> y=sin(x);
  >> plot(x,y,'o') 
  
-------------------------------

* **ezplot('x^2+y^2=4')** - narysuje nam okrąg o promieniu 2;
* **clear('zmienna')** - usuwa zmienną z pamięci;
* **A'** - transpozycja macierzy A;
* **.** - działania tablicowe;

----------------------------

###Przykłady
 >> x=[1 2 3 ],
  x =
     1     2     3
  >> y=[4 5 6], 
  y =
 4     5     6
  >> x.*y, 
  ans =
     4    10    18

------------------------------------

##Ciekawsze funkcje

* **factorial(10)**  - oblicza silnie 10!;
* **primes(120)** - wypisuje liczby pierwsze nie większe od 120;
* **max(x)** - największa wartość w wektorzex;
* **roots(w)** - obliczanie pierwiastków wielomianu, w wektor współczynników wielomianu;
* **,** -przecinek znak oddzielający w strukrze, kilka operacji w jednej linijce:
  >> x=2,y=3
  x =
     2
  y =
     3
* **;** - średnik umieszczany na końcu lini wstrzymuje wydruk;
* **:** -dwukropek separator w poleceniu tworzenia wektora;
* **()** - nawiasy okrągłe, zawierają indeksy elementu macierzy;
* **[]** - nawiasy kwadratowe, tworzą tablice liczb lub łańcuchów znaków;
* **xlabel('funkcja x y')** - podpisywnie osi x, gdy wstawimy y podpisze y;
* **%** - oznacza początek komentarza;
* **%{** - zawiera blok linii komentarza;
* **...** - wielokropek następna linia jest kontynuacją poprzedniej linii;
* **@** - tworzy uchwyt funkcji np @nazwa;
* **\** - ukośnik lewy macierzowy operator matematyczny oraz używany do generacji greckich liter i symbolów matematycznych w gafice
* **disp** - wyświetla wyniki;
* **clc** - usuwa wszystko z okna Command Window;
* **clear all** - usuuwa wszystkie zmienne;

-----------------------------------------------
###Rozwiązywanie numeryczne równania f(x)=0

Aby zlokalizować pierwiastek równania f(x)=0 potrzeba kilku kroków:

```
 Czy funkcja w danym przedziale zmienia znak: f(a)*f(b)<0 ?
```

#### Metody lokalizacji pierwiastka


1. bisekcja

    x1=(b-a)/2 & |f(x)|<E
  
    f(a)*f(xi)>0
    
    f(xi)*f(b)<0
    
    a=x2
    
2. metoda iteracji prostej

``` 
    f(x)=0
    x=g(x)
    xn+1=y(xn)
    x2=xp
```
 
    
d) Metoda siecznych
regula falsi 
  
    patrzymy w kórym przedziale jest pierwiastek i puszczam sieczna
  
e) Metoda Newtona-Raphsona - metoda stycznych
  
    f(x+h)=f(x)+1/1!hf'(x)+1/2!hf''(x)...
    
    f(x+x1-x)=f(x)+hf'(x)=0
    
    0=f(x+x1-x)=f(x)+hf'(x) --> x2=x-(f(x)/f'(x))
    
    
  
## Pętle w Matlab'ie
  
  Petla **FOR**: 
  
    for s=0.0:0.01:1.0
        disp(s)
    end

## Instrukcje warunkowe

  Warunek IF:
c=5
    
    if r == c
      disp('sylwek');
      else
         disp('zonk');
      end


# Zajęcia 14.04.2013 mała powtórka

### Zmienne zapisywane w systemie podwójnej precyzji:

* **realmax**
* **realmin**
* **eps**- 1+**eps**>1

Skalarne a=1

Wektory 
        x=[1 2 3]
        y=[1;2;3]
Macierze 
        [1,2;2,3]
        daje wynik: 
        1   2
        2   3


Polecenia:

        **who** wyświetla informcje o zmiennych
        **whos**
        **clear all** - usuwa zmienne z przestrzeni roboczj
### Obliczenia numeryczne (można czasami używać symboliczne)

      okna:
        komendy
        grafika
        edytor dzielimy na skrypt i funkcje

Skrypty:
        Możemy tworzyć petle for, if, while
        Obliczać sumowania

Operacje:
      Algebra liniowa
        dodawnia +
        odejmowania -
        mnożenia *
      Tablicowe(kropkowe)
        element * element
        
Te operacje można realizować przez pętle.

# Ćwiczenia

### Cwiczenie 2
#### Operacje na liczbach 0blicz:
 x=(-log(2.4)+sqrt(sin(4)-4*exp(3.4)))/(2*pi)

      x=sqrt(4*exp(12.4))/(2*tan(pi*0.47))
      
***
### Sprawdzanie numeryczne tożsamości trygonometrycznej dla kilku wartości kątów alfa i beta np. pi/2, 0.366pi itp.;

       w=[]
    for b=0:0.1:1
       disp(b);

      c= cos(b).^2+sin(b).^2-1;
      w=[w,c]
    end
    w
***
### Zadanie z cos(\alpha)+cos(\beta)

    alfa=pi/2
    beta=0.366*pi
    z=(cos(alfa)+cos(beta))-(2*cos(0.5*(alfa+beta)))*(cos(0.5*(alfa-beta)))
    
***

### Generowanie wektorów, przetestuj wyrażenia:

    a=[1 2 3];
    b=[1,2,3];
    c=[1;2;3];
y=b'
    c==y
    c(1)=5
    b(2)=6
    clc
    
### Przykład b)
    
    c==y
    d=[-1.3*sin(sqrt(5))*(log(6)-5)]
    e=[1:10]
    e=[1:.1:10]

***
### Zadanie - Dostep do elementów wektorów i macierzy

### Przyklad a)

    a=[1:5] % a=[1,2,3,4,5]
    a(1),a(2) %a(1)=1, a(2)=2;
    a(10) %błąd, wektor ma tylko 5 elementów;
    a(10)=123%co się stanie, przecież a ma rozmiar 5 
    % zostaje utworzony wektor z a , gdzie elemeny a(6:9)=0 i a(10)=123
   
### Przyklad b)

    b=[2:2:20]
    b/2
    2\b
    c=[1:10]
b/c
    b./c
    
### Zadanie - Interpolacja
 _metoda numeryczna polegająca na wyznaczaniu w danym przedziale tzw. funkcji interpolacyjnej, 
 która przyjmuje w nim z góry zadane wartości w ustalonych punktach, nazywanych węzłami_
    
    x=[1,2,3]
    y=[3.20,3.29,3.32]
        
    p=polyfit(x,y,2)
    x1=1:0.1:3;
    y1=polyval(p,x1)
    plot(x,y,'o',x1,y1,'--')
    
### Aproksymacja 
_Aproksymacja – proces określania rozwiązań przybliżonych na podstawie rozwiązań znanych, 
które są bliskie rozwiązaniom dokładnym w ściśle sprecyzowanym sensie. Zazwyczaj aproksymuje się byty (np. funkcje)
skomplikowane bytami prostszymi. Często stosowana w przypadku szukania rozwiązań dla danych uzyskanych metodami 
empirycznymi, które mogą być obarczone błędami_

    x=[1,2,3]
    y=[3.20,3.29,3.32]
        
    p=polyfit(x,y,2)
    p1=polyfit(x,y,1)
    x1=1:0.1:3;
    y1=polyval(p,x1)
    y2=polyval(p1,x1)
    plot(x,y,'o',x1,y1,'--',x1,y2)


## Macierze

      A=[1 2 3;4 5 6;7 8 9]
      B=A'
A(2,3)
      C=[1:10;11:20;21:30;31:40]
      C(1:2,1:4)
      C(2:3,1:1)
      C(1:1,5:8)
      D=[C,[1;2;3;4]]
      Z=zeros(2,4)
      
      
      x=rand(4,4)
      F=5*ones(3,3)
      F=F*2
      F=F/5
      G=4*ones(3,3)
      G/F
      G./F
      G*F
      G.*F
      
### Operacje macierzowe

    z=rand(4,4)
    det(z)
    sum(z)
    min(z)
    max(z)
    x=inv(z)
    x*z
    diag(z)
    rank(z)
### Układ równan liniowych

    a=[1 -4 3 5;3 1 -2 7;2 1 1 8;-1 -2 -5 -2];
    b=[-7;14;5;4];
    [x]=[a]\[b]
  
### Liczby zespolone

    a=4+3i
    b=5+2i
    a+b;a-b;a*b;a/b;
    real(a)
    imag(b)
    conj(a)
    abs(a)
    angle(a)
    c=5*(cos(0.6435)+i*sin(0.6435))
    d=5*exp(i*0.6435)
    
#Wykresy

### Dwuwymiarowy wykres

    x=-10:.005:40;
    y=[1.5*cos(x)+4*exp(-.01*x).*cos(x)+exp(.07*x).*sin(3*x)];
    plot(x,y)
    
### Wykres3D
 [x,y]=meshgrid(-3:.12:3);
    z=sin(x).*exp(y)+x.*y;
    mesh(x,y,z);
    
#Funkje

### Otwieranie funkcji z zapisanej w skrypcie w WindowCommand

    function[val]=kwadratowa(a,b,c,x)
    
    val=a*x.^2+b*x+c;
    end
    
Funkcje wywołujemy poleceniem>> kwadratowa(1,1,1[1 2 3])

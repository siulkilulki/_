## Wyrażenia regularne w języku Python

#### Definicja
___
**_E_** - alfabet
+ Pusty wyraz (**_e_** epsilon) jest wyrażeniem regularnym.
+ Jeśli **_a_** i **_b_** są wyrażeniami to:
 + **_a*_** (_domknięcie Kleenego_)
 + **_ab_** (_konkatenacja_)
 + **_a | b_** (_alternatywa_)
są wyrażeniami regularnymi.

+ Nic poza tym nie jest wyrażeniem regularnym.

> Bonus:
**_a+_** == **_aa*_**
>

Nieformalnie wyrażenia regularne opisują wzorce używane w wyszukiwaniu
i podmienianiu _stringów_ w tekście.

#### Składnia wyrażen regularnych
___
**w praktyce** | **w teorii** | **komentarz**
:---: | :---: | :---
**_""_** | _e_ (_epsilon_) | pusty znak
<text>&#124;</text>| + | alternatywa
[0-2a-c@] | 0+1+2+a+b+c+@  |  zakres znaków
. | a+b+...+z+A+B+...+Z | dowolny znak z alfabetu
* | * | 0 lub więcej wystąpień
a? | a + _e_ | wyrażenie _a_ występuje 0 lub 1 raz
a+ | aa* | wyrażenie _a_ występuje 1 lub więcej razy
^ | brak | metaznak ozaczający początek łańcucha <br>Uwaga! W [^_a_] oznacza negację _a_
$ | brak | metaznak oznaczjący koniec łańcucha
a{4} | aaaa | określona liczba powtórzeń (tutaj 4)
a{4,7} | aaaa(a + a)(a + a)(a + a) | określony zakres liczby powtórzeń (tutaj od 4 do 7)

___

A co gdy chcemy szukać np **`*`**. Wtedy z pomocą przychodzi tzw. _escape charcter_. Jest to **`\`**.
**`*`** zapiszemy więc tak **\\***.

Dzięki wykorzystaniu **\** mamy do dyspozycji dodatkowe specjalne znaki.
Oto one:

**znak** | **interpretacja**
:---: | :---:
\d | [0-9]
\w | [a-zA-Z0-9_]
\t | tab
\r | koniec linii
\n | nowa linia
\s | [\t\r\n]
\D | [^\d]
\W | [^\w]
\S | [^\s]

#### Python
___

##### Ogólnie
W pythonie aby skorzystać z potęgi wyrażeń regularnych wystaczy zaimportować moduł '**re**'.
Dokładny opis składni, dostępnych metod znajduje się w dokumentacji i jest to najlepsze źródło
informacji do którego powinno się spojrzeć w pierwszej kolejności jeśli czegoś szukamy.

Podstawowe funkcje na które trzeba zwrócić uwagę to: **compile**, **search**, **group**, **findall** i **match**.

##### Asercje lookahead i lookbehind
Nazywane są również razem jako _lookaround_

+ **Negative lookahead ?!** - ogląda jedną grupę naprzód w celu "negatywnego" potwierdzenia.
Np. Jeśli chcemy znaleźć _a_ po którym nie następuje _b_ to napiszemy: **a(?!b)**
+ **Positive lookahead ?=** - ogląda jedną grupę naprzód w celu "pozytywnego potwierdzenia"
Np. Jeśli chcemy znaleźć _a_ po którym nie następuje _b_ to napiszemy: **a(?=b)**
+ **Negative lookbehind ?<!** -  ogląda jedną grupę wstecz w celu "negatywnego" potwierdzenia.
Np. Jeśli chcemy znaleźć _a_ przed którym nie ma _b_ to napiszemy **a(?<!b)**
+ **Postiive lookbehind ?<= ** - ogląda jedną grupę wstecz w celu "pozytywnego" potwierdzenia.
Np. Jeśli chcemy znaleźć _a_ przed którym jest _b_ to napiszemy **a(?<=b)**

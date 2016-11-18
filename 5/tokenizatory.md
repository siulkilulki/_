# Tokenizatory on-line

## Rozpatrywane tokenizatory:
+ MorphAdorner V2.0
+ Xerox Tokenizator
+ TextBlob
+ TreeBankWordTokenizer
+ WordPunctTokenizer
+ PunktWordTokenizer
+ WhitespaceTokenizer
+ pattern tokenizer

Przy testach pojedyńcze tokeny będą umieszczane w kwadratowych nawiasach np **[.]** ("kropka" jako jeden token)

### Problemy z "kropką":
Testowane na zadaniu _People have linked to it, and so other people in turn link to it, etc., etc._

__Idealny rezultat__:
```
[People] [have] [linked] [to] [it] [,] [and] [so] [other] [people] [in] [turn] [link] [to]
[it] [,] [etc.] [,] [etc.] [.]
```
__Dopuszczalny rezultat:__
```
[People] [have] [linked] [to] [it] [,] [and] [so] [other] [people] [in] [turn] [link] [to]
[it] [,] [etc.] [,] [etc] [.]
```
__Wyniki__

| Tokenizator | Wynik | Komentarz |
| :---: | :---: | :---  |
|MorphAdorner V2.0| błędny | Nie uznał kropki kończącej zdanie jako oddzielnego tokena|
|Xerox tokenizer| błędny| Nie uznał kropki kończącej zdanie jako oddzielnego tokena|
|TreeBankWordTokenizer|dopuszczalny rezultat |. |
|WordPunctTokenizer| dopuszczalny rezultat  |. |
|PunktWordTokenizer|błędny | Nie uznał kropki kończącej zdanie jako oddzielnego tokena|
|WhitespaceTokenizer|błędny | Nie uznał kropki kończącej zdanie jako oddzielnego tokena||
|pattern tokenizer|dopuszczalny rezultat |. |

### Problemy ze "spacją"
Testowane na zadaniu _Los Angeles and Salt Lake City are cities._

__Idealny rezultat__:
```
[Los Angeles] [and] [Salt Lake City] [are] [cities] [.]
```

__Wyniki__

Żaden z tokenizatorów nie traktuje nazw własnych, w tym przypadku miast jako tokenów tylko dzieli je na odrębne tokeny. Szkoda.

### Problemy z "myślnikiem" i "łącznikiem"
Testowane na zadaniu _Lower-case letters incompre-
hensibilities ._

__Idealny rezultat__:
```
[Lower-case] [letters] [incomprehensibilities] [.]
```
__Wyniki__

Żaden z tokenizerów nie uznał _incomprehensibilities_ jako jednego tokena.
Za to wszystkie prócz WordPunctTokenizer'a dały sobie radę z zaklasyfikowaniem *Lower-case* jako jednego tokena.

### Problemy ze specjalnymi tokenami(w tym emotikony, c++ itd.):
Testowane na zadaniu _C++ is great programming language_

__Idealny rezultat__:
```
[C++] [is] [great] [programming] [language]
```
__Wyniki__

| Tokenizator | Wynik | Komentarz |
| :---: | :---: | :---  |
|MorphAdorner V2.0| idealny |. |
|Xerox tokenizer|idealny |. |
|TreeBankWordTokenizer| idealny|. |
|WordPunctTokenizer|błędny | rozbił _C++_ na dwa tokeny _C_ i _++_ |
|PunktWordTokenizer|idealny |. |
|WhitespaceTokenizer|idealny |. |
|pattern tokenizer|błędny | rozbił _C++_ na trzy tokeny _C_ i + i + |


## Podusmowanie
Co tokenizator to inne podejście. Z pewnością jednak, ciężko powiedzieć który jest najlepszy.
Na pewno żaden nie jest jeszcze idealny.

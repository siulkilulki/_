# Sentence-spittery online

## Testowane sentence spittery:
+ MorphAdorner V2.0
+ TextBlob
+ Pattern
+ spaCy
+ NLTK

### Pierwszy test

**Testowane na:** _The U.S. department, and e.g. Mr. Hockey were nice, lovely etc., etc._

Oczekiwany wynik to __jedno zdanie__.

**Wyniki:**

Tylko spaCy i Pattern poprawnie podzieliły testowy przypadek.

Pozostałe zgodnie uznały, że są dwa następujące zdania:

1. _The U.S. department, and e.g. Mr._
2. _Hockey were nice, lovely etc., etc._

### Drugi test

**Testowane na**: _No, to my mind, the Journal did not "defend sleaze, fraud, waste, embezzlement, influence-peddling and abuse of the public trust..." it defended appropriate constitutional safeguards and practical common sense._

Oczekiwany wynik to __jedno zdanie__.

**Wyniki:**
Tylko _Pattern_ nie poradził sobie z przypadkiem testowym. Podzielił na dwa następujące zdania:

1. _No , to my mind , the Journal did not " defend sleaze , fraud , waste , embezzlement , influence-peddling and abuse of the public trust ..._

2. _" it defended appropriate constitutional safeguards and practical common sense ._

Zaskakujące jest to, że reszta sentence-spitterów dała sobie radę.

### Trzeci test
**Testowane na**: _Everyone please note my blog on Donews http://blog.donews.com/pangshengdong. What I say is not necessarily right, but I am confident that if you read it carefully it should give you a start._

Oczekiwant wynik to __dwa zdania__.


**Wyniki:**

Wszystkie sentence-spittery dają sobie radę z URL.

## Podsumowanie:
Sentence-spittery dość dobrze radzą sobie z dzieleniem tesktu na zdania.
Robią co prawda błedy. Tylko spaCy przeszedł 3 testy bezbłednie.

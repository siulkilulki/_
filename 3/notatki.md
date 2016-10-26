## Notatki z wykładu nr 3

#### Podstawy teoretyczne

**Gramatyka** - sposób opisu podzbioru wszystkich słów skończonej długości nad danym __alfabetem__.
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Np **alfabet** to  {_ jeden, mały, trzy _}.

__Gramatyka formalna__ składa się z:
+ Symboli terminalnych
+ Symboli nieterminalnych
+ Symbolu statrowego
+ Reguł gramatyki

> Bonus: **Gramatyka bezkontekstowa** to taka dla której po lewej stronie stoi tylko jeden symbol nieterminalny.

__Symbol terminalny__ - jest to symbol elementarny tworzący wyrazy języka formalnego.
**Symbol nieterminalny** - jest to symbol, który można definiować.

__Przykład__:
Symbol startowy - **S**
Symbole nieterminalne - **A**, **B**
Symbole terminalne - **{** a, b  __}__

**Reguły**:
S -> aA
A -> bA
A -> b

Jest to gramatyka bezkontekstowa która umożliwia wygenerowanie słów postaci **ab**, __abb__, **abbb** itd.

#### Analiza leksykalna
__Analiza leksykalna__ jest to proces przetwarzania sekwencji znaków w sekwencję tokenów.
Analizą leksykalną zajmuje się program zwany **lekserem**.

#### Analiza składniowa
**Analiza składniowa** lub inaczej również __parsowanie__ służy sprawdzaniu czy wejście jest zgodne z regułami gramatyki.
Analizą składniową zajmuje się program zwany **parserem**.

#### Narzędzia
Popularne narzędzia do analizy składniowej to np:
+ **Lex** - dla języka C/C++.
+ **JavaCC** - dla języka Java. Obsługuje Unicode.
+ **PLY** - dla języka Python. Analiza leksykalna i parsowanie.

Popularne parsery:
+ **Yacc**- dla języka C/C++.
+ **CookCC** - dla języka Java.
+ **PLY** - wyżej wymieniony.


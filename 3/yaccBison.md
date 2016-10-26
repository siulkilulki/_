# Porównanie Lex/Yacc z ANTLR

Jedną z głównych różnic jest to że **ANTLR** generuje parser __LL(*)__, a **YACC** LALR. 
<br>W __LL(*)__ bardzo prosto pisze się parsery, ponieważ można używać notacji **EBNF**, zamiast notacji __BNF__ na której bazowany jest **YACC**.

Notacja EBNF eliminuje kilka wad BNF:
+ BNF używa symboli (<, >, |, ::=) dla siebie; gdy pojawią się one w języku który ma być definiowany, notacja BNF nie może być użyta bez modyfikacji i objaśnień.
+ Składnia BNF może reprezentować wyłącznie jedną regułę w jednej linii.

EBNF rozwiązuje te problemy:
+ Symbole terminalne są zamknięte pomiędzy znakami cudzysłowu ("..." lub '...'), a symbole w sekwencji rozdzielane przecinkami. Ostre nawiasy ("<...>") dla symboli nieterminalnych mogą zostać pominięte.
+ Każdą regułę kończy znak ograniczający – według normy średnik.

**ANTLR** generuje tzw. _recursive descent parsers_ co oznacza, logika jest zawarta w kodzie parsera.
Zaletą tego rozwiązania jest to, że łatwo jest się zorientować co robi parser tylko czytając jego kod. <br>Debuggowanie również jest dużo łatwiejsze. <br>**ANTLR** w przeciwieństwie do __YACC__ posiada również IDE o nazwie ANTLRworks które znacząco ułatwia pracę.  

Wadą jest to, że w przeciwieństwie do **YACC** kod jest większy, a program wolniejszy.

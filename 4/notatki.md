# AIML i czatboty
## Czatboty
__Czatbot__ - Program który symuluje naturalną rozmowę (dialog). Czatbot udaje, że jest człowiekiem.

Czatboty są lepsze w __mówieniu__ niż w słuchaniu. Próbują również pokierować konwersacją w kierunku konkretnego znanego dla nich **tematu**.

Czatboty są robione:
+ dla rozrywki,
+ zapewniają informacje (odpowiadają na pytania lub przekierowują na stronę internetową)

#### Angielskie czatboty
__Dawne czatboty (prekursorzy)__:
+ Eliza (1966)
+ Parry (1972)

__Nowoczesne__:
+ Kapitan Kirk
+ Cleverbot
+ Jabberwacky
+ Elbot

#### Polskie czatboty:
+ Ada - wirtualna asystentka, która pomaga znaleźć mieszkanie
+ Mateusz Transporteusz - pomaga uzyskać informacje o rozkładach jazdy ZTM
+ Ludzik Mubu - pomaga uzytkownikom poruszac sie po stronie sprzedawcy uzytecznosci komorkowych.

#### Zalety czatbotów:
+ Wejście w postaci języka naturalnego
+ Wyjście w postaci języka naturalnego
+ Dokładnie jedna odpowiedź

#### Wady czatbotów:
+ Często się mylą
+ Zazwyczaj wyspecjalizowane tylko w konkretnej dziedzinie
+ Często nie dają odpowiedzi na zadane pytanie

## AIML
+ Wynaleziony w 1995
+ Oparty na języku XML
+ Umożliwia stworzenie bota _ALICE_

Dużo interpreterów:
+ PHP AIML interpreter (Program O)
+ Python AIML interpreter (PyAIML)
+ Java AIML interpreter (Chatterbean)

#### Budowa AIML
AIML składa się z:
+ słów (tylko litery i liczby)
+ spacje
+ wildcards: * _
+ tagi

Przykład programu w AIML:

```
<aiml version="1.0.1">
<category>
  <pattern>Hej</pattern>
  <template>Witam</template>
</category>
</aiml>
```

Tutorial dla AIML: https://www.tutorialspoint.com/aiml/index.htm

#### Porównanie wyrażeń regularnych języka Javascript i języka C

##### Wstęp
Oba języki bardzo popularne, ale również bardzo się od siebie różniące.
Zainteresowało mnie jak się do siebie mają pod względem wyrażeń regularnych.
Porównuję "goły" **Javascript**, czyli bez zewnętrznych bibliotek.
Natomiast **C** z bardzo popularną i powszechnie używaną biblioteką **GLib**.

##### Części wspólne
+ kwantyfikator **+**
+ zanegowany zakres znaków
+ leniwe kwantyfikatory
+ grupy niezapamiętywane
+ lookahead
+ odniesienia wsteczne po indeksie (ang. _backreferences_)
+ możliwość odniesienia się do wyszukań po indeksie
+ tryb case-insensitive
+ oba nie wspierają tzw. _free spacing syntax_

##### C ma, Javascript nie ma
+ warunkowe wyrażenia regularne!
+ rekursja
+ lookbehind
+ niezależne podwyrażenia (ang. _atomic groups_)
+ odniesienia wsteczne po nazwie
+ komentarze (pozwalają komentować różne części wyrażenia tak aby było czytelne co robią)

##### Podsumowanie
**C** z biblioteką **GLib** ma zdecydowanie większe możliwości pod względem wyrażeń regularnych niż **Javascript**.
Oczywiście starcie nie było do końca uczciwe, bo jestem przekonany, że Javascript też ma wiele wspaniałych zewnętrznych bibliotek do wyrażeń regularnych, które być może mogą się równać lub są nawet lepsze niż **C** z **GLib**.
Nie mniej jednak możemy powiedzieć, że nawet taki język jak **C** ma duże możliwości w przetwarzaniu wyrażeń regularnych. Było to dla mnie zaskoczeniem.

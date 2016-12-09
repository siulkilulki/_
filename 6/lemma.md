# Lematyzatory online

### Rozważane lematyzatory
+ NLTK Wordnet Lemmatizer
+ MorphAdorner V2.0
+ TwinWord
+ CST Lemmatiser

Pierwsza obserwacja jest taka, że żaden z powyższych lematyzatorów nie podaje informacji morfologicznych, a jedynie podstawową formę wyrazów (**lemma**).

Będę zatem poniżej rozważał tylko i wyłącznie to jak dobrze lematyzatory zwracają _lemma_.

Lematyzatory były testowane na następującym zbiorze słów: __{better, worse, did, saving }__

Oczekiwane odpowiedzi:

+ better -> good
+ worse -> bad
+ did -> do
+ saving -> save



### NLTK Wordnet Lemmatizer

Nie dał sobie rady z lematyzacją _worse_. Zamiast _bad_ na wyjściu otrzymałem _worse_.

Poradził sobie z resztą słów.

### MorphAdorner V2.0

Poradził sobie z całym zbiorem słów.

### TwinWord

Z żadnym słowem nie dał sobie rady. Dla każdego słowa prócz _did_, na wyjściu otrzymaliśmy słowo z wejścia. _did_ nie wykrył w ogóle (komunikat "lemma not found")

### CST Lemmatizer

Ten lematyzer poradził sobie z najłatwiejszymi słowami czyli _did_ i _saving_. Niestety dla _better_ i _worse_ na wyjściu otrzymaliśmy to samo co na wejściu.

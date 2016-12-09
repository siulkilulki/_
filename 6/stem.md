# Stemmery online

### Rozważane stemmery
+ Porter
+ Lancaster
+ Snowball

Stemmery były testowane na następującym zbiorze słów: __{boy, celebrity, celebrate, celebration, cats, catlike, catty, stems, stemmer, stemming, fishing, fished, fisher, argue, argued, argues, argus, friendlies}__

Oczekiwane poprawne odpowiedzi to:
 + boy -> boy
 + {celebrity, celebrate, celebration} -> celebr
 + {cats, catlike, catty, stems, stemmer, stemming} -> stem
 + {fished, fisher} -> fish
 + {argue, argues, argus} -> argu
 + friendlies -> friend

## Wyniki

Pogrubione wyjście oznacza **błędną** odpowiedź (tylko po to by łatwo było zauważyć co dobrze, a co źle).

### Porter

|wejście|wyjście|poprawna odpowiedź|
|-------|-------|------------------|
|boy    | boy |boy |
| celebrity |boy |celebr |
| celebrate |boy |celebr |
| celebration |boy |celebr |
| cats |cat |cat |
| catlike |**catlik** |cat |
|catty |**catti** |cat |
|stems |stem | stem|
| stemmer|**stemmer** |stem |
| stemming |stem |stem |
| fishing |fish |fish|
| fished |fish |fish |
| fisher |**fisher** |fish |
| argue |argu |argu |
|argued |argu |argu |
| argues|argu |argu |
|argus |argu |argu |
| friendlies |**friendli** |friend |

### Lancaster
|wejście|wyjście|poprawna odpowiedź|
|-------|-------|------------------|
|boy    |boy |boy |
| celebrity |celebr |celebr |
| celebrate |celebr |celebr |
| celebration |celebr |celebr |
| cats |cat |cat |
| catlike |**catlik** |cat |
|catty |**catty** |cat |
|stems |stem | stem|
| stemmer|stem |stem |
| stemming |stem |stem |
| fishing |fish |fish|
| fished |fish |fish |
| fisher |fish |fish |
| argue |argu |argu |
|argued |argu |argu |
| argues|argu |argu |
|argus |**arg** |argu |
| friendlies |friend |argu |



### Snowball
|wejście|wyjście|poprawna odpowiedź|
|-------|-------|------------------|
|boy    |boy |boy |
| celebrity |celebr |celebr |
| celebrate |celebr |celebr |
| celebration |celebr |celebr |
| cats |cat |cat |
| catlike |**catlik** |cat |
|catty |**catti** |cat |
|stems |stem | stem|
| stemmer|**stemmer** |stem |
| stemming |stem |stem |
| fishing |fish |fish|
| fished |fish |fish |
| fisher |**fisher** |fish |
| argue |argu |argu |
|argued |argu |argu |
| argues|argu |argu |
|argus |**argus** |argu |
| friendlies |friend |argu |

## Podsumowanie

Najlepiej na zbiorze testowym poradził sobie Lancaster (3 błędy), a potem ex aequo Snoball i Porter (5 błędów). Jeśliby wziąć sumę wszystkich poprawne odpowiedzi tych 3 stemerów to popełniłyby one błąd tylko na podchwytliwych _catlike_ i _catti_.

Zaskakujące było, że czasem proste słowa z końcówką _er_  były źle przetworzone przez stemmery Snowball i Lancaster.

Za to dobrze przetworzone trudne słowo _friendlies_ przez stemmery Snowball i Lancaster uznaję za duży pozytyw.

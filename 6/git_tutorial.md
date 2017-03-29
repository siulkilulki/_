# Tutorial git'a

### Tworzenie
Sklonuj istniejące repozytorium

`git clone ssh://user@domain`

Tworzenie nowego repozytorium

`git init`

### Zmianny lokalne
Pokaż zmiennione pliki w katalogu roboczym

`git status`

Pokaż zmiany w śledzonych plikach

`git diff`

Dodaj wszystkie zmiany do następnego commita

`git add .`

Zacommituj zmiany:

`git commit`

Zmień ostatniego commita:

`git commit --amend`

### Histora commitów
Pokaż wszystkie commity poczynając od najnowszego:

`git log`

Zobacz kto, kiedy i co zmienił w pliku:

`git blame`

### Branche i tagi
Pokaż wszystkie istniejące branche:

`git branch -av`

Zmień HEAD brancha (przejście na inny branch):

`git checkout [branch]`

Stwórz nowy branch na bazie aktualnej HEAD (na bazie aktualnego zchekoutowanego brancha):

`git branch [new branch]`

Usuń lokalny branch:

`git branch -d [branch]`

Oznacz aktualny branch tagiem:

`git tag [tag name]`

### Update i publikowanie (push)

Wylistuj wszystkie skonfigurowane remote'y:

`git remote -v`

Dodaj nowe zdalne repozytorium:

`git remote add [shortname] [url]`

Ściągnij wszystkie zmiany z [remote], ale bez integrowania do HEAD

`git fetch [remote]`

Ściągnij zmiany i zmerguj do HEAD:

`git pull [remote] [head]`

Opublikuj zmian lokalne na remote'a:

`git push [remote] [branch]`

### Merge i Rebase
Merge [branch] do aktualnego HEAD

`git merge [branch]`

Rebase aktualny HEAD do [branch]:

`git rebase [branch]`

Rozwiąż konflikty po mergu ustawionym narzędziem do tego:

`git mergetool`

### Undo
Usuń wszytkie lokalne zmiany w katalogu roboczym:

`git reset -hard HEAD`

Usuń lokalne zmiay w konkretnym pliku:

`git checkout HEAD [file]`

Odwróc commit, poprzez zrobienie nowego z przeciwnymi zmianami:

`git revert [commit]`

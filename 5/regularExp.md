# Przydatne wyrażenia regularne

#### Dopasowanie e-maili
```
^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$
```
**Przykład dopasowania:** _dawjur@st.amu.edu.pl_
**Nie dopasuje:** _dawjur@st.wiecejnizszesc_

#### Dopasowanie URL
```
^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$
```
**Przykład dopasowania:** _http://net.fajnastrona.go.art.pl/about_
**Nie dopasuje:** _http://go.art.pl/file!.html_ bo zawiera wykrzyknik.

#### Dopasowanie adresu IP
```
^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$
```
**Przykład dopasowania:** _72.59.122.123_
**Nie dopasuje:** _192.168.1.256_ bo 256 to za duża wartość. Każdy tzw. oktet składa się z 8 bitów czyli wartości od 0 do 255.


#### Dopasowanie heksadecymalnej liczby w HTML, CSS, SVG i tym podobnych
```
^#?([a-fA-F0-9]{6})$
```
**Przykład dopasowania:** _#abcdef_
**Nie dopasuje:** _#00F99K_ bo heksadecymalne liczba nie zawiera "_K_"

#### Dodatnie i ujemne liczby rzeczywiste
```
^-?\d*\.?\d+$
```

**Przykład dopasowania:** _2134.241356_

#### Dopasowanie daty w formacie yyyy/mm/dd z różnymi separatorami
```
^(19|20)\d\d[- /.](0[1-9]|1[012])[- /.](0[1-9]|[12][0-9]|3[01])$
```

**Przykłady dopasowań:**
_1992.07.12_
_1992-07-12_
_1992/07/12_

**Nie dopasuje** dat w foramcie _dd/mm/yyyy_ i *mm/dd/yyyy*

Aby dopasować daty w formacie **dd/mm/yyyy** z różnymi sepratorami wystarczy zmienić trochę powyższe wyrażenie regularne.
Oto one po zmianie:
```
^(0[1-9]|[12][0-9]|3[01])[- /.](0[1-9]|1[012])[- /.](19|20)\d\d$
```

I analogicznie dla dat **mm/dd/yyyy** z różnymi separatorami mamy:
```
^(0[1-9]|1[012])[- /.](0[1-9]|[12][0-9]|3[01])[- /.](19|20)\d\d$
```

#### Dopasowanie czasu w formacie 12h
```
(1[012]|[1-9]):[0-5][0-9](\\s)?(?i)(am|pm)
```
__Przykład dopasowania:__ *12:12 am*

#### Dopasowanie czasu w formacie 24h
```
([01]?[0-9]|2[0-3]):[0-5][0-9]
```

**Przykład dopasowania:** _23:59_

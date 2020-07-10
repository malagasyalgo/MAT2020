[Malagasy]

__[Easy]__

Mampianatra kajy amin'ny EPP ianao.  Rehefa tonga ny fotoana hampianarana ny ankizy ny "multiplication" dia sahirantsaina ianao ny mitady ohatra mora indrindra mba hahazahoan'i mpianatra azy. Tapak'hevitra ary ianao fa andeha resaka multiplication-na "text" no ho entinao hitondrana azy. Noho izany, ny multiplication dia toa ny text iray miverimberina `n` fois. 

Raisina ohatra, `3 x "malagasy" = "malagasymalagasymalagasy"`

I Lita mpianatrao anefa izay azo atao hoe lalin-tsaina dia nanontany ny fanontaniana hoe : "possible ve ny hahafantarana fa raha manana `text1` ohatra, **esorina izay tsy ilaina** amin'ilay `text1`,  dia mety ahazo multiplicaton `k x text2` ka ny `text2` eto izany **"sous-ensemble"** an'ny `text1`?" 
Talanjona ianao nahare ilay fanontaniana ka ny hariva an'io ihany dia nanarotra programa kely hitadiavana ny "minimum" an'ny **litera afaka esorina** amin'ny `text1` mba hahazahoana ny `k * text2`.

Manorata ary programme mitady ny "minimum"-ny *litera afaka esorina amin'ny* `text1` mba hahazahoana ny "multiplication" `k * text2`.

__Input__
- `text1`: text hijerena ny minimum afaka esorina mba hahazahoana mulplication `k * text2`
- `text2`: "reference"-na *text* hamoronana an'ilay muplication.

__Output__
Minimum-ny litera ("characters") afaka esorina amin'ny `text1`, mba hahazahoana an'ily mupliplication `k * text2`.

__Exemple__
- Raha `text1 = "abyab"`,  `text2 = "ab"` dia `1` no valiny => Ny `y` izao eto no mila esorina dia mahazo mulptiplication `2 * ab`. Izany hoe minimum na caractère afaka esorina eto dia `1`.
- Raha `text1 = "ab"`,  `text2 = "malagasy"` dia `2` no valiny => Satria tsy misy `"malagasy"` mihintsy ao amin'ny `"ab"`, noho izany dia mila esorina daholo ny litera ao amin'ny `text1` mba hilazana fa `0` ilay multiplication, izany hoe `0 x "malagasy" = ""` (`0 x text2 = text1`). 

© [ramamj](https://app.codesignal.com/profile/ramamj)


[English]

__[Easy]__

You are a Maths teacher in the primary school. You struggle to find the best examples for the students to easily understand *multiplication* using numbers. So instead you decided to use **texts** in your examples. You explain that multiplication *by `n`* of a text is *that text repeated `n` times*. 

For example: `3 x "malagasy" = "malagasymalagasymalagasy"`

Lita, a (smart) student then asked : "Is it possible that given a `text1`, **we remove some (or no) characters** from `text1`, we get `text1 = k x text2` where `text1` is a **multiple of** `text2`?"

You were so amazed by such a question that you decided to write a program to find the **minimum** *number of characters* **to be removed** from `text1` to get `text1 = k * text2`.

__Input__
Given `text1` and `text2`, write the program described above.

__Output__
Minimum number of characters to be removed from `text1` to get `tet1 = k * text2`.

__Exemple__
- For `text1 = "abyab"` and  `text2 = "ab"`, the answer is `1` => We removed `y` to get the mulptiplication `2 * ab`, the minimum number of characters to remove is `1`.
- For `text1 = "ab"` and  `text2 = "malagasy"`, the answer is `2` => Because there is no `"malagasy"` in `"ab"`, it means we have to remove all the characters of `text1` to get `"" = 0 x "malagasy"` (`text1 = 0 x text2`). 

© [ramamj](https://app.codesignal.com/profile/ramamj)

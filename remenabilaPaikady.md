[Malagasy]

__[Medium]__

Voaray hiasa ao amin'ny Remenabila Service Ltd. ianao. Ny andro voalohany dia efa misy asa tokony ho vitaina maika satria tokony hanafika tanana iray ny ekipa mpikatroka. Mila manoratra programa iray ianao, programa mamantatra hoe *tafa* sa *tsy tafa* ny manafika tanàna iray raha fantatra mialoha ny endriky ny `saritany` misy ilay tanàna. Tena ilaina be io service ray io satria mba hisorohana amin'ny fotoana very ary hialana amin'ny mety hifanenana amin'ny zandarimaria.

__Input__
- `saritany`: "matrix"-na "integers" izay `0` na `1` ihany no misy ao aminy.
- `toeranaHiaingana`: "array"-na integers ny "ordonné" ("row") sy abscisse ("column") an'ny toerana hiaingan'ireo mpanafika.
- `tananaHotafihana`: "array"-na integers ny "ordonné" ("row") sy abscisse ("column") an'ilay tanàna hotafihana.

Sahala amin'izao ny endriky ny `sarintany` : 
<table>
  <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>0</td><td>0</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
</table>

Ny isa `1` eto amin'ny `saritany` dia midika hoe misy làlana azo aleha eo, ny isa `0` kosa midika hoe tsy misy làlana.

*Fanamarihana* : 
- "Guaranteed" fa làlana iray ihany no mampifandray toerana roa amin'ny "test cases" rehetra.
- *0-based* ny saritany ary manaraka `[row, column]`, any amin'ny "top-left" ny `[0, 0]`.
- Tsy afaka manafika ny tanàna amin'ny `toeranaHiaingana` ny dahalo (tsy "mangery an-tanàna").

__Output__
Raha *tafa* ny fanafihana dia avohay anatina string ny làlana tokony ho arahin'ireo mpanafika, miendrika toa izao `"<r0, c0> => <r1, c1> => ... => <rn, cn>"`. (Ny "exemple" manazava azy kokoa)
Raha *tsy tafa* dia `"TSY TAFA"` avoaka.

__Examples__
Raha 
```
saritany = 
[[1,1,1], 
 [0,0,1], 
 [1,1,1]]
```
, `toeranaHiaingana = [0, 0]` ary `tananaHotafihana = [2, 2]` dia `<0, 0> => <0, 1> => <0, 2> => <1, 2> => <2, 2>` no valiny. Hitantsika mazava eto fa misy làlana miainga avy eo amin'ny `[0, 0]` mandrapahatonga any amin'ny `[2, 2]`.

Raha 
```
saritany = 
[[1,0], 
 [0,0], 
 [1,1]]
```
, `toeranaHiaingana = [0, 0]` ary `tananaHotafihana = [2, 1]` dia `"TSY TAFA"` no valiny. Hitantsika fa tsy misy làlana avy eo amin'ny `[0, 0]` makany amin'ny `[2, 1]`.
 
 © [ramamj](https://app.codesignal.com/profile/ramamj)


[English]

__[Medium]__

You were hired by [Remenabila](https://reliefweb.int/report/madagascar/hunt-remenabila) Service Ltd. You are already given an urgent task on your first day. You have to write a program that tells if you *can* (*tafa*) or *cannot* (*tsy tafa*) attack a given village if we know its *coordinates* in a *map* (`saritany`). This program is very important because the "dahalo" wouldn't like to start a riot with the military.

__Input__
- `saritany`: the **map** which is represented by a matrix of integers `0` and `1` only.
- `toeranaHiaingana`: the **coordinates** of the bunker from which the "dahalo" will come from, stored in an array of integers `[row, col]`.
- `tananaHotafihana`: the **coordinates** of the village the "dahalo" will attack.

Below is how the *map* `sarintany` looks like: 
<table>
  <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>0</td><td>0</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
  <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
</table>

`1` means there is a path the "dahalo" can cross, `0` means the path is blocked.

*Note* : 
- It's guaranteed that there is only **one** or **no** *shortest* path that connects the start position `toeranaHiaingana` to the destination `tananaHotafihana` in each of the test cases.
- The coordinates are *0-based* and `[0, 0]` is the "top-left" corner.
- The "dahalo" **cannot attack** *their own bunker* `toeranaHiaingana`.

__Output__
If the attack is **possible**, return the *shortest path* that the "dahalo" should follow in a string like this: `"<r0, c0> => <r1, c1> => ... => <rn, cn>"`. (The examples will clarify)
If the attach is **not possible**, return `"TSY TAFA"`.

__Examples__
For 
```
saritany = 
[[1,1,1], 
 [0,0,1], 
 [1,1,1]]
```
, `toeranaHiaingana = [0, 0]` and `tananaHotafihana = [2, 2]`, the answer should be `<0, 0> => <0, 1> => <0, 2> => <1, 2> => <2, 2>`. We can see that there is a clear path between `[0, 0]` and `[2, 2]`.

For 
```
saritany = 
[[1,0], 
 [0,0], 
 [1,1]]
```
, `toeranaHiaingana = [0, 0]` and `tananaHotafihana = [2, 1]`, then the answer is `"TSY TAFA"`. There is no path between `[0, 0]` and `[2, 1]`.
 
 © [ramamj](https://app.codesignal.com/profile/ramamj)

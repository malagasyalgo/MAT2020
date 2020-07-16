[Malagasy]

__[Very Easy]__

Mpikirakira "données informatiques" ao amin'ny laboratoire manamboatra ny Covid Organics ianao. Ny "données" (`data`) izay ampiasaina dia azo avy amin'ny "analyse médical" an'ireo marary sy ny biby.
Ny asanao dia ny mi-traiter an'ireo "données medicales" ireo ho azo ampiasaina anaty solontsaina ka mba ahafahana manao ny analyse sy exploitation. 

Mila amboarina kely noho izany ireo `data` azo satria ny solonsaina ampiasaina ao dia **tsy afaka ny mi-traiter isa hafa tsy ny `0` hatramin'ny `10`**. Ka tao izao ny fitsipika hanamboaranao ireo `data` ireo:
- Raha misy na iray aza mihoatran'ny `100` (`data[i] > 100`) ao amin'ilay `data` dia atao **division par `100`** daholo izy rehetra
- Raha misy na iray aza mihoatran'ny `10` (`data[i] > 10`) fa tsy misy mihoatran'ny `100` ao amin'ilay `data` dia atao **division par `10`** daholo izy rehetra
- Raha tsy misy mihoatran'ny `100` sy `10` dia tsy kitihina ilay `data`.

*Guaranteed constraints:*
`0 <= data.length <= 100`
`1 <= data[i] <= 1000`

__Exemple__
- Raha `data = [3, 5, 8, 7, 6]` dia `[3, 5, 8, 7, 6]` no valiny => tsy misy na iray aza mihoatran'ny `10` sy `100` ao, noho izany dia tsy kitihina ilay izy.
- Raha `data = [300, 50, 8, 700, 60]` dia `[3, 0, 0, 7, 0]` no valiny => ny `300` sy `700` eto mihoatran'ny `100`, noho izany dia atao division par `100` izy rehetra.

**Fanamarihana**
- *Integer Floor Division* no ilaina atao, izany hoe `50 // 100 = 0 (int)` fa tsy `50 / 100 = 0.5 (float)`, ohatra faharoa `306 // 100 = 3` fa tsy `306 / 100 = 3.06`

© [ramamj](https://app.codesignal.com/profile/ramamj)

[English]

__[Very Easy]__

You are a data scientist at a not so well know medical laboratory. The `data` that are manipulated there are data from medical analysis of animals and sometimes humans.
You task is to transform those data into more computable ones, especially for a computer that **cannot process numbers below `0` and above `10`**. 

Below are the rules for transforming those data:
- If there is even **one** number that is **greater than `100`** int the `data` (`data[i] > 100`) then all of its members **must be divided by `100`**
- If there is even **one** number that is **greater than `10`** (`data[i] > 10`) but none is greater than `100` then all of its members **must be divided by `10`**
- If there is no number greater than `100` or `10` then the `data` are good and you don't need to transform them.

*Guaranteed constraints:*
`0 <= data.length <= 100`
`1 <= data[i] <= 1000`

__Exemple__
- For `data = [3, 5, 8, 7, 6]`, the answer is `[3, 5, 8, 7, 6]` => If there is no number greater than `10` or `100`, so we don't transform them.
- For `data = [300, 50, 8, 700, 60]`, the answer is `[3, 0, 0, 7, 0]` => `300` and `700` are greater than `100`, so we devide everything by `100`.

**Remark**
- User *Integer Floor Division*

© [ramamj](https://app.codesignal.com/profile/ramamj)

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

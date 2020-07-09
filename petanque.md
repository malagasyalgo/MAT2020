__[Hard]__

Ianao dia tena hikoaizana mihitsy amin'ny filalaovana "Boules" ([Petanque](https://en.wikipedia.org/wiki/P%C3%A9tanque)). Rehefa mitifitra (`TIR`) ianao dia vitanao "[carreau](https://www.obut.com/fr/lexique-de-la-petanque)" **foana** izany, ary rehefa mi-"pointe" (`POINTE`) ianao dia vitanao "minono (biberon)" **foana** izany.

Handray anjara amina fifaninanana iraisam-pirenena ianao sy ny namanao ka hilalao "doublette" ianareo. Manana ahiahy mafy ny tsy handresy ianao satria io namanao io tsy dia mahay loatra, fa ny tena loza dia ianao tena *tsy mahay mandray fanampaha-kevitra mihitsy*: indraindray ianao tokony hitifitra lasa mi-pointe, indraindray tokony hi-pointe lasa mitifitra.

Fantatr'io namanao io anefa fa "programmeur" henjana be ihany koa ianao, ka nanoro hevitra anao izy ny mba hanamboaranao IA mandray ny fanampahan-kevitra ho anao eo am-panaovana ilay fifaninanana, ary ianao dia manantanteraka avy hatrany izay lazain'io IA nataonao io fotsiny sisa.

**Fanamarihana 1:** 
- Ny "terrain" eto dia miendrika "plan 2D" misy "abcisse" sy "ordonnee", ary ny **"cochonet"** (kisoa kely) no eny amin'ny **(0, 0)**
- "Boules" **roa avy isan'olona** no lalaovina, izany hoe manana "boules" **efatra avy ny ekipa roa**.

__Input__
Eo ampilalaovana dia fantatra ao anatin'ny "matrix" `playedBoules` ny momban'ny boules rehetra efa nandeha. Ny "row" iray amin'io "matrix" io dia misy ny mombamombana boule iray ary miendrika toa izao izany `[t, x, y]`, ka:
- `t`: ny ekipa tompon'ilay boule, `1` raha anareo ilay boule, `2` kosa raha an'ny mpifanandrina
- `x`: coordonnee x (abcisse) an'ilay boule mihoatra amin'ny "cochonet"
- `y`: coordonnee y (ordonnee) an'ilay boule mihoatra amin'ny "cochonet"

__Output__
Ny output dia String miendrika `"<DECISIONS> => <X> pts"`, ka:
- `DECISIONS`: ny fanampaha-kevitra noraisin'ilay IA.
  - Ny "DECISION" dia `TIR` na `POINTE`
  - Raha `TIR` dia mila fantarina koa hoe boule iza no tifirina, ka ampiana ny "index"-ny "boule"-n'ny mpifanandrina ho tifirina izany (**0-based**): ohatra `"TIR - 3"` dia midika fa *tifirina ny boule eo amin'ny "index" 3 an'ny `playedBoules`*
  - "DECISION" iray na roa ihany no avoakan'ilay IA (*sarahina amin'ny `","` raha roa*): ireto avy ny karazana decision misy: `"POINTE"`, `"TIR - i"`, `"POINTE, POINTE"`, `"POINTE, TIR - i"`, `"TIR - i, POINTE"`,`"TIR - i, TIR - j"` (`i` sy `j` eto dia index-na boules hotifirina).
- `X`: Ny "total de points" ho azonao raha manatanteraka io fanampaha-kevitra io. Ny **total de points** dia isan'ny boules-ny ekipanao izay manakaiky kokoa ny "cochonet" mihoatra amin'ny boule-ny mpifanandrina akaiky indrindra ilay "cochonet", raha miendrika toizao ny "terrain" `[[1, 1, 1], [2, -5, 2], [2, 3, 3], [1, 2, 1]]` dia `2 pts` izany no an'ny ekipanao ary `0 pts` ny mpifanandrina, raha `[[2, 1, 1], [1, -5, 2], [1, 3, 3], [1, 0, 1]]` kosa dia `1 pts` sisa izany.

**Fanamarihana 2:**
- *Raha toa ka misy "DECISIONS" roa azo hisafidianana, izany hoe mitovy ny total de points azo amin'ny fanatanterahana an'ireo, dia izay mandefa `POINTE` mialoha foana safidiana. Ohatra raha misy decisions roa `"TIR - 3 => 3 pts"` sy `"POINTE => 3 pts"` dia ilay `POINTE` no tokony ho valiny.*
- *Ny `playedBoules` dia ireo boules misy eo amin'ny terrain alohan'ny hilalaovanao, izany hoe mbola tsy misy boule avy any aminao ireo fa kosa mety hisy boule avy amin'ilay namanao. Ary matoa ianao no asaina milalao dia `0 pts` ianareo izany **NA** lany ny boules-n'ny mpifanandrina*:
  - Raha mbola manana boule ny mpifanandrina dia **boule iray ihany** no alefanao ("sur" fa tsy maintsy mahazo points)
  - Raha lany ny an'ny mpifanandrina dia alefanao daholo ny **boules-nao rehetra**
- *Raha ohatra ka mbola misy boule-n'ny mpifanadrina **minono** amin'ilay "cochonet" dia tsy afaka mi-`POINTE` ianao fa tsy maintsy mi-`TIR` io boule io aloha.*

Raha mbola misy tsy mazava hatreto dia araho tsara ny exemples.

__Exemples__
- Raha `playedBoules = [[1,1,1], [2,-5,2], [2,3,3], [2,0,1], [1,2,1]]` dia `"TIR - 3 => 3 pts"` no valiny.
  *Fanazavana*
  - Ny ekipanareo no manomboka ary nandefa boule teo amin'ny `(1, 1)` ny namanao => `1 pts` ianareo izao.
  - Niezaka namaly ny mpifanandrina saingy nitontona teo amin'ny `(-5, 2)` ny boule nalefany.
  - Tsy maintsy mbola mamaly ihany izy satria mbola tsy nahazo point, ka nandefa boule fa mbola teo amin'ny `(3, 3)` ihany izany.
  - Namaly ihany izy ary nitontona teo amin'ny `(0, 1)` izany ka azony indray ilay point. => `0 pts` ianareo izao.
  - Nandefa ny boule farany any aminy ilay namanao saingy nandamoka satria dia eny amin'ny `(2, 1)` ilay izy no nijanona.
  - Anjaranao amin'izay izao. Lany ny boule-ny namanao saingy mbola manana boule iray ny mpifanandrina => izany hoe boule **iray ihany** no tokony ho alefanao. Manana safidy ny hi-pointe na hitifitra ilay IA:
    - Raha `"POINTE"` dia mitontona eny amin'ny `(0, 0)` ilay boule-nao ary mahazo `1 pts` indray ianareo (pointe tonda dia minono foana ny anao).
    - Raha `"TIR - 3"` kosa anefa, izany hoe tifirinao ilay boule-ny mpifanandrina eo amin'ny index `3` izay nitontona teo amin'ny `(0, 1)`, dia mahazo `3 pts` ianareo (tir a carreau *"pour 3"* no hataonao)

**Hiezaho atao kisarisary ny ohatra mba hampazava azy tsara**

© [lucoram](https://app.codesignal.com/profile/lucoram)

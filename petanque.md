[Malagasy]

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


[English]

__[Hard]__

Everyone is amazed by your skills at "Boules" ([Petanque](https://en.wikipedia.org/wiki/P%C3%A9tanque)). When you do a "shoot" (`TIR`), it is **always** a "[carreau](https://www.obut.com/en/glossary-of-petanque-terms)" (literraly "tile", meaning a direct stun shot), and when you do a "throw" (`POINTE`), it is **always** a "biberon" (the boule you threw sticks to the "cochonet" (jack)).

You and your friend will participate in an internationnal tournament as a "doublette" (a team of two people). You are worried you will not win the tournament even though you are very good because your friend is not got at all, and to make things worse, *you are very bad at decision making*: it's very often that when it's better for you to do shoot, you do throw instead, or vice-versa.

Your friend knows you are a skillfull programmer as well, so he advised you to build an AI which will make the decision for you during the tournament, and you will just follow the AI's instructions.

**Remark #1:** 
- The field you are playing on is mapped as an orthogonal 2D plane with (x, y) coordinates, and the **"cochonet"** is situated at origin **(0, 0)**
- You play **two boules per person** against another team of two, meaning each team has **four boules each**.

__Input__
During the game, you are given the list of `playedBoules` in a matrix of integers. The *row* of the matrix stores the details of **one** played boule, in the following format `[t, x, y]`, where:
- `t`: the team who owns this boule, `1` if it's *your* team's boule, `2` if it's the *opponent's*
- `x`: x coordinate of the boule compared to the "cochonet" (origin)
- `y`: y coordinate of the boule compared to the "cochonet" (origin)

__Output__
The output is a string of the format `"<DECISIONS> => <X> pts"`, where:
- `DECISIONS`: the decision that the AI made.
  - A "DECISION" is either `TIR` or `POINTE`
  - If `TIR` then we need to know which boule to shoot, so we concatenate the *index* of the *opponent's boule* that we will shoot (**0-based**): example `"TIR - 3"` means we sill shoot *the boule at index 3* of `playedBoules`
  - The AI will make **one or two** DECISION(S) only (*separate the decisions with `","` if two*). Following are all the possible combinations of decisions: `"POINTE"`, `"TIR - i"`, `"POINTE, POINTE"`, `"POINTE, TIR - i"`, `"TIR - i, POINTE"`,`"TIR - i, TIR - j"` (`i` and `j` indexes of boules which will be shot).
- `X`: the *total points* that your team will get after executing the decision(s). The **total points** is equal to the number of *your team's* boules that are closer to the "cochonet" *than your opponent's best boule* (the one that is closest to the "cochonet" for the opponent's team). If the field is like the following: `[[1, 1, 1], [2, -5, 2], [2, 3, 3], [1, 2, 1]]` then your team gets `2 pts` and `0 pts` for your opponents, if `[[2, 1, 1], [1, -5, 2], [1, 3, 3], [1, 0, 1]]` then you get only `1 pts`.

**Remark #2:**
- *If there are two "DECISIONS" that you can choose from, meaning the total points got from executing either one is the same, then choose the one with `POINTE` as first decision. For example, if there are two decisions `"TIR - 3 => 3 pts"` and `"POINTE => 3 pts"` then choose the `POINTE` one.*
- *The `playedBoules` are the boules that are already on the field **before** you (yourself) start playing, meaning it will not contain any of your boules but might contain your teammate's boules. And when you are asked to play, it's because your team got `0 pts` so far **OR** your opponents don't have anymore boules to play*:
  - If your opponents still have boules to play, the you play **only one boule** (it's for sure that you will get points)
  - If your opponents don't have any boules left then you play your **two boules**
- *If there is still an opponent's boule that is on **"biberon"** with the "cochonet" then you cannot `POINTE`, you must `TIR` this boule first*

Watch the example carefully if there are still things unclear.

__Exemples__
- For `playedBoules = [[1,1,1], [2,-5,2], [2,3,3], [2,0,1], [1,2,1]]` then the answer is `"TIR - 3 => 3 pts"`.
  *Explanation*
  - You team open the game and you friend throws one of his boule at `(1, 1)` => `1 pts` for your team so far.
  - The opponents tried to do a better throw but failed and sent their first boule at `(-5, 2)`.
  - The tried a second time but failed again, their second boule went at `(3, 3)`.
  - They trie a third time and the third boule went at `(0, 1)`, which is better than your friend's. => `0 pts` for your team so far.
  - Your friend threw his second boule without success, it landed at `(2, 1)`.
  - It's your turn now. Your friend has no more boule, but the opponents still have one last boule => meaning you only have to play **one boule**. The AI has two decisions it can choose from:
    - If `"POINTE"` then your boule will land at `(0, 0)` and you will get `1 pts` (remember, you always make a "biberon" when throwing).
    - If `"TIR - 3"`, you shoot the opponent's boule at index `3` which landed at `(0, 1)`, you will get `3 pts` with that decicion (you make a "carreau" for 3 points*)

**Try to draw the scenes so you will have a better understanding**

© [lucoram](https://app.codesignal.com/profile/lucoram)

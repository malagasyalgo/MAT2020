[Malagasy]

__[Medium]__

Misy namanao te hianatra hilalao Fanorona ary mangataka anao hampianatra azy. Tsy dia manampotoana firy nefa ianao hampianarana azy ka aleonao manamboatra programa izay ahafahany mampiana-tena. Ny zavatra voalohany tsy maintsy ataon'ilay programanao dia ny mijery hoe "valide" ve sa tsia ny "mouvement" tian'ilay namanao atao.

Raiso ohatra ity "grille"-na Fanorona manana **halehibe `45`** ity, misy "numero" *`01`* hatramin'ny *`45`* ny "case" tsirairay:

<table>
 <tr><td>01</td><td>02</td><td>03</td><td>04</td><td>05</td><td>06</td><td>07</td><td>08</td><td>09</td></tr>
 <tr><td>10</td><td>11</td><td>12</td><td>13</td><td>14</td><td>15</td><td>16</td><td>17</td><td>18</td></tr>
 <tr><td>19</td><td>20</td><td>21</td><td>22</td><td>23</td><td>24</td><td>25</td><td>26</td><td>27</td></tr>
 <tr><td>28</td><td>29</td><td>30</td><td>31</td><td>32</td><td>33</td><td>34</td><td>35</td><td>36</td></tr>
 <tr><td>37</td><td>38</td><td>39</td><td>40</td><td>41</td><td>42</td><td>43</td><td>44</td><td>45</td></tr>
</table>

***Tsy maintsy 9 ny "largeur" an'ilay grille***

Araky ny ["Regle du jeu"](http://gasy-fanorona.sourceforge.net/docs/fanorona_rules.html) an'ny Fanorona dia:
- Misy karazany roa ny "mouvement" afaka ataon'ny vato ("pieces ou pions") arakaraky ny `positionDepart` ("case de depart") misy azy:
	- **Mouvement à 4**: mouvement **orthogonal** (vertical ou horizontal), izany hoe miakatra na midina na mankany ankavia na ankavanana (mouvement vers le haut ou bas ou gauche ou droite)
	- **Mouvement à 8**: mouvement **orthogonal** (a 4) miampy mouvement en **diagonal** (haut-gauche, haut-droite, bas-gauche et bas-droite)
- Ireo karazana mouvement ireo dia mifandimby isaky ny "case", izany hoe ny case `01` afaka hanaovana mouvement à 8, ny case `02` -> mouvement à 4, case `03` -> 8, ..., case `09` -> 8, case `10` -> 4, ..., case `45` -> 8.
- Tsy maintsy mifanakaiky ny cases anakiroa (`positionDepart` sy `positionCible`) izay hanaovana ny mouvement, izany hoe tsy afaka mandingana case.

__Input__
Raha nomena ary ny:
- `positionDepart`: numero an'ilay case misy ny vaton'ny namanao
- `positionCible`: numero an'ilay case tian'ilay namano aleha
- `tailleGrille`: halehiben'ny "grille" hilalaovany

dia jereo hoe "valide" sa tsia io "mouvement" io

*Guaranteed Constraints:*
- `1 <= positionDepart, positionCible, tailleGrille <= 450000000`
- `tailleGrille % 9 == 0`

__Output__
"array"-na integers miisa 5 miendrika `[y1, x1, y2, x2, v]` ka:
- `y1`: ordonnee na "row" an'ilay case de depart
- `x1`: abcisse na "column" -> case de depart
- `y2`: ordonnee -> case cible
- `x2`: abcisse -> case cible
- `v`: `0` -> tsy valide ilay mouvement, na `1` -> valide

* Marihina fa ny position farany ambony any amin'ny havia (top-left) no manana coordonnees (0, 0)
* Raha hita fa ivelan'ilay grille ny `positionDepart` sy/na `positionCible` dia tonga dia `[0, 0, 0, 0, 0]` avy hatrany averina. 

__Examples__
- Raha `positionDepart = 1`, `positionCible = 2` ary `tailleGrille = 45` dia `[0, 0, 0, 1, 1]` no valiny
  *Fanazavana:*
  - ny coordonnees an'ny case de depart eto dia (0, 0) : `y1 = 0` et `x1 = 0`
  - ny an'ny case cible kosa dia (0, 1) : `y2 = 0` et `x2 = 1`
  - afaka manao mouvement à 8 ny case de depart, saingy miisa 3 ihany ireo cases tena afaka alehany (case 2, 11 et 10) satria izy any amin'ny sisiny.
  - hitatsika fa afaka alehan'ny vato avy eo amin'ny case 1 ny case 2, noho izany dia valide ilay mouvement: `v = 1`
- Raha `positionDepart = 45`, `positionCible = 36` ary `tailleGrille = 27` dia `[0, 0, 0, 0, 0]` no valiny satria ivelan'ny grille no misy ireo positions roa, depart sy cible
- Raha `positionDepart = 44`, `positionCible = 36` ary `tailleGrille = 45` dia `[4, 7, 3, 8, 0]` no valiny: na dia mifanakaiky aza ireo cases roa, dia tsy afaka mandeha mankany amin'ny case 36 ny avy eo amin'ny case 44 satria tsy afaka manao mouvement en diagonal avy eo.

© [ramamj](https://app.codesignal.com/profile/ramamj)


[English]

__[Medium]__

There is a friend of yours who is interested in [Fanorona](https://en.wikipedia.org/wiki/Fanorona) and he asked you to teach him how to play it. But you are a pretty busy person, so you preferred to write program which will help your friend learn to play Fanorona by himself. The first thing your program needs to do is to check whether your friend's move is **valid** *or* **not valid**.

Below is an example of a Fanorona grid with **size of `45`**, each cell has a number *`01`* to *`45`*:

<table>
 <tr><td>01</td><td>02</td><td>03</td><td>04</td><td>05</td><td>06</td><td>07</td><td>08</td><td>09</td></tr>
 <tr><td>10</td><td>11</td><td>12</td><td>13</td><td>14</td><td>15</td><td>16</td><td>17</td><td>18</td></tr>
 <tr><td>19</td><td>20</td><td>21</td><td>22</td><td>23</td><td>24</td><td>25</td><td>26</td><td>27</td></tr>
 <tr><td>28</td><td>29</td><td>30</td><td>31</td><td>32</td><td>33</td><td>34</td><td>35</td><td>36</td></tr>
 <tr><td>37</td><td>38</td><td>39</td><td>40</td><td>41</td><td>42</td><td>43</td><td>44</td><td>45</td></tr>
</table>

***The width of the gird must by of 9 cells***

According to the [Rules of Fanorona](http://gasy-fanorona.sourceforge.net/docs/fanorona_rules.html):
- There are **two** kinds of moves each piece can do depending on the `positionDepart` (starting cell) it is on:
	- **Move by 4**: **orthogonal** move (vertical or horizontal), i.e. going up, down, to the left or to the right.
	- **Move by 8**: **orthogonal** (by 4) move + **diagonal** move (up-left, up-right, down-left and down-right).
- Those two kinds of moves **alternate** for every cell, i.e. cell `01` has a *move by 8* kind, cell `02` -> *move by 4*, cell `03` -> 8, ..., cell `09` -> 8, cell `10` -> 4, ..., cell `45` -> 8.
- Two cells (`positionDepart` and `positionCible` (destination cell)) *must be **adjacent*** in order to make a move from one to another, meaning we *cannot skip cells*.

__Input__
Given:
- `positionDepart`: number of the starting cell of your friend's piece
- `positionCible`: number of the destination cell
- `tailleGrille`: size of the grid

check whether this move is valid or not.

*Guaranteed Constraints:*
- `1 <= positionDepart, positionCible, tailleGrille <= 450000000`
- `tailleGrille % 9 == 0`

__Output__
array of integers of size 5 in the format `[y1, x1, y2, x2, v]` where:
- `y1`: **row** coordinate of the starting cell.
- `x1`: **column** coordinate of the starting cell.
- `y2`: **row** -> destination cell.
- `x2`: **column** -> destination cell.
- `v`: `0` -> the move is **not** valid, or `1` -> **valid**

* The top-left corner of the grid has the coordinates (0, 0)
* In the case where `positionDepart` or `positionCible` are outside the grid, return `[0, 0, 0, 0, 0]` as the answer. 

__Examples__
- for `positionDepart = 1`, `positionCible = 2` and `tailleGrille = 45`, the answer is `[0, 0, 0, 1, 1]`
  *Explanation:*
  - the coordinates of the starting cell is (0, 0) : `y1 = 0` and `x1 = 0`
  - the coordinates of the destination cell is (0, 1) : `y2 = 0` and `x2 = 1`
  - we can do a "move by 8" from the starting cell, but there are only 3 cells we can move to in reality (cells 2, 11 et 10) because it is at a corner of the grid.
  - we see that we can move the piece from cell 1 to cell 2, so the move is valid: `v = 1`
- For `positionDepart = 45`, `positionCible = 36` and `tailleGrille = 27`, the answer is `[0, 0, 0, 0, 0]` because the starting and destination cells are outside the grid.
- For `positionDepart = 44`, `positionCible = 36` and `tailleGrille = 45`, the answer is `[4, 7, 3, 8, 0]`: even if the two cells are close to each over, we cannot move to cell 36 from cell 44 because we cannot do a diagonal move from there.

© [ramamj](https://app.codesignal.com/profile/ramamj)

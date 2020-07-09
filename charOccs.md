__[Very Easy]__

Ny ekipanao ao amin'ny AIML Inc. dia miasa amina "project"-na "machine learning" iray izay entina mamantatra hoe tena misy dikany ve ny laha-tsoratra iray sa tsy misy. Ny anjaranao amin'ilay "project" dia ny manamboatra programa **manisa ny "letters" mitovy** ao anatin'ilay lahatsoratra.

__Input__
- `text`: lahatsoratra iray mety hisy ny "letters" rehetra ao anatin'ny "[ascii table](http://www.asciitable.com/)"

__Output__
- "array"-na "integers" miisa **26** misy ny isan'ny "letters" rehetra an'ny "alphabet" anglisy ao amin'ilay lahatsoratra: `output[0]` = isan'ny `"a"`, `output[1]` = isan'ny `"b"`, `...`, `output[25]` = isan'ny `"z"`.

**Fanamarihana**: ny isan'ny "letters" ihany no tadiavina fa tsy mijery ny ankoatr'izay ("punctuations", "symbols", "numbers", ...), ary **case insensitive** ny fanisana azy, izany hoe isaina mitovy ihany ny `a` "lowercase" sy ny `A` "uppercase".

__Examples__
- Raha `text = "this is a test test case"` dia `[2, 0, 1, 0, 3, 0, 0, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 5, 5, 0, 0, 0, 0, 0, 0]` no valiny. Hitantsika eto fa `2` ihany ny isan'ny `a` ao, `0` ny `b`, `...`, samy `5` avy ny `s` sy ny `t`.
- Raha `text = "TheRe arE UPPERCASES, punctuations!! and numb4rs"` dia  `[4, 1, 2, 1, 5, 0, 0, 1, 1, 0, 0, 0, 1, 4, 1, 3, 0, 4, 4, 3, 4, 0, 0, 0, 0, 0]` no valiny: tsy isaina ny "punctuations" (`!`, `,`) sy ny numbers (`4`) ary isaina mitovy ny "uppercase" sy "lowercase".

© [lucoram](https://app.codesignal.com/profile/lucoram)

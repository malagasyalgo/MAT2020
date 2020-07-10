[Malagasy]

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


[English]

__[Very Easy]__

Your team at AIML Inc is working on a Machine Learning project used to tell if a text has a meaning or not. Your task is to create a program that *counts the occurences* of **each letter** in the text.

__Input__
- `text`: a text that may contain every charachters in the "[ascii table](http://www.asciitable.com/)"

__Output__
- an "array" of "integers" of length **26** that store the occurences of each letter of the english alphabet : `output[0]` = occurence of `"a"`, `output[1]` = occurence of `"b"`, `...`, `output[25]` = occurence of `"z"`.

**N.B**: count the occurrences of the "letters" only, ignore all other characters ("punctuations", "symbols", "numbers", ...), and the count must be **case insensitive**, meaning "lowercase" `a` and "uppercase" `A` are the same.

__Examples__
- For `text = "this is a test test case"`, the answer should be `[2, 0, 1, 0, 3, 0, 0, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 5, 5, 0, 0, 0, 0, 0, 0]`. We can see that there are only `2` `a`s in the text, `0` `b`s, `...`, `s` and `t` are each `5`.
- For `text = "TheRe arE UPPERCASES, punctuations!! and numb4rs"`, the answer should be  `[4, 1, 2, 1, 5, 0, 0, 1, 1, 0, 0, 0, 1, 4, 1, 3, 0, 4, 4, 3, 4, 0, 0, 0, 0, 0]` : we don't count the "punctuations" (`!`, `,`) and numbers (`4`), "uppercases" and "lowercases" count the same.

© [lucoram](https://app.codesignal.com/profile/lucoram)

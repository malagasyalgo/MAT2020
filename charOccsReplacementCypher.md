[Malagasy]

__[Easy]__

Raikitra ny ady lehibe fahatelo ary voageja indray Madagasikara. Soa ihany ianao sy ny fianankavianao fa tafaafina tsara, saingy mila miresaka amin'ny any ivelany ianao momban'ny stratejia ahafahanareo mitsoaka any. Ny fifandraisana rehetra anefa voaramaso daholo, ka mila mitady hevitra mba tsy ho fantatra ny hafatra hifanaovanareo. Noho izany, namorona "methode d'encryption" vaovao ianao ampiasaina amin'izany.

Tsotra anefa sarotra vinavinaina io "methode" io, ny filaharan'ny "alphabet" no ampifamadibadihanao ary atakalonao amin'izay mifanandrify tamin'ilay filaharan'ny alphabet "original" ny "lettres" rehetra ao amin'ilay hafatra tianao ho alefa.

Raha ohatra ka `"misy hafatra tiako alefa ity"` no tianao alefa, rehefa avy nampiasa ilay methode ianao dia lasa hoe `"vczj pbgbdxb dcbqw bungb cdj"` ilay izy. Toa izao no nahatonga izany:

1 - Isaina mitovy amin'ny tao amin'ny [charOccs](https://app.codesignal.com/challenge/ZT4gu22RmaxDYcKrC) ny "letters" ao anatin'ilay hafatra, ka ireto izany isa izany: `[6, 0, 0, 0, 1, 2, 0, 1, 3, 0, 1, 1, 1, 0, 1, 0, 0, 1, 1, 3, 0, 0, 0, 0, 2, 0]` => `6` ny isan'ny `a`, `0` ny `b`, `...`, `1` ny `e`, `2` ny `f`, `...`, `2` ny `x` ary `0` ny `z`.  Marihana fa **"alphabet" Anglisy** no isaina fa tsy "abidia" Malagasy.

2 - Rehefa azo ny isan'ny letters, dia **nafamadika** ny letters manana isa **betsaka indrindra voalohany sy ny kely indrindra voalohany**, dia avy eo ny *lehibe indrindra **faharoa** sy ny kely indrindra **faharoa***, avy eo ny **fahatelo**, **fahaefatra**, etc. => Izany hoe nafamadika ny `a` (miisa 6) sy ny `b` (miisa 0), avy eo nafamadika ny `i` (miisa 3) sy ny `c` (miisa 0), avy eo ny `t` (miisa 3) sy ny `d` (miisa 0), etc. ka nahazo "alphabet" vaovao ohatr'izao: `"baitngfpcyquvewhkxzdlmorjs"`
  - *Rehefa avy nafamadika ny "Letters" anakiroa dia tsy afaka afamadika amin'ny hafa instony*
  - *Na mitovy aza ny isan'ny "Letters" roa ka tsy misy betsaka na kely anoaktr'ireo intsony dia tsy maintsy afamadika ihany ireo, izany hoe raha samy `0` ny isan'ny `l` sy `m` ohatra ka samy mbola tsy nafamadika tamina "letter" hafa ry zareo dia ampifamadihana* (**Test 4** tena mampazava azy)

3 - Farany, nosoloina nifanaraka tamin'io "alphabet" vaovao io ireo "letters" rehetra tao amin'ilay hafatra ka nahazoana ny hafatra "encrypted" hoe :`"vczj pbgbdxb dcbqw bungb cdj"`. **Raha misy "uppercase" dia mila tazomina ilay "case" na dia misolo aza ilay "letter", ary tazomina ihany koa ny "punctuation", "spaces", sns ankoatry ny "letters".**

Arak'ireo, "encrypt"-eo amin'ilay programanao ary ny hafatrao ao amin'ny `text` alohan'ny handefasana azy any ivelany.

© [lucoram](https://app.codesignal.com/profile/lucoram)



[English]

__[Easy]__

World war three has started, and your country is one of the main participants. Fortunately, you and your family made it to the bunker in time. But you need to communicate with the other safer countries to discuss strategies for you to escape there. All communications are monitored though, so you have to find a way to obfuscate the messages you sent to each other, but as an ex-software engineer, you were able to create a new encryption method for that purpose.

You method is simple but hard to crack: you create a *new alphabet* by swapping the letters of the existing one then you encrypt the original message with this new alphabet (the example will clarify).

If we want to send the message `"misy hafatra tiako alefa ity"`, after it has been encrypted, it will become `"vczj pbgbdxb dcbqw bungb cdj"`. Following is how:

1 - We count the occurrences of the letters as in [charOccs](https://app.codesignal.com/challenge/ZT4gu22RmaxDYcKrC) and we get: `[6, 0, 0, 0, 1, 2, 0, 1, 3, 0, 1, 1, 1, 0, 1, 0, 0, 1, 1, 3, 0, 0, 0, 0, 2, 0]` => `6` occurrences of `a`, `0` of `b`, `...`, `1` of `e`, `2` of `f`, `...`, `2` of `x` and `0` of `z`.

2 - After we got the occurences of the letters, we **swap** the **first letter with the most occurrences** with the **first letter with the least occurrences**, then the **second most** with the **second least**, then the **thid most** with the **third least**, then the **forth**, **fitch**, etc. => In sum, we swapped `a` (which has 6 occurrences) with `b` (which has 0), then we swapped `i` (3) with `c` (0), then `t` (3) with `d` (0), etc. and we got our *new alphabet*: `"baitngfpcyquvewhkxzdlmorjs"`
  - *After two letters have been swapped, they cannot be swapped with other letters anymore*
  - *Even if two letters have the same number of occurrence, and there are no more letters that have more or less occurrences than them, we still need to swap them, meaning: if `l` and `m` have the same number of occurrences which is `0` and they have not been swapped yet with any other letters then we swap them* (**Test 4** for example)

3 - Lastly, we replace the letters in the original message with their corresponding letters in the *new alphabet* then we got the encrypted message:`"vczj pbgbdxb dcbqw bungb cdj"`. **If there are "uppercase" then we keep the "case" even if the letter is swapped, we keep the "punctuations", "spaces" and any other characters than letters as well.**

Based on the above, encrypt the message in `text` with a program before sending it abroad.

© [lucoram](https://app.codesignal.com/profile/lucoram)

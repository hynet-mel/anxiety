# intro

`SceneSetup.intro();`

# intro-play-button

(...51)

[PLAY!](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

# intro-start

(...500)

`clearText()`

n3: Dus voordat we beginnen, hoe lees *jij* graag?

`publish("show_options_bottom")`

# intro-start-2

n3: Nu, laten we ons verhaal beginnen...

```
publish("hide_tabs");
clearText();
```

(...1000)

`publish("intro-to-game-2")`

n2: DIT IS EEN MENS

(...600)

`clearText()`

(...300)

`publish("intro-to-game-3")`

# act1

```
SceneSetup.act1();
publish("hide_tabs");
music('battle', {volume:0.5});
```

(...300)

n: EN DIT IS DE MENS ZIJN ANGST

n: _JIJ_ BENT DE ANGST

(#act1_normal)


# act1_normal

```
hong({body:"putaway"});
sfx("rustle");
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Nee. Niks niet, ik luister niet. Ik ga mijn mobiel checken.

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: JOUW TAAK IS OM JOUW MENS VOOR *GEVAAR* TE BEHOEDEN

`bb({eyes:"look", mouth:"small_lock", body:"fear"})`

b: Ah! Je scrolt je leven weg op Twitter! Alweer!

```
bb({eyes:"normal", mouth:"normal", body:"normal"});
hong({eyes:"annoyed"});
```

h: Ja ik vraag me af waarom ik niet vaker stilzit om naar mijn gedachten te luisteren.

`hong({eyes:"neutral"});`

n: VLUG, WAARSCHUW HEM VOOR EEN *GEVAAR!*

```
bb({eyes:"look"});
```

[Oh nee, kijk naar dat vreselijke nieuwsverhaal!](#act1d_news)

[Oh nee, gaat die tweet misschien over *ons*?](#act1d_subtweet)

[Hé, een GIF van een kat die melk drinkt](#act1d_milk)

# act1d_milk

`hong({mouth:"smile", eyes:"surprise"});`

h: Ha, ja dat is best schattig, ik--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: KATTEN KUNNEN GEEN MELK VERTEREN, WE ZIJN AKELIGE MENSEN DIE GENIETEN VAN DIERENMISHANDELING

(...200)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("20p", "bad");
publish("hp_show");
```




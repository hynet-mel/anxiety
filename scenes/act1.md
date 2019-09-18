# act1

```
SceneSetup.act1();
```

(...300)

n: EN DIT IS DE MENS ZIJN ANGST

n: _JIJ_ BENT DE ANGST

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}



# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: Oh hé! Zijn we hier weer?

`hong({eyes:"0_neutral"})`

n: JOUW TAAK IS OM JOUW MENS VOOR *GEVAAR* TE BEHOEDEN

`bb({eyes:"look", mouth:"small_lock"})`

n: HET HERHALEN VAN DIT SPEL BRENGT HEM IN FEITE OP DIT MOMENT IN *GEVAAR*

n: VLUG, WAARSCHUW HEM!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Mens! Luister, we zijn in gevaar! De speler...

[...staat op het punt on weer te kwellen!](#act1_replay_torture)

[...zal geen alternatief einde vinden!](#act1_replay_alternate)

[...krijgt last van ludonarratieve dissonantie!](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: Hij zal ons doen oprollen in een huilende bal!
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: Hij zal ons je mobiel laten vernielen vanwege een paniekaanval!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: Hij zal ons de gastvrouw *NIET* doen slaan!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight"}}
b: Hij zal ons de Sympathieke Anti-Schurk gastvrouw doen slaan!
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: Al springen we deze keer misschien niet van het da--
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b: HIJ LAAT ONS VAN HET DAK SPRINGEN.
{{/if}}

`bb({body:"fear"});`

b: ALLEMAAL NIEUWE VRESELIJKE DINGEN GAAN ONS OVERKOMEN, EN WE ZULLEN--

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Het verhaal in zijn *geheel* mag hetzelfde zijn, maar ieder hoofdstuk heeft twee eindes, en alle vertakkende gespreksmoge--

`bb({body:"fear"});`

b: Dan raakt de speler teleurgesteld, sluit de browsertab, verwijdert onzo software, en dan gaan we--

(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Een loeder-wat?

`bb({eyes:"normal"});`

b: Het verhaal ging erom dat je *KIEST* om een gezonde samenwerking met je angst te vormen,

`bb({eyes:"normal_right"});`

b: Maar de game herhalen geeft hetzelfde verhaal, insinuerend dat je *KEUZES* niet uitmaken,

`bb({eyes:"narrow_eyebrow"});`

b: Wat de tegenstrijdigheid blootlegt tussen het verhaal en de speldynamiek,

`bb({eyes:"fear"});`

b: Waardoor de hele realitieit van ons verhaal ontrafelt,

`bb({body:"fear"});`

b: En dan gaan we--

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: DOOOOOOOOOOOOOOOOOOOD

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.clearText();
```

(...1001)

```
bb({body:"laugh"});
hong({body:"laugh"});
Game.clearText();
sfx("laugh");
```

(...5001)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({body:"0_sammich"});
```

h: Oké, laten we terug in karakter gaan.

```
Game.clearText();
```

n4: (LAAT _JOUW_ ANGST BLA BLA BLA HET MEEST LIJKT OP WAAR _JIJ_ BANG BLA BLA JE WEET HOE HET WERKT)

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: Oh prachtig, mijn wolf is er weer. Gewèèèldig.

`hong({eyes:"0_neutral"})`

n: JOUW TAAK IS OM JOUW MENS VOOR *GEVAAR* TE BEHOEDEN

`bb({eyes:"look", mouth:"small_lock"})`

n: DIE BOTERHAM BRENGT HEM IN FEITE OP DIT MOMENT IN *GEVAAR*

n: VLUG, WAARSCHUW HEM!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Mens! Luister, we zijn in gevaar! Het gevaar is...

`bb({body:"squeeze"})`

n4: (LAAT _JOUW_ ANGST NAAR VOREN KOMEN! KIES WAT HET MEEST LIJKT OP WAAR _JIJ_ BANG VOOR BENT)

(#act1_normal_choice)

# act1_normal_choice

[We eten onze lunch helemaal alleen! Alweer!](#act1a_alone) `bb({body:"squeeze_talk"})`

[We zijn onproductief tijdens het eten!](#act1a_productive) `bb({body:"squeeze_talk"})`

[Witbrood is superslecht voor ons!](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: Weet je niet dat eenzaamheid wat betreft voortijdig sterven gelijkstaat aan 15 sigaretjes per dag roken?-

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad 2010, PLoS Medicine)

`hong({eyes:"0_annoyed"})`

h: Uh, fijn dat je je bronnen vermeldt maar--

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: Wat betekent dat als we niet *direct* iemand opzoeken, dan gaan we-

`bb({body:"panic"})`

b: DOOOOOOOOOOOOOOOOOOOD

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: JE GEBRUIKT *ANGST OM ONGELIEFD TE ZIJN*

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: Pak nu meteen je laptop en werk aan iets!

`hong({eyes:"0_annoyed"})`

h: Uh, ik krijg liever geen kruimels in mijn toetsenbo--

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Als we niet bijdragen aan de samenleving dan zijn we een maatschappelijke parasiet!
If we're not contributing to the body of society then we're a society-parasite!

b: Dan gaat het maatschappelijk lichaam naar de maatchappelijke dokter want het wil de maatschappelijke parasieten--

```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: DOOOOOOOOOOOOOOOOOOOD

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n: JE GEBRUIKT *ANGST OM EEN SLECHT MENS TE ZIJN*

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: Zijn die studies gereplicee--

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Verwerkte tarwe laat onze bloedsuiker pieken zodat al onze ledematen geämputeerd moeten worden en dan gaan we--

`bb({body:"panic"})`

b: DOOOOOOOOOOOOOOOOOOOD

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: JE GEBRUIKT *ANGST OM VERWOND TE WORDEN*

(#act1b)

# act1b

n: HET IS SUPER EFFECTIEF

`bb({mouth:"smile", eyes:"smile"});`

b: Nou, mens? Ben ik niet je trouwe waak-wolf?

`bb({body:"pride_talk"});`

b: Vertrouw je onderbuik! Je gevoelens deugen altijd!

`bb({body:"pride"});`

n: BRENG DE ENERGIEMETER VAN JE MENS NAAR NUL

n: OM ZIJN FYSIEKE + SOCIALE + MORELE BEHOEFTEN TE BESCHERMEN, GEBRUIK:

n: ANGST OM *VERWOND TE WORDEN* #harm#

n: ANGST OM *ONGELIEFD TE ZIJN* #alone#

n: EN ANGST OM *EEN SLECHT MENS TE ZIJN* #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: (PRO-TIP: KIES DE OPTIES DIE JE EIGEN DIEPSTE, DONKERSTE ANGSTEN RAKEN!~)

h: ...

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: weet je wat ik denk dat ik mijn mobiel ga checken.

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: BERSCHERM JOUW MENS

n: VAN DE WERELD. VAN ANDERE MENSEN. VAN ZICHZELF.

n: VEEL GELUK

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: EERSTE RONDE: *VECHT!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: Huh. Facebook feed zegt dat er dit weekend een feest is.

`bb({eyes:"uncertain"});`

b: Geeft die malloot niet *ieder* weekend een feest?

`bb({eyes:"uncertain_right"});`

b: Wat voor innerlijke leegte denkt ze te vullen? Ze is vast compleet gestoord vanbinnen!

`hong({eyes:"surprise"});`

h: En ik ben uitgenodigd?

`bb({eyes:"fear", mouth:"normal"});`

b: Nou dan!

[Accepteer, anders gaan we dood van eenzaamheid!](#act1c_loner)

[Weiger, het is daar vol met dodelijke drugs!](#act1c_drugs)

[Negeer, feestjes worden alleen maar somber van ons.](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: Vijftien sigaretjes per dag, mens! Vijftien!
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: Dan komt er niemand op onze begrafenis, ze dumpen onze as in de zee, we worden opgegeten door een walvis,
{{/if}}

{{if !_.fifteencigs}}
b: en dan worden we WALVISPOEP!
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: Dus ja, ga naar dat feest!
{{/if}}

{{if _.parasite}}
b: Neem wel je laptop mee om te werken zodat we geen maatschappelijke parasiet zijn.
{{/if}}

{{if _.whitebread}}
b: Zo lang ze maar geen WITBROOD serveren
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: MIJN GOD. Als je erover ophoudt, mij best.

h: Ik accepteer.

{{if _.whalepoop}}
b: Walvispoep, mens! Walvispoep!
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: of erger... WITBROOD
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: We kijgen zo'n overdosis aan meth en witbrood dat ons vette lijk niet eens meer in de crematieoven past!
{{/if}}

{{if !_.whitebread}}
b: We krijgen zo'n overdosis dat de begrafenisondernemer zich afvraagt hoe ons lijk al *vooraf* gebalsemd is geraakt!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: We kunnen trouwens niet eens feesten, we moeten werken om geen vreselijke parasiet te zijn!
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: MIJN GOD. Als je erover ophoudt, mij best.

h: Ik weiger.

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: We huilen altijd alleen maar in een hoekje over hoe eenzaamheid zo dodelijk is als 15 sigaretjes per dag.
{{/if}}

{{if _.parasite}}
b: We piekeren op feestjes altijd alleen maar over hoe we eigenlijk productief moeten zijn.
{{/if}}

{{if _.whitebread}}
b: We piekeren altijd alleen over hoe alle ongezonde snacks ons doodmaken.
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: wauw hoe zou dat komen.

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: Dus als we komen maken we ze ongelukkig, maar als we de uitnodiging weigeren worden ze ook ongelukkig!

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: MENSEN RAKEN ALLEEN MAAR ONGELUKKIG VAN ONS, WE MOETEN ONS SCHAMEN

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: Ugh. Als je erover ophoudt, mij best.

h: Ik negeer de uitnodiging.

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: Hoe dan ook... Facebook is me te veel. Ik heb iets kalmers en minder zorgwekkends nodig.

`hong({eyes:"neutral"});`

h: Wat is er op Twitter te doen?

`bb({eyes:"look"});`

[Oh nee, kijk naar dat vreselijke nieuwsverhaal!](#act1d_news)

[Oh nee, gaat die tweet misschien over *ons*?](#act1d_subtweet)

[Hé, een GIF van een kat die melk drinkt](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: God, het voelt of de wereld in brand staat, of niet?

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: Het voelt alsof alles ermee ophoudt, alsof iedereen doodgaat en we gedoemd zijn en er niks aan te doen is.

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: Laten we het retweeten!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Oké ik retweet het, blijk in hemelsnaam rustig!

`hong({mouth:"neutral", eyes:"annoyed"});`

h: Laat maar, ik ga wel naar Snapchat.

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: Het is een subtweet! Een stiekeme, gluiperige subtweet!

`hong({eyes:"annoyed"});`

h: Volgens mij niet?

`bb({eyes:"narrow", mouth:"small"});`

b: maar wat als ze allemaal achter onze rug om smoezen

h: Ze smoezen nie--

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: VÓÓR ONZE RUG

`hong({eyes:"sad", mouth:"sad"});`

h: Ik d--

`bb({eyes:"narrow", mouth:"small"});`

b: maar *wat als*

h: H--

`bb({eyes:"narrow_eyebrow"});`

b: *wat als*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ...

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: JUIST, laten we Snapchat proberen.

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: Ha, ja dat is best schattig, ik heb het geretweet, ik--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: KATTEN KUNNEN GEEN MELK VERTEREN, WE ZIJN AKELIGE MENSEN DIE GENIETEN VAN DIERENMISHANDELING

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("18p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: JUIST, laten we Snapchat proberen.

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: Huh, foto's van gisternacht. Dus *dat* is hoe die wekelijkse feestjes eruit zien.

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: Oef, dat ziet er veel te druk uit voor mijn angstproblemen.

h: Misschien had ik beter niet kunnen accepteren?

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[Ons antwoord veranderen? Als een ploert?!](#act1e_yes_dontchange)

[Verander ons antwoord! Het is te druk!](#act1e_yes_changetono)

{{if _.subtweet}}
[Ja ze waren ons echt wel aan het subtweeten.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Wacht we hebben geretweet zonder de feiten te checken.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Wist je dat je een hele slechte houding hebt?](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Ze rekenen op ons en nu verraden we hun vertrouwen? Wil je soms eenzaam doodgaan?!

{{if _.fifteencigs}}
b: VIJFTIEN. SIGARETTEN.
{{/if}}

{{if _.whalepoop}}
b: WALVISPOEP.
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Hou op hou op ik laat hem op 'ja' staan!

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Weet je niks over menselijke stormlopen?

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: In 2003 brak er brand uit in een nightclub in Rhode Island en de uitgangen slibden dicht met bange mensen en er brandden er 100 dood-

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: WIL JE DAT DAT ONS OVERKOMT-

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: ZEG NEE ZEG NEE ZEG NEE ZEG NEE ZEG NEE ZEG NEE ZEG NEE ZEG N-


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Hou op hou op ik zet mijn antwoord op 'nee'! Mijn hemel!

(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: Hm... dat lijkt best gezellig.

h: Misschien had ik de uitnodiging niet moeten weigeren?

`bb({mouth:"normal", eyes:"normal"});`

[Ons antwoord veranderen? Als een ploert?!](#act1e_no_dontchange)

[Verander ons antwoord! Ga niet eenzaam dood!](#act1e_no_changetoyes)

{{if _.subtweet}}
[Ja ze waren ons echt wel aan het subtweeten.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Wacht we hebben geretweet zonder de feiten te checken.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Wist je dat je een hele slechte houding hebt?](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: Iedereen rekent op ons!

b: ...om ze met rust te laten zodat ze een leuk feest kunnen hebben zonder een walgelijke {{if _.whitebread}}witbrood-vretende{{/if}} gluiperd zoals o--


```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Hou op hou op ik houd het op 'nee'!

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Chronische eenzaamheid verhoogt ons cortisolniveau en risico op hart-en-vaatziekten en beroertes!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: VIJFTIEN! SIGARETTEN.
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Hou op hou op ik zet mijn antwoord op 'ja'! Mijn hemel!

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: All onze problematische tweets halen ons in!

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: We worden voor paal gezet en krijgen ervan langs en worden met een touw achter een paard door door de drek getrokken!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Waarom doe je dit me aan?!

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: We verspreiden desinformatie! We ondermijnen vertrouwen in de vrije pers!

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Wij zijn de reden dat fascisme op zal rijzen uit de ruïne van democratie!

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
_.factcheck = true;
```

h: Waarom doe je dit me aan?!

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Wil je een ruggegraat als een krakeling?! Stop met over je scherm te buigen!

```
bb({body:"meta"});
```

b: En jij ook.

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Waarom doe je dit me aan?!

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: Hm... dat lijkt best gezellig.

h: Misschien had ik de uitnodiging niet moeten negeren?

`bb({mouth:"normal", eyes:"normal"});`

[Blijf negeren, we zijn nog altijd spelbrekers.](#act1e_ignore_continue)

[Weet je, zeg maar ja.](#act1e_ignore_changetoyes)

[Weet je, zeg maar nee.](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: Is het niet onbeleefd om het te blijven negeren?

`bb({eyes:"normal_right"});`

b: Nou andere mensen negeren *ons* altijd, dus

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: nu staan we gelijk.

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: You're... letting me have fun?

b: Well, I mean, loneliness *can* kill us.

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: It's too crowded. Crowds are dangerous.

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: Whatever. New Tinder notification.

`bb({eyes:"uncertain"})`

b: What, that hookup app?

`hong({eyes:"annoyed"})`

h: It's not a hookup app, it's just a way to meet new peopl--

`bb({eyes:"narrow"})`

b: It's a hookup app.

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: Oh, I got a match! They look cute!

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: Please don't ruin this for m--

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: DANGER DANGER DANGER DANGER DANGER DANGER

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[We're being *used* by other people.](#act1f_used_by_others)

[We're just *using* other people.](#act1f_using_others)

[YOUR MATCH IS A SERIAL KILLER](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: Random hookups may be able to fill the hole down there,

b: but they can never fill the hole...

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: in *here*.

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: The point is WE'RE GOING TO DIE ALONE

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: You think other people's genitals are Pokémon for us to collect?

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ (pokemon theme song)-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ I wanna be, the ^slut^ti-est-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ Like no one ever was-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ Thighs n' ^ass^, voluptuous breast-

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ with sweaty ^dick^ and balls!-

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ PERVY-MON! GOTTA CA-

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: The point is we're a manipulative creep.

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: They'll trap you in a well and force-feed you white bread to fatten you up so they can wear your skin like a suit!
{{/if}}

{{if _.parasite}}
b: They'll bludgeon you with a pomodoro timer and say "YOU SHOULDA BEEN MORE PRODUCTIVE YOU PARASITE"
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: They'll tear your flesh to gory confetti, turn your entrails into streamers, and mix your blood into a punch bowl!
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: How's THAT for a party invite?!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ...

(...500)

h: i'm so sick of this game.

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"loneliness will kill us"... {{/if}}
{{if _.parasite}}"we're a society-parasite"... {{/if}}
{{if _.whitebread}}"don't eat that, it'll kill us"... {{/if}}
{{if _.subtweet}}"they're talking behind our back"... {{/if}}
{{if _.badnews}}"the world is burning"... {{/if}}
{{if _.hookuphole}}"we'll die alone"... {{/if}}
{{if _.serialkiller}}"they're a serial killer"... {{/if}}
{{if _.catmilk}}"cats can't digest milk"... {{/if}}
{{if _.pokemon}}a ^crappy^ parody song... {{/if}}

h: i just want to live my life.

h: i just want to be free from all this... pain.

`bb({eyes:"look_sad"});`

b: Hey... human...

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: It'll be okay.

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: As your loyal guard-wolf, I'll always keep an eye out for danger, and do my best to keep you safe.

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: I promise.

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: Last app. Instagram. What you got?

`hong({eyes:"sad"});`

h: It's... more party pictures.

`hong({mouth:"sad"});`

h: Everyone looks so happy. Free from worry. Free from anxiety.

`hong({mouth:"anger"});`

h: God, why can't I be like them? Why can't I just be *normal?*

`bb({eyes:"normal_right"});`

b: Speaking of parties, about this weekend's invite. Here's my FINAL decision:

`bb({eyes:"normal"});`

[We should go.](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[We should not go.](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: We sh--

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *^FUCK^.*

`hong({body:"2_you"});`

h: YOU.

(...500)

b: w

(...1500)

`bb({eyes:"wat_2"});`

b: wha?

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: I'm going to say YES to that party,

{{if _.act1g=="go"}}
h: NOT because you want me to, but because *I* want to.
{{/if}}

{{if _.act1g=="dont"}}
h: Precisely BECAUSE you don't want me to.
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: You're NOT in control of me.

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: Now excuse me while I eat this delicious sandwich in ^goddamn^ peace.

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ...

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ...

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[AHHHH WE'RE GONNA DIE](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[AHHHH EVERYONE HATES US](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[AHHHH WE'RE HORRIBLE PEOPLE](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHH WE'RE GONNA DIE AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHH EVERYONE HATES US AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHH WE'RE HORRIBLE PEOPLE AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: CONGRATULATIONS

(...500)

n: YOU'VE SUCCESSFULLY PROTECTED YOUR HUMAN'S PHYSICAL + SOCIAL + MORAL NEEDS

n: WHY, LOOK HOW GRATEFUL THEY ARE!

(...500)

n: NOW THAT THEIR ENERGY IS ZERO, YOU CAN DIRECTLY CONTROL THEIR ACTIONS

`bb({mouth:"smile", eyes:"normal"});`

n: PICK YOUR ENDING MOVE

`bb({mouth:"small_lock", eyes:"fear"});`

n: *FINISH THEM*

[{FIGHT: Punish your stressful phone!}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{FLIGHT: Curl up in a ball and cry!}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: Your phone was giving you a panic attack!

`bb({eyes:"anger"})`

b: Zuckerberg and Co are hijacking your mental health for venture capitalist money!

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Punish your phone! Destroy it! Kill it!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL I--

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: The whole world is filled with danger!

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Do like the armadillo! Curl up into a ball for self-defense!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CR-- 

(#act1j)

# act1j

`SceneSetup.act1_outro()`

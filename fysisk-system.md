### Indholdsfortegnelse

* [Indledning](https://mpsteenstrup.github.io/Maanen-tur-retur/README.html)
* [Former](https://mpsteenstrup.github.io/Maanen-tur-retur/former.html)
* [bevaegelse](https://mpsteenstrup.github.io/Maanen-tur-retur/bevaegslse.html)
* [Fysisk system](https://mpsteenstrup.github.io/Maanen-tur-retur/fysisk-system.html)
* [Jorden og satellit](https://mpsteenstrup.github.io/Maanen-tur-retur/jorden-og-satellit.html)
* [Jorden - månen, tur - retur](https://mpsteenstrup.github.io/Maanen-tur-retur/jorden-og-manen-tur-retur.html)
* [Kodestumper og opsamling](https://mpsteenstrup.github.io/Maanen-tur-retur/kodestumper-og-opsamling.html)

# Simulering  med Python

Python bruger tabulator indrykning når den laver løkker. Det er ofte her det går galt når man kopierer kode fra andre steder. Løsningen er at slette indrykkene og lave dem igen, med tabulator knappen.

## Det simpleste eksempel
Vi starter med det lodrette kast uden luftmodstand. Fysikken er kendt som bevægelse med konstant acceleration. Startbetingerlserne er
* y = 10 m
* v = -10 m/s
* g = -9.82 m/s/s
* m = 1 kg

Hvilket svarer til at en bold 10 meter over jorden med en hastighed på v=-10m/s (nedad). Kør simuleringen
![[Bold hopper 1](https://glowscript.org/#/user/mps/folder/maanen/program/fysisk-system-1)](billeder/fysisk-system-1.png)
LINK: [https://glowscript.org/#/user/mps/folder/maanen/program/fysisk-system-1](https://glowscript.org/#/user/mps/folder/maanen/program/fysisk-system-1)

Jeg gennemgår koden i denne video.
![video (https://youtu.be/EiCOQMKtnUE)](billeder/video.png)
[Link til video.]((https://youtu.be/EiCOQMKtnUE))

### Prøv selv

Den bedste måde at få forståelse for programmet er at lave om i det. Prøv jer frem, men gør kun én ting af gangen, så kan I altid komme tilbage. Hver gang I laver noget om skal I prøve at baskrive hvad der er forandret i simuleringen.

* lav om på startbetingelserne, v og y
* Hvad sker der hvis hastigheden er positiv?


## Fysiske model

Det går selvfølgeligt ikke at bolden bare forsvinden op i luften. Ændring i hastighed hedder acceleration og er på jorden tyngdeaccelerationen, g=-9.82. Vi opdaterer hastigheden ved
```
v = v + g*dt
```
altså opdatere hastigheden med g gange tidsskridtet dt.

* fjern # fra linje 20,  v = v + g*dt så hastigheden bliver opdateret og sæt v=0 som start.
* hvordan ser bevægelsen nu ud?

### Grafer

Det er let at lave grafer, så lad os gøre det. Vi vil gerne undersøge hypotesen om at den mekaniske energi er bevaret.


* Udkommenter de sidste grønne linjer for at få graferne.
* Beskriv graferne, sæt evt. ```rate``` ned, så det ikke går så hurtigt.


### Bold på Månen

Hvis bolden er på Månen er den udsat for en mindre tyngdekraft. Det betyder at accelerationen på månen er gm = -1.6.

nedenfor er en ekstra bold sat ind som hopper på Månen.

![[to bolde, forskellig tyngdekraft](https://glowscript.org/#/user/mps/folder/maanen/program/fysisk-system-2)](billeder/fysisk-system-2.png)
LINK: [https://glowscript.org/#/user/mps/folder/maanen/program/fysisk-system-2](https://glowscript.org/#/user/mps/folder/maanen/program/fysisk-system-2)

Graferne viser den potentielle energi for de to bolde ved fald fra samme højde.
* Beskriv de to grafer og overvej hvordan graferne for den kinetiske energi vil se ud.
* Prøv at lav om i koden så du plotter den kinetiske energi.





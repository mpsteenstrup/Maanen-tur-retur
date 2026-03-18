### Indholdsfortegnelse

* [Indledning](https://mpsteenstrup.github.io/Maanen-tur-retur/maanen-tur-retur.html)
* [Former](https://mpsteenstrup.github.io/Maanen-tur-retur/former.html)
* [bevaegelse](https://mpsteenstrup.github.io/Maanen-tur-retur/bevaegslse.html)
* [Fysisk system](https://mpsteenstrup.github.io/Maanen-tur-retur/fysisk-system.html)
* [Jorden og satellit](https://mpsteenstrup.github.io/Maanen-tur-retur/jorden-og-satellit.html)
* [Jorden - månen, tur - retur](https://mpsteenstrup.github.io/Maanen-tur-retur/jorden-og-manen-tur-retur.html)
* [Kodestumper og opsamling](https://mpsteenstrup.github.io/Maanen-tur-retur/kodestumper-og-opsamling.html)

## Jorden og en satellit, simpelt setup

For at komme i gang vil vi se på Jorden og få en satellit til at foretage cirkelbevægelser omkring den.

VPython har elementer som sphere og arrows, som bliver skrevet som vektorer. Det er meget brugbart for os, da bevægelse og kræfter også kan beskrives med vektorer.
Kraften, kan skrives som 

$$
\vec{F} = (F_x,F_y,F_z)
$$

Vi kan bruge Newtons 2 lov til at finde accelerationen, hvis vi kender massen,m

$$
\vec{a} = \frac{\vec{F}}{m}.
$$

Den eneste kraft er tyngdekraften og den kan skrives som,

$$
\vec{F} = -G\frac{mM}{r^3}\vec{r},
$$

hvor, *G* er gravitationskonstanten, *m* satellittens masse, *M* jordens masse og *r* afstanden mellem jordens centrum og satellitten.

### Affyring fra jorden

Jo længere vi er væk fra Jorden jo lavere er tyngdekraften. I loopet beregnes tyngdekraften med. 
```
 F=-G*mSat*mEarth/(mag(r)**3)*r

```
hvor 
```
mag()
```
giver størrelsen, eller længden af vektoren.

Prøv at kør programmet.

![[Kredsløb om Jorden, lav bane.](https://glowscript.org/#/user/mps/folder/maanen/program/satellitter)](billeder/jorden-og-satellit-1.png)

 [https://glowscript.org/#/user/mps/folder/maanen/program/satellitter](https://glowscript.org/#/user/mps/folder/maanen/program/satellitter)

### Øvelse

* Tjek om den mekaniske energi er bevaret, og fortolk graferne for den kinetiske og potentielle.
* Prøv at skift affyringsretning til lodret affyring, linje 28, ```v.sat=vec(0,v,0)```.
* Prøv at fortolk Ekin og Epot ogEmek.


### Affyring til kredsløb 

Ovenfor fik vi en satellit i kredsløb ved at sende den vandret afsted. Det resulterede i en bane hvor satelitten kom tilbage til afsenderen, altså tilbage til Jorden. Hvis vi vil have et rigtigt kredsløb bliver vi nød til at give vores satellit endnu et skub. 

Det gøres ved
```
if (t>(60*60*5) and a==0):
    F = F + push*norm(sat.v)
    arrow(pos=sat.pos, axis=norm(sat.v)*1e7)
    a=1
```
inde i while loopet. Koden aktiveres når tiden er større end ```60*60*5```sekunder og ```a==0``` gør at det kun sker én gang. Kraften bliver opdateret med et skub, push, i sattelittens bevægelsesretning, norm(sat.v).

![[Op i rigtig bane, men hvordan?](https://glowscript.org/#/user/mps/folder/maanen/program/satellitter-2)](billeder/jorden-og-satellit-2.png)

 [https://glowscript.org/#/user/mps/folder/maanen/program/satellitter-2](https://glowscript.org/#/user/mps/folder/maanen/program/satellitter-2)



### Øvelse

* Prøv at lav den mest ciruklære orbit som muligt, ved at ændre på, størrelsen af skubbet, push, og tidspunktet for skubbet ( hint overvej hvornår satellitten er længst fra Jorden).
* Undersøg sattelittens fart ved at plotte grafen for ```(t,mag(sat.v))```.
* Undersøg hvad der sker hvis skubbet ikke er i sattelittens bevægelsesretning, indsæt eks. ```vec(0,1,0)``` i linje 37 i stedet for norm(sat.v).


### Satellit i kredsløb

I simulationen nedenfor starten vores satellit i højden, d, med en hastighed, v, vinkelret på Jorden.

![[Cirkulært orbit. ](https://glowscript.org/#/user/mps/folder/maanen/program/satellit-3)](billeder/jorden-og-satellit-3.png)
[https://glowscript.org/#/user/mps/folder/maanen/program/satellit-3](https://glowscript.org/#/user/mps/folder/maanen/program/satellit-3)



### Øvelse

* Besktiv om det visuelt ser ud til at satellittens fart er konstant.
* Hvad er forskellen på hastighed og fart.

For at komme videre skal I ændre i koden

## Øvelser

Vektoren (0,v,0) i linje 27 definerer starthastigheden 

* Prøv at ændre i starthastigheden, eks. 80% eller 120%.
* Prøv også at ændre vinklen ved at give en hastighed langs de andre akser

## Øvelse

Der er flere parametre I kan ændre på, og det skal I.

* Find det sted i koden hvor Jordens masse bliver defineret, Me, og forøg den. Hvad sker der med omløbstiden.
* Gør det samme med satellittens masse. Hvad sker der så.
* Prøv også at ændre på afstanden, hvordan tror I at omløbstiden afhænger af afstanden.

## Konklusion, eller metarefleksion
Overvej hvor du har brugt de fire elementer af Computational Thinking 

* Decomposition
* Abstraction
* Pattern recognition
* Algorithms


<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
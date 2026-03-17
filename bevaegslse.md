### Indholdsfortegnelse

* [Indledning](https://mpsteenstrup.github.io/Maanen-tur-retur/)
* [Former](https://mpsteenstrup.github.io/Maanen-tur-retur/former.html)
* [bevaegelse](https://mpsteenstrup.github.io/Maanen-tur-retur/bevaegslse.html)
* [Fysisk system](https://mpsteenstrup.github.io/Maanen-tur-retur/fysisk-system.html)
* [Jorden og satellit](https://mpsteenstrup.github.io/Maanen-tur-retur/jorden-og-satellit.html)
* [Jorden - månen, tur - retur](https://mpsteenstrup.github.io/Maanen-tur-retur/jorden-og-manen-tur-retur.html)
* [Kodestumper og opsamling](https://mpsteenstrup.github.io/Maanen-tur-retur/kodestumper-og-opsamling.html)

# Bevæglse

Hvis vi skal have noget til at bevæge sig skal vi bruge et loop. Loops er enormt smarte.

Nedenunder er lavet en pil ved brug af arrow kommandoen. For at få den til at bevæge sig skal vi opdatere hvor den er, positionen. x positionen af pilen skrives som pil.pos.x ( pilens x position).

Loopet starter med at vi sætter i=0 for at have en start. De tre indrykkede linjer bliver kørt igen og igen så længe betingelsen (i<20) er opfyldt. Derfor er det vigtigt med tredje linje hvor i=i+1. Det giver ikke matematisk mening men betyder at vi lægger 1 til i.
```
i=0
while i<20:
  rate(10)
  pil.pos.x = i
  i = i+1
```
prøv at kør programmet og se hvad det gør.

![[Bevægelse](https://glowscript.org/#/user/mps/folder/maanen/program/move)](billeder/move.png)
LINK: [https://glowscript.org/#/user/mps/folder/maanen/program/move](https://glowscript.org/#/user/mps/folder/maanen/program/move)

* Beskriv hvad der sker med pilen.
* Lav om på rate.
* Skriv pil.pos.x = i + pil.pos.x, hvad sker der?
* Udkommenter de fire linjer med rotation.
* Prøv at beskriv hvad den nye del af koden gør.
* Fri leg, lav andre figure og få dem til at flytte sig.
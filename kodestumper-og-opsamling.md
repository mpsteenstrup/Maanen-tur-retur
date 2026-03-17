### Indholdsfortegnelse

* [Indledning](https://mpsteenstrup.github.io/Maanen-tur-retur/)
* [Former](https://mpsteenstrup.github.io/Maanen-tur-retur/former.html)
* [bevaegelse](https://mpsteenstrup.github.io/Maanen-tur-retur/bevaegslse.html)
* [Fysisk system](https://mpsteenstrup.github.io/Maanen-tur-retur/fysisk-system.html)
* [Jorden og satellit](https://mpsteenstrup.github.io/Maanen-tur-retur/jorden-og-satellit.html)
* [Jorden - månen, tur - retur](https://mpsteenstrup.github.io/Maanen-tur-retur/jorden-og-manen-tur-retur.html)
* [Kodestumper og opsamling](https://mpsteenstrup.github.io/Maanen-tur-retur/kodestumper-og-opsamling.html)

** opsamling programmering **

I har været igennem nogle centrale elementer i programmering her kommer en opsummering.

## løkker
Løkker eller loops, er dele af programmet som gentages. I python sker det ved indryk, i andre programmet eks. vec {}.

```python
i = 0
while i < 20:
  sphere(pos=vec(i-10,0,0))
  i = i+2
```
[Link til koden.](https://glowscript.org/#/user/mps/folder/MyPrograms/program/kodestumper-1)

* eksperimenter, prøv eks. at lave et gitter
* prøv at få noget til at bevæge sig, eks. pil.pos.x=pil.pos.x+1 i en løkke



## hvis betingelser
De er også kaldet if statements. If statements tjekker en betingelse og udfører det indrykkede hvis betingelsen er opfyldt.

```python
a=0
i = 0
while i < 20:
  sphere(pos=vec(i-10,a,0))
  i = i+2
  if i>10:
    a=random()*10
```
[Link til koden.](https://glowscript.org/#/user/mps/folder/maanen/program/kodestumper-2)


## Break

Vi kan også få noget til at køre uendeligt, eller indtil en betingelse er opfyldt. Det sker med if True og break.

```python
i = 0
while True:
  sphere(pos=vec(i-10,0,0))
  i = i+2
  if i>10:
    break
```

[Link til koden.](https://glowscript.org/#/user/mps/folder/maanen/program/kodestumper-3)

## Lister

Lister kaldes også arrays og skrives med [] omkring. Man kan putte alt muligt ind i listerne.

```python
c = [color.blue, color.green]
n = [-1, 1, -3, 3, -5, 5, -7, 7]
t = ['en', 'to', 'tre', '4', '5', '6', '7', '8']

i = 0

# Vi bruger len(n) for at sikre, at vi ikke løber tør for tal i listen
while i < len(n):
    sphere(pos=vec(n[i], 0, 0), color=c[i % 2], radius=0.3)
    # Vi rykker teksten lidt op med vec(n[i], 0.5, 0), så den ikke overlapper kuglen
    label(pos=vec(n[i], 1.0, 0), text=t[i], box=False)
    i = i + 1

# Tilføj et element til listen t
t.append("9")
print(t)
```

[Link til koden.](https://glowscript.org/#/user/mps/folder/maanen/program/kodestumper-4)


### opsummering fysik
Formålet med fysikken var at træne jeres forståelse af Potentiel og Kinetisk energi i forbindelse med orbitaler, planeter, satellitter osv.

I skulle gerne kunne svare på følgende.

* Hvordan ser kurverne for Ekin og Epot ud for en satellit i orbit.
* Hvordan afhænger den potentielle energi af afstanden til Jorden.
* Hvordan kommer man fra en kraft til en acceleration.
* Hvordan kommer man fra en acceleration til en ændring i hastigheden.
* Hvordan kommer man fra en hastighed til en ændring i positionen.




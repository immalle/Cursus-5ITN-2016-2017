# Drankautomaat

# Oefening drankautomaat (update)

Ken je de oefening van de drankautomaat nog? Je steekt een bedrag in eurocenten in een automaat en deze moet geld teruggeven. Kan je een functie schrijven die het retour-geld als waarde returnt en deze 2 parameters gebruikt : 

- het ingeworpen geld (in eurocent, b.v. 250)
- de prijs van het product (in eurocent, b.v. 210)

> Merk op wat **nieuw** is aan deze oefening : het gebruik van een **functie**. Het
algoritme (dat in de functie moet) kan je uit je vorige oplossingen halen maar
het is natuurlijk altijd een goed idee om het algoritme (de benodigde
variabelen, de %-operator, ...) eerst nog eens zelf te proberen vinden.

De functie (ik noem ze hier `BerekenRetour`) moet dus zo te gebruiken zijn:

```
int retourGeld = BerekenRetour(250, 210);
Console.WriteLine(retourGeld);
```

of wat vollediger:

```
int inworp = 250;
string keuze = "bruiswater";
if(keuze == "bruiswater") {
	int kostprijs = 210;
	int retourGeld = BerekenRetour(inworp, kostprijs);
	Console.WriteLine("U hebt {0} cent ingeworpen en wil een {1} van {2} cent? Dan krijgt u {3} cent terug.", inworp, keuze, kostprijs, retourGeld);
} else {
	Console.WriteLine("Ongeldige keuze. Uw inworp wordt teruggegeven.");
}
```

> Merk dus op hoe we `BerekenRetour` gebruiken als een *bouwsteen* van het
programma. Een bouwsteen die we verschillende malen (met andere
parameters/argumenten) kunnen gebruiken.


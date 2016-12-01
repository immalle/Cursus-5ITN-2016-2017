# Lists

In programma's heb je zeer vaak een verzameling (collectie) van dingen nodig.
De meest gebruikte en handigste datastructuur in C# is de `List`, meerbepaald
een *generische* `List`.

> Generisch wil zeggen dat we tussen `<`- en `>`-tekens het **type** v.d. `List`
meegeven.

## basishandelingen

Deze code initialiseert een nieuwe lege lijst:

```
List<int> getallen = new List<int>();
```

Dit kan ook korter geschreven worden:

```
var getallen = new List<int>();
```

Vervolgens kunnen we er basis-operaties op uitvoeren zoals

- toevoegen

```
getallen.Add(3);
```

- een getal verwijderen

```
getallen.Remove(3);
```

- een getal uitlezen via de indexer (AKA de index-operator)

```
Console.WriteLine(getallen[3]);
int x = getallen[1];
```

- een getal verwijderen

```
getallen.Remove(3);
```

- een getal verwijderen a.h.v. zijn index

```
getallen.RemoveAt(0);
```

- (in-place) sorteren

```
getallen.Sort();
```


# itereren

Itereren over een `List` doe je meestal met 

- een `for`-lus:

```
for (int i = 0; i < getallen.Count; i++)
{
  Console.WriteLine(getallen[i]);
}
```

- een `foreach`-lus:

```
foreach(var getal in getallen) 
{
  Console.WriteLine(getal);
}
```


## Voorbeeld

In dit voorbeeld vullen we een lijst met 1000 getallen van max. 1 miljoen groot.
Daarna sorteren we de lijst en verwijderen we het element op index 0 of m.a.w.
verwijderen we het laagste getal uit de lijst.

```
List<int> getallen = new List<int>();
Random rndGen = new Random();

for (int i = 0; i < 1000; i++)
{
    getallen.Add(rndGen.Next(1000000));
}

for (int i = 0; i < getallen.Count; i++)
{
    Console.WriteLine(getallen[i]);
}

getallen.Sort();

getallen.RemoveAt(0);
```


## Functies die een `List` als parameter nemen

> Opgelet: `List<int>` is een ander type dan `List<string>`.
> Bij het definiëren v.e. method moet het type dus correct zijn!

```
static void PrintGetallen(List<int> getallenLijst)
{
   Console.WriteLine("Er zitten {0} getal(len) in deze lijst.", getallenLijst.Count);
   foreach(var getal in getallenLijst)
   {
      Console.WriteLine(getal);
   }
   Console.WriteLine(new String('-', 79));
}
```


## Functies die een `List` als return-waarde hebben

```
static List<int> GenereerGetallen(int start, int stop, int stap)
{
   List<int> temp = new List<int>();

   for (var i = start; i < stop; i += stap)
   {
      temp.Add(i);
   }

   return temp;
}
```

**Belangrijk**: er wordt (net zoals bij elke andere class) pas een nieuwe lijst
gemaakt als `new` aangeroepen wordt.
Deze code returnt dus een *referentie* naar een nieuwe gemaakte lijst!


## `List`'s van andere dingen

### Strings

```
var namen = new List<string>();

namen.Add("Jos");
namen.Add("Willy");

foreach(var naam in namen) {
  Console.WriteLine("Hallo {0}!", naam);
}
```

### Objecten

In deze voorbeelden werken we steeds met `List`'s van `int`
maar uiteraard kan je ook `List`'s maken van eigen objecten,
zoals `Dier`, `Persoon`, ...

Handig is dan dat `foreach` automatisch dit type overneemt:

```
List<Dier> dieren = new List<Dier>();
// ...

foreach(Dier d in dieren) 
{
   // ...
}
```

of korter:

```
foreach(var d in dieren)
{
   Console.WriteLine(d.Gewicht); // stel dat de class Dier een property Gewicht heeft
}
```

## Demo

- met getallen : https://dotnetfiddle.net/DTzt7Z
- met `Dier`en : https://dotnetfiddle.net/TKu4Ox


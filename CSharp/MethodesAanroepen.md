# Methodes aanroepen

In de voorgaande hoofdstukken heb je al heel wat methodes aangeroepen.

Ze zijn steeds te herkennen aan de ronde haken `()`. Tussen de haken kunnen
we **argumenten** meegeven.

Voorbeelden:

```
paper.DrawRectangle(pen, 10, 100, 50, 50);  // DrawRectangle met 5 argumenten
Console.WriteLine("Hallo");                 // WriteLine met 1 string-argument
```

Sommige van deze methods, hebben een **return-waarde**.

Voorbeelden:

```
string s = Console.ReadLine();              // ReadLine zonder argumenten met string-return waarde
int i = Convert.ToInt32(6.4);               // ToInt32 met 1 double-parameter en int-return waarde
```

De return-waarde kan worden opgeslagen in een variabele met de
**toekenningsoperator** (`=`).

Het is niet omdat een method een return-waarde heeft, dat we er ook iets
mee **moeten** doen.

B.v.

```
Console.ReadLine();
```

heeft als return-waarde hetgeen de gebruiker ingetypt heeft maar hier
wordt deze waarde gewoon weggegooid. We gebruiken `ReadLine()` hier enkel
zodat de gebruiker op `<ENTER>` zou drukken om verder te gaan.

# Methodes aanroepen

Ze zijn steeds te herkennen aan de ronde haken `()`. Tussen de haken kunnen
we **argumenten** meegeven.

Voorbeelden:

```
Console.WriteLine("Hallo");                 // WriteLine met 1 string-argument. WriteLine is een static method van de class Console
paperCanvas.Children.Add(ellipse1);         // De Add-method met 1 parameter (een Ellipse object) van een object gereturnt door de property Children (Children is van type UIElementCollection)
```

Sommige van deze methods, hebben een **return-waarde**.

Voorbeelden:

```
string s = Console.ReadLine();              // ReadLine zonder argumenten met string-return waarde
int i = Convert.ToInt32(6.4);               // ToInt32 met 1 double-parameter en int-return waarde
double x = Math.Floor(4.6);                 // Floor is een static method van de class Math
double y = Math.Round(4.6);
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

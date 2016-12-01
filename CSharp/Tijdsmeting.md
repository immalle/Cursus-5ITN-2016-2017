# Tijdsmetingen

De techniek bestaat er in om op 2 tijdstippen het huidige tijdstip vast te leggen.
Nadien kan het verschil (een `TimeSpan`) berekend worden.

```
static void Main(string[] args)
        {
            DateTime voor = DateTime.Now;

            Console.Write("Geef je naam: ");
            string naam = Console.ReadLine();

            DateTime na = DateTime.Now;
            TimeSpan verschil = na - voor;

            Console.WriteLine("Dag {0}. Je hebt er {1} seconden over gedaan om je naam van {2} karakters in te typen!", 
                naam, 
                verschil.TotalSeconds,
                naam.Length);

            double timePerCharacter = verschil.TotalSeconds / naam.Length;

            if(timePerCharacter > 0.50)
            {
                Console.WriteLine("Jij bent wel een trage typer!");
            }
        }
```

# Profilen

Profilen is het uitzoeken waar de *bottle-neck* in snelheid (of geheugengebruik)
van een programma optreedt.

> Men zegt trouwens : **Premature optimization is the root of all evil**.
> D.w.z. dat je in eerste instantie duidelijke code moet schrijven
> en pas achteraf moet gaan uitzoeken waar er - **indien nodig** - 
> snelheidsverbeteringen kunnen doorgevoerd worden.

Er bestaan tools om uitgebreid te *profilen* maar met deze eenvoudige techniek
is het ook mogelijk:

```
DateTime pre = DateTime.Now;

UInt64 sum = 0;
		
Console.WriteLine(UInt32.MaxValue);

for(UInt64 i = 0; i < UInt32.MaxValue; i++)
{
	sum += i;
}

DateTime post = DateTime.Now;
	
Console.WriteLine(post - pre);
```

# Voorbeelden

- https://dotnetfiddle.net/E0ckHf (Time limit exceeded error : probeer op eigen computer)

# Seconden omzetten naar uren, minuten en seconden 

## Intro

Kijk zeker eerst naar het omgekeerde algoritme : het omzetten van seconden naar
dagen, uren en minuten.

Het algoritme en de berekeningen op zich zou je ondertussen zelf moeten kunnen
afleiden (vergelijk ook met het algoritme van het wisselgeld met de
drankautomaat).

De moeilijkheid hier zit bij het *refactoren* naar methods. C# ondersteund immers
slechts functies met 1 return-waarde (i.t.t. sommige andere talen zoals Python,
Go, ...). Als naam kiezen we voor de method `SecondenNaarUMS` maar welke
parameters en return-waarden moeten we dan kiezen?

We zullen enkele manieren bespreken en welke je best gebruikt:

- gebruik van `out`-parameters (te complex)
- gebruik van globale variabelen (slecht!!)
- gebruik van een `struct` als return-type (goed!)
- gebruik van een `class` als return-type (goed!)

> Merk ook op dat deze functionaliteit al in dotnet aanwezig is vanuit de
> `DateTime`-struct en je in een echt programma dit algoritme dus niet opnieuw
> zou moeten uitvinden!

## Analyse

Enkele voorbeelden:

### 200 seconden

```
200 / 60 = 3
200 % 60 = 20
```

dus 200 secconden zijn 3 min. en 20 seconden

### 1000000 seconden

```
1 000 000 / 3600 = 277
1 000 000 % 3600 = 2800

2800 / 60 = 46
2800 % 60 = 40
```

dus 1 miljoen seconden zijn 277 uur, 46 minuten en 40 seconden.

## Input- en output-variabelen

De **input**-variabele is een `totaalSeconden` (`int`).

De **output**-variabelen zijn: `uren`, `minuten`, `seconden` (`int`).

## Algoritme

Afgeleid uit de voorbeelden en gebruik makend van de juiste variabele-namen,
kunnen we nu dus een algemeen algoritme opstellen:

```
// input-variabele
int totaalAantalSeconden = 100;

// output-variabelen
int uren = 0;
int minuten = 0;
int seconden = 0;

// tijdelijke tussentijdse variabele
int rest = 0;

// algoritme:
uren = totaalAantalSeconden / (60 * 60);
rest = totaalAantalSeconden % (60 * 60);
minuten = rest / 60;
seconden = rest % 60;
```

## Testen

Voorzie een aantal mogelijke testen, zoals die uit het voorbeeld.

Beschouw zeker ook randgevallen en makkelijk te controleren waarden, zoals:

- `1 sec`
- `1 minuut`
- `1 uur`
- ...

## Afgewerkt programma m.b.v. `out`-parameters

Het is mogelijk om met een method te werken die meer dan 1 return-waarde heeft
door met `out`-parameters te werken maar dat is meestal niet de elegantste manier.

Het voordeel is wel dat de method altijd werkt zoals verwacht: met inputs en outputs.
Ze verandert b.v. geen globale variabelen. We zijn altijd zeker dat deze method met
dezelfde inputs, dezelfde outputs zal genereren.

```
class Program
{
    static void SecToHMS(int totaalAantalSeconden, out int uren, out int minuten, out int seconden)
    {
        // tijdelijke tussentijdse variabele
        int rest = 0;

        // algoritme:
        uren = totalSeconds / (60 * 60);
        rest = totalSeconds % (60 * 60);
        minuten = rest / 60;
        seconden = rest % 60;
    }

    static void Main(string[] args)
    {
        int h = 0;
        int m = 0;
        int s = 0;

        SecToHoursMinsSecs(61, out h, out m, out s);

        Console.WriteLine("{0} hours {1} minutes and {2} seconds", h, m, s);
    }
}
```

## Afgewerkt programma m.b.v. globale variabelen (SLECHT!)

Vele programmeurs komen in de verleiding om *globale* variabelen (in dit geval:
class-variabelen) te gebruiken die dan kunnen aangepast worden door een method en
gebruikt worden op een andere plaats.

We zondigen dan echter (in dit geval slechts een beetje omdat het zo'n klein
programma is) tegen het principe van **encapsulatie** dat eigenlijk zegt dat we
zoveel mogelijk beïnvloeding van buiten af moeten vermijden.

```
class Program
{
    static int hours;
    static int mins;
    static int secs;

    static void SecToHoursMinsSecs(int totalSeconds)
    {
        int rest = 0;

        hours = totalSeconds / (60 * 60);
        rest = totalSeconds % (60 * 60);
        mins = rest / 60;
        secs = rest % 60;
    }

    static void Main(string[] args)
    {
        SecToHoursMinsSecs(61);

        Console.WriteLine("{0} hours {1} minutes and {2} seconds", hours, mins, secs);
    }
}
```

## Afgewerkt programma m.b.v. struct

Dit is een elegante oplossing voor het probleem van de meerdere return-waarden
omdat we ze nu gegroepeerd hebben in 1 data-structuur.

Een method kan zonder probleem 1 dergelijke struct returnen.

We hebben dus opnieuw een method waarbij met bepaalde inputs, steeds dezelfde
output verwacht wordt. Het algoritme is netjes geëncapsuleerd in deze éne method.

```
struct HMSTime
{
    public int Hours;
    public int Mins;
    public int Secs;
}


class Program
{
    static HMSTime SecToHMS(int totalSeconds)
    {
        HMSTime time;
        int rest = 0;

        time.Hours = totalSeconds / (60 * 60);
        rest = totalSeconds % (60 * 60);
        time.Mins = rest / 60;
        time.Secs = rest % 60;

        return time;
    }

    static void Main(string[] args)
    {
        HMSTime time = SecToHMS(61);
        Console.WriteLine("{0} hours {1} minutes and {2} seconds", time.Hours, time.Mins, time.Secs);
    }

}
```

De struct `HMSTime` mag eventueel ook *binnen* de class `Program` staan
maar dan zou je deze daarbuiten niet kunnen gebruiken.

Je zou ook kunnen overwegen om een method te schrijven die met deze `HMSTime` overweg kan, b.v.

```
static void PrintHMSTime(HMSTime time)
{
    Console.WriteLine("{0} hours {1} minutes and {2} seconds", time.Hours, time.Mins, time.Secs);
}
```

Je roept deze method dan aan in je `Main`-method.

Nog beter is om b.v. de `ToString()`-functie te overriden in de struct:

```
struct HMSTime
{
    public int Hours;
    public int Mins;
    public int Secs;

    public override string ToString()
    {
        return String.Format("{0} hours {1} minutes and {2} seconds", Hours, Mins, Secs);
    }
}
```

> Merk op: hoewel een struct een **value**-type is en we er normaal gezien niet van kunnen
> overerven, kunnen we wel de method van `System.Object` (zoals `ToString`) overriden.

Het gebruik wordt dan simpelweg:

```
static void Main(string[] args)
{
    HMSTime time = SecToHMS(61);

    Console.WriteLine(time);
}
```

## Afgewerkt programma m.b.v. class

:construction:


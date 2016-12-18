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

:construction:

## Afgewerkt programma m.b.v. globale variabelen (SLECHT!)

:construction:

## Afgewerkt programma m.b.v. struct

:construction:

## Afgewerkt programma m.b.v. class

:construction:


# Gehele getallen

## Declaratie en initialisatie

Declaratie van een geheel getal:

```
int x;
```

Declaratie + initialisatie van een geheel getal :

```
int x = 3;
```

## Rekenkundige operatoren

Variabelen van type `int` ondersteunen volgende rekenkundige operatoren:

| operator     | omschrijving                          | voorbeeld         |
|--------------|---------------------------------------|-------------------|
| `+`          | som van 2 termen                      | `int a = 2 + 3;`  |
| `-`          | verschil tussen 2 termen              | `int b = 8 - 12;` |
| `*`          | product van 2 factoren                | `int p = 2 * 7;`  |
| `/`          | quotient van 2 deeltal met deler      | `int q = 13 / 3;` |
| `%`          | rest bij (gehele) deling              | `int r = 13 % 3;` |
| prefix `++`  | eerst met 1 verhogen, daarna returnen | `int b = ++a;`    |
| postfix `++` | eerst returnen, daarna met 1 verhogen | `int b = a++;`    |

## Voorbeeld

https://dotnetfiddle.net/Al9h5s

## Vergelijkingsoperatoren

Het resultaat van een vergelijking is een `bool` (`true` of `false`):

> Stel dat we eerst 2 `int`'s `a` en `b` definiëren:

```
int a = 4;
int b = 8;
```

| operator | omschrijving          | voorbeeld          |
|----------|-----------------------|--------------------|
| `>`      | groter dan            | `bool r = a > b;`  |
| `<`      | kleiner dan           | `bool r = a < b;`  |
| `>=`     | groter of gelijk aan  | `bool r = a >= b;` |
| `<=`     | kleiner of gelijk aan | `bool r = a <= b;` |
| `==`     | gelijk aan            | `bool r = a == b;` |
| `!=`     | niet gelijk aan       | `bool r = a != b;` |

> Vergelijkingsoperatoren worden b.v. gebruikt in een `if`-voorwaarde:

```
if(a > b) {
    Console.WriteLine("{0} is groter dan {1}.", a, b);
} else if(a < b) {
    Console.WriteLine("{0} is kleiner dan {1}.", a, b);
} else {
    Console.WriteLine("{0} is gelijk aan {1}.", a, b);
}
```

## Denkoefening

Wat doet deze code?

```
bool b = 2 == 2;
```

> TIP: maak onderscheid tussen:
> - `=`, de toekenningsoperator
> - `==`, de vergelijkingsoperator om te controleren of 2 variabelen gelijk zijn

## Varianten

Een `int` in C# komt overeen met het .NET type `System.Int32`.

Een greep uit enkele andere types voor gehele getallen:

| C# type | .NET type     | beschrijving       | grootte | kleinst mogelijke waarde | grootste mogelijke waarde |
|---------|---------------|--------------------|---------|--------------------------|---------------------------|
| byte    | System.Byte   | een unsigned byte  | 8 bits  |                        0 |                       255 |
| sbyte   | System.SByte  | een signed byte    | 8 bits  |                     -128 |                       127 |
| ushort  | System.UInt16 | een unsigned short | 16 bits |                        0 |                     65535 |
| short   | System.Int16  |                    | 16 bits |                   -32768 |                     32767 |

Zie ook:

- https://dotnetfiddle.net/5up6Og
- https://msdn.microsoft.com/en-us/library/exx3b86w.aspx


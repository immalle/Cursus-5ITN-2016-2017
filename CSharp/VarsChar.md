# Karakters

Een karakter heeft het type `char` en wordt voorgesteld tussen
single quotes (`'`).

```
char x = 'x';
char a = 'a';
```

## ASCII en Unicode

Voor een computer worden karakters gewoon voorgesteld door getallen.
Van oudsher wordt hiervoor de ASCII-tabel gebruikt.
Tegenwoordig gebruiken we de Unicode-tabel.

De `UTF-8`-Unicode-codering is *backwards compatible* met de `ASCII`-tabel.

Zie https://nl.wikipedia.org/wiki/ASCII_(tekenset)

> We gebruiken soms liever de **hexadecimale** voorstelling.
> Dit kan in C# met het prefix `0x`.
> Een getal weergeven als hexadecimaal kan met de juiste format-string.

```
int a = 0x3;
int b = 0xa; // 0xA = 10
Console.WriteLine(a + b); // resultaat wordt in decimaal
Console.WriteLine("{0:X}"); // resultaat in hexadecimaal
```

## Voorbeeld

https://dotnetfiddle.net/6QqPMP



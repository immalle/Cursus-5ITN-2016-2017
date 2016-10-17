# Argumenten en overloads

In deze code

```
Console.WriteLine("Hallo");
```

wordt de method `WriteLine` aangeroepen met als argument de string `"Hallo"`.

Wanneer er meerdere methodes zijn met **dezelfde naam** maar met een
**ander aantal parameters** spreken we van **overloads**.

Voor `WriteLine` zijn er verschillende **overloads** gedefinieerd.
Je kan `WriteLine` ook aanroepen met een `int` of `double` als argument:

```
Console.WriteLine(3);
Console.WriteLine(4.0);
```

In dit screenshot zie je hoe de 11e van de 19 overloads van `Console.WriteLine`
wordt geslecteerd :

![Method Overloads in VS](img/MethodOverloadsInVS.png)

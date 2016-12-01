# Legende

- :hash: `x` : dit komt aan bod in hoofdstuk `x` van het handboek
- :pushpin: : dit zou je volledig moeten beheersen
- :rocket: : hier moet je momenteel op oefenen
- :checkered_flag: : dit komt aan bod op de volgende test

# Allerlei

- [Begrippenlijst : Allerlei](Begrippenlijst/Allerlei.md)
- [Speciale karakters : naamgeving + ASCII-code](Begrippenlijst/SpecialeKarakters.md)

# Excel

- :pushpin: [Cell Formatting / Celweergave (b.v. percentages)](Excel/CellFormatting.md)

# Visual Studio (Code)

- :rocket: [Commando's in VS Code](VS/VSCodeCommands.md) 

# VirtualBox

- :rocket: [VirtualBox basisconfiguratie](VirtualBox/Basis.md)

# Linux

- :rocket: [Linux basis-commando's](Linux/BasicCmds.md)
- :rocket: [Linux directory structuur](Linux/Directories.md)
- :rocket: [Apt repositories en `.deb`-files](Linux/Apt.md)
- :rocket: [PATH omgevingsvariabele](Linux/Path.md)
- :rocket: [XFCE Window Manager tips](Linux/Xfce.md)

# Git en GitHub

- :rocket: Een repository maken op GitHub
- :rocket: Een GitHub-repository clonen met SourceTree
- :rocket: Een issue oplossen op GitHub met een juiste commit-tekst
- :rocket: Een bestaande repository toevoegen aan SourceTree
- :rocket: Bestaande repositories updaten (pull)
- :rocket: Bestaande GitHub-repositories updaten (push)
- :rocket: Een branch maken in SourceTree
- :rocket: Commits maken op verschillende branches met SourceTree en Visual Studio Team Explorer
- :rocket: Titels, opsommingen en code-fragmenten in markdown opmaken op GitHub
- :rocket: Links leggen naar andere mappen of markdown-bestanden in markdown op GitHub

# CSharp

## Types van variabelen

Primitieve types:

- :pushpin: (:hash: 4)  [Variabelen declareren](CSharp/Vars.md)
- :pushpin: (:hash: 4)  [Gehele getallen (`int`)](CSharp/VarsInt.md)
- :pushpin: (:hash: 4)  [Komma-getallen (`double`)](CSharp/VarsDouble.md)
- :pushpin: (:hash: 7) [Boolean (`bool`)](CSharp/VarsBool.md)
- :rocket: (:hash: 16) [Karakters (`char`)](CSharp/VarsChar.md)

Objecten:

- :rocket: (:hash: 16) [Karakterreeksen (`string`)](CSharp/VarsString.md) 
- :rocket: (:hash: 3) [WPF Objecten en constructors](CSharp/WPFObjects.md)
- :construction: [Objecten](CSharp/Objects.md) 
- Enums
- Structs (*Value-types*)
- Classes (*Reference-types*)
	- (:hash: 10) classes maken
	- (:hash: 11) overerving (inheritance)
	- abstracte classes
	- (:hash: 23) interfaces

Overige:

- Converteren van types (**casten**) (b.v. `Convert.ToChar(...)` of `(char)`)

## Operatoren

- :pushpin: (:hash: 4) [Toekenningsoperator](CSharp/Toekenningsoperator.md) 
- :pushpin: (:hash: 7) [Vergelijkingsoperatoren](CSharp/Vergelijkingsoperatoren.md) 

## Controlestructuur : selectie

- :pushpin: (:hash: 7) [if/then/else](CSharp/IfThenElse.md) 
- :pushpin: (:hash: 7) [Oefeningen if/then/else](CSharp/IfThenElseOef.md)
- :pushpin: (:hash: 7) [switch/case](CSharp/SwitchCase.md) 

## Controlestructuur : loops

- :pushpin: (:hash: 8) [`while`- en `for`-loops](CSharp/Loops.md)

## Controlestructuur : exceptions

- (:hash: 17) Exceptions

## Datastructuren

- :rocket: (:hash: 13) [Generieke lijst `List<T>`](CSharp/DatastructList.md)
- (:hash: 14) arrays
- (:hash: 15) 2D-arrays
- Dictionary / HashMap / Key-Value-structuur

## Format strings

- :pushpin: (:hash: 4) [Eenvoudige format strings](CSharp/SimpleFormatStrings.md) 
- [Geavanceerde format strings en cultuurgebonden instellingen](CSharp/AdvancedFormatStrings.md)

## Methodes

- :pushpin: (:hash: 5) [Methodes aanroepen](CSharp/MethodesAanroepen.md)
- :pushpin: (:hash: 5) [Methodes : overloads](CSharp/MethodesOverloads.md)
- :pushpin: (:hash: 5) [Methodes schrijven](CSharp/MethodesSchrijven.md)
- :pushpin: (:hash: 5) [Parameters toevoegen aan methodes](CSharp/MethodesParameters.md)
- :pushpin: (:hash: 5) [Optionele parameters](CSharp/MethodesOptioneleParameters.md)
- :pushpin: (:hash: 5) [Overloads van zelf geschreven methods](CSharp/MethodesSchrijvenOverloads.md) 
- :pushpin: (:hash: 5) [Methodes met return-waarden schrijven](CSharp/MethodesReturn.md) 
- :pushpin: (:hash: 5) [Compiler-fouten : code-paden](CSharp/MethodesCodePaths.md) 
- :pushpin: (:hash: 5) [Code-paden bij void-methods](CSharp/MethodesVoid.md) 

## Scope

- :rocket: (:hash: 6) [Scope van lokale en class-variabelen](CSharp/ScopeVars.md) 
- [Scope van methods en variabelen uit verschillende classes](CSharp/ScopeInterClass.md)
- :rocket: (:hash: 6) [Namespaces en `using`](CSharp/Namespaces.md) 

## Uitgelichte classes en structs

CSharp

- :pushpin: [Math functies](CSharp/MethodesAanroepen.md#math-functies)
- :rocket: (:hash: 6) [`Random`-class](CSharp/Random.md)
- :rocket: (:hash: 6 (oef)) [`DateTime` en `TimeSpan`](CSharp/DateTime.md)
- :pushpin: [Console-class : basis](CSharp/Console.md)
- Console-class : cursor verplaatsen
- Console-class : `Console.ReadKey()` en de `ConsoleKeyInfo`-struct
- Classes i.v.m. bestanden en directories uit `System.IO` (`File`, `Directory`, ...)


WPF

- :rocket: (:hash: 2, 18) `MessageBox`
- :rocket: (:hash: 6) `Window` 
- :rocket: (:hash: 6) `Slider` 
- :rocket: (:hash: 6) `DispatcherTimer`
- :rocket: (:hash: 7) `CheckBox`
- :rocket: (:hash: 7) `RadioButton`

## Voorbeelden

- :pushpin: [Het retour-geld van een drankautomaat berekenen m.b.v. een functie](CSharp/Drankautomaat.md) 
- :rocket: Het spel Hoger/Lager (raad het random getal)

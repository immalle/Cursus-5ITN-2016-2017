# Legende

- :hash: `x` : dit komt aan bod in hoofdstuk `x` van het handboek
- :pushpin: : dit zou je volledig moeten beheersen
- :rocket: : hier moet je momenteel op oefenen
- :checkered_flag: : dit komt aan bod op de volgende test
- :bangbang: : nog niet gevraagd op een test maar kan wel op het PW voorkomen

# Allerlei

- [Begrippenlijst : Allerlei](Begrippenlijst/Allerlei.md)
- [Speciale karakters : naamgeving + ASCII-code](Begrippenlijst/SpecialeKarakters.md)

# Excel

- :pushpin: [Cell Formatting / Celweergave (b.v. percentages)](Excel/CellFormatting.md)

# Visual Studio Code en .Net Core in Xubuntu via VirtualBox

- :rocket: [VirtualBox basisconfiguratie](VirtualBox/Basis.md)
- :rocket: [Commando's in VS Code](VS/VSCodeCommands.md)

zie ook:

- https://gitter.im/5ITN-immalle/Chatbox/archives/2016/11/14
- https://www.microsoft.com/net/core : .Net Core
- https://code.visualstudio.com/ : Visual Studio Code
- http://lmgtfy.com/?q=virtualbox+tutorial

# Linux

- :rocket: [Linux basis-commando's](Linux/BasicCmds.md)
- :rocket: [Linux directory structuur](Linux/Directories.md)
- :rocket: [Apt repositories en `.deb`-files](Linux/Apt.md)
- :rocket: [PATH omgevingsvariabele](Linux/Path.md)
- :rocket: [XFCE Window Manager tips](Linux/Xfce.md)

# Powershell

- :rocket: [Installatie en controleren van de versie](Powershell/InstallatieVersie.md)
- :rocket: [De Powershell ISE werkomgeving](Powershell/Werkomgeving.md)
- :rocket: [Enkele commando's](Powershell/EnkeleCommandos.md)
- :rocket: [Parameters meegeven](Powershell/Parameters.md)
- :rocket: [Commando's combineren met `|` en de OOP-Shell](Powershell/Commandos.md)
- :rocket: [Variabelen](Powershell/Variabelen.md)

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
- :bangbang: (:hash: 16) [Karakters (`char`)](CSharp/VarsChar.md)

Objecten:

- :bangbang: (:hash: 16) [Karakterreeksen (`string`)](CSharp/VarsString.md) 
- :pushpin: (:hash: 3) [WPF Objecten en constructors](CSharp/WPFObjects.md)
- :construction: [Objecten](CSharp/Objects.md) 
- Enums
- Structs (*Value-types*)
- Classes (*Reference-types*)
	- (:hash: 10) [Classes](CSharp/Classes)
	- (:hash: 11) [overerving (inheritance) + abstracte classes](CSharp/Overerving)
	- (:hash: 23) interfaces

Overige:

- :rocket: Converteren van types (**casten**) (b.v. `Convert.ToChar(...)` of `(char)`)

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

- :bangbang: (:hash: 13) [Generieke lijst `List<T>`](CSharp/DatastructList.md)
- (:hash: 14) arrays
- (:hash: 15) 2D-arrays
- Dictionary / HashMap / Key-Value-structuur
- Stack
- Queue

## Format strings

- :pushpin: (:hash: 4) [Eenvoudige format strings](CSharp/SimpleFormatStrings.md) 
- :bangbang: [Geavanceerde format strings en cultuurgebonden instellingen](CSharp/AdvancedFormatStrings.md)

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

## Classes

- :pushpin: (:hash: 10) [Oef. hst. 10](CSharp/OefHst10.md)
- :pushpin: [Tutorial: zelf classes schrijven](CSharp/classes)
- :rocket: [Interface : introductie](CSharp/InterfacesIntro.md)

## Scope

- :pushpin: (:hash: 6) [Scope van lokale en class-variabelen](CSharp/ScopeVars.md) 
- [Scope van methods en variabelen uit verschillende classes](CSharp/ScopeInterClass.md)
- :pushpin: (:hash: 6) [Namespaces en `using`](CSharp/Namespaces.md) 

## Uitgelichte classes en structs

CSharp

- :pushpin: [Math functies](CSharp/MethodesAanroepen.md#math-functies)
- :bangbang: (:hash: 6) [`Random`-class](CSharp/Random.md)
- :bangbang: (:hash: 6 (oef)) [`DateTime` en `TimeSpan`](CSharp/DateTime.md)
- :pushpin: [Console-class : basis](CSharp/Console.md)
- Console-class : cursor verplaatsen
- Console-class : `Console.ReadKey()` en de `ConsoleKeyInfo`-struct
- Classes i.v.m. bestanden en directories uit `System.IO` (`File`, `Directory`, ...)
- [Timers, system sounds en Speech Synthesizer](TimerSoundsSpeech.md)

WPF

- :bangbang: (:hash: 2, 18) `MessageBox`
- :bangbang: (:hash: 6) `Window` 
- :bangbang: (:hash: 6) `Slider` 
- :bangbang: (:hash: 6) `DispatcherTimer`
- :bangbang: (:hash: 7) `CheckBox`
- :bangbang: (:hash: 7) `RadioButton`
- :bangbang: Panels: `Canvas`, `WrapPanel`, `StackPanel`, `GridPanel` (http://wpftutorial.net/Layout.html)
- :rocket: (:hash: 13) [`ListBox`](WPF/ListBox.md)

## Code lezen

- :bangbang: [Waarom en hoe code lezen?](CSharp/LezenIntro.md)
- :bangbang: [Lezen van expressies met variabelen](CSharp/LezenVars.md)
- :bangbang: [Lezen van method-aanroepen en -definities](CSharp/LezenMethods.md)
- :bangbang: [Lezen van object members (constructors, methods, properties)](CSharp/LezenObjects.md)
- Lezen van classes

## Voorbeelden van algoritmen

- :bangbang: [Dagen, uren, minuten en seconden omzetten naar seconden](CSharp/Voorbeelden/NaarSeconden.md)
- [Seconden omzetten naar uren, minuten en seconden](CSharp/Voorbeelden/NaarUrenMinutenSeconden.md)
- :pushpin: [Het retour-geld van een drankautomaat berekenen](CSharp/Voorbeelden/Drankautomaat.md)
- :pushpin: [Het spel Hoger/Lager (raad het random getal)](CSharp/Voorbeelden/HogerLager.md)
- :bangbang: [Tijdsmetingen / profilen van algoritmen](CSharp/Voorbeelden/Tijdsmeting.md)
- [Animated GIF omzetten naar ASCII en afbeelden op console](CSharp/Voorbeelden/AnimatedASCIIArt.md)

## Oefeningen (algoritmen)

- :rocket: [C# Interactive](CSharp/CSharpInteractive.md)
- binary AND/OR/XOR
- rotate text string

## Online Oefeningen

- Project Euler
- Rosalind
- Exercism ([Instructies](Exercism.md))
- CodinGame
- ...

# Exercism

Alle info is ook op de site van Exercism te vinden.

Enkel om de tests te runnen, moet je weten hoe je de NUnit-dependency kan installeren en gebruiken.

Toch volgt hier wat extra uitleg.

## Vanuit Windows en Visual Studio

### Set-Up

- Installeer chocolatey
	- vanuit Powershell
	- `Set-ExecutionPolicy -ExecutionPolicy Unrestricted` of zie *Windows Instellingen* -> *Voor ontwikkelaars*
	- zie https://chocolatey.org/install
- Installeer de exercism CLI-tool
	- zie http://exercism.io/cli/windows
	- `choco install exercismio-cli`
- Download het Visual Studio project van Exercism
	- zie http://exercism.io/languages/csharp/installing
	- clone de repo https://github.com/rprouse/Exercism.VisualStudio b.v. in `c:\workcsharp` (de directory waar je CSharp projecten staan)
	- Open de solution
	- Installeer de NUnit-dependency van het project : rechts-klik op solution en *restore NuGet packages"
	- Installeer NUnit Test Runner : Tools -> Extension and Updates -> Online -> `NUnit Test Adapter` (**niet** `NUnit 3 Test Adapter)
- Configureer de exercism CLI-tool
	- gebruik de directory van het VS project! :
	  `exercism configure --dir c:\workchsarp\Exercism.VisualStudio`
	- configureer je eigen key!
	- controleer met `exercism configure`

### Gebruik

- fetch een oefening
- druk op de *show all files*-button in de solution explorer
- rechts-klik op de map v.d. oef. om te includen in het project
- kies Run All Tests (`CTRL-R A`)
- maak eventueel een commit (je zit wel in de clone van de exercism repo te werken)
- submit een oefening

## Vanuit Linux met dotnet core

### Set-Up

- installatie
	- zie http://exercism.io/cli/linux
	- exercism executable downloaden en in juiste map zetten
	- `$PATH` aanpassen zodat de executable overal kan uitgevoerd worden
- Configuratie
	- kies een map voor de exercism oefeningen
	- `exercism configure --dir /home/imma/exercism`
	- vergeet je persoonlijke exercism key niet te configureren!
	- controleer je instellingen met `exercism configure`

### Gebruik

> Dit is EEN mogelijke manier!

- fetch een oef.
- ga naar de directory en maak een nieuw dotnet core project met `dotnet new`
- bewerk `project.json` zodat de NUnit-dependency geconfigureerd is 
  (of kopieer de file uit een voorgaand project)

```
{
    "version": "1.0.0-*",

    "dependencies": {
        "NUnit": "3.5.0",
        "dotnet-test-nunit": "3.4.0-beta-3"
    },

    "testRunner": "nunit",

    "frameworks": {
		...
    }
}
```

- voer de tests uit `dotnet test`
- submit een oef.

# Booleans

Booleaanse variabelen hebben 2 toestanden:

- true
- false

Declaratie en initialisatie:

```
bool klaar = true;
bool gameOver = false;
```

## Rekenkundige operatoren

Het *rekenen* met booleaanse variabelen noemen we Booleaanse Algebra.


| operator | omschrijving                  | voorbeeld                |
|---|---|---|
| `&&`     | logische AND van 2 variabelen | `bool b = true && false` |
| `||`     | logische OR van 2 variabelen | `bool b = true |   | false` |
| `!`      | logische NOT van 1 variabele  | `bool b = !true |

## Voorbeelden

Een Boolean kan *getoggled* worden met de NOT-operator:

```
bool gameOver = false;
gameOver = !gameOver; // toggle
```

Een vergelijkingsoperatie returnt een Boolean:

```
bool heating = false;
double setTemperature = 20.5;
double measuredTemperature = 19;
bool heating = setTemperature > measuredTemperature; // "schakel de verwarming aan als ..."
```

Een waarschuwingssysteem in een auto voor gladde wegen kan een logische AND doen van 2 sensor-inputs:

```
bool koud = false;
bool rijdend = false;

if(koud && rijdend) {
  waarschuwChauffeur(); // method die b.v. een geluidssignaal afspeelt en een display op het dashboard update
}
```

Een oneindige lus (het programma zal op een andere manier of met `break;` moeten afgesloten worden):

```
bool koud = false;
bool rijdend = false;

startAuto();

while(true) {
  if(rijdend && koud) {
    waarschuwChauffeur();
  } else if(!rijdend) {
    break;
  }
}
```
maar de `while`-loop kunnen we ook zo schrijven:

```
while(rijdend) {
  if(koud) {
    waarschuwChauffeur();
  }
}
```

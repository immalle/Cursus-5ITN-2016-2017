# Selectie

Een basis-programmeerstructuur is de **selectie**:
op basis v.e. voorwaarde slaat het programma een *andere weg* in.

Er zijn vaak meerdere mogelijke wegen ("code paths").

> Bij het testen v.e. programma moeten eigenlijk alle *code paths* uitgetest
zijn vooraleer je zeker kan zijn dat er geen run-time fouten zullen optreden.



## if-else

```
if(x > 3) {

} else {

}
```



## if-elseif-else

Je kan zo veel `else if`'s toevoegen als je wil:

```
if(x > 3) {

} else if( x < 21) {

} else if( x < 80) {

}
```

> Denk eraan dat de tests steeds sequentieel (van boven naar onder) doorlopen
> worden. Denk zelf na hoe dat in bovenstaand voorbeeld misschien anders
> uitdraaid dan je op het eerste zicht zou denken.


## switch/case

Als je zeer veel `else if`'s nodig hebt, kan het handiger zijn een
`switch` te gebruiken.


## Oef

### Weekloon

Een normale werkweek bestaat uit 38 uur.
Een arbeider wordt 14 euro per uur betaald.
Voor overuren krijgt hij 35% extra.

Bereken het `weekloon` dat deze arbeider ontvangt 
als hij die week `aantalUur` gewerkt heeft.

Gegeven:

```
int uurloon = 14;
```
  
### Verkoopprijs

Een winkel berekent de `verkoopprijs` v.e. artikel normaal gezien door
simpelweg het dubbele v.d. `inkoopprijs` te nemen.
Als de `verkoopprijs` echter hoger is 40,00 euro, wordt hier 20% van af gedaan.
Als de `verkoopprijs` hoger is dan 80,00 euro, wordt hier 30% van af gedaan.

Dus b.v. gegeven is:

```
double inkoopprijs = 65.00;
```

### Lengtes

3 dingen worden gemeten:

b.v.

- `lengteA = 2.4`
- `lengteB = 4.7`
- `lengteC = 3.8`

Bepaal de `kortste` en de `langste` lengte.


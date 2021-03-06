## Programdesign
### Klassen Node
Klassen skal kunne initiere nye objekter med ønsket minnestørrelse og prosessorantall, og for øvrig tilby tjenester (metoder) som trengs i andre deler av programmet.
### Klassen Rack
Klassen Rack skal lagre Node-objektene som hører til et rack i en liste. Vi skal kunne legge til noder i racket hvis det er færre enn maks antall noder der fra før. For enkelhets skyld skal vi
anta at hvert rack i dataklyngen har plass til like mange noder. Opprett andre instansvariable og metoder etter behov.
### Klassen Dataklynge
Klassen Dataklynge skal holde rede på en liste med racks, og må tilby en metode som tar imot et nodeobjekt og plasserer det i et rack med ledig plass. Hvis alle rackene er fulle, skal det lages
et nytt Rack-objekt som legges inn i listen, og noden plasseres i det nye racket. *Tips: Det kan være lurt å ta inn antall noder per rack i konstruktøren til Dataklynge.*

## 1. Klasser
Skriv klassene beskrevet under “Programdesign”. Der det ikke er oppgitt hva slags datatype som skal brukes (for eksempel ved valg av listetype) forventes det at du selv gjør fornuftige valg og begrunner disse gjennom kommentarer i koden.

## 2. Antall prosessorer og minnekrav
Lag en metode antProsessorer i Dataklynge som returnerer det totale antall prosessorer i dataklyngen. 

Noen programmer trenger mye minne, typisk et gitt antall GB med minne på hver node vi bruker. Vi er derfor interessert i å vite hvor mange noder som har nok minne til at vi kan bruke dem. Lag en metode noderMedNokMinne(int paakrevdMinne) i Dataklynge som returnerer antall noder med minst paakrevdMinne GB minne. 

Utvid klassene Node og Rack slik at de støtter implementeringen av disse metodene.

## 3. Hovedprogram
Skriv en klasse Hovedprogram med en main-metode for å teste at klassene virker som de skal. Lag en dataklynge, abel, og la det være plass til 12 noder i hvert rack. Legg inn 650 noder med 64 GB minne og en prosessor hver. Legg også inn 16 noder med 1024 GB minne og to prosessorer.

Sjekk hvor mange noder som har minst 32 GB, 64 GB og 128 GB minne. Finn totalt antall prosessorer, og sjekk hvor mange rack som brukes. Skriv ut svarene i terminalen. 

##  Lese fra fil
Skriv en ny konstruktør til klassen Dataklynge. Denne skal ha et filnavn som parameter (i stedet for max antall noder per rack), og lese alle data om dataklyngen fra fil. Filen er bygget opp slik at første linje beskriver antall noder per rack, mens de neste linjene beskriver hvor mange noder, med hvor mye minne og antall prosessorer som skal settes inn.

Endre hovedprogrammet fra deloppgave D slik at du oppretter en dataklynge med data fra filen "dataklynge.txt" (som vist over) før det gjør beregningene beskrevet i deloppgave D). Test gjerne med flere variasjoner av data i filen og sjekk at du får riktig resultat.

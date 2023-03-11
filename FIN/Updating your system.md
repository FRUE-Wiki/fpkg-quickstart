# Järjestelmä päpivyttyneenäpitäminen on tärkeää. FPKG tekee tästä helppoa

## Järjestelmän päivittäminen tavallisesti.
Void hakea uudet hakemistot näin:
```
# fpkg -up
```
`-u`-vaihtoehto päivittää ja '-p' käskee `-u`:ta päivittämään hakemistot. Älä koskaan käytä `-p`:tä itsekseen.

Ja kaikkien pakettien päivittämiseen:
```
# fpkg -ui
```
`-i`-vaihtoehto `-u`:n kanssa päivittää kaikki paketit.

*Ekspertit saattavat haluta tsiigata tämän [[Updating individual packages]]*

*Kotisivulle: [[FPKG Quick Start Guide]]*

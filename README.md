# Project 2021-2022 (Juni)

## Deadlines

De opdracht en/of deelopdrachten worden ingeleverd voor deadlines die hieronder beschreven staan. Een te late submissie wordt niet verbeterd.

1. Onderwerp opdracht invullen in excel. Deadline: 23:59 CEST 9 Maart 2022.
2. Demo webapp. Deadline: 23:59 CEST 22 Mei 2022.

Time management is **jouw** verantwoordelijkheid.

---

## Rules

* Algemene informatie vind je terug in de [studiewijzer](https://github.com/ucll-internet-programming-major/algemene-info).
* Er wordt gebruik gemaakt van GitHub Classroom. De link komt op Toledo.
* Tijdens het examen zal je een extra functionaliteit aan je applicatie moeten toevoegen. Zorg dat je applicatie eenvoudig uitgebreid kan worden.
* Omdat het project een onderdeel is voor de evaluatie van dit vak, is het examenreglement hierop van toepassing. Schrijf dus je eigen oplossing!
* Heb je problemen met je project kan je altijd vragen stellen tijdens de les. Mails met vragen zullen onbeantwoord blijven.

---

## Opgaves

### Onderwerp kiezen

Je kiest zelf een onderwerp voor je project. Dit vul je aan in deze [excel](https://ucll-my.sharepoint.com/:x:/g/personal/u0124976_ucll_be/EZ5NXKjRKSNCnNJnuj4-RRMBcPGWbwJ8ikeZdO-s_9Imow?e=hun58k) en toets je samen met de lector af. 

Voorwaarden (db design):

* De applicatie gebruikt 1 of meerdere n:m (many to many) relationships.
* De Excel is voor de deadline ingevuld & bij de lector afgetoest

### Voorbeeld onderwerpen

TODO

### Inhoudelijk

Afhankelijk van jullie onderwerp, zal natuurlijk de applicatie verschillend zijn van elkander. Voorzie het volgende in jullie applicatie:

* De repository van de applicatie is opgezet volgens de best practices
  * Geen project map in het root path van de repository
  * Geschikte .gitignore. Gebruik hiervoor [gitignore.io](gitignore.io).
  * Gecompileerde bestanden worden niet op GitHub gezet.
  * De README.md bevat instructies over hoe het project opgezet kan worden (dev modus - geen productie builds)
  * Wachtwoorden voor publieke services staan **NIET** in plaintext op jullie repository. Dit is een grote security breach en wordt ook zo gepenaliseerd. Gebruik hiervoor environment variabelen. Bij twijfel, contacteer de lector. _(lokale wachtwoorden mogen in je config files staan. Bijv. default postgres username & wachtwoord voor je docker image.)_
* De applicatie heeft authenticatie
* De applicatie heeft authorizatie
* De applicatie ondersteunt i18n
* De applicatie is veilig
* De applicatie is volgens design principes gemaakt dat in de les werd afgesproken
* De applicatie bevat onderwerp-specifieke pagina's.
* De applicatie wordt volgens best-practices gemaakt (algemene clausule). Enkele voorbeelden van bad-practices:
  * crashes op pagina's of na specifieke flows
  * geen error messages
  * links die niet werken
  * assets die niet laden
  * ... Dit is geen exhaustieve lijst, bij twijfel kan je de lector hier op voorhand over aanspreken tijdens de les.
* Er wordt gebruik gemaakt van esbuild om bepaalde Javascript op specifieke pagina's te tonen.

### Demo

De code wordt ingeleverd via GitHub classroom. Bij de voorstelling van het project moet de student in 20 minuten een volledige demonstratie kunnen geven. Er wordt **geen** powerpoint verwacht, enkel een demo. Deze demo wordt opgenomen.

Het project wordt van scratch gecloned van GitHub. We verwachten dat je met een git clone commando klaar staat.

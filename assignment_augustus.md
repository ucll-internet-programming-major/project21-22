# Project 2021-2022 (Augustus)

## Deadlines

GitHub Classroom link: [https://classroom.github.com/a/VKhdrpl6](https://classroom.github.com/a/VKhdrpl6)

De opdracht en/of deelopdrachten worden ingeleverd voor deadlines die hieronder beschreven staan. Een te late submissie wordt niet verbeterd.

1. Onderwerp opdracht & Database schema op repo zetten. Deadline: 23:59 CEST 14 Augustus 2022.
2. Demo webapp. Excel met time slots volgt nog.

Time management is **jouw** verantwoordelijkheid.

---

## Rules

* Algemene informatie vind je terug in de [studiewijzer](https://github.com/ucll-internet-programming-major/algemene-info).
* Er wordt gebruik gemaakt van GitHub Classroom. De link komt op Toledo.
* Tijdens het examen zal je een extra functionaliteit aan je applicatie moeten toevoegen. Zorg dat je applicatie eenvoudig uitgebreid kan worden.
* Omdat het project een onderdeel is voor de evaluatie van dit vak, is het examenreglement hierop van toepassing. Schrijf dus je eigen oplossing!
* Heb je problemen met je project kan je altijd vragen stellen tijdens de les. Mails met vragen zullen onbeantwoord blijven.
* Er kan enkel een punt (voor het project) bekomen worden indien je je applicatie voorstelt tijdens het demo moment.

---

## Opgaves

### Onderwerp kiezen

Je kiest zelf een onderwerp voor je project. Dit zet je in je Readme met een beknopte uitleg. _Let op: je projectscope moet complex genoeg zijn. Dit betekent dus dat er minstens 4 betekenisvolle tabellen in je database aanwezig zijn, waarboven je onderstaande features moet implementeren._

Voorwaarden (db design):

* De applicatie gebruikt 1 of meerdere n:m (many to many) relationships.
* Minstens 4 betekenisvolle tabellen (e.g. gebouw, reservatie, user, foto-informatie, ...)

### Voorbeeld onderwerpen

* Webshop
* Online ToDo takenlijst (waarbij takenlijst gedeeld kan worden door meerdere gebruikers)
* Social media kanaal (Waarbij mensen elkaar kunnen volgen)
* Evenementen kalender
* ...

### Inhoudelijk

Afhankelijk van jullie onderwerp, zal natuurlijk de applicatie verschillend zijn van elkander. Voorzie het volgende in jullie applicatie:

* De repository van de applicatie is opgezet volgens de best practices
  * Geen project map in het root path van de repository
  * Geschikte .gitignore. Gebruik hiervoor [gitignore.io](gitignore.io).
    * __LET OP: de versie op gitignore.io is voor v1.5, de huidige Phoenix versie is 1.6 . Clone je eigen repo en zie of je applicatie nog werkt zoals verwacht.
  * Gecompileerde bestanden worden niet op GitHub gezet.
  * De README.md bevat instructies over hoe het project opgezet kan worden (dev modus - geen productie builds)
  * Wachtwoorden voor publieke services staan **NIET** in plaintext op jullie repository. Dit is een grote security breach en wordt ook zo gepenaliseerd. Gebruik hiervoor environment variabelen. Bij twijfel, contacteer de lector. _(lokale wachtwoorden mogen in je config files staan. Bijv. default postgres username & wachtwoord voor je docker image.)_
* De applicatie is opgebouwd volgens de umbrella structuur
* De applicatie heeft authenticatie __en registratie__
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
* De applicatie heeft de onderstaande extensie
* Er wordt een publieke en private API voorzien die gebruikers kunnen raadplegen. Gebruikers kunnen API keys genereren en op **een veilige manier** meesturen naar de beveiligde API.

### Extensie: server metrics

De applicatie houdt server metrics bij. Deze informatie is enkel voor browser-gerelateerde activiteiten (niet je API). Deze informatie omvat:

* Pad van de request zonder GET request parameters
* Type request (GET / POST / PUT / PATCH / ...)
* Hoe vaak een bepaalde user het pad heeft bezocht
* Is de user niet ingelogd, mag dit null zijn

Voorbeeld data (fictieve CSV export):

```
path;request-type;user;n-visits;
/home;GET;;99
/home;GET;wannes;1
/logout;POST;wannes;5
...
```

Visualisatie van de data wordt enkel voorzien voor mensen met de `Admin` rol of `Business Analyst` rol. Deze gebruikers kunnen de data zien op `business-analyst/statistics/` waar ze volgende informatie zien:

```
/home              GET           100         details
/logout            POST           55         details
...
```

Wanneer je op de details knop drukt, zie je een overzicht van wie het path heeft bezocht (en hoeveel keer). Toon meer dan enkel de user zijn id (naam/ e-mail). Bij het verwijderen van een user mogen de server metrics mee verwijderd worden.

Hou rekening met queries en performantie. _Ter verduidelijking: De overzichtspagina toont __geen__ user-gerelateerde info, dit is pas zichtbaar vanaf je naar de detail pagina gaat._

### Demo

De code wordt ingeleverd via GitHub classroom. Bij de voorstelling van het project moet de student in 20 minuten een volledige demonstratie kunnen geven. Er wordt **geen** powerpoint verwacht, enkel een demo en bijhorende documentatie.

Het project wordt van scratch gecloned van GitHub. We verwachten dat je met een git clone commando klaar staat.

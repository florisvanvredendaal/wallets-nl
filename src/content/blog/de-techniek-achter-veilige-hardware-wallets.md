---
title: "De techniek achter veilige hardware wallets"
description: "Hardware wallets zijn in de regel veiliger dan software wallets of online wallets. Daarom zijn hardware wallets de afgelopen jaren flink populairder geworden. E"
pubDate: "2018-12-12T21:04:52"
updatedDate: "2018-12-12T21:05:59"
author: "wallets"
heroImage: "https://www.wallets.nl/wp-content/uploads/2018/12/techniek-hardware-wallets.jpg"
categories:
  - "Algemeen"
slug: "de-techniek-achter-veilige-hardware-wallets"
draft: false
---

Hardware wallets zijn in de regel veiliger dan software wallets of online wallets. Daarom zijn hardware wallets de afgelopen jaren flink populairder geworden. Er wordt veel geschreven over dat hardware wallets de voorkeur hebben, maar de technische reden blijft vaak achterwege.

Sommige hardware wallets hebben een beveiligd besturingssystemen dat door een eigen team wordt ontwikkeld. Een goed voorbeeld daarvan is bijvoorbeeld [de Ledger Nano S](https://www.wallets.nl/ledger/nano-s/). Ledger heeft een Secure Element chip en daarvoor een eigen beveiligd besturingssysteem ontwikkeld. Dat systeem heet BOLOS en heeft speciale functies om een hardware wallet nog veiliger te maken. Wallets.nl dook in de beveiliging van [verschillende hardware wallets](/kopen). In deze blog leggen we uit hoe de techniek achter de beveiliging werkt.

## Een Secure Element chip

Als je een [hardware wallet](/) hebt, wil je uiteraard dat je cryptovaluta zo goed mogelijk beschermd zijn tegen cybercriminelen en verlies van cryptovaluta. Daarom maken hardware wallets gebruik van een microcontroller. Het is namelijk vrij ingewikkeld om de beveiliging van een hardware wallet op orde te krijgen. Een microcontroller is goed te vergelijken met bijvoorbeeld een processor in een smartphone of tablet.

Omdat hardware wallets qua formaat vaak te vergelijken zijn met een creditcard of USB-stick, is er maar beperkte ruimte om een beveiligingschip in te bouwen. Een microcontroller is om die reden veel kleiner dan een gebruikelijke chip. Een microcontroller wordt een MCU genoemd. Daarvan zijn er ruwweg twee soorten.

Ten eerste bespreken we de niet-beveiligde MCU-chip. Die wordt vaak gebruikt in bijvoorbeeld een magnetron of een afstandsbediening. Deze MicroController Unit is vrij goedkoop in de aanschaf en heeft geen uitgebreide beveiligingsfuncties.

De andere, beveiligde MCU-chip vinden we niet alleen terug in hardware wallets, maar bijvoorbeeld ook in betaalpassen en simkaarten. Het gaat hier om de gouden chip die op iedere kaart te vinden is. Zo’n MCU-chip wijst op extra veiligheid en heet om die reden een Secure Element genoemd. De SE-chip wordt dus vooral gebruikt als er privacy, geld of identiteitsbeveiliging in het geding is.

### Hoe werkt de Secure Element chip?

Een Secure Element chip hebben we onbewust vaker van dichtbij gezien dan we denken. Het is het goudkleurige plaatje dat op iedere simkaart, paspoort en betaalpas te vinden is. In principe is een Secure Element een geharde microcontroller. Deze chip is streng beveiligd tegen invloeden van buitenaf. Dit is een beveiliging tegen zogenaamde ‘koppelvlakken’, de mogelijkheid om de chip te koppelen aan een extern risico. Op die manier worden aanvallen beperkt. Uiteraard zijn er nog steeds cybercriminelen die de beveiliging proberen te kraken. Ook de Secure Element-chip krijgt het in sommige aanvallen te verduren, maar dit leidt amper tot een succes.

Een Secure Element-chip moet namelijk systemen ervan verzekeren dat er niet mee geknoeid kan worden. Als er geknoeid wordt met een systeem, dan weet de chip dat onmiddellijk. Daarom beschikt de chip over verschillende technische methoden om aanvallen af te slaan. Denk dan bijvoorbeeld aan side channel analysis of fault injection. Dergelijke methodes vinden we bijvoorbeeld terug bij bankpassen, waarbij na een aantal keren de verkeerde code intoetsen de pas geblokkeerd wordt. Hetzelfde geldt voor simkaarten, waarbij men na een aantal foutieve pogingen een PUK-code in moet voeren. Bij een hardware wallet is het wel aan te raden een [pincode te kiezen](https://www.wallets.nl/zo-makkelijk-is-jouw-pincode-te-raden/) die niet voor de hand ligt.

Eigenlijk is een microcontroller te vergelijken met een bouwpakket. Het is vaak eenvoudig om ze in elkaar te zetten, maar ze uit elkaar halen is een stuk moeilijker. Cybercriminelen proberen dergelijke beveiligingen ook te kraken aan de hand van reverse engineering. Dit betekent dat de chip programmatisch wordt aangevallen om zo een pincode te kunnen herleiden. Secure Elements hebben een zeer complex ontwerp waardoor reverse engineering vrijwel onmogelijk is. Het geheugen is zelfs versleuteld met zeer ingewikkelde algoritmes, waardoor de hardware wallet in de praktijk zeer moeilijk te kraken is.

### Certificaten Secure Element

Een Secure Element moet uiteraard echte veiligheid bieden. Een SE-chip is daar speciaal voor ontworpen. Toch moet er een derde externe partij zijn die de veiligheid van iedere chip controleert. Daarom worden er in hardware wallets enkel Secure Elements gebruikt die zijn gecertificeerd. Iedere chip wordt streng gecontroleerd en vervolgens gecertificeerd.

Een Secure Element moet aan bepaalde eisen voldoen om een certificering te ontvangen. Zo moeten de chips steeds worden doorontwikkeld. Wanneer een chip namelijk gehackt kan worden met de nieuwste technieken, dan faalt de chip voor de test. Het hele productieproces van de chips worden bovendien ook streng gecontroleerd. Dat betekent dat van het moment dat de chip geproduceerd wordt, tot het moment dat deze verpakt wordt, altijd onder toezicht staat van een derde partij.

Tenslotte bevat ieder Secure Element een mechanisme, waarmee enkel de fabrikant de chip kan hergebruiken. Het is dus niet mogelijk om als derde partij te knoeien met de chip, bijvoorbeeld door een code te wijzigen. De fabrikant beschikt over speciale hardware en software. Aan de hand van deze manier van produceren kan er niet met de firmware van een chip geknoeid worden. Het is dus praktisch onmogelijk om de chip te manipuleren.

## Afzondering van private keys

Hardware wallets worden in de praktijk vaak gebruikt om private keys mee op te slaan. Op die manier is het mogelijk toegang te krijgen tot cryptovaluta. Uit de private key wordt een public address gegenereerd, die onmogelijk kan worden omgekeerd. Het is dus niet mogelijk vanuit een public key een private key te destilleren.

Dat komt mede doordat alle private keys geïsoleerd worden opgeslagen. De methode waarbij het onmogelijk wordt gemaakt om private keys zonder toegang op te vragen noemen we ‘cold storage’. Private keys zouden nooit online moeten worden opgeslagen. Ze dienen opgeslagen te worden op een apparaat dat geen toegang heeft tot het internet, zoals bijvoorbeeld een hardware wallet.

De private keys worden op de Secure Element opgeslagen. Daardoor staat [de private key](https://www.wallets.nl/private-key/) altijd veilig opgeslagen en kunnen indringers er van buitenaf niet bij.

### Isolatie via BOLOS

Om de SE-chip goed te laten werken, is er een besturingssysteem nodig. Een voorbeeld daarvan is het systeem van [Ledger](/Ledger). De meeste besturingssystemen voor SE-chips zijn oud en niet erg flexibel. Daardoor ondersteunen ze maar een beperkt aantal cryptovaluta.

Fabrikant Ledger voelde zich geroepen om een nieuwe, speciaal beveiligde besturingssysteem te programmeren. Het gaat hier om Blockchain Open Ledger Operating System (BOLOS). Het besturingssysteem is speciaal gebouwd met het oog op beveiliging, maar de flexibiliteit om apps te installeren. Daardoor is het mogelijk meerdere cryptowallets op een hardware wallet te zetten.
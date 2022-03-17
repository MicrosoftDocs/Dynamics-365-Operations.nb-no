---
title: Direkte utligning med fysisk verdi og merking
description: Avveid gjennomsnitt er en lagermodell som er basert på prinsippet for avveid gjennomsnitt, der avganger fra lageret beregnes ut fra gjennomsnittsverdien for varene som mottas i lageret under lagerets periodeavslutning, pluss all lagerbeholdning fra den forrige perioden.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c124716b70be837573506a738ef2034397f2bda
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330232"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Direkte utligning med fysisk verdi og merking

[!include [banner](../includes/banner.md)]

Avveid gjennomsnitt er en lagermodell som er basert på et gjennomsnitt som er resultatet av multipliseringen av hver komponent (varetransaksjon) med en faktor (kostpris) som gjenspeiler viktigheten (antall). Det går også an å si at avveid gjennomsnitt er en lagermodell som tilordner kostnaden ved avgangstransaksjoner basert på middelverdien til all beholdning som er mottatt i perioden, pluss all lagerbeholdning fra den forrige perioden.

Når du kjører en lagerlukking ved hjelp av lagermodellen for avveid gjennomsnitt, kan du opprette en utligning på to måter. Vanligvis utlignes alle kvitteringene mot en virtuell avgang, som holder totalt mottatt antall og verdi. Denne virtuelle avgangen har et korresponderende virtuelt mottak fra der avgangene utlignes. På denne måten får alle avgangene samme gjennomsnittskostnad. Den virtuelle avgangen og mottaket kan vises som en virtuell overføring kalt *overføring av avveid gjennomsnitt fra lagerlukking*. Denne utligningsmetoden kalles en *summert utligning av avveid gjennomsnitt*. Hvis det bare er ett mottak, kan alle avgangene utlignes fra dette, og det opprettes ikke en virtuell overføring. Denne utligningsmetoden kalles en *direkte utligning*. Eventuell lagerbeholdning som er til overs etter at lagerlukkingen er utført, verdsettes til det avveide gjennomsnittet fra forrige periode og tas med i beregningen av avveid gjennomsnitt i neste periode.

Du kan overstyre prinsippet for avveid gjennomsnitt ved å merke lagertransaksjoner slik at et bestemt varemottak utlignes mot en bestemt avgang. En periodisk lagerlukking er nødvendig når du bruker lagermodellen for avveid gjennomsnitt til å opprette utligninger og justere verdien av avganger i henhold til prinsippet for avveid gjennomsnitt. Før du kjører lagerlukkingsprosessen, blir avgangstransaksjoner verdsatt med glidende gjennomsnitt da de fysiske og finansielle oppdateringene fant sted. Med mindre du bruker merking, beregnes glidende gjennomsnitt når den fysiske eller finansielle oppdateringen utføres.

Metoden for avveid gjennomsnittlig lagerlukking beregnes ved hjelp av følgende formel:

- Avveid gjennomsnitt = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = transaksjonsantallet  
P = transaksjonsprisen

Utligninger er lagerlukkingsposteringer som justerer avganger med det avveide gjennomsnittet som gjelder på datoen for lagerlukking. Eksemplene nedenfor viser virkningene når avveid gjennomsnitt brukes i fem forskjellige konfigurasjoner:

- Direkte utligning for avveid gjennomsnitt uten alternativet **Ta med fysisk verdi**
- Summert utligning for avveid gjennomsnitt uten alternativet **Ta med fysisk verdi**
- Direkte utligning for avveid gjennomsnitt med alternativet **Ta med fysisk verdi**
- Summert utligning for avveid gjennomsnitt med alternativet **Ta med fysisk verdi**
- Avveid gjennomsnitt med merking

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Direkte utligning for avveid gjennomsnitt uten Ta med fysisk verdi

Prinsippet for direkte utligning oppretter utligninger direkte mellom mottak og avganger uten å opprette flere lagertransaksjoner. Systemet bruker dette prinsippet for direkte utligning i følgende situasjoner:

- Når én tilgang og én eller flere avganger er postert i perioden.
- Når bare avganger er postert i perioden, og beholdningen inneholder varer fra en tidligere lagerlukking.

I dette eksemplet er det ikke merket av for **Ta med fysisk verdi** i **Varemodellgruppe** for det frigitte produktet. Illustrasjonen nedenfor viser disse transaksjonene:

- 1a. Fysisk lagermottak av et antall på 10 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 10 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 10 til kost USD 20,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 10,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 10,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 4a. Fysisk lageravgang av et antall på 1 til en kostnad på USD 10,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 4b. Økonomisk lageravgang av et antall på 1 til en kostnad på USD 10,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 5a. Fysisk lageravgang av et antall på 1 til en kostnad på USD 10,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 6\. Lagerlukking utføres. Systemet bruker metoden for direkte utligning fordi bare ett mottak blir økonomisk oppdatert i perioden basert på metoden for avveid gjennomsnitt. I dette eksemplet opprettes det én utligning mellom 1b og 3b og en annen mellom 1b og 4b. Det gjøres ingen justering, fordi det glidende gjennomsnittet er det samme som det avveide gjennomsnittet.

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt og prinsippet for direkte utligning uten alternativet **Ta med fysisk verdi**.

![Direkte utligning for avveid gjennomsnitt uten Ta med fysisk verdi.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Nøkkel til diagram**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Hver dato i diagrammet er atskilt med en tynn, svart loddrett linje. Datoen er notert nederst i diagrammet.
- Lagerlukkinger vises med en rød linje med vannrette streker.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Summert utligning for avveid gjennomsnitt uten alternativet Ta med fysisk verdi

Når det forekommer flere mottak i en periode, bruker avveid gjennomsnitt prinsippet for summert utligning der alle mottak i en avslutningsperiode summeres i en ny transaksjon kalt *avveid gjennomsnittlig lagerlukking*. Alle mottakene for perioden blir utlignet mot avgangen til den nylig opprettede lagertransaksjonen. Alle avganger for perioden blir utlignet mot mottaket av den nye lagertransaksjonen. Hvis det er lagerbeholdningsverdi til overs etter lagerlukkingen, tas lagerbeholdningsverdien med i mottakstransaksjonen for transaksjonene for avveid gjennomsnittlig lagerlukking.

Følgende transaksjoner illustreres på figuren som følger:

- 1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
- 2b. Økonomisk lagertilgang av et antall på 1 til kost USD 22,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Fysisk lageravgang av et antall på 1 til kostpris USD 23,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 7\. Lagerlukking utføres.
- 7a. Den økonomiske avgangen Lagerlukkingstransaksjon for avveid gjennomsnitt opprettes for å summere utligningene av alle de økonomiske lagermottakene.
  - Transaksjon 1b utlignes for et antall på 1 med et utlignet beløp på USD 10,00.
  - Transaksjon 2b utlignes for et antall på 1 med et utlignet beløp på USD 22,00.
  - Transaksjon 5b utlignes for et antall på 1 med et utlignet beløp på USD 30,00.
  - Transaksjon 7a. opprettes for et antall på 3 med et utlignet beløp på USD 62,00. Denne transaksjonen motposterer summen av de tre mottakstransaksjonene som oppdateres økonomisk i perioden.
- 7b. Det opprettes en økonomisk tilgang til avveid gjennomsnitt av verdien for lagerlukkingstransaksjonen, som brukes til å utligne økonomisk posterte avganger.
  - Transaksjon 3b utlignes for et antall på 1 med et utlignet beløp på USD 20,67. Denne transaksjonen justeres med USD 4,67 for å få den opprinnelige verdien på USD 16,00 til 20,67, som er det avveide gjennomsnittet av økonomisk posterte transaksjoner for perioden.
  - Transaksjon 7b. opprettes for et antall på 1 med et utlignet beløp på USD 20,67 for å utligne 3b. Denne transaksjonen motposterer summen av den ene avgangstransaksjon som oppdateres økonomisk i perioden.

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt og prinsippet for summert utligning uten alternativet **Ta med fysisk verdi**.

![Summert utligning for avveid gjennomsnitt uten Ta med fysisk verdi.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Nøkkel til diagram**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Hver dato i diagrammet er atskilt med en tynn, svart loddrett linje. Datoen er notert nederst i diagrammet.
- Lagerlukkinger vises med en rød linje med vannrette streker.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Direkte utligning for avveid gjennomsnitt med alternativet Ta med fysisk verdi

Parameteren **Ta med fysisk verdi** fungerer på en annen måte med lagermodellen for avveid gjennomsnitt enn i tidligere versjoner av produktet. Når du velger alternativet **Ta med fysisk verdi** for en vare i skjemaet **Varemodellgruppe**, bruker systemet fysisk oppdaterte mottak når den estimerte avgangskostprisen eller glidende gjennomsnitt beregnes. Avganger blir postert på grunnlag av denne estimerte kostprisen for perioden. I løpet av lagerlukkingen vil bare økonomisk oppdaterte mottak bli vurdert i beregningen av avveid gjennomsnitt.

Følgende transaksjoner illustreres på figuren som følger:

- 1a. Fysisk lagermottak av et antall på 10 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 10 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 10 til kost USD 20,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 15,00 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 15,00 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 4a. Fysisk lageravgang av et antall på 1 til en kostnad på USD 15,00 per stykk (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 4b. Økonomisk lageravgang av et antall på 1 til en kostnad på USD 15,00 per stykk (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 5a. Fysisk lageravgang av et antall på 1 til en kostnad på USD 15,00 per stykk (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 6\. Lagerlukking utføres. Systemet bruker metoden for direkte utligning fordi bare ett mottak blir økonomisk oppdatert i perioden basert på metoden for avveid gjennomsnitt. I dette eksemplet opprettes det én utligning mellom 1b og 3b og en annen mellom 1b og 4b. Transaksjon 3b og 4b blir begge justert med USD −5,00 for å få verdien til USD 10,00.

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt og prinsippet for direkte utligning med alternativet **Ta med fysisk verdi**.

![Direkte utligning for avveid gjennomsnitt med Ta med fysisk verdi.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Nøkkel til diagram**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Hver dato i diagrammet er atskilt med en tynn, svart loddrett linje. Datoen er notert nederst i diagrammet.
- Lagerlukkinger vises med en rød linje med vannrette streker.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Summert utligning for avveid gjennomsnitt med alternativet Ta med fysisk verdi

Parameteren **Ta med fysisk verdi** fungerer på en annen måte med avveid gjennomsnitt enn i tidligere versjoner. Merk av for **Ta med fysisk verdi** for en vare på siden **Varemodellgruppe**. Systemet vil deretter bruke fysisk oppdaterte tilganger under beregning av den estimerte kostprisen eller det glidende gjennomsnittet. Avganger blir postert på grunnlag av denne estimerte kostprisen for perioden. I løpet av lagerlukkingen vil bare økonomisk oppdaterte mottak bli vurdert i beregningen av avveid gjennomsnitt. Det anbefales en månedelig lagerlukking når du bruker lagermodellen for avveid gjennomsnitt. I dette eksemplet med summert utligning av avveid gjennomsnitt, er lagermodellen merket for å ta med fysisk verdi.

Følgende transaksjoner illustreres på figuren som følger:

- 1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
- 2b. Økonomisk lagertilgang av et antall på 1 til kost USD 22,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 16,00 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 16,00 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Fysisk lageravgang av et antall på 1 til kostpris USD 23,67 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 7\. Lagerlukking utføres.
- 7a. Den økonomiske avgangen Lagerlukkingstransaksjon for avveid gjennomsnitt opprettes for å summere utligningene av alle de økonomiske lagermottakene.
  - Transaksjon 1b utlignes for et antall på 1 med et utlignet beløp på USD 10,00.
  - Transaksjon 2b utlignes for et antall på 1 med et utlignet beløp på USD 22,00.
  - Transaksjon 5b utlignes for et antall på 1 med et utlignet beløp på USD 30,00.
  - Transaksjon 7a. opprettes for et antall på 3 med et utlignet beløp på USD 62,00.  
- 7b. Det opprettes en økonomisk tilgang til avveid gjennomsnitt av verdien for lagerlukkingstransaksjonen, som brukes til å utligne økonomisk lukkede avgangstransaksjoner.
  - Transaksjon 3b utlignes for et antall på 1 med et utlignet beløp på USD 20,67. Denne transaksjonen justeres med USD 4,67 for å få den opprinnelige verdien på USD 16,00 til 20,67, som er det avveide gjennomsnittet av økonomisk posterte transaksjoner for perioden.
  - Transaksjon 7b. opprettes for et antall på 1 med et utlignet beløp på USD 20,67 for å utligne 3b.

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt og prinsippet for summert utligning uten alternativet **Ta med fysisk verdi**.

![Summert utligning for avveid gjennomsnitt med Ta med fysisk verdi.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Nøkkel til diagram**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Hver dato i diagrammet er atskilt med en tynn, svart loddrett linje. Datoen er notert nederst i diagrammet.
- Lagerlukkinger vises med en rød linje med vannrette streker.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-with-marking"></a>Avveid gjennomsnitt med merking

Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres.

La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Siden dette er en hasteordre, blir du nødt til å betale en høyere pris for denne varen for å betjene kundens forespørsel. Du må være sikker på at denne lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for denne salgsordrefakturaen.

Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Dette salgsordredokumentet merkes for eksempel mot bestillingen før følgeseddelen eller fakturaen posteres. Vareforbruket vil være USD 120,00 i stedet for det gjeldende glidende gjennomsnittet av varens kost. Hvis bestillingens følgeseddel eller faktura posteres før merkingen skjer, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen.

Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres.

En mottakstransaksjon er merket mot en avgangstransaksjon. Vurderingsmetoden som er valgt for varens varemodellgruppe, ignoreres deretter, og systemet utligner disse transaksjonene mot hverandre.

Du kan merke en avgangstransaksjon mot en tilgang før transaksjonen er postert. Du kan gjøre dette fra en salgsordrelinje på siden **Salgsordredetaljer**. De åpne tilgangstransaksjonene vises på **Merking**-siden.

Du kan merke en avgangstransaksjon mot en tilgang etter transaksjonen er postert. Du kan samsvare eller merke en avgangstransaksjon for en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal.

Følgende transaksjoner illustreres på figuren som følger:

- 1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
- 2b. Økonomisk lagertilgang av et antall på 1 til kost USD 22,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3c. Økonomisk lageravgang for 3b er merket mot økonomisk lageravgang for 2b.
- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Fysisk lageravgang av et antall på 1 til kostpris USD 23,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 7\. Lagerlukking utføres. Basert på merkingsprinsippet som bruker metoden for avveid gjennomsnitt, utlignes de merkede transaksjonene mot hverandre. I dette eksemplet utlignes 3b mot 2b, og en justering på USD 6,00 posteres til 3b for å få verdien til å bli USD 22,00. I dette eksemplet utføres ingen flere utligninger, fordi lukkingen oppretter utligninger bare for økonomisk oppdaterte transaksjoner.

Diagrammet nedenfor illustrerer denne serien av transaksjoner og viser virkningen av å velge lagermodellen for avveid gjennomsnitt med merking.

![Avveid gjennomsnitt med merking.](media/weighted-average-with-marking.png)

**Nøkkel til diagram**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Hver dato i diagrammet er atskilt med en tynn, svart loddrett linje. Datoen er notert nederst i diagrammet.
- Lagerlukkinger vises med en rød linje med vannrette streker.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

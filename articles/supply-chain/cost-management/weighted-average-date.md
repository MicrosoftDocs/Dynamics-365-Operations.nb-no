---
title: Dato avveid gjennomsnitt
description: Dato avveid gjennomsnitt er en lagermodell basert på avveid gjennomsnitt-prinsippet, hvor frigivelser fra lageret verdsettes til gjennomsnittsverdien av varene som er mottatt på lageret for hver separate dag i lageravslutningsperioden.
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b89082ef0dcaafd059fdc496acf49efbf2b9324a
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569208"
---
# <a name="weighted-average-date"></a>Dato avveid gjennomsnitt

[!include [banner](../includes/banner.md)]

Dato for avveid gjennomsnitt er en lagermodell som er basert på prinsippet for avveid gjennomsnitt. I avveid gjennomsnitt-prinsippet verdsettes frigivelser fra lageret til gjennomsnittsverdien av varene som er mottatt på lageret for hver separate dag i lageravslutningsperioden. 

Når du kjører en lageravslutning ved hjelp av dato for avveid gjennomsnitt, utlignes alle daglige mottak mot en virtuell avgang. Denne virtuelle avgangen inneholder totalt mottatt antall og verdi for den aktuelle dagen. Den virtuelle frigivelsen har et tilsvarende virtuelt mottak, som frigivelsene utlignes mot. Derfor får alle avgangene samme gjennomsnittskostnad. Du kan se på denne virtuelle avgangen som en virtuell overføring, som kalles *overføring av avveid gjennomsnitt fra lagerlukking*. 

Hvis det bare har skjedd ett mottak på eller før datoen, trenger du ikke verdsette gjennomsnittsverdien. Fordi alle avganger utlignes fra dette mottaket, vil ikke den virtuelle overføringen bli opprettet. På samme måte, hvis det bare skjer frigivelser på den aktuelle datoen, vil det ikke finnes noen mottak å verdsette en gjennomsnittsverdi fra, og den virtuelle overføringen vil ikke bli opprettet. Når du bruker dato for avveid gjennomsnitt, kan du merke lagertransaksjoner slik at et bestemt varemottak utlignes mot en bestemt avgang. I dette tilfellet bruker du ikke dato for avveid gjennomsnitt-regelen. Månedlig lagerlukking anbefales når du bruker dato avveid gjennomsnitt-lagermodellen. 

Følgende formel brukes til å beregne metoden for dato for avveid gjennomsnitt: 

Avveid gjennomsnitt = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q*n* × P*n*\]) ÷ (Q1 + Q2 + Q*n*) 

Når lagerlukking pågår, utføres beregningen hver dag i hele lukkingsperioden, som vist i illustrasjonen nedenfor. 

![Dato avveid gjennomsnitt for daglig beregningsmodell](./media/weightedaveragedatedailycalculationmodel.gif) 

Lagertransaksjoner som forlater lageret, for eksempel salgsordrer, lagerjournaler og produksjonsordrer, forekommer til en estimert kostpris på posteringsdatoen. Denne estimerte kostprisen kalles også glidende gjennomsnitt av kostpris. På datoen for lagerlukking analyserer systemet lagertransaksjonene for tidligere perioder, tidligere dager og gjeldende dato. Denne analysen brukes til å avgjøre hvilket av de følgende prinsippene for lukking som skal brukes:

-   Direkte bosetting
-   Summert utligning

Utligninger er lagerlukkingsposteringer som justerer avganger med det avveide gjennomsnittet som gjelder på datoen for lagerlukking. 

**Obs!** Hvis du vil ha mer informasjon om utligninger, kan du se artikkelen om lagerlukking. Eksemplene nedenfor viser virkningene når avveid gjennomsnitt brukes i fem konfigurasjoner:

-   Direkte utligning med dato for avveid gjennomsnitt når alternativet **Ta med fysisk verdi** ikke brukes
-   Summert utligning med dato for avveid gjennomsnitt når alternativet **Ta med fysisk verdi** ikke brukes
-   Direkte utligning med dato for avveid gjennomsnitt når alternativet **Ta med fysisk verdi** brukes
-   Summert utligning med dato for avveid gjennomsnitt når alternativet **Ta med fysisk verdi** brukes
-   Dato for avveid gjennomsnitt når merking brukes

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Direkte utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi ikke brukes
Gjeldende versjon bruker det samme prinsippet for direkte utligning som ble brukt for avveid gjennomsnitt i tidligere versjoner. Systemet bruker direkte utligning mellom mottak og avganger. Systemet bruker dette prinsippet for direkte utligning i noen bestemte situasjoner:

-   Når én tilgang og én eller flere avganger er postert i perioden.
-   Når bare avganger er postert i perioden, og beholdningen inneholder varer fra en tidligere lagerlukning.

I det følgende scenariet er økonomisk oppdaterte avganger og tilganger postert. Under lagerlukking vil systemet utligne tilganger direkte mot avganger, og det er ikke nødvendig å justere kostpris for avganger. 

Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak oppdateres med et antall på 5 til kostpris USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang oppdateres med et antall på 5 til kostpris USD 10,00 per stykk.
-   2a. Fysisk lageravgang oppdateres med et antall på 2 til kostpris USD 10,00 per stykk.
-   2b. Økonomisk lageravgang oppdateres med et antall på 2 til kostpris USD 10,00 per stykk.
-   3. Lagerlukkingen er utført med metoden for direkte utligning for å utligne økonomiske lagertilganger mot økonomiske lageravganger.

![Direkte utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi ikke brukes](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Nøkkel til illustrasjonen:**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet *Antall*@*Enhetspris*.
-   Hvis en lagertransaksjon står i parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis en lagertransaksjon ikke står i parenteser, betyr det at lagertransaksjonen er økonomisk postert til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. IDene vises langs tidslinjen, og viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Summert utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi ikke brukes
Avveid gjennomsnitt er basert på prinsippet om at alle mottak i en avslutningsperiode summeres i en ny lageroverføringstransaksjon. Denne transaksjonen er kjent som *avveid gjennomsnittlig lagerlukking*. Alle mottakene for dagen utlignes mot avgangen til den nylig opprettede lageroverføringstransaksjonen. Alle avganger for dagen utlignes mot mottaket av den nye lageroverføringstransaksjonen. Hvis lagerbeholdningen er positiv etter lagerlukkingen, summeres lagerbeholdningen og verdien av lageret i den nye tilgangstransaksjonen for lageroverføring. Hvis lagerbeholdningen er negativ etter lagerlukkingen, er lagerbeholdningen og verdien av lageret lik summen av de enkelte avgangene som ikke er fullt utlignet. 

I det følgende scenariet posteres flere økonomisk oppdaterte tilganger og avganger i løpet av perioden. Under lagerlukkingen vil systemet undersøke hver dag for seg, for å avgjøre hvordan den enkelte dagen skal behandles. 

Illustrasjonen nedenfor viser disse transaksjonene: 

**Dag 1:**

-   1a. Fysisk mottak til lager oppdateres med et antall på 3 til USD 15,00 per stykk.
-   1b. Økonomisk tilgang til lager oppdateres med et antall på 3 til USD 15,00 per stykk.
-   2a. Fysisk lageravgang av et antall på 1 til glidende gjennomsnitt av kostpris, som er USD 15,00.
-   2b. Økonomisk lageravgang av et antall på 1 til glidende gjennomsnitt av kostpris, som er USD 15,00.

Systemet vil bruke direkte utligning for dag 1. 

**Dag 2:**

-   3a. Fysisk lageravgang av et antall på 1 til glidende gjennomsnitt av kostpris, som er USD 15,00
-   3b. Økonomisk lageravgang av et antall på 1 til glidende gjennomsnitt av kostpris, som er USD 15,00

Systemet vil bruke direkte utligning for dag 2. 

**Dag 3:**

-   4a. Fysisk lageravgang av et antall på 1 til glidende gjennomsnitt av kostpris, som er USD 15,00
-   4b. Økonomisk lageravgang av et antall på 1 til glidende gjennomsnitt av kostpris, som er USD 15,00
-   5a. Fysisk mottak til lager av et antall på 1 til USD 17,00 per stykk
-   5b. Økonomisk tilgang til lager av et antall på 1 til USD 17,00 per stykk

Lagerlukking utføres. Her må direkte utligning brukes, fordi det finnes flere tilganger som skjer på flere forskjellige dager.

-   7a. Det opprettes en økonomisk avgang til avveid gjennomsnitt av verdien for lagerlukkingstransaksjonen, med et antall på 2 til USD 32,00 for å summere utligninger av alle økonomiske tilganger til lager som ennå ikke er lukket på denne datoen.
-   7b. Det opprettes en økonomisk tilgang til avveid gjennomsnitt av verdien for lagerlukkingstransaksjonen, som brukes til å utligne 7a.

Systemet genererer og posterer den summerte lageroverføringstransaksjonen. I tillegg utligner systemet alle tilganger for dagen og lagerbeholdning på tidligere dager mot den summerte avgangstransaksjonen for lageroverføring. Alle avganger for dagen utlignes mot den summerte tilgangstransaksjonen for lageroverføring. Det avveide gjennomsnittet av kostprisen beregnes til USD 16,00. Avgangen justeres med USD 1,00 for å justere den til det avveide gjennomsnittet av kostprisen. Det nye glidende gjennomsnittet av kostprisen er USD 16,00. 

Illustrasjonen nedenfor viser denne serien av transaksjoner og virkningen av å bruke lagermodellen for avveid gjennomsnitt og prinsippet for summert utligning, men uten å bruke alternativet **Ta med fysisk verdi**. 

![Summert utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi ikke brukes](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Nøkkel til illustrasjonen**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet *Antall*@*Enhetspris*.
-   Hvis en lagertransaksjon står i parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis en lagertransaksjon ikke står i parenteser, betyr det at lagertransaksjonen er økonomisk postert til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. IDene vises langs tidslinjen, og viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde piler som går diagonalt fra tilgang til avgang.
-   Heltrukne røde diagonale piler viser tilgangstransaksjonene som utlignes mot avgangstransaksjoner som opprettes av systemet.
-   Den heltrukne grønne diagonale pilen viser tilgangstransaksjonen som opprettes av systemet, og som brukes til å utligne den opprinnelige, posterte avgangstransaksjonen.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Direkte utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi brukes
Gjeldende versjon bruker det samme prinsippet for direkte utligning som brukes for avveid gjennomsnitt i tidligere versjoner. Systemet bruker direkte utligning mellom mottak og avganger. Systemet bruker dette prinsippet for direkte utligning i noen bestemte situasjoner:

-   Når én tilgang og én eller flere avganger er postert i perioden.
-   Når bare avganger er postert i perioden, og beholdningen inneholder en lagerbeholdning fra en tidligere lagerlukking.

Hvis du merker av for **Ta med fysisk verdi** for en vare på siden **Varemodellgruppe**, bruker systemet fysisk oppdaterte tilganger når den estimerte kostprisen eller glidende gjennomsnitt beregnes. Avganger posteres på grunnlag av denne estimerte kostprisen for perioden. Under lagerlukkingen tas det bare hensyn til økonomisk oppdaterte tilganger når avveid gjennomsnitt beregnes.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Summert utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi brukes
Hvis du merker av for **Ta med fysisk verdi** for en vare på siden **Varemodellgruppe**, bruker systemet fysisk oppdaterte tilganger når den estimerte kostprisen eller glidende gjennomsnitt beregnes. Avganger posteres på grunnlag av denne estimerte kostprisen for perioden. Under lagerlukkingen tas det bare hensyn til økonomisk oppdaterte tilganger når avveid gjennomsnitt beregnes. Utligning for avveid gjennomsnitt er basert på prinsippet om at mottak i en avslutningsperiode summeres i en ny lageroverføringstransaksjon, som kalles *avveid gjennomsnittlig lagerlukking*. Alle mottakene for dagen utlignes mot avgangen til den nylig opprettede lageroverføringstransaksjonen. Alle avganger for dagen utlignes mot mottaket av den nye lageroverføringstransaksjonen. Hvis lagerbeholdningen er positiv etter lagerlukkingen, summeres denne lagerbeholdningen og verdien av lageret i den nye lageroverføringstransaksjonen (tilganger). Hvis lagerbeholdningen er negativ etter lagerlukkingen, er lagerbeholdningen og verdien av lageret lik summen av de enkelte avgangene som ikke er fullt utlignet.

## <a name="weighted-average-date-when-marking-is-used"></a>Dato for avveid gjennomsnitt når merking brukes
Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres. 

La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Fordi dette er en hasteordre, blir du nødt til å betale en høyere pris for denne varen for å imøtekomme kundens forespørsel. Du må være sikker på at denne lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for denne salgsordrefakturaen. Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Salgsordredokumentet merkes mot bestillingen før følgeseddelen eller fakturaen posteres. Vareforbruket vil være USD 120,00 i stedet for det gjeldende glidende gjennomsnittet av varens kost. Hvis bestillingens følgeseddel eller faktura posteres før merkingen skjer, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen. Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres. Når en tilgangstransaksjon merkes mot en avgangstransaksjon, ses det bort fra vurderingsmetoden som er definert i varens varemodellgruppe. I stedet utligner systemet disse transaksjonene mot hverandre. 

Du kan merke en avgangstransaksjon mot en tilgang før transaksjonen er postert. Du kan gjøre dette fra en salgsordrelinje på siden **Salgsordredetaljer**. Du kan vise de åpne tilgangstransaksjonene på **Merking**-siden. Du kan merke en avgangstransaksjon mot en tilgang etter transaksjonen er postert. Du kan samsvare eller merke en avgangstransaksjon for en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal. Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak av et antall på 1 til kostpris USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kostpris USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 1 til kostpris USD 20,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 1 til kostpris USD 20,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kostpris USD 25,00 per stykk.
-   4a. Fysisk lagermottak av et antall på 1 til kostpris USD 30,00 per stykk.
-   4b. Økonomisk lagertilgang av et antall på 1 til kostpris USD 30,00 per stykk.
-   5a. Fysisk lageravgang av et antall på 1 til kostpris USD 21,25 (glidende gjennomsnitt av økonomisk og fysisk oppdaterte transaksjoner).
-   5b. Økonomisk lageravgang av et antall på 1 merkes mot lagertilgangen 2b før transaksjonen posteres. Denne transaksjonen posteres med en kostpris på USD 20,00.
-   6a. Fysisk lageravgang av et antall på 1 til kostpris USD 21,25.
-   7. Lagerlukking utføres. Fordi den økonomisk oppdaterte transaksjonen er merket mot en eksisterende tilgang, utlignes disse transaksjonene mot hverandre, og det gjøres ingen justering.

Det nye glidende gjennomsnittet av kostprisen gjenspeiler gjennomsnittet av de økonomisk og fysisk oppdaterte transaksjonene med USD 27,50. Diagrammet nedenfor viser denne serien av transaksjoner og virkningen av å bruke lagermodellen med dato for avveid gjennomsnitt og merking.

![Dato for avveid gjennomsnitt med merking](./media/weightedaveragedatewithmarking.gif) 

**Nøkkel til illustrasjonen:**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet *Antall*@*Enhetspris*.
-   Hvis en lagertransaksjon står i parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis en lagertransaksjon ikke står i parenteser, betyr det at lagertransaksjonen er økonomisk postert til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. IDene vises langs tidslinjen, og viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde piler som går diagonalt fra tilgang til avgang.





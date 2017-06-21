---
title: Direkte utligning med fysisk verdi og merking
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cdbca6d9c71c901a1f4e7a8e5a2f9be1d3efb355
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="weighted-average-with-physical-value-and-marking"></a>Direkte utligning med fysisk verdi og merking

[!include[banner](../includes/banner.md)]




Når du kjører en lageravslutning, utlignes alle kvitteringene mot en virtuell avgang, som holder totalt mottatt antall og verdi. Denne virtuelle avgangen har et korresponderende virtuelt mottak fra der avgangene utlignes. På denne måten får alle avgangene samme gjennomsnittskostnad. Virtuell avgangen og mottak kan vises som en virtuell overføring, kalt lageravslutningsoverføring med avveid gjennomsnitt.

Hvis det bare er ett mottak, kan alle avgangene utlignes fra dette, og det opprettes ikke en virtuell overføring. 

Når du bruker avveid gjennomsnitt, kan du merke lagertransaksjonene slik at et bestemt varemottak utlignes mot en bestemt avgang i stedet for å bruke regelen for avveid gjennomsnitt. 

Vi anbefaler en månedelig lageravslutning når du bruker lagermodellen for avveid gjennomsnitt. 

Metoden for avveid gjennomsnittlig lagerlukking beregnes ved hjelp av følgende formel:
-   Avveid gjennomsnitt = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Lagertransaksjoner som forlater lageravgangene. Dette inkluderer salgsordrer, lagerjournaler og produksjonsordrer, og skjer til estimert kostpris på posteringsdatoen. Det refereres også til denne estimerte kostprisen som glidende gjennomsnitt. Når lageret lukkes, vil systemet analysere lagertransaksjonene for forrige og gjeldende perioder, og fastslå hvilke av lukkingsprinsippene nedenfor som skal brukes.
-   Direkte utligning
-   Summert utligning

Utligninger er lagerlukkingsposteringer som justerer avganger med det avveide gjennomsnittet som gjelder på datoen for lagerlukking. Eksemplene nedenfor viser virkningene når avveid gjennomsnitt brukes i fem forskjellige konfigurasjoner:
-   Direkte utligning for avveid gjennomsnitt uten alternativet Ta med fysisk verdi
-   Summert utligning for avveid gjennomsnitt uten alternativet Ta med fysisk verdi
-   Direkte utligning for avveid gjennomsnitt med alternativet Ta med fysisk verdi
-   Summert utligning for avveid gjennomsnitt med alternativet Ta med fysisk verdi
-   Avveid gjennomsnitt med merking

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Direkte utligning for avveid gjennomsnitt uten Ta med fysisk verdi
Prinsippet for direkte utligning er det sammen som brukes for avveid gjennomsnitt i tidligere versjoner. Systemet vil bruke direkte utligning mellom mottak og avganger. Systemet bruker dette prinsippet for direkte utligning i noen bestemte situasjoner:
-   Når én tilgang og én eller flere avganger er postert i perioden
-   Når bare avganger er postert i perioden, og beholdningen inneholder varer fra en tidligere lagerlukning

I scenariet i følgende deler er økonomisk oppdaterte avganger og tilganger postert. Under lagerlukking vil systemet utligne tilganger direkte mot avganger, og det er ikke nødvendig å justere kostpris for avganger. Følgende transaksjoner illustreres i grafikken.
-   1a. Fysisk lagermottak oppdatert for et antall på 5 til NOK 60,00 per stykk
-   1b. Økonomisk lagermottak oppdatert for et antall på 5 til NOK 60,00 per stykk
-   2a. Fysisk lageravgang oppdatert for et antall på 2 til NOK 60,00 per stykk
-   2b. Økonomisk lageravgang oppdatert for et antall på 2 til NOK 60,00 per stykk
-   3. Lagerlukking utføres ved hjelp av metoden for direkte utligning for å utligne det økonomiske lagermottaket mot den økonomiske lageravgangen.

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt og prinsippet for direkte utligning uten alternativet Ta med fysisk verdi. 

![Direkte utligning for avveid gjennomsnitt uten ta med fysisk verdi](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Nøkkel til diagram**
-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Quantity@Unitprice.
-   Hvis verdien til en lagertransaksjon står i parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon vises uten parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. IDene vises langs tidslinjen, og viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten Lagerlukking.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde piler som går diagonalt fra mottak til avgang.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Summert utligning for avveid gjennomsnitt uten alternativet Ta med fysisk verdi
Avveid gjennomsnitt brukerutligningsprinsippet om at alle mottak i en avslutningsperiode summeres i en ny transaksjon kalt Avveid gjennomsnittlig lagerlukking. Alle mottakene for perioden blir utlignet mot avgangen til den nylig opprettede lageroverføringstransaksjonen. Alle avganger for perioden blir utlignet mot mottaket av den nye lageroverføringstransaksjonen. Hvis lagerbeholdningen er positiv etter lagerlukkingen, summeres lagerbeholdningen og verdien av lageret i den nye lageroverføringstransaksjonen (tilganger). Hvis lagerbeholdningen er negativ etter lagerlukkingen, er lagerbeholdningen og verdien av lageret lik summen av de enkelte avgangene som ikke er fullt utlignet. I scenariet nedenfor er flere økonomisk oppdaterte mottak og én avgang postert. 

Under lagerlukkingen vil systemet generere og postere den summerte lageroverføringstransaksjonen og utligne alle mottakene for perioden mot den summerte lageroverføringstransaksjonen for avgang. Alle avgangene som er postert for perioden, vil utlignes mot den summerte lageroverføringstransaksjonen for mottak. Det avveide gjennomsnittet blir beregnet til NOK 90,00. Avgangen ble opprinnelig postert med en estimert kostpris på NOK 88,02. En justering med det negative beløpet NOK 0,33 opprettes og posteres derfor på avgangen. Når det gjelder lagerlukkingsdatoen, er lagerbeholdningen 3 stykk med en verdi på NOK 270,00. 

Følgende transaksjoner illustreres i grafikken nedenfor:
-   1a. Fysisk lagermottak oppdatert for et antall på 2 til NOK 66,00 per stykk.
-   1b. Økonomisk lagermottak oppdatert for et antall på 2 til NOK 84,00 per stykk.
-   2a. Fysisk lagermottak oppdatert for et antall på 2 til NOK 72,00 per stykk.
-   2b. Økonomisk lagermottak oppdatert for et antall på 1 til NOK 96,00 per stykk.
-   3a. Fysisk lageravgang oppdatert for et antall på 1 til NOK 88,02 per stykk (glidende gjennomsnitt).
-   3b. Økonomisk lageravgang oppdatert for et antall på 1 til NOK 88,02 per stykk (glidende gjennomsnitt).
-   4a. Fysisk lagermottak oppdatert for et antall på 2 til NOK 84,00 per stykk.
-   4b. Økonomisk lagermottak oppdatert for et antall på 1 til NOK 96,00 per stykk.
-   5. Lagerlukking utføres.
-   6a. Det opprettes en økonomisk avgang "Lagerlukkingstransaksjon for avveid gjennomsnitt", for å summere utligningene av alle de økonomiske lagermottakene.
-   6b. Det opprettes en økonomisk avgang "Lagerlukkingstransaksjon for avveid gjennomsnitt"  som motregning til 5a.

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt og prinsippet for summert utligning uten alternativet Ta med fysisk verdi. 

![Summert utligning for avveid gjennomsnitt uten ta med fysisk verdi](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Nøkkel til diagram**
-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Quantity@Unitprice.
-   Hvis verdien til en lagertransaksjon står i parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon vises uten parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. IDene vises langs tidslinjen, og viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten Lagerlukking.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde piler som går diagonalt fra mottak til avgang.
-   Røde piler illustrerer mottakstransaksjonen som blir utlignet mot avgangstransaksjonen som ble opprettet av systemet.
-   Den grønne pilen representerer den motposterte systemgenererte mottakstransaksjonen som den opprinnelige posterte avgangstransaksjonen utlignes mot

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Direkte utligning for avveid gjennomsnitt med alternativet Ta med fysisk verdi
Parameteren Ta med fysisk verdi fungerer på en annen måte med lagermodellen for avveid gjennomsnitt enn i tidligere versjoner av produktet. Merk av i boksen Ta med fysisk verdi for en vare i Varemodellgruppe-skjemaet. Systemet vil deretter bruke fysisk oppdaterte tilganger når den estimerte kostprisen eller det glidende gjennomsnittet beregnes. Avganger blir postert på grunnlag av denne estimerte kostprisen for perioden. I løpet av lagerlukkingen vil bare økonomisk oppdaterte mottak bli vurdert i beregningen av avveid gjennomsnitt. Vi anbefaler en månedelig lagerlukking når du bruker lagermodellen for avveid gjennomsnitt. I dette eksemplet med direkte utligning av avveid gjennomsnitt, er varemodellgruppen merket for å ta med fysisk verdi. 

Følgende transaksjoner illustreres i grafikken nedenfor:
-   1a. Fysisk lagermottak oppdatert for et antall på 1 til NOK 66,00 per stykk.
-   1b. Økonomisk lagermottak oppdatert for et antall på 1 til NOK 60,00 per stykk.
-   2a. Fysisk lagermottak oppdatert for et antall på 1 til NOK 90,00 per stykk.
-   3a. Fysisk lageravgang oppdatert for et antall på 1 til NOK 75,00 per stykk (glidende gjennomsnittskostnad, siden den fysiske mottaksverdien blir tatt hensyn til).
-   3b. Økonomisk lageravgang oppdatert for et antall på 1 til NOK 75,00 per stykk (glidende gjennomsnittskostnad, siden den fysiske mottaksverdien blir tatt hensyn til).
-   4. Lagerlukking utføres. Under lagerlukking vil systemet ignorere alle lagertransaksjoner om bare er fysisk oppdatert. I stedet brukes prinsippet for direkte utligning, fordi det bare finnes ett økonomisk mottak. En justering på NOK 15,00 blir postert til lagertransaksjonen som er økonomisk avgitt på lagerlukkingsdatoen. Etter lagerlukkingen vil lagerbeholdningen være et antall på 1 med en glidende gjennomsnittlig kostpris på NOK 90,00.

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt og prinsippet for direkte utligning med alternativet Ta med fysisk verdi. 

![Direkte utligning for avveid gjennomsnitt uten ta med fysisk verdi](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Nøkkel til diagram**
-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Quantity@Unitprice.
-   Hvis verdien til en lagertransaksjon står i parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon vises uten parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. IDene vises langs tidslinjen, og viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten Lagerlukking.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde piler som går diagonalt fra mottak til avgang.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Summert utligning for avveid gjennomsnitt med alternativet Ta med fysisk verdi
Parameteren Ta med fysisk verdi fungerer på en annen måte med avveid gjennomsnitt enn i tidligere versjoner. Merk av i boksen Ta med fysisk verdi for en vare på Varemodellgruppe-siden. Systemet vil deretter bruke fysisk oppdaterte tilganger under beregning av den estimerte kostprisen eller det glidende gjennomsnittet. Avganger posteres basert på denne estimerte kostprisen i løpet av perioden. I løpet av lagerlukkingen vil bare økonomisk oppdaterte mottak bli vurdert i beregningen av avveid gjennomsnitt. Vi anbefaler en månedelig lagerlukking når du bruker lagermodellen for avveid gjennomsnitt. I dette eksemplet med summert utligning av avveid gjennomsnitt, er lagermodellen merket for å ta med fysisk verdi. 

Følgende transaksjoner illustreres i grafikken nedenfor:
-   1a. Fysisk lagermottak oppdatert for et antall på 2 til NOK 66,00 per stykk.
-   1b. Økonomisk lagermottak oppdatert for et antall på 2 til NOK 84,00 per stykk.
-   2. Fysisk lagermottak av et antall på 1 til kostpris USD 10,00 per stykk.
-   3a. Fysisk lagermottak oppdatert for et antall på 2 til NOK 72,00 per stykk.
-   3b. Økonomisk lagermottak oppdatert for et antall på 1 til NOK 96,00 per stykk.
-   4a. Fysisk lageravgang oppdatert for et antall på 1 til NOK 81,00 per stykk (glidende gjennomsnittskostnad, siden den fysiske mottaksverdien blir tatt hensyn til).
-   4b. Økonomisk lageravgang oppdatert for et antall på 1 til NOK 81,00 per stykk (glidende gjennomsnittskostnad, siden den fysiske mottaksverdien blir tatt hensyn til).
-   5a. Fysisk lagermottak oppdatert for et antall på 2 til NOK 84,00 per stykk.
-   5b. Økonomisk lagermottak oppdatert for et antall på 1 til NOK 96,00 per stykk.
-   6. Lagerlukking utføres. Under lagerlukking vil systemet ignorere alle lagertransaksjoner som bare er fysisk oppdatert. Prinsippet for summert utligning brukes, fordi det bare finnes ett økonomisk mottak. En justering på NOK 9,00 blir postert til lagertransaksjonen som er økonomisk avgitt på lagerlukkingsdatoen. Etter lagerlukkingen vil lagerbeholdningen være et antall på 3 med en glidende gjennomsnittlig kostpris på NOK 90,00.
-   7a. Det opprettes en økonomisk avgang "Lagerlukkingstransaksjon for avveid gjennomsnitt", for å summere utligningene av alle de økonomiske lagermottakene.
-   7b. Det opprettes en økonomisk avgang "Lagerlukkingstransaksjon for avveid gjennomsnitt"  som motregning til 5a.

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt og prinsippet for summert utligning uten alternativet Ta med fysisk verdi. 

![Summert utligning for avveid gjennomsnitt med ta med fysisk verdi](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Nøkkel til diagram**
-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Quantity@Unitprice.
-   Hvis verdien til en lagertransaksjon står i parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon vises uten parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel 1a. IDene vises langs tidslinjen, og viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten Lagerlukking.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde piler som går diagonalt fra mottak til avgang.
-   Røde piler illustrerer mottakstransaksjonen som blir utlignet mot avgangstransaksjonen som ble opprettet av systemet.
-   Den grønne pilen representerer den motposterte systemgenererte mottakstransaksjonen som den opprinnelige posterte avgangstransaksjonen utlignes mot

## <a name="weighted-average-with-marking"></a>Avveid gjennomsnitt med merking
Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres. 

La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Fordi dette er en hasteordre, blir du nødt til å betale en høyere pris for denne varen for å betjene kundens forespørsel. Du må være sikker på at denne lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for denne salgsordrefakturaen. 

Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Dette salgsordredokumentet merkes for eksempel mot bestillingen før følgeseddelen eller fakturaen posteres. Vareforbruket vil være USD 120,00 i stedet for det gjeldende glidende gjennomsnittet av varens kost. Hvis bestillingens følgeseddel eller faktura posteres før merkingen skjer, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen. 

Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres. 

En mottakstransaksjon er merket mot en avgangstransaksjon. Vurderingsmetoden som er valgt for varens varemodellgruppe, ignoreres deretter, og systemet vil utligne disse transaksjonene mot hverandre. 

Du kan merke en avgangstransaksjon mot en tilgang før transaksjonen er postert. Du kan gjøre dette fra en salgsordrelinje på siden Salgsordredetaljer. De åpne tilgangstransaksjonene vises på Merking-siden. 

Du kan merke en avgangstransaksjon mot en tilgang etter transaksjonen er postert. Du kan samsvare eller merke en avgangstransaksjon for en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal. 

Følgende transaksjoner illustreres i grafikken nedenfor:
-   1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 1 til kost USD 20,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
-   4a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
-   4b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
-   5a. Fysisk lagermottak av et antall på 1 til kostpris NOK 127,50 per stykk (glidende gjennomsnitt av økonomisk og fysisk oppdaterte transaksjoner).
-   5b. Økonomisk lageravgang av et antall på 1 merkes mot lagertilgangen 2b før transaksjonen posteres. Denne transaksjonen posteres med en kostpris på NOK 120,00.
-   6a. Fysisk lageravgang av et antall på 1 til en kostpris på NOK 127,50 per stykk.
-   7. Lagerlukking utføres. Fordi den økonomisk oppdaterte transaksjonen er merket mot en eksisterende tilgang, utlignes disse transaksjonene mot hverandre, og det gjøres ingen justering.

Det nye glidende gjennomsnittet av kostprisen gjenspeiler gjennomsnittet av de økonomisk og fysisk oppdaterte transaksjonene med USD 27,50. 

Diagrammet nedenfor illustrerer denne serien av transaksjoner, og viser virkningen av å velge lagermodellen for avveid gjennomsnitt med merking. 

![Avveid gjennomsnitt med merking](./media/weightedaveragewithmarking.gif) 

**Nøkkel til diagram**
-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Quantity@Unitprice.
-   Hvis verdien til en lagertransaksjon står i parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon vises uten parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. IDene vises langs tidslinjen, og viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten Lagerlukking.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde piler som går diagonalt fra tilgang til avgang.







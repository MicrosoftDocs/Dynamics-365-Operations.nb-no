---
title: LIFO-dato med fysisk verdi og merking
description: "Sist inn, først ut etter dato (LIFO-dato) er en lagermodell basert på LIFO-prinsippet. Avganger fra lageret utlignes mot de siste mottakene til lageret, basert på datoen for lagertransaksjonen. Med LIFO-datoen, hvis det ikke er et mottak før avgangen, utlignes avgangen mot alle mottak som skjer etter datoen for avgangen. Flere avganger på samme dato kan utlignes i rekkefølgen siste avgang, siste mottak."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-23 23 - 07 - 14
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7a2430de79cd56441c8101336992d4a10889a126
ms.lasthandoff: 03/29/2017


---

# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO-dato med fysisk verdi og merking

Sist inn, først ut etter dato (LIFO-dato) er en lagermodell basert på LIFO-prinsippet. Avganger fra lageret utlignes mot de siste mottakene til lageret, basert på datoen for lagertransaksjonen. Med LIFO-datoen, hvis det ikke er et mottak før avgangen, utlignes avgangen mot alle mottak som skjer etter datoen for avgangen. Flere avganger på samme dato kan utlignes i rekkefølgen siste avgang, siste mottak. 

Hvis det ikke er et mottak før avgangen når du bruker LIFO-datolagermodellen (Sist inn, først ut etter dato), utlignes avgangen mot alle mottak som skjer etter datoen for avgangen. Flere avganger på samme dato kan utlignes i rekkefølgen siste avgang, siste mottak. Når du bruker LIFO-dato, trenger du ikke å bruke LIFO-datoregelen. Når du bruker dato for avveid gjennomsnitt, kan du i stedet merke lagertransaksjoner slik at et bestemt varemottak utlignes mot en bestemt avgang. En periodisk lagerlukking anbefales når du bruker LIFO-datolagermodellen. Eksemplene nedenfor viser effekten når LIFO-dato brukes med tre forskjellige konfigurasjoner:

-   LIFO-dato når alternativet **Ta med fysisk verdi** ikke brukes
-   LIFO-dato når alternativet **Ta med fysisk verdi** brukes
-   LIFO-dato med merking

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-dato når alternativet Ta med fysisk verdi ikke brukes
I dette eksemplet er det ikke merket av for Ta med fysisk verdi for varemodellgruppen. Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 1 til kost USD 20,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
-   4a. Fysisk lageravgang av et antall på 1 til kostpris USD 15,00 per stykk (glidende gjennomsnitt av økonomisk oppdaterte transaksjoner).
-   4b. Økonomisk lageravgang av et antall på 1 til kostpris USD 15,00 per stykk (glidende gjennomsnitt av økonomisk oppdaterte transaksjoner).
-   5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
-   5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
-   6. Lagerlukking utføres. I samsvar med LIFO-datometoden blir den sist økonomisk oppdaterte avgangen utlignet mot den sist økonomisk oppdaterte tilgangen etter dato. Avgangstransaksjonen justeres med USD 5,00. Disse transaksjonene utlignes mot hverandre.

Det nye glidende gjennomsnittet for kostpris gjenspeiler gjennomsnittet for økonomisk oppdaterte transaksjoner, det vil si USD 15,00. Illustrasjonen nedenfor viser virkningene av LIFO-datolagermodellen når alternativet **Ta med fysisk verdi** ikke brukes. ![LIFO-dato med ta med fysisk verdi](./media/lifodatewithoutincludephysicalvalue.gif) **Nøkkel til diagram**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil verdien til lagertransaksjonen som er angitt i formatetQuantity@Unitprice.
-   Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-dato når alternativet Ta med fysisk verdi brukes
Du kan merke av i boksen **Ta med fysisk verdi** for en vare på **Varemodellgrupper**-siden. I dette tilfellet bruker systemet mottakstransaksjoner for både fysiske og økonomiske til å beregne løpende gjennomsnittlig kostpris. Der det er relevant, justerer systemet også den fysisk oppdaterte avgangstransaksjonen. Hvis det ikke er merket av for boksen **Ta med fysisk verdi**, vil lagerlukking med LIFO-datolagermodellen bare utligne transaksjoner som er økonomisk oppdatert. I dette eksemplet er det merket av for Ta med fysisk verdi for varemodellgruppen. Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 1 til kost USD 20,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
-   4a. Fysisk lageravgang av et antall på 1 til kostpris USD 18,33 per stykk (glidende gjennomsnitt av økonomisk oppdaterte transaksjoner).
-   4b. Økonomisk lageravgang av et antall på 1 til kostpris USD 18,33 per stykk (glidende gjennomsnitt av økonomisk oppdaterte transaksjoner).
-   5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
-   5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
-   6. Lagerlukking utføres. I samsvar med LIFO-datometoden blir den sist oppdaterte avgangen justert eller utlignet mot den sist oppdaterte tilgangen etter dato. Disse transaksjonene blir ikke utlignet av hverandre, fordi den økonomiske mottakstransaksjonen justeres mot en fysisk oppdateringstransaksjon. I stedet vil bare en justering med USD 6,67 gjøres i avgangstransaksjonen.

Det nye glidende gjennomsnittet for kostpris gjenspeiler gjennomsnittet for økonomisk oppdaterte transaksjoner, det vil si USD 20,00. Illustrasjonen nedenfor viser virkningene av LIFO-lagermodellen når alternativet **Ta med fysisk verdi** brukes. ![LIFO-dato med ta med fysisk verdi](./media/lifodatewithincludephysicalvalue.gif) **Nøkkel til diagram**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil verdien til lagertransaksjonen som er angitt i formatetQuantity@Unitprice.
-   Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="lifo-date-with-marking"></a>LIFO-dato med merking
Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres. La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Fordi dette er en hasteordre, blir du nødt til å betale en høyere pris for denne varen for å imøtekomme kundens forespørsel. Du må kontrollere at denne lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for denne salgsordrefakturaen. Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Hvis dette salgsordredokumentet merkes mot bestillingen før følgeseddelen eller fakturaen posteres, vil solgte varers kost (Vareforbruk) være USD 120,00, ikke det gjeldende glidende gjennomsnittet av varens kost. Hvis bestillingens følgeseddel eller faktura posteres før merkingen skjer, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen. Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres. En mottakstransaksjon er for eksempel merket for en avgangstransaksjon. I dette tilfellet vil vurderingsmetoden som er definert i varens varemodellgruppe ignoreres, og systemet utligner disse transaksjonene mot hverandre. Du kan merke en avgangstransaksjon mot en tilgang før transaksjonen er postert. Du kan gjøre dette fra en salgsordrelinje på siden **Salgsordredetaljer**. Du kan vise de åpne tilgangstransaksjonene på **Merking**-siden. Du kan også merke en avgangstransaksjon mot en tilgang etter transaksjonen er postert. Du kan samsvare eller merke en avgangstransaksjon for en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal. Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 1 til kost USD 20,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
-   4a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
-   4b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
-   5a. Fysisk lagermottak av et antall på 1 til kostpris USD 21,25 per stykk (glidende gjennomsnitt av økonomisk og fysisk oppdaterte transaksjoner).
-   5b. Økonomisk lageravgang av et antall på 1 merkes mot lagertilgangen 2b før transaksjonen posteres. Denne transaksjonen posteres med en kostpris på USD 20,00 per stykk.
-   6a. Fysisk lageravgang av et antall på 1 til kostpris USD 21,25 per stykk.
-   7. Lagerlukking utføres. Fordi den økonomisk oppdaterte FIFO-transaksjonen er merket mot en eksisterende tilgang, utlignes disse transaksjonene mot hverandre, og det gjøres ingen justering.

Det nye glidende gjennomsnittet av kostprisen gjenspeiler gjennomsnittet av de økonomisk og fysisk oppdaterte transaksjonene med USD 27,50. Illustrasjonen nedenfor viser virkningene av LIFO-lagermodellen når merking mellom avganger og tilganger brukes. ![LIFO-dato med merking](./media/lifodatewithmarking.gif) **Nøkkel til diagrammet**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil verdien til lagertransaksjonen som er angitt i formatetQuantity@Unitprice.
-   Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.




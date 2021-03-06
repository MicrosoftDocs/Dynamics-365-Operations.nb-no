---
title: FIFO med fysisk verdi og merking
description: FIFO (First in, First out - først inn, først ut) er en lagermodell der de første mottakene utstedes først. Økonomisk oppdaterte avganger fra lager utlignes mot de første økonomisk oppdaterte mottakene i lager, basert på den økonomiske datoen til lagertransaksjonen.
author: AndersGirke
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d37efef723a7ca5e5f2333ff41cdf8351156e9bb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821615"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO med fysisk verdi og merking

[!include [banner](../includes/banner.md)]

FIFO (First in, First out - først inn, først ut) er en lagermodell der de første mottakene utstedes først. Økonomisk oppdaterte avganger fra lager utlignes mot de første økonomisk oppdaterte mottakene i lager, basert på den økonomiske datoen til lagertransaksjonen. 

Når du bruker FIFO, trenger du ikke å bruke FIFO-regelen. Når du bruker dato for avveid gjennomsnitt, kan du i stedet merke lagertransaksjoner slik at et bestemt varemottak utlignes mot en bestemt avgang. Det anbefales en periodisk lagerlukking når du bruker FIFO-lagermodellen. Eksemplene nedenfor viser effekten når FIFO brukes med tre forskjellige konfigurasjoner:

-   FIFO når alternativet **Ta med fysisk verdi** ikke brukes
-   FIFO når alternativet **Ta med fysisk verdi** brukes
-   FIFO med merking

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO når alternativet Ta med fysisk verdi ikke brukes
I dette eksemplet er det ikke merket av for Ta med fysisk verdi for varemodellgruppen. Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 2 til kost USD 10,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 2 til kost USD 10,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
-   4a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
-   4b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
-   5a. Fysisk lageravgang av et antall på 1 til kostpris USD 20,00 per stykk (glidende gjennomsnitt av økonomisk oppdaterte transaksjoner).
-   5b. Økonomisk lageravgang av et antall på 1 til kostpris USD 15,00 per stykk (glidende gjennomsnitt av økonomisk oppdaterte transaksjoner).
-   6. Lagerlukking utføres. I samsvar med FIFO-metoden blir den først økonomisk oppdaterte avgangen utlignet mot den først økonomisk oppdaterte tilgangen. Avgangstransaksjonen justeres med USD -5,00.

Det nye glidende gjennomsnittet for kostpris gjenspeiler gjennomsnittet for økonomisk oppdaterte transaksjoner. Illustrasjonene nedenfor viser virkningene av FIFO-lagermodellen for denne transaksjonsserien når alternativet **Ta med fysisk verdi** ikke brukes. 

![FIFO uten ta med fysisk verdi](./media/fifowithoutincludephysicalvalue.gif) 

**Nøkkel til diagrammet**

- Lagertransaksjoner vises med loddrette piler.
- Mottak til lager vises med loddrette piler over tidslinjen.
- Avganger fra lager vises med loddrette piler under tidslinjen.
- Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Antall@Enhetspris.
- Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
- Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO når alternativet Ta med fysisk verdi brukes
Hvis det er merket av i avmerkingsboksen **Ta med fysisk verdi** for en vare på siden **Varemodellgruppe**, bruker systemet både fysiske og økonomiske tilgangstransaksjoner når det glidende gjennomsnittet av kostprisen beregnes. Der det er relevant, justerer systemet også den fysisk oppdaterte avgangstransaksjonen. Hvis det ikke er merket av for avmerkingsboksen **Ta med fysisk verdi**, vil lagerlukking med FIFO-lagermodellen bare utligne transaksjoner som er økonomisk oppdatert. Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 1 til kost USD 20,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
-   4a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
-   4b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
-   5a. Fysisk lagertilgang av et antall på 1 til kostpris USD 21,25 per stykk (glidende gjennomsnitt av økonomisk og fysisk oppdaterte transaksjoner).
-   5b. Økonomisk lageravgang av et antall på 1 til kostpris USD 21,25 per stykk (glidende gjennomsnitt av økonomisk og fysisk oppdaterte transaksjoner).
-   6a. Fysisk lageravgang av et antall på 1 til kostpris USD 21,25 per stykk.
-   7. Lagerlukking utføres. I samsvar med FIFO-metoden blir den første økonomiske avgangstransaksjonen justert eller utlignet mot den først oppdaterte tilgangen, enten økonomisk eller fysisk.

Transaksjon 5b utlignes mot 1b. Det vi være en justering på negative USD 11,25 for denne avgangstransaksjonen. Det nye glidende gjennomsnittet av kostprisen gjenspeiler gjennomsnittet av de økonomisk og fysisk oppdaterte transaksjonene, USD 27,50. Illustrasjonen nedenfor viser virkningene av FIFO-lagermodellen for denne transaksjonsserien når alternativet **Ta med fysisk verdi** brukes. 

![FIFO med ta med fysisk verdi](./media/fifowithincludephysicalvalue.gif) 

**Nøkkel til diagrammet**

- Lagertransaksjoner vises med loddrette piler.
- Mottak til lager vises med loddrette piler over tidslinjen.
- Avganger fra lager vises med loddrette piler under tidslinjen.
- Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Antall@Enhetspris.
- Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
- Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="fifo-with-marking"></a>FIFO med merking
Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres. La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Fordi dette er en hasteordre, må du betale en høyere pris for denne varen for å imøtekomme kundens forespørsel. Du må kontrollere at denne lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for denne salgsordrefakturaen. Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Hvis dette salgsordredokumentet merkes mot bestillingen før følgeseddelen eller fakturaen posteres, vil solgte varers kost (Vareforbruk) være USD 120,00, ikke det gjeldende glidende gjennomsnittet av varens kost. Hvis bestillingens følgeseddel eller faktura posteres før merkingen skjer, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen. Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres. Når en tilgangstransaksjon samsvares med en avgangstransaksjon, ses det bort fra vurderingsmetoden som er definert i varemodellgruppen, og systemet utligner disse transaksjonene mot hverandre. Du kan merke en avgangstransaksjon mot en tilgang før transaksjonen er postert. Du kan gjøre dette fra en salgsordrelinje på siden **Salgsordredetaljer**. Du kan vise de åpne tilgangstransaksjonene på **Merking**-siden. Du kan også merke en avgangstransaksjon mot en tilgang etter transaksjonen er postert. Du kan samsvare eller merke en avgangstransaksjon for en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal. Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 1 til kost USD 20,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
-   4a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
-   4b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
-   5a. Fysisk lagermottak av et antall på 1 til kostpris USD 21,25 per stykk (glidende gjennomsnitt av økonomisk og fysisk oppdaterte transaksjoner).
-   5b. Økonomisk lageravgang av et antall på 1 merkes mot lagertilgangen 2b før transaksjonen posteres. Denne transaksjonen posteres med en kostpris på NOK 120,00 per stykk.
-   6a. Fysisk lageravgang av et antall på 1 til kostpris USD 21,25 per stykk.
-   7. Lagerlukking utføres. Siden den økonomisk oppdaterte FIFO-transaksjonen er merket mot en eksisterende tilgang, utlignes disse transaksjonene mot hverandre, og det gjøres ingen justering.

Det nye glidende gjennomsnittet av kostprisen gjenspeiler gjennomsnittet av de økonomisk og fysisk oppdaterte transaksjonene, USD 27,50. Illustrasjonen nedenfor viser virkningen FIFO-lagermodellen på denne transaksjonsserien når det brukes merking mellom avganger og tilganger. 

![FIFO med merking](./media/fifowithmarking.gif) 

**Nøkkel til diagrammet**

- Lagertransaksjoner vises med loddrette piler.
- Mottak til lager vises med loddrette piler over tidslinjen.
- Avganger fra lager vises med loddrette piler under tidslinjen.
- Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Antall@Enhetspris.
- Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
- Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
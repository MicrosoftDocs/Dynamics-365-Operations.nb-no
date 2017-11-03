---
title: LIFO med fysisk verdi og merking
description: "LIFO (\"Last in, First out\") er en lagermodell der de siste (nyeste) tilgangene tas ut først. Avganger fra lageret utlignes mot de siste mottakene til lageret, basert på datoen for lagertransaksjonen."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 86bafb9346b7335bf0a5d6c156eee6d53f1998a9
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="lifo-with-physical-value-and-marking"></a>LIFO med fysisk verdi og merking

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


LIFO ("Last in, First out") er en lagermodell der de siste (nyeste) tilgangene tas ut først. Avganger fra lageret utlignes mot de siste mottakene til lageret, basert på datoen for lagertransaksjonen. 

I LIFO-lagermodellen (Last in, first out - sist inn, først ut) utstedes de siste (nyeste) mottakene først. Avganger fra lageret utlignes mot de siste mottakene til lageret, basert på datoen for lagertransaksjonen. Når du bruker LIFO, trenger du ikke å bruke LIFO-regelen. Du kan i stedet merke lagertransaksjoner slik at en bestemt vareavgang utlignes mot et bestemt mottak. Når lagermodellen LIFO brukes, anbefaler vi at lagerlukking utføres periodisk. 

Eksemplene nedenfor viser effekten når LIFO brukes med tre forskjellige konfigurasjoner:

-   LIFO når alternativet **Ta med fysisk verdi** ikke brukes
-   LIFO når alternativet **Ta med fysisk verdi** brukes
-   LIFO med merking

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO når alternativet Ta med fysisk verdi ikke brukes
I dette eksemplet er det ikke merket av for Ta med fysisk verdi for varemodellgruppen. Illustrasjonen nedenfor viser disse transaksjonene:

-   1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
-   1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
-   2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
-   2b. Økonomisk lagertilgang av et antall på 1 til kost USD 20,00 per stykk.
-   3a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
-   4a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
-   4b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
-   5a. Fysisk lageravgang av et antall på 1 til kostpris USD 20,00 per stykk (glidende gjennomsnitt av økonomisk oppdaterte transaksjoner).
-   5a. Økonomisk lageravgang av et antall på 1 til kostpris USD 20,00 per stykk (glidende gjennomsnitt av økonomisk oppdaterte transaksjoner).
-   6. Lagerlukking utføres. I samsvar med LIFO-metoden blir den sist økonomisk oppdaterte avgangen utlignet mot den sist økonomisk oppdaterte tilgangen. Avgangstransaksjonen justeres med USD 10,00.

Det nye glidende gjennomsnittet for kostpris gjenspeiler gjennomsnittet for økonomisk oppdaterte transaksjoner, det vil si USD 15,00. Illustrasjonen nedenfor viser virkningene av LIFO-lagermodellen for denne transaksjonsserien når alternativet **Ta med fysisk verdi** ikke brukes. ![LIFO uten ta med fysisk verdi](./media/lifowithoutincludephysicalvalue.gif) 

**Nøkkel til diagrammet**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Quantity@Unitspris.
-   Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO når alternativet Ta med fysisk verdi brukes
Hvis det er merket av i avmerkingsboksen **Ta med fysisk verdi** for en vare på siden **Varemodellgrupper**, bruker systemet både fysiske og økonomiske tilgangstransaksjoner når det glidende gjennomsnittet av kostprisen beregnes. Der det er relevant, justerer systemet også den fysisk oppdaterte avgangstransaksjonen. Hvis det ikke er merket av for avmerkingsboksen **Ta med fysisk verdi**, vil lagerlukking med LIFO-lagermodellen bare utligne transaksjoner som er økonomisk oppdatert. 

Illustrasjonen nedenfor viser disse transaksjonene:

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
-   7. Lagerlukking utføres. I samsvar med LIFO-metoden blir den siste avgangstransaksjonen justert eller utlignet mot den sist oppdaterte tilgangen.

Transaksjonen 6a justeres mot tilgangstransaksjonen 4b. Systemet vil ikke utligne disse transaksjonene, fordi mottaket bare oppdateres fysisk, ikke økonomisk. I stedet vil bare en justering på USD 8,75 posteres mot den fysiske avgangstransaksjonen. Transaksjonen 5b justeres mot den fysiske mottakstransaksjonen 3a. Systemet vil ikke utligne disse transaksjonene, fordi de ikke er økonomisk oppdatert. I stedet vil bare en justering med beløpet USD 3,75 gjøres i denne avgangstransaksjonen. Det nye glidende gjennomsnittet av kostprisen gjenspeiler gjennomsnittet av de økonomisk og fysisk oppdaterte transaksjonene, USD 20,00. 

Illustrasjonen nedenfor viser virkningene av LIFO-lagermodellen for denne transaksjonsserien når alternativet **Ta med fysisk verdi** brukes. ![LIFO med ta med fysisk verdi](./media/lifowithincludephysicalvalue.gif) 

**Nøkkel til diagrammet**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Quantity@Unitspris.
-   Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="lifo-with-marking"></a>LIFO med merking
Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres. La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Fordi dette er en hasteordre, må du betale en høyere pris for denne varen for å imøtekomme kundens forespørsel. 

Du må kontrollere at denne lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for denne salgsordrefakturaen. Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Hvis dette salgsordredokumentet merkes mot bestillingen før følgeseddelen eller fakturaen posteres, vil solgte varers kost (Vareforbruk) være USD 120,00, ikke det gjeldende glidende gjennomsnittet av varens kost. Hvis bestillingens følgeseddel eller faktura posteres før merkingen skjer, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen. 

Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres. 

Du kan merke en avgangstransaksjon mot en tilgang før transaksjonen er postert. Du kan gjøre dette fra en salgsordrelinje på siden **Salgsordredetaljer**. Du kan vise de åpne tilgangstransaksjonene på **Merking**-siden. 

Du kan også merke en avgangstransaksjon mot en tilgang etter transaksjonen er postert. Du kan samsvare eller merke en avgangstransaksjon for en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal. 

Illustrasjonen nedenfor viser disse transaksjonene:

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
-   7. Lagerlukking utføres. Siden den økonomisk oppdaterte FIFO-transaksjonen er merket mot en eksisterende tilgang, utlignes disse transaksjonene mot hverandre, og det gjøres ingen justering.

Det nye glidende gjennomsnittet av kostprisen gjenspeiler gjennomsnittet av de økonomisk og fysisk oppdaterte transaksjonene, USD 27,50. 

Illustrasjonen nedenfor viser virkningen LIFO-lagermodellen på denne transaksjonsserien når det brukes merking mellom avganger og tilganger. ![LIFO med merking](./media/lifowithmarking.gif) 

**Nøkkel til diagram**

-   Lagertransaksjoner vises med loddrette piler.
-   Mottak til lager vises med loddrette piler over tidslinjen.
-   Avganger fra lager vises med loddrette piler under tidslinjen.
-   Over (eller under) hver loddrett pil vises lagertransaksjonens verdi i formatet Quantity@Unitspris.
-   Hvis verdien av en lagertransaksjon vises mellom parenteser, betyr det at lagertransaksjonen er postert fysisk til lager.
-   Hvis verdien av en lagertransaksjon ikke vises mellom parenteser, betyr det at lagertransaksjonen er postert økonomisk til lager.
-   Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
-   Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
-   Lagerlukkinger vises med en rød linje med vannrette streker, og med etiketten *Lagerlukking*.
-   Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.






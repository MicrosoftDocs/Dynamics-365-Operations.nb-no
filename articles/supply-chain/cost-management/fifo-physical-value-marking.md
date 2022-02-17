---
title: FIFO med fysisk verdi og merking
description: FIFO (First in, First out - først inn, først ut) er en lagermodell der de første mottakene utstedes først. Økonomisk oppdaterte avganger fra lager utlignes mot de første økonomisk oppdaterte mottakene i lager, basert på den økonomiske datoen til lagertransaksjonen.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092146"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO med fysisk verdi og merking

[!include [banner](../includes/banner.md)]


FIFO (First in, first out - først inn, først ut) er en lagerstyrings- og vurderingsmetode der beholdning som produseres eller anskaffes først, selges, brukes eller avhendes først. Under lagerlukkingsprosessen i Microsoft Dynamics 365 Supply Chain Management oppretter systemet utligninger der det første mottaket sammenlignes med den første avgangen og så videre.

Utligningene og samsvarsprinsippet er basert på den økonomiske datoen til lagertransaksjonene. En foreløpig vurdering av utligningene og justeringene kan utføres ved å kjøre omberegningsprosessen for lager.

Du kan overstyre FIFO-prinsippet ved å merke lagertransaksjoner slik at et bestemt varemottak utlignes mot en bestemt avgang. En periodisk lagerlukking er nødvendig når du bruker FIFO-lagermodellen til å opprette utligninger og justere verdien av avganger i henhold til FIFO-prinsippet. Før du kjører lagerlukkingsprosessen, blir avgangstransaksjoner verdsatt med glidende gjennomsnitt da de fysiske og finansielle oppdateringene fant sted. Med mindre du bruker merking, beregnes glidende gjennomsnitt når den fysiske eller finansielle oppdateringen utføres. Eksemplene nedenfor viser effekten når FIFO brukes med tre forskjellige konfigurasjoner:

- FIFO når alternativet **Ta med fysisk verdi** ikke brukes
- FIFO når alternativet **Ta med fysisk verdi** brukes
- FIFO med merking

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO når alternativet Ta med fysisk verdi ikke brukes

I dette eksemplet er det ikke merket av for **Ta med fysisk verdi** i varemodellgruppen for det frigitte produktet. Illustrasjonen nedenfor viser disse transaksjonene:

- 1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
- 2b. Økonomisk lagertilgang av et antall på 1 til kost USD 22,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Fysisk lageravgang av et antall på 1 til kostpris USD 23,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner)
- 7\. Lagerlukking utføres. I samsvar med FIFO-metoden blir den først økonomisk oppdaterte avgangen utlignet mot den først økonomisk oppdaterte tilgangen, og så videre. I dette eksemplet opprettes det én utligning mellom 1b og 3b. En justering på USD -6,00 blir gjort for 3b, og den resulterende endelige kostnaden blir USD 10,00.

Det nye glidende gjennomsnittet for kostpris gjenspeiler gjennomsnittet for økonomisk oppdaterte transaksjoner. Illustrasjonene nedenfor viser virkningene av FIFO-lagermodellen for denne transaksjonsserien når alternativet **Ta med fysisk verdi** ikke brukes.

![FIFO når alternativet Ta med fysisk verdi ikke brukes.](./media/fifo-without-include-physical-value.png)

**Nøkkel til diagrammet**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over tidslinjen.
- Avganger fra lager vises med loddrette piler under tidslinjen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Hver dato i diagrammet er atskilt med en tynn, svart loddrett linje. Datoen er notert nederst i diagrammet.
- Lagerlukkinger vises med en rød linje med vannrette streker.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO når alternativet Ta med fysisk verdi brukes

Hvis det er merket av i avmerkingsboksen **Ta med fysisk verdi** for en vare på siden **Varemodellgruppe**, bruker systemet både fysiske og økonomiske tilgangstransaksjoner når det glidende gjennomsnittet av kostprisen beregnes. Der det er relevant, justerer systemet også den fysisk oppdaterte avgangstransaksjonen. Lagerlukking som bruker FIFO-lagermodellen, utligner bare transaksjoner som er økonomisk oppdatert. Illustrasjonen nedenfor viser disse transaksjonene:

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
- 7\. Lagerlukking utføres. I samsvar med FIFO-metoden blir den først økonomisk oppdaterte avgangen utlignet mot den først økonomisk oppdaterte tilgangen, og så videre. I dette eksemplet opprettes det én utligning mellom 1b og 3b. En justering på USD -6,00 blir gjort for 3b, og den resulterende endelige kostnaden blir USD 10,00. Transaksjonen 6a justeres i tillegg mot mottakstransaksjonskostnaden for 2b. Systemet vil ikke utligne disse transaksjonene, fordi mottaket bare oppdateres fysisk, ikke økonomisk. I stedet vil bare en justering på USD -1,67 posteres til den fysiske avgangstransaksjonen, og den resulterende justerte kostnaden vil bli USD 22,00.

![FIFO når alternativet Ta med fysisk verdi brukes.](./media/fifo-with-include-physical-value.png)

Legg merke til at resultatet av å kjøre lagerlukkingsprosessen er den samme, uansett om du velger alternativet **Ta med fysisk verdi** på siden **Varemodellgruppe**. Alternativet **Ta med fysisk verdi** påvirker bare glidende gjennomsnitt.

**Nøkkel til diagrammet**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over tidslinjen.
- Avganger fra lager vises med loddrette piler under tidslinjen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Hver dato i diagrammet er atskilt med en tynn, svart loddrett linje. Datoen er notert nederst i diagrammet.
- Lagerlukkinger vises med en rød linje med vannrette streker.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="fifo-with-marking"></a>FIFO med merking

Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres.

La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Fordi dette er en hasteordre, må du betale en høyere pris for denne varen for å imøtekomme kundens forespørsel. Du må kontrollere at lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for salgsordrefakturaen. Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Hvis salgsordredokumentet merkes mot bestillingen før følgeseddelen eller fakturaen posteres, vil solgte varers kost (Vareforbruk) være USD 120,00, ikke det gjeldende glidende gjennomsnittet av varens kost. Hvis bestillingens følgeseddel eller faktura posteres før merkingen skjer, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen. Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres.

Når en tilgangstransaksjon er merket mot en avgangstransaksjon, ses det bort fra vurderingsmetoden som er definert i varemodellgruppen, og systemet utligner disse transaksjonene mot hverandre. Du kan merke en transaksjon manuelt mot en salgsordrelinje på siden **Salgsordredetaljer** ved å velge **Beholdning \> Merking** på hurtigfanen **Salgsordrelinjer**. Du kan vise de åpne tilgangstransaksjonene på **Merking**-siden. Du kan samsvare eller merke en avgangstransaksjon til en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal. Illustrasjonen nedenfor viser disse transaksjonene:

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
- 6a. Fysisk lageravgang av et antall på 1 til kostpris USD 23,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner)
- 7\. Lagerlukking utføres. Basert på merkingsprinsippet som bruker FIFO-metoden, utlignes de merkede transaksjonene mot hverandre. I dette eksemplet utlignes 3b mot 2b, og en justering på USD 6,00 posteres til 3b for å få verdien til å bli USD 22,00. I dette eksemplet utføres ingen flere utligninger, fordi lukkingen oppretter utligninger bare for økonomisk oppdaterte transaksjoner.

Illustrasjonen nedenfor viser virkningen FIFO-lagermodellen på denne transaksjonsserien når det brukes merking mellom avganger og tilganger.

![FIFO med merking.](./media/fifo-with-marking.png)

**Nøkkel til diagrammet**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over tidslinjen.
- Avganger fra lager vises med loddrette piler under tidslinjen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Hver dato i diagrammet er atskilt med en tynn, svart loddrett linje. Datoen er notert nederst i diagrammet.
- Lagerlukkinger vises med en rød linje med vannrette streker.
- Utligninger og merkinger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra mottak til avgang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

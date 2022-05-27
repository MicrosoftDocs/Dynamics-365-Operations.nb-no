---
title: LIFO med fysisk verdi og merking
description: LIFO ("Last in, First out") er en lagermodell der de siste (nyeste) tilgangene tas ut først. Avganger fra lageret utlignes mot de siste mottakene til lageret, basert på datoen for lagertransaksjonen.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45316c40cce988c0758e70af627b0123ec1f7873
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670447"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO med fysisk verdi og merking

[!include [banner](../includes/banner.md)]

LIFO (Last in, first out - sist inn, først ut) er en lagerstyrings- og vurderingsmetode der beholdning som ble produsert eller anskaffet sist, selges, brukes eller avhendes først. Under lagerlukkingsprosessen i Microsoft Dynamics 365 Supply Chain Management oppretter systemet utligninger der det siste mottaket sammenlignes med den første avgangen og så videre. Utligningene og samsvarsprinsippet er basert på den økonomiske datoen til lagertransaksjonene. En foreløpig vurdering av utligningene og justeringene kan utføres ved å kjøre omberegningsprosessen for lager.

Du kan overstyre LIFO-prinsippet ved å merke lagertransaksjoner slik at et bestemt varemottak utlignes mot en bestemt avgang. En periodisk lagerlukking er nødvendig når du bruker LIFO-lagermodellen til å opprette utligninger og justere verdien av avganger i henhold til LIFO-prinsippet. Før du kjører lagerlukkingsprosessen, blir avgangstransaksjoner verdsatt med glidende gjennomsnitt da de fysiske og finansielle oppdateringene fant sted. Med mindre du bruker merking, beregnes glidende gjennomsnitt når den fysiske eller finansielle oppdateringen utføres.

Eksemplene nedenfor viser effekten når LIFO brukes med tre forskjellige konfigurasjoner:

- LIFO når alternativet **Ta med fysisk verdi** ikke brukes
- LIFO når alternativet **Ta med fysisk verdi** brukes
- LIFO med merking

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO når alternativet Ta med fysisk verdi ikke brukes

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
- 7\. Lagerlukking utføres. I samsvar med LIFO-metoden blir den først økonomisk oppdaterte avgangen utlignet mot den sist økonomisk oppdaterte tilgangen, og så videre. I dette eksemplet opprettes det én utligning mellom 5b og 3b. En justering på USD 14,00 blir gjort for 3b, og den resulterende endelige kostnaden blir USD 30,00.

Illustrasjonen nedenfor viser virkningene av FIFO-lagermodellen for denne transaksjonsserien når alternativet **Ta med fysisk verdi** ikke brukes.

![LIFO når alternativet Ta med fysisk verdi ikke brukes.](./media/lifo-without-including-physical-value.png)

**Nøkkel til diagrammet**

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

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO når alternativet Ta med fysisk verdi brukes

Hvis det er merket av i avmerkingsboksen **Ta med fysisk verdi** for en vare på siden **Varemodellgrupper**, bruker systemet både fysiske og økonomiske tilgangstransaksjoner når det glidende gjennomsnittet av kostprisen beregnes. Der det er relevant, justerer systemet også den fysisk oppdaterte avgangstransaksjonen. Hvis det ikke er merket av for boksen **Ta med fysisk verdi**, vil lagerlukking med LIFO-beholdningsmodellen bare utligne transaksjoner som er økonomisk oppdatert.

Illustrasjonen nedenfor viser disse transaksjonene:

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
- 7\. Lagerlukking utføres. I samsvar med LIFO-metoden blir den først økonomisk oppdaterte avgangen utlignet mot den sist økonomisk oppdaterte tilgangen, og så videre. I dette eksemplet opprettes det én utligning mellom 3b og 5b. En justering på USD 14,00 blir gjort for 3b, og den resulterende endelige kostnaden blir USD 30,00. Transaksjonen 6a justeres i tillegg mot mottakstransaksjonskostnaden for 4a. Systemet vil ikke utligne disse transaksjonene, fordi mottaket bare oppdateres fysisk, ikke økonomisk. I stedet vil bare en justering på USD 1,33 posteres til den fysiske avgangstransaksjonen, og den resulterende justerte kostnaden vil bli USD 25,00.

Illustrasjonen nedenfor viser virkningene av LIFO-lagermodellen for denne transaksjonsserien når alternativet **Ta med fysisk verdi** brukes.

![LIFO når alternativet Ta med fysisk verdi brukes.](./media/lifo-with-included-physical-value.png)

**Nøkkel til diagrammet**

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

## <a name="lifo-with-marking"></a>LIFO med merking

Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres. La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Fordi dette er en hasteordre, må du betale en høyere pris for varen for å imøtekomme kundens forespørsel.

Du må kontrollere at lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for salgsordrefakturaen. Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Hvis dette salgsordredokumentet merkes mot bestillingen før følgeseddelen eller fakturaen posteres, vil solgte varers kost (Vareforbruk) være USD 120,00, ikke det gjeldende glidende gjennomsnittet av varens kost. Hvis bestillingens følgeseddel eller faktura posteres før merkingen skjer, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen.

Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres.

Du kan merke en avgangstransaksjon mot en tilgang før transaksjonen er postert. Du kan utføre denne merkingen fra en salgsordrelinje på siden **Salgsordredetaljer** ved å velge **Beholdning \> Merking** på hurtigfanen **Salgsordrelinjer**. Du kan vise de åpne tilgangstransaksjonene på **Merking**-siden.

Du kan også merke en avgangstransaksjon mot en tilgang etter transaksjonen er postert. Du kan samsvare eller merke en avgangstransaksjon for en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal.

Illustrasjonen nedenfor viser disse transaksjonene:

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
- 7\. Lagerlukking utføres. Basert på merkingsprinsippet som bruker LIFO-metoden, utlignes de merkede transaksjonene mot hverandre. I dette eksemplet utlignes 3b mot 2b, og en justering på USD 6,00 posteres til 3b for å få verdien til å bli USD 22,00. I dette eksemplet utføres ingen flere utligninger, fordi lukkingen oppretter utligninger bare for økonomisk oppdaterte transaksjoner.

Det nye glidende gjennomsnittet av kostprisen gjenspeiler gjennomsnittet av de økonomisk og fysisk oppdaterte transaksjonene, USD 27,50.

Illustrasjonen nedenfor viser virkningen LIFO-lagermodellen på denne transaksjonsserien når det brukes merking mellom avganger og tilganger.

![LIFO med merking.](./media/lifo-with-marking.png)

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
- Utligninger og merkinger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra mottak til avgang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

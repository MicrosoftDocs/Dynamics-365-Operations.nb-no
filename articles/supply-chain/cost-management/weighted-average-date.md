---
title: Dato for avveid gjennomsnitt med Inkluder fysisk verdi og merking
description: Dato avveid gjennomsnitt er en lagermodell basert på avveid gjennomsnitt-prinsippet, hvor frigivelser fra lageret verdsettes til gjennomsnittsverdien av varene som er mottatt på lageret for hver separate dag i lageravslutningsperioden.
author: JennySong-SH
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1497cb08f4cc5a455c832b9bf125c309cd90aa3d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672129"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Dato for avveid gjennomsnitt med Inkluder fysisk verdi og merking

[!include [banner](../includes/banner.md)]

*Dato for avveid gjennomsnitt* er en lagermodell som er basert på et gjennomsnitt som beregnes ved å multiplisere hver komponent (varetransaksjon) med en faktor (kostpris) som gjenspeiler viktigheten (antallet) på hver dag i perioden. Denne lagermodellen tilordner med andre ord kostnaden for avgangstransaksjoner basert på gjennomsnittsverdien til alt lager som mottas hver dag, i tillegg til eventuell lagerbeholdning fra forrige dag.

Når du kjører en lagerlukking ved hjelp av lagermodellen for dato for avveid gjennomsnitt, kan to metoder brukes til å opprette en utligning. Vanligvis utlignes alle kvitteringene mot en virtuell avgang, som holder totalt mottatt antall og verdi. Denne virtuelle avgangen har et korresponderende virtuelt mottak som avgangene utlignes fra. På denne måten får alle avgangene samme gjennomsnittskostnad hver dag. Den virtuelle avgangen og det virtuelle mottaket kan betraktes som en virtuell overføring. Denne virtuelle overføringen kalles *lageravslutningsoverføring med avveid gjennomsnitt*. Denne utligningsmetoden er derfor kjent som en *summert utligning av avveid gjennomsnitt*. Hvis det bare er ett mottak, kan alle avgangene utlignes fra dette, og det opprettes ikke en virtuell overføring. Denne utligningsmetoden kalles *direkte utligning*. Eventuell lagerbeholdning som er til overs etter at lagerlukkingen er utført, verdsettes til det avveide gjennomsnittet fra siste dag i forrige periode og tas med i beregningen av dato for avveid gjennomsnitt i neste periode.

Du kan overstyre prinsippet for dato for avveid gjennomsnitt ved å merke lagertransaksjoner slik at et bestemt varemottak utlignes mot en bestemt avgang. En periodisk lagerlukking er nødvendig når du bruker lagermodellen for dato for avveid gjennomsnitt til å opprette utligninger og justere verdien av avganger i henhold til prinsippet for dato for avveid gjennomsnitt. Før du kjører lagerlukkingen, blir avgangstransaksjoner verdsatt med glidende gjennomsnitt da de fysiske og finansielle oppdateringene fant sted. Med mindre du bruker merking, beregnes glidende gjennomsnitt når den fysiske eller finansielle oppdateringen utføres.

Etterkalkuleringsmetoden for dato for avveid gjennomsnitt beregnes ved hjelp av følgende formel hver dag:

*Kostnad* = \[(*Q*<sub>*b*</sub> × *P*<sub>*b*</sub>) + &#x2211;<sub>*n*</sub>(*Q*<sub>*n*</sub> × *P*<sub>*n*</sub>)\] ÷ (*Q*<sub>*b*</sub> + &#x2211;<sub>*n*</sub>*Q*<sub>*n*</sub>)

- *Q* = transaksjonsantallet
- *P* = transaksjonsprisen

Den avveide gjennomsnittskostnaden er med andre ord lik startantallet ganger startprisen, pluss summen av hvert mottaksantall ganger mottaksprisen, alle delt på startantallet pluss summen av mottaksantallet.

Når lagerlukking pågår, utføres beregningen hver dag i hele lukkingsperioden.

> [!NOTE]
> For mer informasjon om utligninger, se [Lagerlukking](inventory-close.md).

Eksemplene nedenfor viser virkningene når dato for avveid gjennomsnitt brukes i fem konfigurasjoner:

- Direkte utligning med dato for avveid gjennomsnitt når alternativet **Ta med fysisk verdi** ikke brukes
- Summert utligning med dato for avveid gjennomsnitt når alternativet **Ta med fysisk verdi** ikke brukes
- Direkte utligning med dato for avveid gjennomsnitt når alternativet **Ta med fysisk verdi** brukes
- Summert utligning med dato for avveid gjennomsnitt når alternativet **Ta med fysisk verdi** brukes
- Dato for avveid gjennomsnitt når merking brukes

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Direkte utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi ikke brukes

Prinsippet for direkte utligning oppretter utligninger direkte mellom mottak og avganger uten å opprette flere lagertransaksjoner. Systemet bruker dette prinsippet for direkte utligning i følgende situasjoner:

- Når én tilgang og én eller flere avganger er postert i perioden.
- Når bare avganger er postert i perioden, og beholdningen inneholder varer fra en tidligere lagerlukning.

I dette eksemplet er det ikke merket av for **Ta med fysisk verdi** på siden **Varemodellgruppe** for det frigitte produktet. Diagrammet nedenfor viser disse transaksjonene:

**Dag 1:**

- 1a. Fysisk lagermottak av et antall på 10 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 10 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 10 til kost USD 20,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 10,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 10,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).

**Dag 2:**

- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Økonomisk lageravgang av et antall på 1 til en kostnad på USD 20,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).

**Dag 3:**

- 7\. Lagerlukking utføres. Systemet bruker metoden for direkte utligning fordi bare ett mottak blir økonomisk oppdatert 30. desember basert på metoden for dato avveid gjennomsnitt den 30. desember. I dette eksemplet opprettes det én utligning mellom transaksjon 1b og 3b. En justering på USD 10,00 for å bringe verdien av transaksjon 3b opp til 20,00. Ingen justering eller utligning foretas 31. desember fordi det ikke er noen økonomisk oppdaterte avganger på denne datoen.

Diagrammet nedenfor viser denne serien av transaksjoner og virkningen av å bruke lagermodellen for avveid gjennomsnitt og prinsippet for direkte utligning uten alternativet **Ta med fysisk verdi**.

![Direkte utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi ikke brukes.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Nøkkel til diagrammet:**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Datoer er atskilt med tynne, sorte, loddrette linjer. Datoene er notert nederst i diagrammet.
- Lagerlukkinger vises med en røde, vertikale og stiplede linjer.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Summert utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi ikke brukes

Når det forekommer flere mottak i en periode, bruker dato for avveid gjennomsnitt prinsippet for summert utligning der alle mottak i løpet av én dag summeres i en ny transaksjon kalt *avveid gjennomsnittlig lagerlukking*. Alle mottakene for dagen blir utlignet mot avgangen til den nylig opprettede lagertransaksjonen. Alle avganger for dagen blir utlignet mot mottaket av den nye lagertransaksjonen. Hvis det er lagerbeholdningsverdi til overs etter lagerlukkingen, tas lagerbeholdningsverdien med i mottakstransaksjonen for transaksjonene for avveid gjennomsnittlig lagerlukking.

Diagrammet nedenfor viser disse transaksjonene:

**Dag 1:**

- 1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
- 2b. Økonomisk lagertilgang av et antall på 1 til kost USD 22,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).

**Dag 2:**

- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Fysisk lageravgang av et antall på 1 til kostpris USD 23,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).

**Dag 3:**

- 7\. Lagerlukking utføres.
- 7a. Den økonomiske avgangen Lagerlukkingstransaksjon for avveid gjennomsnitt opprettes for å summere utligningene av alle de økonomiske lagermottakene.

    - Transaksjon 1b utlignes for et antall på 1 med et utlignet beløp på USD 10,00.
    - Transaksjon 2b utlignes for et antall på 1 med et utlignet beløp på USD 22,00.
    - Transaksjon 7a utlignes for et antall på 2 med et utlignet beløp på USD 32,00. Denne transaksjonen motposterer summen av de to mottakstransaksjonene som oppdateres økonomisk i perioden.

- 7b. Det opprettes en økonomisk tilgang til avveid gjennomsnitt av verdien for lagerlukkingstransaksjonen, som brukes til å utligne økonomisk posterte avganger.

    - Transaksjon 3b utlignes for et antall på 1 med et utlignet beløp på USD 16,00. Transaksjonen justeres ikke, fordi den er det avveide gjennomsnittet av økonomisk posterte transaksjoner den 1. desember.
    - Transaksjon 7b opprettes for et antall på 2 med et økonomisk beløp på USD 32,00 og et utlignet beløp på USD 16,00 for å motpostere transaksjon 3b. Denne transaksjonen motposterer summen av den ene avgangstransaksjon som oppdateres økonomisk i perioden. Transaksjonen forblir åpen fordi det fremdeles er én tilgjengelig.

Diagrammet nedenfor viser denne serien av transaksjoner og virkningen av å bruke lagermodellen for avveid gjennomsnitt og prinsippet for summert utligning, men uten å bruke alternativet **Ta med fysisk verdi**.

![Summert utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi ikke brukes.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Nøkkel til diagrammet:**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Datoer er atskilt med tynne, sorte, loddrette linjer. Datoene er notert nederst i diagrammet.
- Lagerlukkinger vises med en røde, vertikale og stiplede linjer.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Direkte utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi brukes

I den gjeldende versjonen av produktet fungerer alternativet **Ta med fysisk verdi** på en annen måte med lagermodellen for dato for avveid gjennomsnitt enn i tidligere versjoner. Når du merker av for **Ta med fysisk verdi** for en vare på siden **Varemodellgruppe**, bruker systemet fysisk oppdaterte tilganger når den estimerte varekostprisen eller glidende gjennomsnitt beregnes. Avganger blir postert på grunnlag av denne estimerte kostprisen for perioden. Under lagerlukkingen tas det bare hensyn til økonomisk oppdaterte tilganger når avveid gjennomsnitt beregnes.

Diagrammet nedenfor viser disse transaksjonene:

**Dag 1:**

- 1a. Fysisk lagermottak av et antall på 10 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 10 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 10 til kost USD 20,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 15,00 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 15,00 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).

**Dag 2:**

- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Fysisk lageravgang av et antall på 1 til en kostnad på USD 21,25 per stykk (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).

**Dag 3:**

- 7\. Lagerlukking utføres. Systemet bruker metoden for direkte utligning fordi bare ett mottak blir økonomisk oppdatert 30. desember basert på metoden for dato avveid gjennomsnitt den 30. desember. I dette eksemplet opprettes det én utligning mellom transaksjon 1b og 3b. Ingen justering blir gjort for avgangen den 30.12. I tillegg foretas ingen justering eller utligning 31. desember fordi det ikke er noen økonomisk oppdaterte avganger på denne datoen.

Diagrammet nedenfor viser denne serien av transaksjoner og virkningen av å bruke lagermodellen for avveid gjennomsnitt og prinsippet for direkte utligning med alternativet **Ta med fysisk verdi**.

![Direkte utligning for avveid gjennomsnitt med Ta med fysisk verdi.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Nøkkel til diagrammet:**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Datoer er atskilt med tynne, sorte, loddrette linjer. Datoene er notert nederst i diagrammet.
- Lagerlukkinger vises med en røde, vertikale og stiplede linjer.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Summert utligning med dato for avveid gjennomsnitt når alternativet Ta med fysisk verdi brukes

I den gjeldende versjonen av produktet fungerer alternativet **Ta med fysisk verdi** på en annen måte med avveid gjennomsnitt enn i tidligere versjoner. Når du merker av for **Ta med fysisk verdi** for en vare på siden **Varemodellgruppe**, bruker systemet fysisk oppdaterte tilganger når den estimerte kostprisen eller glidende gjennomsnitt beregnes. Avganger blir postert på grunnlag av denne estimerte kostprisen for perioden. Under lagerlukkingen tas det bare hensyn til økonomisk oppdaterte tilganger når avveid gjennomsnitt beregnes. Det anbefales at du utfører en månedelig lagerlukking når du bruker lagermodellen for avveid gjennomsnitt. I dette eksemplet med summert utligning av dato for avveid gjennomsnitt, er lagermodellen merket for å ta med fysisk verdi.

Diagrammet nedenfor viser disse transaksjonene:

**Dag 1:**

- 1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
- 2b. Økonomisk lagertilgang av et antall på 1 til kost USD 22,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 16,00 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 16,00 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).

**Dag 2:**

- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Fysisk lageravgang av et antall på 1 til kostpris USD 23,67 (glidende gjennomsnitt av fysiske og økonomisk posterte transaksjoner).

**Dag 3:**

- 7\. Lagerlukking utføres.
- 7a. Den økonomiske avgangen Lagerlukkingstransaksjon for avveid gjennomsnitt opprettes for å summere utligningene av alle de økonomiske lagermottakene.

    - Transaksjon 1b utlignes for et antall på 1 med et utlignet beløp på USD 10,00.
    - Transaksjon 2b utlignes for et antall på 1 med et utlignet beløp på USD 22,00.
    - Transaksjon 7a utlignes for et antall på 2 med et utlignet beløp på USD 32,00. Denne transaksjonen motposterer summen av de to mottakstransaksjonene som oppdateres økonomisk i perioden.

- 7b. Det opprettes en økonomisk tilgang til avveid gjennomsnitt av verdien for lagerlukkingstransaksjonen, som brukes til å utligne økonomisk posterte avganger.

    - Transaksjon 3b utlignes for et antall på 1 med et utlignet beløp på USD 16,00. Transaksjonen justeres ikke, fordi den er det avveide gjennomsnittet av økonomisk posterte transaksjoner den 1. desember.
    - Transaksjon 7b opprettes for et antall på 2 med et økonomisk beløp på USD 32,00 og et utlignet beløp på USD 16,00 for å motpostere transaksjon 3b. Denne transaksjonen motposterer summen av den ene avgangstransaksjon som oppdateres økonomisk i perioden. Transaksjonen forblir åpen fordi det fremdeles er én tilgjengelig.

Diagrammet nedenfor viser denne serien av transaksjoner og virkningen av å bruke lagermodellen for avveid gjennomsnitt og prinsippet for summert utligning uten alternativet **Ta med fysisk verdi**.

![Summert utligning for avveid gjennomsnitt med Ta med fysisk verdi.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Nøkkel til diagrammet:**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Datoer er atskilt med tynne, sorte, loddrette linjer. Datoene er notert nederst i diagrammet.
- Lagerlukkinger vises med en røde, vertikale og stiplede linjer.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

## <a name="weighted-average-date-when-marking-is-used"></a>Dato for avveid gjennomsnitt når merking brukes

Merking er en prosess som lar deg koble, eller merke, en avgangstransaksjon til en tilgangstransaksjon. Merking kan skje enten før eller etter at en transaksjon posteres. Du kan bruke merking når du vil være sikker på at du kjenner den nøyaktige lagerkostnaden når transaksjonen posteres eller når lagerlukking utføres.

La oss si at kundeserviceavdelingen godtar en hasteordre fra en viktig kunde. Siden dette er en hasteordre, blir du nødt til å betale en høyere pris for denne varen for å betjene kundens forespørsel. Du må kontrollere at denne lagerkostnaden gjenspeiles i bidraget, eller kostnader for solgte varer (Vareforbruk), for denne salgsordrefakturaen.

Når bestillingen posteres, skjer tilgangen til lager med en kost på USD 120,00. Hvis salgsordredokumentet merkes mot bestillingen før følgeseddelen eller fakturaen posteres, vil solgte varers kost (Vareforbruk) være USD 120,00, i stedet for det gjeldende glidende gjennomsnittet av varens kost. Hvis merkingen inntreffer etter bestillingens følgeseddel eller faktura er postert, vil solgte varers kost posteres med det glidende gjennomsnittet av kostprisen.

Disse to transaksjonene kan merkes mot hverandre helt til lagerlukkingen utføres.

Hvis en tilgangstransaksjon er merket mot en avgangstransaksjon, ses det bort fra vurderingsmetoden som er valgt for varens varemodellgruppe, og systemet utligner disse transaksjonene mot hverandre.

Du kan merke en avgangstransaksjon mot en tilgang før transaksjonen er postert. Du kan gjøre denne markeringen fra en salgsordrelinje på siden **Salgsordredetaljer**. De åpne tilgangstransaksjonene vises på **Merking**-siden.

Du kan også merke en avgangstransaksjon mot en tilgang etter transaksjonen er postert. Du kan samsvare eller merke en avgangstransaksjon for en åpen mottakstransaksjon for en lagervare fra en postert lagerjusteringsjournal.

Diagrammet nedenfor viser disse transaksjonene:

**Dag 1:**

- 1a. Fysisk lagermottak av et antall på 1 til kost USD 10,00 per stykk.
- 1b. Økonomisk lagertilgang av et antall på 1 til kost USD 10,00 per stykk.
- 2a. Fysisk lagermottak av et antall på 1 til kost USD 20,00 per stykk.
- 2b. Økonomisk lagertilgang av et antall på 1 til kost USD 22,00 per stykk.
- 3a. Fysisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3b. Økonomisk lageravgang av et antall på 1 til kostpris USD 16,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).
- 3c. Økonomisk lageravgang for transaksjon 3b er merket mot økonomisk lageravgang for transaksjon 2b.

**Dag 2:**

- 4a. Fysisk lagermottak av et antall på 1 til kost USD 25,00 per stykk.
- 5a. Fysisk lagermottak av et antall på 1 til kost USD 30,00 per stykk.
- 5b. Økonomisk lagertilgang av et antall på 1 til kost USD 30,00 per stykk.
- 6a. Fysisk lageravgang av et antall på 1 til kostpris USD 23,00 per stykk (glidende gjennomsnitt av økonomisk posterte transaksjoner).

**Dag 3:**

- 7\. Lagerlukking utføres. Basert på merkingsprinsippet som bruker metoden for avveid gjennomsnitt, utlignes de merkede transaksjonene mot hverandre. I dette eksemplet utlignes transaksjon 3b mot transaksjon2b, og en justering på USD 6,00 posteres til transaksjon 3b for å få verdien til å bli USD 22,00. I dette eksemplet utføres ingen flere utligninger, fordi lukkingen oppretter utligninger bare for økonomisk oppdaterte transaksjoner.

Diagrammet nedenfor viser denne serien av transaksjoner og virkningen av å bruke lagermodellen med avveid gjennomsnitt med merking.

![Avveid gjennomsnitt med merking.](media/weighted-average-date-with-marking.png)

**Nøkkel til diagrammet:**

- Lagertransaksjoner vises med loddrette piler.
- Fysiske transaksjoner vises med kortere lysegrå piler.
- Økonomiske transaksjoner representeres med lengre sorte piler.
- Mottak til lager vises med loddrette piler over aksen.
- Avganger fra lager vises med loddrette piler under aksen.
- Hver ny mottaks- eller avgangstransaksjon merkes med en ny etikett.
- Hver loddrett pil har en etikett med en sekvensiell ID, for eksempel *1a*. ID-ene viser i hvilken rekkefølge lagertransaksjonene posteres.
- Datoer er atskilt med tynne, sorte, loddrette linjer. Datoene er notert nederst i diagrammet.
- Lagerlukkinger vises med en røde, vertikale og stiplede linjer.
- Utligninger som skjer før lagerlukking, vises med prikkede røde diagonale prikkede piler som går diagonalt fra tilgang til avgang.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

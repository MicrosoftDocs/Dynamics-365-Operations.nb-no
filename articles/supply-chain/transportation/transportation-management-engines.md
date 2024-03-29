---
title: Transportbehandlingsmotorer
description: Transportbehandlingsmotorer definerer logikken som brukes til å generere og behandle transportsatser i transportbehandling.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4a49ed7a91ec9a1b89564d40bef38cc4ea45532
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669607"
---
# <a name="transportation-management-engines"></a>Transportbehandlingsmotorer

[!include [banner](../includes/banner.md)]

Transportbehandlingsmotorer definerer logikken som brukes til å generere og behandle transportsatser i transportbehandling. 

En transportbehandlingsmotor beregner oppgaver, for eksempel transportørens transportsats. Med motorsystemet kan du endre beregningsstrategier under kjøring, basert på data i Supply Chain Management. En transportbehandlingsmotor ligner en plugin-modul som er relatert til en bestemt transportørkontrakt.

## <a name="what-engines-are-available"></a>Hvilke motorer er tilgjengelige?
Tabellen nedenfor viser transportbehandlingsmotorene som er tilgjengelige.

| Transportbehandlingmotor | Beskrivelse                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ratemotor**                  | Beregn satser.                                                                                                                                                                                                                                                                                                           |
| **Generell motor**               | Enkle hjelpemotorer som brukes av andre søkemotorer som ikke krever data fra Supply Chain Management, for eksempel en fordelingsmotor. Fordelingsmotorer brukes til å redusere de endelige kostnadene for transport for bestemte ordrer og linjer, basert på dimensjoner, for eksempel volum og vekt. |
| **Kjørelengdemotor**               | Beregner transportavstanden.                                                                                                                                                                                                                                                                                     |
| **Transittidmotor**          | Beregner tiden det tar å reise fra startstedet til bestemmelsesstedet.                                                                                                                                                                                                                                       |
| **Sonemotor**                  | Beregner sonen basert på gjeldende adresse, og beregner antall soner som må krysses for å reise fra adresse A til adresse B.                                                                                                                                                                    |
| **Fraktbrevtype**            | Standardiserer fraktfakturaen og fraktbrevlinjene og brukes til automatisk fraktbrevsamsvar.                                                                                                                                                                                                                |


## <a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Hvilke motorer må konfigureres for å vurdere en forsendelse?

Hvis du vil rangere en forsendelse ved hjelp av en bestemt leverandør, må du konfigurere flere transportbehandlingsmotorer. **Ratemotor** er obligatorisk, men andre transportbehandlingsmotorer kan være nødvendige for å støtte **Ratemotor**. **Ratemotoren** kan for eksempel brukes til å hente data fra **kjørelengdemotoren** for beregning av satsen basert på antall kilometer mellom kilden og målet.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Hva kreves for å initialisere en transportbehandlingsmotor?
En transportbehandlingsmotor krever at du definerer initialiseringsdata for å fungere på en bestemt måte. Oppsettet kan inneholde følgende typer data:
-   Referanser til andre motorer for transportbehandling. Hvis du vil ha mer informasjon, kan du se konfigurasjonseksemplet i denne delen.
-   Referanser til .NET-typer som brukes av transportbehandlingsmotoren.
-   Enkle konfigurasjonsdata.

I de fleste tilfeller kan du klikke **Parametere**-knappen i oppsettskjemaene for transportbehandlingsmotoren for å konfigurere initialiseringsdataene. **Eksempel på konfigurasjon av en ratemotor som refererer til en kjørelengdemotor** Eksemplet nedenfor viser oppsettet som kreves for en ratemotor som er basert på .NET-motortypen Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine og refererer til en kjørelengdemotor.

|          Parameter           |                                                                                  Beskrivelse                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>RateBaseAssigner</em>   | .NET-typen som tolker dataene for tilordning av satsgrunnlag for et bestemt skjema. Syntaksen for parameterverdien består av to segmenter som er avgrenset av en loddrett strek ( |
|  <em>MileageEngineCode</em>  |                       Kode for kjørelengdemotor som identifiserer posten for kjørelengdemotor i databasen.                        |
| <em>ApportionmentEngine</em> |                        Kode for generell motor som identifiserer fordelingsmotoren i databasen.                        |

## <a name="how-is-metadata-used-in-transportation-management-engines"></a>Hvordan brukes metadata i transportbehandlingsmotorer?

Transportbehandlingsmotorer som er avhengige av data som er definert i Supply Chain Management kan bruke forskjellige dataskjemaer. Transportbehandlingssystemet aktiverer ulike transportbehandlingsmotorer til å bruke de samme generelle fysiske databasetabellene. Hvis du vil sikre at kjøretidstolkingen av motordataene er riktig, kan du definere metadata for databasetabellene. Dette reduserer kostnadene ved bygging av nye transportbehandlingsmotorer fordi flere tabell- og skjemastrukturer ikke er nødvendig i Operations.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Hva kan brukes som søkedata i satsberegninger?
Dataene som du bruker når du beregner satser, kontrolleres av metadatakonfigurasjonen. Hvis du for eksempel vil søke etter satser basert på postnumre, må du definere metadata som er basert på oppslagstypen for et postnummer.

## <a name="do-all-engine-configurations-require-metadata"></a>Krever alle motorkonfigurasjoner metadata?
Nei, transportbehandlingsmotorer som brukes til å hente dataene som kreves for satsberegning fra eksterne systemer, trenger ikke metadata. Satsdataene for disse motorene kan hentes fra eksterne transportsystemer, vanligvis via en webtjeneste. Du kan for eksempel bruke en kjørelengdemotor som henter data direkte fra Bing-kart, slik at du ikke trenger et metadata for denne motoren.

| **Obs!**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transportbehandlingsmotorer som leveres med Supply Chain Management, bruker data som hentes fra programmet. Søkemotorer som kobler til eksterne systemer, er ikke inkludert i Operations. Den motorbaserte utvidelsesmodellen lar deg imidlertid bygge tillegg ved hjelp av Visual Studio Tools. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Hvordan konfigurerer jeg metadataene for en transportbehandlingsmotor?
Metadata for transportbehandlingsmotorer konfigureres forskjellig for ulike typer motorer.

| Transportbehandlingmotor               | Metadatakonfigurasjon                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ratemotor**                                | Krever en **satsgrunnlagstype**. Satsgrunnlagstypen inneholder metadata for satsstamdataene og data for tilordning av satsgrunnlag. Strukturen til metadata for vurderingsgrunnlagstype bestemmes av ratemotoren. Strukturen til metadata for vurderingsgrunnlagstype bestemmes av typen satsgrunnlagstilordner som er tilknyttet denne ratemotoren. Du definerer satsgrunnlagstypen for en ratemotor på **Ratemotor**-siden og **Vurderingsstandard**-siden. |
| **Sonemotor**                                | Krever at metadata konfigureres direkte i sonemalen.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Transittidmotor** og **Kjørelengdemotor** | Henter metadataene direkte fra kjørelengdemotorens skjema for konfigurasjonsoppsett.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Eksempel på metadata for en ratemotor** Transportbehandlingsmotoren krever identifikasjon av den opprinnelige adressen, målfylke og land/region, og start- og sluttpunktet for forsendelsen. Når disse kravene brukes, ser metadataene ut som dataene i tabellen nedenfor. Tabellen inneholder også informasjon om hvilken type inndata som kreves.
-   Definer denne informasjonen i **Transportstyring** &gt; **Oppsett** på siden **Vurderingsgrunnlagstype**.

| Rekkefølge | Navn                          | Felttype | Datatype | Oppslagstype    | Obligatorisk |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Avsenders postnummer            | Tildeling | Streng    | Postnummer    | Valgt  |
| 2        | Målfylke             | Tildeling | Streng    | Statlig          |           |
| 3        | Første målpostnummer | Tildeling | Streng    | Postnummer    | Valgt  |
| 4        | Siste målpostnummer   | Tildeling | Streng    | Postnummer    | Valgt  |
| 5        | Målland           | Tildeling | Streng    | Land/område |           |

### <a name="whitepaper"></a>Hvitbok

Hvis du vil ha mer informasjon, kan du laste ned følgende hvitbok (skrevet for å støtte AX2012, men gjelder fortsatt for Dynamics 365 Supply Chain Management)

- [Transportstyringsmotorer](https://download.microsoft.com/download/e/0/9/e0957665-c12f-43c7-94c0-611cc49d7d61/TransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Arbeidsområde for leverandørbetalinger
description: Dette emnet gir informasjon om det mobile arbeidsområdet for leverandørbetalinger. Arbeidsområdet for leverandørbetalinger viser informasjon som er knyttet til behandling av leverandørbetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 03fd290f8ad780e740a8fe6552c7a64c44b65a67
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "346117"
---
# <a name="vendor-payments-workspace"></a>Arbeidsområde for leverandørbetalinger

[!include [banner](../includes/banner.md)]

Arbeidsområdet for **leverandørbetalinger** viser informasjon som er knyttet til behandling av leverandørbetalinger. Arbeidsområdet inneholder en **Mitt arbeid**-visning og en **Analyse**-side. **Mitt arbeid**-visningen viser sammendragsfliser, rutenett for leverandørtransaksjoner og tilknyttet leverandørinformasjon. **Analyse**-siden bruker funksjonene i Microsoft Power BI for å vise bilder som er knyttet til leverandørbetalinger.

## <a name="my-work-view"></a>Mitt arbeid-visning

### <a name="summary-tiles"></a>Sammendrag-fliser

Rutene i delen **Sammendrag** gir en oversikt over tilstanden for betalingsinformasjonen. Du kan se betalingsjournaler som ennå ikke er postert, fakturaer som er forfalt, alle leverandører og leverandører som er satt på vent. Fra **Sammendrag**-delen kan du opprette en ny betalingskjøring.

Informasjonen i **Sammendrag**-delen er for firmaet som du er logget på.

### <a name="vendor-transactions-grids"></a>Rutenett for leverandørtransaksjoner

Delen **Leverandørtransaksjoner** inneholder rutenett som viser fakturaene som har forfalt og betalinger som ikke er utlignet. Fra **Forfalte fakturaer**-rutenettet kan du vise utligningshistorikken for en valgt faktura. Fra **Forfalte fakturaer**-rutenettet kan du vise utligningshistorikken for en valgt faktura og utligne en faktura.

Medarbeidere for sentralisert betaling kan bruke et filter som vises øverst i hvert rutenett, til å velge et firma. Rutenettet blir deretter filtrert slik at det viser bare firmaer som er definert i organisasjonshierarkiet for sentralisert betaling, som medarbeideren for sentralisert betaling har rettigheter til å vise.

Kategorien **Søk etter transaksjoner** i **Leverandørtransaksjoner**-delen lar deg søke etter en leverandørtransaksjon.

### <a name="related-information"></a>Beslektet informasjon

Du kan vise rapporten **Aldersfordeling for leverandør** og rapporten **Utbetalingsoppsummering etter dato** ved hjelp av koblingene i **Relatert informasjon**-delen i arbeidsområdet.

## <a name="analytics-page"></a>Analyse-side

**Analyse**-siden inneholder viktige mål, for eksempel leverandørfakturaer som har forfalt, og leverandørfakturaer som forfaller i fremtiden. Denne siden inneholder ni rapportsider. Én side gir en oversikt, og de andre åtte sidene inneholder opplysninger om leverandørbetalingsmål.

Tabellen nedenfor viser visuaiseringene som er tilgjengelig på hver rapportside.


|            Rapportside            |                                                                                                                                                                                Visualisering                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Oversikt over leverandørbetalinger      | <ul><li>Forfalte fakturaer</li><li>Fakturaer som forfaller i dag</li><li>Innvilgede rabatter mot rabatter tapt</li><li>Fakturaer som forfaller i fremtiden, etter kontantrabattdato</li><li>Fakturaer som forfaller i fremtiden, etter forfallsdato</li><li>Fakturaer betalt for sent sammenlignet med fakturaer som er betalt i tide</li><li>Tilordning av betalingsarbeidsflyt</li><li>Saldo for leverandør mot kunde</li><li>Åpne fakturaer med betalingssperre</li></ul> |
|         Forfalte fakturaer         |                                                                                             <ul><li>Forfalte fakturaer</li><li>Detaljer om forfalte fakturaer</li><li>Totalt antall åpne fakturaer</li><li>Forfalte fakturaer per leverandørgruppe</li><li>Forfalte fakturaer per firma</li></ul>                                                                                              |
|        Fakturaer som forfaller i dag         |                                                                                                         <ul><li>Fakturaer som forfaller i dag</li><li>Detaljer om fakturaer som forfaller i dag</li><li>Fakturaer som forfaller i dag per firma</li><li>Fakturaer som forfaller i dag per leverandørgruppe</li></ul>                                                                                                          |
| Innvilgede rabatter mot rabatter tapt |                                                                             <ul><li>Innvilgede rabatter mot rabatter tapt</li><li>Detaljer om innvilgede rabatter mot rabatter tapt</li><li>Innvilgede rabatter mot rabatter tapt per firma</li><li>Innvilgede rabatter mot rabatter tapt per leverandørgruppe</li></ul>                                                                              |
|      Fakturaer som forfaller i fremtiden       |                                                 <ul><li>Fakturaer som forfaller i fremtiden</li><li>Detaljer om fakturaer som forfaller i fremtiden</li><li>Fakturaer som forfaller i fremtiden per firma</li><li>Fakturaer som forfaller i fremtiden per leverandørgruppe</li><li>Fakturaer som forfaller i fremtiden, etter kontantrabattdato</li><li>Fakturaer som forfaller i fremtiden, etter forfallsdato</li></ul>                                                  |
|        Fakturaer betalt for sent         |                                                         <ul><li>Fakturaer betalt etter forfallsdato</li><li>Detaljer om fakturaer betalt etter forfallsdato</li><li>Fakturaer betalt etter forfallsdato per firma</li><li>Fakturaer betalt etter forfallsdato per leverandørgruppe</li><li>Fakturaer betalt for sent sammenlignet med fakturaer som er betalt i tide</li></ul>                                                          |
|         Arbeidsflyt for betalinger          |                                                                                <ul><li>Arbeidsflytforekomster for leverandørbetalinger</li><li>Arbeidsflytforekomster for leverandørbetalinger per godkjenner</li><li>Arbeidsflytforekomster for leverandørbetalinger per firma</li><li>Gjennomsnittlig antall dager i arbeidsflyt etter godkjenner</li></ul>                                                                                |
|    Saldo for leverandør mot kunde     |                                                                                                                   <ul><li>Saldo for leverandør mot kunde</li><li>Saldo for leverandør mot kunde per firma</li><li>Detaljer om saldo for leverandør mot kunde</li></ul>                                                                                                                    |
|    Fakturaer med betalingssperre     |                                                                                         <ul><li>Fakturaer med betalingssperre</li><li>Detaljer om fakturaer med betalingssperre</li><li>Fakturaer med betalingssperre per firma</li><li>Fakturaer med betalingssperre per leverandørgruppe</li></ul>                                                                                          |


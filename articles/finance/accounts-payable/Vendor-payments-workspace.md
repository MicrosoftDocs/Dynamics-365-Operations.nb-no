---
title: Arbeidsområde for leverandørbetalinger
description: Denne artikkelen gir informasjon om det mobile arbeidsområdet for leverandørbetalinger. Arbeidsområdet for leverandørbetalinger viser informasjon som er knyttet til behandling av leverandørbetalinger.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6463e25fdcbc77dacc286460f3acd30ccc3d6e86
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847038"
---
# <a name="vendor-payments-workspace"></a>Arbeidsområde for leverandørbetalinger

[!include [banner](../includes/banner.md)]

Arbeidsområdet for **leverandørbetalinger** viser informasjon som er knyttet til behandling av leverandørbetalinger. Arbeidsområdet inneholder en **Mitt arbeid**-visning og en **Analyse**-side. **Mitt arbeid**-visningen viser sammendragsfliser, rutenett for leverandørtransaksjoner og tilknyttet leverandørinformasjon. Siden **Analyse** bruker funksjonene i Microsoft Power BI til å vise bilder som er knyttet til leverandørbetalinger.

## <a name="setup-needed-to-view-power-bi-content"></a>Oppsett måtte vise Power BI-innhold

Følgende oppsett må fullføres for at data skal kunne vises i Power BI-visualobjekter for **Leverandørbetalinger**.
1. Gå til **Systemadministrasjon > Oppsett > Systemparametere** for å angi **Systemvaluta** og **Valutakurs for system**.
2. Gå til **Økonomi > Kalendere > Regnskapskalendere** for å validere regnskapskalenderdatoer som er tilordnet den aktive tidsperioden.
3. Gå til **Økonomimodul > Oppsett > Finans** for å angi **Regnskapsvaluta** og **Type valutakurs**. 
4. Definer valutakurser mellom transaksjonsvalutaer og regnskapsvaluta og regnskapsvaluta og systemvaluta. Du kan gjøre dette ved å gå til **Økonomimodul > Valutaer > Valutakurser**.
5. Gå til **Systemadministrasjon > Oppsett > Enhetslager** for å oppdatere den aggregerte målingen **VendPaymentBIMeasureV2**.

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
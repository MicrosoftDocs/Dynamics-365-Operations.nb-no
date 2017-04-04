---
title: "Kjøp Forbruksanalyse Power BI-innhold"
description: "Dette emnet beskriver hva som er inkludert i kjøpet bruker analyse content pack for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert i innhold pack, og gir informasjon om datamodell og enheter som brukes til å lage innhold pack."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Kjøp Forbruksanalyse Power BI-innhold

Dette emnet beskriver hva som er inkludert i kjøpet bruker analyse content pack for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert i innhold pack, og gir informasjon om datamodell og enheter som brukes til å lage innhold pack.

<a name="overview"></a>Oversikt
--------

Kjøp bruker analyse content pack for Microsoft Power BI ble opprettet for å kjøpe ressursansvarlige og ledere som er ansvarlig for budsjetter. Den er utformet for å hjelpe dem med å holde øye med kjøp utgifter. Den bruker kjøp transaksjonsdata fra Microsoft Dynamics 365 for operasjoner, og gir både en aggregert visning av firmaet kjøp tallene og en analyse av kjøp utgifter etter leverandør og vare. Rapporter merke endringer i innkjøp utgifter over tid. Derfor kan de brukes til å varsle ledere om positive og negative utgifter trender for individuelle leverandører og produkter. Stolpediagrammer viser kjøp utgifter for forskjellige innkjøpskategorier og leverandørgrupper. Kategori og regionale ledere kan det være nyttig å bruke disse diagrammene til å identifisere endringer i virkemåten for utgifter. Content pack vi innkjøpssjefer og ledere som er ansvarlig for budsjetter analysere kjøp utgifter på følgende måter:

-   Kjøp hittil i år (ved leverandørgruppen og individuelle leverandører, innkjøpskategorien og enkeltprodukter og leverandør plassering)
-   Endre år-over-år bestillinger (etter leverandør-gruppen og innkjøp kategori)

## <a name="accessing-the-content-pack"></a>Tilgang til innhold pack
Kjøp bruker analyse innhold pack er publisert som et anleggsmiddel for implementeringen i Microsoft Dynamics Lifecycle tjenester (LCS) og er tilgjengelig fra Microsoft Dynamics 365 for operasjoner. Hvis du vil ha mer informasjon om hvordan du access og åpne strømmen BI-rapporter, se [strømmen BI-innhold i LCS fra Microsoft og partnere på](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Mål som er inkludert i innhold pack
Kjøp bruker analyse innhold pack inneholder en rapport som består av et sett med mål. Disse mål er visualized som tabeller, diagrammer og fliser. Tabellen nedenfor gir en oversikt over effekter i innhold pack.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Rapportside</th>
<th>Diagrammer</th>
<th>Side ved side</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kjøp etter leverandør</td>
<td><ul>
<li>De 10 viktigste leverandørene ved kjøp (stablet liggende stolpediagram)</li>
<li>Total innkjøp etter leverandør gruppe / land / navn (sektordiagram)</li>
<li>Innkjøp etter leverandør gruppe / land / navn (kolonnediagram)</li>
<li>Gjennomsnittlig innkjøp etter leverandør gruppe / land / navn (kolonnediagram)</li>
</ul></td>
<td><ul>
<li>Totale innkjøp</li>
<li>YOY kjøp vekst</li>
<li>Totalt # leverandører</li>
<li>Totalt antall aktive leverandører</li>
</ul></td>
</tr>
<tr class="even">
<td>Kjøp av produktet</td>
<td><ul>
<li>Kjøp etter innkjøpskategori / product name (kolonnediagram)</li>
<li>Totalt kjøp etter innkjøpskategori / product name (sektordiagram)</li>
<li>Topp 10 produkter etter kjøpet (stablet liggende stolpediagram)</li>
</ul></td>
<td><ul>
<li>Totalt antall produkter</li>
<li>Totalt antall aktive produkter prosent av totalt antall produkter</li>
<li>Antall produkter regnskap for 80 % kjøp</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kjøp av perioden *</td>
<td><ul>
<li>Kjøp etter måned / dag (kolonnediagram)</li>
<li>Kumulativ YOY kjøpsavvik (foss diagram)</li>
<li>Totalt kjøp YOY vekst (kolonnediagram)</li>
<li>Innkjøp-setning (matrise)</li>
</ul></td>
<td><ul>
<li>YOY kjøp vekst</li>
<li>YOY kjøp vekst %</li>
</ul></td>
</tr>
<tr class="even">
<td>Kjøp etter leverandør plassering</td>
<td><ul>
<li>Kjøp etter poststed</li>
<li>Kjøp YOY vekst %</li>
<li>Kjøp etter land</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Kjøp forbruk analyse etter tid</td>
<td><ul>
<li>Kjøp inneværende år etter måned / dag (linjediagram)</li>
<li>Kjøpe gjeldende og forrige år (linje- og diagram)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Kjøp bruker analyse av leverandør</td>
<td><ul>
<li>Topp 10 leverandør kjøp % av kjøp (trakt)</li>
<li>De 10 viktigste leverandørene med økte utgifter YOY</li>
<li>De 10 viktigste leverandørene med reduserte utgifter YOY</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Innkjøp i år og i fjor og vekst etter innkjøpskategori

## <a name="data-model-and-entities"></a>Datamodell og enheter
Dynamics 365 for operasjoner brukes dataene for rapporten i Kjøp bruke content pack for analyse. Disse dataene er representert som samlet mål mellomlagres i butikken enhet, som er en Microsoft SQL-database som er optimalisert for analyse. Hvis du vil ha mer informasjon om enheten butikken, se på [strømmen BI-integrasjon med enhet-butikken i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogginnlegg. Samlet mål i denne innholdspakken er delsett av samlet mål som var tilgjengelige i bestilling-kube i Microsoft Dynamics AX 2012 og Microsoft Dynamics-365 for operasjoner 2012 R3. Hvis du vil sette kubens samlet mål i lageret for enheten, må du gjøre dem distribueres. Hvis du vil ha mer informasjon, se fremgangsmåten for å sette opp samlet mål i butikken enhet i den [strømmen BI-integrasjon med enhet-butikken i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogginnlegg. Følgende viktige samlet målene er tilgjengelige direkte fra enhet for linjer på fakturaen og brukes som grunnlag for innhold pack.

| Enhet        | Viktige samlet mål | Datakilde for Dynamics 365 for operasjoner | Felt              | beskrivelse                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Fakturalinjer | Innkjøp                   | VendInvoiceTrans                            | Sum(LineAmountMST) | Beløpet i regnskapsvaluta |

Tabellen nedenfor viser viktige mål som er beregnet i innholdspakken fra enhet for linjer på fakturaen.

| Mål               | Beregning                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Kjøp inneværende år | Kjøp inneværende år = SUMMER ('Fakturalinjene'\[kjøp\])                                            |
| Kjøp fjor    | Kjøp fjor = BEREGN (SUMMER ('Fakturalinjene'\[kjøp\]), SAMEPERIODLASTYEAR (datoer\[dato\])) |
| YOY kjøp vekst   | YOY kjøpe vekst = \[kjøpe inneværende år\] – \[kjøpe fjor\]                            |

Følgende viktige dimensjoner i innhold pack brukes som filtre kan skjære samlet mål, slik at du kan oppnå mer tetthet og dypere analytisk innsikt.

| Enhet                 | Eksempler på attributtene                                |
|------------------------|-------------------------------------------------------|
| Leverandører                | Leverandørgrupper, leverandører land eller regioner, Leverandørnavn |
| Produkter               | Produktnummer, produktnavn, Varenavn for grupper        |
| Innkjøpskategorier | Innkjøpskategori, kategorinavn for innkjøp      |
| Juridiske enheter         | Navn på juridisk enhet                                     |
| Datoer                  | Datoer, år forskyvning                                    |

Som standard viser innhold pack data for gjeldende kalenderår. Du kan imidlertid endre datofilteret i rapporten filtre-delen. Du kan også endre firma.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)




---
title: "Kjøps- og forbruksanalyse-innhold for Power BI"
description: "Dette emnet beskriver hva som er inkludert i Kjøps- og forbruksanalyse-innholdspakken for Microsoft Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ad0ee95113d05710cccc1a5e9d215b38244c2047
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Kjøps- og forbruksanalyse-innhold for Power BI

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hva som er inkludert i Kjøps- og forbruksanalyse-innholdspakken for Microsoft Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken.

<a name="overview"></a>Oversikt
--------

Kjøps- og forbruksanalyse-innholdspakken for Microsoft Power BI ble opprettet for innkjøpsledere og ledere som er ansvarlig for budsjetter. Den er utformet for å hjelpe dem med å holde øye med kjøpsutgifter. Den bruker kjøpstransaksjonsdata fra Microsoft Dynamics 365 for Operations, og gir både en aggregert visning av kjøpstall for hele selskapet og en analyse av kjøpsutgifter etter leverandør og vare. Rapportene uthever endringer i kjøpsutgifter over tid. Derfor kan de brukes til å varsle ledere om positive og negative utgiftstrender for individuelle leverandører og produkter. Diagrammer viser kjøpsutgifter for forskjellige innkjøpskategorier og leverandørgrupper. For kategori- og distriktsledere kan det være nyttig å bruke disse diagrammene til å identifisere endringer i forbruksatferd. Innholdspakken lag innkjøpssjefer og ledere som er ansvarlig for budsjetter, analysere kjøpsutgifter på følgende måter:

-   Kjøp hittil i år (etter leverandørgruppe og enkeltleverandører, innkjøpskategori og enkeltprodukter og leverandørplassering)
-   Årlig kjøpsendring (etter leverandørgruppe og innkjøpkategori)

## <a name="accessing-the-content-pack"></a>Tilgang til innholdspakken
Kjøps- og forbruksanalyse-innholdspakken publiseres som et implementeringsaktiva i Microsoft Dynamics Lifecycle Services (LCS) og er tilgjengelig fra Microsoft Dynamics 365 for Operations. Hvis du vil ha mer informasjon om hvordan du får tilgang til og åpner Power BI-rapporter, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md).
Obs!  KB 4011327 er en forutsetning for Power BI-innholdet. Når du logger deg på Lifecycle Services, kan du få tilgang til KB her: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="metrics-that-are-included-in-the-content-pack"></a>Mål som er inkludert i innholdspakken
Kjøps- og forbruksanalyse-innholdspakken inneholder en rapport som består av et sett med mål. Disse målene vises som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over effektene i innholdspakken.

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
<th>Fliser</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kjøp etter leverandør</td>
<td><ul>
<li>De 10 viktigste leverandørene etter kjøp (stablet liggende stolpediagram)</li>
<li>Totalt innkjøp etter leverandørgruppe / land / navn (sektordiagram)</li>
<li>Innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</li>
<li>Gjennomsnittlig innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)</li>
</ul></td>
<td><ul>
<li>Totale innkjøp</li>
<li>Årlig innkjøpsvekst</li>
<li>Totalt antall leverandører</li>
<li>Totalt antall aktive leverandører</li>
</ul></td>
</tr>
<tr class="even">
<td>Kjøp etter produkt</td>
<td><ul>
<li>Kjøp etter innkjøpskategori / produktnavn (stående stolpediagram)</li>
<li>Totalt innkjøp etter innkjøpskategori / produktnavn (sektordiagram)</li>
<li>De 10 viktigste produktene etter kjøp (stablet liggende stolpediagram)</li>
</ul></td>
<td><ul>
<li>Totalt antall produkter</li>
<li>Totalt antall aktive produktprosentdeler av totalt antall produkter</li>
<li>Antall produkter som står for 80 % av innkjøp</li>
</ul></td>
</tr>
<tr class="odd">
<td>Innkjøp etter periode*</td>
<td><ul>
<li>Innkjøp etter måned / dag (stående stolpediagram)</li>
<li>Kumulativ årlig kjøpsavvik (fossefallsdiagram)</li>
<li>Totalt årlig kjøpsvekst (stående stolpediagram)</li>
<li>Innkjøpsutdrag (matrise)</li>
</ul></td>
<td><ul>
<li>Årlig innkjøpsvekst</li>
<li>Årlig innkjøpsvekst i %</li>
</ul></td>
</tr>
<tr class="even">
<td>Kjøp etter leverandørplassering</td>
<td><ul>
<li>Kjøp etter by</li>
<li>Årlig innkjøpsvekst i %</li>
<li>Kjøp etter land</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Kjøps- og forbruksanalyse etter tid</td>
<td><ul>
<li>Kjøp inneværende år etter måned / dag (linjediagram)</li>
<li>Kjøp inneværende or forrige år (linjediagram og stående stolpediagram)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Kjøps- og forbruksanalyse etter leverandør</td>
<td><ul>
<li>De 10 viktigste leverandørkjøpene i % av kjøp (trakt)</li>
<li>De 10 viktigste leverandørene med økte årlige kjøp</li>
<li>De 10 viktigste leverandørene med reduserte årlige kjøp</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Innkjøp i år og forrige år. og vekst etter innkjøpskategori

## <a name="data-model-and-entities"></a>Datamodell og enheter
Dynamics 365 for Operations-data brukes til rapporten i Kjøps- og forbruksanalyse-innholdspakken. Disse dataene representeres som aggregerte målinger som mellomlagres i enhetsbutikken, som er en Microsoft SQL-database som er optimalisert for analyse. Hvis du vil ha mer informasjon om enhetsbutikken, kan du se blogginnlegget [Power BI-integrering med enhetsbutikken i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i innkjøpskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. For å plassere kubens aggregerte målinger i enhetslageret må du gjøre dem distribuerbare. Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i blogginnlegget [Power BI-integrering med enhetslageret i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De aggregerte nøkkelmålingene er tilgjengelige direkte fra fakturalinjeenheten, og brukes som grunnlag for innholdspakken.

| Enhet        | Aggregerte nøkkelmålinger | Datakilde for Dynamics 365 for Operations | Felt              | beskrivelse                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Fakturalinjer | Innkjøp                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Beløpet i regnskapsvaluta |

Tabellen nedenfor viser viktige målinger som beregnes i innholdspakken fra fakturalinjeenheten.

| Mål               | Beregning                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Kjøp inneværende år | Kjøp inneværende år = SUM('Fakturalinjer'\[Kjøp\])                                            |
| Kjøp forrige år    | Kjøp forrige år = CALCULATE(SUM('Fakturalinjer'\[Kjøp\]), SAMEPERIODLASTYEAR((Datoer\[Dato\])) |
| Årlig innkjøpsvekst   | Årlig kjøpsvekst = \[Kjøp inneværende år\] – \[Kjøp forrige år\]                            |

Nøkkeldimensjonene nedenfor i innholdspakken brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.

| Enhet                 | Eksempler på attributter                                |
|------------------------|-------------------------------------------------------|
| Leverandører                | Leverandørgrupper, leverandørland eller områder, leverandørnavn |
| Produkter               | Produktnummer, produktnavn, navn på varegrupper        |
| Innkjøpskategorier | Innkjøpskategori, navn på innkjøpskategori      |
| Juridiske enheter         | Navn på juridisk enhet                                     |
| Datoer                  | Datoer, årsforskyvning                                    |

Som standard viser innholdspakkedataene for inneværende kalenderår. Du kan imidlertid endre datofilteret i delen for rapportfiltre. Du kan også endre firmafilteret.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)






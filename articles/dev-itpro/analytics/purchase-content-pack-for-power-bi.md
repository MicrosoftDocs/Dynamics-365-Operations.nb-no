---
title: "Kjøps- og forbruksanalyse-innhold for Power BI"
description: "Dette emnet beskriver hva som er inkludert i Kjøps- og forbruksanalyse-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 07b6f433a8355d7f9ed6dce8e26f78d38a86a713
ms.contentlocale: nb-no
ms.lasthandoff: 12/18/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Kjøps- og forbruksanalyse-innhold for Power BI

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i **Kjøps- og forbruksanalyse**-innhold for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

**Kjøps- og forbruksanalyse**-innhold for Power BI ble utformet for å hjelpe innkjøpsledere og ledere som er ansvarlige for budsjetter, med å holde øye med kjøpsutgifter. Ledere kan analysere kjøpsutgifter på følgende måter:

-   Kjøp hittil i år (etter leverandørgruppe og enkeltleverandører, innkjøpskategori og enkeltprodukter og leverandørplassering)
-   Årlig kjøpsendring (etter leverandørgruppe og innkjøpkategori)

Innholdet bruker kjøpstransaksjonsdata, og gir både en aggregert visning av kjøpstall for hele selskapet og en analyse av kjøpsutgifter etter leverandør og vare. Rapportene uthever endringer i kjøpsutgifter over tid. Derfor kan de brukes til å varsle ledere om positive og negative utgiftstrender for individuelle leverandører og produkter. I tillegg viser diagrammer kjøpsutgifter for forskjellige innkjøpskategorier og leverandørgrupper. Kategori- og distriktsledere kan derfor bruke diagrammene til å identifisere endringer i forbruksatferd.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold
Power BI-innholdet **Analyse av innkjøp og forbruk** vises på **Analyse av innkjøp og forbruk**-siden (**Innkjøp og leverandører** > **Forespørsler og rapporter** > **Analyse av innkjøpsytelse** > **Analyse av innkjøp og forbruk**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
**Kjøps- og forbruksanalyse**-innhold for Power BI inneholder en rapport som består av et sett med mål. Disse målene vises som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over effektene.

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
Følgende data brukes til å fylle ut rapportsidene i **Kjøps- og forbruksanalyse**-innholdet for Power BI. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i innkjøpskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. For å plassere kubens aggregerte målinger i enhetslageret må du gjøre dem distribuerbare. Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i blogginnlegget [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md). De aggregerte nøkkelmålingene er tilgjengelige direkte fra fakturalinjeenheten, og brukes som grunnlag for innholdet.

| Enhet        | Aggregerte nøkkelmålinger | Datakilde                                 | Felt              | beskrivelse                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Fakturalinjer | Innkjøp                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Beløpet i regnskapsvaluta |

Tabellen nedenfor viser viktige målinger som beregnes i innholdet fra fakturalinjeenheten.

| Mål               | Beregning                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Kjøp inneværende år | Kjøp inneværende år = SUM('Fakturalinjer'\[Kjøp\])                                            |
| Kjøp forrige år    | Kjøp forrige år = CALCULATE(SUM('Fakturalinjer'\[Kjøp\]), SAMEPERIODLASTYEAR((Datoer\[Dato\])) |
| Årlig innkjøpsvekst   | Årlig kjøpsvekst = \[Kjøp inneværende år\] – \[Kjøp forrige år\]                            |

Nøkkeldimensjonene nedenfor i innholdet brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.

| Enhet                 | Eksempler på attributter                                |
|------------------------|-------------------------------------------------------|
| Leverandører                | Leverandørgrupper, leverandørland eller områder, leverandørnavn |
| Produkter               | Produktnummer, produktnavn, navn på varegrupper        |
| Innkjøpskategorier | Innkjøpskategori, navn på innkjøpskategori      |
| Juridiske enheter         | Navn på juridisk enhet                                     |
| Datoer                  | Datoer, årsforskyvning                                    |

Som standard viser innholdspakkedataene for inneværende kalenderår. Du kan imidlertid endre datofilteret i delen for rapportfiltre. Du kan også endre firmafilteret.


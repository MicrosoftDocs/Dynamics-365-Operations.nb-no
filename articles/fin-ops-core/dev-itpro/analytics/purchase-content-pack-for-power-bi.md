---
title: Power BI-innholdet Analyse av innkjøp og forbruk
description: Dette emnet beskriver hva som er inkludert i Kjøps- og forbruksanalyse-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdet, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdet.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2d31aaf14f6399baca8531707864c48cd2d56ac2
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769977"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI-innholdet Analyse av innkjøp og forbruk

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i **Kjøps- og forbruksanalyse**-innhold for Power BI. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

**Kjøps- og forbruksanalyse**-innhold for Power BI ble utformet for å hjelpe innkjøpsledere og ledere som er ansvarlige for budsjetter, med å holde oversikt over kjøpsutgifter. Ledere kan analysere kjøpsutgifter på følgende måter:

- Kjøp hittil i år (etter leverandørgruppe og enkeltleverandører, innkjøpskategori og enkeltprodukter og leverandørplassering)
- Årlig kjøpsendring (etter leverandørgruppe og innkjøpkategori)

Innholdet bruker kjøpstransaksjonsdata, og gir både en aggregert visning av kjøpstall for hele selskapet og en analyse av kjøpsutgifter etter leverandør og vare. Rapportene uthever endringer i kjøpsutgifter over tid. Derfor kan de brukes til å varsle ledere om positive og negative utgiftstrender for individuelle leverandører og produkter. I tillegg viser diagrammer kjøpsutgifter for forskjellige innkjøpskategorier og leverandørgrupper. Kategori- og distriktsledere kan derfor bruke diagrammene til å identifisere endringer i forbruksatferd.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet
Power BI-innholdet **Analyse av innkjøp og forbruk** vises på **Analyse av innkjøp og forbruk**-siden (**Innkjøp og leverandører** \> **Forespørsler og rapporter** \> **Analyse av innkjøpsytelse** \> **Analyse av innkjøp og forbruk**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
**Kjøps- og forbruksanalyse**-innhold for Power BI inneholder en rapport som består av et sett med mål. Disse målene vises som diagrammer, fliser og tabeller. 

Delene nedenfor gir en oversikt over effektene.

### <a name="purchase-by-vendor-report-page"></a>Rapportsiden Kjøp etter leverandør
**Diagrammer**
- De 10 viktigste leverandørene etter kjøp (stablet liggende stolpediagram)
- Totalt innkjøp etter leverandørgruppe / land / navn (sektordiagram)
- Innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)
- Gjennomsnittlig innkjøp etter leverandørgruppe / land / navn (stående stolpediagram)

**Fliser**
- Totale innkjøp
- Årlig innkjøpsvekst
- Totalt antall leverandører
- Totalt antall aktive leverandører

**Eksempel**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Rapportsiden Kjøp etter produkt

**Diagrammer**
- Kjøp etter innkjøpskategori / produktnavn (stående stolpediagram)
- Totalt innkjøp etter innkjøpskategori / produktnavn (sektordiagram)
- De 10 viktigste produktene etter kjøp (stablet liggende stolpediagram)

**Fliser**
- Totalt antall produkter</li>
- Totalt antall aktive produktprosentdeler av totalt antall produkter
- Antall produkter som står for 80 % av innkjøp

**Eksempel**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Rapportsiden Innkjøp etter periode
Denne siden viser innkjøp i år og forrige år, og vekst etter innkjøpskategori.

**Diagrammer** 
- Innkjøp etter måned / dag (stående stolpediagram)
- Kumulativ årlig kjøpsavvik (fossefallsdiagram)
- Totalt årlig kjøpsvekst (stående stolpediagram)
- Innkjøpsutdrag (matrise)

**Fliser**
- Årlig innkjøpsvekst
- Årlig innkjøpsvekst i %

**Eksempel**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Rapportsiden Kjøp etter leverandørplassering

**Diagrammer**
- Kjøp etter by
- Årlig innkjøpsvekst i %
- Kjøp etter land

**Eksempel**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Rapportsiden Kjøps- og forbruksanalyse etter tid

**Diagrammer** 
- Kjøp inneværende år etter måned / dag (linjediagram)
- Kjøp inneværende or forrige år (linjediagram og stående stolpediagram)

**Eksempel**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Rapportsiden Kjøps- og forbruksanalyse etter leverandør

**Diagrammer** 
- De 10 viktigste leverandørkjøpene i % av kjøp (trakt)
- De 10 viktigste leverandørene med økte årlige kjøp
- De 10 viktigste leverandørene med reduserte årlige kjøp

**Eksempel** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Datamodell og enheter
Følgende data brukes til å fylle ut rapportsidene i **Kjøps- og forbruksanalyse**-innholdet for Power BI. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md).

De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i kjøpskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. For å plassere kubens aggregerte målinger i enhetslageret må du gjøre dem distribuerbare. Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i  [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md). De aggregerte nøkkelmålingene er tilgjengelige direkte fra fakturalinjeenheten, og brukes som grunnlag for innholdet.

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

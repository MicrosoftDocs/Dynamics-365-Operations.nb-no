---
title: Resultat av salg og fortjeneste for Power BI-innhold
description: "Dette emnet beskriver hva som er inkludert i Power BI-innholdet Resultat av salg og fortjeneste. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 16fef86e330a392ddd888fcb46060c3e1efa87c5
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Resultat av salg og fortjeneste for Power BI-innhold

[!include[banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i Microsoft Power BI-innholdet **Resultat av salg og fortjeneste**. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="overview"></a>Oversikt

Power BI-innholdet **Resultat av salg og fortjeneste** ble opprettet slik at salgsledere kan overvåke salghovedmål for omsetning, bruttofortjeneste og bruttofortjeneste. Den bruker salgstransaksjonsdata, og gir både en aggregert visning av salgstall for hele selskapet og en analyse av salgsresultat for kunder og produkter.

Rapporter uthever endringer i inntekts- og fortjenestevekst over tid. Derfor kan de brukes til å varsle ledere om positive og negative trender for individuelle kunder og produkter. I tillegg sammenligner diagrammer inntekter og lønnsomhet over ulike produktkategorier og kundegrupper med hverandre. Kategori- og distriktsledere kan derfor identifisere etternølere og ledere. Til slutt, en omfattende rapport som tegner inn omsetning og fortjenestemargin for enkeltkunder. Dette gir regnskapsansvarlige et datastøttet grunnlag for å justere sin salg- og markedsføringsinnsats til profilene for hver enkelt kunde. 

**Resultat av salg og fortjeneste**-innholdet lar salgssjefer analysere salgsresultat på følgende måter:

-   Inntekt, hittil i år (etter kundegruppe og enkeltkunder, salgkategorier og enkeltprodukter og områder)
-   Inntektsendring, årlig (etter kundeområder og salgskategorier)

Fortjenesten kan analyseres på følgende måter:

-   Bruttofortjeneste og fortjenestemargin (etter kundegrupper og salgskategorier for produkt)
-   Bruttofortjenesteendring, årlig
-   Kundelønnsomhet (etter omsetning kontra bruttofortjeneste)

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold
Hvis du bruker oppdateringen for juli 2017 av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, vises **Resultat av salg og fortjeneste** for Power BI-innhold på siden **Resultat av salg og fortjeneste** (**Salg og markedsføring** > **Forespørsler og rapporter** > **Analyse av salgsytelse** > **Resultat av salg og fortjeneste**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål som er inkludert i Power BI-innholdet
**Resultat av salg og fortjeneste** for Power BI-innhold omfatter en rapport som består av et sett med mål. Disse målene vises som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over effektene i innholdspakken.

| Rapportside            | Diagrammer                                     | Fliser                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Inntekt etter kunde    | De ti viktigste kundene etter inntekt                | Totalinntekt                                           |
|                        | Total inntekt etter kundegruppe            | Årlig inntekstvekst                                      |
|                        | Gjennomsnittlig kundeinntekt etter kundegruppe | Bruttofortjeneste                                            |
|                        | Inntekt og bruttofortjeneste etter kundegruppe   |                                                         |
| Inntekt etter produkt     | Inntekt og bruttofortjeneste etter salgskategori   | Total \# produkter                                    |
|                        | De ti viktigste produktene etter inntekt                 | Totalt antall aktive produkter og prosentdeler av total |
|                        | Total inntekt etter salgskategori            | Antall produkter som står for 80 % av inntekten           |
| Inntekt etter periode\*    | Inntekt etter måned                           | Årlig inntekstvekst                                      |
|                        | Etterfølgende årlig inntektsavvik             | Årlig inntekstvekst i %                                    |
|                        | Totalt salgsavvik etter kundeområde    |                                                         |
| Inntekt etter lokasjon    | Salgsinntekt etter by                      |                                                         |
|                        | Årlig inntekstvekst i %                       |                                                         |
|                        | Salgsinntekt etter område                    |                                                         |
| Kundelønnsomhet | Bruttofortjeneste kontra inntekt, etter kunder   | Fortjenestemargin, bruttofortjeneste, årlig inntektsvekst          |
| Fortjenesteanalyse | Inntekt og bruttofortjeneste etter måned          |                                                         |
|                        | De 15 viktigste kundene etter bruttofortjeneste           |                                                         |
|                        | Bruttofortjeneste etter måned, årlig                 |                                                         |

\* Inntekt i år og forrige år. og vekst etter salgskategori.

## <a name="extending-the-power-bi-content"></a>Utvide Power BI-innholdet
Hvis du bruker innholdspakkene som er tilgjengelige i Microsoft Dynamics Lifecycle Services (LCS), kan du gi personer som ikke logger på Microsoft Dynamics 365, gode analyser. Du kan endre disse innholdspakkene slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publisere innholdspakkene på Power BI.com-leieren for analyse.

Du kan finne **Resultat av salg og fortjeneste** for Power BI-innhold i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Pass på at du laster ned **Resultat av salg og fortjeneste**-innholdet som gjelder for versjonen av Dynamics 365 du bruker.

> [!NOTE]
> Hvis du bruker oppdateringen for Microsoft Dynamics 365 for Operations versjon 1611, er KB 4011327 en forutsetning for dette Power BI-innholdet. Når du logger deg på LCS, har du tilgang til KB-artikkelen på https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Følgende data brukes til å fylle ut rapporten i Power BI-innholdet **Resultat av salg og fortjeneste**. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](power-bi-integration-entity-store.md). 

De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i salgskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. For å plassere kubens aggregerte målinger i enhetslageret må du gjøre dem distribuerbare. Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i blogginnlegget [Power BI-integrering med enhetslageret i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). 

De aggregerte nøkkelmålingene for fakturalinjer, som du finner nedenfor, brukes som grunnlag for innholdspakken.

| Enhet        | Aggregerte nøkkelmålinger                   | Datakilde for Dynamics 365                    | Felt                                        | beskrivelse                                   |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|----------------------------------------------|
| Fakturalinjer | Omsetning                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Beløpet i regnskapsvaluta            |
|               | Solgte varers kost                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Summen av kostbeløp og justering.    |
|               | Provisjonslinjebeløp – regnskapsvaluta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Provisjonsbeløpet i regnskapsvalutaen. |

Tabellen nedenfor viser aggregerte nøkkelmålinger for fakturalinjeenheten som brukes til å opprette flere beregnede målinger i datasettet for innholdspakken.

| Mål           | Beregning                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Bruttofortjeneste      | SUM(Inntekt – Vareforbruk – Provisjon – Merverdiavgift (inkludert i kundefakturalinjebeløp)          |
| Bruttofortjeneste      | SUM(Bruttofortjeneste / (Inntekt - Merverdiavgift (inkludert i kundefakturalinjebeløp)))             |
| Inntekt forrige år | Inntekt forrige år = CALCULATE(SUM('Fakturalinjer'\[Inntekt\]), SAMEPERIODLASTYEAR((Datoer\[Dato\]) |

Nøkkeldimensjonene nedenfor i salgskuben brukes som filtre for å dele opp de aggregerte målingene, slik at du kan få flere detaljer og dypere analytisk innsikt.

| Enhet           | Eksempler på attributter                               |
|------------------|------------------------------------------------------|
| Kunder        | Kundegrupper, kundeområder, adresse, bransje |
| Produkter         | Produktnummer, produktnavn, navn på varegrupper       |
| Salgskategorier | Navn på salgskategorier                                 |
| Juridiske enheter   | Navn på juridiske enheter                                   |
| Datoer            | Datoer                                                |

Som standard viser innholdspakkedataene for inneværende kalenderår. Du kan imidlertid endre datofilteret i delen for rapportfiltre. Du kan også endre firmafilteret.


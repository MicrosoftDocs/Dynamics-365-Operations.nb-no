---
title: Resultat av salg og fortjeneste for Power BI-innhold
description: "Dette emnet beskriver hva som er inkludert i Dynamics 365 for Operations - Resultat av salg og fortjeneste-innholdspakken for Microsoft Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Resultat av salg og fortjeneste for Power BI-innhold

Dette emnet beskriver hva som er inkludert i Dynamics 365 for Operations - Resultat av salg og fortjeneste-innholdspakken for Microsoft Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken.

<a name="overview"></a>Oversikt
--------

Denne innholdspakken ble laget for salgssjefer for å overvåke salghovedmål for omsetning, bruttofortjeneste og bruttofortjeneste. Den bruker salgstransaksjonsdata fra Dynamics 365 for Operations, og gir både en aggregert visning av salgstall for hele selskapet og en analyse av salgsresultat for kunder og produkter. Ved å utheve endringer i inntekts- og fortjenestevekst over tid, kan rapporter brukes til å varsle ledere om positive og negative trender for enkeltkunder og -produkter. For kategori- og distriktsledere kan det være nyttig å ha diagrammer som sammenligner inntekter og lønnsomhet for ulike produktkategorier og kundegrupper med hverandre for å sortere ut etternølere og ledere. En omfattende rapport som tegner inn omsetning og fortjenestemargin for enkeltkunder gir regnskapsansvarlige et datastøttet grunnlag for å justere sin salg- og markedsføringsinnsats til profilene for hver enkelt kunde. Resultat av salg og fortjeneste-innholdspakken lar salgssjefer analysere salgsresultat ved å:

-   Inntekt, hittil i år (etter kundegruppe og enkeltkunder, salgkategorier og enkeltprodukter og områder)
-   Inntektsendring, årlig (etter kundeområder og salgskategorier)

Lønnsomhet kan analyseres etter:

-   Bruttofortjeneste og fortjenestemargin (etter kundegrupper og salgskategorier for produkt)
-   Bruttofortjenesteendring, årlig
-   Kundelønnsomhet (etter omsetning kontra bruttofortjeneste)

## <a name="accessing-the-content-pack"></a>Tilgang til innholdspakken
Resultat av salg og fortjeneste-innholdspakken for Power BI publiseres som et implementeringsaktiva i Lifecycle Services (LCS) og er tilgjengelig fra Dynamics 365 for Operations. Hvis du vil ha mer informasjon om hvordan du får tilgang til og åpner Power BI-rapporter, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Mål som er inkludert i innholdspakken
Resultat av salg og fortjeneste-innholdspakken inneholder en rapport som består av et sett med mål som vises som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over effektene i innholdspakken.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Rapportside**        | **Diagrammer**                                 | **Fliser**                                               |
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

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for Operations-data brukes til å fylle ut rapportsider i Resultat av salg og fortjeneste-innholdspakken. Dette representeres som aggregerte målinger som mellomlagres i enhetsbutikken, som er en Microsoft SQL-database som er optimalisert for analyse. Les mer om dette i bloggen [Power BI-integrering med enhetsbutikken i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De aggregerte målingene i denne innholdspakken er delsett av aggregerte målinger som var tilgjengelige i salgskuben i Dynamics AX 2012 og AX 2012 R3. For å plassere kubens aggregerte målinger i enhetsbutikken må du gjøre dem distribuerbare. Hvis du vil ha mer informasjon, kan du se fremgangsmåten for hvordan du plasserer aggregerte målinger i enhetsbutikken i bloggen [Power BI-integrering med enhetsbutikken i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Deaggregerte nøkkelmålingene for fakturalinjer, som du finner nedenfor, brukes som grunnlag for innholdspakken.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Enhet**    | **Aggregerte nøkkelmålinger**               | **Datakilde for Dynamics 365 for Operations** | **Felt**                                    | **Beskrivelse**                          |
| Fakturalinjer | Omsetning                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Beløp i regnskapsvaluta            |
|               | Solgte varers kost                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Kostnadsbeløp + justering                 |
|               | Provisjonslinjebeløp – regnskapsvaluta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Provisjonsbeløp i regnskapsvaluta |

Tabellen nedenfor viser aggregerte nøkkelmålinger for fakturalinjeenheten som brukes til å opprette flere beregnede målinger i datasettet for innholdspakken.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Måling**       | **Beregnet som**                                                                                |
| Bruttofortjeneste      | SUM(Inntekt – Vareforbruk – Provisjon – Merverdiavgift (inkludert i kundefakturalinjebeløp)          |
| Bruttofortjeneste      | SUM(Bruttofortjeneste / (Inntekt - Merverdiavgift (inkludert i kundefakturalinjebeløp)))             |
| Inntekt forrige år | Inntekt forrige år = CALCULATE(SUM('Fakturalinjer'\[Inntekt\]), SAMEPERIODLASTYEAR((Datoer\[Dato\]) |

Nøkkeldimensjonene nedenfor i **salgskuben** brukes som filtre kan dele opp de aggregerte målingene for å gi flere detaljer og dypere analytisk innsikt.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Enhet**       | **Eksempler på attributter**                           |
| Kunder        | Kundegrupper, kundeområder, adresse, bransje |
| Produkter         | Produktnummer, produktnavn, navn på varegrupper       |
| Salgskategorier | Navn på salgskategorier                                 |
| Juridiske enheter   | Navn på juridiske enheter                                   |
| Datoer            | Datoer                                                |

Innholdspakken viser data for gjeldende kalenderår som standard, men du kan åpne delen med rapportfiltre og endre datofilteret. Du kan også endre firmafilteret.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)




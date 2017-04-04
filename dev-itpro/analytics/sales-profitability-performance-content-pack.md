---
title: "Salg og fortjeneste ytelse strømmen BI-innhold"
description: "Dette emnet beskriver hva som er inkludert i Dynamics-365 for operasjoner - salg og fortjeneste ytelse content pack for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert i pakken innhold og gir informasjon om datamodell og enheter som brukes til å lage innhold pack."
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

# <a name="sales-and-profitability-performance-power-bi-content"></a>Salg og fortjeneste ytelse strømmen BI-innhold

Dette emnet beskriver hva som er inkludert i Dynamics-365 for operasjoner - salg og fortjeneste ytelse content pack for Microsoft Power BI. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert i pakken innhold og gir informasjon om datamodell og enheter som brukes til å lage innhold pack.

<a name="overview"></a>Oversikt
--------

Denne innholdspakken ble opprettet for salgssjefer å overvåke salg hovedmål for omsetning, bruttofortjeneste og Bruttofortjeneste marger. Den bruker salg transaksjonsdata fra Dynamics 365 for operasjoner, og inneholder både en aggregert visning av salgstallene for firmaet og en oppdeling av salgsytelse for kunder og produkter. Ved å utheve endringer i inntekt og fortjeneste vekst over tid, kan rapporter brukes til å varsle ledere om positive og negative trender for individuelle kunder og produkter. Kategori og regionale ledere vil finne det nyttig å ha diagrammer som sammenligner inntekter og lønnsomhet for ulike produktkategorier og kundegrupper til hverandre for å sortere ut Etterslengere og ledere. En omfattende rapport som tegner inntegninger individuelle kunden omsetning og fortjenestemargin gir kontoadministratorer en data-støttet foundation for å attune sine anstrengelser for salg og markedsføring i respektive profil for hver kunde. Salgs- og lønnsomhet ytelse innhold pack muliggjør salgssjefer til å analysere salg ytelse ved å:

-   Inntekt, år-til-dato (etter kundegruppe og individuelle kunder, salg kategorier, og enkelte produkter og områder)
-   Inntektsendring, år-over-år (etter kunde regioner og salget kategorier)

Lønnsomhet kan analyseres ved:

-   Bruttofortjeneste og fortjenestemargin (ved kundegrupper og produktkategorier salg)
-   Bruttofortjeneste endring, år-over-år
-   Kundelønnsomhet (etter omsetning kontra Bruttofortjeneste)

## <a name="accessing-the-content-pack"></a>Tilgang til innhold pack
Salgs- og lønnsomhet ytelse strøm BI innhold pack er publisert som et anleggsmiddel for implementering i livssyklusen tjenester (LCS), og kan nås fra Dynamics 365 for operasjoner. Hvis du vil ha mer informasjon om hvordan du får tilgang til og starte strømmen BI-rapporter, se [strømmen BI-innhold i LCS fra Microsoft og partnere på](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Mål som er inkludert i innhold pack
Content pack inneholder en rapport som består av et sett med mål visualized som tabeller, diagrammer og fliser. Tabellen nedenfor gir en oversikt over visualisations i innhold pack.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Rapportside**        | **Charts**                                 | **Side ved side**                                               |
| Omsetning per kunde    | Topp 10-kunder etter inntekt                | Totalinntekt                                           |
|                        | Samlet omsetning av kundegruppe            | YOY vekst i inntekt                                      |
|                        | Gjennomsnittlig Kundeomsetning etter kundegruppe | Bruttofortjeneste                                            |
|                        | Inntekt & Bruttofortjeneste etter kunde   |                                                         |
| Omsetning etter produkt     | Inntekt & Bruttofortjeneste etter kategori   | Total \#av produkter                                    |
|                        | Topp 10 produkter etter inntekt                 | Totalt antall aktive produkter og prosent av total |
|                        | Samlet omsetning etter kategori            | Antall produkter regnskap for 80 % inntekt           |
| Inntekter per periode\*    | Omsetning etter måned                           | YOY vekst i inntekt                                      |
|                        | Etterfølgende omsetning avvik, YOY             | YOY omsetning vekst %                                    |
|                        | Totalt salg avvik etter kunde-område    |                                                         |
| Omsetning per lokasjon    | Inntekter fra salg etter poststed                      |                                                         |
|                        | YOY omsetning vekst %                       |                                                         |
|                        | Inntekter fra salg etter region                    |                                                         |
| Kundelønnsomhet | Bruttofortjeneste kontra omsetning per kunde   | Bruttofortjeneste, Bruttofortjeneste, YOY vekst i inntekt          |
| Fortjenesteanalyse | Omsetning og Bruttofortjeneste per måned          |                                                         |
|                        | Topp 15 kunder etter Bruttofortjeneste           |                                                         |
|                        | Bruttofortjeneste etter måned, YOY                 |                                                         |

\*Omsetning dette og siste år og vekst etter kategori.

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for operasjoner data brukes til å fylle ut rapporten i salg og fortjeneste ytelse innhold pack. Dette er representert som samlet mål mellomlagres i butikken enhet, som er en Microsoft SQL-database som er optimalisert for analyse. Les mer om det i bloggen [strømmen BI-integrasjon med enhet-butikken i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Samlet mål i denne innholdspakken er delsett av samlet mål som var tilgjengelige i kuben, salg i Dynamics AX 2012 og AX 2012 R3. For å stadium i kubens samlet mål i butikken enhet må du gjøre dem distribueres. Hvis du vil ha mer informasjon, se fremgangsmåten for hvordan du trinn samlet mål i enhet-butikken i bloggen [strømmen BI-integrasjon med enhet-butikken i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Følgende viktige samlet mål for fakturaen linjer enheten som skal brukes som grunnlag for innhold pack.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Viktige samlet mål**               | **Datakilde for Dynamics 365 for operasjoner** | **Field**                                    | **Description**                          |
| Fakturalinjer | Omsetning                                      | CustInvoiceTrans                                | Sum(LineAmountMST)                           | Beløp i regnskapsvaluta            |
|               | Solgte varers kost                           | InventTrans                                     | SUM (CostAmountPosted + CostAmountAdjustment) | Kostbeløp + justering                 |
|               | Linje av provisjonsbeløpet – regnskapsvalutaen | CustInvoiceTrans                                | Sum(CommissAmountMST)                        | Provisjonsbeløpet i regnskapsvalutaen |

Tabellen nedenfor viser viktige samlet målene for enheten som fakturaen linjer som brukes til å opprette flere beregnede mål i den innholdspakken dataset.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Beregnet som**                                                                                |
| Bruttofortjeneste      | SUM (omsetning – VAREFORBRUK – provisjon – merverdiavgift (inkludert i Kundefakturalinjebeløp))          |
| Bruttofortjeneste      | SUM (Bruttofortjeneste / (inntekter - merverdiavgift (inkludert i Kundefakturalinjebeløp)))             |
| Inntekt forrige år | Omsetning fjor = BEREGN (SUMMER ('Fakturalinjene'\[inntekt\]), SAMEPERIODLASTYEAR (datoer\[dato\]) |

Følgende nøkkel dimensjoner i den **kube for salg** brukes som filtre kan skjære samlet mål for å oppnå større tetthet og dypere analytisk kunnskap.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Eksempler på attributtene**                           |
| Kunder        | Kundegrupper, kunden regioner, adresse, bransje |
| Produkter         | Produktnummer, produktnavn, Varenavn for grupper       |
| Salgskategorier | Salg kategorinavn                                 |
| Juridiske enheter   | Navn på juridisk enhet                                   |
| Datoer            | Datoer                                                |

Content pack viser data for gjeldende kalenderåret som standard, men du kan åpne rapportinndelingen filtre og endre datofilteret. Du kan også endre firma.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)




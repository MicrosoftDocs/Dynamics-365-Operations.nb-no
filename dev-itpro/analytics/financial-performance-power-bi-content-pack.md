---
title: "Økonomiske ytelse strømmen BI-innhold"
description: "Dette emnet beskriver Microsoft Dynamics 365 for operasjoner økonomiske resultater content pack for Microsoft Power BI. Den beskriver instrumentbord og rapporter som er inkludert i innhold pack, og gir informasjon om en datamodell og enheter som ble brukt til å lage innhold pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Økonomiske ytelse strømmen BI-innhold

Dette emnet beskriver Microsoft Dynamics 365 for operasjoner økonomiske resultater content pack for Microsoft Power BI. Den beskriver instrumentbord og rapporter som er inkludert i innhold pack, og gir informasjon om en datamodell og enheter som ble brukt til å lage innhold pack.

<a name="accessing-the-content-pack"></a>Tilgang til innhold pack
--------------------------

Det finnes to versjoner av økonomiske resultater innhold pack. Én versjon er tilgjengelig fra Microsoft Dynamics Lifecycle tjenester (LCS), og den andre er tilgjengelig fra PowerBI.com.

-   **Versjonen som er tilgjengelig fra LCS:** den økonomiske resultater innhold pack som er tilgjengelig fra LCS støtter Microsoft Dynamics 365 for operasjoner versjon 1611. Du kan finne innhold pack i biblioteket Delte aktiva i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innhold pack og koble den til din Microsoft Dynamics-365 for operasjoner data, se [strømmen BI-innhold i LCS fra Microsoft og partnere på](power-bi-content-microsoft-partners.md).
-   **Versjonen som er tilgjengelig fra PowerBI.com:** den økonomiske resultater innhold pack som er tilgjengelig fra PowerBI.com støtter Microsoft Dynamics AX-versjon 7.0 og 7.0.1. Hvis du vil ha mer informasjon om hvordan du kobler og laste inn dine Dynamics 365 for operasjoner data, se [Access strømmen BI-innhold fra PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Installasjonsprogrammet for hovedkonto
Organisasjoner vil gjeld og omsetningsbeløp skal vises som positive beløp i rapporter, er det viktig med oppsettet av de primære kontoene i Dynamics 365 for operasjoner. Hovedkontotypen for disse viktigste kontoene skal vises som positive beløp, må settes til **ansvar** eller **inntekt**. Når du bruker disse kontotypene, vil rapportere via Microsoft Power BI tilbakeføre tegnene og vise beløpene som positive.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Instrumentbord og rapporter som er inkludert i innhold pack
Når du har knyttet innholdspakken til Dynamics 365 for Operations-dataene dine, viser instrumentbordet og rapportene de økonomiske dataene dine. Hvis du aldri har brukt strøm BI før, kan du lære mer om det på den [veiledende læring side for strøm BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Instrumentbordet inneholder fliser med oppsummerte data som er basert på underliggende rapporter. Hver flis viser sammendragsinformasjon for inneværende år for alle firmaer i en organisasjon. Her er noen av brikkene:

-   Kontant
-   Totalomsetning i inneværende år
-   Totale utgifter i inneværende år
-   Nettoinntekt i inneværende år
-   Likviditetsgrad II
-   Totale utgifter i år etter kontokategori
-   Likviditetsgrad
-   Gjeld på samlede aktiva
-   Faktisk i forhold til anslått omsetning
-   Fakturert inntekt i inneværende år
-   Driftsutgiftsgrad i inneværende år
-   Fortjenestemargin i inneværende år
-   Faktiske i forhold til budsjetterte utgifter – alle selskaper

Hvert panel er støttet av en støttende rapport. Disse rapportene inneholder både diagrammer og tabeller som gir mer informasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                      | Informasjon som rapporten inneholder                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kontantanalyse               | Kontant ved juridisk enhet, kontanter etter kvartal, totale kontanter og kontanter pr. konto **notat:** de **kontanter etter kvartal** rapporten ikke inneholder startsaldoer i samlet for første kvartal. Det viser summen av nye transaksjoner som er postert i hvert kvartal.                                                                                |
| Likviditetsgradsanalyse      | Likviditetsgrad etter juridisk enhet, likviditetsgrad etter kvartal og saldoer for omsetningsaktiva og kortsiktig gjeld                                                                                                                                                                                                                              |
| Analyse av likviditetsgrad II        | Rask forholdet etter juridisk enhet, rask forholdet etter kvartal og saldoer for kontanter, kontoer kunde og gjeldende gjeld                                                                                                                                                                                                                      |
| Analyse av solgte varers kost | Solgte varers kost (vareforbruk) etter juridisk enhet, vareforbruk i år og i fjor etter kvartal, vareforbruk i forhold til salg etter juridisk enhet, totalt vareforbruk og vareforbruk i forhold til salg i prosent                                                                                                                                                                                   |
| Driftskapitalanalyse    | Driftskapital etter juridisk enhet, driftskapital etter kvartal, omsetningsaktiva, kortsiktig gjeld og total driftskapital                                                                                                                                                                                                                   |
| Aktiva- og gjeldsanalyse     | Avkastning på samlede aktiva og gjeld på samlede aktiva etter juridisk enhet, gjeld på samlede aktiva og avkastning på samlede aktiva hittil i kvartalet, aktiva og gjeld                                                                                                                                                                                     |
| Analyse av fortjenestemargin      | Faktisk og budsjettert fortjenestemargin etter juridisk enhet, fortjenestemargin etter kvartal, fortjenestemargin i prosent og fortjenestemargin                                                                                                                                                                                                                       |
| Nettoinntektsanalyse         | Faktisk og budsjettert nettoinntekt etter juridisk enhet, nettoinntekt i år og i fjor og utgifter i forhold til nettinntekt i prosent                                                                                                                                                                                                                       |
| Analyse av inntekter           | Faktiske og budsjetterte inntekter før renter og avgifter etter juridisk enhet, inntekter før renter og avgifter i år og i fjor, utgifter i forhold til inntekter i prosent og faktiske og budsjetterte utgifter i forhold til inntekter                                                                                                                                                          |
| Omsetningsanalyse            | Totalomsetning, faktisk og budsjettert totalomsetning etter juridisk enhet, totalomsetning i år og i fjor, budsjettavvik for omsetning etter juridisk enhet og totalomsetning i denne perioden og siste periode                                                                                                                                                 |
| Utgiftsanalyse            | Totale utgifter, faktiske i forhold til budsjetterte totale utgifter etter juridisk enhet, faktiske og budsjetterte totale utgifter etter kvartal, totale utgifter etter kontokategori og driftsutgiftsgrad                                                                                                                                                                 |
| Analyse av fakturert inntekt     | Total kundereskontro, total kundereskontro etter juridisk enhet, totalt antall kunder etter kvartal og saldoer for kunder-kontoer **notat:** rapportene ikke Inkluder startsaldoer for kontoer fordringer finanskontoene. De viser summen av nye transaksjoner som er postert til kontoene fordringer. |

Diagrammer og fliser for alle disse rapportene kan filtreres og festes på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dataene som fyller instrumentbord og rapporter i økonomiske resultater innhold pack er Dynamics 365 for operasjoner data. Følgende enheter ble brukt som grunnlag for innhold pack: **samle data enheter**

-   **GeneralLedgerActivities** – denne enheten samler Generelt finanssaldoer av kontokategorien.
-   **BudgetActivities** – denne enheten samler budsjettsaldoer av kontokategorien.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Finanskontoer
-   ChartofAccounts

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. De beregnede mål brukes til å beregne viktige ytelsesindikatorer (KPIer) og rapporter som brukes i content pack. Som standard henter innholdspakken data for de siste tre årene og ett år frem. Hvis du vil ta med flere beregninger i rapportene og på instrumentbord, kan du endre [Microsoft Excel-arbeidsboken](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Denne arbeidsboken er standarddatamodellen som ble brukt til å opprette innholdspakken. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)




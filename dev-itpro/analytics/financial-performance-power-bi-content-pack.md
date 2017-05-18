---
title: Finansresultat for Power BI-innhold
description: "Dette emnet beskriver hvor du får tilgang til finansresultat-innholdspakken i Microsoft Dynamics 365 for Operations for Microsoft Power BI. Det beskriver instrumentbordet og rapportene som er inkludert i innholdspakken, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bb9a12dd45e227e86ba47c19f0850a73b77bc735
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="financial-performance-power-bi-content"></a>Finansresultat for Power BI-innhold

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvor du får tilgang til finansresultat-innholdspakken i Microsoft Dynamics 365 for Operations for Microsoft Power BI. Det beskriver instrumentbordet og rapportene som er inkludert i innholdspakken, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken.

<a name="accessing-the-content-pack"></a>Tilgang til innholdspakken
--------------------------

Det finnes to versjoner av Finansresultat-innholdspakken. Én versjon er tilgjengelig fra Microsoft Dynamics Lifecycle Services (LCS), og den andre er tilgjengelig fra PowerBI.com.

-   **Versjonen som er tilgjengelig fra LCS:** Finansresultat-innholdspakken som er tilgjengelig fra LCS, støtter Microsoft Dynamics 365 for Operations versjon 1611. Du kan finne innholdspakken i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdspakken og kobler den til Microsoft Dynamics 365 for Operations-data, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md).
-   **Versjonen som er tilgjengelig fra PowerBI.com:** Finansresultat-innholdspakken som er tilgjengelig fra PowerBI.com, støtter Microsoft Dynamics AX versjon 7.0 og 7.0.1. Hvis du vil ha mer informasjon om hvordan du kobler til og laster inn Dynamics 365 for Operations-data, se [Tilgang til Power BI-innhold fra PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Hovedkontooppsett
Fordi organisasjoner vil at gjeld og omsetningsbeløp skal vises som positive beløp i rapporter, er oppsettet av hovedkontoene i Dynamics 365 for Operations viktig. For at disse hovedkontoene skal vises som positive beløp, må hovedkontotypen settes til **Gjeld** eller **Inntekt**. Når du bruker disse kontotypene, vil rapportering via Microsoft Power BI tilbakeføre tegnene og vise beløpene som positive.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Instrumentbord og rapporter som er inkludert i innholdspakken
Når du har knyttet innholdspakken til Dynamics 365 for Operations-dataene dine, viser instrumentbordet og rapportene de økonomiske dataene dine. Hvis du aldri har brukt Power BI før, kan du finne ut mer på siden [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Instrumentbordet inneholder fliser med oppsummerte data som er basert på underliggende rapporter. Hver flis viser sammendragsinformasjon for inneværende år for alle firmaer i en organisasjon. Her er noen av flisene:

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

Hver flis leveres med en tilhørende rapport. Disse rapportene inneholder både diagrammer og tabeller som gir mer informasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                      | Informasjon som rapporten inneholder                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kontantanalyse               | Kontanter etter juridisk enhet, kontanter etter kvartal, kontanter totalt og kontanter etter konto **Obs!** Rapporten **Kontanter etter kvartal** inkluderer ikke startsaldoer i summen for første kvartal. Den viser summen av nye transaksjoner som er postert i hvert kvartal.                                                                                |
| Likviditetsgradsanalyse      | Likviditetsgrad etter juridisk enhet, likviditetsgrad etter kvartal og saldoer for omsetningsaktiva og kortsiktig gjeld                                                                                                                                                                                                                              |
| Analyse av likviditetsgrad II        | Likviditetsgrad II etter juridisk enhet, likviditetsgrad II etter kvartal og saldoer for kontanter, kundereskontro og kortsiktig gjeld                                                                                                                                                                                                                      |
| Analyse av solgte varers kost | Solgte varers kost (vareforbruk) etter juridisk enhet, vareforbruk i år og i fjor etter kvartal, vareforbruk i forhold til salg etter juridisk enhet, totalt vareforbruk og vareforbruk i forhold til salg i prosent                                                                                                                                                                                   |
| Driftskapitalanalyse    | Driftskapital etter juridisk enhet, driftskapital etter kvartal, omsetningsaktiva, kortsiktig gjeld og total driftskapital                                                                                                                                                                                                                   |
| Aktiva- og gjeldsanalyse     | Avkastning på samlede aktiva og gjeld på samlede aktiva etter juridisk enhet, gjeld på samlede aktiva og avkastning på samlede aktiva hittil i kvartalet, aktiva og gjeld                                                                                                                                                                                     |
| Analyse av fortjenestemargin      | Faktisk og budsjettert fortjenestemargin etter juridisk enhet, fortjenestemargin etter kvartal, fortjenestemargin i prosent og fortjenestemargin                                                                                                                                                                                                                       |
| Nettoinntektsanalyse         | Faktisk og budsjettert nettoinntekt etter juridisk enhet, nettoinntekt i år og i fjor og utgifter i forhold til nettinntekt i prosent                                                                                                                                                                                                                       |
| Analyse av inntekter           | Faktiske og budsjetterte inntekter før renter og avgifter etter juridisk enhet, inntekter før renter og avgifter i år og i fjor, utgifter i forhold til inntekter i prosent og faktiske og budsjetterte utgifter i forhold til inntekter                                                                                                                                                          |
| Omsetningsanalyse            | Totalomsetning, faktisk og budsjettert totalomsetning etter juridisk enhet, totalomsetning i år og i fjor, budsjettavvik for omsetning etter juridisk enhet og totalomsetning i denne perioden og siste periode                                                                                                                                                 |
| Utgiftsanalyse            | Totale utgifter, faktiske i forhold til budsjetterte totale utgifter etter juridisk enhet, faktiske og budsjetterte totale utgifter etter kvartal, totale utgifter etter kontokategori og driftsutgiftsgrad                                                                                                                                                                 |
| Analyse av fakturert inntekt     | Total kundereskontro, total kundereskontro etter juridisk enhet, total kundereskontro etter kvartal og saldoer for kontiene for kundereskontro **Obs!** Rapportene inkluderer ikke startsaldoer for kundefinanskontoene. De viser summen av nye transaksjoner som er postert til kunder. |

Diagrammer og fliser for alle disse rapportene kan filtreres og festes på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dataene som brukes til å fylle ut instrumentbordet og rapportene i finansresultat-innholdspakken, er Dynamics 365 for Operations-data. Følgende enheter ble brukt som grunnlag for innholdspakken: **Aggregerte dataenheter**

-   **GeneralLedgerActivities** – Denne enheten aggregerer saldoer i økonomimodulen etter kontokategori.
-   **BudgetActivities** – Denne enheten aggregerer budsjettsaldoer etter kontokategori.

**Dataenheter**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Finanskontoer
-   ChartofAccounts

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. De beregnede målene brukes til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdspakken. Som standard henter innholdspakken data for de siste tre årene og ett år frem. Hvis du vil ta med flere beregninger i rapportene og på instrumentbord, kan du endre [Microsoft Excel-arbeidsboken](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Denne arbeidsboken er standarddatamodellen som ble brukt til å opprette innholdspakken. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](..\data-entities\data-entities.md)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](configure-power-bi-integration.md)






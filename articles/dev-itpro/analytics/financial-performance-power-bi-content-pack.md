---
title: Finansresultat-innhold for Power BI
description: "Dette emnet beskriver Power BI-innholdet om finansresultat. Det beskriver instrumentbordet og rapporter som er inkludert, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: kweekley
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f111698315cd42c0c1c0d470b94688b548375bee
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="financial-performance-power-bi-content"></a>Finansresultat-innhold for Power BI

[!include[banner](../includes/banner.md)]

Dette emnet beskriver Power BI-innholdet om **finansresultat**. Det beskriver instrumentbordet og rapporter som er inkludert, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innhold

Du kan få tilgang til **Finansresultat** i Power BI fra Microsoft Dynamics Lifecycle Services (LCS) and from PowerBI.com.

### <a name="available-from-lcs"></a>Tilgjengelig fra LCS
Power BI-innhold om **finansresultat** som er tilgjengelig fra LCS, støtter følgende versjoner:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017)
- Microsoft Dynamics 365 for Operations versjon 1611 

Du kan finne Power BI-innholdet i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdspakken og implementerer den i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](power-bi-content-microsoft-partners.md). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

### <a name="available-from-powerbicom"></a>Tilgjengelig fra PowerBI.com
Power BI-innhold om **finansresultat** som er tilgjengelig fra PowerBI.com, støtter Microsoft Dynamics AX versjon 7.0 og 7.0.1. Hvis du vil ha mer informasjon om hvordan du kobler til og laster inn Dynamics AX-data, se [Tilgang til Power BI-innhold fra PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Hovedkontooppsett
Fordi organisasjoner vil at gjeld og omsetningsbeløp skal vises som positive beløp i rapporter, er oppsettet av hovedkontoene viktig. For at disse hovedkontoene skal vises som positive beløp, må hovedkontotypen settes til **Gjeld** eller **Inntekt**. Når du bruker disse kontotypene, vil rapportering via Power BI tilbakeføre tegnene og vise beløpene som positive.

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a>Instrumentbord og rapporter som er inkludert i Power BI-innholdet
Instrumentbordet inneholder fliser med oppsummerte data som er basert på underliggende rapporter. Hver flis viser sammendragsinformasjon for inneværende år for alle firmaer i en organisasjon. Her er noen av flisene:

- Kontant
- Totalomsetning i inneværende år
- Totale utgifter i inneværende år
- Nettoinntekt i inneværende år
- Likviditetsgrad II
- Totale utgifter i år etter kontokategori
- Likviditetsgrad
- Gjeld på samlede aktiva
- Faktisk i forhold til anslått omsetning
- Fakturert inntekt i inneværende år
- Driftsutgiftsgrad i inneværende år
- Fortjenestemargin i inneværende år
- Faktiske i forhold til budsjetterte utgifter – alle selskaper

Hver flis leveres med en tilhørende rapport. Disse rapportene inneholder både diagrammer og tabeller som gir mer informasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                      | Informasjon som rapporten inneholder |
|-----------------------------|--------------------------------------|
| Kontantanalyse               | Kontanter etter juridisk enhet, kontanter etter kvartal, kontanter totalt og kontanter etter konto<blockquote>[!NOTE]<br>Kontanter etter kvartal inkluderer ikke startsaldoer i totalen for det første kvartalet. Den viser summen av nye transaksjoner som er postert i hvert kvartal.</blockquote> |
| Likviditetsgradsanalyse      | Likviditetsgrad etter juridisk enhet, likviditetsgrad etter kvartal og saldoer for omsetningsaktiva og kortsiktig gjeld |
| Analyse av likviditetsgrad II        | Likviditetsgrad II etter juridisk enhet, likviditetsgrad II etter kvartal og saldoer for kontanter, kundereskontro og kortsiktig gjeld |
| Analyse av solgte varers kost | Solgte varers kost (vareforbruk) etter juridisk enhet, vareforbruk i år og i fjor etter kvartal, vareforbruk i forhold til salg etter juridisk enhet, totalt vareforbruk og vareforbruk i forhold til salg i prosent |
| Driftskapitalanalyse    | Driftskapital etter juridisk enhet, driftskapital etter kvartal, omsetningsaktiva, kortsiktig gjeld og total driftskapital |
| Aktiva- og gjeldsanalyse     | Avkastning på samlede aktiva og gjeld på samlede aktiva etter juridisk enhet, gjeld på samlede aktiva og avkastning på samlede aktiva hittil i kvartalet, aktiva og gjeld |
| Analyse av fortjenestemargin      | Faktisk og budsjettert fortjenestemargin etter juridisk enhet, fortjenestemargin etter kvartal, fortjenestemargin i prosent og fortjenestemargin |
| Nettoinntektsanalyse         | Faktisk og budsjettert nettoinntekt etter juridisk enhet, nettoinntekt i år og i fjor og utgifter i forhold til nettinntekt i prosent |
| Analyse av inntekter           | Faktiske og budsjetterte inntekter før renter og avgifter etter juridisk enhet, inntekter før renter og avgifter i år og i fjor, utgifter i forhold til inntekter i prosent og faktiske og budsjetterte utgifter i forhold til inntekter |
| Omsetningsanalyse            | Totalomsetning, faktisk og budsjettert totalomsetning etter juridisk enhet, totalomsetning i år og i fjor, budsjettavvik for omsetning etter juridisk enhet og totalomsetning i denne perioden og siste periode |
| Utgiftsanalyse            | Totale utgifter, faktiske i forhold til budsjetterte totale utgifter etter juridisk enhet, faktiske og budsjetterte totale utgifter etter kvartal, totale utgifter etter kontokategori og driftsutgiftsgrad |
| Analyse av fakturert inntekt     | Total kundereskontro, total kundereskontro etter juridisk enhet, total kundereskontro etter kvartal og saldoer for kontiene for kundereskontro<blockquote>[!NOTE]<br>Informasjonen inkluderer ikke startsaldoer for kundesfinanskontoene. Den viser summen av nye transaksjoner som er postert til kunder.</blockquote> |

Diagrammer og fliser for alle disse rapportene kan filtreres og festes på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Følgende enheter ble brukt som grunnlag for Power BI-innholdet om : **finansresultat**:

**Aggregerte dataenheter**

- **GeneralLedgerActivities** – Denne enheten aggregerer saldoer i økonomimodulen etter kontokategori.
- **BudgetActivities** – Denne enheten aggregerer budsjettsaldoer etter kontokategori.

**Dataenheter**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Finanskontoer
- ChartofAccounts

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. De beregnede målene brukes til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdet. Som standard henter innholdet data for de siste tre årene og ett år frem. Hvis du vil ta med flere beregninger i rapportene og på instrumentbord, kan du endre [Microsoft Excel-arbeidsboken](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Denne arbeidsboken er standarddatamodellen som ble brukt til å opprette innholdet. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.


---
title: Finansresultat for PowerBI.com-løsning
description: Dette emnet beskriver PowerBI.com-løsningen for finansresultat.
author: kweekley
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76f0c35ce9db89dd93292c4e39315a5833f38d54
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568853"
---
# <a name="financial-performance-powerbicom-solution"></a>Finansresultat for PowerBI.com-løsning

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Denne PowerBI.com-løsningen er avskrevet som dokumentert i [Fjernede eller avskrevne funksjoner for Finance and Operations](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Dette emnet beskriver PowerBI.com-løsningen for **finansresultat**. Det beskriver instrumentbordet og rapporter som er inkludert, og gir informasjon om datamodellen og enhetene som brukes til å bygge løsningen.

## <a name="main-account-setup"></a>Hovedkontooppsett
Fordi organisasjoner vil at gjeld og omsetningsbeløp skal vises som positive beløp i rapporter, er oppsettet av hovedkontoene viktig. For at disse hovedkontoene skal vises som positive beløp, må hovedkontotypen settes til **Gjeld** eller **Inntekt**. Når du bruker disse kontotypene, vil rapportering via Power BI tilbakeføre tegnene og vise beløpene som positive.

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a>Instrumentbord og rapporter som er inkludert i PowerBI.com-løsningen
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
| Kontantanalyse               | Kontanter etter juridisk enhet, kontanter etter kvartal, kontanter totalt og kontanter etter konto<blockquote>[!NOTE] Kontanter etter kvartal inkluderer ikke startsaldoer i totalen for det første kvartalet. Den viser summen av nye transaksjoner som er postert i hvert kvartal.</blockquote> |
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
| Analyse av fakturert inntekt     | Total kundereskontro, total kundereskontro etter juridisk enhet, total kundereskontro etter kvartal og saldoer for kontiene for kundereskontro<blockquote>[!NOTE] Informasjonen inkluderer ikke startsaldoer for kundesfinanskontoene. Den viser summen av nye transaksjoner som er postert til kunder.</blockquote> |

Diagrammer og fliser for alle disse rapportene kan filtreres og festes på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Følgende enheter ble brukt som grunnlag for PowerBI.com-løsningen **finansresultat**:

**Aggregerte dataenheter**

- **GeneralLedgerActivities** – Denne enheten aggregerer saldoer i økonomimodulen etter kontokategori.
- **BudgetActivities** – Denne enheten aggregerer budsjettsaldoer etter kontokategori.

**Dataenheter**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Finanskontoer
- ChartofAccounts

Disse enhetene ble brukt til å opprette beregnede mål i datamodellen. De beregnede målene brukes til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdet. Som standard henter innholdet data for de siste tre årene og ett år frem. Hvis du vil ta med flere beregninger i rapportene og på instrumentbord, kan du endre [Microsoft Excel-arbeidsboken](https://docs.microsoft.com/dynamics/s-e/). Denne arbeidsboken er standarddatamodellen som ble brukt til å opprette innholdet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
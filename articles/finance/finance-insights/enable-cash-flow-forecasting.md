---
title: Aktivere kontantstrømprognose (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 1977dac4a3ab66cca2248dc0124d3a06d6963f40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978770"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Aktivere kontantstrømprognose (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.

> [!NOTE]
> For å kunne bruke betalingsprognoser i kontantstrømmen må du konfigurere funksjonen for kundebetalingsprognoser som beskrevet i [Aktivere kundebetalingsprognoser](enable-cust-paymnt-prediction.md).

1. Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet. Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet. (Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Hvis distribusjonen av Microsoft Dynamics 365 Finance er en Service Fabric-distribusjon, kan du hoppe over dette trinnet. Finance Insights-teamet skal allerede ha aktivert testversjonen for deg. Hvis du ikke ser funksjonene i arbeidsområdet **Funksjonsbehandling**, eller hvis du får problemer når du prøver å aktivere dem, kontakter du <fiap@microsoft.com>.
  
2. Åpne arbeidsområdet **Funksjonsbehandling**, og følg denne fremgangsmåten:

    1. Velg **Se etter oppdateringer**.
    2. Aktiver følgende funksjoner:

        - Ny rutenettkontroll
        - Gruppering i rutenett (forhåndsversjon) 
        - Kundebetalingsforutsigelser (forhåndsversjon)
        - Kontantstrømprognoser (forhåndsversjon)

3. Gå til **Kontant- og bankbehandling \> Oppsett for kontantstrømprognose**, og legg til likviditetskontoene som skal tas med i prognosene.

    > [!NOTE]
    > Hvis likviditetskontoer ikke er opprettet, kan ikke kontantstrømmen genereres.

4. Gå til **Kontant- og bankbehandling \> Oppsett \> Finance Insights (forhåndsversjon) \> Kontantstrømprognoser (forhåndsversjon)**, og følg denne fremgangsmåten:

    1. Velg **Aktiver funksjon** i fanen **Kontantstrømprognose**.
    2. Velg **Opprett prognosemodell**.

Hvis du vil ha mer informasjon om funksjonen for kontantstrømprognose, kan du se [Kontantstrømprognose](cash-flow-forecast-intro.md).

## <a name="privacy-notice"></a>Personvernerklæring

Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.

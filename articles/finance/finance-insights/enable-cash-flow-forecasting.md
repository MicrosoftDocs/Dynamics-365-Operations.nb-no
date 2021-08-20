---
title: Aktivere kontantstrømprognose (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b5a4e1c3401c945df936258f0c97d2d406019438eb14a01d901f7777c8f0b7d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768921"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Aktivere kontantstrømprognose (forhåndsversjon)

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.

> [!NOTE]
> For å kunne bruke betalingsprognoser i kontantstrømmen må du konfigurere funksjonen for kundebetalingsprognoser som beskrevet i [Aktivere kundebetalingsprognoser](enable-cust-paymnt-prediction.md).

1. Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet. Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet. (Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Hopp over dette trinnet hvis du bruker versjon 10.0.20 eller nyere, eller hvis du bruker en Service Fabric-distribusjon. Finance Insights-teamet skal allerede ha aktivert testversjonen for deg. Hvis du ikke ser funksjonen i arbeidsområdet **Funksjonsbehandling** eller får problemer når du prøver å aktivere den, kontakter du <fiap@microsoft.com>.
  
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

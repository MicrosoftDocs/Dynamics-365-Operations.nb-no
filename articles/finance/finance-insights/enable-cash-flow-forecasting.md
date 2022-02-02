---
title: Aktiver kontantstrømprognose
description: Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: cfcdbe76d640d1786b4622febf9157f5fb1c42f9
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969143"
---
# <a name="enable-cash-flow-forecasting"></a>Aktiver kontantstrømprognose

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.

> [!NOTE]
> For å kunne bruke betalingsprognoser i kontantstrømmen må du konfigurere funksjonen for kundebetalingsprognoser som beskrevet i [Aktivere kundebetalingsprognoser](enable-cust-paymnt-prediction.md).
  
1. Åpne arbeidsområdet **Funksjonsbehandling**, og følg denne fremgangsmåten:

    1. Velg **Se etter oppdateringer**.
    2. På **Alle**-fanen søker du etter **Kontantstrømprognoser**. Hvis du ikke funner denne funksjonen, søker du etter **(Forhåndsversjon) Kontantstrømprognoser**. 
    3. Aktivere funksjonen.

2. Gå til **Kontant- og bankbehandling \> Oppsett for kontantstrømprognose**, og legg til likviditetskontoene som skal tas med i prognosene. Definer også likviditetskontoen for betalinger på fanene **Kunder** og **Leverandører**. Pass på at kontantstrømprognosen beregnes på nytt.

    > [!NOTE]
    > Hvis likviditetskontoer ikke er opprettet, kan ikke kontantstrømmen genereres.
    >
    > Hvis du vil ha mer informasjon om hvordan du definerer kontantstrømprognoser, kan du se [Kontantstrømprognose](../cash-bank-management/cash-flow-forecasting.md).

3. Gå til **Kontant- og bankbehandling \> Oppsett \> Finance Insights (forhåndsversjon) \> Kontantstrømprognoser (forhåndsversjon)**, og følg denne fremgangsmåten:

    1. Velg **Aktiver funksjon** i fanen **Kontantstrømprognose**.
    2. Velg **Opprett prognosemodell**.

Hvis du vil ha mer informasjon om funksjonen for kontantstrømprognose, kan du se [Kontantstrømprognose](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

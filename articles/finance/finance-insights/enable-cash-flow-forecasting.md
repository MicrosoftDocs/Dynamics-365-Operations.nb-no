---
title: Aktiver kontantstrømprognose
description: Denne artikkelen forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 253e3ea9c1c44573b37503f167b4cb3860683c10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859882"
---
# <a name="enable-cash-flow-forecasting"></a>Aktiver kontantstrømprognose

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.

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

> [!NOTE]
> Opplæringen av modellen **Kontantstrømprognose** krever data med 100 eller flere transaksjoner som strekker seg over mer enn et år. Vi anbefaler at du har minst to år med data med flere enn 1 000 transaksjoner.

Hvis du vil ha mer informasjon om funksjonen for kontantstrømprognose, kan du se [Kontantstrømprognose](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

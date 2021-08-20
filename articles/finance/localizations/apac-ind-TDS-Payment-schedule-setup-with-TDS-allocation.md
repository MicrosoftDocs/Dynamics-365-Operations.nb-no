---
title: Konfigurere betalingsplaner med TDS-tildeling
description: Dette emnet forklarer hvordan du konfigurerer betalingsplaner med TDS-tildeling (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 55bfdfb97c418ec9fd856a151da46c1bcf94aa2cb4df85185b47f722d8526ef2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769728"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Konfigurere betalingsplaner med TDS-tildeling

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer betalingsplaner med TDS-tildeling (Tax Deducted at Source).

1. Gå til **Leverandører \> Betalingsoppsett \> Betalingsplaner**.

    [![Siden Betalingsplaner.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Velg **Ny** i handlingsruten for å opprette en betalingsplan, og angi de nødvendige detaljene.
3. Velg metoden du vil bruke til å tildele betalingen for betalingsplanen, i **Tildeling**-feltet:

    - Totalsum
    - Fast beløp
    - Fast antall
    - Angitt

    Feltet **Tildeling av kildeskatt** viser TDS-tildelingsmetoden for betalingsplanen. Hvis du velger **Totalsum** i **Tildeling**-feltet, settes feltet **Tildeling av kildeskatt** automatisk til **Totalsum**. Hvis du velger **Fast beløp**, **Fast antall** eller **Angitt** i **Tildeling**-feltet, settes feltet **Tildeling av kildeskatt** automatisk til **Proporsjonalt**.

    > [!NOTE]
    > Hvis feltet **Tildeling av kildeskatt** er satt til **Totalsum**, beregnes betalingsavdragene basert på bruttobeløpet, som omfatter TDS-beløpet. Hvis feltet **Tildeling av kildeskatt** er satt til **Proporsjonalt**, beregnes betalingsavdragene basert på netto fakturabeløp etter at TDS-beløpet er trukket fra.

4. Angi de andre nødvendige detaljene, og lukk deretter siden.

---
title: Konfigurere betalingsplaner med TDS-tildeling
description: Denne artikkelen forklarer hvordan du konfigurerer betalingsplaner med TDS-tildeling (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 48891c32f39b743ce26e265c5682dab28ecb4b27
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868319"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Konfigurere betalingsplaner med TDS-tildeling

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer betalingsplaner med TDS-tildeling (Tax Deducted at Source).

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

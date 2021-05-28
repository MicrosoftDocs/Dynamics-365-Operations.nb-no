---
title: Angi TDS-parameterne
description: Dette emnet forklarer hvordan du angir parametere for å aktivere TDS-funksjonaliteten (Tax Deducted at Source) i bestemte transaksjoner. Dette er et nødvendig trinn for å bruke TDS-funksjonen (Tax Deducted at Source).
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023476"
---
# <a name="set-the-tds-parameters"></a>Angi TDS-parameterne

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du angir parametere for å aktivere TDS-funksjonaliteten (Tax Deducted at Source) i bestemte transaksjoner. Dette er et nødvendig trinn for å bruke TDS-funksjonen (Tax Deducted at Source).

1. Gå til **Økonomimodul \> Finansoppsett \> Parametere for økonomimodul**.
2. Sett alternativet **Aktiver TDS** til **Ja** i delen **TDS (Tax Deducted at Source)** i fanen **Direkte avgifter** for å aktivere TDS-funksjonaliteten og sidene og feltene som brukes for det.
3. Sett alternativet **Faktura** til **Ja** for å aktivere feltene som brukes til å beregne og trekke fra TDS på fakturanivå.
4. Sett alternativet **Betaling** til **Ja** for å aktivere feltene som brukes til å beregne og trekke fra TDS på betalingsnivået.

    [![Fanen Direkte avgifter](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Finn raden der **Referanse**-feltet er satt til **Kildeskattbetaling** i fanen **Nummerserier**. Velg nummerseriekoden i feltet **Nummerseriekode** for raden. Nummerseriekoden brukes til å generere bilagsnumre for den periodiske TDS-utligningsprosessen.

    > [!NOTE]
    > Hvis du vil kjøre den periodiske TDS-utligningsprosessen, går du til **Avgift \> Deklareringer \> Kildeskatt \> Kildeskattbetaling**.

    [![Fanen Nummerserier](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Lukk siden.

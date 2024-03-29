---
title: Kildeskatt i kjøpstransaksjoner
description: For leverandører med kildeskatt, kan du tilordne standard **Kildeskattgruppe** på siden **Alle leverandører**.
author: kailiang
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c2220159cef31bf3343bcf39325c7a0ff3e0cf47
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727209"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Kildeskatt i kjøpstransaksjoner

For leverandører med kildeskatt, kan du tilordne standard **Kildeskattgruppe** på siden **Alle leverandører**.

1. Gå til **Navigasjonsruten > Moduler > Leverandører > Leverandører > Alle leverandører**.

2. Klikk den aktuelle leverandørkontoen, og klikk **Rediger**.

3. I kategorien **Faktura og levering** setter du feltet **Beregn kildeskatt** til **Ja**.

   > [!NOTE] 
   > Kildeskatt beregnes ikke hvis **Beregn kildeskatt** ikke er aktivert for denne leverandøren i dataene.

4. Velg en kildeskattgruppe i **Kildeskattgruppe**.

5. Klikk **Lagre**.

For varer/tjenester som er pålagt kildeskatt, kan du tilordne standard **Kildeskattegrupper for vare** i **Frigitte produkter**.

1. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.

2. Klikk det aktuelle varenummeret, og klikk **Rediger**.

3. I kategorien **Kjøp** klikker du **Beregn kildeskatt**.

   > [!NOTE] 
   > Kildeskatt beregnes ikke hvis **Beregn kildeskatt** ikke er satt til **Ja** for denne varen i kategorien **Kjøp** på siden **Frigitt produkt**.

4. Velg en kildeskattgruppe i listen **Kildeskattegrupper for vare**.

5. Klikk **Lagre**.

Kildeskattgrupper og kildeskattgrupper for vare kan tilordnes på sidene: 

- **Bestilling**
- **Leverandørfaktura**
- **Fakturajournal**

Standard kildeskattgruppe og kildeskattgrupper for vare føres inn på linjene ved oppretting av **Bestillinger** og/eller **Ventende leverandørfakturaer**. For **Fakturajournal leverandør** kan du aktivere **Beregn kildeskatt** og velge **Kildeskattegrupper for vare** i kategorien **Generelt** i journalen.

Det midlertidige beløpet for kildeskatt er tilgjengelig i feltet **Justert kildeskatt** i kategorien **Totaler** på siden **Bestilling**.

![Kildeskatt er inkludert i bestillingen.](media/withholding-tax-adjusted.png)

Kildeskatt beregnes på **Leverandørbetalingsjournal**. Du kan justere gjeldende kildeskattkoder manuelt og de faktiske kildeskattbeløpene i kategorien **Kildeskatt** på siden **Utlign transaksjoner**.

![Kildeskatt kan justeres manuelt på siden Utlign transaksjoner.](media/withholding-tax-vendor-payment-tab.png)

Det avledede kildeskattbeløpet blir trukket fra leverandørbetalingen og postert til **Kildeskattkonto** i et tilknyttet bilag.

![Kildeskattkonto som viser et tilknyttet bilag.](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

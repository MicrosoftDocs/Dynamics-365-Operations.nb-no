---
title: Kildeskatt i salgstransaksjoner
description: Dette emnet viser en liste over trinnene for å unngå beregning av kildeskatt for valgte kunder. For kunder som angir kildeskatt i betalingene sine, kan du tilordne standard kildeskattgruppe.
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
ms.openlocfilehash: 72d659004a1f61b63d6a782ba6b45bb99030bae9
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727433"
---
# <a name="withholding-tax-in-sales-transactions"></a>Kildeskatt i salgstransaksjoner

Dette emnet viser en liste over trinnene for å unngå beregning av kildeskatt for valgte kunder. For kunder som angir kildeskatt i betalingene sine, kan du tilordne standard **Kildeskattgruppe** på siden **Kunder**. 

1. Gå til **Navigasjonsrute > Moduler > Kunder > Kunder > Alle kunder**.

2. Klikk den aktuelle kundekontoen, og klikk **Rediger**.

3. I kategorien **Faktura og levering** setter du feltet **Beregn kildeskatt** til **Ja**.

   > [!NOTE] 
   > Kildeskatt beregnes ikke hvis **Beregn kildeskatt** ikke er aktivert for denne kunden i hoveddataene.

4. Velg en kildeskattgruppe i **Kildeskattgruppe**.

5. Klikk **Lagre**.

For varer/tjenester som er pålagt kildeskatt, kan du tilordne standard **Kildeskattegrupper for vare** i **Frigitte produkter**.

1. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.

2. Klikk det aktuelle varenummeret, og klikk **Rediger**.

3. I kategorien **Salg** klikker du **Beregn kildeskatt**.

   > [!NOTE] 
   > Kildeskatt beregnes ikke hvis **Beregn kildeskatt** ikke er satt til **Ja** for denne varen i kategorien **Salg** på siden **Frigitt produkt**.

4. Velg en kildeskattgruppe i listen **Kildeskattegrupper for vare**.

5. Klikk **Lagre**.

Kildeskattgrupper og kildeskattegrupper for vare kan tilordnes ved hjelp siden **Salgsordre**. 

Standard kildeskattgruppe og kildeskattgruppe for varer blir brukt som standardoppføringer på salgsordrelinjer når du oppretter en ny salgsordre.

Kildeskatt beregnes og posteres med **Kundebetalingsjournal**. Du kan justere den gjeldende kildeskattkoden manuelt og det faktiske kildeskattbeløpet i kategorien **Kildeskatt** på siden **Utlign transaksjoner**.

Det beregnede kildeskattbeløpet blir trukket fra kundebetalingen og postert til **Kildeskattmotkonto** i et tilknyttet bilag.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

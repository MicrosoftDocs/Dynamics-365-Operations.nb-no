---
title: TDS-beregning for konserninterne transaksjoner
description: Denne artikkelen beskriver fremgangsmåten som brukes til å beregne TDS (Tax Deducted at Source) for konserninterne transaksjoner i faser.
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
ms.openlocfilehash: c27bea997804f2c5eff6be2b20064b272ccd062f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888980"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS-beregning for konserninterne transaksjoner

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver fremgangsmåten som brukes til å beregne TDS (Tax Deducted at Source) for konserninterne transaksjoner i faser.

Når det opprettes en konsernintern bestilling eller salgsordre, brukes den standard TDS-gruppen som er definert for kunden eller leverandøren, til å beregne TDS-beløpet. TDS-beløpet posteres på fradragskontoene eller leverandørreskontroene etter at fakturaen er postert.

En konsernintern salgsordre eller bestilling opprettes automatisk for den opprinnelige bestillingen eller salgsordren. Standard TDS-gruppe vises i den konserninterne ordren, slik at TDS kan beregnes. Du kan endre TDS-gruppen. Fakturaen kan bare posteres hvis netto fakturabeløp i den konserninterne ordren som opprettes automatisk, er i samsvar med netto fakturabeløp i den opprinnelige ordren. (Nettobeløpet er fakturabeløpet etter at TDS er trukket fra.)

La oss si at en salgsfaktura opprettes for 50 000 og TDS-gruppen **10 %** er knyttet til den. Det posterte fakturabeløpet er 45 000, og det posterte TDS-beløpet for salgsfakturaen er 5 000. Det opprettes automatisk en bestilling for den konserninterne salgsordren, og TDS-gruppen **10 %** er knyttet til den. Hvis du endrer TDS-gruppen til **15 %**, kan du ikke postere fakturaen, fordi netto fakturabeløp i den konserninterne salgsordren som ble opprettet automatisk, ikke samsvarer med netto fakturabeløp for den opprinnelige salgsordren.

En betalingsjournal som opprettes for en konsernintern faktura, posteres automatisk. Denne betalingsjournalen kan bare posteres hvis netto betalingsbeløp på den er i samsvar med netto betalingsbeløp i den opprinnelige betalingsjournalen.

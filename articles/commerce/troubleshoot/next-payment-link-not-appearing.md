---
title: Lagring for mitt neste betalingsalternativ vises ikke
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe når avmerkingsboksen Lagre for neste betaling ikke vises under Betalingsmåte på betalingssiden til et e-handelsområde.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 679c2453068695caca03ac9618573eba0686b863
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347326"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Alternativet Lagre for min neste betaling vises ikke

[!include [banner](../../includes/banner.md)]

Dette emnet gir feilsøkingsveiledning som kan hjelpe når avmerkingsboksen **Lagre for neste betaling** ikke vises under **Betalingsmåte** på betalingssiden til et e-handelsområde.

## <a name="description"></a>beskrivelse

Avmerkingsboksen **Lagre for min neste betaling** vises ikke i delen **Betalingsmåte** på betalingssiden til en e-handel.

Illustrasjonen nedenfor viser et eksempel på en utsjekkingsside som inneholder avmerkingsboksen **Lagre for min neste betaling**.

![Lagre for min neste betaling i betalingsmodulen.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Løsning

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Kontroller at Dynamics 365 Payment Connector for Adyen er riktig konfigurert i Commerce Headquarters

Hvis du vil kontrollere at Dynamics 365 Payment Connector for Adyen er riktig konfigurert i Commerce Headquarters, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Kanaler \> Nettbutikker**.
1. Velg nettbutikken.
1. I hurtigfanen **Betalingskontoer** kontrollerer du at feltet **Tillat lagring av betalingsinformasjon i e-handel** er satt til **Sann**.

![Tillat lagring av betalingsinformasjon i e-handelsfelt i Commerce Headquarters.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Tilleggsressurser

[Betalingsmodul](../payment-module.md)

[Lagre betalingsmåter på nett med Adyen-koblingen](../dev-itpro/adyen-connector-listPI.md)

---
title: Lagring for mitt neste betalingsalternativ vises ikke
description: Denne artikkelen gir feilsøkingsveiledning som kan hjelpe når avmerkingsboksen Lagre for neste betaling ikke vises under Betalingsmåte på betalingssiden til et e-handelsområde.
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
ms.openlocfilehash: efa04c87f78c376fd00da1b26aedb9e8b428dfa5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871561"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Alternativet Lagre for min neste betaling vises ikke

[!include [banner](../../includes/banner.md)]

Denne artikkelen gir feilsøkingsveiledning som kan hjelpe når avmerkingsboksen **Lagre for neste betaling** ikke vises under **Betalingsmåte** på betalingssiden til et e-handelsområde.

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

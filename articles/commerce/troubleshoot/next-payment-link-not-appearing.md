---
title: Lagring for mitt neste betalingsalternativ vises ikke
description: Denne artikkelen gir feilsøkingsveiledning som kan hjelpe når avmerkingsboksen Lagre for neste betaling ikke vises under Betalingsmåte på betalingssiden til et e-handelsområde.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287491"
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

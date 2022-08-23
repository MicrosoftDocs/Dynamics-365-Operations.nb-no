---
title: Betalinger utlignes automatisk før ordrer faktureres eller sendes
description: Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe når en betaling utlignes i Adyen-portalen rett etter at en ordre er lagt inn, selv om salgsordren ikke er fakturert eller sendt.
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
ms.openlocfilehash: 6fdaf48600edc22b5423e0167177616758e2dc6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282714"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Betalinger utlignes automatisk før ordrer faktureres eller sendes

[!include [banner](../../includes/banner.md)]

Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe når en betaling utlignes i Adyen-portalen rett etter at en ordre er lagt inn, selv om salgsordren ikke er fakturert eller sendt.

## <a name="description"></a>beskrivelse

Etter at en ordre er plassert, blir betalingen umiddelbart utlignet i Adyen-portalen, selv om salgsordren ikke er fakturert eller sendt.

## <a name="resolution"></a>Oppløsning

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Konfigurere manuell henting for e-handelbetalinger i Adyen-portalen

Hvis du vil konfigurere manuell henting for e-handelsbetalinger i Adyen-portalen, gjør du følgende.

1. Logg på Adyen-portalen.
1. Velg forretningskontoen for e-handelskanalen øverst til høyre.
1. Velg **Konto** i det øverste navigasjonsfeltet, og velg deretter **Innstillinger**.
1. Velg **manuell** i feltet **Opptaksforsinkelse**.

    ![Innstillingen Opptaksforsinkelse i Adyen-portalen.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Tilleggsressurser

[Lagring av Adyen-betaling](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector for Adyen](../dev-itpro/adyen-connector.md)

[Konfigurere Adyen-betalingskobling for Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)

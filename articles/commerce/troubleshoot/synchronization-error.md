---
title: Ordresynkroniseringsfeil relatert til den standard betalingstjenesten
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.
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
ms.openlocfilehash: 6f8e0ea7675ffc5cbada36207422b410234e33afcaec90636e90e573a90ac484
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715242"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Ordresynkroniseringsfeil relatert til den standard betalingstjenesten

[!include [banner](../../includes/banner.md)]

Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.

## <a name="description"></a>beskrivelse

Når du synkroniserer en nettordre, får du følgende feilmelding: Det må være en standard betalingstjeneste for å behandle kredittkorttransaksjoner.

![Feilen Manglende standard betalingstjeneste.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Løsning

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Bekreft eller angi standard betalingstjeneste i Commerce Headquarters

Hvis du vil bekrefte eller angi standard betalingstjeneste i Commerce Headquarters, gjør du følgende.

1. Gå til **Kunder \> Betalingsoppsett \> Betalingstjenester**.
1. Kontroller at alternativet **Standardbehandler for nye kredittkort** er satt til **Ja** for én betalingstjeneste.

## <a name="additional-resources"></a>Tilleggsressurser

[Kredittkortoppsett, godkjenning og registrering](../../finance/accounts-receivable/credit-card-authorizations.md)
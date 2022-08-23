---
title: Ordresynkroniseringsfeil relatert til den standard betalingstjenesten
description: Denne artikkelen gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.
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
ms.openlocfilehash: aa57366fb8f351a8275c947220de78fe809b7b5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276696"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Ordresynkroniseringsfeil relatert til den standard betalingstjenesten

[!include [banner](../../includes/banner.md)]

Denne artikkelen gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.

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

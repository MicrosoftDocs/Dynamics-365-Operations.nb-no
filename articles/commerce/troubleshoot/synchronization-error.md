---
title: Ordresynkroniseringsfeil relatert til den standard betalingstjenesten
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585459"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Ordresynkroniseringsfeil relatert til den standard betalingstjenesten

[!include [banner](../../includes/banner.md)]

Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.

## <a name="description"></a>beskrivelse

Når du synkroniserer en nettordre, får du følgende feilmelding: Det må være en standard betalingstjeneste for å behandle kredittkorttransaksjoner.

![Feilen Manglende standard betalingstjeneste](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Oppløsning

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Bekreft eller angi standard betalingstjeneste i Commerce Headquarters

Hvis du vil bekrefte eller angi standard betalingstjeneste i Commerce Headquarters, gjør du følgende.

1. Gå til **Kunder \> Betalingsoppsett \> Betalingstjenester**.
1. Kontroller at alternativet **Standardbehandler for nye kredittkort** er satt til **Ja** for én betalingstjeneste.

## <a name="additional-resources"></a>Tilleggsressurser

[Kredittkortoppsett, godkjenning og registrering](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)

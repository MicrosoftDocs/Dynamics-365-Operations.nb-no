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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021133"
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

[Kredittkortoppsett, godkjenning og registrering](../../finance/accounts-receivable/credit-card-authorizations.md)
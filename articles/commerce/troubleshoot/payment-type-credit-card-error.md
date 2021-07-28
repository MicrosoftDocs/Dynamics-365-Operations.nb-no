---
title: Betalingstypen må være kredittkortfeil på salgsordresiden
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når det vises en feilmelding på salgsordresiden etter at en ordre er synkronisert.
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
ms.openlocfilehash: 1d6813a642aefa59e20a7c77ddcf53ce7d3625eb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347350"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Feilen Betalingstypen må være kredittkort på salgsordresiden

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når det vises en feilmelding på salgsordresiden etter at en ordre er synkronisert.

## <a name="description"></a>beskrivelse

Når du åpner salgsordresiden etter at du har synkronisert en ordre, får du følgende feilmelding: Betalingstypen må være kredittkort ettersom kredittkortnummeret er angitt.

![Betalingstype må være kredittkortfeil.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Løsning

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Angi betalingstypen i Commerce Headquarters

1. Gå til **Kunder \> Betalingsoppsett \> Betalingsbetingelser**.
1. Velg betalingsbetingelsene til venstre.
1. Kontroller at det er merket av for **Kredittkort** i feltet **Betalingstype**.

## <a name="additional-resources"></a>Tilleggsressurser

[Postering av elektroniske salg og betalinger](../tasks/posting-online-sales-payments.md)

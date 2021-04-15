---
title: Betalingstypen må være kredittkortfeil på salgsordresiden
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når det vises en feilmelding på salgsordresiden etter at en ordre er synkronisert.
author: Reza-Assadi
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801681"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Feilen Betalingstypen må være kredittkort på salgsordresiden

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når det vises en feilmelding på salgsordresiden etter at en ordre er synkronisert.

## <a name="description"></a>beskrivelse

Når du åpner salgsordresiden etter at du har synkronisert en ordre, får du følgende feilmelding: Betalingstypen må være kredittkort ettersom kredittkortnummeret er angitt.

![Betalingstype må være kredittkortfeil](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Oppløsning

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Angi betalingstypen i Commerce Headquarters

1. Gå til **Kunder \> Betalingsoppsett \> Betalingsbetingelser**.
1. Velg betalingsbetingelsene til venstre.
1. Kontroller at det er merket av for **Kredittkort** i feltet **Betalingstype**.

## <a name="additional-resources"></a>Tilleggsressurser

[Postering av elektroniske salg og betalinger](../tasks/posting-online-sales-payments.md)

---
title: Bekrefte betalingsplaner for aktivaleie i en bunke
description: Denne artikkelen forklarer hvordan du bekrefter flere betalingsplaner i en bunke.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895058"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Bekrefte betalingsplaner for aktivaleie i en bunke

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du bekrefter flere betalingsplaner i en bunke. Betalingsplaner bekreftes enten på en leie-til-leie-basis eller gjennom bunkeprosessen for bekreftelse. En journaloppføring kan bare posteres mot en leieavtale som har en bekreftet betalingsplan. Bekreftelse av betalingsplanen fungerer som en endelig godkjenning av den økonomiske informasjonen for leieavtalen. Alle fremtidige endringer i den økonomiske informasjonen for leieavtalen, for eksempel betalinger og leieperioden, utgjør en leiejustering og skal behandles på denne måten.

Hvis du vil bekrefte flere betalingsplaner, følger du denne fremgangsmåten.

1. Gå til **Aktivaleie \> Periodisk \> Bekreftelsesbunke**.
2. På siden **Bekreftelsesbunke** velger du **Bekreftelsesbunke**.
3. I dialogboksen som vises, filtrerer du for tablåene du vil bekrefte.

    - Hvis du vil bekrefte alle tablåene i en bestemt leiegruppe, velger du gruppen i feltet **Leiegruppe**.
    - Hvis du vil bekrefte bestemte tablåer, velger du tablåene i feltet **Tablå-ID**.
    - Hvis du vil bekrefte alle tablåer, aktiverer du parameteren **For alle tablåer**.

Informasjon for de nylig bekreftede bøkene vises på siden **Bekreftede tablåer**. Etter at betalingsplanene er bekreftet, kan journaloppføringene for opprinnelig føring posteres mot leieavtalen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

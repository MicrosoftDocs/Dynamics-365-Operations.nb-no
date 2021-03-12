---
title: Bekrefte betalingsplaner for aktivaleie i en bunke
description: Dette emnet forklarer hvordan du bekrefter flere betalingsplaner i en bunke.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971384"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Bekrefte betalingsplaner for aktivaleie i en bunke

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du bekrefter flere betalingsplaner i en bunke. Betalingsplaner bekreftes enten på en leie-til-leie-basis eller gjennom bunkeprosessen for bekreftelse. En journaloppføring kan bare posteres mot en leieavtale som har en bekreftet betalingsplan. Bekreftelse av betalingsplanen fungerer som en endelig godkjenning av den økonomiske informasjonen for leieavtalen. Alle fremtidige endringer i den økonomiske informasjonen for leieavtalen, for eksempel betalinger og leieperioden, utgjør en leiejustering og skal behandles på denne måten.

Hvis du vil bekrefte flere betalingsplaner, følger du denne fremgangsmåten.

1. Gå til **Aktivaleie \> Periodisk \> Bekreftelsesbunke**.
2. På siden **Bekreftelsesbunke** velger du **Bekreftelsesbunke**.
3. I dialogboksen som vises, filtrerer du for tablåene du vil bekrefte.

    - Hvis du vil bekrefte alle tablåene i en bestemt leiegruppe, velger du gruppen i feltet **Leiegruppe**.
    - Hvis du vil bekrefte bestemte tablåer, velger du tablåene i feltet **Tablå-ID**.
    - Hvis du vil bekrefte alle tablåer, aktiverer du parameteren **For alle tablåer**.

Informasjon for de nylig bekreftede bøkene vises på siden **Bekreftede tablåer**. Etter at betalingsplanene er bekreftet, kan journaloppføringene for opprinnelig føring posteres mot leieavtalen.

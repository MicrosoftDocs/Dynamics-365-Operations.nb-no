---
title: Begrense betalingsmåter for returer uten en kvittering
description: Dette emnet beskriver hvordan bestemte betalingstyper kan være begrenset for refusjon hvis returer gjøres uten et mottak.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1ff301aa5f88e34ed7ca24aa54df3fdc7daa1bf7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012397"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Begrense betalingsmåter for returer uten en kvittering


[!include [banner](includes/banner.md)]

Hver betalingstype en forhandler godtar, må konfigureres når systemet defineres. Dette emnet beskriver hvordan bestemte betalingstyper kan være begrenset for refusjon hvis returer gjøres uten et mottak.

## <a name="set-up-payment-methods"></a>Definere betalingsmåter

Du må fullføre følgende oppgaver hvis du vil definere betalingsmåter.
1. Opprett betalingsmåtene som godtas av hele organisasjonen.
2. Opprett korttyper og kortnumre for hele organisasjonen. Hvis kredittkortene eller debetkortene godtas, må du opprette én betalingsmetode for kort og deretter opprette korttypene og kortnumrene for hele organisasjonen.
3. Definere betalingsmåter i butikker. Knytt betalingsmåter til hver butikk, og angi deretter de butikkspesifikke innstillingene for hvert betalingsmåte.
4. Definer kortbetalingsmåter for butikker. Fullfør kortoppsettet for alle kortbetalingsmåter som butikken godtar.

![Butikkoppsett](media/NoReceiptReturns1.png "Oppsett av detaljhandel") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Begrense betalingsmåter for returer uten en kvittering

For hver betalingsmåte for butikk, på siden **Butikkadministrasjon** under **Returer uten kvittering**, sett **Begrens for refusjoner uten kvittering** til **Ja**. 

Standardverdien for av/på er **Nei**, som sikrer at betalingsmåten er tillatt for refusjoner. 

Når **Begrens for refusjoner uten kvittering** er satt til **Ja**, tillates ikke den valgte betalingsmåten for refusjoner. 

![Butikkbetalingsmåte](media/NoReceiptReturns3.png "Betalingsmåte for detaljhandel") 

> [!NOTE]
> Når en kasserer legger til en betalingsmåte som er begrenset for refusjon uten kvittering, vises en melding for å bekrefte de akseptable betalingsmåtene.

![Akseptable betalingsmåter](media/NoReceiptReturns4.png "Akseptable betalingsmåter") 

Hvis en transaksjon har både en retur med kvittering og en retur uten kvittering, fremtvinges ikke begrensningsbetingelsene, fordi transaksjonen vil være en returarbeidsflyt med kvittering. 


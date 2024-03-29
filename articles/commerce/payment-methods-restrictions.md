---
title: Begrense betalingsmåter for returer uten en kvittering
description: Denne artikkelen beskriver hvordan bestemte betalingstyper kan være begrenset for refusjon hvis returer gjøres uten et mottak.
author: josaw1
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: 9b14d7d8f6a2d9209ad6a12cd53bce4a9b50178d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281403"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Begrense betalingsmåter for returer uten en kvittering


[!include [banner](includes/banner.md)]

Hver betalingstype en forhandler godtar, må konfigureres når systemet defineres. Denne artikkelen beskriver hvordan bestemte betalingstyper kan være begrenset for refusjon hvis returer gjøres uten et mottak.

## <a name="set-up-payment-methods"></a>Definere betalingsmåter

Du må fullføre følgende oppgaver hvis du vil definere betalingsmåter.
1. Opprett betalingsmåtene som godtas av hele organisasjonen.
2. Opprett korttyper og kortnumre for hele organisasjonen. Hvis kredittkortene eller debetkortene godtas, må du opprette én betalingsmetode for kort og deretter opprette korttypene og kortnumrene for hele organisasjonen.
3. Definere betalingsmåter i butikker. Knytt betalingsmåter til hver butikk, og angi deretter de butikkspesifikke innstillingene for hvert betalingsmåte.
4. Definer kortbetalingsmåter for butikker. Fullfør kortoppsettet for alle kortbetalingsmåter som butikken godtar.

![Butikkoppsett.](media/NoReceiptReturns1.png "Oppsett av detaljhandel") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Begrense betalingsmåter for returer uten en kvittering

For hver betalingsmåte for butikk, på siden **Butikkadministrasjon** under **Returer uten kvittering**, sett **Begrens for refusjoner uten kvittering** til **Ja**. 

Standardverdien for av/på er **Nei**, som sikrer at betalingsmåten er tillatt for refusjoner. 

Når **Begrens for refusjoner uten kvittering** er satt til **Ja**, tillates ikke den valgte betalingsmåten for refusjoner. 

![Butikkbetalingsmåte.](media/NoReceiptReturns3.png "Betalingsmåte for detaljhandel") 

> [!NOTE]
> Når en kasserer legger til en betalingsmåte som er begrenset for refusjon uten kvittering, vises en melding for å bekrefte de akseptable betalingsmåtene.

![Akseptable betalingsmåter.](media/NoReceiptReturns4.png "Akseptable betalingsmåter") 

Hvis en transaksjon har både en retur med kvittering og en retur uten kvittering, fremtvinges ikke begrensningsbetingelsene, fordi transaksjonen vil være en returarbeidsflyt med kvittering. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]

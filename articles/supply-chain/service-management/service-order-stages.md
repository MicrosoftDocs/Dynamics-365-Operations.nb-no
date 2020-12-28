---
title: Serviceordrestadier
description: Når du definerer stadiene for en serviceordre og tilordner dem til arbeidere, kan du styre flyten i en serviceordre gjennom oppgavene som ulike personer utfører i serviceorganisasjonen.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bcb72e8222b378198fcd044428fa1a4a0e8944
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434092"
---
# <a name="service-order-stages"></a>Serviceordrestadier   

[!include [banner](../includes/banner.md)]


Du kan opprette stadier for en serviceordre for å definere oppgavene som må fullføres, rekkefølgen de skal fullføres i, og arbeiderne som er ansvarlige for å fullføre dem. Når du definerer stadiene for en serviceordre og tilordner dem til arbeidere, kan du styre flyten i en serviceordre gjennom oppgavene som ulike personer utfører i serviceorganisasjonen. Stadienes rekkefølge må inneholde et innledende stadium.

Du kan også definere hvilke handlinger som skal tillates på hvert stadium. Hvis du for eksempel fjerner merket for **Poster** for alle stadier unntatt det siste stadiet, hindrer du at serviceordrer posteres før serviceordrene er behandlet i hele sekvensen av stadier.

## <a name="branching-in-service-order-stages"></a>Forgrening i serviceordrestadier

Når du oppretter et servicestadium, kan du opprette flere alternativer, eller grener, som du kan velge blant for det neste servicestadiet. Alle grenene du oppretter, er tilgjengelige for valg når det innledende stadiet er fullført. La oss si at du definerer **Planlegging** som et første stadium. Du oppretter to stadier kalt **Pågår** og **Avbryt**, og velger deretter **Planlegging** som overordnet for dem. Du tilordner **Planlegging**-stadiet til salgsordren. Når planleggingsstadiet for salgsordren er fullført, kan du velge stadiet **Pågår** hvis salgsordren er klar til å bli arbeidet med, eller du kan velge stadiet **Avbryt** hvis salgsordren er avbrutt.

## <a name="see-also"></a>Se også

[Definer serviceordrestadier](set-up-service-order-stages.md)

[Endre serviceordrestadiet](change-service-order-stage.md)

  



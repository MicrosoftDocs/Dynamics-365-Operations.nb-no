---
title: Automatisk opprette serviceordrer
description: Du kan generere serviceordrer som er basert på serviceavtale, for den gyldige perioden for serviceavtalen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08fb7363ab87fd6a7f3d38406e72b1f542dc2c2a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434587"
---
# <a name="automatically-create-service-orders"></a>Automatisk opprette serviceordrer 

[!include [banner](../includes/banner.md)]


Du kan generere serviceordrer som er basert på serviceavtale, for den gyldige perioden for serviceavtalen.

Serviceordrer du genererer fra en serviceavtale, vil alle være knyttet til den aktuelle serviceavtalen.

Serviceordrer genereres automatisk fra følgende innstillinger:

  - Serviceavtaleintervallet som er definert på serviceavtalelinjene. Serviceavtaleintervallet angir hvor ofte det opprettes serviceordrelinjer. Hvis du vil ha mer informasjon om serviceintervaller, se [Serviceintervaller](service-intervals.md).

  - Perioden du angir for å definere serviceperioden i feltene **Fra dato** og **Til dato** i skjemaet **Opprett serviceordrer**. Hvis du vil ha mer informasjon om å kombinere serviceordrer, se [Opprette serviceordrer automatisk](create-service-orders-automatically.md).

  - Alternativet **Kombiner serviceordrer** i serviceavtalehodet. Dette alternativet definerer om serviceordrelinjer som er generert fra en serviceavtale, kombinerer serviceordrer i henhold til ansatt, serviceoppgave, serviceobjekt eller serviceavtale. Hvis du vil ha mer informasjon, se [Kombinere serviceordrer](combine-service-orders.md).

  - Alternativet **Tidsvindu** på serviceavtalelinjen. Tidsvinduet definerer hvor langt en serviceordrelinje kan flyttes i forhold til den beregnede datoen. Hvis du vil har mer informasjon, se [Tidsvinduer](time-windows.md).


> [!NOTE]
> <P>Hvis dagen som er angitt for en serviceordre, ikke er åpen i kalenderen du har valgt i skjemaet <STRONG>Servicestyringsparametere</STRONG>, får du en melding om at det er en konflikt med kalenderen. Du kan trygt ignorere denne meldingen. Srviceordren opprettes selv om dagen er lukket i kalenderen.</P>

## <a name="example-1"></a>Eksempel 1

Serviceavtalen varer fra 1. januar 2012 til 31. desember 2012. Hvis serviceperioden du angir i skjemaet **Opprett serviceordrer**, går fra 1. november 2012 til 1. februar 2013, opprettes det serviceordrer fra 1. november 2012 til 31. desember 2012.

## <a name="example-2"></a>Eksempel 2

Serviceavtalen varer fra 1. januar 2012 til 31. desember 2012. To serviceavtalelinjer er knyttet til serviceavtalen. Den første serviceavtalelinjen har startdatoen 2. januar 2012 og sluttdatoen 1. mars 2012. Den andre serviceavtalelinjen har startdatoen 1. april 2012 og sluttdatoen 31. desember 2012. Du kan angi en periode i skjemaet **Opprett serviceordrer** som går fra 1. oktober 2012 til 31. desember 2012. Det genereres derfor bare serviceordrer for den andre avtalelinjen, siden startdatoen og sluttdatoen for den første avtalelinjen er før perioden du angav for serviceordren.

  



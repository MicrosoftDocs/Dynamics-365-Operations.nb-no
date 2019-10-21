---
title: Planlegge arbeidsordre på bestemt dato og klokkeslett
description: Dette emnet forklarer hvordan du planlegger en arbeidsordre på en bestemt dato og klokkeslett i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f818c4c3b669cc94e37cba1e3571c57b5c0dd1b
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887371"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Planlegge arbeidsordre på bestemt dato og klokkeslett

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Hvis en arbeidsordre må planlegges på en bestemt dato *og* klokkeslett, kan du overstyre standard planleggingsprosess i Aktivastyring og opprette en bestemt tidsplan for en arbeidsordre.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. I arbeidsordrelisten klikker du på ID-en for arbeidsordren i kolonnen **Arbeidsordre**.

3. Klikk **Rediger**.

4. Sett inn start- og sluttdato og klokkeslett i feltene **Forventet start** og **Forventet slutt** i hurtigfanen **Arbeidsordrehode**.

![Figur 1](media/05-work-order-scheduling.png)

5. I kategorien **Generelt** klikker du på **Planlegg** for å bruke standard planleggingsprosess, eller klikker på **Fordeling** hvis du vil tilordne arbeidsordren til en bestemt arbeider.

6. Hvis du vil overstyre eventuelle eksisterende kapasitetsreservasjoner for å sikre at arbeidsordren planlegges i den forventede perioden, gjør du valgene som vist i figuren nedenfor i dialogboksen **Planlegg arbeidsordre** > **Begrenset kapasitet**-delen. Dette betyr at planleggingsprosessen vil ignorere eksisterende kapasitetsreservasjoner fordi arbeidsordren må starte på forventet starttidspunkt.

![Figur 2](media/06-work-order-scheduling.png)

7. Klikk på **OK** for å starte planleggingen.

8. Hvis planleggingsprosessen resulterer i dobbeltreservering, vil du se en melding på skjermen, og du kan justere de tilknyttede arbeidsordrene.

>[!NOTE]
>Hvis du vil planlegge en vedlikeholdsperson for arbeidsordren, må vedlikeholdspersonen være tilgjengelig på forventet startdato og -klokkeslett. Arbeidertilgjengelighet defineres i [arbeiderkalenderen](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 

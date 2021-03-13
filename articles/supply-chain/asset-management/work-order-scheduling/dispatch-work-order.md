---
title: Fordelingsarbeidsordre
description: Dette emnet forklarer hvordan du fordeler arbeidsordrer i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b4b05dfe351bb61dc47c9c2bfe30831ab7b0a16
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016862"
---
# <a name="dispatch-work-order"></a>Fordelingsarbeidsordre

[!include [banner](../../includes/banner.md)]

 

Du kan planlegge én arbeidsordre eller arbeidsordrejobber til én arbeider ved hjelp av **fordeling**-funksjonen.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren i listen.

3. Gå til fanen **Generelt**, og klikk på **Fordeling**.

4. I dialogboksen **Planlegg arbeidsordre** velger du arbeideren i **Arbeider**-feltet.

5. I feltet **Planlegg timer** kan du sette inn forventede arbeidstimer i tilfelle forventede arbeidstimer avviker fra prognosetimer.

6. I **Planlagt start** -feltet kan du redigere startdato og -klokkeslett om nødvendig.

7. Hvis planleggingsprosessen skal observere kapasitetsbegrensninger for ressurser som allerede er planlagt for andre jobber, må du kontrollere at veksleknappene for **Aktivum**, **Verktøy** og **Arbeider** er satt til **Ja**. Hvis du vil ha detaljert informasjon om planleggingsprosessen, velger du **Ja** på **Detaljert**-veksleknappen. Dette betyr at detaljert informasjon om de beregnede resultatene for arbeidsordren vises i informasjonsloggen.

8. Velg **Ja** på veksleknappen **Ignorer tidsplan** for å ignorere lukkede dager i kalenderen (gjelder for aktiva, arbeider og verktøy). Velg **Ja** på veksleknappen **Ignorer planlagt kjøring** for å ignorere begrensninger som kan ha blitt valgt for arbeidsordren angående planlegging. 

    Se delen [Planlagt kjøring](../setup-for-work-orders/scheduled-execution.md) hvis du vil ha informasjon om oppsett av planlagt kjøring.

9. Klikk på **OK**. Livssyklustilstanden for arbeidsordren oppdateres automatisk til livssyklustilstanden **Planlagt** som er angitt i **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Livssyklusmodeller**.

Figuren nedenfor viser et eksempel på fordelingsvalg i dialogboksen **Planlegge arbeidsordre**.

![Figur 1](media/04-work-order-scheduling.png)

[!NOTE]
Hvis du vil slette tidsplanen for en arbeidsordre, velger du arbeidsordren i **Alle arbeidsordrer**, og deretter klikker du på **Slett tidsplan** i fanen **Generelt**. Husk å oppdatere livssyklustilstanden for arbeidsordren manuelt hvis du sletter tidsplanen.


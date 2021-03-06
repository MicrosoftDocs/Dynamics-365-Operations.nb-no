---
title: Kostnader for vedlikeholdsplan
description: Dette emnet beskriver kostnader for vedlikeholdsplan i Aktivastyring.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 405fd7fbbbb8862446d09b9ea33ef14348e691f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813779"
---
# <a name="maintenance-schedule-cost"></a>Kostnader for vedlikeholdsplan

[!include [banner](../../includes/banner.md)]

 

I Aktivastyring kan du beregne budsjettkostnader på vedlikeholdsplanlinjer. Dette er nyttig hvis du vil ha en oversikt over forventede kostnader, for eksempel kostnader knyttet til planlagte forebyggende vedlikeholdsjobber for neste år. Beregningene er basert på eksisterende vedlikeholdsplanlinjer av typen Vedlikeholdsplaner, Vedlikeholdsrunder og Vedlikeholdsforespørsler.

1. Klikk på **Aktivastyring** > **Forespørsler** > **Aktiva** > **Kostnader for vedlikeholdsplan**.

2. I dialogboksen **Kostnader for vedlikeholdsplan** kan du velge et **finansdimensjonssett** hvis du vil se kostnader gruppert i finansdimensjoner.

>[!NOTE]
>Finansdimensjonssett blir definert i **Finans** > **Kontoplan** > **Dimensjoner** > **Finansdimensjonssett**.

3. Du kan bruke **Nivå**-feltet til å angi hvor detaljert vedlikeholdsplanlinjene skal være når det gjelder arbeidssted. Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene på alle arbeidsstedsnivåene de er relatert til.

4. Hvis du vil gjøre en beregning for bestemte aktiva , klikker du på **Filter** i hurtigfanen **Poster som skal inkluderes**, og velger de relevante aktivaene. Hvis det er nødvendig, kan du også angi en **Forventet startdato** for kostberegningen, eller velge en annen **Status** for kostberegningen.

5. Klikk på **OK** for å starte kostberegningen.

6. I fanen **Kostnader for vedlikeholdsplan** > i **Grupper etter...**-handlingsrutegruppene klikker du på de relevante knappene for å vise det nødvendige detaljnivået for kostnadsberegningen. De valgte handlingsrutegruppeknappene er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

7. Klikk på knappen **Beregn kostnad** hvis du vil foreta en ny kostberegning.

Illustrasjonen nedenfor viser resultatet av en beregning av kostnader for vedlikeholdsplan.

![Figur 1](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
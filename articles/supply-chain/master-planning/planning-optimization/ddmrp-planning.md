---
title: Etterspørselsdrevet planlegging
description: Artikkelen beskriver hvordan du genererer planlagte bestillinger for varer som er angitt som utkoblingspunkter.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740309"
---
# <a name="demand-driven-planning"></a>Etterspørselsdrevet planlegging

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Artikkelen beskriver hvordan du genererer planlagte bestillinger for varer som er angitt som utkoblingspunkter.

## <a name="net-flow-and-qualified-demand"></a>Nettoflyt og kvalifisert etterspørsel

Under hovedplanleggingen bruker systemet konseptet *nettoflyt* for å etablere den effektive lagerbeholdningen basert på den faktiske lagerbeholdningen, pluss beholdning som er i bestilling (eksisterende forsyningsordrer som ennå ikke er mottatt), minus det som kalles for *kvalifisert etterspørsel* (kvalifisert kommende salg), som vist i illustrasjonen nedenfor. Når systemet skal fastslå hvilken buffersone en vare tilhører og hva det bestilte antallet skal være, evaluerer det nettoflyten, ikke den faktiske lagerbeholdningen.

![Eksempel på et diagram for beregning av nettoflyt.](media/ddmrp-net-flow-example.png "Eksempel på et diagram for beregning av nettoflyt")

Når en planlagt bestilling utløses under en planleggingskjøring, vil det bestilte antallet være maksimumsnivået minus nettoflyten. Når du skal tilordne en ordreprioritet, bruker systemet [prioritetsbasert planleggingsfunksjonalitet](priority-based-planning.md) i stedet for behovsdatoer. DDMRP (Demand Driven Material Requirements Planning – etterspørselsdrevet planlegging av materialkrav) tilordner prioriteten til en planlagt bestilling basert på det bestilte antallet som en prosent av maksimum beholdning. I den forrige illustrasjonen er det bestilte antallet 53 prosent av det maksimale antallet. Derfor blir ordreprioriteten for etterfylling 53. (For kontekst har 0 høyest prioritet, og 100 har lavest prioritet.)

*Kvalifisert etterspørsel* er den etterspørsel etter forfallsdato, pluss dagens etterspørsel, pluss kvalifiserte bestillingstopper i fremtiden. Illustrasjonen nedenfor viser et eksempel på etterspørselsnivåene for i dag (12. juni) og de neste tre dagene. Med DDMRP kan du definere en terskel for en kraftig økning for å identifisere etterspørsel som overgår vanlige forventninger. Hvis terskelen er satt til 25 stykker, vil to av de fremtidige datoene som vises i illustrasjonen, være kvalifisert som bestillingstopper. Du må tilordne en terskel for bestillingstopp for hvert produkt individuelt ved å bruke produktets **Varedekning**-side, som beskrevet i [Definer buffere for en vare som har et utkoblingspunkt](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Eksempel på et diagram for beregning av kvalifisert etterspørsel.](media/ddmrp-net-qualified-demand-example.png "Eksempel på et diagram for beregning av kvalifisert etterspørsel")

Forutsatt at det ikke er forfalt etterspørsel, kan du nå legge til dagens etterspørsel (18) i antallene for de to bestillingstoppene (29 og 26) for å få et kvalifisert behov på 73. Selv om det er etterspørsel for 23. juni, kan du legge merke til at det ikke er inkludert i beregningen av nettoflyten, fordi DDMRP utløser en planlagt bestilling på en annen måte enn tradisjonelle planlegging av dekningsgrupper.

## <a name="generating-planned-orders-with-ddmrp"></a>Generering av planlagte bestillinger med DDMRP

Under en planleggingskjøring vil systemet opprette en ny planlagt bestilling hvis nettoflyten for en vare synker under gjenbestillingspunktet. Når du bruker DDMRP, vil du vanligvis utføre en planleggingskjøring hver dag. Derfor kontrollerer du essensielt beholdningsnivåene én gang om dagen for å finne ut hvilke varer som må etterfylles.

Illustrasjonen nedenfor viser et eksempel på en situasjon der du har en bestilling på 18 stykker den 20. juni, 29 stykker den 21. juni, 26 stykker den 22. juni og 20 stykker den 23. juni. Siden terskelen for kraftig økning er satt til 25 stykker, flagges to av disse ordrene som kraftige økninger. Det er 220 stykker av denne varen på lager.

![Planleggingseksempel 1.](media/ddmrp-planning-example-1.png "Planleggingseksempel 1")

Hvis du kjører hovedplanlegging nå, genererer dette en planlagt bestilling hvis nettoflyten synker under gjenbestillingspunktet (219 stykker i dette eksemplet).

![Planleggingseksempel 2.](media/ddmrp-planning-example-2.png "Planleggingseksempel 2")

I dette eksemplet produseres et bestillingsforslag for et antall på 130, som tilsvarer maksimumsnivået minus nettoflyten. Den planlagte bestillingen tilordnes en prioritet på 53,07, basert på prosenten av maksimalt antall. Siden disse verdiene ble funnet 20. juni, oppretter systemet en planlagt bestilling som er datert 20. juni, pluss den utkoblede leveringstiden for varen (fem virkedager i dette eksemplet). Fordi fem virkedager er én uke fra i dag, er den planlagte bestillingen datert til 27. juni.

> [!NOTE]
> Hovedplanlegging beregner bare utkoblede varer ved hjelp av DDMRP. Alle andre varer beregnes ved hjelp av standard planlegging av materialbehov (MRP).

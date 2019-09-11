---
title: Vedlikeholdsstatus
description: Dette emnet forklarer hvordan du beregner vedlikeholdsstatus i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918355"
---
# <a name="maintenance-status"></a>Vedlikeholdsstatus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Aktivastyring kan du foreta en beregning for å se en oversikt over nye, aktive og fullførte vedlikeholdsforespørsler, arbeidsordrer og aktiviteter for vedlikeholdsnedetid for en bestemt periode. Du kan også se antall fullførte betingelsesvurderinger for samme periode. Bruk denne beregningen til å få en oversikt over arbeidsbelastningen for innkommende og fullførte vedlikeholdsforespørsler og arbeidsordrer.

## <a name="make-a-maintenance-status-calculation"></a>Foreta en vedlikeholdsstatusberegning

1. Klikk på **Aktivastyring** > **Forespørsler** > **Vedlikeholdsstatus**.

2. I dialogboksen **Beregn status** velger du perioden du vil gjøre beregningen for, i feltene **Fra dato** og **Til dato**.

3. Du kan bruke **Nivå**-feltet til å angi hvor detaljert vedlikeholdslinjene skal være når det gjelder arbeidssted. Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdslinjene for et arbeidssted på øverste nivå, og derfor kan det hende at statusen på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. Hvis du setter inn tallet 0 i **Nivå**-feltet, ser du et detaljert resultat som viser alle vedlikeholdslinjene på alle arbeidsstedsnivåene de er relatert til.

4. Klikk på **OK** for å starte beregningen.

5. I handlingsrutegruppene **Grupper etter...** klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen. De valgte handlingsrutegruppeknappene er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

6. Husk å klikke på **Oppdater**-knappen for å oppdatere beregningen hver gang du gjør endringer ved å aktivere eller deaktivere **Grupper etter...**-knappene, eller ved å gjøre en beregning for en ny periode.

7. Klikk på **Status** hvis du vil opprette en ny vedlikeholdsstatusberegning.

>[!NOTE]
>Resultatene som vises i **Vedlikeholdsstatus**, inkluderer bare vedlikeholdsforespørsler og arbeidsordrer med faktisk startdato og -klokkeslett. Sluttdato og -klokkeslett kan være tomt.

*Eksempel 1:*

I figuren nedenfor er knappene **År** og **Måned** aktivert. Her får du en generell oversikt på månedlig basis av arbeidsmengde og gjennomstrømning relatert til vedlikeholdsforespørsler og arbeidsordrer. 

![Figur 1](media/13-controlling-and-reporting.png)

*Eksempel 2:*

I figuren nedenfor er informasjon om arbeidssteder lagt til. Nå er det mulig å sammenligne arbeidsmengde og gjennomstrømming mellom arbeidssteder, som kan representere geografiske steder, fabrikker eller arbeidsområder. 

![Figur 2](media/14-controlling-and-reporting.png)


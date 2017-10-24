---
title: Kanban-jobbplanlegging for Lean manufacturing
description: "Denne artikkelen inneholder informasjon om visuell kontroll over planlegging av kanban-jobb og forskjellige måter å planlegge kanban-jobber."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a8b2949fde28d83968f45535a5c47f263efbb18f
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kanban-jobbplanlegging for Lean manufacturing

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om visuell kontroll over planlegging av kanban-jobb og forskjellige måter å planlegge kanban-jobber.  

Siden **Kanban-jobbplanlegging** gir visuell kontroll over tidsplanene for arbeidsceller for lean manufacturing. Den gir en oversikt over alle kanban-jobber og inneholder flere filtreringsmuligheter. Du kan flytte til alle andre sider som er knyttet til kanban-konfigurasjon og -kjøring fra denne siden.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Automatisk planlegging av kanban-jobber
Planlegging kan utløses automatisk hvis du angir parameteren **Antall for automatisk planlegging** for kanban-regelen. Hvis du setter **Antall for automatisk planlegging** til **1**, hver kanban-jobben er planlagt umiddelbart når det er opprettet. Resultatet er en serie med operasjoner av typen første pull, første betjening. Hvis du setter **Antall for automatisk planlegging** til en verdi som er mer enn 1, grupperes kanban-jobber før de planlegges. 

Dette konseptet gjør det mulig for kanban-størrelser å bli redusert til under de faktiske økonomiske partistørrelsene. Den økonomiske gruppestørrelse for et bestemt element (eller varefamilie) er for eksempel 30. I stedet for å opprette kanbaner som bruker produktantallet, 30, kan du konfigurere kanban-regelen slik at den har et produktantall på 10 og en **Antall for automatisk planlegging**-verdi av **3**. Selv om automatisk planlegging planlegger kanban-jobbene for arbeidscellen bare når det finnes tre ikke-planlagte jobber, er det helt transparent for planleggeren og arbeidslederen at to ikke-planlagte jobber kan vente på kjøring. Planleggeren eller arbeidslederen kan deretter ta de to jobbene i produksjonen ved å planlegg dem manuelt eller opprette ekstra Kanbaner.

## <a name="manual-scheduling"></a>Manuell planlegging
Microsoft Dynamics AX 2012 innførte kanban-plankortet for manuell planlegging. Manuell planlegging kan kombineres med automatisk planlegging. Med Kanban-plankortet kan du planlegge og oppheve planlegging av jobber, flyttet dem i rekkefølge, eller flytte dem fra periode til periode. For jobber som er basert på en kanban-regel hvor verdien for **Automatisk planlegging** er mer enn **0**, kan planlegging oppheves manuelt. Disse jobbene blir imidlertid planlagt på nytt når den neste hendelsen for automatisk planlegging forekommer (det vil si når det opprettes en ny kanban). Følgende alternativer er tilgjengelige for manuell planlegging:

-   **Tidsplan** planlegger de valgte jobbene i henhold til forfallsdatoen. (Dette alternativet ligner automatisk planlegging.)
-   **Planlegg fremover fra dato** prøver å planlegge de valgte jobbene i henhold til forfallsdatoen, men begrenser resultatet ved hjelp av den angitte tidligste startdatoen.
-   **Bakover** flytter valgte planlagte jobber bakover i rekkefølgen i perioden.
-   **Forover** flytter valgte planlagte jobber forover i rekkefølgen i perioden.
-   **Forrige periode** flytter de valgte planlagte jobbene til starten eller slutten på forrige periode.
-   **Neste periode** flytter de valgte planlagte jobbene til starten eller slutten på neste periode.
-   **Plan** &gt; **Tilbakestill jobbstatus** lar deg oppheve planlegging av en planlagt jobb.

## <a name="lean-scheduling-groups"></a>Lean-planleggingsgrupper
Hver farge representerer en lean-planleggingsgruppe. Lean-planleggingsgrupper kan defineres fritt som generelle grupper eller grupper som tilhører en enkelt celle. Varer og dimensjoner kan tilordnes fritt til planleggingsgruppene. I en malingscelle kan for eksempel en tidsplangruppe representere en farge for produktet. I arbeid som styres av bestemte krav til verktøy, kan varene være gruppert etter krav til verktøy, og en emballasjearbeidscelle kan gruppere elementer etter emballasjemal. Bruk av farger for lean-planleggingsgrupper er valgfritt men anbefales. Det forbedrer innsyn i statusen for planen. Det er for eksempel svært enkelt å se hvilke farger som produseres på hvilken dag, og du raskt kan se hvordan dette arbeidet kan optimaliseres.

## <a name="work-cell-capacity-and-period-capacity"></a>Arbeidscellekapasitet og periodekapasitet
Kapasitet for en lean-arbeidscelle er alltid samtidig kapasitet. Med andre ord kan flere jobber være aktive i en arbeidscelle samtidig. Kapasitet kan spores i to modi: produksjon og timer.

### <a name="throughput"></a>Produksjon

Kapasiteten for en arbeidscelle er definert av gjennomsnittlig produksjonsantall for en referanseperiode (standard arbeidsdag, uke eller måned). Faktisk kapasitet per dag eller uke beregnes deretter basert på arbeidstiden for kalenderen som er tilordnet til arbeidscellen. Kapasiteten som er lastet etter jobb, er antallet for jobben, justert etter produksjonsforholdet for varen i arbeidscellen.

### <a name="hours"></a>Timeantall

Tilgjengelig kapasitet per dag eller uke er definert av kalenderen som er tilordnet til arbeidscellen. Kapasiteten som er lastet inn etter jobb, er Syklustiden for aktiviteten, justert etter antallet (standard aktivitetsantall kontra faktisk jobbantall) og produksjonsforholdet for varen i arbeidscellen.

#### <a name="period-capacity-factbox"></a>Faktaboksen Periodekapasitet

Listesiden **Kanban-jobbplanlegging** inneholder en faktaboks som viser tilgjengelig og bestilt periodekapasitet for den valgte arbeidscellen. Avhengig av de valgte tidsplanperiodene i produksjonsflytmodellen viser periodene dager eller uker.

<a name="see-also"></a>Se også
--------





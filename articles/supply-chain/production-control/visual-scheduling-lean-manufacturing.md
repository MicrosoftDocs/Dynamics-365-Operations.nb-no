---
title: Visuell planlegging for lean manufacturing
description: Dette emnet gir informasjon om Kanban-plankortet, som produksjonsplanleggeren kan bruke til å kontrollere og optimalisere produksjonsplanen for kanban-jobber.
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization, KanbanBoardUnplannedJobs
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45a63ab0f5baadf6bef646224b3f0bf5327ee923
ms.sourcegitcommit: 4a32634690a741535f3f4babfd753f7c227ad6fe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/05/2020
ms.locfileid: "3958747"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a>Visuell planlegging for lean manufacturing

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om Kanban-plankortet, som produksjonsplanleggeren kan bruke til å kontrollere og optimalisere produksjonsplanen for kanban-jobber.

Dette emnet gir informasjon om Kanban-plankortet, som produksjonsplanleggeren kan bruke til å kontrollere og optimalisere produksjonsplanen for kanban-jobber.

Kanban-plankortet lar produksjonsplanleggeren kontrollere og optimalisere produksjonsplanen for kanban-jobber. Det gjør flyten av kanban-jobber gjennomsiktig og gir produksjonsplanleggeren et verktøy som optimaliserer og justerer produksjonsplanen for arbeidscellen for lean manufacturing.

## <a name="visual-scheduling-of-kanban-jobs"></a>Visuell planlegging av kanban-jobber
En kanban-jobb kan bestå av én eller flere kanban-jobber. Det finnes to typer Kanban-jobber:

-   Prosess
-   Overføring

Du kan planlegge bare jobber av **Prosess** -typen. Kanban-jobben og egenskapene, for eksempel aktivitetstiden, defineres i kanban-flyten for produksjon. I kanban-flyten for produksjon blir kanban-jobben også tilordnet til en arbeidscelle. Den daglige kapasiteten for arbeidscellen beregnes basert på arbeidscellekapasiteten som er angitt i ressursgruppen. Den justeres etter daglig arbeidstid i den tilknyttede kalenderen. Når en kanban-jobben er planlagt, laster jobben kapasiteten for arbeidscellen. Kanban-plankortet inneholder følgende hovedfunksjoner:

-   En grafisk oversikt over produksjonsplanen i en lean-arbeidscelle. Denne oversikten viser de planlagte kanban-prosessjobbene i definerte perioder.
-   Et verktøy som lar deg planlegge ikke-planlagte kanban-jobber og planlegge tidligere planlagte jobber på nytt.

## <a name="kanban-schedule-board"></a>Kanban-plankort
Siden **Kanban-plankort** inneholder sju hovedelementer, som vist i illustrasjonen nedenfor. 

![Kanban-plankort](./media/kanban-schedule-board-1024x554.png)
1.  Handlingsrute
2.  Filter-felt
3.  Knapp for ikke-planlagte jobber
4.  Periode-node
5.  Kanban-jobb
6.  Kapasitetslinje
7.  Tidsskala

### <a name="view-the-time-scale"></a>Vis tidsskalaen

Kortet er delt inn i perioder, og hver periode er representert som en node (4). Periodenodene er oppført på den loddrette aksen, og den vannrette aksen representerer en tidsskala (7) som viser lengden på perioden. En periode har en lengde på en dag eller én uke. Periodlengden avhenger av konfigurasjonen for arbeidscellen som er valgt for Kanban-plankortet (2). For hver periodenode angir Kanban-plankortet hvor mye de planlagte kanban-jobbene lastes i perioden. Det finnes også en indikasjon på maksimum gjennomstrømning for perioden. Hvis den planlagte gjennomstrømningen overskrider den maksimale gjennomstrømningen, regnes perioden som overbelastet, og det vises et rødt varselsymbol. En planlagt kanban-jobb vises i en periode som har planlagte start- og sluttklokkeslett (5). Lengden på jobben er lik aktivitetstiden. Kanban-jobber vises som overlappende i en periode hvis aktivitetstidene overskrider takttiden for arbeidscellen.

### <a name="view-job-status"></a>Vis jobbstatus

Mer informasjon om en kanban-jobb er tilgjengelig i verktøytipset som vises når du holder pekeren over jobben. Et symbol gir informasjon om statusen for jobben. Et klokkesymbol angir for eksempel at kanban-jobben er forfalt.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Bruke farger for å vise Kanban-plankortet

Hvis du vil forbedre oversikten som Kanban-plankortet gir, kan du bruke farger til å skille mellom kanban-jobber. Fargen på en kanban-jobb konfigureres i lean-planleggingsgruppen, der du kan samle produktene som skal produseres i samme sekvens. **Bruk temafarger** -knappen i kategorien **Kort** i handlingsruten lar deg bytte mellom programtemafargene og fargene som er konfigurert i lean-planleggingsgruppen. For hver periode angir en kapasitetslinje (6) hvor mange tilgjengelige timer for perioden som har blitt lastet med kanban-jobber. Hvis perioden er overbelastet, vises kapasitetslinjen tykkere og i rødt. Alle disse funksjonene er tilgjengelige i **Kort** -kategorien i handlingsruten (1) på toppen av siden **Kanban-plankort** .

## <a name="plan-unplanned-jobs"></a>Planlegg ikke-planlagte jobber
Du kan planlegge ikke-planlagte kanban-jobber fra dialogboksen **Planlegg ikke-planlagte jobber** . Hvis du vil åpne denne dialogboksen, klikker du knappen **Ikke-planlagte jobber** som viser gjeldende antall ikke-planlagte jobber. Alternativt kan du klikke **Planlegg ikke-planlagte jobber** i **Kort** -kategorien i handlingsruten. Dialogboksen viser en liste over de ikke-planlagte kanban-jobbene for arbeidscellen. Du kan bruke **Filter** -feltet til å filtrere etter alle felt i rutenettet. Du kan for eksempel filtrere etter kanban-jobber for et bestemt produkt. Når du har en filtrert liste over jobbene som du vil planlegge, merker du dem i listen, og klikk deretter **OK** . Hvis du vil bruke automatisk planlegging for jobbene, kan du angi alternativet **Automatisk planlegging** som **Ja** . I dette tilfellet planlegges jobbene i en periode i henhold til forfallsdatoen. Du kan også planlegge jobbene etter periode. Velg ganske enkelt en periode i feltet **Periode** . Illustrasjonen nedenfor viser et eksempel på dialogboksen **Planlegg ikke-planlagte jobber** . 

![Dialogboksen Planlegg ikke-planlagte jobber](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Sekvensiere kanban-jobber i den samme perioden
Du kan endre rekkefølgen for én eller flere valgte jobber innenfor en periode. Denne funksjonen kan være nyttig hvis du vil prioritere enkelte jobber i perioden. Det kan også hende at du vil sekvensiere jobber som har samme produktattributter, for å optimalisere jobbutføring. Du kan endre rekkefølgen ved hjelp av en dra og slipp-operasjon, eller ved hjelp av menyelementene **Bakover** og **Fremover** i **Kort** -kategorien i handlingsruten.

## <a name="reassign-kanban-jobs-across-periods"></a>Tilordne kanban-jobber på nytt på tvers av perioder
Jobber kan tilordnes på nytt fra én periode til en annen. Denne funksjonen kan være nyttig hvis en periode er overbelastet og du vil fordele belastningen til perioder som har ledig kapasitet. Du kan tilordne jobber på nytt ved hjelp av en dra og slipp-operasjon, eller ved hjelp av menyelementene **Neste periode** og **Forrige periode** i **Kort** -kategorien i handlingsruten.

## <a name="open-the-kanban-schedule-board"></a>Åpne Kanban-plankortet
Du kan åpne Kanban-plankortet ved hjelp av menyelementet på følgende sider:

-   **Produksjonsområde** -siden
-   **Kanban-jobbplanlegging** -siden
-   Siden **Visualisering av produksjonsflyt**


<a name="additional-resources"></a>Tilleggsressurser
--------

[Kanban-jobbplanlegging for lean manufacturingl](lean-manufacturing-kanban-job-scheduling.md)


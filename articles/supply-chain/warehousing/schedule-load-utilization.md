---
title: Planlegg kapasitetsutnyttelse
description: Dette emnet forklarer hvordan du definerer og planlegger belastningen på et lager.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434199"
---
# <a name="schedule-load-utilization"></a>Planlegg kapasitetsutnyttelse

[!include[banner](../includes/banner.md)]

Du kan planlegge kapasitetsutnyttelse for valgte lokasjonstyper, og du kan også prosjektere gjeldende og fremtidig kapasitetsutnyttelse. Du kan prosjektere belastningen av ett eller flere områder, for belastningsenhetene (sone eller lager), eller for en kombinasjon av sone og lager.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Planlegge og vise belastningen for et lager eller område

Hvis du vil planlegge belastningen for områder, lagre, eller soner, oppretter du et oppsett for plassutnyttelse og knytter den til en hovedplan.

I oppsettet for plassutnyttelse du bruker lokasjonstyper, som **Masseplassering** og **Plukklokasjon**, til å angi hvordan plassbruk skal prosjekteres. Du angir også en lagerbelastningsmodus, for eksempel **Sone**.

Prosjekteringen av fremtidig plassutnyttelse er basert på informasjon som beregnes i den tilknyttede hovedplanen. Hovedplaner forutsier ressursplanleggingen for innkommende og utgående ordrer for produksjon og operasjoner. Prosjekteringen av tilgjengelig plass er basert på forholdet mellom oppsettet for plassutnyttelse og den valgte hovedplanen.

Ved hjelp av lagerbelastningsmodusen du valgte i oppsettet for plassutnyttelse, kan du angi om belastningen skal prosjekteres for hvert lager eller hver sone, eller om prosjekteringene skal inkludere informasjon om både varehus og soner. Du angir også om blokkerte lokasjoner skal ekskluderes fra beregningen av plassutnyttelse.

Du kan prosjektere plassutnyttelsen ved å generere rapporten **Utnyttelse av lagerkapasitet**. Når du genererer denne rapporten, kan du angi om plassutnyttelsen skal prosjekteres for hvert område eller på tvers av områder for den valgte belastningsenheten, for eksempel sone eller lager.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Opprette et oppsett for utnyttelse av lagerplass

1. Velg **Lagerstyring** \> **Oppsett** \> **Lagerovervåking** \> **Plassbruk**.
2. Velg **Ny** for å opprette et oppsett for plassutnyttelse. Angi en ID og et navn for det nye oppsettet.
3. Velg om oversikten over plassutnyttelse skal vise informasjon etter lager, sone eller lager og sone, i feltet **Lagerbelastningsmodus**.
4. Angi alternativet **Utelat blokkerte lokasjoner** til **Ja** for å utelate blokkerte lagerlokasjoner fra beregningen av tilgjengelig plass. Du kan blokkere en lagerlokasjon for innlevering eller utlevering ved å angi en blokkeringsårsak for lokasjonen i feltet **Innlevering blokkert** eller **Utlevering blokkert** på hurtigfanen **Andre** på siden **Lagerlokasjoner**.
5. Velg lokasjonstyper som skal inkluderes i beregningen av plassutnyttelse, på hurtigfanen **Lokasjonstype**. Du må velge minst én lokasjonstype for prosjekteringen.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Knytte et oppsett for plassutnyttelse til en hovedplan

1. Velg **Lagerstyring** \> **Periodiske oppgaver** \> **Planlegg kapasitetsutnyttelse**.
2. Velg en hovedplan i feltet **Hovedplan**.
3. Angi antall dager som skal inkluderes i prosjekteringen av gjeldende og fremtidig arbeidsmengde, i feltet **Antall dager**.
4. Angi oppsettet for plassutnyttelse som skal brukes i prosjekteringen av gjeldende og fremtidig arbeidsmengde, i feltet **Plassbruk**.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Angi prosjekteringen av plassutnyttelse og vise informasjon

1. Velg **Lagerstyring** \> **Forespørsler og rapporter** \> **Rapporter for fysisk beholdning** \> **Utnyttelse av lagerkapasitet**.
2. Velg prosjekteringsnivået for plassutnyttelse i feltet **Vis etter**:

    - **Område** – prosjekter plassutnyttelsen for hvert område. Denne prosjekteringen er nyttig hvis du for eksempel vil vise alle lagrene for et område, slik at du kan balansere plassutnyttelsen mellom lagrene.
    - **Belastningsenhet** – prosjekter plassutnyttelsen for soner eller lagre. Den tilgjengelige plassen prosjekteres deretter i henhold til verdien du valgte i feltet **Lagerbelastningsmodus** på siden **Plassbruk**, da du opprettet plassbrukoppsettet.

3. Flkg ett av disse trinnene, avhengig av verdien du valgte i forrige trinn:

    - Hvis du valgte **Område** i **Vis etter**-feltet, er **Område**-feltet tilgjengelig. Velg ett eller flere områder du vil inkludere i prosjekteringen.
    - Hvis du valgte **Belastningsenhet** i **Vis etter**-feltet, er **Belastningsenhet**-feltet tilgjengelig. Velg belastningsenheten.

4. I feltet **Belastningstype** velger du **Volum** eller **Vekt** for å angi to lagerdriftsenheten du vil prosjektere plass for.
5. Angi oppsettet for plassbruk som prosjekteringen skal baseres på, i feltet **Plassbrukoppsett**.

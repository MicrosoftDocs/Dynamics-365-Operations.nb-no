---
title: Planlegge kapasitet for arbeidsmengde
description: Dette emnet forklarer hvordan du definerer og planlegger arbeidsmengdekapasiteten for ansatte i et lager eller et helt lager.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: 1b1334dcba7d12f2da301f70e21a08fceb88e2b4
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2018

---

# <a name="schedule-workload-capacity"></a>Planlegge kapasitet for arbeidsmengde

[!include[banner](../includes/banner.md)]

Du kan planlegge arbeidsmengdekapasitet for lagre, og du kan også projisere gjeldende og fremtidig arbeidsmengde for arbeiderne på individuelle lagre. Du kan projisere arbeidsmengden for hele lageret, eller du kan projisere arbeidsmengden separat for innkommende og utgående arbeidsmengde.

For å projisere levert arbeidsmengde for valgte lagre må det finnes hovedplanleggingsdata tilgjengelige for disse lagrene. Hvis du vil ha mer informasjon om hovedplaner, kan du se [Hovedplaner](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Planlegg og vis arbeidsmengder for et lager

For å planlegge arbeidsmengdekapasitet for et lager oppretter du et arbeidsmengdeoppsett for et eller flere lagre, og tilknytter deretter arbeidsmengdeoppsett med en hovedplan. I arbeidsmengdeoppsettet kan du definere grenser for vekt eller volum for innkommende og utgående transaksjoner. Du kan også opprette mer enn ett oppsett for hver lager og deretter knytte oppsettet til individuelle hovedplaner. Du kan for eksempel bruke denne fremgangsmåten for å være i tråd med sesongendringer i arbeidsstyrken.

Hvis arbeiderne på et lager jobber med transaksjoner for både innkommende og utgående arbeidsmengder, kan du konfigurere lagerkapasitetsoppsettet, slik at arbeidsmengden prosjekteres i en kombinert visning.

For å planlegge og vise arbeidsmengder for lagre, må du utføre følgende oppgaver:

1. Opprett et arbeidsmengdekapasitetsoppsett og definer begrensninger for arbeidsmengdekapasitet for ett eller flere lagre.
2. Knytt arbeidsmengdekapasitetsoppsettet til en hovedplan for å opprette arbeidsmengdeprojeksjoner og spesifisere hvor lenge disse projeksjonene gjelder.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Opprett et arbeidsmengdekapasitetsoppsett for et lager

1. Velg **Lagerstyring** \> **Oppsett** \> **Lagerovervåking** \> **Arbeidsmengdekapasitet**.
2. I handlingsruten velger du **Ny** for å opprette et oppsett for arbeidsmengdekapasitet.
3. På hurtigfanen **Lagre** velger du **Ny**, og angi deretter verdiene på linjen for å knytte et lager til arbeidsmengdekapasitetsoppsettet.
4. Merk av for **Kombinert innkommende og utgående arbeidsmengde** hvis rapporten **Arbeidsmengdekapasitet** skal vise den totale arbeidsmengden for innkommende og utgående transaksjoner i én visning.
5. På hurtigfanen **Transaksjonstyper** velger du de innkommende og utgående transaksjonstypene som arbeidsmengdebegrensningene gjelder.

    > [!NOTE]
    > Du må velge minst én transaksjonstype for både den innkommende og den utgående arbeidsmengden.

#### <a name="define-limits-for-volume-or-weight"></a>Definere grenser for volum eller vekt

Du kan definere grenser for volum eller vekt avhengig av begrensningene som gjelder for lagerets arbeidsstyrke. Grensene du spesifiserer, inkluderes i projeksjonen av arbeidsmengdekapasitet som du kan se i rapporten **Arbeidsmengdekapasitet**.

For å prosjektere informasjon om volum og vekt for varer må standardvolumet til én lagervare og vekten av én lagervare spesifiseres for alle produkter. Feltene som kreves er tilgjengelige i følgende feltgrupper på hurtigfanen **Administrer lager** på siden **Detaljer om frigitt produkt**:

- Behandling
- Fysiske dimensjoner
- Vektmålinger

Hvis denne informasjonen ikke blir korrekt spesifisert, vil du motta en melding når du genererer rapporten **Arbeidsmengdekapasitet**. Fra rapporten kan du vise flere detaljer for å identifisere den manglende informasjonen som kreves, for å prosjektere fremtidig arbeidsmengde.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Knytt et arbeidsmengdekapasitetsoppsett til en hovedplan

1. Velg **Lagerstyring** \> **Periodiske oppgaver** \> **Planlegg arbeidsmengde**.
2. I **Hovedplan**-feltet velger du hovedplanen som skal brukes for arbeidsmengdeprojeksjoner.
3. Spesifiser antall dager arbeidsmengdeprojeksjonen dekker i feltet **Antall dager**.
4. Velg arbeidsmengdeoppsettet du vil knytte til hovedplanen, i **Arbeidsmengde**-feltet.

### <a name="view-workload-capacity"></a>Vis arbeidsmengdekapasitet

1. Velg **Lagerstyring** \> **Forespørsler og rapporter** \> **Rapporter for fysisk beholdning** \> **Arbeidsmengdekapasitet**.
2. Spesifiser antall kolonner som skal vises på rapporten, i feltet **Antall kolonner**.
3. I feltet **Ordretype** velger du **Planlagt og bekreftet**, **Planlagt** eller **Bekreftet** for å angi hvilke typer ordrer som skal prosjekteres i rapporten.
4. Velg en belastningstype i **Belastningstype**-feltet for å angi om arbeidsmengdekapasiteten skal prosjekteres for volum eller vekt.
5. I feltet **Arbeidsmengdekapasitet** velger du et arbeidsmengdekapasitetsoppsett.


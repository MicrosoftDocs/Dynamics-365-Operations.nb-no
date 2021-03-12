---
title: Klargjøre en juridisk enhet for konsolideringsprosessen
description: Under en konsolidering samler du transaksjoner fra flere sett med kontoer for juridisk enhet i ett sett med kontoer for juridisk enhet. Dette emnet beskriver hvordan du klargjør en juridisk enhet for konsolidering.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990314"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Klargjøre en juridisk enhet for konsolideringsprosessen

[!include [banner](../includes/banner.md)]

Under en konsolidering samler du transaksjoner fra flere sett med kontoer for juridisk enhet i ett sett med kontoer for juridisk enhet. Dette emnet beskriver hvordan du klargjør en juridisk enhet for konsolidering.

> [!NOTE]
> Vi anbefaler at du bruker Management Reporter for Microsoft Dynamics 365 Finance til å kombinere de økonomiske resultatene for flere juridiske enheter i et konsolidert format. Management Reporter lar deg opprette konsoliderte finansrapporter på tvers av juridiske enheter, bruke Excel til å importere konsolideringsdata fra andre kilder og omsette beløp til et hvilket som helst antall rapporteringsvalutaer uten å måtte kjøre konsolideringsprosessen i Dynamics 365 Finance.

Du kan skrive ut rapporter, for eksempel regnskapsoppgjør, fra den konsoliderte juridiske enheten. Du kan imidlertid ikke bruke den konsoliderte juridiske enheten for daglige transaksjoner.

Du kan konsolidere data fra juridiske enheter som bruker andre databaser enn den konsoliderte juridiske enheten. Denne konsolideringsprosessen kalles en *importkonsolidering*. Alternativt kan juridiske enheter bruke den samme databasen som den konsoliderte juridiske enheten. Denne konsolideringsprosessen kalles en *online konsolidering*.

Den konsoliderte juridiske enheten samler resultatene og saldoene for datterselskapene. Hvis du vil klargjøre en konsolidert juridisk enhet for en konsolidering, følger du trinnene nedenfor.

1. Gå til **Økonomimodul \> Oppsett \> Organisasjon \> Juridiske enheter**.
2. Velg **Ny** for å opprette den nye juridiske enheten som skal være den konsoliderte juridiske enheten.
3. Merk av for **Bruk for finanskonsolideringsprosess**, og angi deretter informasjon om den konsoliderte juridiske enheten. Sørg for å angi denne informasjon nøyaktig slik du vil at den skal vises på regnskapsoppgjør for den konsoliderte juridiske enheten.
4. Lukk siden.
5. Velg den konsoliderte juridiske enheten i feltet i øvre høyre hjørne på siden, og velg deretter **OK**.
6. Gå til **Økonomimodul \> Oppsett \> Finans**.
7. Velg kontoplanen, den økonomiske kalenderen, regnskapsvalutaen, en valgfri rapporteringsvalutaen og standard valutakurstype for den konsoliderte juridiske enheten. 
8. Gå til **Økonomimodul \> Oppsett \> Valuta \> Valutakurser**.
9. Definer valutakurser i relevante perioder for valutaene for de juridiske enhetene for datterselskap.
10. Lukk siden.
11. Hvis den konsoliderte juridiske enheten har datterselskaper med utenlandske valutaer, følger du disse trinnene:

    1. Gå til **Økonomimodul \> Oppsett \> Postering \> Kontoer for automatiske transaksjoner**.
    2. I feltet **Posteringstype** velger du en passende konto:

        - Hvis den juridiske enheten har utenlandske datterselskaper som er økonomisk eller driftsmessig avhengige av den overordnede juridiske enheten, velger du en passende konto for posteringstypen **Resultatkonto for konsolideringsdifferanser**.
        - Hvis du konsoliderer et datterselskap som er økonomisk og driftsmessig uavhengig av den overordnede juridiske enheten, eller en juridisk enhet som inneholder resultatene av flere datterselskaper som er økonomisk og driftsmessig uavhengige av den overordnede juridiske enheten, og hvis du bruker oversettingsmetoder til å konsolidere dataene, velger du en aktuell konto for posteringstypen **Balansekonto for konsolideringsdifferanser**.

    3. I **Hovedkonto**-feltet velger du hovedkontoene som skal brukes til justeringer av revaluering av utenlandsk valuta.
    4. Lukk siden.

    Hvis du oppretter den konsoliderte juridiske enheten tidlig i en periode, kan du revaluere beløpene i utenlandsk valuta etter hvert som valutakurser endres i konsolideringsperioden.

Den konsoliderte juridiske enheten er nå definert for den periodiske jobben **Konsolider**. Du kan enten gjøre en importkonsolidering eller en online konsolidering.

- Hvis du vil gjøre en importkonsolidering, kan du gå til **Økonomimodul \> Periodisk \> Konsolider \> Konsolider \[Importer fra\]**.
- Hvis du vil gjøre en online konsolidering, kan du gå til **Økonomimodul \> Periodisk \> Konsolider \> Konsolider \[Online\]**.

> [!NOTE]
> Før du kan behandle konsolideringen, må du klargjøre de juridiske enhetene for datterselskap for konsolidering. Hvis du vil ha mer informasjon, kan du se [Definere en juridisk enhet for datterselskap for konsolidering](set-up-subsidiary-company-for-consolidation.md).

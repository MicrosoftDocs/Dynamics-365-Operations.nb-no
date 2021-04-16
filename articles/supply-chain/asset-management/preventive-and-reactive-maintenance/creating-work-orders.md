---
title: Opprette arbeidsordrer
description: Dette emnet forklarer hvordan du oppretter arbeidsordrer i Aktivastyring.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836740"
---
# <a name="creating-work-orders"></a>Opprette arbeidsordrer

[!include [banner](../../includes/banner.md)]

Etter at du har planlagt forebyggende vedlikeholdsjobber, er neste trinn å opprette arbeidsordrer for dem. Du kan fullføre dette trinnet ved å bruke en av vedlikeholdsplanene. De planlagte jobbene i en vedlikeholdsplan kan ha forskjellige referansetyper, som beskrevet i tabellen nedenfor.

| Referansetype | beskrivelse |
|---|---|
| Vedlikeholdsplaner | Forebyggende vedlikeholdsjobber som er basert på vedlikeholdsplantypen *Tid* eller *Teller*. |
| Vedlikeholdsrunder | Forebyggende vedlikeholdsjobber som inneholder flere aktiva som krever en lignende type vedlikehold. |
| Melding | En manuelt opprettet forespørsel om vedlikehold eller reparasjon av et aktivum. Denne forespørselen kan konverteres til en arbeidsordre. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Opprette arbeidsordrer basert på vedlikeholdsplanen

Følg denne fremgangsmåten for å opprette arbeidsordrer som er basert på vedlikeholdsplanen.

1. Åpne en av følgende sider, avhengig av hvordan du vil planlegge varer for arbeidsordrene:

    - Alle vedlikeholdsplaner (**Aktivastyring \> Styringsplan \> Alle vedlikeholdsplaner**)
    - Åpne vedlikeholdsplanlinjer (**Aktivastyring \> Styringsplan \> Åpne vedlikeholdsplanlinjer**)
    - Åpne vedlikeholdsplanpuljer (**Aktivastyring \> Styringsplan \> Åpne vedlikeholdsplanpuljer**)

1. Merk av for hver planlagte vedlikeholdsjobb du vil opprette en arbeidsordre for, i rutenettet. Velg deretter **Arbeidsordre** i handlingsruten.

    Dialogboksen **Opprett arbeidsordrer** vises. Det totale antallet prognosetimer for de valgte linjene vises i feltet **Vedlikeholdsprognosetimer**.

    ![Dialogboksen Opprett arbeidsordrer](media/18-preventive-maintenance.png)

1. I **Parametere**-delen angir du antall arbeidsordrer som skal opprettes. Velg ett av følgende alternativer:

    - **Én arbeidsordre per linje** – Opprett én arbeidsordre per vedlikeholdsplanlinje.
    - **Én arbeidsordre per** – Opprett arbeidsordrer som grupperes i henhold til innstillingene for de andre alternativene som blir tilgjengelige når du velger dette alternativet.

1. I feltet **Arbeidsordretype** velger du arbeidsordretypen som skal brukes for alle arbeidsordrene du oppretter.
1. Velg **OK** for å opprette arbeidsordrene i henhold til innstillingene.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Gruppere arbeidsordrelinjer som opprettes automatisk mens en vedlikeholdsplan kjører

Med denne funksjonen kan du definere regler for gruppering av arbeidsordrelinjer under én arbeidsordre når systemet er konfigurert slik at det genererer arbeidsordrer automatisk, basert på en vedlikeholdsplan. Tidligere kunne automatisk genererte arbeidsordrer bare inneholde én linje. Nå kan du imidlertid gruppere arbeidsordrer etter for eksempel aktiva, aktivatype eller funksjonslokasjon. (Manuelt genererte arbeidsordrer kan allerede grupperes på denne måten, som beskrevet i den forrige delen i dette emnet.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Aktivere gruppering for automatisk genererte arbeidsordrer

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Aktivastyring*
- **Funksjonsnavn:** *Bruk regler for gruppering av arbeidsordrer mens en vedlikeholdsplan kjører*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Konfigurere gruppering for automatisk genererte arbeidsordrer

Følg denne fremgangsmåten for å konfigurere gruppering for automatisk genererte arbeidsordrer.

1. Gå til **Aktivastyring \> Oppsett \> Forebyggende vedlikehold \> Vedlikeholdsplaner**.
1. Følg denne fremgangsmåten for hver plan der du vil generere grupperte arbeidsordrer:

    1. Velg planen i listeruten.
    1. Kontroller at det er merket av for **Opprett automatisk** på hver linje i hurtigfanen **Linje**.

1. Gå til **Aktivastyring \> Periodisk \> Forebyggende vedlikehold \> Planlegg vedlikeholdsplaner**.
1. Angi tidshorisonten for planen (hvor langt fremover du skal se når du finner planlagte vedlikeholdsjobber du skal generere arbeid for) i **Periode**-delen i dialogboksen **Planlegg vedlikeholdsplaner**.
1. Angi *Ja* for alternativet **Opprett arbeidsordre fra plan automatisk**.
1. Velg ett av følgende alternativer i delen **Arbeidsordre**:

    - **Én arbeidsordre per linje** – Opprett én arbeidsordre per vedlikeholdsplanlinje. (Dette alternativet gir samme funksjonalitet som er tilgjengelig når funksjonen *Bruk regler for gruppering av arbeidsordrer mens en vedlikeholdsplan kjører* er deaktivert.)
    - **Én arbeidsordre per** – Opprett arbeidsordrer som grupperes i henhold til innstillingene for de andre alternativene som blir tilgjengelige når du velger dette alternativet.

1. Hvis du vil at alternativene skal brukes når du bare kjører noen av vedlikeholdsplanene, legger du til filtre etter behov i hurtigfanen **Poster som skal inkluderes**, slik du kan gjøre for andre satsvise jobber i Microsoft Dynamics 365 Supply Chain Management.
1. Konfigurer alternativer for satsvise jobber og planlegging etter behov i hurtigfanen **Kjør i bakgrunnen**, slik du kan gjøre for andre satsvise jobber i Supply Chain Management.
1. Velg **OK** for å kjøre og/eller planlegge de valgte vedlikeholdsplanene.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
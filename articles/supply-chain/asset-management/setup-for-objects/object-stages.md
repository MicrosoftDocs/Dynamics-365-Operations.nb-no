---
title: Livsløpstilstander for aktiva
description: Dette emnet forklarer livsløpstilstander for aktiva og livsløpsmodeller i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e542a0bc7335d16139ef6e34b6794161ab4be195
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571191"
---
# <a name="asset-lifecycle-states"></a>Livsløpstilstander for aktiva

[!include [banner](../../includes/banner.md)]

 

Dette emnet forklarer livsløpstilstander for aktiva og livsløpsmodeller i Aktivastyring. Livsløpstilstander for aktiva brukes til å definere om aktivaet er aktivt eller inaktivt. Du kan for eksempel definere livsløpstilstander for aktiva, blant annet **Opprettet**, **Aktiv** og **Avsluttet**.

> [!NOTE]
> - Livsløpstilstander for forespørsel er knyttet til livsløpstilstander for aktiva. Når en forespørsel endres til en ny livsløpstilstand for forespørsel, endres derfor aktivumet som er knyttet til forespørselen, til en ny livsløpstilstand for aktiva. Hvis for eksempel livsløpstilstanden for en forespørsel endres til **Inngående**, endres livsløpstilstanden til det tilknyttede anleggsmidlet til livsløpstilstanden som er valgt i feltet **Innkommende livsløpstilstand** på hurtigfanen **Livsløpstilstand for aktiva** på siden **Livsløpstilstand for aktivamodeller**. 


Livsløpstilstander for aktiva kan defineres i livsløpsmodeller for aktiva, der du kan definere de nødvendige livsløpstilstandene for ulike typer aktiva. Du setter først opp livsløpstilstander. Deretter oppretter du en livsløpsmodell og velger livsløpstilstander for den.

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Livsløpstilstander**.
2. Velg **Ny** for å opprette en ny livsløpstilstand.
3. I feltet **Livsløpstilstand** angir du ID-en for livsløpstilstanden.
4. Angi en beskrivelse i **Navn**-feltet.

    Feltet **Livsløpsmodeller** viser antall livsløpsmodeller for aktiva som bruker livsløpstilstanden for aktiva.

5. Angi **Aktiv** til **Ja** hvis denne livsløpstilstanden skal være en aktiv livsløpstilstand (med andre ord om arbeidsordrer kan opprettes for aktiva som er i denne livsløpstilstanden).
6. Sett alternativet **Slett åpne kalenderlinjer** til **Ja** hvis åpne aktivakalenderlinjer som har livsløpstilstanden **Opprettet**, skal slettes når de er i denne livsløpstilstanden. Denne innstillingen er nyttig hvis du vil rydde opp i eventuelle åpne vedlikeholdsplaner som ikke lenger er relevante for aktivaet (for eksempel hvis aktivaet ikke lenger er aktiv).

> [!NOTE]
> Livsløpstilstander for aktiva, livsløpsmodeller for aktiva og aktivatyper er relatert. De brukes på samme måte som livsløpstilstander for arbeidsordrer, livsløpsmodeller for arbeidsordrer og arbeidsordretyper. 


Når du har opprettet de nødvendige livsløpstilstandene for aktiva, kan du definere livsløpstilstander i livsløpsmodeller for aktiva.

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Livsløpsmodeller**.
2. Velg **Ny** for å opprette en ny livsløpsmodell.
3. I feltet **Livsløpsmodell** angir du ID-en for livsløpsmodellen.
4. Angi en beskrivelse i **Navn**-feltet.

    Feltet **Livsløpstilstander** viser antall livsløpstilstander for aktiva som er valgt i livsløpsmodellen for aktiva. Feltet **Aktivatyper** viser antall aktivatyper som bruker livsløpsmodellen.

5. I hurtigfanen **Livsløpstilstander** velger du livsløpstilstandene for aktiva som skal inkluderes i livsløpsmodellen for aktiva:

    - Hvis du vil bruke en livsløpstilstand for modellen, velger du den i delen **Gjenværende livsløpstilstander**, og deretter velger du pil høyre ![Pil høyre](media/15-setup-for-objects.png) for å flytte den til delen **Valgte livsløpstilstander**.
    - Hvis du vil bruke alle tilgjengelige livsløpstilstander for modellen, velger du **Alle tilgjengelige livsløpstilstander**-knappen ![Alle tilgjengelige livsløpstilstander](media/20-setup-for-objects.png). Alle livsløpstilstander overføres til delen **Valgte livsløpstilstander**.
    - Hvis du vil fjerne en livsløpstilstand fra modellen, velger du den i delen **Valgte livsløpstilstander**, og deretter velger du pil venstre ![Pil venstre](media/16-setup-for-objects.png) for å flytte den til delen **Gjenværende livsløpstilstander**.

6. Velg **Oppdateringer av livsløpstilstander** for å definere livsløpstilstander for aktiva som kan følge en valgt livsløpstilstand.
7. Du bruker hurtigfanen **Aktiva** hvis du håndterer aktiva du mottar for reparasjon. I delen **Innkommende/utgående** kan du velge livsløpstilstander for aktiva for å angi arbeidsflyten for et aktivum du mottar for reparasjon. Hvis du tilbyr lån av aktiva til kunder eller avdelinger i **Lån**-delen, kan du velge livsløpstilstander for lånte aktiva.

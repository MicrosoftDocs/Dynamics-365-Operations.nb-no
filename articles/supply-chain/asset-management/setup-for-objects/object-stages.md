---
title: Livssyklustilstander for aktiva
description: Dette emnet forklarer livssyklustilstander for aktiva og livssyklusmodeller i Aktivastyring.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db025b3edb9daa2ffc19b5fc92930f76d8007dce
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360107"
---
# <a name="asset-lifecycle-states"></a>Livssyklustilstander for aktiva

[!include [banner](../../includes/banner.md)]

 

Dette emnet forklarer livssyklustilstander for aktiva og livssyklusmodeller i Aktivastyring. Livssyklustilstander for aktiva brukes til å definere om aktivumet er aktivt eller inaktivt. Du kan for eksempel definere livssyklustilstander for aktiva, blant annet **Opprettet**, **Aktiv** og **Avsluttet**.

> [!NOTE]
> - Livssyklustilstander for forespørsel er knyttet til livssyklustilstander for aktiva. Når en forespørsel endres til en ny livssyklustilstand for forespørsel, endres derfor aktivumet som er knyttet til forespørselen, til en ny livssyklustilstand for aktiva. Hvis for eksempel livssyklustilstanden for en forespørsel endres til **Inngående**, endres livssyklustilstanden til det tilknyttede anleggsmidlet til livssyklustilstanden som er valgt i feltet **Innkommende livssyklustilstand** på hurtigfanen **Livssyklustilstand for aktiva** på siden **Livssyklustilstand for aktivamodeller**. 


Livssyklustilstander for aktiva kan defineres i livssyklusmodeller for aktiva, der du kan definere de nødvendige livssyklustilstandene for ulike typer aktiva. Du setter først opp livssyklustilstander. Deretter oppretter du en livssyklusmodell og velger livssyklustilstander for den.

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Livssyklustilstander**.
2. Velg **Ny** for å opprette en ny livssyklustilstand.
3. I feltet **Livssyklustilstand** angir du ID-en for livssyklustilstanden.
4. Angi en beskrivelse i **Navn**-feltet.

    Feltet **Livssyklusmodeller** viser antall livssyklusmodeller for aktiva som bruker livssyklustilstanden for aktiva.

5. Angi **Aktiv** til **Ja** hvis denne livssyklustilstanden skal være en aktiv livssyklustilstand (med andre ord om arbeidsordrer kan opprettes for aktiva som er i denne livssyklustilstanden).
6. Sett alternativet **Slett åpne kalenderlinjer** til **Ja** hvis åpne aktivakalenderlinjer som har livssyklustilstanden **Opprettet**, skal slettes når de er i denne livssyklustilstanden. Denne innstillingen er nyttig hvis du vil rydde opp i eventuelle åpne vedlikeholdsplaner som ikke lenger er relevante for aktivumet (for eksempel hvis aktivumet ikke lenger er aktiv).

> [!NOTE]
> Livssyklustilstander for aktiva, livssyklusmodeller for aktiva og aktivatyper er relatert. De brukes på samme måte som livssyklustilstander for arbeidsordrer, livssyklusmodeller for arbeidsordrer og arbeidsordretyper. 


Når du har opprettet de nødvendige livssyklustilstandene for aktiva, kan du definere livssyklustilstander i livssyklusmodeller for aktiva.

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Livssyklusmodeller**.
2. Velg **Ny** for å opprette en ny livssyklusmodell.
3. I feltet **Livssyklusmodell** angir du ID-en for livssyklusmodellen.
4. Angi en beskrivelse i **Navn**-feltet.

    Feltet **Livssyklustilstander** viser antall livssyklustilstander for aktiva som er valgt i livssyklusmodellen for aktiva. Feltet **Aktivatyper** viser antall aktivatyper som bruker livssyklusmodellen.

5. I hurtigfanen **Livssyklustilstander** velger du livssyklustilstandene for aktiva som skal inkluderes i livssyklusmodellen for aktiva:

    - Hvis du vil bruke en livssyklustilstand for modellen, velger du den i delen **Gjenværende livssyklustilstander**, og deretter velger du pil høyre ![Pil høyre.](media/15-setup-for-objects.png) for å flytte den til delen **Valgte livssyklustilstander**.
    - Hvis du vil bruke alle tilgjengelige livssyklustilstander for modellen, velger du **Alle tilgjengelige livssyklustilstander**-knappen ![Alle tilgjengelige livssyklustilstander.](media/20-setup-for-objects.png). Alle livssyklustilstander overføres til delen **Valgte livssyklustilstander**.
    - Hvis du vil fjerne en livssyklustilstand fra modellen, velger du den i delen **Valgte livssyklustilstander**, og deretter velger du pil venstre ![Pil venstre.](media/16-setup-for-objects.png) for å flytte den til delen **Gjenværende livssyklustilstander**.

6. Velg **Oppdateringer av livssyklustilstander** for å definere livssyklustilstander for aktiva som kan følge en valgt livssyklustilstand.
7. Du bruker hurtigfanen **Aktiva** hvis du håndterer aktiva du mottar for reparasjon. I delen **Innkommende/utgående** kan du velge livssyklustilstander for aktiva for å angi arbeidsflyten for et aktivum du mottar for reparasjon. Hvis du tilbyr lån av aktiva til kunder eller avdelinger i **Lån**-delen, kan du velge livssyklustilstander for lånte aktiva.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
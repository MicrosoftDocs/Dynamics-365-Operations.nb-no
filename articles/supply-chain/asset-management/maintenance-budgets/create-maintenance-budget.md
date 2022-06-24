---
title: Opprette vedlikeholdsbudsjetter
description: Denne artikkelen forklarer hvordan du oppretter et vedlikeholdsbudsjett i Aktivastyring.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1fa5e4c76621634930206c1d89fd8e8f4f541fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858047"
---
# <a name="create-maintenance-budgets"></a>Opprette vedlikeholdsbudsjetter

[!include [banner](../../includes/banner.md)]

 



Vedlikeholdsbudsjetter brukes til å gi en oversikt over forventede kostnader for forebyggende vedlikehold. Budsjettlinjer beregnes på grunnlag av vedlikeholdsplanlinjer som har en forventet startdato i løpet av budsjettperioden.

Vedlikeholdsbudsjetter er basert på kosttypene som brukes i Aktivastyring: **Forebyggende**, **Korrigerende** og **Investering.** Budsjettkostnader for investeringsvedlikehold er inkludert for aktive anleggsmidler som har en erstatningsdato i løpet av budsjettperioden og en relatert erstatningsverdi. Budsjettkostnader for korrigerende vedlikehold inkluderes hvis en tidligere korrigeringsdato er inkludert i budsjettberegningen. I dette tilfellet beregnes korrigerende kostnader fra en tidligere periode for den samme fremtidige perioden som du beregner vedlikeholdsbudsjettet for.

## <a name="create-a-maintenance-budget"></a>Opprette et vedlikeholdsbudsjett

1. Velg **Aktivastyring** \> **Forespørsler** \> **Vedlikeholdsbudsjett** \> **Budsjett**.
2. Velg **Opprett budsjett**.
3. Angi en budsjett-ID i feltet **Vedlikeholdsbudsjett**.
4. Angi en beskrivelse i **Beskrivelse**-feltet.
4. Angi start- og sluttdatoene for budsjettperioden i **Periode**-hurtigfanen i feltene **Fra dato** og **Til dato**.
5. Hvis du vil inkludere korrigerende budsjettkostnader som beregnes på grunnlag av faktiske kostnader fra en tidligere periode, angir du startdatoen for perioden som disse kostnadene skal tas med fra, i feltet **Korrigerende fra-dato**.
6. Avhengig av detaljnivået som kreves i budsjettet, angir du relevante alternativer i de fem **Grupper etter**-hurtigfanene.
7. Velg **OK**.
8. Velg **Budsjettlinjer** for å åpne siden **Vedlikeholdsbudsjettlinjer**, der du kan vise alle budsjettlinjene som er opprettet for perioden.
9. Hvis du vil godkjenne budsjettet, velger du det på siden **Vedlikeholdsbudsjetter** og velger deretter **Godkjenn**. Deretter velger **OK** i dialogboksen **Godkjenn budsjett**. Navnet angis i **Godkjent av**-feltet på siden **Vedlikeholdsbudsjetter**.

    > [!NOTE]
    > Når du har godkjent et vedlikeholdsbudsjett, kan du ikke beregne på nytt eller justere de relaterte linjene på siden **Vedlikeholdsbudsjettlinjer** hvis du ikke først fjerner godkjenningen. Hvis du vil fjerne godkjenningen av et vedlikeholdsbudsjett, velger du det på siden **Vedlikeholdsbudsjetter** og velger deretter **Godkjenn**. Deretter velger **OK** i dialogboksen **Godkjenn budsjett**.

![Vedlikeholdsbudsjetter.](media/01-maintenance-budgets.png)

Du kan også opprette et nytt vedlikeholdsbudsjett ved å kopiere et eksisterende budsjett. På siden **Vedlikeholdsbudsjetter** velger du budsjettet du vil kopiere, og deretter velger du **Kopier**. Denne fremgangsmåten er nyttig hvis du for eksempel har opprettet et budsjett for én måned og vil kopiere det til andre måneder.

> [!NOTE]
> Vedlikeholdsbudsjettet beregner bare budsjettkostnader på grunnlag av vedlikeholdsplanlinjer. Hvis du vil beregne faktiske kostnader for samme periode, kan du utføre denne beregningen på siden **Kostnadskontroll for aktivum**. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
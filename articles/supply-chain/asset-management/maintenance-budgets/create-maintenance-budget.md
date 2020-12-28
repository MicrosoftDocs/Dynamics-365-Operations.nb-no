---
title: Opprette vedlikeholdsbudsjetter
description: Dette emnet forklarer hvordan du oppretter et vedlikeholdsbudsjett i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2aaba8794bf0025f0449509752e4f197d3bf3db4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434473"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="18c5c-103">Opprette vedlikeholdsbudsjetter</span><span class="sxs-lookup"><span data-stu-id="18c5c-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="18c5c-104">Vedlikeholdsbudsjetter brukes til å gi en oversikt over forventede kostnader for forebyggende vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="18c5c-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="18c5c-105">Budsjettlinjer beregnes på grunnlag av vedlikeholdsplanlinjer som har en forventet startdato i løpet av budsjettperioden.</span><span class="sxs-lookup"><span data-stu-id="18c5c-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="18c5c-106">Vedlikeholdsbudsjetter er basert på kosttypene som brukes i Aktivastyring: **Forebyggende**, **Korrigerende** og **Investering.**</span><span class="sxs-lookup"><span data-stu-id="18c5c-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="18c5c-107">Budsjettkostnader for investeringsvedlikehold er inkludert for aktive anleggsmidler som har en erstatningsdato i løpet av budsjettperioden og en relatert erstatningsverdi.</span><span class="sxs-lookup"><span data-stu-id="18c5c-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="18c5c-108">Budsjettkostnader for korrigerende vedlikehold inkluderes hvis en tidligere korrigeringsdato er inkludert i budsjettberegningen.</span><span class="sxs-lookup"><span data-stu-id="18c5c-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="18c5c-109">I dette tilfellet beregnes korrigerende kostnader fra en tidligere periode for den samme fremtidige perioden som du beregner vedlikeholdsbudsjettet for.</span><span class="sxs-lookup"><span data-stu-id="18c5c-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="18c5c-110">Opprette et vedlikeholdsbudsjett</span><span class="sxs-lookup"><span data-stu-id="18c5c-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="18c5c-111">Velg **Aktivastyring** \> **Forespørsler** \> **Vedlikeholdsbudsjett** \> **Budsjett**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="18c5c-112">Velg **Opprett budsjett**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="18c5c-113">Angi en budsjett-ID i feltet **Vedlikeholdsbudsjett**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="18c5c-114">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="18c5c-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="18c5c-115">Angi start- og sluttdatoene for budsjettperioden i **Periode**-hurtigfanen i feltene **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="18c5c-116">Hvis du vil inkludere korrigerende budsjettkostnader som beregnes på grunnlag av faktiske kostnader fra en tidligere periode, angir du startdatoen for perioden som disse kostnadene skal tas med fra, i feltet **Korrigerende fra-dato**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="18c5c-117">Avhengig av detaljnivået som kreves i budsjettet, angir du relevante alternativer i de fem **Grupper etter**-hurtigfanene.</span><span class="sxs-lookup"><span data-stu-id="18c5c-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="18c5c-118">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-118">Select **OK**.</span></span>
8. <span data-ttu-id="18c5c-119">Velg **Budsjettlinjer** for å åpne siden **Vedlikeholdsbudsjettlinjer**, der du kan vise alle budsjettlinjene som er opprettet for perioden.</span><span class="sxs-lookup"><span data-stu-id="18c5c-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="18c5c-120">Hvis du vil godkjenne budsjettet, velger du det på siden **Vedlikeholdsbudsjetter** og velger deretter **Godkjenn**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="18c5c-121">Deretter velger **OK** i dialogboksen **Godkjenn budsjett**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="18c5c-122">Navnet angis i **Godkjent av**-feltet på siden **Vedlikeholdsbudsjetter**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="18c5c-123">Når du har godkjent et vedlikeholdsbudsjett, kan du ikke beregne på nytt eller justere de relaterte linjene på siden **Vedlikeholdsbudsjettlinjer** hvis du ikke først fjerner godkjenningen.</span><span class="sxs-lookup"><span data-stu-id="18c5c-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="18c5c-124">Hvis du vil fjerne godkjenningen av et vedlikeholdsbudsjett, velger du det på siden **Vedlikeholdsbudsjetter** og velger deretter **Godkjenn**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="18c5c-125">Deretter velger **OK** i dialogboksen **Godkjenn budsjett**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Vedlikeholdsbudsjetter](media/01-maintenance-budgets.png)

<span data-ttu-id="18c5c-127">Du kan også opprette et nytt vedlikeholdsbudsjett ved å kopiere et eksisterende budsjett.</span><span class="sxs-lookup"><span data-stu-id="18c5c-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="18c5c-128">På siden **Vedlikeholdsbudsjetter** velger du budsjettet du vil kopiere, og deretter velger du **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="18c5c-129">Denne fremgangsmåten er nyttig hvis du for eksempel har opprettet et budsjett for én måned og vil kopiere det til andre måneder.</span><span class="sxs-lookup"><span data-stu-id="18c5c-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="18c5c-130">Vedlikeholdsbudsjettet beregner bare budsjettkostnader på grunnlag av vedlikeholdsplanlinjer.</span><span class="sxs-lookup"><span data-stu-id="18c5c-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="18c5c-131">Hvis du vil beregne faktiske kostnader for samme periode, kan du utføre denne beregningen på siden **Kostnadskontroll for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="18c5c-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 

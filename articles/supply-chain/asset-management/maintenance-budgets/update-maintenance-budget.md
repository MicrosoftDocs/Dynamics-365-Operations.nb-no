---
title: Oppdatere vedlikeholdsbudsjetter
description: Dette emnet forklarer hvordan du oppdaterer et vedlikeholdsbudsjett i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 21aba6224bba98eb9bbb423847e123616003b5d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253476"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="88c8e-103">Oppdatere vedlikeholdsbudsjetter</span><span class="sxs-lookup"><span data-stu-id="88c8e-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="88c8e-104">Siden **Vedlikeholdsbudsjettlinjer** viser alle budsjettlinjene som er opprettet for budsjettet som er valgt på siden **Vedlikeholdsbudsjetter**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="88c8e-105">(Hvis du vil ha mer informasjon, se [Opprette vedlikeholdsbudsjetter](create-maintenance-budget.md).) Du kan beregne på nytt og justere linjer for vedlikeholdsbudsjett til vedlikeholdsbudsjettet er godkjent.</span><span class="sxs-lookup"><span data-stu-id="88c8e-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="88c8e-106">Når budsjettperioden er passert, og kostnadene er postert i Aktivastyring, kan du også oppdatere budsjettlinjene med faktiske kostnader.</span><span class="sxs-lookup"><span data-stu-id="88c8e-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="88c8e-107">Beregne et vedlikeholdsbudsjett på nytt</span><span class="sxs-lookup"><span data-stu-id="88c8e-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="88c8e-108">Du kan beregne et vedlikeholdsbudsjett på nytt på siden **Vedlikeholdsbudsjettlinjer**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="88c8e-109">Når du beregner et vedlikeholdsbudsjett på nytt, slettes de eksisterende budsjettlinjene, og det gjøres en ny beregning.</span><span class="sxs-lookup"><span data-stu-id="88c8e-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="88c8e-110">Velg **Beregn på nytt** på siden **Vedlikeholdsbudsjettlinjer**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="88c8e-111">I dialogboksen **Beregn budsjett på nytt** utfører du de nødvendige endringene for den nye beregningen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="88c8e-112">Nye budsjettlinjer opprettes i henhold til verdiene du angir.</span><span class="sxs-lookup"><span data-stu-id="88c8e-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="88c8e-113">Justere budsjettlinjer</span><span class="sxs-lookup"><span data-stu-id="88c8e-113">Adjust budget lines</span></span>

<span data-ttu-id="88c8e-114">I stedet for å beregne hele vedlikeholdsbudsjettet på nytt, kan du justere valgte linjer som er knyttet til budsjettkostnader.</span><span class="sxs-lookup"><span data-stu-id="88c8e-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="88c8e-115">På siden **Vedlikeholdsbudsjettlinjer** velger du linjene du vil oppdatere budsjettkostnadene for.</span><span class="sxs-lookup"><span data-stu-id="88c8e-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="88c8e-116">Velg **Juster**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="88c8e-117">Hvis du vil legge til et beløp på de valgte linjene, merker du av for **Legg til kostnad**, og deretter angir du verdien i **Legg til verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="88c8e-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="88c8e-118">Hvis du vil multiplisere budsjettkostnaden på de valgte budsjettlinjene med en faktor, merker du av for **Multipliser kostnad** og angir faktoren i feltet **Multipliser verdi**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="88c8e-119">Hvis du for eksempel angir **1,2** i feltet **Multipliser verdi**, øker du budsjettkostnaden på de valgte linjene med 20 prosent.</span><span class="sxs-lookup"><span data-stu-id="88c8e-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="88c8e-120">Hvis du angir **0,7**, reduserer du budsjettkostnaden på de valgte linjene med 30 prosent.</span><span class="sxs-lookup"><span data-stu-id="88c8e-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="88c8e-121">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-121">Select **OK**.</span></span>

<span data-ttu-id="88c8e-122">De valgte budsjettlinjene oppdateres i henhold til verdiene du angir i trinn 3 eller 4.</span><span class="sxs-lookup"><span data-stu-id="88c8e-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="88c8e-123">Oppdatere faktiske kostnader</span><span class="sxs-lookup"><span data-stu-id="88c8e-123">Update actual costs</span></span>

<span data-ttu-id="88c8e-124">Når datoene på budsjettlinjene er passert, og faktiske kostnader er postert i Aktivastyring, kan du oppdatere de faktiske kostnadene i vedlikeholdsbudsjettet.</span><span class="sxs-lookup"><span data-stu-id="88c8e-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="88c8e-125">Velg **Oppdater kostnad** på siden **Vedlikeholdsbudsjettlinjer**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="88c8e-126">I dialogboksen **Beregn faktisk kostnad** velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="88c8e-127">**Faktisk kostnad**-feltene på budsjettlinjene oppdateres hvis faktiske kostnader er postert.</span><span class="sxs-lookup"><span data-stu-id="88c8e-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="88c8e-128">Nye budsjettlinjer kan genereres hvis det er opprettet nye aktivatyper etter at du opprettet budsjettet, og hvis disse aktivatypene er brukt på aktiva som arbeidsordrer er opprettet for og tilknyttede kostnader er postert for.</span><span class="sxs-lookup"><span data-stu-id="88c8e-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="88c8e-129">Nye budsjettlinjer viser bare faktiske kostnader fordi det ikke er beregnet noen budsjettkostnader for dem.</span><span class="sxs-lookup"><span data-stu-id="88c8e-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="88c8e-130">Hvis du vil vise en oversikt over faktiske kostnader delt inn i forebyggende, korrigerende og investeringskostnader, kan du utføre en beregning for den samme perioden på siden **Kostnadskontroll for aktivum**.</span><span class="sxs-lookup"><span data-stu-id="88c8e-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="88c8e-131">Legge til budsjettlinjer manuelt</span><span class="sxs-lookup"><span data-stu-id="88c8e-131">Manually add budget lines</span></span>

<span data-ttu-id="88c8e-132">På siden **Vedlikeholdsbudsjettlinjer** kan du manuelt legge til en ny budsjettlinje ved å velge **Ny** og deretter foreta valg på linjen.</span><span class="sxs-lookup"><span data-stu-id="88c8e-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="88c8e-133">Her er noen eksempler på situasjoner der denne fremgangsmåten kan være nyttig:</span><span class="sxs-lookup"><span data-stu-id="88c8e-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="88c8e-134">Du vet at reparasjon av enkelte aktiva er for øyeblikket i planleggingsfasen, men tilknyttede jobber er ennå ikke opprettet i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="88c8e-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="88c8e-135">Du vil imidlertid at budsjettkostnader for disse jobbene skal være med i vedlikeholdsbudsjettet.</span><span class="sxs-lookup"><span data-stu-id="88c8e-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="88c8e-136">Det er opprettet nye aktiva eller aktivatyper siden du opprettet vedlikeholdsbudsjettet, men vedlikeholdsplaner er ennå ikke definert for disse aktivaene eller aktivatypene.</span><span class="sxs-lookup"><span data-stu-id="88c8e-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="88c8e-137">Du vil imidlertid at budsjettkostnader for disse aktivatypene skal være med i vedlikeholdsbudsjettet.</span><span class="sxs-lookup"><span data-stu-id="88c8e-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
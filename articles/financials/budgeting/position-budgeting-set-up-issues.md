---
title: "Feilsøke stillingsbudsjettering"
description: "Denne artikkelen inneholder svar på spørsmål du kan ha når du konfigurerer stillingsbudsjettering. Det tar for seg vanlige spørsmål om hvordan du oppretter budsjettetkostnadselementer, kompensasjonsgrupper og kompensasjonsrutenett."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 421520fcd1b215a19c126ccea51b025977552448
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---

# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="c65a2-104">Feilsøke stillingsbudsjettering</span><span class="sxs-lookup"><span data-stu-id="c65a2-104">Position budgeting troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c65a2-105">Denne artikkelen inneholder svar på spørsmål du kan ha når du konfigurerer stillingsbudsjettering.</span><span class="sxs-lookup"><span data-stu-id="c65a2-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="c65a2-106">Det tar for seg vanlige spørsmål om hvordan du oppretter budsjettetkostnadselementer, kompensasjonsgrupper og kompensasjonsrutenett.</span><span class="sxs-lookup"><span data-stu-id="c65a2-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="c65a2-107">Hvorfor finner jeg ikke siden med prognosestillinger under Personale?</span><span class="sxs-lookup"><span data-stu-id="c65a2-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="c65a2-108">Prognosestillinger er flyttet til Budsjettering.</span><span class="sxs-lookup"><span data-stu-id="c65a2-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="c65a2-109">Hvorfor kan jeg ikke slette et budsjettkostnadselement?</span><span class="sxs-lookup"><span data-stu-id="c65a2-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="c65a2-110">Du kan ikke slette et budsjettkostnadselement som er tilordnet til en prognosestilling.</span><span class="sxs-lookup"><span data-stu-id="c65a2-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="c65a2-111">Før du kan slette et budsjettkostnadselement, må du fjerne det fra alle prognosestillinger.</span><span class="sxs-lookup"><span data-stu-id="c65a2-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="c65a2-112">**Tips:** For å finne alle stillinger som et budsjettert kostnadselement er tilordnet til, må du velge kostnadselementer å¨sioden **Budsjettkostnadselementer** og klikk deretter **Oppdater stillinger**.</span><span class="sxs-lookup"><span data-stu-id="c65a2-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="c65a2-113">Stillinger som bruker kostnadselementet, vises i det øvre rutenettet.</span><span class="sxs-lookup"><span data-stu-id="c65a2-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="c65a2-114">Hvordan kan jeg fjerne et kostnadselement fra flere prognosestillinger uten å åpne dem?</span><span class="sxs-lookup"><span data-stu-id="c65a2-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="c65a2-115">Du kan ikke fjerne et kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="c65a2-115">You can’t remove a cost element.</span></span> <span data-ttu-id="c65a2-116">Hvis du imidlertid endrer start- og sluttdatoene slik at de faller utenfor datoene for budsjettplanleggingssyklusen, blir kostnadselementert ikke lenger tilordnet til prognosestillingene i budsjettplanleggingssyklusen.</span><span class="sxs-lookup"><span data-stu-id="c65a2-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="c65a2-117">Til å gjøre denne endringen åpner du det budsjetterte kostnadselementet, og deretter i hurtigkategorien **Kostnadsberegning** klikker du **Endre datoer** og endre gjeldende dato eller utløpsdatoen.</span><span class="sxs-lookup"><span data-stu-id="c65a2-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="c65a2-118">Velg **OK** for å oppdatere automatisk alle prognosestillingene som kostnadelementet er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="c65a2-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="c65a2-119">**Tips!** Hvis du bruker denne metoden, må du være oppmerksom på at budsjettkostnadselementet dermed fjernes fra **alle** prognosestillinger der start- og sluttdatoene ikke lenger er i det aktuelle området.</span><span class="sxs-lookup"><span data-stu-id="c65a2-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="c65a2-120">Hvis dette ikke er det vil skal skje, må du åpne hver prognosestilling du vil fjerne budsjettkostnadselementet fra, og foreta endringen manuelt.</span><span class="sxs-lookup"><span data-stu-id="c65a2-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="c65a2-121">Hvorfor kan jeg ikke angi et årlig beløp i hurtigkategorien Kostnadsberegning for budsjettkostnadselementet?</span><span class="sxs-lookup"><span data-stu-id="c65a2-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="c65a2-122">Du kan ikke angi et årlig beløp hvis det finnes budsjettkostnadselementer i hurtigkategorien **Beregningsgrunnlag**, fordi systemet krever en prosent for å beregne verdien.</span><span class="sxs-lookup"><span data-stu-id="c65a2-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="c65a2-123">Fjern alle budsjettkostnadselementer fra hurtigkategorien **Beregningsgrunnlag** for å endre denne verdien.</span><span class="sxs-lookup"><span data-stu-id="c65a2-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="c65a2-124">Hvorfor kan jeg ikke endre budsjettkostnadstypen fra inntekt til en annen budsjettkostnadstype?</span><span class="sxs-lookup"><span data-stu-id="c65a2-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="c65a2-125">Noen budsjettkostnadselementer bruker kostnadselementet inntekt som beregningsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="c65a2-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="c65a2-126">Hvis du vil endre feltet **Budsjettkostnadstype**, må du fjerne kostnadselementet inntekt fra hurtigkategorien **Beregningsgrunnlag** for alle budsjettkostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="c65a2-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="c65a2-127">Hvorfor kan jeg ikke endre datoen på linjer for budsjettkostnadselement for et budsjettkostnadselement?</span><span class="sxs-lookup"><span data-stu-id="c65a2-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="c65a2-128">Du kan ikke endre datoen på linjen for budsjettkostnadselementet når et budsjettskostnadselement brukes av en prognosestilling.</span><span class="sxs-lookup"><span data-stu-id="c65a2-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="c65a2-129">Denne begreningein sikrer at prognosestillingene alltid er innenfor retningslinjene for budsjettkostnadselementet.</span><span class="sxs-lookup"><span data-stu-id="c65a2-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="c65a2-130">Hvis duvil endre datoen i hurtigkategorien **Kostnadsberegning**, klikker du **Endre datoer** og angir de nye datoene.</span><span class="sxs-lookup"><span data-stu-id="c65a2-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="c65a2-131">Klikk deretter **OK** for å oppdatere prognosestillingene som kostnadelementet er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="c65a2-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="c65a2-132">Hvorfor kan jeg ikke endre kostnadene for et budsjettkostnadselement på siden Kompensasjonsgruppe?</span><span class="sxs-lookup"><span data-stu-id="c65a2-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="c65a2-133">Du kan bare opprette og endre budsjettkostnadselementer på siden **Budsjettkostnadselementer**.</span><span class="sxs-lookup"><span data-stu-id="c65a2-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="c65a2-134">Hvorfor får jeg en feilmelding når jeg endrer datoene for et kostnadselement i en prognosestilling?</span><span class="sxs-lookup"><span data-stu-id="c65a2-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="c65a2-135">Datoene på prognosestillingens linje for kostnadselement må være innenfor følgende områder:</span><span class="sxs-lookup"><span data-stu-id="c65a2-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="c65a2-136">Aktiverings- og pensjonavgangsdatoene for stillingen.</span><span class="sxs-lookup"><span data-stu-id="c65a2-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="c65a2-137">Aktiverings- og utløpsdatoene for budsjettkostnadselementet.</span><span class="sxs-lookup"><span data-stu-id="c65a2-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="c65a2-138">Start- og sluttdatoene for budsjettsyklusen som er knyttet til budsjettplanleggingsprosessen for prognosestillingen.</span><span class="sxs-lookup"><span data-stu-id="c65a2-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>






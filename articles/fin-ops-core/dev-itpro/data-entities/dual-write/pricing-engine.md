---
title: Synkronisere med prismotoren for Supply Chain Management ved behov
description: Dette emnet beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Supply Chain Management fra Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: bf4154816f01040a236dde77b92ee69396158614
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750770"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="d6a4d-103">Synkronisere med prismotoren for Supply Chain Management ved behov</span><span class="sxs-lookup"><span data-stu-id="d6a4d-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="d6a4d-104">Microsoft Dynamics 365 Supply Chain Management inkluderer en prissettingsmotor som håndterer forretningsavtaler, prislister, fordelsprogrammer, kampanjer og rabatter.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="d6a4d-105">Prissettingsmotoren bruker komplekse regler til å bestemme den beste prisen for et gitt tilbud eller ordre.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="d6a4d-106">Når du bruker dobbel skriving, bruker du enten statisk prissetting eller prissettingsmotoren fra Dynamics 365 Supply Chain Management på tilbuds- og ordresider i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="d6a4d-107">Bruk prissettingsmotoren fra Supply Chain Management i Sales</span><span class="sxs-lookup"><span data-stu-id="d6a4d-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="d6a4d-108">I Sales går du til **Salg \> Ordrer**.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="d6a4d-109">Velg **Ny** for å opprette en ny ordre, eller velg en eksisterende ordre i **Mine ordrer**-listen.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="d6a4d-110">Legg til en ny ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-110">Add a new order line.</span></span>
4. <span data-ttu-id="d6a4d-111">Hvis du oppretter en ny ordre, velger du **Prisordre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="d6a4d-112">Hvis du oppdaterer en eksisterende ordre, velger du **Beregn på nytt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="d6a4d-113">Følgende kolonner fylles ut automatisk:</span><span class="sxs-lookup"><span data-stu-id="d6a4d-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="d6a4d-114">Detaljbeløp</span><span class="sxs-lookup"><span data-stu-id="d6a4d-114">Detail Amount</span></span>
    + <span data-ttu-id="d6a4d-115">Rabatt-%</span><span class="sxs-lookup"><span data-stu-id="d6a4d-115">Discount %</span></span>
    + <span data-ttu-id="d6a4d-116">Rabatt</span><span class="sxs-lookup"><span data-stu-id="d6a4d-116">Discount</span></span>
    + <span data-ttu-id="d6a4d-117">Beløp før frakt</span><span class="sxs-lookup"><span data-stu-id="d6a4d-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="d6a4d-118">Fraktbeløp</span><span class="sxs-lookup"><span data-stu-id="d6a4d-118">Freight Amount</span></span>
    + <span data-ttu-id="d6a4d-119">Total avgift</span><span class="sxs-lookup"><span data-stu-id="d6a4d-119">Total Tax</span></span>
    + <span data-ttu-id="d6a4d-120">Totalbeløp</span><span class="sxs-lookup"><span data-stu-id="d6a4d-120">Total Amount</span></span>
    
5. <span data-ttu-id="d6a4d-121">For å sikre at systemet vurderer handels- og salgsavtaler for å beregne prisen:</span><span class="sxs-lookup"><span data-stu-id="d6a4d-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="d6a4d-122">Gå til Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="d6a4d-123">Gå til **Kunder \> Oppsett \> Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="d6a4d-124">Velg fanen **Priser** i sidenavigasjonsfeltet.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="d6a4d-125">Fjern merket for **Manuell registrering** under hurtigfanen **Evaluering av handelssavtale**.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="d6a4d-126">Hvordan det fungerer</span><span class="sxs-lookup"><span data-stu-id="d6a4d-126">How it works</span></span>

<span data-ttu-id="d6a4d-127">Når du velger **Prisordre** i Sales, kalles **Summer**-funksjonen i fanen **Salgsordre \> Vis** i Supply Chain Management for den tilknyttede salgsordren.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="d6a4d-128">Verdiene i ordretotalen i Sales brukes til å fylle ut de tilsvarende kolonnene i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="d6a4d-129">Når salgsordretotalen beregnes i Supply Chain Management, evaluerer beregningen de eksisterende forretningsavtalene og salgsavtalene for kunden og produktene som er oppført i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="d6a4d-130">Denne informasjonen brukes til å beregne totalene.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="d6a4d-131">Når **Prisordre** er valgt, gjenspeiler Sale automatisk alle oppsett som er utført i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="d6a4d-132">Begrensninger</span><span class="sxs-lookup"><span data-stu-id="d6a4d-132">Limitations</span></span>

<span data-ttu-id="d6a4d-133">Når kolonnene i Sales fylles ut, gjelder følgende begrensninger:</span><span class="sxs-lookup"><span data-stu-id="d6a4d-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="d6a4d-134">Oppsettet av gebyrer og gebyrfordelinger i Supply Chain Management replikeres ikke i Sales.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="d6a4d-135">Prissetting tar ikke hensyn til spesielle detaljhandelpriser som er angitt i **Detaljhandelskanal**-kolonnen på salgsordrelinje-siden i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="d6a4d-136">Rabatter som er definert i delen **Handelsrabattbehandling** i Supply Chain Management, vurderes ikke.</span><span class="sxs-lookup"><span data-stu-id="d6a4d-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
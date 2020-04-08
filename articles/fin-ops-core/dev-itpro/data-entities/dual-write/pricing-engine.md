---
title: Synkronisere med prissettingsmotoren i Dynamics 365 Supply Chain Management ved forespørsel
description: Dette emnet beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Supply Chain Management fra Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173183"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="ae278-103">Synkronisere med prissettingsmotoren i Dynamics 365 Supply Chain Management ved forespørsel</span><span class="sxs-lookup"><span data-stu-id="ae278-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="ae278-104">Microsoft Dynamics 365 Supply Chain Management inkluderer en prissettingsmotor som håndterer forretningsavtaler, prislister, fordelsprogrammer, kampanjer og rabatter.</span><span class="sxs-lookup"><span data-stu-id="ae278-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="ae278-105">Prissettingsmotoren bruker komplekse regler til å bestemme den beste prisen for et gitt tilbud eller ordre.</span><span class="sxs-lookup"><span data-stu-id="ae278-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="ae278-106">Når du bruker dobbel skriving, bruker du enten statisk prissetting eller prissettingsmotoren fra Dynamics 365 Supply Chain Management på tilbuds- og ordresider i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ae278-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="ae278-107">Bruk prissettingsmotoren fra Supply Chain Management i Sales</span><span class="sxs-lookup"><span data-stu-id="ae278-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="ae278-108">I Sales går du til **Salg \> Ordrer**.</span><span class="sxs-lookup"><span data-stu-id="ae278-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="ae278-109">Velg **Ny** for å opprette en ny ordre, eller velg en eksisterende ordre i **Mine ordrer**-listen.</span><span class="sxs-lookup"><span data-stu-id="ae278-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="ae278-110">Legg til en ny ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="ae278-110">Add a new order line.</span></span>
4. <span data-ttu-id="ae278-111">Hvis du oppretter en ny ordre, velger du **Prisordre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ae278-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="ae278-112">Hvis du oppdaterer en eksisterende ordre, velger du **Beregn på nytt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ae278-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="ae278-113">Følgende felt fylles ut automatisk:</span><span class="sxs-lookup"><span data-stu-id="ae278-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="ae278-114">Detaljbeløp</span><span class="sxs-lookup"><span data-stu-id="ae278-114">Detail Amount</span></span>
    + <span data-ttu-id="ae278-115">Rabatt-%</span><span class="sxs-lookup"><span data-stu-id="ae278-115">Discount %</span></span>
    + <span data-ttu-id="ae278-116">Rabatt</span><span class="sxs-lookup"><span data-stu-id="ae278-116">Discount</span></span>
    + <span data-ttu-id="ae278-117">Beløp før frakt</span><span class="sxs-lookup"><span data-stu-id="ae278-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="ae278-118">Fraktbeløp</span><span class="sxs-lookup"><span data-stu-id="ae278-118">Freight Amount</span></span>
    + <span data-ttu-id="ae278-119">Total avgift</span><span class="sxs-lookup"><span data-stu-id="ae278-119">Total Tax</span></span>
    + <span data-ttu-id="ae278-120">Totalbeløp</span><span class="sxs-lookup"><span data-stu-id="ae278-120">Total Amount</span></span>

## <a name="how-it-works"></a><span data-ttu-id="ae278-121">Hvordan det fungerer</span><span class="sxs-lookup"><span data-stu-id="ae278-121">How it works</span></span>

<span data-ttu-id="ae278-122">Når du velger **Prisordre** i Sales, kalles **Summer**-funksjonen i kategorien **Salgsordre \> Vis** i Supply Chain Management for den tilknyttede salgsordren.</span><span class="sxs-lookup"><span data-stu-id="ae278-122">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="ae278-123">Verdiene i ordretotalen i Sales brukes til å fylle ut de tilsvarende feltene i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae278-123">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="ae278-124">Når salgsordretotalen beregnes i Supply Chain Management, evaluerer beregningen de eksisterende forretningsavtalene og salgsavtalene for kunden og produktene som er oppført i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="ae278-124">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="ae278-125">Denne informasjonen brukes til å beregne totalene.</span><span class="sxs-lookup"><span data-stu-id="ae278-125">This information is used to calculate the totals.</span></span> <span data-ttu-id="ae278-126">Når **Prisordre** er valgt, gjenspeiler Sale automatisk alle oppsett som er utført i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae278-126">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="ae278-127">Begrensninger</span><span class="sxs-lookup"><span data-stu-id="ae278-127">Limitations</span></span>

<span data-ttu-id="ae278-128">Når feltene i Sale er fylt ut, gjelder følgende begrensninger:</span><span class="sxs-lookup"><span data-stu-id="ae278-128">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="ae278-129">Oppsettet av gebyrer og gebyrfordelinger i Supply Chain Management replikeres ikke i Sales.</span><span class="sxs-lookup"><span data-stu-id="ae278-129">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="ae278-130">Prissetting tar ikke hensyn til spesielle detaljhandelpriser som er angitt i **Detaljhandelskanal**-feltet på salgsordrelinje-siden i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae278-130">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="ae278-131">Rabatter som er definert i delen **Handelsrabattbehandling** i Supply Chain Management, vurderes ikke.</span><span class="sxs-lookup"><span data-stu-id="ae278-131">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>

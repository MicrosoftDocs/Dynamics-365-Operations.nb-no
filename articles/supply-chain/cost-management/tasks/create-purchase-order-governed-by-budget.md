---
title: Opprette en bestilling som styres av budsjett
description: Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbfbbef3bd7c7398f0f17b6cddbbff8c4755638d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963719"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="5e13b-103">Opprette en bestilling som styres av budsjett</span><span class="sxs-lookup"><span data-stu-id="5e13b-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e13b-104">Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.</span><span class="sxs-lookup"><span data-stu-id="5e13b-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="5e13b-105">Denne registreringen bruker USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="5e13b-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="5e13b-106">Gå gjennom budsjettkontrollkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="5e13b-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="5e13b-107">Gå til Budsjettering > Oppsett > Budsjettkontroll > Busjettkontrollkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="5e13b-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="5e13b-108">Klikk på fanen Tilgjengelige budsjettmidler.</span><span class="sxs-lookup"><span data-stu-id="5e13b-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="5e13b-109">Klikk på fanen Dokumenter og kladder.</span><span class="sxs-lookup"><span data-stu-id="5e13b-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="5e13b-110">Klikk på fanen Definer budsjettkontrollregler.</span><span class="sxs-lookup"><span data-stu-id="5e13b-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="5e13b-111">Klikk på fanen Definer budsjettgrupper.</span><span class="sxs-lookup"><span data-stu-id="5e13b-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="5e13b-112">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5e13b-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="5e13b-113">Opprette bestillingshode</span><span class="sxs-lookup"><span data-stu-id="5e13b-113">Create the purchase order header</span></span>
1. <span data-ttu-id="5e13b-114">Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="5e13b-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="5e13b-115">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="5e13b-115">Click New.</span></span>
3. <span data-ttu-id="5e13b-116">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="5e13b-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="5e13b-117">Utvid delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="5e13b-117">Expand the General section.</span></span>
5. <span data-ttu-id="5e13b-118">Angi datoen til 2016-01-01 i feltet Regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="5e13b-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="5e13b-119">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="5e13b-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="5e13b-120">Legge til en bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="5e13b-120">Add a purchase order line</span></span>
1. <span data-ttu-id="5e13b-121">Angi eller velg en verdi i feltet Innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="5e13b-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="5e13b-122">Sett Antall til 2.</span><span class="sxs-lookup"><span data-stu-id="5e13b-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="5e13b-123">Angi eller velg en verdi i Enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="5e13b-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="5e13b-124">Sett enhetspris til 10000.</span><span class="sxs-lookup"><span data-stu-id="5e13b-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="5e13b-125">Klikk på Finans.</span><span class="sxs-lookup"><span data-stu-id="5e13b-125">Click Financials.</span></span>
6. <span data-ttu-id="5e13b-126">Klikk på Fordel beløp.</span><span class="sxs-lookup"><span data-stu-id="5e13b-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="5e13b-127">Angi verdien 601300-001-023-- i feltet Finanskonto.</span><span class="sxs-lookup"><span data-stu-id="5e13b-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="5e13b-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5e13b-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="5e13b-129">Utfør budsjettkontroll</span><span class="sxs-lookup"><span data-stu-id="5e13b-129">Perform budget checking</span></span>
1. <span data-ttu-id="5e13b-130">Klikk på Finans.</span><span class="sxs-lookup"><span data-stu-id="5e13b-130">Click Financials.</span></span>
2. <span data-ttu-id="5e13b-131">Klikk på Utfør budsjettkontroll.</span><span class="sxs-lookup"><span data-stu-id="5e13b-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="5e13b-132">Klikk på Finans.</span><span class="sxs-lookup"><span data-stu-id="5e13b-132">Click Financials.</span></span>
4. <span data-ttu-id="5e13b-133">Klikk på Feil eller advarsler for budsjettkontroll.</span><span class="sxs-lookup"><span data-stu-id="5e13b-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="5e13b-134">Klikk på Lukk.</span><span class="sxs-lookup"><span data-stu-id="5e13b-134">Click Close.</span></span>


--- 
title: Opprette en bestilling som styres av budsjett
description: "Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ddd725df4e06caf36be0e8913b556469421fa1af
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="49dbc-103">Opprette en bestilling som styres av budsjett</span><span class="sxs-lookup"><span data-stu-id="49dbc-103">Create a purchase order governed by budget</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49dbc-104">Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.</span><span class="sxs-lookup"><span data-stu-id="49dbc-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="49dbc-105">Denne registreringen bruker USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="49dbc-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="49dbc-106">Gå gjennom budsjettkontrollkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="49dbc-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="49dbc-107">Gå til Budsjettering > Oppsett > Budsjettkontroll > Busjettkontrollkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="49dbc-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="49dbc-108">Klikk fanen Tilgjengelige budsjettmidler.</span><span class="sxs-lookup"><span data-stu-id="49dbc-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="49dbc-109">Klikk fanen Dokumenter og kladder.</span><span class="sxs-lookup"><span data-stu-id="49dbc-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="49dbc-110">Klikk fanen Definer budsjettkontrollregler.</span><span class="sxs-lookup"><span data-stu-id="49dbc-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="49dbc-111">Klikk fanen Definer budsjettgrupper.</span><span class="sxs-lookup"><span data-stu-id="49dbc-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="49dbc-112">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="49dbc-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="49dbc-113">Opprette bestillingshode</span><span class="sxs-lookup"><span data-stu-id="49dbc-113">Create the purchase order header</span></span>
1. <span data-ttu-id="49dbc-114">Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="49dbc-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="49dbc-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="49dbc-115">Click New.</span></span>
3. <span data-ttu-id="49dbc-116">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="49dbc-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="49dbc-117">Utvid delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="49dbc-117">Expand the General section.</span></span>
5. <span data-ttu-id="49dbc-118">Angi datoen til 2016-01-01 i feltet Regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="49dbc-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="49dbc-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="49dbc-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="49dbc-120">Legge til en bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="49dbc-120">Add a purchase order line</span></span>
1. <span data-ttu-id="49dbc-121">Angi eller velg en verdi i feltet Innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="49dbc-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="49dbc-122">Sett Antall til 2.</span><span class="sxs-lookup"><span data-stu-id="49dbc-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="49dbc-123">Angi eller velg en verdi i Enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="49dbc-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="49dbc-124">Sett enhetspris til 10000.</span><span class="sxs-lookup"><span data-stu-id="49dbc-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="49dbc-125">Klikk Finans.</span><span class="sxs-lookup"><span data-stu-id="49dbc-125">Click Financials.</span></span>
6. <span data-ttu-id="49dbc-126">Klikk Fordel beløp.</span><span class="sxs-lookup"><span data-stu-id="49dbc-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="49dbc-127">Angi verdien 601300-001-023-- i feltet Finanskonto.</span><span class="sxs-lookup"><span data-stu-id="49dbc-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="49dbc-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="49dbc-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="49dbc-129">Utfør budsjettkontroll</span><span class="sxs-lookup"><span data-stu-id="49dbc-129">Perform budget checking</span></span>
1. <span data-ttu-id="49dbc-130">Klikk Finans.</span><span class="sxs-lookup"><span data-stu-id="49dbc-130">Click Financials.</span></span>
2. <span data-ttu-id="49dbc-131">Klikk Utfør budsjettkontroll.</span><span class="sxs-lookup"><span data-stu-id="49dbc-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="49dbc-132">Klikk Finans.</span><span class="sxs-lookup"><span data-stu-id="49dbc-132">Click Financials.</span></span>
4. <span data-ttu-id="49dbc-133">Klikk Feil eller advarsler for budsjettkontroll.</span><span class="sxs-lookup"><span data-stu-id="49dbc-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="49dbc-134">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="49dbc-134">Click Close.</span></span>



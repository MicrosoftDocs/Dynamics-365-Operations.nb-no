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
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 319eb0070a3677035e2a5d89744e80cd38c08d8e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434484"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="98c37-103">Opprette en bestilling som styres av budsjett</span><span class="sxs-lookup"><span data-stu-id="98c37-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98c37-104">Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.</span><span class="sxs-lookup"><span data-stu-id="98c37-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="98c37-105">Denne registreringen bruker USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="98c37-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="98c37-106">Gå gjennom budsjettkontrollkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="98c37-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="98c37-107">Gå til Budsjettering > Oppsett > Budsjettkontroll > Busjettkontrollkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="98c37-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="98c37-108">Klikk fanen Tilgjengelige budsjettmidler.</span><span class="sxs-lookup"><span data-stu-id="98c37-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="98c37-109">Klikk fanen Dokumenter og kladder.</span><span class="sxs-lookup"><span data-stu-id="98c37-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="98c37-110">Klikk fanen Definer budsjettkontrollregler.</span><span class="sxs-lookup"><span data-stu-id="98c37-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="98c37-111">Klikk fanen Definer budsjettgrupper.</span><span class="sxs-lookup"><span data-stu-id="98c37-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="98c37-112">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98c37-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="98c37-113">Opprette bestillingshode</span><span class="sxs-lookup"><span data-stu-id="98c37-113">Create the purchase order header</span></span>
1. <span data-ttu-id="98c37-114">Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="98c37-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="98c37-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="98c37-115">Click New.</span></span>
3. <span data-ttu-id="98c37-116">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="98c37-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="98c37-117">Utvid delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="98c37-117">Expand the General section.</span></span>
5. <span data-ttu-id="98c37-118">Angi datoen til 2016-01-01 i feltet Regnskapsdato.</span><span class="sxs-lookup"><span data-stu-id="98c37-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="98c37-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="98c37-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="98c37-120">Legge til en bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="98c37-120">Add a purchase order line</span></span>
1. <span data-ttu-id="98c37-121">Angi eller velg en verdi i feltet Innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="98c37-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="98c37-122">Sett Antall til 2.</span><span class="sxs-lookup"><span data-stu-id="98c37-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="98c37-123">Angi eller velg en verdi i Enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="98c37-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="98c37-124">Sett enhetspris til 10000.</span><span class="sxs-lookup"><span data-stu-id="98c37-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="98c37-125">Klikk Finans.</span><span class="sxs-lookup"><span data-stu-id="98c37-125">Click Financials.</span></span>
6. <span data-ttu-id="98c37-126">Klikk Fordel beløp.</span><span class="sxs-lookup"><span data-stu-id="98c37-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="98c37-127">Angi verdien 601300-001-023-- i feltet Finanskonto.</span><span class="sxs-lookup"><span data-stu-id="98c37-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="98c37-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="98c37-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="98c37-129">Utfør budsjettkontroll</span><span class="sxs-lookup"><span data-stu-id="98c37-129">Perform budget checking</span></span>
1. <span data-ttu-id="98c37-130">Klikk Finans.</span><span class="sxs-lookup"><span data-stu-id="98c37-130">Click Financials.</span></span>
2. <span data-ttu-id="98c37-131">Klikk Utfør budsjettkontroll.</span><span class="sxs-lookup"><span data-stu-id="98c37-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="98c37-132">Klikk Finans.</span><span class="sxs-lookup"><span data-stu-id="98c37-132">Click Financials.</span></span>
4. <span data-ttu-id="98c37-133">Klikk Feil eller advarsler for budsjettkontroll.</span><span class="sxs-lookup"><span data-stu-id="98c37-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="98c37-134">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="98c37-134">Click Close.</span></span>


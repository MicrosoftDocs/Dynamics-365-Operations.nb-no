---
title: Opprett utlånsvarer
description: Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75b2f17eb41ead7422276f72429eb6ede2ef4759
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "856237"
---
# <a name="create-loan-items"></a><span data-ttu-id="b47e9-103">Opprett utlånsvarer</span><span class="sxs-lookup"><span data-stu-id="b47e9-103">Create loan items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b47e9-104">Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere.</span><span class="sxs-lookup"><span data-stu-id="b47e9-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="b47e9-105">Hver fysiske vare må ha en tilsvarende utlånsvare.</span><span class="sxs-lookup"><span data-stu-id="b47e9-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="b47e9-106">Hver utlånsvarepost må beskrive hva som lånes ut, hvem som er ansvarlig for utlånet og antall dager varen kan lånes ut.</span><span class="sxs-lookup"><span data-stu-id="b47e9-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="b47e9-107">Du kan opprette flere utlånsvarer, for eksempel nøkler, adgangskort eller uniformer, samtidig.</span><span class="sxs-lookup"><span data-stu-id="b47e9-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="b47e9-108">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="b47e9-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="b47e9-109">Opprette utlånstyper</span><span class="sxs-lookup"><span data-stu-id="b47e9-109">Create Loan types</span></span>
1. <span data-ttu-id="b47e9-110">Gå til Personale > Arbeidere > Utlånsvarer > Utlånstyper.</span><span class="sxs-lookup"><span data-stu-id="b47e9-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="b47e9-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b47e9-111">Click New.</span></span>
3. <span data-ttu-id="b47e9-112">Skriv inn en verdi i feltet Utlånstype.</span><span class="sxs-lookup"><span data-stu-id="b47e9-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="b47e9-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b47e9-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b47e9-114">Definer antall dager som varer som er tilordnet til denne utlånstypen, kan være forfalt med.</span><span class="sxs-lookup"><span data-stu-id="b47e9-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="b47e9-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b47e9-115">Click Save.</span></span>
7. <span data-ttu-id="b47e9-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b47e9-116">Close the page.</span></span>
8. <span data-ttu-id="b47e9-117">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="b47e9-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="b47e9-118">Opprette utlånsvarer</span><span class="sxs-lookup"><span data-stu-id="b47e9-118">Create Loan items</span></span>
1. <span data-ttu-id="b47e9-119">Gå til Personale > Arbeidere > Utlånsvarer > Utlånsvarer.</span><span class="sxs-lookup"><span data-stu-id="b47e9-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="b47e9-120">Klikk Opprett utlånsvarer.</span><span class="sxs-lookup"><span data-stu-id="b47e9-120">Click Create loan items.</span></span>
3. <span data-ttu-id="b47e9-121">I Antall-feltet angir du et nummer.</span><span class="sxs-lookup"><span data-stu-id="b47e9-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="b47e9-122">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b47e9-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b47e9-123">Klikk rullegardinknappen i Utlånstype-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b47e9-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b47e9-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b47e9-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b47e9-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b47e9-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b47e9-126">Angi antallet dager varen kan være på utlån.</span><span class="sxs-lookup"><span data-stu-id="b47e9-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="b47e9-127">Standardverdien for Planlagt retur-feltet på siden Lånt utstyr blir beregnet som gjeldende dato pluss dette antallet.</span><span class="sxs-lookup"><span data-stu-id="b47e9-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="b47e9-128">Klikk rullegardinknappen i Ansvarlig-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b47e9-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="b47e9-129">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="b47e9-129">Click Select.</span></span>
11. <span data-ttu-id="b47e9-130">Angi et tall i Startverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="b47e9-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="b47e9-131">Angi et tall i Intervall-feltet.</span><span class="sxs-lookup"><span data-stu-id="b47e9-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="b47e9-132">Skriv inn en verdi i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="b47e9-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="b47e9-133">Hvis startnummeret for en utlånsvare for eksempel er 10, angir du to nummersymboler i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="b47e9-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="b47e9-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b47e9-134">Click OK.</span></span>
15. <span data-ttu-id="b47e9-135">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="b47e9-135">Refresh the page.</span></span>


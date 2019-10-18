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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179329"
---
# <a name="create-loan-items"></a><span data-ttu-id="09ff3-103">Opprett utlånsvarer</span><span class="sxs-lookup"><span data-stu-id="09ff3-103">Create loan items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09ff3-104">Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere.</span><span class="sxs-lookup"><span data-stu-id="09ff3-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="09ff3-105">Hver fysiske vare må ha en tilsvarende utlånsvare.</span><span class="sxs-lookup"><span data-stu-id="09ff3-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="09ff3-106">Hver utlånsvarepost må beskrive hva som lånes ut, hvem som er ansvarlig for utlånet og antall dager varen kan lånes ut.</span><span class="sxs-lookup"><span data-stu-id="09ff3-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="09ff3-107">Du kan opprette flere utlånsvarer, for eksempel nøkler, adgangskort eller uniformer, samtidig.</span><span class="sxs-lookup"><span data-stu-id="09ff3-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="09ff3-108">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="09ff3-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="09ff3-109">Opprette utlånstyper</span><span class="sxs-lookup"><span data-stu-id="09ff3-109">Create Loan types</span></span>
1. <span data-ttu-id="09ff3-110">Gå til Personale > Arbeidere > Utlånsvarer > Utlånstyper.</span><span class="sxs-lookup"><span data-stu-id="09ff3-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="09ff3-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="09ff3-111">Click New.</span></span>
3. <span data-ttu-id="09ff3-112">Skriv inn en verdi i feltet Utlånstype.</span><span class="sxs-lookup"><span data-stu-id="09ff3-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="09ff3-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="09ff3-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="09ff3-114">Definer antall dager som varer som er tilordnet til denne utlånstypen, kan være forfalt med.</span><span class="sxs-lookup"><span data-stu-id="09ff3-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="09ff3-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="09ff3-115">Click Save.</span></span>
7. <span data-ttu-id="09ff3-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="09ff3-116">Close the page.</span></span>
8. <span data-ttu-id="09ff3-117">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="09ff3-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="09ff3-118">Opprette utlånsvarer</span><span class="sxs-lookup"><span data-stu-id="09ff3-118">Create Loan items</span></span>
1. <span data-ttu-id="09ff3-119">Gå til Personale > Arbeidere > Utlånsvarer > Utlånsvarer.</span><span class="sxs-lookup"><span data-stu-id="09ff3-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="09ff3-120">Klikk Opprett utlånsvarer.</span><span class="sxs-lookup"><span data-stu-id="09ff3-120">Click Create loan items.</span></span>
3. <span data-ttu-id="09ff3-121">I Antall-feltet angir du et nummer.</span><span class="sxs-lookup"><span data-stu-id="09ff3-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="09ff3-122">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="09ff3-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="09ff3-123">Klikk rullegardinknappen i Utlånstype-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="09ff3-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="09ff3-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="09ff3-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="09ff3-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="09ff3-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="09ff3-126">Angi antallet dager varen kan være på utlån.</span><span class="sxs-lookup"><span data-stu-id="09ff3-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="09ff3-127">Standardverdien for Planlagt retur-feltet på siden Lånt utstyr blir beregnet som gjeldende dato pluss dette antallet.</span><span class="sxs-lookup"><span data-stu-id="09ff3-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="09ff3-128">Klikk rullegardinknappen i Ansvarlig-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="09ff3-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="09ff3-129">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="09ff3-129">Click Select.</span></span>
11. <span data-ttu-id="09ff3-130">Angi et tall i Startverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="09ff3-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="09ff3-131">Angi et tall i Intervall-feltet.</span><span class="sxs-lookup"><span data-stu-id="09ff3-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="09ff3-132">Skriv inn en verdi i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="09ff3-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="09ff3-133">Hvis startnummeret for en utlånsvare for eksempel er 10, angir du to nummersymboler i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="09ff3-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="09ff3-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="09ff3-134">Click OK.</span></span>
15. <span data-ttu-id="09ff3-135">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="09ff3-135">Refresh the page.</span></span>


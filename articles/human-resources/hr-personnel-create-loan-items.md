---
title: Opprett utlånsvarer
description: Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11c81e37952c59325c4f7dd46fd19599fbf8390f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056834"
---
# <a name="create-loan-items"></a><span data-ttu-id="ca9df-103">Opprett utlånsvarer</span><span class="sxs-lookup"><span data-stu-id="ca9df-103">Create loan items</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="ca9df-104">Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere.</span><span class="sxs-lookup"><span data-stu-id="ca9df-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="ca9df-105">Hver fysiske vare må ha en tilsvarende utlånsvare.</span><span class="sxs-lookup"><span data-stu-id="ca9df-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="ca9df-106">Hver utlånsvarepost må beskrive hva som lånes ut, hvem som er ansvarlig for utlånet og antall dager varen kan lånes ut.</span><span class="sxs-lookup"><span data-stu-id="ca9df-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="ca9df-107">Du kan opprette flere utlånsvarer, for eksempel nøkler, adgangskort eller uniformer, samtidig.</span><span class="sxs-lookup"><span data-stu-id="ca9df-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="ca9df-108">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ca9df-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="ca9df-109">Opprette utlånstyper</span><span class="sxs-lookup"><span data-stu-id="ca9df-109">Create Loan types</span></span>
1. <span data-ttu-id="ca9df-110">Gå til Personale > Arbeidere > Utlånsvarer > Utlånstyper.</span><span class="sxs-lookup"><span data-stu-id="ca9df-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="ca9df-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ca9df-111">Click New.</span></span>
3. <span data-ttu-id="ca9df-112">Skriv inn en verdi i feltet Utlånstype.</span><span class="sxs-lookup"><span data-stu-id="ca9df-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="ca9df-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ca9df-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ca9df-114">Definer antall dager som varer som er tilordnet til denne utlånstypen, kan være forfalt med.</span><span class="sxs-lookup"><span data-stu-id="ca9df-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="ca9df-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ca9df-115">Click Save.</span></span>
7. <span data-ttu-id="ca9df-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca9df-116">Close the page.</span></span>
8. <span data-ttu-id="ca9df-117">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="ca9df-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="ca9df-118">Opprette utlånsvarer</span><span class="sxs-lookup"><span data-stu-id="ca9df-118">Create Loan items</span></span>
1. <span data-ttu-id="ca9df-119">Gå til Personale > Arbeidere > Utlånsvarer > Utlånsvarer.</span><span class="sxs-lookup"><span data-stu-id="ca9df-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="ca9df-120">Klikk Opprett utlånsvarer.</span><span class="sxs-lookup"><span data-stu-id="ca9df-120">Click Create loan items.</span></span>
3. <span data-ttu-id="ca9df-121">I Antall-feltet angir du et nummer.</span><span class="sxs-lookup"><span data-stu-id="ca9df-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="ca9df-122">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ca9df-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ca9df-123">Klikk rullegardinknappen i Utlånstype-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ca9df-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ca9df-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ca9df-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ca9df-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ca9df-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ca9df-126">Angi antallet dager varen kan være på utlån.</span><span class="sxs-lookup"><span data-stu-id="ca9df-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="ca9df-127">Standardverdien for Planlagt retur-feltet på siden Lånt utstyr blir beregnet som gjeldende dato pluss dette antallet.</span><span class="sxs-lookup"><span data-stu-id="ca9df-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="ca9df-128">Klikk rullegardinknappen i Ansvarlig-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ca9df-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ca9df-129">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="ca9df-129">Click Select.</span></span>
11. <span data-ttu-id="ca9df-130">Angi et tall i Startverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca9df-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="ca9df-131">Angi et tall i Intervall-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca9df-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="ca9df-132">Skriv inn en verdi i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca9df-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="ca9df-133">Hvis startnummeret for en utlånsvare for eksempel er 10, angir du to nummersymboler i Format-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca9df-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="ca9df-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ca9df-134">Click OK.</span></span>
15. <span data-ttu-id="ca9df-135">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="ca9df-135">Refresh the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
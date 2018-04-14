--- 
title: Definer mva-utligningsperioder
description: "Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6de8dbd33a02183ee8bafca720c3738e8eac44e8
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="affaa-103">Definer mva-utligningsperioder</span><span class="sxs-lookup"><span data-stu-id="affaa-103">Set up sales tax settlement periods</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="affaa-104">Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for.</span><span class="sxs-lookup"><span data-stu-id="affaa-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="affaa-105">En utligningsprosess kan kjøres for en utligningsperiode for et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="affaa-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="affaa-106">Alle mva-koder som er knyttet til utligningsperioden, blir utlignet.</span><span class="sxs-lookup"><span data-stu-id="affaa-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="affaa-107">Avhengig av oppsettet av den beslektede skattemyndigheten, posteres skattegjelden til en leverandør eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="affaa-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="affaa-108">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="affaa-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="affaa-109">Gå til Avgift > Indirekte avgifter > Merverdiavgift > Mva-utligningsperioder.</span><span class="sxs-lookup"><span data-stu-id="affaa-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="affaa-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="affaa-110">Click New.</span></span>
3. <span data-ttu-id="affaa-111">Angi en verdi i feltet Utligningsperiode.</span><span class="sxs-lookup"><span data-stu-id="affaa-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="affaa-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="affaa-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="affaa-113">I Skattemyndighet-feltet velger du skattemyndigheten som skal motta rapportene og betalingene som er opprettet for utligningsperioden.</span><span class="sxs-lookup"><span data-stu-id="affaa-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="affaa-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="affaa-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="affaa-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="affaa-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="affaa-116">Klikk rullegardinknappen i Betalingsbetingelser-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="affaa-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="affaa-117">Den relaterte skattemyndigheten kan defineres som en leverandør og mva-utligningen oppretter en åpen leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="affaa-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="affaa-118">Betalingsbetingelsene definerer forfallsdatoen for den åpne leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="affaa-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="affaa-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="affaa-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="affaa-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="affaa-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="affaa-121">Velg en type for utligningsperiodeintervallet.</span><span class="sxs-lookup"><span data-stu-id="affaa-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="affaa-122">Angi antall enheter i periodeintervallet per periode.</span><span class="sxs-lookup"><span data-stu-id="affaa-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="affaa-123">Et kvartal har for eksempel 3 måneder.</span><span class="sxs-lookup"><span data-stu-id="affaa-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="affaa-124">Merk av eller fjern merket i avmerkingsboksen Bruk satsvis behandling for utligning av merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="affaa-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="affaa-125">Utligningsprosessen for utligningsperioden kan behandles som en satsvis jobb i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="affaa-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="affaa-126">Dette anbefales for et stort antall mva-transaksjoner i et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="affaa-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="affaa-127">Utvid kategorien Periodeintervaller.</span><span class="sxs-lookup"><span data-stu-id="affaa-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="affaa-128">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="affaa-128">Click Add.</span></span>
16. <span data-ttu-id="affaa-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="affaa-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="affaa-130">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="affaa-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="affaa-131">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="affaa-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="affaa-132">Klikk Nytt periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="affaa-132">Click New period interval.</span></span>
    * <span data-ttu-id="affaa-133">Når det første periodeintervallet er angitt, kan du opprette nye perioder automatisk.</span><span class="sxs-lookup"><span data-stu-id="affaa-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="affaa-134">Du kan gå tilbake og legge til nye periodeintervallene etter behov.</span><span class="sxs-lookup"><span data-stu-id="affaa-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="affaa-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="affaa-135">Close the page.</span></span>



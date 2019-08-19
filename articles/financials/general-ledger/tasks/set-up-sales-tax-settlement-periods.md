---
title: Definer mva-utligningsperioder
description: Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862994"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="ee64e-103">Definer mva-utligningsperioder</span><span class="sxs-lookup"><span data-stu-id="ee64e-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee64e-104">Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for.</span><span class="sxs-lookup"><span data-stu-id="ee64e-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="ee64e-105">En utligningsprosess kan kjøres for en utligningsperiode for et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="ee64e-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="ee64e-106">Alle mva-koder som er knyttet til utligningsperioden, blir utlignet.</span><span class="sxs-lookup"><span data-stu-id="ee64e-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="ee64e-107">Avhengig av oppsettet av den beslektede skattemyndigheten, posteres skattegjelden til en leverandør eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="ee64e-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="ee64e-108">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ee64e-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="ee64e-109">Gå til Avgift > Indirekte avgifter > Merverdiavgift > Mva-utligningsperioder.</span><span class="sxs-lookup"><span data-stu-id="ee64e-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="ee64e-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ee64e-110">Click New.</span></span>
3. <span data-ttu-id="ee64e-111">Angi en verdi i feltet Utligningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ee64e-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="ee64e-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ee64e-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ee64e-113">I Skattemyndighet-feltet velger du skattemyndigheten som skal motta rapportene og betalingene som er opprettet for utligningsperioden.</span><span class="sxs-lookup"><span data-stu-id="ee64e-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="ee64e-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ee64e-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ee64e-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ee64e-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ee64e-116">Klikk rullegardinknappen i Betalingsbetingelser-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ee64e-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ee64e-117">Den relaterte skattemyndigheten kan defineres som en leverandør og mva-utligningen oppretter en åpen leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="ee64e-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="ee64e-118">Betalingsbetingelsene definerer forfallsdatoen for den åpne leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="ee64e-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="ee64e-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ee64e-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ee64e-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ee64e-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ee64e-121">Velg en type for utligningsperiodeintervallet.</span><span class="sxs-lookup"><span data-stu-id="ee64e-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="ee64e-122">Angi antall enheter i periodeintervallet per periode.</span><span class="sxs-lookup"><span data-stu-id="ee64e-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="ee64e-123">Et kvartal har for eksempel 3 måneder.</span><span class="sxs-lookup"><span data-stu-id="ee64e-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="ee64e-124">Merk av eller fjern merket i avmerkingsboksen Bruk satsvis behandling for utligning av merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="ee64e-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="ee64e-125">Utligningsprosessen for utligningsperioden kan behandles som en satsvis jobb i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="ee64e-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="ee64e-126">Dette anbefales for et stort antall mva-transaksjoner i et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="ee64e-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="ee64e-127">For øyeblikket støttes ikke dette i Østerrike, Belgia, Spania, Italia, Japan og Nederland.</span><span class="sxs-lookup"><span data-stu-id="ee64e-127">Currently this is not supported in Austria, Belgium, Spain, Italy, Japan, and the Netherlands.</span></span>
14. <span data-ttu-id="ee64e-128">Merk eller fjern merket i avmerkingsboksen Hindre generering av transaksjoner for motregningsavgift.</span><span class="sxs-lookup"><span data-stu-id="ee64e-128">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="ee64e-129">Som standard genererer systemet transaksjoner for motregningsavgift under utligningsprosessen, som kan føre til ytelsesproblemer hvis det finnes et stort antall avgiftstransaksjoner i et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="ee64e-129">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="ee64e-130">Merk av i denne avmerkingsboksen for å hindre generering av transaksjoner for motregningsavgift.</span><span class="sxs-lookup"><span data-stu-id="ee64e-130">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="ee64e-131">Utvid kategorien Periodeintervaller.</span><span class="sxs-lookup"><span data-stu-id="ee64e-131">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="ee64e-132">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ee64e-132">Click Add.</span></span>
17. <span data-ttu-id="ee64e-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ee64e-133">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="ee64e-134">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee64e-134">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="ee64e-135">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee64e-135">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="ee64e-136">Klikk Nytt periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="ee64e-136">Click New period interval.</span></span>
    * <span data-ttu-id="ee64e-137">Når det første periodeintervallet er angitt, kan du opprette nye perioder automatisk.</span><span class="sxs-lookup"><span data-stu-id="ee64e-137">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="ee64e-138">Du kan gå tilbake og legge til nye periodeintervallene etter behov.</span><span class="sxs-lookup"><span data-stu-id="ee64e-138">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="ee64e-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ee64e-139">Close the page.</span></span>


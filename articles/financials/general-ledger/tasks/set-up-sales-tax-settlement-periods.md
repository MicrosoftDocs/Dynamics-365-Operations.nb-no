---
title: Definer mva-utligningsperioder
description: Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for.
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569592"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="bcb64-103">Definer mva-utligningsperioder</span><span class="sxs-lookup"><span data-stu-id="bcb64-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bcb64-104">Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for.</span><span class="sxs-lookup"><span data-stu-id="bcb64-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="bcb64-105">En utligningsprosess kan kjøres for en utligningsperiode for et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="bcb64-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="bcb64-106">Alle mva-koder som er knyttet til utligningsperioden, blir utlignet.</span><span class="sxs-lookup"><span data-stu-id="bcb64-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="bcb64-107">Avhengig av oppsettet av den beslektede skattemyndigheten, posteres skattegjelden til en leverandør eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="bcb64-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="bcb64-108">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="bcb64-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="bcb64-109">Gå til Avgift > Indirekte avgifter > Merverdiavgift > Mva-utligningsperioder.</span><span class="sxs-lookup"><span data-stu-id="bcb64-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="bcb64-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bcb64-110">Click New.</span></span>
3. <span data-ttu-id="bcb64-111">Angi en verdi i feltet Utligningsperiode.</span><span class="sxs-lookup"><span data-stu-id="bcb64-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="bcb64-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="bcb64-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bcb64-113">I Skattemyndighet-feltet velger du skattemyndigheten som skal motta rapportene og betalingene som er opprettet for utligningsperioden.</span><span class="sxs-lookup"><span data-stu-id="bcb64-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="bcb64-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bcb64-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="bcb64-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bcb64-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bcb64-116">Klikk rullegardinknappen i Betalingsbetingelser-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="bcb64-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bcb64-117">Den relaterte skattemyndigheten kan defineres som en leverandør og mva-utligningen oppretter en åpen leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="bcb64-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="bcb64-118">Betalingsbetingelsene definerer forfallsdatoen for den åpne leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="bcb64-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="bcb64-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bcb64-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="bcb64-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bcb64-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="bcb64-121">Velg en type for utligningsperiodeintervallet.</span><span class="sxs-lookup"><span data-stu-id="bcb64-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="bcb64-122">Angi antall enheter i periodeintervallet per periode.</span><span class="sxs-lookup"><span data-stu-id="bcb64-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="bcb64-123">Et kvartal har for eksempel 3 måneder.</span><span class="sxs-lookup"><span data-stu-id="bcb64-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="bcb64-124">Merk av eller fjern merket i avmerkingsboksen Bruk satsvis behandling for utligning av merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="bcb64-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="bcb64-125">Utligningsprosessen for utligningsperioden kan behandles som en satsvis jobb i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="bcb64-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="bcb64-126">Dette anbefales for et stort antall mva-transaksjoner i et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="bcb64-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="bcb64-127">Merk eller fjern merket i avmerkingsboksen Hindre generering av transaksjoner for motregningsavgift.</span><span class="sxs-lookup"><span data-stu-id="bcb64-127">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="bcb64-128">Som standard genererer systemet transaksjoner for motregningsavgift under utligningsprosessen, som kan føre til ytelsesproblemer hvis det finnes et stort antall avgiftstransaksjoner i et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="bcb64-128">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="bcb64-129">Merk av i denne avmerkingsboksen for å hindre generering av transaksjoner for motregningsavgift.</span><span class="sxs-lookup"><span data-stu-id="bcb64-129">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="bcb64-130">Utvid kategorien Periodeintervaller.</span><span class="sxs-lookup"><span data-stu-id="bcb64-130">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="bcb64-131">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bcb64-131">Click Add.</span></span>
17. <span data-ttu-id="bcb64-132">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bcb64-132">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="bcb64-133">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="bcb64-133">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="bcb64-134">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="bcb64-134">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="bcb64-135">Klikk Nytt periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="bcb64-135">Click New period interval.</span></span>
    * <span data-ttu-id="bcb64-136">Når det første periodeintervallet er angitt, kan du opprette nye perioder automatisk.</span><span class="sxs-lookup"><span data-stu-id="bcb64-136">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="bcb64-137">Du kan gå tilbake og legge til nye periodeintervallene etter behov.</span><span class="sxs-lookup"><span data-stu-id="bcb64-137">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="bcb64-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bcb64-138">Close the page.</span></span>


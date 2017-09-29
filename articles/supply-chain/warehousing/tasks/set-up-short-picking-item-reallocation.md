--- 
title: Definere ny tildeling av vare for plukking med mangler
description: "Denne fremgangsmåten viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b67965b6c8641b5d91ab3c5b0a7a7fd28a07cba6
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="82e55-103">Definere ny tildeling av vare for plukking med mangler</span><span class="sxs-lookup"><span data-stu-id="82e55-103">Set up short picking item reallocation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82e55-104">Denne fremgangsmåten viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til.</span><span class="sxs-lookup"><span data-stu-id="82e55-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="82e55-105">Det er mulig å bruke en automatisk prosess for ny tildeling, som bruker lokasjonsdirektiver til å hente varene hvis de er tilgjengelige på en annen lokasjon.</span><span class="sxs-lookup"><span data-stu-id="82e55-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="82e55-106">Når manuell ny tildeling brukes, vises også en liste over lokasjoner med det tilgjengelige antallet på den mobile enheten, noe som gjør at lagerarbeideren kan velge hvilken lokasjon som skal brukes for beholdningen.</span><span class="sxs-lookup"><span data-stu-id="82e55-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="82e55-107">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="82e55-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="82e55-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="82e55-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="82e55-109">Konfigurer arbeidsunntak</span><span class="sxs-lookup"><span data-stu-id="82e55-109">Set up work exceptions</span></span>
1. <span data-ttu-id="82e55-110">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsunntak.</span><span class="sxs-lookup"><span data-stu-id="82e55-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="82e55-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="82e55-111">Click New.</span></span>
    * <span data-ttu-id="82e55-112">Det er mulig å definere flere arbeidsunntak med ulike varetildelingspolicyer, slik at lagermedarbeideren kan velge én basert på behovene i forsendelsen de behandler.</span><span class="sxs-lookup"><span data-stu-id="82e55-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="82e55-113">Skriv inn en verdi i feltet Kode for arbeidsunntak.</span><span class="sxs-lookup"><span data-stu-id="82e55-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="82e55-114">Gi arbeidsunntaket en tittel for å angi hva den skal brukes til.</span><span class="sxs-lookup"><span data-stu-id="82e55-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="82e55-115">Eksempel: Plukking med mangler manuelt.</span><span class="sxs-lookup"><span data-stu-id="82e55-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="82e55-116">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="82e55-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82e55-117">Velg Plukk med mangler i Unntakstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="82e55-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="82e55-118">Merk av for Juster beholdning.</span><span class="sxs-lookup"><span data-stu-id="82e55-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="82e55-119">Dette alternativet betyr at lageret blir automatisk justert til 0 på lokasjonen med mangler.</span><span class="sxs-lookup"><span data-stu-id="82e55-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="82e55-120">Angi eller velg en verdi i feltet Standard justeringstypekode.</span><span class="sxs-lookup"><span data-stu-id="82e55-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="82e55-121">I USMF kan du for eksempel velge Remove Res Adj Out.</span><span class="sxs-lookup"><span data-stu-id="82e55-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="82e55-122">Velg Manuell i feltet Ny fordeling av vare.</span><span class="sxs-lookup"><span data-stu-id="82e55-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="82e55-123">Hvis du velger Manuell, eller Automatisk og Manuell, må lagermedarbeideren aktiveres for å bruke manuell ny tildeling.</span><span class="sxs-lookup"><span data-stu-id="82e55-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="82e55-124">Konfigurere en arbeider til å bruke manuell ny tildeling av vare</span><span class="sxs-lookup"><span data-stu-id="82e55-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="82e55-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82e55-125">Close the page.</span></span>
2. <span data-ttu-id="82e55-126">Gå til Lagerstyring > Oppsett > Arbeider.</span><span class="sxs-lookup"><span data-stu-id="82e55-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="82e55-127">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="82e55-127">Click Edit.</span></span>
4. <span data-ttu-id="82e55-128">Velg arbeider 24 i listen.</span><span class="sxs-lookup"><span data-stu-id="82e55-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="82e55-129">Utvid seksjonen Arbeid.</span><span class="sxs-lookup"><span data-stu-id="82e55-129">Expand the Work section.</span></span>
6. <span data-ttu-id="82e55-130">Velg Ja i feltet Tillat manuell ny tildeling av vare.</span><span class="sxs-lookup"><span data-stu-id="82e55-130">Select Yes in the Allow manual item reallocation field.</span></span>



---
title: Definere ny tildeling av vare for plukking med mangler
description: Dette emnet viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til.
author: ShylaThompson
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90aeb860dc95a348b000a0f994fadc5cc9aea7e6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814422"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="f9ad7-103">Definere ny tildeling av vare for plukking med mangler</span><span class="sxs-lookup"><span data-stu-id="f9ad7-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9ad7-104">Denne fremgangsmåten viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="f9ad7-105">Den nye tildelingsprosessen styres av et **arbeidsunntak** og brukes av **lagermedarbeideren.**</span><span class="sxs-lookup"><span data-stu-id="f9ad7-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="f9ad7-106">Det er mulig å bruke automatisk, manuell eller begge prosessene for ny tildeling:</span><span class="sxs-lookup"><span data-stu-id="f9ad7-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="f9ad7-107">Automatisk ny tildeling – lokasjonsdirektiver brukes til å fastslå om varene er tilgjengelige på en annen lokasjon.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="f9ad7-108">Hvis det er mulig, oppdateres arbeidet og lagerbrukeren blir dirigert til den alternative lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="f9ad7-109">Manuell ny tildeling – gjør at lagerbrukeren kan velge blant én eller flere lokasjoner med ikke-reservert antall varer.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="f9ad7-110">Automatisk og manuell – hvis systemet ikke klarer å utføre automatisk ny tildeling, og lokasjoner er tilgjengelige med ikke-reservert antall, blir brukeren bedt om å velge en lokasjon.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="f9ad7-111">Konfigurer arbeidsunntak</span><span class="sxs-lookup"><span data-stu-id="f9ad7-111">Set up work exceptions</span></span>
<span data-ttu-id="f9ad7-112">Det er mulig å definere flere arbeidsunntak med ulike varetildelingspolicyer, slik at lagermedarbeideren kan velge én basert på behovene i forsendelsen de behandler.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="f9ad7-113">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="f9ad7-114">I **navigasjonsruten** går du til **Lagerstyring > Oppsett > Arbeid > Arbeidsunntak**.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="f9ad7-115">Klikk på **Ny**</span><span class="sxs-lookup"><span data-stu-id="f9ad7-115">Click **New**</span></span> 
3. <span data-ttu-id="f9ad7-116">Skriv inn en verdi i feltet **Kode for arbeidsunntak**.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="f9ad7-117">Dette er tittelen på dette unntaket.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-117">This will be the title of this exception .</span></span> <span data-ttu-id="f9ad7-118">Eksempel: Plukking med mangler manuelt.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="f9ad7-119">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="f9ad7-120">Dette vil være en kort beskrivelse av bruken av dette unntaket.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="f9ad7-121">For eksempel Plukk med mangler – vare ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="f9ad7-122">Velg **Plukk med mangler** i **Unntakstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="f9ad7-123">Merk av for **Juster beholdning**.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="f9ad7-124">Hvis valg betyr det at lageret blir automatisk justert til 0 på lokasjonen med mangler.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="f9ad7-125">Angi eller velg en verdi i feltet **Standard justeringstypekode**.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="f9ad7-126">I USMF kan du for eksempel velge **Remove Res Adj Out**. Hver justeringstypekode inneholder fire karakteristikker: navn, beskrivelse, navn på lagerjournal og **Fjern reservasjoner**.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="f9ad7-127">Hvis **Fjern reservasjoner** er aktivert, vil reservasjonene for ordrelinjen med plukk med mangler.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="f9ad7-128">I **Ny tildeling av vare**-feltet velger du en verdi, som Manuell.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="f9ad7-129">Hvis du velger Manuell, eller Automatisk og Manuell, må lagermedarbeideren aktiveres for å bruke manuell ny tildeling.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="f9ad7-130">Konfigurere en arbeider til å bruke manuell ny tildeling av vare</span><span class="sxs-lookup"><span data-stu-id="f9ad7-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="f9ad7-131">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="f9ad7-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-132">Close the page.</span></span>
2. <span data-ttu-id="f9ad7-133">I **navigasjonsruten** går du til **Lagerstyring > Oppsett > Arbeider**.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="f9ad7-134">Klikk på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-134">Click **Edit**.</span></span>
4. <span data-ttu-id="f9ad7-135">Velg arbeider i listen.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-135">In the list, select worker.</span></span> <span data-ttu-id="f9ad7-136">For eksempel Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="f9ad7-137">Utvid **Brukere**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="f9ad7-138">Velg en **bruker-ID** i listen.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="f9ad7-139">For eksempel 24.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-139">For example, 24.</span></span>
7. <span data-ttu-id="f9ad7-140">Utvid **Arbeid**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="f9ad7-141">Velg **Ja** i feltet **Tillat manuell ny tildeling av vare**.</span><span class="sxs-lookup"><span data-stu-id="f9ad7-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
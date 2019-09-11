---
title: Definere en profil for vareankomstoversikt
description: Dette emnet fokuserer på oppsettet for en profil for ankomstoversikt.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1c6bcbb71f52e0ec5f979f8d79c896d10689a1b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867240"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="39684-103">Definere en profil for vareankomstoversikt</span><span class="sxs-lookup"><span data-stu-id="39684-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39684-104">Dette emnet fokuserer på oppsettet for en profil for ankomstoversikt.</span><span class="sxs-lookup"><span data-stu-id="39684-104">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="39684-105">Profil for ankomstoversikt er en samling av regler som skal brukes når en bruker åpner en side for ankomstoversikt.</span><span class="sxs-lookup"><span data-stu-id="39684-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="39684-106">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="39684-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="39684-107">Denne fremgangsmåten utføres vanligvis av en mottaksassistent.</span><span class="sxs-lookup"><span data-stu-id="39684-107">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="39684-108">I navigasjonsruten går du til **Moduler > Beholdningsstyring > Oppsett > Distribusjon > Profiler for ankomstoversikt**.</span><span class="sxs-lookup"><span data-stu-id="39684-108">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="39684-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="39684-109">Select **New**.</span></span> <span data-ttu-id="39684-110">Fordi du nesten alltid vil arbeide i det samme lageret med å laste ut fulle vognlass, bør du opprette en profil for ankomstoversikt for å forenkle prosessen med å registrere mottatte varer.</span><span class="sxs-lookup"><span data-stu-id="39684-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="39684-111">I feltet **Profilnavn for ankomstoversikt** skriver du inn en verdi.</span><span class="sxs-lookup"><span data-stu-id="39684-111">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="39684-112">Velg et alternativ i feltet **Vis linjer**.</span><span class="sxs-lookup"><span data-stu-id="39684-112">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="39684-113">Velg hvilke linjer som skal vises for mottaket:</span><span class="sxs-lookup"><span data-stu-id="39684-113">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="39684-114">**Alle** – Vis alle linjer uansett status.</span><span class="sxs-lookup"><span data-stu-id="39684-114">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="39684-115">**Pågår** – Vis linjer for mottak der fremdriften er fullstendig eller delvis.</span><span class="sxs-lookup"><span data-stu-id="39684-115">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="39684-116">Dette betyr at for hver linje er enten hele antallet eller et delantall registrert i en ankomstjournal.</span><span class="sxs-lookup"><span data-stu-id="39684-116">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="39684-117">**Ikke fullstendig** – Vis linjer for mottak der fremdriften er ingen eller delvis.</span><span class="sxs-lookup"><span data-stu-id="39684-117">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="39684-118">Dette betyr at for hver linje er enten ingen eller bare en del av antallet registrert i en ankomstjournal.</span><span class="sxs-lookup"><span data-stu-id="39684-118">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="39684-119">Vis eller skjul delen **Ankomstalternativer**.</span><span class="sxs-lookup"><span data-stu-id="39684-119">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="39684-120">Skriv inn en verdi i feltet **Dager fremover**.</span><span class="sxs-lookup"><span data-stu-id="39684-120">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="39684-121">Dette angir et filter som viser mottakslinjene som forventes å mottas i løpet av de neste dagene (avhengig av tallet du angir).</span><span class="sxs-lookup"><span data-stu-id="39684-121">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="39684-122">Skriv inn en verdi i feltet **Dager bakover**.</span><span class="sxs-lookup"><span data-stu-id="39684-122">In the **Days back** field, type a value.</span></span> <span data-ttu-id="39684-123">Dette angir et filter som viser linjene som forventes å mottas et antall dager før dagens dato.</span><span class="sxs-lookup"><span data-stu-id="39684-123">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="39684-124">Skriv inn en verdi i feltet **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="39684-124">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="39684-125">Filtrere på ett eller flere lagre.</span><span class="sxs-lookup"><span data-stu-id="39684-125">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="39684-126">Velg en verdi i **Leveringsmåte**-feltet.</span><span class="sxs-lookup"><span data-stu-id="39684-126">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="39684-127">Dette angir et filter for å vise bare mottakslinjene med denne leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="39684-127">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="39684-128">Velg WHS i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="39684-128">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="39684-129">Velg lager 24 i **Lager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="39684-129">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="39684-130">Dette er standardlageret som skal brukes for registrerte mottakslinjer som bruker denne profilen.</span><span class="sxs-lookup"><span data-stu-id="39684-130">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="39684-131">Velg **Rampedør** i **Lokasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="39684-131">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="39684-132">Dette er standardlokasjonen som skal brukes for registrerte mottakslinjer som bruker denne profilen.</span><span class="sxs-lookup"><span data-stu-id="39684-132">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="39684-133">Vis eller skjul delen **Detaljer om spørring etter ankomst**.</span><span class="sxs-lookup"><span data-stu-id="39684-133">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="39684-134">Velg område 2 i feltet **Begrens til område**.</span><span class="sxs-lookup"><span data-stu-id="39684-134">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="39684-135">Dette angir et filter for å vise bare mottakslinjene med dette området.</span><span class="sxs-lookup"><span data-stu-id="39684-135">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="39684-136">Sett alternativet **Bestillinger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="39684-136">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="39684-137">Velg mottakslinjer fra bestillinger.</span><span class="sxs-lookup"><span data-stu-id="39684-137">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="39684-138">Sett alternativet **Overføringsordrer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="39684-138">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="39684-139">Velg mottakslinjer fra overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="39684-139">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="39684-140">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="39684-140">Select **Save**.</span></span>
18. <span data-ttu-id="39684-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39684-141">Close the page.</span></span>


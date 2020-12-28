---
title: Definere en profil for vareankomstoversikt
description: Dette emnet fokuserer på oppsettet for en profil for ankomstoversikt.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69389dd3a53ffec11116e16512bd038b45eda4d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434666"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="2e619-103">Definere en profil for vareankomstoversikt</span><span class="sxs-lookup"><span data-stu-id="2e619-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="2e619-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="2e619-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="2e619-105">Dette emnet fokuserer på oppsettet for en profil for ankomstoversikt.</span><span class="sxs-lookup"><span data-stu-id="2e619-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="2e619-106">Profil for ankomstoversikt er en samling av regler som skal brukes når en bruker åpner en side for ankomstoversikt.</span><span class="sxs-lookup"><span data-stu-id="2e619-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="2e619-107">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="2e619-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="2e619-108">Denne fremgangsmåten utføres vanligvis av en mottaksassistent.</span><span class="sxs-lookup"><span data-stu-id="2e619-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="2e619-109">I navigasjonsruten går du til **Moduler > Beholdningsstyring > Oppsett > Distribusjon > Profiler for ankomstoversikt**.</span><span class="sxs-lookup"><span data-stu-id="2e619-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="2e619-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2e619-110">Select **New**.</span></span> <span data-ttu-id="2e619-111">Fordi du nesten alltid vil arbeide i det samme lageret med å laste ut fulle vognlass, bør du opprette en profil for ankomstoversikt for å forenkle prosessen med å registrere mottatte varer.</span><span class="sxs-lookup"><span data-stu-id="2e619-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="2e619-112">I feltet **Profilnavn for ankomstoversikt** skriver du inn en verdi.</span><span class="sxs-lookup"><span data-stu-id="2e619-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="2e619-113">Velg et alternativ i feltet **Vis linjer**.</span><span class="sxs-lookup"><span data-stu-id="2e619-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="2e619-114">Velg hvilke linjer som skal vises for mottaket:</span><span class="sxs-lookup"><span data-stu-id="2e619-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="2e619-115">**Alle** – Vis alle linjer uansett status.</span><span class="sxs-lookup"><span data-stu-id="2e619-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="2e619-116">**Pågår** – Vis linjer for mottak der fremdriften er fullstendig eller delvis.</span><span class="sxs-lookup"><span data-stu-id="2e619-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="2e619-117">Dette betyr at for hver linje er enten hele antallet eller et delantall registrert i en ankomstjournal.</span><span class="sxs-lookup"><span data-stu-id="2e619-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="2e619-118">**Ikke fullstendig** – Vis linjer for mottak der fremdriften er ingen eller delvis.</span><span class="sxs-lookup"><span data-stu-id="2e619-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="2e619-119">Dette betyr at for hver linje er enten ingen eller bare en del av antallet registrert i en ankomstjournal.</span><span class="sxs-lookup"><span data-stu-id="2e619-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="2e619-120">Vis eller skjul delen **Ankomstalternativer**.</span><span class="sxs-lookup"><span data-stu-id="2e619-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="2e619-121">Skriv inn en verdi i feltet **Dager fremover**.</span><span class="sxs-lookup"><span data-stu-id="2e619-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="2e619-122">Dette angir et filter som viser mottakslinjene som forventes å mottas i løpet av de neste dagene (avhengig av tallet du angir).</span><span class="sxs-lookup"><span data-stu-id="2e619-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="2e619-123">Skriv inn en verdi i feltet **Dager bakover**.</span><span class="sxs-lookup"><span data-stu-id="2e619-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="2e619-124">Dette angir et filter som viser linjene som forventes å mottas et antall dager før dagens dato.</span><span class="sxs-lookup"><span data-stu-id="2e619-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="2e619-125">Skriv inn en verdi i feltet **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2e619-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="2e619-126">Filtrere på ett eller flere lagre.</span><span class="sxs-lookup"><span data-stu-id="2e619-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="2e619-127">Velg en verdi i **Leveringsmåte**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e619-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="2e619-128">Dette angir et filter for å vise bare mottakslinjene med denne leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="2e619-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="2e619-129">Velg WHS i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e619-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="2e619-130">Velg lager 24 i **Lager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e619-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="2e619-131">Dette er standardlageret som skal brukes for registrerte mottakslinjer som bruker denne profilen.</span><span class="sxs-lookup"><span data-stu-id="2e619-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="2e619-132">Velg **Rampedør** i **Lokasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e619-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="2e619-133">Dette er standardlokasjonen som skal brukes for registrerte mottakslinjer som bruker denne profilen.</span><span class="sxs-lookup"><span data-stu-id="2e619-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="2e619-134">Vis eller skjul delen **Detaljer om spørring etter ankomst**.</span><span class="sxs-lookup"><span data-stu-id="2e619-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="2e619-135">Velg område 2 i feltet **Begrens til område**.</span><span class="sxs-lookup"><span data-stu-id="2e619-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="2e619-136">Dette angir et filter for å vise bare mottakslinjene med dette området.</span><span class="sxs-lookup"><span data-stu-id="2e619-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="2e619-137">Sett alternativet **Bestillinger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2e619-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="2e619-138">Velg mottakslinjer fra bestillinger.</span><span class="sxs-lookup"><span data-stu-id="2e619-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="2e619-139">Sett alternativet **Overføringsordrer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2e619-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="2e619-140">Velg mottakslinjer fra overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="2e619-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="2e619-141">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2e619-141">Select **Save**.</span></span>
18. <span data-ttu-id="2e619-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2e619-142">Close the page.</span></span>


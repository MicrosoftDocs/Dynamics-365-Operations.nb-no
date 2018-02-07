---
title: Definere en profil for vareankomstoversikt
description: "Denne oppgaven fokuserer på oppsettet for en profil for ankomstoversikt."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ddc491d73bbb6ac02e37a9c9b9d93545f6f9556
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="d8c9a-103">Definere en profil for vareankomstoversikt</span><span class="sxs-lookup"><span data-stu-id="d8c9a-103">Set up an item arrival overview profile</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8c9a-104">Denne oppgaven fokuserer på oppsettet for en profil for ankomstoversikt.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="d8c9a-105">Profil for ankomstoversikt er en samling av regler som skal brukes når en bruker åpner en side for ankomstoversikt.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="d8c9a-106">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="d8c9a-107">Denne fremgangsmåten utføres vanligvis av en mottaksassistent.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="d8c9a-108">Gå til Lagerstyring > Oppsett > Distribusjon > Profiler for ankomstoversikt.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="d8c9a-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-109">Click New.</span></span>
    * <span data-ttu-id="d8c9a-110">Fordi du nesten alltid vil arbeide i det samme lageret med å laste ut fulle vognlass, bør du opprette en profil for ankomstoversikt for å forenkle prosessen med å registrere mottatte varer.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="d8c9a-111">I feltet Profilnavn for ankomstoversikt skriver du inn en verdi.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="d8c9a-112">Velg et alternativ i feltet Vis linjer.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="d8c9a-113">Velg hvilke linjer som skal vises for mottaket: Alle – Vis alle linjer uansett status.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="d8c9a-114">Pågår – Vis linjer for mottak der fremdriften er fullstendig eller delvis.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="d8c9a-115">Dette betyr at for hver linje er enten hele antallet eller et delantall registrert i en ankomstjournal.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="d8c9a-116">Ikke fullstendig – Vis linjer for mottak der fremdriften er ingen eller delvis.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="d8c9a-117">Dette betyr at for hver linje er enten ingen eller bare en del av antallet registrert i en ankomstjournal.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="d8c9a-118">Vis eller skjul delen Ankomstalternativer.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="d8c9a-119">Skriv inn en verdi i feltet Dager fremover.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="d8c9a-120">Dette angir et filter som viser mottakslinjene som forventes å mottas i løpet av de neste dagene (avhengig av tallet du angir).</span><span class="sxs-lookup"><span data-stu-id="d8c9a-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="d8c9a-121">Skriv inn en verdi i feltet Dager bakover.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="d8c9a-122">Dette angir et filter som viser linjene som forventes å mottas et antall dager før dagens dato.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="d8c9a-123">Skriv inn en verdi i feltet Lagre.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="d8c9a-124">Filtrere på ett eller flere lagre.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="d8c9a-125">Velg en verdi i Leveringsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="d8c9a-126">Dette angir et filter for å vise bare mottakslinjene med denne leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="d8c9a-127">Velg WHS i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="d8c9a-128">Velg lager 24 i Lager-feltet.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="d8c9a-129">Dette er standardlageret som skal brukes for registrerte mottakslinjer som bruker denne profilen.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="d8c9a-130">Velg Rampedør i Lokasjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="d8c9a-131">Dette er standardlokasjonen som skal brukes for registrerte mottakslinjer som bruker denne profilen.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="d8c9a-132">Vis eller skjul delen Detaljer om spørring etter ankomst.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="d8c9a-133">Velg område 2 i feltet Begrens til område.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="d8c9a-134">Dette angir et filter for å vise bare mottakslinjene med dette området.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="d8c9a-135">Sett alternativet Bestillinger til Ja.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="d8c9a-136">Velg mottakslinjer fra bestillinger.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="d8c9a-137">Sett alternativet Overføringsordrer til Ja.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="d8c9a-138">Velg mottakslinjer fra overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="d8c9a-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-139">Click Save.</span></span>
18. <span data-ttu-id="d8c9a-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-140">Close the page.</span></span>


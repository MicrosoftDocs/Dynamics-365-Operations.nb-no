--- 
title: "Konfigurere økonomisk datadeling mellom firmaer"
description: "Denne fremgangsmåten viser hvordan du konfigurerer, aktiverer, validerer og løser konflikter ved deling av data mellom firmaer."
author: aprilolson
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 547e5d82defbf004335e1c5fcd5e2cd7013e1b63
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="dc0cd-103">Konfigurere økonomisk datadeling mellom firmaer</span><span class="sxs-lookup"><span data-stu-id="dc0cd-103">Configure financial cross-company data sharing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc0cd-104">Denne fremgangsmåten viser hvordan du konfigurerer, aktiverer, validerer og løser konflikter ved deling av data mellom firmaer.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="dc0cd-105">Den bruker USMF-firmaet og malen for deling av økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="dc0cd-106">Denne oppgaveveiledningen krever Dynamics AX-plattform 7.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="dc0cd-107">Gå til Systemadministrasjon > Arbeidsområder > Databehandling.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="dc0cd-108">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-108">Click Import.</span></span>
3. <span data-ttu-id="dc0cd-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dc0cd-110">Velg pakketype i feltet Kildedataformat.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="dc0cd-111">Klikk Last opp.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-111">Click Upload.</span></span> <span data-ttu-id="dc0cd-112">Gå til plasseringen til malpakkefilen for deling av økonomiske data, og velg filen.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="dc0cd-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-113">Click Save.</span></span>
6. <span data-ttu-id="dc0cd-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dc0cd-115">Velg datadelingspolicyen som nettopp ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="dc0cd-116">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-116">Click Import.</span></span>
8. <span data-ttu-id="dc0cd-117">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-117">Click Close.</span></span>
9. <span data-ttu-id="dc0cd-118">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-118">Refresh the page.</span></span>
10. <span data-ttu-id="dc0cd-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-119">Close the page.</span></span>
11. <span data-ttu-id="dc0cd-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-120">Close the page.</span></span>
12. <span data-ttu-id="dc0cd-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-121">Close the page.</span></span>
13. <span data-ttu-id="dc0cd-122">Gå til Systemadministrasjon > Oppsett > Konfigurer datadeling mellom firmaer.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="dc0cd-123">Finn og velg Betalingsdager i listen.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="dc0cd-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-124">Click Add.</span></span>
16. <span data-ttu-id="dc0cd-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="dc0cd-126">Skriv USSI i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="dc0cd-127">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-127">Click Add.</span></span>
19. <span data-ttu-id="dc0cd-128">Skriv USMF i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="dc0cd-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-129">Click Save.</span></span>
21. <span data-ttu-id="dc0cd-130">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-130">Click Enable.</span></span>
22. <span data-ttu-id="dc0cd-131">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-131">Click Yes.</span></span>
23. <span data-ttu-id="dc0cd-132">Klikk Finn delingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="dc0cd-133">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-133">Click Yes.</span></span>
25. <span data-ttu-id="dc0cd-134">Klikk Oppdater feltverdi.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-134">Click Update field value.</span></span>
26. <span data-ttu-id="dc0cd-135">Klikk Bruk verdi fra firma 1.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="dc0cd-136">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-136">Refresh the page.</span></span>
28. <span data-ttu-id="dc0cd-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dc0cd-137">Close the page.</span></span>



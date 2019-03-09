---
title: Konfigurere økonomisk datadeling mellom firmaer
description: Denne fremgangsmåten viser hvordan du konfigurerer, aktiverer, validerer og løser konflikter ved deling av data mellom firmaer.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 784a925fa06148cad780b494c88b9a7af1809c9d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "357847"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="c23c0-103">Konfigurere økonomisk datadeling mellom firmaer</span><span class="sxs-lookup"><span data-stu-id="c23c0-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c23c0-104">Denne fremgangsmåten viser hvordan du konfigurerer, aktiverer, validerer og løser konflikter ved deling av data mellom firmaer.</span><span class="sxs-lookup"><span data-stu-id="c23c0-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="c23c0-105">Den bruker USMF-firmaet og malen for deling av økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="c23c0-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="c23c0-106">Denne oppgaveveiledningen krever Dynamics AX-plattform 7.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="c23c0-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="c23c0-107">Gå til Systemadministrasjon > Arbeidsområder > Databehandling.</span><span class="sxs-lookup"><span data-stu-id="c23c0-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="c23c0-108">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="c23c0-108">Click Import.</span></span>
3. <span data-ttu-id="c23c0-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="c23c0-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c23c0-110">Velg pakketype i feltet Kildedataformat.</span><span class="sxs-lookup"><span data-stu-id="c23c0-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="c23c0-111">Klikk Last opp.</span><span class="sxs-lookup"><span data-stu-id="c23c0-111">Click Upload.</span></span> <span data-ttu-id="c23c0-112">Gå til plasseringen til malpakkefilen for deling av økonomiske data, og velg filen.</span><span class="sxs-lookup"><span data-stu-id="c23c0-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="c23c0-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c23c0-113">Click Save.</span></span>
6. <span data-ttu-id="c23c0-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c23c0-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c23c0-115">Velg datadelingspolicyen som nettopp ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="c23c0-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="c23c0-116">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="c23c0-116">Click Import.</span></span>
8. <span data-ttu-id="c23c0-117">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="c23c0-117">Click Close.</span></span>
9. <span data-ttu-id="c23c0-118">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="c23c0-118">Refresh the page.</span></span>
10. <span data-ttu-id="c23c0-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c23c0-119">Close the page.</span></span>
11. <span data-ttu-id="c23c0-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c23c0-120">Close the page.</span></span>
12. <span data-ttu-id="c23c0-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c23c0-121">Close the page.</span></span>
13. <span data-ttu-id="c23c0-122">Gå til Systemadministrasjon > Oppsett > Konfigurer datadeling mellom firmaer.</span><span class="sxs-lookup"><span data-stu-id="c23c0-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="c23c0-123">Finn og velg Betalingsdager i listen.</span><span class="sxs-lookup"><span data-stu-id="c23c0-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="c23c0-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="c23c0-124">Click Add.</span></span>
16. <span data-ttu-id="c23c0-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c23c0-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="c23c0-126">Skriv USSI i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="c23c0-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="c23c0-127">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="c23c0-127">Click Add.</span></span>
19. <span data-ttu-id="c23c0-128">Skriv USMF i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="c23c0-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="c23c0-129">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c23c0-129">Click Save.</span></span>
21. <span data-ttu-id="c23c0-130">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="c23c0-130">Click Enable.</span></span>
22. <span data-ttu-id="c23c0-131">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="c23c0-131">Click Yes.</span></span>
23. <span data-ttu-id="c23c0-132">Klikk Finn delingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="c23c0-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="c23c0-133">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="c23c0-133">Click Yes.</span></span>
25. <span data-ttu-id="c23c0-134">Klikk Oppdater feltverdi.</span><span class="sxs-lookup"><span data-stu-id="c23c0-134">Click Update field value.</span></span>
26. <span data-ttu-id="c23c0-135">Klikk Bruk verdi fra firma 1.</span><span class="sxs-lookup"><span data-stu-id="c23c0-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="c23c0-136">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="c23c0-136">Refresh the page.</span></span>
28. <span data-ttu-id="c23c0-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c23c0-137">Close the page.</span></span>


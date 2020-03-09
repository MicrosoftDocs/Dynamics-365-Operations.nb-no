---
title: " Opprette og tilknytte en maskinvarestasjon"
description: Denne prosedyren hjelper med å opprette en ny maskinvarestasjon.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 772ccc44c01d97a07796bd1ee443012448955f49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023551"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="9ed23-103"> Opprette og tilknytte en maskinvarestasjon</span><span class="sxs-lookup"><span data-stu-id="9ed23-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9ed23-104">Denne prosedyren hjelper med å opprette en ny maskinvarestasjon.</span><span class="sxs-lookup"><span data-stu-id="9ed23-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="9ed23-105">En ny maskinvareprofil opprettes og brukes til å legge til nye maskinvarestasjoner i en forhåndsdefinert butikk (kanal).</span><span class="sxs-lookup"><span data-stu-id="9ed23-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="9ed23-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="9ed23-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9ed23-107">Gå til Grunnleggende om handel > Kanaler > ..</span><span class="sxs-lookup"><span data-stu-id="9ed23-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="9ed23-108">> ..</span><span class="sxs-lookup"><span data-stu-id="9ed23-108">> ..</span></span> <span data-ttu-id="9ed23-109">> ..</span><span class="sxs-lookup"><span data-stu-id="9ed23-109">> ..</span></span> <span data-ttu-id="9ed23-110">> Profiler for maskinvarestasjon.</span><span class="sxs-lookup"><span data-stu-id="9ed23-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="9ed23-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9ed23-111">Click New.</span></span>
3. <span data-ttu-id="9ed23-112">Skriv inn TestHWProfile i feltet Maskinvarestasjon-ID.</span><span class="sxs-lookup"><span data-stu-id="9ed23-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="9ed23-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9ed23-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9ed23-114">Angi et tall i feltet Portnummer.</span><span class="sxs-lookup"><span data-stu-id="9ed23-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="9ed23-115">Klikk rullegardinknappen i Maskinvareprofil-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9ed23-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9ed23-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9ed23-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9ed23-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9ed23-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9ed23-118">Klikk rullegardinknappen i feltet Pakkenavn for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9ed23-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="9ed23-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9ed23-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9ed23-120">Dette er standardpakken som følger med et nytt miljø.</span><span class="sxs-lookup"><span data-stu-id="9ed23-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="9ed23-121">Versjonsnummeret kan variere.</span><span class="sxs-lookup"><span data-stu-id="9ed23-121">The version number may vary.</span></span>  
11. <span data-ttu-id="9ed23-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9ed23-122">Click Save.</span></span>
12. <span data-ttu-id="9ed23-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9ed23-123">Close the page.</span></span>
13. <span data-ttu-id="9ed23-124">Gå til Retail og Commerce > Kanaler > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="9ed23-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="9ed23-125">Velg rad 17 i listen.</span><span class="sxs-lookup"><span data-stu-id="9ed23-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="9ed23-126">Hvis du bruker demonstrasjonsdatafirmaet USRT, er dette Houston-butikken.</span><span class="sxs-lookup"><span data-stu-id="9ed23-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="9ed23-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9ed23-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="9ed23-128">Aktiver/deaktiver utvidelsen av delen Maskinvarestasjoner.</span><span class="sxs-lookup"><span data-stu-id="9ed23-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="9ed23-129">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="9ed23-129">Click Add.</span></span>
18. <span data-ttu-id="9ed23-130">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9ed23-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="9ed23-131">Klikk rullegardinknappen i feltet Profil-ID for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9ed23-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="9ed23-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9ed23-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9ed23-133">Dette må være den nye maskinvarestasjonsprofilen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="9ed23-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="9ed23-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9ed23-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="9ed23-135">Skriv inn en verdi i feltet Vertsnavn.</span><span class="sxs-lookup"><span data-stu-id="9ed23-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="9ed23-136">Skriv inn en verdi i feltet EFT-terminal-ID.</span><span class="sxs-lookup"><span data-stu-id="9ed23-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="9ed23-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9ed23-137">Click Save.</span></span>

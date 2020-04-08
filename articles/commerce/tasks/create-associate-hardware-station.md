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
ms.openlocfilehash: 305308b0e4ba99aae4bf6f8f94041db570a25893
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141043"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="4d37b-103"> Opprette og tilknytte en maskinvarestasjon</span><span class="sxs-lookup"><span data-stu-id="4d37b-103">Create and associate a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d37b-104">Denne prosedyren hjelper med å opprette en ny maskinvarestasjon.</span><span class="sxs-lookup"><span data-stu-id="4d37b-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="4d37b-105">En ny maskinvareprofil opprettes og brukes til å legge til nye maskinvarestasjoner i en forhåndsdefinert butikk (kanal).</span><span class="sxs-lookup"><span data-stu-id="4d37b-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="4d37b-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="4d37b-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4d37b-107">Gå til Grunnleggende om handel > Kanaler > ..</span><span class="sxs-lookup"><span data-stu-id="4d37b-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="4d37b-108">> ..</span><span class="sxs-lookup"><span data-stu-id="4d37b-108">> ..</span></span> <span data-ttu-id="4d37b-109">> ..</span><span class="sxs-lookup"><span data-stu-id="4d37b-109">> ..</span></span> <span data-ttu-id="4d37b-110">> Profiler for maskinvarestasjon.</span><span class="sxs-lookup"><span data-stu-id="4d37b-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="4d37b-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4d37b-111">Click New.</span></span>
3. <span data-ttu-id="4d37b-112">Skriv inn TestHWProfile i feltet Maskinvarestasjon-ID.</span><span class="sxs-lookup"><span data-stu-id="4d37b-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="4d37b-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d37b-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4d37b-114">Angi et tall i feltet Portnummer.</span><span class="sxs-lookup"><span data-stu-id="4d37b-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="4d37b-115">Klikk rullegardinknappen i Maskinvareprofil-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4d37b-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4d37b-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4d37b-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="4d37b-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4d37b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="4d37b-118">Klikk rullegardinknappen i feltet Pakkenavn for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4d37b-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="4d37b-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4d37b-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4d37b-120">Dette er standardpakken som følger med et nytt miljø.</span><span class="sxs-lookup"><span data-stu-id="4d37b-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="4d37b-121">Versjonsnummeret kan variere.</span><span class="sxs-lookup"><span data-stu-id="4d37b-121">The version number may vary.</span></span>  
11. <span data-ttu-id="4d37b-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4d37b-122">Click Save.</span></span>
12. <span data-ttu-id="4d37b-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4d37b-123">Close the page.</span></span>
13. <span data-ttu-id="4d37b-124">Gå til Retail og Commerce > Kanaler > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="4d37b-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="4d37b-125">Velg rad 17 i listen.</span><span class="sxs-lookup"><span data-stu-id="4d37b-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="4d37b-126">Hvis du bruker demonstrasjonsdatafirmaet USRT, er dette Houston-butikken.</span><span class="sxs-lookup"><span data-stu-id="4d37b-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="4d37b-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4d37b-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="4d37b-128">Aktiver/deaktiver utvidelsen av delen Maskinvarestasjoner.</span><span class="sxs-lookup"><span data-stu-id="4d37b-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="4d37b-129">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4d37b-129">Click Add.</span></span>
18. <span data-ttu-id="4d37b-130">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4d37b-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="4d37b-131">Klikk rullegardinknappen i feltet Profil-ID for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4d37b-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="4d37b-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4d37b-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4d37b-133">Dette må være den nye maskinvarestasjonsprofilen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="4d37b-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="4d37b-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4d37b-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="4d37b-135">Skriv inn en verdi i feltet Vertsnavn.</span><span class="sxs-lookup"><span data-stu-id="4d37b-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="4d37b-136">Skriv inn en verdi i feltet EFT-terminal-ID.</span><span class="sxs-lookup"><span data-stu-id="4d37b-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="4d37b-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4d37b-137">Click Save.</span></span>


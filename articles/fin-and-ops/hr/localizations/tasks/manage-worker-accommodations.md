--- 
title: Behandle arbeidertilpassinger
description: "Denne fremgangsmåten går gjennom trinnene for å definere tilpasningstyper for arbeidsmiljø, for eksempel ergonomiske stoler eller periodiske pauser."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 10d34d0b2eca95034d1f67931ff72a035be9a6b8
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="manage-worker-accommodations"></a><span data-ttu-id="65e13-103">Behandle arbeidertilpassinger</span><span class="sxs-lookup"><span data-stu-id="65e13-103">Manage worker accommodations</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="65e13-104">Denne fremgangsmåten går gjennom trinnene for å definere tilpasningstyper for arbeidsmiljø, for eksempel ergonomiske stoler eller periodiske pauser.</span><span class="sxs-lookup"><span data-stu-id="65e13-104">This procedure walks through the steps for setting up work environment accommodation types, such as ergonomic chairs or periodic breaks.</span></span> <span data-ttu-id="65e13-105">Den viser også hvordan du tilordner disse tilpasningstyper til en arbeider, og enten godkjenner eller avviser tilpasningstypen.</span><span class="sxs-lookup"><span data-stu-id="65e13-105">It also shows how to assign these accommodation types to a worker, and either approve or deny the accommodation type.</span></span> <span data-ttu-id="65e13-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="65e13-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="setup-accommodations"></a><span data-ttu-id="65e13-107">Definer tilpasninger</span><span class="sxs-lookup"><span data-stu-id="65e13-107">Setup accommodations</span></span>
1. <span data-ttu-id="65e13-108">Gå til Personale > Oppsett > Tilpasningstyper.</span><span class="sxs-lookup"><span data-stu-id="65e13-108">Go to Human resources > Setup > Accommodation types.</span></span>
2. <span data-ttu-id="65e13-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="65e13-109">Click New.</span></span>
3. <span data-ttu-id="65e13-110">I Tilpasningstype-feltet angir du et navn på tilpasningen.</span><span class="sxs-lookup"><span data-stu-id="65e13-110">In the Accommodation type field, enter a name for the accommodation.</span></span> <span data-ttu-id="65e13-111">Eksempel: tastatur.</span><span class="sxs-lookup"><span data-stu-id="65e13-111">Example: Keyboard.</span></span>
4. <span data-ttu-id="65e13-112">I Beskrivelse-feltet skriver du inn en beskrivelse for tilpasningen.</span><span class="sxs-lookup"><span data-stu-id="65e13-112">In the Description field, enter a description for the accommodation.</span></span> <span data-ttu-id="65e13-113">Eksempel: Ergonomisk tastatur.</span><span class="sxs-lookup"><span data-stu-id="65e13-113">Example: Ergonomic Keyboard.</span></span>
5. <span data-ttu-id="65e13-114">Angi informasjon som hjelper deg med å klargjøre tilpasningen i Merknad-feltet.</span><span class="sxs-lookup"><span data-stu-id="65e13-114">In the Note field, enter any information that helps to clarify the accommodation.</span></span>
6. <span data-ttu-id="65e13-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="65e13-115">Click Save.</span></span>
7. <span data-ttu-id="65e13-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65e13-116">Close the page.</span></span>

## <a name="assign-accommodations"></a><span data-ttu-id="65e13-117">Tilordne tilpasninger</span><span class="sxs-lookup"><span data-stu-id="65e13-117">Assign accommodations</span></span>
1. <span data-ttu-id="65e13-118">Gå til Personale > Arbeidere > Ansatte.</span><span class="sxs-lookup"><span data-stu-id="65e13-118">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="65e13-119">Velg en ansatt fra listen.</span><span class="sxs-lookup"><span data-stu-id="65e13-119">From the list, select an employee.</span></span>
3. <span data-ttu-id="65e13-120">Klikk navnet på den ansatte for å vise detaljer om ansatt som ber om tilpasningen.</span><span class="sxs-lookup"><span data-stu-id="65e13-120">Click the employee's name to view details about the employee who is requesting the accommodation.</span></span>
4. <span data-ttu-id="65e13-121">Utvid hurtigkategorien Personlig informasjon.</span><span class="sxs-lookup"><span data-stu-id="65e13-121">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="65e13-122">Klikk Tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="65e13-122">Click Accommodations.</span></span>
6. <span data-ttu-id="65e13-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="65e13-123">Click New.</span></span>
7. <span data-ttu-id="65e13-124">Velg den aktuelle tilpasningen i feltet Tilpasningstype.</span><span class="sxs-lookup"><span data-stu-id="65e13-124">In the Accommodation type field, select the appropriate accommodation.</span></span> <span data-ttu-id="65e13-125">Eksempel: tastatur</span><span class="sxs-lookup"><span data-stu-id="65e13-125">Example: Keyboard</span></span>
8. <span data-ttu-id="65e13-126">I feltet Jobboppgave angir du arbeidsoppgaven som krever tilpasning.</span><span class="sxs-lookup"><span data-stu-id="65e13-126">In the Job task field, enter the work task that requires the accommodation.</span></span>
9. <span data-ttu-id="65e13-127">I Status-feltet angir du den aktuelle statusen.</span><span class="sxs-lookup"><span data-stu-id="65e13-127">In the Status field, enter the appropriate status.</span></span> <span data-ttu-id="65e13-128">Eksempel: rimelig</span><span class="sxs-lookup"><span data-stu-id="65e13-128">Example: Reasonable</span></span>
    * <span data-ttu-id="65e13-129">Følgende statuser er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="65e13-129">The following statuses are available.</span></span> <span data-ttu-id="65e13-130">Forespurt angir at tilpasningen er opprettet, men ennå ikke er gjennomgått.</span><span class="sxs-lookup"><span data-stu-id="65e13-130">Requested indicates that the accommodation has been created but not yet reviewed.</span></span> <span data-ttu-id="65e13-131">Rimelig angir at tilpasningen er rimelig og skal gis.</span><span class="sxs-lookup"><span data-stu-id="65e13-131">Reasonable indicates that the accommodation is reasonable and will be granted.</span></span> <span data-ttu-id="65e13-132">Med overlast angir at tilpasningen vil plassere en uforholdsmessige belastning på arbeidsgiver og er avslått.</span><span class="sxs-lookup"><span data-stu-id="65e13-132">Undue hardship indicates that the accommodation will place an unreasonable burden on the employer, and has been denied.</span></span> <span data-ttu-id="65e13-133">I dette eksemplet ble forespørselen umiddelbart godkjent fordi forespørselen om tilpasning var minimal.</span><span class="sxs-lookup"><span data-stu-id="65e13-133">In this example, the request was approved immediately because the accommodation request was minimal.</span></span>  
10. <span data-ttu-id="65e13-134">I feltet Godkjent velger du personen som godtok forespørselen om tilpasning.</span><span class="sxs-lookup"><span data-stu-id="65e13-134">In the Accepted field, select the person who accepted the accommodation request.</span></span>
11. <span data-ttu-id="65e13-135">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="65e13-135">Click Select.</span></span>
12. <span data-ttu-id="65e13-136">Angi datoen og klokkeslettet da forespørselen om tilpasning ble godtatt i feltet Dato og klokkeslett for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="65e13-136">In the Accepted date field, enter the date and time when the accommodation request was accepted.</span></span>
13. <span data-ttu-id="65e13-137">Utvid merknadsdelen.</span><span class="sxs-lookup"><span data-stu-id="65e13-137">Expand the Note section.</span></span>
14. <span data-ttu-id="65e13-138">Angi informasjon eller ressurskostnader som bidrar til å klargjøre virkningen av tilpasningen, i feltet Økonomisk.</span><span class="sxs-lookup"><span data-stu-id="65e13-138">In the Financial field, enter any information or resource costs that helps to clarify the impact of the accommodation.</span></span>
    * <span data-ttu-id="65e13-139">Hvis tilpasning er avslått, kan Svar-feltet brukes til å angi hvorfor en forespørsel ble avvist.</span><span class="sxs-lookup"><span data-stu-id="65e13-139">If the accommodation has been denied, the Reply field can be used to indicate why a request was denied.</span></span>  
15. <span data-ttu-id="65e13-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="65e13-140">Click Save.</span></span>



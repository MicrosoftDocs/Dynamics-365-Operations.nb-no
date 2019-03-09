---
title: Definere en arbeidsmal for bestillinger
description: Denne prosedyren fokuserer på oppsettet for enkel arbeidsmal for som skal brukes når du plasserer mottatte varer.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d737f9dfd1888602266a87853e54407618ae2781
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "318034"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="227a9-103">Definere en arbeidsmal for bestillinger</span><span class="sxs-lookup"><span data-stu-id="227a9-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="227a9-104">Denne prosedyren fokuserer på oppsettet for enkel arbeidsmal for som skal brukes når du plasserer mottatte varer.</span><span class="sxs-lookup"><span data-stu-id="227a9-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="227a9-105">Arbeidsmaler bestemmer settet med instruksjoner som presenteres for lagermedarbeideren på en mobil enhet når de flytter varer fra mottaksområdet.</span><span class="sxs-lookup"><span data-stu-id="227a9-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="227a9-106">Du kan bruke denne fremgangsmåten med data som er nevnt i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="227a9-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="227a9-107">Før du starter denne veiledningen kan du opprette en arbeidspulje-ID.</span><span class="sxs-lookup"><span data-stu-id="227a9-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="227a9-108">I dette eksemplet brukes en arbeidpulje-ID kalt Innkommende.</span><span class="sxs-lookup"><span data-stu-id="227a9-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="227a9-109">Denne fremgangsmåten er ment for lagersjef.</span><span class="sxs-lookup"><span data-stu-id="227a9-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="227a9-110">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.</span><span class="sxs-lookup"><span data-stu-id="227a9-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="227a9-111">Velg Bestillinger i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="227a9-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="227a9-112">Opprette et arbeidsmalhode</span><span class="sxs-lookup"><span data-stu-id="227a9-112">Create a work template header</span></span>
1. <span data-ttu-id="227a9-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="227a9-113">Click New.</span></span>
2. <span data-ttu-id="227a9-114">Angi et nummer i Sekvensnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="227a9-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="227a9-115">Dette er sekvensen der arbeidsmalene blir evaluert.</span><span class="sxs-lookup"><span data-stu-id="227a9-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="227a9-116">Du kan endre rekkefølgen om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="227a9-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="227a9-117">Angi en verdi i feltet Arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="227a9-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="227a9-118">Dette er den unike identifikatoren for denne malen.</span><span class="sxs-lookup"><span data-stu-id="227a9-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="227a9-119">Skriv inn en verdi i feltet Beskrivelse av arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="227a9-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="227a9-120">Alternativet gyldig kontrolleres ikke før du har fullført all informasjonen som kreves av malen og deretter har klikket Lagre.</span><span class="sxs-lookup"><span data-stu-id="227a9-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="227a9-121">En arbeidsordre av typen Bestilling kan ikke kan behandles automatisk, så la alternativet Behandle automatisk være satt til Nei.</span><span class="sxs-lookup"><span data-stu-id="227a9-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="227a9-122">Skriv inn en verdi i feltet ID for arbeidsutvalg.</span><span class="sxs-lookup"><span data-stu-id="227a9-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="227a9-123">Arbeidspulje-ID-er gir deg muligheten til å organisere arbeidet i grupper.</span><span class="sxs-lookup"><span data-stu-id="227a9-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="227a9-124">Verdien du angir her, blir standardverdien for arbeid som opprettes med denne malen.</span><span class="sxs-lookup"><span data-stu-id="227a9-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="227a9-125">I Arbeidsprioritet-feltet angir du '1'.</span><span class="sxs-lookup"><span data-stu-id="227a9-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="227a9-126">Dette indikerer viktigheten av arbeidet, og verdien du angir her, blir standard for alt arbeid som er opprettet ved hjelp av denne malen.</span><span class="sxs-lookup"><span data-stu-id="227a9-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="227a9-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="227a9-127">Click Save.</span></span>
    * <span data-ttu-id="227a9-128">Du må lagre arbeidsmalhodet før knappen Rediger spørring blir tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="227a9-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="227a9-129">Konfigurere spørringen for arbeidsmalen</span><span class="sxs-lookup"><span data-stu-id="227a9-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="227a9-130">Klikk Rediger spørring.</span><span class="sxs-lookup"><span data-stu-id="227a9-130">Click Edit query.</span></span>
    * <span data-ttu-id="227a9-131">Vi vil angi en begrensning slik at malen bare kan brukes i et bestemt lager.</span><span class="sxs-lookup"><span data-stu-id="227a9-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="227a9-132">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="227a9-132">Click Add.</span></span>
3. <span data-ttu-id="227a9-133">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="227a9-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="227a9-134">Skriv lager i Felt-feltet.</span><span class="sxs-lookup"><span data-stu-id="227a9-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="227a9-135">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="227a9-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="227a9-136">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="227a9-136">Click OK.</span></span>
7. <span data-ttu-id="227a9-137">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="227a9-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="227a9-138">Angi arbeidsmaldetaljer</span><span class="sxs-lookup"><span data-stu-id="227a9-138">Set work template details</span></span>
1. <span data-ttu-id="227a9-139">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="227a9-139">Click New.</span></span>
2. <span data-ttu-id="227a9-140">Velg Plukk i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="227a9-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="227a9-141">Skriv inn innkjøp i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="227a9-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="227a9-142">Arbeidsklassen som du angir her, blir standard på alle arbeidslinjer av typen Plukk som opprettes ved hjelp av denne malen.</span><span class="sxs-lookup"><span data-stu-id="227a9-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="227a9-143">Arbeidsklassen kan ikke overskrives fra arbeidsordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="227a9-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="227a9-144">Arbeidsklasser brukes til å styre og/eller begrense typen arbeidsordrelinjer som en lagermedarbeider kan behandle på en mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="227a9-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="227a9-145">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="227a9-145">Click New.</span></span>
5. <span data-ttu-id="227a9-146">Velg Plasser i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="227a9-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="227a9-147">Skriv inn en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="227a9-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="227a9-148">Instruksjoner for plukking og plassering er et sett.</span><span class="sxs-lookup"><span data-stu-id="227a9-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="227a9-149">Hvert plukk/plasser-sett må ha samme arbeidsklasse.</span><span class="sxs-lookup"><span data-stu-id="227a9-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="227a9-150">Bruk samme arbeidsklasse som du har angitt for plukkinstruksjonen.</span><span class="sxs-lookup"><span data-stu-id="227a9-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="227a9-151">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="227a9-151">Click Save.</span></span>
    * <span data-ttu-id="227a9-152">Legg merke til at det nå merket av for Gyldig.</span><span class="sxs-lookup"><span data-stu-id="227a9-152">Note that the Valid checkbox is now checked.</span></span>  


---
title: Definere en arbeidsmal for bestillinger
description: Dette emnet beskriver hvordan du definerer en enkel arbeidsmal som skal brukes når du plasserer mottatte varer.
author: ShylaThompson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 473bb133159bb6cdcbbd30ab2c8452eb69f8cfaf
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148207"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="36549-103">Definere en arbeidsmal for bestillinger</span><span class="sxs-lookup"><span data-stu-id="36549-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36549-104">Dette emnet beskriver hvordan du definerer en enkel arbeidsmal som skal brukes når du plasserer mottatte varer.</span><span class="sxs-lookup"><span data-stu-id="36549-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="36549-105">Arbeidsmaler bestemmer settet med instruksjoner som presenteres for lagermedarbeideren på en mobil enhet når de flytter varer fra mottaksområdet.</span><span class="sxs-lookup"><span data-stu-id="36549-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="36549-106">Du kan bruke denne fremgangsmåten med data som er nevnt i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="36549-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="36549-107">Før du starter denne veiledningen kan du opprette en arbeidspulje-ID.</span><span class="sxs-lookup"><span data-stu-id="36549-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="36549-108">I dette eksemplet brukes en arbeidpulje-ID kalt Innkommende.</span><span class="sxs-lookup"><span data-stu-id="36549-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="36549-109">Denne fremgangsmåten er ment for lagersjef.</span><span class="sxs-lookup"><span data-stu-id="36549-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="36549-110">I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Arbeid > Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="36549-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="36549-111">Velg **Bestillinger** i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="36549-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="36549-112">Opprette et arbeidsmalhode</span><span class="sxs-lookup"><span data-stu-id="36549-112">Create a work template header</span></span>
1. <span data-ttu-id="36549-113">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="36549-113">Select **New**.</span></span>
2. <span data-ttu-id="36549-114">Angi et nummer i **Sekvensnummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36549-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="36549-115">Dette er sekvensen der arbeidsmalene blir evaluert.</span><span class="sxs-lookup"><span data-stu-id="36549-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="36549-116">Du kan endre rekkefølgen om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="36549-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="36549-117">Angi en verdi i feltet **Arbeidsmal**.</span><span class="sxs-lookup"><span data-stu-id="36549-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="36549-118">Dette er den unike identifikatoren for denne malen.</span><span class="sxs-lookup"><span data-stu-id="36549-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="36549-119">Skriv inn en verdi i feltet **Beskrivelse av arbeidsmal**.</span><span class="sxs-lookup"><span data-stu-id="36549-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="36549-120">Alternativet **Gyldig** kontrolleres ikke før du har fullført all informasjonen som kreves av malen og deretter har valgt **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="36549-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="36549-121">En arbeidsordre av typen **Bestilling** kan ikke kan behandles automatisk, så la alternativet **Behandle automatisk** være satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="36549-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="36549-122">Skriv inn en verdi i feltet **ID for arbeidsutvalg**.</span><span class="sxs-lookup"><span data-stu-id="36549-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="36549-123">Arbeidspulje-ID-er gir deg muligheten til å organisere arbeidet i grupper.</span><span class="sxs-lookup"><span data-stu-id="36549-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="36549-124">Verdien du angir her, blir standardverdien for arbeid som opprettes med denne malen.</span><span class="sxs-lookup"><span data-stu-id="36549-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="36549-125">I **Arbeidsprioritet**-feltet angir du `1`.</span><span class="sxs-lookup"><span data-stu-id="36549-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="36549-126">Dette indikerer viktigheten av arbeidet, og verdien du angir her, blir standard for alt arbeid som er opprettet ved hjelp av denne malen.</span><span class="sxs-lookup"><span data-stu-id="36549-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="36549-127">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="36549-127">Select **Save**.</span></span> <span data-ttu-id="36549-128">Du må lagre arbeidsmalhodet før knappen **Rediger spørring** blir tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="36549-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="36549-129">Konfigurere spørringen for arbeidsmalen</span><span class="sxs-lookup"><span data-stu-id="36549-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="36549-130">Velg **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="36549-130">Select **Edit query**.</span></span> <span data-ttu-id="36549-131">Vi vil angi en begrensning slik at malen bare kan brukes i et bestemt lager.</span><span class="sxs-lookup"><span data-stu-id="36549-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="36549-132">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="36549-132">Select **Add**.</span></span>
3. <span data-ttu-id="36549-133">Skriv inn `warehouse` i **Felt**-feltet i den nye raden.</span><span class="sxs-lookup"><span data-stu-id="36549-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="36549-134">Skriv inn en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36549-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="36549-135">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="36549-135">Select **OK**.</span></span>
6. <span data-ttu-id="36549-136">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="36549-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="36549-137">Angi arbeidsmaldetaljer</span><span class="sxs-lookup"><span data-stu-id="36549-137">Set work template details</span></span>
1. <span data-ttu-id="36549-138">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="36549-138">Select **New**.</span></span>
2. <span data-ttu-id="36549-139">Velg **Plukk** i **Arbeidstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36549-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="36549-140">Skriv inn `purchase` i feltet **Arbeidsklasse-ID**.</span><span class="sxs-lookup"><span data-stu-id="36549-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="36549-141">Arbeidsklassen som du angir her, blir standard på alle arbeidslinjer av typen Plukk som opprettes ved hjelp av denne malen.</span><span class="sxs-lookup"><span data-stu-id="36549-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="36549-142">Arbeidsklassen kan ikke overskrives fra arbeidsordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="36549-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="36549-143">Arbeidsklasser brukes til å styre og/eller begrense typen arbeidsordrelinjer som en lagermedarbeider kan behandle på en mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="36549-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="36549-144">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="36549-144">Select **New**.</span></span>
5. <span data-ttu-id="36549-145">Velg **Plasser** i **Arbeidstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36549-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="36549-146">Skriv inn en verdi i feltet **Arbeidsklasse-ID**.</span><span class="sxs-lookup"><span data-stu-id="36549-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="36549-147">Instruksjoner for plukking og plassering er et sett.</span><span class="sxs-lookup"><span data-stu-id="36549-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="36549-148">Hvert plukk/plasser-sett må ha samme arbeidsklasse.</span><span class="sxs-lookup"><span data-stu-id="36549-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="36549-149">Bruk samme arbeidsklasse som du har angitt for plukkinstruksjonen.</span><span class="sxs-lookup"><span data-stu-id="36549-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="36549-150">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="36549-150">Select **Save**.</span></span> <span data-ttu-id="36549-151">Legg merke til at det nå merket av for **Gyldig**.</span><span class="sxs-lookup"><span data-stu-id="36549-151">Note that the **Valid** checkbox is now checked.</span></span>  


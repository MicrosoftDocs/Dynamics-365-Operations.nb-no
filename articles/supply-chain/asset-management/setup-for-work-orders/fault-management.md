---
title: Feilstyring
description: Dette emnet beskriver feilstyring i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78c062f9982ca7b18fa00d60928089d09a5d552d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570961"
---
# <a name="fault-management"></a><span data-ttu-id="6ca7e-103">Feilstyring</span><span class="sxs-lookup"><span data-stu-id="6ca7e-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6ca7e-104">I Aktivastyring kan du bruke feilutformingen til å definere feilsymptomer, feilområder og feiltyper på anleggsmiddeltyper.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="6ca7e-105">På denne måten kan du styre feil som oppdages i aktiva.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="6ca7e-106">I tillegg kan feilårsaker og forslag til reparasjon av feil registreres i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="6ca7e-107">Prosessen for feilregistrering og -styring består av disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="6ca7e-108">Opprett en liste over feilsymptomer, feilområder og feiltyper som kan oppstå på anleggsmiddeltypene.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="6ca7e-109">I feilutformingen definerer du symptomer, feilområder og feiltyper.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="6ca7e-110">Her er noen eksempler som kan hjelpe deg med å forstå forskjellen mellom feilsymptomer, feilområder og feiltyper.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="6ca7e-111">**Feilsymptomer:**</span><span class="sxs-lookup"><span data-stu-id="6ca7e-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="6ca7e-112">Ubalanserte spenninger</span><span class="sxs-lookup"><span data-stu-id="6ca7e-112">Unbalanced voltages</span></span>
- <span data-ttu-id="6ca7e-113">Kortslutning</span><span class="sxs-lookup"><span data-stu-id="6ca7e-113">Short circuit</span></span>
- <span data-ttu-id="6ca7e-114">Støy</span><span class="sxs-lookup"><span data-stu-id="6ca7e-114">Noise</span></span>
- <span data-ttu-id="6ca7e-115">Lekkasje</span><span class="sxs-lookup"><span data-stu-id="6ca7e-115">Leak</span></span>
- <span data-ttu-id="6ca7e-116">Vibrasjoner</span><span class="sxs-lookup"><span data-stu-id="6ca7e-116">Vibrations</span></span>

<span data-ttu-id="6ca7e-117">**Feilområder:**</span><span class="sxs-lookup"><span data-stu-id="6ca7e-117">**Fault areas:**</span></span>

- <span data-ttu-id="6ca7e-118">Elektrisk</span><span class="sxs-lookup"><span data-stu-id="6ca7e-118">Electrical</span></span>
- <span data-ttu-id="6ca7e-119">Mekanisk</span><span class="sxs-lookup"><span data-stu-id="6ca7e-119">Mechanical</span></span>
- <span data-ttu-id="6ca7e-120">Hydraulisk</span><span class="sxs-lookup"><span data-stu-id="6ca7e-120">Hydraulic</span></span>
- <span data-ttu-id="6ca7e-121">Pneumatisk</span><span class="sxs-lookup"><span data-stu-id="6ca7e-121">Pneumatic</span></span>

<span data-ttu-id="6ca7e-122">**Feiltyper:**</span><span class="sxs-lookup"><span data-stu-id="6ca7e-122">**Fault types:**</span></span>

- <span data-ttu-id="6ca7e-123">Feil i vikling av hovedstator</span><span class="sxs-lookup"><span data-stu-id="6ca7e-123">Faulty main stator winding</span></span>
- <span data-ttu-id="6ca7e-124">Defekt diode</span><span class="sxs-lookup"><span data-stu-id="6ca7e-124">Faulty diode</span></span>
- <span data-ttu-id="6ca7e-125">Skitne viklinger</span><span class="sxs-lookup"><span data-stu-id="6ca7e-125">Dirty windings</span></span>
- <span data-ttu-id="6ca7e-126">Defekt generator</span><span class="sxs-lookup"><span data-stu-id="6ca7e-126">Defective generator</span></span>
- <span data-ttu-id="6ca7e-127">Defekt sensor</span><span class="sxs-lookup"><span data-stu-id="6ca7e-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="6ca7e-128">Opprette feilsymptomer</span><span class="sxs-lookup"><span data-stu-id="6ca7e-128">Create fault symptoms</span></span>

<span data-ttu-id="6ca7e-129">Følg denne fremgangsmåten for å opprette en liste over symptomer som kan brukes i feilutformingen.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="6ca7e-130">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilsymptomer**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="6ca7e-131">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="6ca7e-132">Skriv inn et navn på feilsymptomet i **Feilsymptom**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="6ca7e-133">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="6ca7e-134">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="6ca7e-135">Opprette feilområder</span><span class="sxs-lookup"><span data-stu-id="6ca7e-135">Create fault areas</span></span>

<span data-ttu-id="6ca7e-136">Følg denne fremgangsmåten for å opprette en liste over områder eller steder som kan brukes i feilutformingen.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="6ca7e-137">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilområder**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="6ca7e-138">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="6ca7e-139">Skriv inn et navn på feilområdet i **Feilområde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="6ca7e-140">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="6ca7e-141">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="6ca7e-142">Opprette feiltyper</span><span class="sxs-lookup"><span data-stu-id="6ca7e-142">Create fault types</span></span>

<span data-ttu-id="6ca7e-143">Følg denne fremgangsmåten for å opprette en liste over feiltyper som kan brukes i feilutformingen.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="6ca7e-144">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feiltyper**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="6ca7e-145">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="6ca7e-146">I **Feiltype**-feltet angir du et navn på feiltypen.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="6ca7e-147">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="6ca7e-148">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="6ca7e-149">Definere feilutformingen</span><span class="sxs-lookup"><span data-stu-id="6ca7e-149">Set up the fault designer</span></span>

<span data-ttu-id="6ca7e-150">I feilutformingen definerer du feildata for anleggsmiddeltyper.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="6ca7e-151">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilutforming**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="6ca7e-152">I venstre rute velger du anleggsmiddeltypen du vil definere en feilpost for.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="6ca7e-153">I hurtigfanen **Feil** velger du **Legg til linje**, og deretter velger du et feilsymptom i **Feilsymptom**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="6ca7e-154">I hurtigfanen **Feilområde** velger du **Legg til linje**, og deretter velger du et feilområde i **Feilområde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="6ca7e-155">I hurtigfanen **Feiltype** velger du **Legg til linje**, og deretter velger du en feiltype i **Feiltype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="6ca7e-156">Hvis du raskt vil opprette kombinasjoner av alle eksisterende feilsymptomer, områder og typer for den valgte anleggsmiddeltypen, velger du **Opprett feilkombinasjoner**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="6ca7e-157">Denne funksjonen er nyttig hvis du har lagt til mange feilsymptomer, områder og typer.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="6ca7e-158">Det er enklere å slette linjene for kombinasjoner som ikke er relevante for anleggsmiddeltypen, enn å opprette nye linjer manuelt.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ca7e-159">Hvis du vil kopiere oppsettet av feilsymptomer, områder og typer fra én anleggsmiddeltype til den valgte anleggsmiddeltypen, velger du **Kopier fra anleggsmiddeltype**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="6ca7e-160">Velg **Lagre** for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-160">Select **Save** to save your changes.</span></span>

![Siden Feilutforming](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="6ca7e-162">Opprette feilårsaker</span><span class="sxs-lookup"><span data-stu-id="6ca7e-162">Create fault causes</span></span>

<span data-ttu-id="6ca7e-163">Følg denne fremgangsmåten for å opprette en liste over kjente feilårsaker som kan legges til i en arbeidsordre eller en vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="6ca7e-164">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilårsaker**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="6ca7e-165">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="6ca7e-166">I **Feilårsak**-feltet angir du et navn på feilårsaken.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="6ca7e-167">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="6ca7e-168">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="6ca7e-169">Opprette feilløsninger</span><span class="sxs-lookup"><span data-stu-id="6ca7e-169">Create fault remedies</span></span>

<span data-ttu-id="6ca7e-170">Følg denne fremgangsmåten for å opprette en liste over forslag til løsning og reparasjon som kan legges til i en arbeidsordre eller en vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="6ca7e-171">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilløsninger**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="6ca7e-172">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="6ca7e-173">Skriv inn et navn på feilløsningen i **Feilløsning**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="6ca7e-174">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="6ca7e-175">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="6ca7e-176">Du kan endre navnene på feilsymptomer, områder, typer, årsaker og løsninger etter behov.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="6ca7e-177">Navneendringene gjenspeiles automatisk i relaterte feilregistreringer.</span><span class="sxs-lookup"><span data-stu-id="6ca7e-177">The name changes are automatically reflected in the related fault registrations.</span></span>

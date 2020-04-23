---
title: Feilstyring
description: Dette emnet beskriver feilstyring i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6665e80342af1baa7176aee92693b77e83b368f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205926"
---
# <a name="fault-management"></a><span data-ttu-id="f90ce-103">Feilstyring</span><span class="sxs-lookup"><span data-stu-id="f90ce-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f90ce-104">I Aktivastyring kan du bruke feilutformingen til å definere feilsymptomer, feilområder og feiltyper på anleggsmiddeltyper.</span><span class="sxs-lookup"><span data-stu-id="f90ce-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="f90ce-105">På denne måten kan du styre feil som oppdages i aktiva.</span><span class="sxs-lookup"><span data-stu-id="f90ce-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="f90ce-106">I tillegg kan feilårsaker og forslag til reparasjon av feil registreres i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="f90ce-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="f90ce-107">Prosessen for feilregistrering og -styring består av disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f90ce-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="f90ce-108">Opprett en liste over feilsymptomer, feilområder og feiltyper som kan oppstå på anleggsmiddeltypene.</span><span class="sxs-lookup"><span data-stu-id="f90ce-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="f90ce-109">I feilutformingen definerer du symptomer, feilområder og feiltyper.</span><span class="sxs-lookup"><span data-stu-id="f90ce-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="f90ce-110">Her er noen eksempler som kan hjelpe deg med å forstå forskjellen mellom feilsymptomer, feilområder og feiltyper.</span><span class="sxs-lookup"><span data-stu-id="f90ce-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="f90ce-111">**Feilsymptomer:**</span><span class="sxs-lookup"><span data-stu-id="f90ce-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="f90ce-112">Ubalanserte spenninger</span><span class="sxs-lookup"><span data-stu-id="f90ce-112">Unbalanced voltages</span></span>
- <span data-ttu-id="f90ce-113">Kortslutning</span><span class="sxs-lookup"><span data-stu-id="f90ce-113">Short circuit</span></span>
- <span data-ttu-id="f90ce-114">Støy</span><span class="sxs-lookup"><span data-stu-id="f90ce-114">Noise</span></span>
- <span data-ttu-id="f90ce-115">Lekkasje</span><span class="sxs-lookup"><span data-stu-id="f90ce-115">Leak</span></span>
- <span data-ttu-id="f90ce-116">Vibrasjoner</span><span class="sxs-lookup"><span data-stu-id="f90ce-116">Vibrations</span></span>

<span data-ttu-id="f90ce-117">**Feilområder:**</span><span class="sxs-lookup"><span data-stu-id="f90ce-117">**Fault areas:**</span></span>

- <span data-ttu-id="f90ce-118">Elektrisk</span><span class="sxs-lookup"><span data-stu-id="f90ce-118">Electrical</span></span>
- <span data-ttu-id="f90ce-119">Mekanisk</span><span class="sxs-lookup"><span data-stu-id="f90ce-119">Mechanical</span></span>
- <span data-ttu-id="f90ce-120">Hydraulisk</span><span class="sxs-lookup"><span data-stu-id="f90ce-120">Hydraulic</span></span>
- <span data-ttu-id="f90ce-121">Pneumatisk</span><span class="sxs-lookup"><span data-stu-id="f90ce-121">Pneumatic</span></span>

<span data-ttu-id="f90ce-122">**Feiltyper:**</span><span class="sxs-lookup"><span data-stu-id="f90ce-122">**Fault types:**</span></span>

- <span data-ttu-id="f90ce-123">Feil i vikling av hovedstator</span><span class="sxs-lookup"><span data-stu-id="f90ce-123">Faulty main stator winding</span></span>
- <span data-ttu-id="f90ce-124">Defekt diode</span><span class="sxs-lookup"><span data-stu-id="f90ce-124">Faulty diode</span></span>
- <span data-ttu-id="f90ce-125">Skitne viklinger</span><span class="sxs-lookup"><span data-stu-id="f90ce-125">Dirty windings</span></span>
- <span data-ttu-id="f90ce-126">Defekt generator</span><span class="sxs-lookup"><span data-stu-id="f90ce-126">Defective generator</span></span>
- <span data-ttu-id="f90ce-127">Defekt sensor</span><span class="sxs-lookup"><span data-stu-id="f90ce-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="f90ce-128">Opprette feilsymptomer</span><span class="sxs-lookup"><span data-stu-id="f90ce-128">Create fault symptoms</span></span>

<span data-ttu-id="f90ce-129">Følg denne fremgangsmåten for å opprette en liste over symptomer som kan brukes i feilutformingen.</span><span class="sxs-lookup"><span data-stu-id="f90ce-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f90ce-130">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilsymptomer**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="f90ce-131">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="f90ce-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f90ce-132">Skriv inn et navn på feilsymptomet i **Feilsymptom**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="f90ce-133">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f90ce-134">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="f90ce-135">Opprette feilområder</span><span class="sxs-lookup"><span data-stu-id="f90ce-135">Create fault areas</span></span>

<span data-ttu-id="f90ce-136">Følg denne fremgangsmåten for å opprette en liste over områder eller steder som kan brukes i feilutformingen.</span><span class="sxs-lookup"><span data-stu-id="f90ce-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f90ce-137">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilområder**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="f90ce-138">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="f90ce-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f90ce-139">Skriv inn et navn på feilområdet i **Feilområde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="f90ce-140">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f90ce-141">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="f90ce-142">Opprette feiltyper</span><span class="sxs-lookup"><span data-stu-id="f90ce-142">Create fault types</span></span>

<span data-ttu-id="f90ce-143">Følg denne fremgangsmåten for å opprette en liste over feiltyper som kan brukes i feilutformingen.</span><span class="sxs-lookup"><span data-stu-id="f90ce-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f90ce-144">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feiltyper**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="f90ce-145">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="f90ce-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f90ce-146">I **Feiltype**-feltet angir du et navn på feiltypen.</span><span class="sxs-lookup"><span data-stu-id="f90ce-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="f90ce-147">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f90ce-148">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="f90ce-149">Definere feilutformingen</span><span class="sxs-lookup"><span data-stu-id="f90ce-149">Set up the fault designer</span></span>

<span data-ttu-id="f90ce-150">I feilutformingen definerer du feildata for anleggsmiddeltyper.</span><span class="sxs-lookup"><span data-stu-id="f90ce-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="f90ce-151">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilutforming**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="f90ce-152">I venstre rute velger du anleggsmiddeltypen du vil definere en feilpost for.</span><span class="sxs-lookup"><span data-stu-id="f90ce-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="f90ce-153">I hurtigfanen **Feil** velger du **Legg til linje**, og deretter velger du et feilsymptom i **Feilsymptom**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="f90ce-154">I hurtigfanen **Feilområde** velger du **Legg til linje**, og deretter velger du et feilområde i **Feilområde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="f90ce-155">I hurtigfanen **Feiltype** velger du **Legg til linje**, og deretter velger du en feiltype i **Feiltype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="f90ce-156">Hvis du raskt vil opprette kombinasjoner av alle eksisterende feilsymptomer, områder og typer for den valgte anleggsmiddeltypen, velger du **Opprett feilkombinasjoner**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="f90ce-157">Denne funksjonen er nyttig hvis du har lagt til mange feilsymptomer, områder og typer.</span><span class="sxs-lookup"><span data-stu-id="f90ce-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="f90ce-158">Det er enklere å slette linjene for kombinasjoner som ikke er relevante for anleggsmiddeltypen, enn å opprette nye linjer manuelt.</span><span class="sxs-lookup"><span data-stu-id="f90ce-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f90ce-159">Hvis du vil kopiere oppsettet av feilsymptomer, områder og typer fra én anleggsmiddeltype til den valgte anleggsmiddeltypen, velger du **Kopier fra anleggsmiddeltype**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="f90ce-160">Velg **Lagre** for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="f90ce-160">Select **Save** to save your changes.</span></span>

![Siden Feilutforming](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="f90ce-162">Opprette feilårsaker</span><span class="sxs-lookup"><span data-stu-id="f90ce-162">Create fault causes</span></span>

<span data-ttu-id="f90ce-163">Følg denne fremgangsmåten for å opprette en liste over kjente feilårsaker som kan legges til i en arbeidsordre eller en vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="f90ce-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="f90ce-164">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilårsaker**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="f90ce-165">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="f90ce-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f90ce-166">I **Feilårsak**-feltet angir du et navn på feilårsaken.</span><span class="sxs-lookup"><span data-stu-id="f90ce-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="f90ce-167">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f90ce-168">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="f90ce-169">Opprette feilløsninger</span><span class="sxs-lookup"><span data-stu-id="f90ce-169">Create fault remedies</span></span>

<span data-ttu-id="f90ce-170">Følg denne fremgangsmåten for å opprette en liste over forslag til løsning og reparasjon som kan legges til i en arbeidsordre eller en vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="f90ce-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="f90ce-171">Velg **Aktivastyring** \> **Oppsett** \> **Feil** \> **Feilløsninger**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="f90ce-172">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="f90ce-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f90ce-173">Skriv inn et navn på feilløsningen i **Feilløsning**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="f90ce-174">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f90ce-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f90ce-175">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="f90ce-176">Du kan endre navnene på feilsymptomer, områder, typer, årsaker og løsninger etter behov.</span><span class="sxs-lookup"><span data-stu-id="f90ce-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="f90ce-177">Navneendringene gjenspeiles automatisk i relaterte feilregistreringer.</span><span class="sxs-lookup"><span data-stu-id="f90ce-177">The name changes are automatically reflected in the related fault registrations.</span></span>

---
title: Fraktcontainere
description: Dette emnet beskriver hvordan du definerer forsendelsescontainere for modulen Netto innkjøpspris.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833719"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="fa09f-103">Oppsett av forsendelsescontainere</span><span class="sxs-lookup"><span data-stu-id="fa09f-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa09f-104">Dette emnet beskriver hvordan du definerer forsendelsescontainere for modulen **Netto innkjøpspris**.</span><span class="sxs-lookup"><span data-stu-id="fa09f-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="fa09f-105">Definere typer forsendelsescontainere</span><span class="sxs-lookup"><span data-stu-id="fa09f-105">Set up shipping container types</span></span>

<span data-ttu-id="fa09f-106">Typer forsendelsescontainere definerer typene forsendelsescontainere som er tilgjengelige for bruk under forsendelse og sjøreiser.</span><span class="sxs-lookup"><span data-stu-id="fa09f-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="fa09f-107">Hvis du vil arbeide med typer forsendelsescontainere, går du til **Netto innkjøpspris \> Containeroppsett \> Typer forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="fa09f-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="fa09f-108">Der kan du vise, legge til og fjerne poster for containertypene dine.</span><span class="sxs-lookup"><span data-stu-id="fa09f-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="fa09f-109">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="fa09f-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fa09f-110">Felt</span><span class="sxs-lookup"><span data-stu-id="fa09f-110">Field</span></span> | <span data-ttu-id="fa09f-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa09f-111">Description</span></span> |
|---|---|
| <span data-ttu-id="fa09f-112">Fraktcontainertype</span><span class="sxs-lookup"><span data-stu-id="fa09f-112">Shipping container type</span></span> | <span data-ttu-id="fa09f-113">Angi et unikt identifikasjonsnavn/-nummer for type forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="fa09f-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="fa09f-114">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa09f-114">Description</span></span> | <span data-ttu-id="fa09f-115">Angi en beskrivelse av typen forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="fa09f-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="fa09f-116">Volum</span><span class="sxs-lookup"><span data-stu-id="fa09f-116">Volume</span></span> | <span data-ttu-id="fa09f-117">Angi det maksimale volumet som er tillatt for forsendelsescontainere av denne typen.</span><span class="sxs-lookup"><span data-stu-id="fa09f-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="fa09f-118">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="fa09f-118">Weight</span></span> | <span data-ttu-id="fa09f-119">Angi den maksimale vekten som er tillatt for forsendelsescontainere av denne typen.</span><span class="sxs-lookup"><span data-stu-id="fa09f-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="fa09f-120">Returnerbar</span><span class="sxs-lookup"><span data-stu-id="fa09f-120">Returnable</span></span> | <span data-ttu-id="fa09f-121">Angi om forsendelsescontainere av denne typen kan returneres til leverandøren etter at de er brukt under en sjøreise.</span><span class="sxs-lookup"><span data-stu-id="fa09f-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="fa09f-122">Hvis du velger *Ja*, kan det hende at tilleggskostnader påløper for retur av forsendelsescontainere av denne typen til opprinnelseshavnen.</span><span class="sxs-lookup"><span data-stu-id="fa09f-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="fa09f-123">Definere forsendelsescontainere</span><span class="sxs-lookup"><span data-stu-id="fa09f-123">Set up shipping containers</span></span>

<span data-ttu-id="fa09f-124">Du bruker poster for forsendelsescontainer til å identifisere hver container du bruker under sjøreiser.</span><span class="sxs-lookup"><span data-stu-id="fa09f-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="fa09f-125">Når du oppretter en sjøreise, kan du velge en bestemt container for sjøreisen i listen over alle postene for forsendelsescontainer du har definert her.</span><span class="sxs-lookup"><span data-stu-id="fa09f-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="fa09f-126">Denne funksjonen er spesielt nyttig hvis firmaet eier sine egne forsendelsescontainere.</span><span class="sxs-lookup"><span data-stu-id="fa09f-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="fa09f-127">Du behøver ikke å angi forsendelsescontainernumre for forsendelsescontainere som bare skal brukes én gang.</span><span class="sxs-lookup"><span data-stu-id="fa09f-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="fa09f-128">I stedet kan du legge til forsendelsescontainernummeret når du oppretter en sjøreise.</span><span class="sxs-lookup"><span data-stu-id="fa09f-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="fa09f-129">Poster for forsendelsescontainer brukes bare i Netto innkjøpspris.</span><span class="sxs-lookup"><span data-stu-id="fa09f-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="fa09f-130">De er ikke tilgjengelige i standardmodulen **Transportstyring** (TMS).</span><span class="sxs-lookup"><span data-stu-id="fa09f-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="fa09f-131">Hvis du vil arbeide med forsendelsescontainere, går du til **Netto innkjøpspris \> Containeroppsett \> Forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="fa09f-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="fa09f-132">Der kan du vise, legge til og fjerne poster for forsendelsescontainerne.</span><span class="sxs-lookup"><span data-stu-id="fa09f-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="fa09f-133">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="fa09f-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fa09f-134">Felt</span><span class="sxs-lookup"><span data-stu-id="fa09f-134">Field</span></span> | <span data-ttu-id="fa09f-135">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa09f-135">Description</span></span> |
|---|---|
| <span data-ttu-id="fa09f-136">Fraktcontainer</span><span class="sxs-lookup"><span data-stu-id="fa09f-136">Shipping container</span></span> | <span data-ttu-id="fa09f-137">Angi et unikt identifikasjonsnavn/-nummer for forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="fa09f-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="fa09f-138">Fraktcontainertype</span><span class="sxs-lookup"><span data-stu-id="fa09f-138">Shipping container type</span></span> | <span data-ttu-id="fa09f-139">Velg typen forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="fa09f-139">Select the type of shipping container.</span></span> <span data-ttu-id="fa09f-140">Hvis du vil ha mer informasjon, kan du se delen [Konfigurere typer forsendelsescontainer](#shipping-container-types) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="fa09f-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="fa09f-141">Oppsettet av forsendelsescontainere er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="fa09f-141">The shipping container setup is optional.</span></span> <span data-ttu-id="fa09f-142">Vanligvis bruker du det bare hvis firmaet eier sine egne forsendelsescontainere eller ofte bruker de samme forsendelsescontainerne på nytt.</span><span class="sxs-lookup"><span data-stu-id="fa09f-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="fa09f-143">Ingen kontrollsifre beregnes for forsendelsescontainernumre.</span><span class="sxs-lookup"><span data-stu-id="fa09f-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="fa09f-144">Definere enhetstyper</span><span class="sxs-lookup"><span data-stu-id="fa09f-144">Set up unit types</span></span>

<span data-ttu-id="fa09f-145">Enhetstyper fastsetter ytterligere grupperinger og identifikasjonsmetoder for forsendelsescontainere.</span><span class="sxs-lookup"><span data-stu-id="fa09f-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="fa09f-146">Enhetstypen brukes vanligvis til å identifisere containertypen varer er pakket i, for eksempel paller eller tromler.</span><span class="sxs-lookup"><span data-stu-id="fa09f-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="fa09f-147">Du kan velge en enhetstype når du definerer en container på siden **Alle forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="fa09f-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="fa09f-148">Enhetstyper brukes bare i Netto innkjøpspris.</span><span class="sxs-lookup"><span data-stu-id="fa09f-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="fa09f-149">De er ikke tilgjengelige i TMS.</span><span class="sxs-lookup"><span data-stu-id="fa09f-149">They aren't available in TMS.</span></span>

<span data-ttu-id="fa09f-150">Hvis du vil arbeide med enhetstyper, går du til **Netto innkjøpspris \> Containeroppsett \> Enhetstyper**.</span><span class="sxs-lookup"><span data-stu-id="fa09f-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="fa09f-151">Der kan du vise, legge til og fjerne poster for enhetstypene dine.</span><span class="sxs-lookup"><span data-stu-id="fa09f-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="fa09f-152">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="fa09f-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fa09f-153">Felt</span><span class="sxs-lookup"><span data-stu-id="fa09f-153">Field</span></span> | <span data-ttu-id="fa09f-154">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa09f-154">Description</span></span> |
|---|---|
| <span data-ttu-id="fa09f-155">Enhetstype</span><span class="sxs-lookup"><span data-stu-id="fa09f-155">Unit type</span></span> | <span data-ttu-id="fa09f-156">Angi et unikt identifikasjonsnavn/-nummer for enhetstypen.</span><span class="sxs-lookup"><span data-stu-id="fa09f-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="fa09f-157">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa09f-157">Description</span></span> | <span data-ttu-id="fa09f-158">Skriv inn en beskrivelse av enhetstypen.</span><span class="sxs-lookup"><span data-stu-id="fa09f-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="fa09f-159">Definere kjøletyper</span><span class="sxs-lookup"><span data-stu-id="fa09f-159">Set up refrigeration types</span></span>

<span data-ttu-id="fa09f-160">Kjøletyper oppretter tilleggsgrupperinger og identifikasjonsmetoder for forsendelsescontainere (vanligvis kjølecontainere).</span><span class="sxs-lookup"><span data-stu-id="fa09f-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="fa09f-161">Du kan velge en kjøletype når du definerer en container på siden **Alle forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="fa09f-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="fa09f-162">Hvis du vil arbeide med kjøletyper, går du til **Netto innkjøpspris \> Containeroppsett \> Kjøletyper**.</span><span class="sxs-lookup"><span data-stu-id="fa09f-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="fa09f-163">Der kan du vise, legge til og fjerne poster for kjøletypene dine.</span><span class="sxs-lookup"><span data-stu-id="fa09f-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="fa09f-164">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="fa09f-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fa09f-165">Felt</span><span class="sxs-lookup"><span data-stu-id="fa09f-165">Field</span></span> | <span data-ttu-id="fa09f-166">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa09f-166">Description</span></span> |
|---|---|
| <span data-ttu-id="fa09f-167">Kjøletype</span><span class="sxs-lookup"><span data-stu-id="fa09f-167">Refrigeration type</span></span> | <span data-ttu-id="fa09f-168">Angi et unikt identifikasjonsnavn/-nummer for kjøletypen.</span><span class="sxs-lookup"><span data-stu-id="fa09f-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="fa09f-169">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa09f-169">Description</span></span> | <span data-ttu-id="fa09f-170">Angi en beskrivelse av kjøletypen.</span><span class="sxs-lookup"><span data-stu-id="fa09f-170">Enter a description of the refrigeration type.</span></span> |

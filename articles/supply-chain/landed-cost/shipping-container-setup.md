---
title: Fraktcontainere
description: Dette emnet beskriver hvordan du definerer forsendelsescontainere for modulen Netto innkjøpspris.
author: sherry-zheng
manager: tfehr
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
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500964"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="474d4-103">Oppsett av forsendelsescontainere</span><span class="sxs-lookup"><span data-stu-id="474d4-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="474d4-104">Dette emnet beskriver hvordan du definerer forsendelsescontainere for modulen **Netto innkjøpspris**.</span><span class="sxs-lookup"><span data-stu-id="474d4-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="474d4-105">Definere typer forsendelsescontainere</span><span class="sxs-lookup"><span data-stu-id="474d4-105">Set up shipping container types</span></span>

<span data-ttu-id="474d4-106">Typer forsendelsescontainere definerer typene forsendelsescontainere som er tilgjengelige for bruk under forsendelse og sjøreiser.</span><span class="sxs-lookup"><span data-stu-id="474d4-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="474d4-107">Hvis du vil arbeide med typer forsendelsescontainere, går du til **Netto innkjøpspris \> Containeroppsett \> Typer forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="474d4-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="474d4-108">Der kan du vise, legge til og fjerne poster for containertypene dine.</span><span class="sxs-lookup"><span data-stu-id="474d4-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="474d4-109">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="474d4-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="474d4-110">Felt</span><span class="sxs-lookup"><span data-stu-id="474d4-110">Field</span></span> | <span data-ttu-id="474d4-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="474d4-111">Description</span></span> |
|---|---|
| <span data-ttu-id="474d4-112">Fraktcontainertype</span><span class="sxs-lookup"><span data-stu-id="474d4-112">Shipping container type</span></span> | <span data-ttu-id="474d4-113">Angi et unikt identifikasjonsnavn/-nummer for type forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="474d4-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="474d4-114">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="474d4-114">Description</span></span> | <span data-ttu-id="474d4-115">Angi en beskrivelse av typen forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="474d4-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="474d4-116">Volum</span><span class="sxs-lookup"><span data-stu-id="474d4-116">Volume</span></span> | <span data-ttu-id="474d4-117">Angi det maksimale volumet som er tillatt for forsendelsescontainere av denne typen.</span><span class="sxs-lookup"><span data-stu-id="474d4-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="474d4-118">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="474d4-118">Weight</span></span> | <span data-ttu-id="474d4-119">Angi den maksimale vekten som er tillatt for forsendelsescontainere av denne typen.</span><span class="sxs-lookup"><span data-stu-id="474d4-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="474d4-120">Returnerbar</span><span class="sxs-lookup"><span data-stu-id="474d4-120">Returnable</span></span> | <span data-ttu-id="474d4-121">Angi om forsendelsescontainere av denne typen kan returneres til leverandøren etter at de er brukt under en sjøreise.</span><span class="sxs-lookup"><span data-stu-id="474d4-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="474d4-122">Hvis du velger *Ja*, kan det hende at tilleggskostnader påløper for retur av forsendelsescontainere av denne typen til opprinnelseshavnen.</span><span class="sxs-lookup"><span data-stu-id="474d4-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="474d4-123">Definere forsendelsescontainere</span><span class="sxs-lookup"><span data-stu-id="474d4-123">Set up shipping containers</span></span>

<span data-ttu-id="474d4-124">Du bruker poster for forsendelsescontainer til å identifisere hver container du bruker under sjøreiser.</span><span class="sxs-lookup"><span data-stu-id="474d4-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="474d4-125">Når du oppretter en sjøreise, kan du velge en bestemt container for sjøreisen i listen over alle postene for forsendelsescontainer du har definert her.</span><span class="sxs-lookup"><span data-stu-id="474d4-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="474d4-126">Denne funksjonen er spesielt nyttig hvis firmaet eier sine egne forsendelsescontainere.</span><span class="sxs-lookup"><span data-stu-id="474d4-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="474d4-127">Du behøver ikke å angi forsendelsescontainernumre for forsendelsescontainere som bare skal brukes én gang.</span><span class="sxs-lookup"><span data-stu-id="474d4-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="474d4-128">I stedet kan du legge til forsendelsescontainernummeret når du oppretter en sjøreise.</span><span class="sxs-lookup"><span data-stu-id="474d4-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="474d4-129">Poster for forsendelsescontainer brukes bare i Netto innkjøpspris.</span><span class="sxs-lookup"><span data-stu-id="474d4-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="474d4-130">De er ikke tilgjengelige i standardmodulen **Transportstyring** (TMS).</span><span class="sxs-lookup"><span data-stu-id="474d4-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="474d4-131">Hvis du vil arbeide med forsendelsescontainere, går du til **Netto innkjøpspris \> Containeroppsett \> Forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="474d4-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="474d4-132">Der kan du vise, legge til og fjerne poster for forsendelsescontainerne.</span><span class="sxs-lookup"><span data-stu-id="474d4-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="474d4-133">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="474d4-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="474d4-134">Felt</span><span class="sxs-lookup"><span data-stu-id="474d4-134">Field</span></span> | <span data-ttu-id="474d4-135">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="474d4-135">Description</span></span> |
|---|---|
| <span data-ttu-id="474d4-136">Fraktcontainer</span><span class="sxs-lookup"><span data-stu-id="474d4-136">Shipping container</span></span> | <span data-ttu-id="474d4-137">Angi et unikt identifikasjonsnavn/-nummer for forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="474d4-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="474d4-138">Fraktcontainertype</span><span class="sxs-lookup"><span data-stu-id="474d4-138">Shipping container type</span></span> | <span data-ttu-id="474d4-139">Velg typen forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="474d4-139">Select the type of shipping container.</span></span> <span data-ttu-id="474d4-140">Hvis du vil ha mer informasjon, kan du se delen [Konfigurere typer forsendelsescontainer](#shipping-container-types) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="474d4-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="474d4-141">Oppsettet av forsendelsescontainere er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="474d4-141">The shipping container setup is optional.</span></span> <span data-ttu-id="474d4-142">Vanligvis bruker du det bare hvis firmaet eier sine egne forsendelsescontainere eller ofte bruker de samme forsendelsescontainerne på nytt.</span><span class="sxs-lookup"><span data-stu-id="474d4-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="474d4-143">Ingen kontrollsifre beregnes for forsendelsescontainernumre.</span><span class="sxs-lookup"><span data-stu-id="474d4-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="474d4-144">Definere enhetstyper</span><span class="sxs-lookup"><span data-stu-id="474d4-144">Set up unit types</span></span>

<span data-ttu-id="474d4-145">Enhetstyper fastsetter ytterligere grupperinger og identifikasjonsmetoder for forsendelsescontainere.</span><span class="sxs-lookup"><span data-stu-id="474d4-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="474d4-146">Enhetstypen brukes vanligvis til å identifisere containertypen varer er pakket i, for eksempel paller eller tromler.</span><span class="sxs-lookup"><span data-stu-id="474d4-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="474d4-147">Du kan velge en enhetstype når du definerer en container på siden **Alle forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="474d4-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="474d4-148">Enhetstyper brukes bare i Netto innkjøpspris.</span><span class="sxs-lookup"><span data-stu-id="474d4-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="474d4-149">De er ikke tilgjengelige i TMS.</span><span class="sxs-lookup"><span data-stu-id="474d4-149">They aren't available in TMS.</span></span>

<span data-ttu-id="474d4-150">Hvis du vil arbeide med enhetstyper, går du til **Netto innkjøpspris \> Containeroppsett \> Enhetstyper**.</span><span class="sxs-lookup"><span data-stu-id="474d4-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="474d4-151">Der kan du vise, legge til og fjerne poster for enhetstypene dine.</span><span class="sxs-lookup"><span data-stu-id="474d4-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="474d4-152">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="474d4-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="474d4-153">Felt</span><span class="sxs-lookup"><span data-stu-id="474d4-153">Field</span></span> | <span data-ttu-id="474d4-154">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="474d4-154">Description</span></span> |
|---|---|
| <span data-ttu-id="474d4-155">Enhetstype</span><span class="sxs-lookup"><span data-stu-id="474d4-155">Unit type</span></span> | <span data-ttu-id="474d4-156">Angi et unikt identifikasjonsnavn/-nummer for enhetstypen.</span><span class="sxs-lookup"><span data-stu-id="474d4-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="474d4-157">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="474d4-157">Description</span></span> | <span data-ttu-id="474d4-158">Skriv inn en beskrivelse av enhetstypen.</span><span class="sxs-lookup"><span data-stu-id="474d4-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="474d4-159">Definere kjøletyper</span><span class="sxs-lookup"><span data-stu-id="474d4-159">Set up refrigeration types</span></span>

<span data-ttu-id="474d4-160">Kjøletyper oppretter tilleggsgrupperinger og identifikasjonsmetoder for forsendelsescontainere (vanligvis kjølecontainere).</span><span class="sxs-lookup"><span data-stu-id="474d4-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="474d4-161">Du kan velge en kjøletype når du definerer en container på siden **Alle forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="474d4-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="474d4-162">Hvis du vil arbeide med kjøletyper, går du til **Netto innkjøpspris \> Containeroppsett \> Kjøletyper**.</span><span class="sxs-lookup"><span data-stu-id="474d4-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="474d4-163">Der kan du vise, legge til og fjerne poster for kjøletypene dine.</span><span class="sxs-lookup"><span data-stu-id="474d4-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="474d4-164">Følgende tabell beskriver feltene som er tilgjengelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="474d4-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="474d4-165">Felt</span><span class="sxs-lookup"><span data-stu-id="474d4-165">Field</span></span> | <span data-ttu-id="474d4-166">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="474d4-166">Description</span></span> |
|---|---|
| <span data-ttu-id="474d4-167">Kjøletype</span><span class="sxs-lookup"><span data-stu-id="474d4-167">Refrigeration type</span></span> | <span data-ttu-id="474d4-168">Angi et unikt identifikasjonsnavn/-nummer for kjøletypen.</span><span class="sxs-lookup"><span data-stu-id="474d4-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="474d4-169">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="474d4-169">Description</span></span> | <span data-ttu-id="474d4-170">Angi en beskrivelse av kjøletypen.</span><span class="sxs-lookup"><span data-stu-id="474d4-170">Enter a description of the refrigeration type.</span></span> |

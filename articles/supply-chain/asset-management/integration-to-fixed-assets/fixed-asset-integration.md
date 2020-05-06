---
title: Integrere aktivabehandling med anleggsmidler
description: Dette emnet beskriver hvordan du integrerer Aktivastyring- og Anleggsmiddel-modulene, slik at du kan knytte anleggsmidler til vedlikeholdsgjenstander.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276949"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="f261f-103">Integrere aktivabehandling med anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="f261f-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f261f-104">Ved å integrere moduelene **Aktivastyring** og **Anleggsmiddel** kan du knytte anleggsmidler til vedlikeholdsgjenstander.</span><span class="sxs-lookup"><span data-stu-id="f261f-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="f261f-105">Anleggsmidler-brukere kan deretter opprette en vedlikeholdsgjenstand fra et nytt eller eksisterende anleggsmiddel, og brukere av Aktivastyring kan knytte en vedlikeholdsgjenstand til et eksisterende anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="f261f-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="f261f-106">Denne funksjonen gjør det også enkelt for anleggsmiddel-brukere å vise kostnadene som ble bokført fra arbeidsordrer for relaterte vedlikeholdsgjenstander.</span><span class="sxs-lookup"><span data-stu-id="f261f-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="f261f-107">I dette emnet refererer *vedlikeholdsgjenstander* til anleggsmidler fra **Aktivastyring**-modulen, og *anleggsmidler* refererer til anleggsmidler fra **Anleggsmidler**-modulen.</span><span class="sxs-lookup"><span data-stu-id="f261f-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="f261f-108">Angi en standardlokasjon for nye vedlikeholdsgjenstander som opprettes fra anleggsmidler (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="f261f-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="f261f-109">Denne valgfrie konfiguasjonen gjør det mulig å angi et arbeidssted for nye vedlikeholdsgjenstander som opprettes fra anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="f261f-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="f261f-110">Du fullfører vanligvis denne konfigurasjonen bare én gang, hvis du fullfører den i det hele tatt.</span><span class="sxs-lookup"><span data-stu-id="f261f-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="f261f-111">Følg fremgangsmåten nedenfor for å fullføre konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="f261f-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="f261f-112">Gå til **Aktivastyring \> Oppsett \> Aktivabehandlingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="f261f-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="f261f-113">Velg standardstedet i kategorien **Anleggsmidler**, i **Arbeidssted**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f261f-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="f261f-114">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f261f-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="f261f-115">Arbeide med integrerte vedlikeholdseiendeler og anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="f261f-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="f261f-116">Denne delen inneholder en samling prosedyrer som viser ulike måter du kan arbeide med funksjonene for integrert aktivakontroll og anleggsmidler på.</span><span class="sxs-lookup"><span data-stu-id="f261f-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="f261f-117">Knytte en eksisterende vedlikeholdsgjenstand til et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="f261f-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="f261f-118">Gjør følgende for å knytte en eksisterende vedlikeholdsgjenstand til et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="f261f-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="f261f-119">Gå til **Aktivastyring \> Aktiva \> Alle aktiva** (eller **Aktive aktiva**).</span><span class="sxs-lookup"><span data-stu-id="f261f-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="f261f-120">Velg et aktivum.</span><span class="sxs-lookup"><span data-stu-id="f261f-120">Select an asset.</span></span>
1. <span data-ttu-id="f261f-121">Velg et eksisterende anleggsmiddel i hurtigfanen **Anleggsmiddel** i feltet **Anleggsmiddelnummer**.</span><span class="sxs-lookup"><span data-stu-id="f261f-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="f261f-122">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f261f-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="f261f-123">Vis anleggsmidlet som er knyttet til en valgt vedlikeholdsgjenstand</span><span class="sxs-lookup"><span data-stu-id="f261f-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="f261f-124">Gjør følgende for å vise anleggsmidlet som er knyttet til en valgt vedlikeholdsgjenstand.</span><span class="sxs-lookup"><span data-stu-id="f261f-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="f261f-125">Gå til **Aktivastyring \> Aktiva \> Alle aktiva** (eller **Aktive aktiva**).</span><span class="sxs-lookup"><span data-stu-id="f261f-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="f261f-126">Velg et aktivum.</span><span class="sxs-lookup"><span data-stu-id="f261f-126">Select an asset.</span></span>
1. <span data-ttu-id="f261f-127">Velg koblingen i hurtigfanen **Anleggsmiddel** i feltet **Anleggsmiddelnummer**.</span><span class="sxs-lookup"><span data-stu-id="f261f-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="f261f-128">**Anleggsmidler**-siden for valgt aktiva åpnes.</span><span class="sxs-lookup"><span data-stu-id="f261f-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="f261f-129">(Denne siden blir vanligvis funnet under **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.)</span><span class="sxs-lookup"><span data-stu-id="f261f-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="f261f-130">Vise vedlikeholdsgjenstanden som er knyttet til et valgt anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="f261f-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="f261f-131">Gjør følgende for å vise vedlikeholdsgjenstanden som er knyttet til et valgt anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="f261f-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="f261f-132">Gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="f261f-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="f261f-133">Velg et aktivum.</span><span class="sxs-lookup"><span data-stu-id="f261f-133">Select an asset.</span></span>
1. <span data-ttu-id="f261f-134">På handlingsruten, i kategorien **Aktivastyring** i **Vis**-gruppen, velger du **Vedlikeholdsgjenstand**.</span><span class="sxs-lookup"><span data-stu-id="f261f-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="f261f-135">**Vedlikeholdsgjenstand**-siden for aktivaet som er knyttet til det valgte anleggsmidlet, åpnes.</span><span class="sxs-lookup"><span data-stu-id="f261f-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="f261f-136">(Denne siden finnes vanligvis under **Aktivastyring \> Anleggsmidler \> Alle anleggsmidler**.)</span><span class="sxs-lookup"><span data-stu-id="f261f-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="f261f-137">Vise vedlikeholdskostnader som er knyttet til et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="f261f-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="f261f-138">Arbeidsordrer for aktivakontroll kan posteres for vedlikeholdsgjenstander, og hver arbeidsordre har vanligvis en pris.</span><span class="sxs-lookup"><span data-stu-id="f261f-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="f261f-139">Når et anleggsmiddel er knyttet til en vedlikeholdsgjenstand, kan du gå direkte fra anleggsmiddelet for å vise de tilknyttede kostnadene.</span><span class="sxs-lookup"><span data-stu-id="f261f-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="f261f-140">Gjør følgende for å vise vedlikeholdskostnadene som er knyttet til et valgt anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="f261f-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="f261f-141">Gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="f261f-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="f261f-142">Velg et aktivum.</span><span class="sxs-lookup"><span data-stu-id="f261f-142">Select an asset.</span></span>
1. <span data-ttu-id="f261f-143">På handlingsruten, i kategorien **Aktivastyring** i **Vis**-gruppen, velger du **Vedlikeholdskostnad**.</span><span class="sxs-lookup"><span data-stu-id="f261f-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="f261f-144">Siden **Vedlikeholdskostnad** åpnes, og viser de tilknyttede kostnadene.</span><span class="sxs-lookup"><span data-stu-id="f261f-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="f261f-145">Opprette en ny vedlikeholdsgjenstand for et eksisterende anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="f261f-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="f261f-146">Gjør følgende for å opprette en ny vedlikeholdsgjenstand for et eksisterende anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="f261f-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="f261f-147">Gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="f261f-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="f261f-148">Velg et aktivum.</span><span class="sxs-lookup"><span data-stu-id="f261f-148">Select an asset.</span></span>
1. <span data-ttu-id="f261f-149">På handlingsruten, i kategorien **Aktivastyring** i **Ny**-gruppen, velger du **Opprett vedlikeholdsgjenstand**.</span><span class="sxs-lookup"><span data-stu-id="f261f-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="f261f-150">(Hvis dette alternativet ikke er tilgjengelig, kan det hende at et vedlikeholdsgjenstanden allerede er knyttet til det valgte anleggsmidlet.)</span><span class="sxs-lookup"><span data-stu-id="f261f-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="f261f-151">Fullfør opprettelsen av aktivumet som beskrevet i [Opprette et aktiva](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="f261f-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="f261f-152">Opprette et nytt anleggsmiddel og legge til en ny vedlikeholdsgjenstand for det</span><span class="sxs-lookup"><span data-stu-id="f261f-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="f261f-153">Gjør følgende for å opprette et nytt anleggsmiddel og legge til en ny vedlikeholdsgjenstand for det.</span><span class="sxs-lookup"><span data-stu-id="f261f-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="f261f-154">Gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="f261f-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="f261f-155">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f261f-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f261f-156">Fullfør opprettelsen av anleggsmidlet som beskrevet i [Opprette et anleggsmiddel](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="f261f-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="f261f-157">På handlingsruten, i kategorien **Aktivastyring** i **Ny**-gruppen, velger du **Opprett vedlikeholdsgjenstand**.</span><span class="sxs-lookup"><span data-stu-id="f261f-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="f261f-158">Fullfør opprettelsen av aktivumet som beskrevet i [Opprette et aktiva](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="f261f-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="f261f-159">Fjerne tilknytningen mellom to anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="f261f-159">Remove the association between two assets</span></span>

<span data-ttu-id="f261f-160">I noen tilfeller kan det hende at du må fjerne tilknytningen for en vedlikeholdsgjenstand til anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="f261f-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="f261f-161">Hvis du for eksempel vil [opprette en ny vedlikeholdsgjenstand](#new-maintenance-from-fixed) fra et anleggsmiddel, må du først fjerne en eventuell eksisterende tilknytning.</span><span class="sxs-lookup"><span data-stu-id="f261f-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="f261f-162">Gjør følgende for å fjerne en tilknytning mellom en vedlikeholdsgjenstand og et anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="f261f-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="f261f-163">Gå til **Aktivastyring \> Aktiva \> Alle aktiva** (eller **Aktive aktiva**).</span><span class="sxs-lookup"><span data-stu-id="f261f-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="f261f-164">Finn og åpne anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="f261f-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="f261f-165">I hurtigfanen **Anleggsmiddel** fjerner du verdien fra **Arbeidssted**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f261f-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="f261f-166">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f261f-166">On the Action Pane, select **Save**.</span></span>

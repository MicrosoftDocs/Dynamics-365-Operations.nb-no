---
title: Definere et lager
description: Dette emnet beskriver hvordan du definerer et lager som skal brukes med en ny kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113765"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="6c7b9-103">Lageroppsett</span><span class="sxs-lookup"><span data-stu-id="6c7b9-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6c7b9-104">Dette emnet beskriver hvordan du definerer et lager som skal brukes med en ny kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6c7b9-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="6c7b9-105">Overview</span></span>

<span data-ttu-id="6c7b9-106">Hver handelskanal krever at et konfigurert lager er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="6c7b9-107">Fremgangsmåtene nedenfor angir minimumskonfigurasjonen som kreves for å definere et lager for en handelskanal.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="6c7b9-108">Hvis du vil ha mer informasjon om lageroppsett, kan du se [Oversikt over lagerstyring](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6c7b9-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="6c7b9-109">Konfigurere et lagerområde</span><span class="sxs-lookup"><span data-stu-id="6c7b9-109">Configure a warehouse site</span></span>

<span data-ttu-id="6c7b9-110">Før du setter opp et lager, må du konfigurere et lagerområde.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="6c7b9-111">Følg denne fremgangsmåten for å konfigurere et lagerområde.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="6c7b9-112">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Områder**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="6c7b9-113">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6c7b9-114">Angi en verdi i feltet **Område**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="6c7b9-115">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="6c7b9-116">I **Generelt**-delen angir du aktuell **Tidssone**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="6c7b9-117">Angi en adresse i **Addresser**-delen.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="6c7b9-118">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6c7b9-119">Bildet nedenfor viser et eksempel på et lagerområde.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-119">The following image shows an example warehouse site.</span></span>

![Eksempel på lagerområde](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="6c7b9-121">Definere et lager</span><span class="sxs-lookup"><span data-stu-id="6c7b9-121">Set up a warehouse</span></span>

<span data-ttu-id="6c7b9-122">Følg denne fremgangsmåten for å definere et lager.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="6c7b9-123">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6c7b9-124">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6c7b9-125">Angi en verdi i feltet **Lager**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="6c7b9-126">Hvis dette er en 1:1-tilordning til en butikk, kan du vurdere å bruke butikknavnet eller navnet på et regionalt distribusjonssenter.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="6c7b9-127">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="6c7b9-128">I rullegardinlisten **Område** velger du lagerområdet som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="6c7b9-129">I feltet **Type** velger du **Standard**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="6c7b9-130">Hvis du vil angi et **Karantenelager**, må du først følge disse trinnene for å opprette et ekstra lager, der **Type** er satt til **Karantene**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="6c7b9-131">Hvis du vil angi et **Transittlager**, må du først følge disse trinnene for å opprette et ekstra lager, der **Type** er satt til **Transitt**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="6c7b9-132">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="6c7b9-133">Definer lagerganger</span><span class="sxs-lookup"><span data-stu-id="6c7b9-133">Set up inventory aisles</span></span>

<span data-ttu-id="6c7b9-134">Hvis du vil konfigurere lagerganger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="6c7b9-135">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lokasjonsoppsett \> Lagerganger**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="6c7b9-136">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6c7b9-137">I rullegardinlisten **Lager** velger du lageret som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="6c7b9-138">I **Gang**-feltet skriver du inn et navn (for eksempel "Std").</span><span class="sxs-lookup"><span data-stu-id="6c7b9-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="6c7b9-139">I **Navn**-feltet skriver du inn et navn (for eksempel "Standard gang").</span><span class="sxs-lookup"><span data-stu-id="6c7b9-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="6c7b9-140">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="6c7b9-141">Konfigurere lagerbeholdningslokasjoner</span><span class="sxs-lookup"><span data-stu-id="6c7b9-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="6c7b9-142">Følg denne fremgangs måten for å definere lagerbeholdningslokasjoner for standard, skadet og returnert beholdning.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="6c7b9-143">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6c7b9-144">Velg lageret du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="6c7b9-145">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="6c7b9-146">I handlingsruten velger du **Lager** og deretter **Beholdningssted**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="6c7b9-147">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-147">On the action pane, select **New**.</span></span> <span data-ttu-id="6c7b9-148">Rullegardinlisten **Lager** skal vise det nye lageret som standard.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6c7b9-149">I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="6c7b9-150">Sett **Manuell oppdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="6c7b9-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6c7b9-151">I **Sted**-boksen angir du navnet på lageret.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="6c7b9-152">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="6c7b9-153">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="6c7b9-154">Rullegardinlisten **Lager** skal vise det nye lageret som standard.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6c7b9-155">I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="6c7b9-156">Sett **Manuell oppdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="6c7b9-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6c7b9-157">I **Sted**-boksen angir du "Skadet".</span><span class="sxs-lookup"><span data-stu-id="6c7b9-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="6c7b9-158">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="6c7b9-159">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="6c7b9-160">Rullegardinlisten **Lager** skal vise det nye lageret som standard.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="6c7b9-161">I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="6c7b9-162">Sett **Manuell oppdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="6c7b9-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="6c7b9-163">I **Sted**-boksen angir du "Returer".</span><span class="sxs-lookup"><span data-stu-id="6c7b9-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="6c7b9-164">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="6c7b9-165">Følgende bilde viser et oppsett av en lagerlokasjon i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Eksempel på lagerlokasjonsoppsett](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="6c7b9-167">Komplett lageroppsett</span><span class="sxs-lookup"><span data-stu-id="6c7b9-167">Complete warehouse setup</span></span>

<span data-ttu-id="6c7b9-168">Følg fremgangsmåten nedenfor for å fullføre lageroppsettet.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="6c7b9-169">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="6c7b9-170">Velg lageret du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="6c7b9-171">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="6c7b9-172">Under **Lagerstyring**:</span><span class="sxs-lookup"><span data-stu-id="6c7b9-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="6c7b9-173">Angi **Standard tilgangssted** til standardstedet som er opprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="6c7b9-174">Angi **Standard avgangssted** til standardstedet som er opprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="6c7b9-175">Under **Adresser**-delen angir du en lageradresse.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="6c7b9-176">Under **Detaljhandel**-delen:</span><span class="sxs-lookup"><span data-stu-id="6c7b9-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="6c7b9-177">I boksen **Standardreturlokasjon** angir du returlokasjonen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="6c7b9-178">Sett **Butikk** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="6c7b9-179">Sett **Vekt** til **1,00**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="6c7b9-180">I boksen **Lagringsdimensjoner** angir du standardlokasjonen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="6c7b9-181">Under **Lager**-delen setter du **Fysisk negativt lager** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="6c7b9-182">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6c7b9-183">Følgende bilde viser detaljer for et konfigurert lager.</span><span class="sxs-lookup"><span data-stu-id="6c7b9-183">The following image shows details for a configured warehouse.</span></span>

![Eksempel på konfigurert lager](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="6c7b9-185">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6c7b9-185">Additional resources</span></span>

[<span data-ttu-id="6c7b9-186">Oversikt over lagerstyring</span><span class="sxs-lookup"><span data-stu-id="6c7b9-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6c7b9-187">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="6c7b9-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6c7b9-188">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="6c7b9-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6c7b9-189">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="6c7b9-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="6c7b9-190">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="6c7b9-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="6c7b9-191">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="6c7b9-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)






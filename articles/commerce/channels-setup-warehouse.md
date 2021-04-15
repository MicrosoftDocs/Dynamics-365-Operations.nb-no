---
title: Definere et lager
description: Dette emnet beskriver hvordan du definerer et lager som skal brukes med en ny kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800501"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="13f6e-103">Lageroppsett</span><span class="sxs-lookup"><span data-stu-id="13f6e-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13f6e-104">Dette emnet beskriver hvordan du definerer et lager som skal brukes med en ny kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="13f6e-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="13f6e-105">Hver handelskanal krever at et konfigurert lager er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="13f6e-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="13f6e-106">Fremgangsmåtene nedenfor angir minimumskonfigurasjonen som kreves for å definere et lager for en handelskanal.</span><span class="sxs-lookup"><span data-stu-id="13f6e-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="13f6e-107">Hvis du vil ha mer informasjon om lageroppsett, kan du se [Oversikt over lagerstyring](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="13f6e-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="13f6e-108">Konfigurere et lagerområde</span><span class="sxs-lookup"><span data-stu-id="13f6e-108">Configure a warehouse site</span></span>

<span data-ttu-id="13f6e-109">Før du setter opp et lager, må du konfigurere et lagerområde.</span><span class="sxs-lookup"><span data-stu-id="13f6e-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="13f6e-110">Følg denne fremgangsmåten for å konfigurere et lagerområde.</span><span class="sxs-lookup"><span data-stu-id="13f6e-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="13f6e-111">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Områder**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="13f6e-112">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="13f6e-113">Angi en verdi i feltet **Område**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="13f6e-114">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="13f6e-115">I **Generelt**-delen angir du aktuell **Tidssone**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="13f6e-116">Angi en adresse i **Addresser**-delen.</span><span class="sxs-lookup"><span data-stu-id="13f6e-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="13f6e-117">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="13f6e-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="13f6e-118">Bildet nedenfor viser et eksempel på et lagerområde.</span><span class="sxs-lookup"><span data-stu-id="13f6e-118">The following image shows an example warehouse site.</span></span>

![Eksempel på lagerområde](media/warehouse-site.png)

## <a name="set-up-a-warehouse&quot;></a><span data-ttu-id=&quot;13f6e-120&quot;>Definere et lager</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-120&quot;>Set up a warehouse</span></span>

<span data-ttu-id=&quot;13f6e-121&quot;>Følg denne fremgangsmåten for å definere et lager.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-121&quot;>To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id=&quot;13f6e-122&quot;>I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-122&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id=&quot;13f6e-123&quot;>I handlingsruten velger du **Ny**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-123&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;13f6e-124&quot;>Angi en verdi i feltet **Lager**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-124&quot;>In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id=&quot;13f6e-125&quot;>Hvis dette er en 1:1-tilordning til en butikk, kan du vurdere å bruke butikknavnet eller navnet på et regionalt distribusjonssenter.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-125&quot;>If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id=&quot;13f6e-126&quot;>Angi en verdi i feltet **Navn**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-126&quot;>In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id=&quot;13f6e-127&quot;>I rullegardinlisten **Område** velger du lagerområdet som ble opprettet tidligere.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-127&quot;>In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id=&quot;13f6e-128&quot;>I feltet **Type** velger du **Standard**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-128&quot;>In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id=&quot;13f6e-129&quot;>Hvis du vil angi et **Karantenelager**, må du først følge disse trinnene for å opprette et ekstra lager, der **Type** er satt til **Karantene**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-129&quot;>If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id=&quot;13f6e-130&quot;>Hvis du vil angi et **Transittlager**, må du først følge disse trinnene for å opprette et ekstra lager, der **Type** er satt til **Transitt**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-130&quot;>If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id=&quot;13f6e-131&quot;>Velg **Lagre** i handlingsruten.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-131&quot;>On the action pane, select **Save**.</span></span>

## <a name=&quot;set-up-inventory-aisles&quot;></a><span data-ttu-id=&quot;13f6e-132&quot;>Definer lagerganger</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-132&quot;>Set up inventory aisles</span></span>

<span data-ttu-id=&quot;13f6e-133&quot;>Hvis du vil konfigurere lagerganger, følger du disse trinnene.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-133&quot;>To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id=&quot;13f6e-134&quot;>I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lokasjonsoppsett \> Lagerganger**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-134&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id=&quot;13f6e-135&quot;>I handlingsruten velger du **Ny**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-135&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;13f6e-136&quot;>I rullegardinlisten **Lager** velger du lageret som ble opprettet tidligere.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;13f6e-136&quot;>In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id=&quot;13f6e-137&quot;>I **Gang**-feltet skriver du inn et navn (for eksempel &quot;Std").</span><span class="sxs-lookup"><span data-stu-id="13f6e-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="13f6e-138">I **Navn**-feltet skriver du inn et navn (for eksempel "Standard gang").</span><span class="sxs-lookup"><span data-stu-id="13f6e-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="13f6e-139">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="13f6e-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="13f6e-140">Konfigurere lagerbeholdningslokasjoner</span><span class="sxs-lookup"><span data-stu-id="13f6e-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="13f6e-141">Følg denne fremgangs måten for å definere lagerbeholdningslokasjoner for standard, skadet og returnert beholdning.</span><span class="sxs-lookup"><span data-stu-id="13f6e-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="13f6e-142">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="13f6e-143">Velg lageret du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="13f6e-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="13f6e-144">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="13f6e-145">I handlingsruten velger du **Lager** og deretter **Beholdningssted**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="13f6e-146">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-146">On the action pane, select **New**.</span></span> <span data-ttu-id="13f6e-147">Rullegardinlisten **Lager** skal vise det nye lageret som standard.</span><span class="sxs-lookup"><span data-stu-id="13f6e-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="13f6e-148">I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="13f6e-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="13f6e-149">Sett **Manuell oppdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="13f6e-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="13f6e-150">I **Sted**-boksen angir du navnet på lageret.</span><span class="sxs-lookup"><span data-stu-id="13f6e-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="13f6e-151">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="13f6e-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="13f6e-152">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="13f6e-153">Rullegardinlisten **Lager** skal vise det nye lageret som standard.</span><span class="sxs-lookup"><span data-stu-id="13f6e-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="13f6e-154">I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="13f6e-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="13f6e-155">Sett **Manuell oppdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="13f6e-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="13f6e-156">I **Sted**-boksen angir du "Skadet".</span><span class="sxs-lookup"><span data-stu-id="13f6e-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="13f6e-157">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="13f6e-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="13f6e-158">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="13f6e-159">Rullegardinlisten **Lager** skal vise det nye lageret som standard.</span><span class="sxs-lookup"><span data-stu-id="13f6e-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="13f6e-160">I **Gang**-boksen skriver du inn navnet på gangen du angav tidligere.</span><span class="sxs-lookup"><span data-stu-id="13f6e-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="13f6e-161">Sett **Manuell oppdatering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="13f6e-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="13f6e-162">I **Sted**-boksen angir du "Returer".</span><span class="sxs-lookup"><span data-stu-id="13f6e-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="13f6e-163">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="13f6e-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="13f6e-164">Følgende bilde viser et oppsett av en lagerlokasjon i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="13f6e-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Eksempel på lagerlokasjonsoppsett](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="13f6e-166">Komplett lageroppsett</span><span class="sxs-lookup"><span data-stu-id="13f6e-166">Complete warehouse setup</span></span>

<span data-ttu-id="13f6e-167">Følg fremgangsmåten nedenfor for å fullføre lageroppsettet.</span><span class="sxs-lookup"><span data-stu-id="13f6e-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="13f6e-168">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Lagre**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="13f6e-169">Velg lageret du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="13f6e-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="13f6e-170">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="13f6e-171">Under **Lagerstyring**:</span><span class="sxs-lookup"><span data-stu-id="13f6e-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="13f6e-172">Angi **Standard tilgangssted** til standardstedet som er opprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="13f6e-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="13f6e-173">Angi **Standard avgangssted** til standardstedet som er opprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="13f6e-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="13f6e-174">Under **Adresser**-delen angir du en lageradresse.</span><span class="sxs-lookup"><span data-stu-id="13f6e-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="13f6e-175">Under **Detaljhandel**-delen:</span><span class="sxs-lookup"><span data-stu-id="13f6e-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="13f6e-176">I boksen **Standardreturlokasjon** angir du returlokasjonen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="13f6e-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="13f6e-177">Sett **Butikk** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="13f6e-178">Sett **Vekt** til **1,00**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="13f6e-179">I boksen **Lagringsdimensjoner** angir du standardlokasjonen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="13f6e-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="13f6e-180">Under **Lager**-delen setter du **Fysisk negativt lager** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="13f6e-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="13f6e-181">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="13f6e-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="13f6e-182">Følgende bilde viser detaljer for et konfigurert lager.</span><span class="sxs-lookup"><span data-stu-id="13f6e-182">The following image shows details for a configured warehouse.</span></span>

![Eksempel på konfigurert lager](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="13f6e-184">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="13f6e-184">Additional resources</span></span>

[<span data-ttu-id="13f6e-185">Oversikt over lagerstyring</span><span class="sxs-lookup"><span data-stu-id="13f6e-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="13f6e-186">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="13f6e-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="13f6e-187">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="13f6e-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="13f6e-188">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="13f6e-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="13f6e-189">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="13f6e-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="13f6e-190">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="13f6e-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]

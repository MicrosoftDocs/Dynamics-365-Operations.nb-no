---
title: Ta i bruk innstillinger for beholdning
description: Dette emnet dekker beholdningsinnstillinger og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dd3db0039525c18521ad6a42b2f281976b7b236a
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937416"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="4f3f7-103">Bruke lagerinnstillinger</span><span class="sxs-lookup"><span data-stu-id="4f3f7-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4f3f7-104">Dette emnet dekker beholdningsinnstillinger og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4f3f7-105">Beholdningsinnstillinger angir om beholdningen skal kontrolleres før produkter legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="4f3f7-106">De definerer også beholdningsrelaterte varemeldinger som for eksempel "På lager" og "Bare noen få igjen."</span><span class="sxs-lookup"><span data-stu-id="4f3f7-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="4f3f7-107">Disse innstillingene sikrer at et produkt ikke kan kjøpes hvis det ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="4f3f7-108">Dynamics 365 Commerce gir estimater for tilgjengelig beholdning for produkter.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="4f3f7-109">Hvis du vil ha informasjon om hvordan estimert beholdningstilgjengelighet blir beregnet, kan du se [Beregne beholdningstilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="4f3f7-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="4f3f7-110">I Commerce Site Builder kan du definere beholdningsterskler og -områder for et produkt eller en kategori.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="4f3f7-111">De bestemmer om beholdningen kan klassifiseres som på lager, få på lager eller tomt på lager.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="4f3f7-112">Hvis du vil ha mer informasjon, kan du se [Konfigurere beholdningsbuffere og beholdningsnivåer](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4f3f7-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4f3f7-113">Støtte for beholdningsterskler og -områder er tilgjengelig i Dynamics 365 Commerce 10.0.12-versjonen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="4f3f7-114">Beholdningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="4f3f7-114">Inventory settings</span></span>

<span data-ttu-id="4f3f7-115">I Commerce defineres beholdningsinnstillinger fra **Områdeinnstillinger \> Utvidelser \> Lagerstyring** i områdebygger.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="4f3f7-116">Det finnes fem beholdningsinnstillinger, hvorav én er foreldet (avviklet):</span><span class="sxs-lookup"><span data-stu-id="4f3f7-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="4f3f7-117">**Aktiver lagersjekk i app** – Denne innstillingen aktiverer en beholdningssjekk for et produkt.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="4f3f7-118">Kjøpsboks-, handlekurv- og hent i butikk-moduler kontrollerer deretter varebeholdningen, og gjør det bare mulig å legge til et produkt i handlekurven hvis varen er tilgjengelig på lager.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="4f3f7-119">**Beholdningsnivå basert på** – denne innstillingen definerer hvordan beholdningsnivåene beregnes.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="4f3f7-120">De tilgjengelige verdiene er **Total tilgjengelig**, **Fysisk tilgjengelig** og **Terskel for tomt på lager**.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="4f3f7-121">I Commerce kan du definere beholdningsterskler og -områder for hvert produkt og hver kategori.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="4f3f7-122">Beholdnings-API-ene returnerer beholdningsinformasjon for produkter for både **Totalt tilgjengelig**-egenskapen og **Fysisk tilgjengelig**-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="4f3f7-123">Forhandleren avgjør om **Totalt tilgjengelig**- eller **Fysisk tilgjengelig**-verdien skal brukes til å fastslå beholdningsantallet og de tilsvarende områdene for statusene "tilgjengelig på lager" og "tomt på lager".</span><span class="sxs-lookup"><span data-stu-id="4f3f7-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="4f3f7-124">**Terskel for tomt på lager**-verdien for **Beholdningsnivå basert på**-innstillingen er en foreldet verdi.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="4f3f7-125">Når den er valgt, bestemmes beholdningstellingen av resultatene av **Totalt tilgjengelig**-verdien, men terskelen defineres av den numeriske **Terskel for tomt på lager**-innstillingen som beskrives senere.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="4f3f7-126">Denne terskelinnstillingen gjelder for alle produkter på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="4f3f7-127">Hvis beholdningen er lavere enn terskelantallet, anses produktet å være tomt på lager.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="4f3f7-128">Hvis ikke anses det å være på lager.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="4f3f7-129">Egenskapene til **Terskel for tomt på lager**-verdien er begrenset, og vi anbefaler at du ikke bruker den i versjon 10.0.12 og nyere.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="4f3f7-130">**Lagernivå for flere lagre** – Denne innstillingen gjør at lagernivået kan beregnes mot standardlageret eller flere lagre.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="4f3f7-131">Alternativet **Basert på individuelt lager** vil det beregne lagernivåer basert på standardlageret.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="4f3f7-132">Et e-handelsområde kan også peke til flere lagre for å legge til rette for innfrielse.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="4f3f7-133">I så fall brukes alternativet **Basert på aggregat for lagre for forsendelse og henting** for å angi lagertilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="4f3f7-134">Hvis for eksempel en kunde kjøper en vare og velger "forsendelse" som leveringsmåte, kan varen sendes fra et hvilket som helst lager i innfrielsesgruppen som har tilgjengelig lager.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="4f3f7-135">Siden med produktdetaljer (PDP) vil vise en "På lager"-melding for forsendelse hvis et tilgjengelig forsendelseslager i oppfyllelsesgruppen har lager.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="4f3f7-136">Innstillingen **Lagernivå for flere lagre** er tilgjengelig fra og med Commerce-versjon 10.0.19-utgivelsen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="4f3f7-137">Hvis du oppdaterer fra en eldre versjon av Commerce, må du manuelt oppdatere appsettings.json-filen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="4f3f7-138">Hvis du vil ha instruksjoner, kan du se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="4f3f7-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="4f3f7-139">**Beholdningsområder** – denne innstillingen definerer beholdningsområdene meldingen vises for på områdemoduler.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="4f3f7-140">Den gjelder bare hvis enten den **Totalt tilgjengelig**-verdien eller **Fysisk tilgjengelig**-verdien er valgt for **Beholdningsnivå basert på**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="4f3f7-141">De tilgjengelige verdiene er **Alle**, **Få eller tomt på lager** og **Tomt på lager**.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="4f3f7-142">Når **Alle** er valgt, vises meldinger for alle beholdningsområder – fra på lager ("Tilgjengelig"-melding) til tomt på lager ("Tomt på lager"-meldingen).</span><span class="sxs-lookup"><span data-stu-id="4f3f7-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="4f3f7-143">Når **Få eller tomt på lager** er valgt, vises meldinger for alle beholdningsområder bortsett fra "på lager" ("Tilgjengelig"-melding).</span><span class="sxs-lookup"><span data-stu-id="4f3f7-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="4f3f7-144">Når **Tomt på lager** er valgt, vises bare "Tomt på lager"-meldingen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="4f3f7-145">**Terskel for tomt på lager** – denne gamle numeriske innstillingen vil bare tre i kraft hvis **Terskel for tomt på lager**-verdien er valgt for **Beholdningsnivå basert på**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="4f3f7-146">Disse innstillingene er tilgjengelige i Dynamics 365 Commerce 10.0.12-versjonen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="4f3f7-147">Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="4f3f7-148">Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="4f3f7-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="4f3f7-149">Moduler som bruker beholdningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="4f3f7-149">Modules that use inventory settings</span></span>

<span data-ttu-id="4f3f7-150">Modulene kjøpsboks, ønskeliste, butikkvelger, handlekurv og handlekurvikon bruker beholdningsinnstillinger for å vise beholdningsområder og -meldinger.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="4f3f7-151">I eksemplet i illustrasjonen nedenfor viser en PDP en finnes-på-lager-melding ("Tilgjengelig").</span><span class="sxs-lookup"><span data-stu-id="4f3f7-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![Eksempel på en PDP-modul med en "finnes på lager"-melding](./media/pdp-InStock.png)

<span data-ttu-id="4f3f7-153">I eksemplet i illustrasjonen nedenfor viser en PDP en "Tomt på lager"-melding.</span><span class="sxs-lookup"><span data-stu-id="4f3f7-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![Eksempel på en PDP-modul med en "ikke på lager"-melding](./media/pdp-outofstock.png)

<span data-ttu-id="4f3f7-155&quot;>I eksemplet i illustrasjonen nedenfor viser en handlevogn en finnes-på-lager-melding (&quot;Tilgjengelig").</span><span class="sxs-lookup"><span data-stu-id="4f3f7-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![Eksempel på en handlevognmodul med en "finnes på lager"-melding](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="4f3f7-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4f3f7-157">Additional resources</span></span>

[<span data-ttu-id="4f3f7-158">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="4f3f7-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4f3f7-159">Konfigurere lagerbuffere og lagernivåer</span><span class="sxs-lookup"><span data-stu-id="4f3f7-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="4f3f7-160">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="4f3f7-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4f3f7-161">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="4f3f7-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4f3f7-162">Kontobehandlingssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="4f3f7-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="4f3f7-163">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="4f3f7-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="4f3f7-164">Oppdateringer for SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="4f3f7-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

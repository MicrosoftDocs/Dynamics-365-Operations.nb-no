---
title: Ta i bruk innstillinger for beholdning
description: Dette emnet dekker beholdningsinnstillinger og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: b2c44eb5ece74de15e22180abc6d9d0448ab401b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798895"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="68b26-103">Bruke lagerinnstillinger</span><span class="sxs-lookup"><span data-stu-id="68b26-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68b26-104">Dette emnet dekker beholdningsinnstillinger og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68b26-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="68b26-105">Beholdningsinnstillinger angir om beholdningen skal kontrolleres før produkter legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="68b26-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="68b26-106">De definerer også beholdningsrelaterte varemeldinger som for eksempel "På lager" og "Bare noen få igjen."</span><span class="sxs-lookup"><span data-stu-id="68b26-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="68b26-107">Disse innstillingene sikrer at et produkt ikke kan kjøpes hvis det ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="68b26-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="68b26-108">Dynamics 365 Commerce gir estimater for tilgjengelig beholdning for produkter.</span><span class="sxs-lookup"><span data-stu-id="68b26-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="68b26-109">Hvis du vil ha informasjon om hvordan estimert beholdningstilgjengelighet blir beregnet, kan du se [Beregne beholdningstilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="68b26-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="68b26-110">I Commerce Site Builder kan du definere beholdningsterskler og -områder for et produkt eller en kategori.</span><span class="sxs-lookup"><span data-stu-id="68b26-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="68b26-111">De bestemmer om beholdningen kan klassifiseres som på lager, få på lager eller tomt på lager.</span><span class="sxs-lookup"><span data-stu-id="68b26-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="68b26-112">Hvis du vil ha mer informasjon, kan du se [Konfigurere beholdningsbuffere og beholdningsnivåer](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="68b26-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="68b26-113">Støtte for beholdningsterskler og -områder er tilgjengelig i Dynamics 365 Commerce 10.0.12-versjonen.</span><span class="sxs-lookup"><span data-stu-id="68b26-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="68b26-114">Beholdningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="68b26-114">Inventory settings</span></span>

<span data-ttu-id="68b26-115">I Commerce defineres beholdningsinnstillinger fra **Områdeinnstillinger \> Utvidelser \> Lagerstyring** i områdebygger.</span><span class="sxs-lookup"><span data-stu-id="68b26-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="68b26-116">Det finnes fire beholdningsinnstillinger, hvorav én er foreldet (avviklet):</span><span class="sxs-lookup"><span data-stu-id="68b26-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="68b26-117">**Aktiver lagersjekk i app** – Denne innstillingen aktiverer en beholdningssjekk for et produkt.</span><span class="sxs-lookup"><span data-stu-id="68b26-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="68b26-118">Kjøpsboks-, handlekurv- og hent i butikk-moduler kontrollerer deretter varebeholdningen, og gjør det bare mulig å legge til et produkt i handlekurven hvis varen er tilgjengelig på lager.</span><span class="sxs-lookup"><span data-stu-id="68b26-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="68b26-119">**Beholdningsnivå basert på** – denne innstillingen definerer hvordan beholdningsnivåene beregnes.</span><span class="sxs-lookup"><span data-stu-id="68b26-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="68b26-120">De tilgjengelige verdiene er **Total tilgjengelig**, **Fysisk tilgjengelig** og **Terskel for tomt på lager**.</span><span class="sxs-lookup"><span data-stu-id="68b26-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="68b26-121">I Commerce kan du definere beholdningsterskler og -områder for hvert produkt og hver kategori.</span><span class="sxs-lookup"><span data-stu-id="68b26-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="68b26-122">Beholdnings-API-ene returnerer beholdningsinformasjon for produkter for både **Totalt tilgjengelig**-egenskapen og **Fysisk tilgjengelig**-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="68b26-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="68b26-123">Forhandleren avgjør om **Totalt tilgjengelig**- eller **Fysisk tilgjengelig**-verdien skal brukes til å fastslå beholdningsantallet og de tilsvarende områdene for statusene "tilgjengelig på lager" og "tomt på lager".</span><span class="sxs-lookup"><span data-stu-id="68b26-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="68b26-124">**Terskel for tomt på lager**-verdien for **Beholdningsnivå basert på**-innstillingen er en foreldet verdi.</span><span class="sxs-lookup"><span data-stu-id="68b26-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="68b26-125">Når den er valgt, bestemmes beholdningstellingen av resultatene av **Totalt tilgjengelig**-verdien, men terskelen defineres av den numeriske **Terskel for tomt på lager**-innstillingen som beskrives senere.</span><span class="sxs-lookup"><span data-stu-id="68b26-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="68b26-126">Denne terskelinnstillingen gjelder for alle produkter på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="68b26-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="68b26-127">Hvis beholdningen er lavere enn terskelantallet, anses produktet å være tomt på lager.</span><span class="sxs-lookup"><span data-stu-id="68b26-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="68b26-128">Hvis ikke anses det å være på lager.</span><span class="sxs-lookup"><span data-stu-id="68b26-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="68b26-129">Egenskapene til **Terskel for tomt på lager**-verdien er begrenset, og vi anbefaler at du ikke bruker den i versjon 10.0.12 og nyere.</span><span class="sxs-lookup"><span data-stu-id="68b26-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="68b26-130">**Beholdningsområder** – denne innstillingen definerer beholdningsområdene meldingen vises for på områdemoduler.</span><span class="sxs-lookup"><span data-stu-id="68b26-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="68b26-131">Den gjelder bare hvis enten den **Totalt tilgjengelig**-verdien eller **Fysisk tilgjengelig**-verdien er valgt for **Beholdningsnivå basert på**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="68b26-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="68b26-132">De tilgjengelige verdiene er **Alle**, **Få eller tomt på lager** og **Tomt på lager**.</span><span class="sxs-lookup"><span data-stu-id="68b26-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="68b26-133">Når **Alle** er valgt, vises meldinger for alle beholdningsområder – fra på lager ("Tilgjengelig"-melding) til tomt på lager ("Tomt på lager"-meldingen).</span><span class="sxs-lookup"><span data-stu-id="68b26-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="68b26-134">Når **Få eller tomt på lager** er valgt, vises meldinger for alle beholdningsområder bortsett fra "på lager" ("Tilgjengelig"-melding).</span><span class="sxs-lookup"><span data-stu-id="68b26-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="68b26-135">Når **Tomt på lager** er valgt, vises bare "Tomt på lager"-meldingen.</span><span class="sxs-lookup"><span data-stu-id="68b26-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="68b26-136">**Terskel for tomt på lager** – denne gamle numeriske innstillingen vil bare tre i kraft hvis **Terskel for tomt på lager**-verdien er valgt for **Beholdningsnivå basert på**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="68b26-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="68b26-137">Disse innstillingene er tilgjengelige i Dynamics 365 Commerce 10.0.12-versjonen.</span><span class="sxs-lookup"><span data-stu-id="68b26-137">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="68b26-138">Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen.</span><span class="sxs-lookup"><span data-stu-id="68b26-138">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="68b26-139">Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="68b26-139">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="68b26-140">Moduler som bruker beholdningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="68b26-140">Modules that use inventory settings</span></span>

<span data-ttu-id="68b26-141">Modulene kjøpsboks, ønskeliste, butikkvelger, handlekurv og handlekurvikon bruker beholdningsinnstillinger for å vise beholdningsområder og -meldinger.</span><span class="sxs-lookup"><span data-stu-id="68b26-141">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="68b26-142">Bildet nedenfor viser et eksempel på en PDP-side (produktinformasjon) med en melding om at varen finnes på lager ("Tilgjengelig").</span><span class="sxs-lookup"><span data-stu-id="68b26-142">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Eksempel på en PDP-modul med en "finnes på lager"-melding](./media/pdp-InStock.png)

<span data-ttu-id="68b26-144">Bildet nedenfor viser et eksempel på en PDP med en "Tomt på lager"-melding.</span><span class="sxs-lookup"><span data-stu-id="68b26-144">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Eksempel på en PDP-modul med en "ikke på lager"-melding](./media/pdp-outofstock.png)

<span data-ttu-id="68b26-146&quot;>Bildet nedenfor viser et eksempel på en handlekurv med en melding om at varen finnes på lager (&quot;Tilgjengelig").</span><span class="sxs-lookup"><span data-stu-id="68b26-146">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Eksempel på en handlevognmodul med en "finnes på lager"-melding](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="68b26-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="68b26-148">Additional resources</span></span>

[<span data-ttu-id="68b26-149">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="68b26-149">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="68b26-150">Konfigurere lagerbuffere og lagernivåer</span><span class="sxs-lookup"><span data-stu-id="68b26-150">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="68b26-151">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="68b26-151">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="68b26-152">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="68b26-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="68b26-153">Kontobehandlingssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="68b26-153">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="68b26-154">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="68b26-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="68b26-155">Oppdateringer for SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="68b26-155">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

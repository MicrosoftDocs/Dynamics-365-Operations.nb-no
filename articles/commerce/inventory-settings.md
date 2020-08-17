---
title: Ta i bruk innstillinger for beholdning
description: Dette emnet dekker beholdningsinnstillinger og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 737e71dc73750bf151629fd904081924ac15b91e
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621227"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="6f3e0-103">Ta i bruk innstillinger for beholdning</span><span class="sxs-lookup"><span data-stu-id="6f3e0-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6f3e0-104">Dette emnet dekker beholdningsinnstillinger og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6f3e0-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="6f3e0-105">Overview</span></span>

<span data-ttu-id="6f3e0-106">Beholdningsinnstillinger angir om beholdningen skal kontrolleres før produkter legges til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="6f3e0-107">De definerer også beholdningsrelaterte varemeldinger som for eksempel "På lager" og "Bare noen få igjen."</span><span class="sxs-lookup"><span data-stu-id="6f3e0-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="6f3e0-108">Disse innstillingene sikrer at et produkt ikke kan kjøpes hvis det ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="6f3e0-109">Dynamics 365 Commerce gir estimater for tilgjengelig beholdning for produkter.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="6f3e0-110">Hvis du vil ha informasjon om hvordan estimert beholdningstilgjengelighet blir beregnet, kan du se [Beregne beholdningstilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="6f3e0-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="6f3e0-111">I Commerce Site Builder kan du definere beholdningsterskler og -områder for et produkt eller en kategori.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="6f3e0-112">De bestemmer om beholdningen kan klassifiseres som på lager, få på lager eller tomt på lager.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="6f3e0-113">Hvis du vil ha mer informasjon, kan du se [Konfigurere beholdningsbuffere og beholdningsnivåer](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="6f3e0-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="6f3e0-114">Beholdningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="6f3e0-114">Inventory settings</span></span>

<span data-ttu-id="6f3e0-115">I Commerce defineres beholdningsinnstillinger fra **Områdeinnstillinger \> Utvidelser \> Lagerstyring** i områdebygger.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="6f3e0-116">Det finnes fire beholdningsinnstillinger, hvorav én er foreldet (avviklet):</span><span class="sxs-lookup"><span data-stu-id="6f3e0-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="6f3e0-117">**Aktiver beholdningssjekk i app** – denne innstillingen aktiverer en beholdningssjekk for et produkt.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-117">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="6f3e0-118">Kjøpsboks-, handlekurv- og hent i butikk-moduler kontrollerer deretter varebeholdningen, og gjør det bare mulig å legge til et produkt i handlekurven hvis varen er tilgjengelig på lager.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="6f3e0-119">**Beholdningsnivå basert på** – denne innstillingen definerer hvordan beholdningsnivåene beregnes.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="6f3e0-120">De tilgjengelige verdiene er **Total tilgjengelig**, **Fysisk tilgjengelig** og **Terskel for tomt på lager**.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="6f3e0-121">I Commerce kan du definere beholdningsterskler og -områder for hvert produkt og hver kategori.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="6f3e0-122">Beholdnings-API-ene returnerer beholdningsinformasjon for produkter for både **Totalt tilgjengelig**-egenskapen og **Fysisk tilgjengelig**-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="6f3e0-123">Forhandleren avgjør om **Totalt tilgjengelig**- eller **Fysisk tilgjengelig**-verdien skal brukes til å fastslå beholdningsantallet og de tilsvarende områdene for statusene "tilgjengelig på lager" og "tomt på lager".</span><span class="sxs-lookup"><span data-stu-id="6f3e0-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="6f3e0-124">**Terskel for tomt på lager**-verdien for **Beholdningsnivå basert på**-innstillingen er en foreldet verdi.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="6f3e0-125">Når den er valgt, bestemmes beholdningstellingen av resultatene av **Totalt tilgjengelig**-verdien, men terskelen defineres av den numeriske **Terskel for tomt på lager**-innstillingen som beskrives senere.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="6f3e0-126">Denne terskelinnstillingen gjelder for alle produkter på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-126">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="6f3e0-127">Hvis beholdningen er lavere enn terskelantallet, anses produktet å være tomt på lager.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="6f3e0-128">Hvis ikke anses det å være på lager.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="6f3e0-129">Egenskapene til **Terskel for tomt på lager**-verdien er begrenset, og vi anbefaler at du ikke bruker den i versjon 10.0.12 og nyere.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="6f3e0-130">**Beholdningsområder** – denne innstillingen definerer beholdningsområdene meldingen vises for på områdemoduler.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="6f3e0-131">Den gjelder bare hvis enten den **Totalt tilgjengelig**-verdien eller **Fysisk tilgjengelig**-verdien er valgt for **Beholdningsnivå basert på**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="6f3e0-132">De tilgjengelige verdiene er **Alle**, **Få eller tomt på lager** og **Tomt på lager**.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="6f3e0-133">Når **Alle** er valgt, vises meldinger for alle beholdningsområder – fra på lager ("Tilgjengelig"-melding) til tomt på lager ("Tomt på lager"-meldingen).</span><span class="sxs-lookup"><span data-stu-id="6f3e0-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="6f3e0-134">Når **Få eller tomt på lager** er valgt, vises meldinger for alle beholdningsområder bortsett fra "på lager" ("Tilgjengelig"-melding).</span><span class="sxs-lookup"><span data-stu-id="6f3e0-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="6f3e0-135">Når **Tomt på lager** er valgt, vises bare "Tomt på lager"-meldingen.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="6f3e0-136">**Terskel for tomt på lager** – denne gamle numeriske innstillingen vil bare tre i kraft hvis **Terskel for tomt på lager**-verdien er valgt for **Beholdningsnivå basert på**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="6f3e0-137">Moduler som bruker beholdningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="6f3e0-137">Modules that use inventory settings</span></span>

<span data-ttu-id="6f3e0-138">Modulene kjøpsboks, ønskeliste, butikkvelger, handlekurv og handlekurvikon bruker beholdningsinnstillinger for å vise beholdningsområder og -meldinger.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-138">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="6f3e0-139">Bildet nedenfor viser et eksempel på en PDP-side (produktinformasjon) med en melding om at varen finnes på lager ("Tilgjengelig").</span><span class="sxs-lookup"><span data-stu-id="6f3e0-139">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Eksempel på en PDP-modul med en "finnes på lager"-melding](./media/pdp-InStock.png)

<span data-ttu-id="6f3e0-141">Bildet nedenfor viser et eksempel på en PDP med en "Tomt på lager"-melding.</span><span class="sxs-lookup"><span data-stu-id="6f3e0-141">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Eksempel på en PDP-modul med en "ikke på lager"-melding](./media/pdp-outofstock.png)

<span data-ttu-id="6f3e0-143">Bildet nedenfor viser et eksempel på en handlekurv med en melding om at varen finnes på lager ("Tilgjengelig").</span><span class="sxs-lookup"><span data-stu-id="6f3e0-143">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Eksempel på en handlevognmodul med en "finnes på lager"-melding](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="6f3e0-145">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6f3e0-145">Additional resources</span></span>

[<span data-ttu-id="6f3e0-146">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="6f3e0-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6f3e0-147">Konfigurere beholdningsbuffere og beholdningsnivåer</span><span class="sxs-lookup"><span data-stu-id="6f3e0-147">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="6f3e0-148">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="6f3e0-148">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6f3e0-149">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="6f3e0-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6f3e0-150">Kontobehandlingssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="6f3e0-150">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="6f3e0-151">Butikkvelgermodul</span><span class="sxs-lookup"><span data-stu-id="6f3e0-151">Store selector module</span></span>](store-selector.md)

---
title: Bruke måleenhetsinnstillinger
description: Dette emnet dekker måleenhetsinnstillinger og beskriver hvordan du bruker dem i Microsoft Microsoft Dynamics 365 Commerce.
author: anupamar-ms
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
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022380"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="fd7af-103">Bruke måleenhetsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="fd7af-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fd7af-104">Dette emnet dekker måleenhetsinnstillinger og beskriver hvordan du bruker dem i Microsoft Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fd7af-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fd7af-105">Et produkt kan selges i forskjellige enheter, for eksempel "hver", "par" og "dusin."</span><span class="sxs-lookup"><span data-stu-id="fd7af-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="fd7af-106">I Commerce Headquarters kan salg per-måleenheten defineres for et produkt, og vises på et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="fd7af-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="fd7af-107">Hvis for eksempel en forhandler selger et produkt både individuelt og i dusinvis, kan de tilgjengelige måleenhetene vises sammen med annen produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="fd7af-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="fd7af-108">I illustrasjonen nedenfor er det konfigurert en salg per-måleenhet for et produkt **hv** (hver) i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="fd7af-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Eksempel på et produkt som er konfigurert med en måleenhet i Commerce Headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="fd7af-110">Støtte for bruk og visning av måleenheten er tilgjengelig fra Commerce versjon 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="fd7af-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="fd7af-111">Måleenhetsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="fd7af-111">Unit of measure settings</span></span>

<span data-ttu-id="fd7af-112">Visningsinnstillinger for måleenhet defineres i Commerce-områdebygger på **Områdeinnstillinger \> Tillegg \> Vis måleenheter for produkter**.</span><span class="sxs-lookup"><span data-stu-id="fd7af-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="fd7af-113">Det finnes tre innstillinger som støttes:</span><span class="sxs-lookup"><span data-stu-id="fd7af-113">There are three supported settings:</span></span>

- <span data-ttu-id="fd7af-114">**Ikke vis** – Når denne innstillingen er valgt, viser ikke e-handelsområdet måleenheten for produktet.</span><span class="sxs-lookup"><span data-stu-id="fd7af-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="fd7af-115">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="fd7af-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="fd7af-116">**Vis i produktkjøpsopplevelsen**– Når denne innstillingen er valgt, vises måleenheten på produktdetaljer, handlekurv, kassen, ordrehistorikk og ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="fd7af-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="fd7af-117">**Vis i produktlesing og kjøpsopplevelse** – Når denne innstillingen er valgt, vises måleenheten på sidene for produktkjøpsopplevelse og også under produktlesingsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="fd7af-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="fd7af-118">Som en del av denne virkemåten vises måleenheter i søkeresultater og i produktsamlingsmoduler.</span><span class="sxs-lookup"><span data-stu-id="fd7af-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd7af-119">Visningsinnstillinger for måleenhet er tilgjengelige i Commerce versjon 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="fd7af-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="fd7af-120">Hvis du oppdaterer fra en eldre versjon av Commerce, må du manuelt oppdatere appsettings.json-filen.</span><span class="sxs-lookup"><span data-stu-id="fd7af-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="fd7af-121">Hvis du vil ha instruksjoner, kan du se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="fd7af-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="fd7af-122">Moduler som bruker måleenhetsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="fd7af-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="fd7af-123">Moduler som bruker måleenhetsinnstillingene, omfatter modulene kjøpsboks, ønskeliste, handlekurv, handlekurvikon, søkeresultatcontainer, produktsamling, utsjekking og moduler med ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="fd7af-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="fd7af-124">I eksemplet i illustrasjonen nedenfor viser en produktdetaljside (PDP) måleenheten (**hv**) for et produkt.</span><span class="sxs-lookup"><span data-stu-id="fd7af-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Eksempel på en PDP som viser måleenheten](./media/Productunit-PDP.png)

<span data-ttu-id="fd7af-126">I eksemplet i illustrasjonen nedenfor viser en produktsamlingsmoduls måleenheten (**hv**) for et produkt.</span><span class="sxs-lookup"><span data-stu-id="fd7af-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Eksempel på en produktsamlingsmodul som viser måleenheten](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="fd7af-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fd7af-128">Additional resources</span></span>

[<span data-ttu-id="fd7af-129">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="fd7af-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fd7af-130">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="fd7af-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fd7af-131">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="fd7af-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fd7af-132">Kontobehandlingssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="fd7af-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="fd7af-133">Oppdateringer for SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="fd7af-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

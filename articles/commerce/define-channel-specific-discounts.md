---
title: Definer kanalspesifikke rabatter
description: Forhandlere angir ofte ulike rabatter i forskjellige kanaler. Dette emnet beskriver begrepene du trenger å kjenne til for å opprette en rabatt for en bestemt kanal.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 539a6f2df46450c5e0fd18ba69501432d6f3fbdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414654"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="e3b0f-104">Definere kanalspesifikke rabatter</span><span class="sxs-lookup"><span data-stu-id="e3b0f-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3b0f-105">Dette emnet beskriver begrepene du trenger å kjenne til for å opprette en rabatt for en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="e3b0f-106">Kanalspesifikke rabatter</span><span class="sxs-lookup"><span data-stu-id="e3b0f-106">Channel-specific discounts</span></span>

<span data-ttu-id="e3b0f-107">Forhandlere tilbyr ofte ulike rabatter i forskjellige kanaler.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="e3b0f-108">Det kan gjøres for å målrette lokale markedsforhold eller for å forholde seg til konkurrerende forhandlere.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="e3b0f-109">Handel bruker prisgrupper til å definere kanalspesifikke rabatter.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="e3b0f-110">Prisgrupper kan tilordnes til én eller flere av følgende enheter: kanaler, kataloger, tilknytninger og fordelsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="e3b0f-111">Denne artikkelen inneholder informasjon om kanaler, men de samme konseptene gjelder for katalograbatter, tilknytningsrabatter og lojalitetsrabatter.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="e3b0f-112">Prisgrupper</span><span class="sxs-lookup"><span data-stu-id="e3b0f-112">Price groups</span></span>

<span data-ttu-id="e3b0f-113">[![Prisgrupper](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="e3b0f-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="e3b0f-114">Diagrammet over illustrerer relasjonen mellom enheter som kan være på en transaksjon (kanal, katalog, tilknytning, kunde, fordelskort) og de ulike typene rabatter som kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="e3b0f-115">Alle transaksjoner skjer i en kanal, slik at kanalen er garantert å finnes på en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="e3b0f-116">De gjenværende enhetene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-116">The remaining entities are optional.</span></span> <span data-ttu-id="e3b0f-117">Det er en kobling til en relatert prisgruppe på hver hoveddataside der du kan vise og legge til prisgrupper etter behov.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="e3b0f-118">En prisgruppe brukes til å relatere fire forskjellige typer enheter til rabatter, prisjusteringer og forretningsavtaler.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="e3b0f-119">Vi anbefaler at du planlegger en strategi for hvordan du navngir prisgrupper for å holde orden på dem.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="e3b0f-120">Ett alternativ er å bruke en bokstav eller tallprefiks eller suffiks til å skille mellom de ulike typene.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="e3b0f-121">For eksempel 1-xxxxx for kanalprisgrupper og 2-xxxxx i katalogprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="e3b0f-122">Det er fire forespørselssider som fokuserer på hver handelsenhet som kan ha rabatter som er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="e3b0f-123">**Prisgrupper for kanal** – Denne siden viser en liste over kanaler og rabatter som er koblet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="e3b0f-124">**Katalogprisgrupper** – Denne siden viser en liste over kataloger og rabatter som er koblet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="e3b0f-125">**Prisgrupper for fordelsprogram** – Denne siden viser en liste over fordelsprogrammer og rabatter som er koblet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="e3b0f-126">**Prisgrupper for tilknytninger** – Denne siden viser en liste over tilknytninger og rabatter som er koblet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="e3b0f-127">Eksempel på kanalrabattoppsett</span><span class="sxs-lookup"><span data-stu-id="e3b0f-127">Example channel discount set up</span></span>

<span data-ttu-id="e3b0f-128">Følgende eksempel viser oppgavene med å konfigurere en kanalrabatt.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="e3b0f-129">Du har for eksempel en kanal som kalles **Houston**, og du skal opprette en ny rabatt kalt **Tilbake til skolen**.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="e3b0f-130">Fordi pris- og rabattstrategien inneholder muligheten for kanalrabatter, oppretter du alltid en kanalspesifikk prisgruppe når du oppretter en kanal.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="e3b0f-131">Du har prisgruppen **Houston-PG**, og den er tilordnet til **Houston**-kanalen.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="e3b0f-132">Når du har opprettet den nye **Tilbake til skolen**-rabatten, må du klikke **Prisgrupper** øverst på **Rabatt**-siden.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="e3b0f-133">**Rabattprisgrupper**-siden åpnes.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="e3b0f-134">Deretter klikker du **Ny** og velger **Houston-PG**-prisgruppen.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="e3b0f-135">Nå kan du aktivere rabatten og overføre den til kanalen.</span><span class="sxs-lookup"><span data-stu-id="e3b0f-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3b0f-136">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e3b0f-136">Additional resources</span></span>

[<span data-ttu-id="e3b0f-137">Prisjusteringer og rabatter</span><span class="sxs-lookup"><span data-stu-id="e3b0f-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)

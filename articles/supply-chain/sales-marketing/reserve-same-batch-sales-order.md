---
title: Reservere samme parti for en salgsordre
description: "Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 2d6089d07b0f8bc1a36703b5b1c2f24af72770d5
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="cf6b0-103">Reservere samme parti for en salgsordre</span><span class="sxs-lookup"><span data-stu-id="cf6b0-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf6b0-104">Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="cf6b0-105">Samme partireservasjon gjør at du kan reservere beholdning for en salgsordrelinje mot ett lagerparti.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="cf6b0-106">En kunde som bestiller tapet, kan for eksempel be om at hele ordren fylles fra samme parti for å unngå manglende overensstemmelse mellom rullene.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="cf6b0-107">Hvis du vil definere et produkt slik at det bruker samme partireservasjon, må følgende innstillinger være aktive i varemodellgruppen, sporingsdimensjonsgruppen, og lagringsdimensjonsgruppen du tilordner til produktet:</span><span class="sxs-lookup"><span data-stu-id="cf6b0-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="cf6b0-108">**Varemodellgrupper** – Varemodellgruppen må ha feltene **Samme partivalg** og **Konsolider krav** valgt i feltgruppen **Reservering** for beholdningspolicyer.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="cf6b0-109">**Sporingsdimensjonsgrupper** – Sporingsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for partinummeret.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="cf6b0-110">**Lagringsdimensjonsgrupper** – Lagringsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for **Område** og **Lager**.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="cf6b0-111">Når du reserverer beholdning for et produkt på en salgsordrelinje som er definert for samme partivalg, prøver Microsoft Dynamics 365 for Finance and Operations å reservere det bestilte antallet fra ett lagerparti.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="cf6b0-112">Det tas også hensyn til eventuelle bestemte partiattributtbehov.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="cf6b0-113">Hvis antallet ikke kan fylles fra ett parti, vise siden **Samme partireservasjonskonflikt**.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="cf6b0-114">Denne siden beskriver problemene samt det du kan gjøre for å fortsette med reserveringen.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="cf6b0-115">Følgende forhold kan forhindre at partiet blir reservert:</span><span class="sxs-lookup"><span data-stu-id="cf6b0-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="cf6b0-116">Partidisposisjonskoden har **Blokker reservering** for salg flagget som **Blokkert**.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="cf6b0-117">Partiet er utløpt, basert på utløpsdatoen og eventuelle gjeldende salgbare dager for kunde.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="cf6b0-118">Varen kan fortsett vurderes for reservasjon hvis varemodellgruppen for varen er FEFO-datokontrollert, og hvis best-før-datoen er valgt som plukkekriteriet.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="cf6b0-119">Partiet har ikke nok holdbarhetsdager igjen, basert på utløpsdatoen og best-før-datoen, i tillegg til eventuelle salgbare dager for kunde.</span><span class="sxs-lookup"><span data-stu-id="cf6b0-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>






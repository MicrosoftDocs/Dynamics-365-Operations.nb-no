---
title: Reservere samme parti for en salgsordre
description: Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e101473c5b6958c7e0fb5c5fa80dccd3d9b467
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216028"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="5ea77-103">Reservere samme parti for en salgsordre</span><span class="sxs-lookup"><span data-stu-id="5ea77-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ea77-104">Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager.</span><span class="sxs-lookup"><span data-stu-id="5ea77-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="5ea77-105">Samme partireservasjon gjør at du kan reservere beholdning for en salgsordrelinje mot ett lagerparti.</span><span class="sxs-lookup"><span data-stu-id="5ea77-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="5ea77-106">En kunde som bestiller tapet, kan for eksempel be om at hele ordren fylles fra samme parti for å unngå manglende overensstemmelse mellom rullene.</span><span class="sxs-lookup"><span data-stu-id="5ea77-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="5ea77-107">Hvis du vil definere et produkt slik at det bruker samme partireservasjon, må følgende innstillinger være aktive i varemodellgruppen, sporingsdimensjonsgruppen, og lagringsdimensjonsgruppen du tilordner til produktet:</span><span class="sxs-lookup"><span data-stu-id="5ea77-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="5ea77-108">**Varemodellgrupper** – Varemodellgruppen må ha feltene **Samme partivalg** og **Konsolider krav** valgt i feltgruppen **Reservering** for beholdningspolicyer.</span><span class="sxs-lookup"><span data-stu-id="5ea77-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="5ea77-109">**Sporingsdimensjonsgrupper** – Sporingsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for partinummeret.</span><span class="sxs-lookup"><span data-stu-id="5ea77-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="5ea77-110">**Lagringsdimensjonsgrupper** – Lagringsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for **Område** og **Lager**.</span><span class="sxs-lookup"><span data-stu-id="5ea77-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="5ea77-111">Når du reserverer beholdning for et produkt på en salgsordrelinje som er definert for samme partivalg, prøver systemet å reservere det bestilte antallet fra ett lagerparti.</span><span class="sxs-lookup"><span data-stu-id="5ea77-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="5ea77-112">Det tas også hensyn til eventuelle bestemte partiattributtbehov.</span><span class="sxs-lookup"><span data-stu-id="5ea77-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="5ea77-113">Hvis antallet ikke kan fylles fra ett parti, vise siden **Samme partireservasjonskonflikt**.</span><span class="sxs-lookup"><span data-stu-id="5ea77-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="5ea77-114">Denne siden beskriver problemene samt det du kan gjøre for å fortsette med reserveringen.</span><span class="sxs-lookup"><span data-stu-id="5ea77-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="5ea77-115">Følgende forhold kan forhindre at partiet blir reservert:</span><span class="sxs-lookup"><span data-stu-id="5ea77-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="5ea77-116">Partidisposisjonskoden har **Blokker reservering** for salg flagget som **Blokkert**.</span><span class="sxs-lookup"><span data-stu-id="5ea77-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="5ea77-117">Partiet er utløpt, basert på utløpsdatoen og eventuelle gjeldende salgbare dager for kunde.</span><span class="sxs-lookup"><span data-stu-id="5ea77-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="5ea77-118">Varen kan fortsett vurderes for reservasjon hvis varemodellgruppen for varen er FEFO-datokontrollert, og hvis best-før-datoen er valgt som plukkekriteriet.</span><span class="sxs-lookup"><span data-stu-id="5ea77-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="5ea77-119">Partiet har ikke nok holdbarhetsdager igjen, basert på utløpsdatoen og best-før-datoen, i tillegg til eventuelle salgbare dager for kunde.</span><span class="sxs-lookup"><span data-stu-id="5ea77-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="5ea77-120">For varer som er knyttet til en lagringsdimensjonsgruppe som har aktivert **Bruk lagerstyringsprosesser**, kan du reservere bestemte partinumre ved å bruke et reservasjonshierarki med partinummer-lagerdimensjonen som er definert ovenfor lokasjonsdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="5ea77-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="5ea77-121">Med **Partireservering**-siden for salgs- og overføringsordrelinjer kan du også velge og reservere flere linjer basert på de tilgjengelige partinumrene.</span><span class="sxs-lookup"><span data-stu-id="5ea77-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="5ea77-122">Hvis du vil ha mer informasjon om hva du skal gjøre hvis du bruker et reservasjonshierarki som har partinummerdimensjonen under lokasjonen, kan du se [Fleksibel dimensjonsreservasjonspolicy for lagernivå](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="5ea77-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>

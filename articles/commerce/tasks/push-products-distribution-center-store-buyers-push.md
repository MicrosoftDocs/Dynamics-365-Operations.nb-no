---
title: " Overføre produkter fra distribusjonssenter til butikk ved hjelp av sentralt innkjøp"
description: Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle et sentralt innkjøp ved distribusjon av produkter fra en lokasjon til én eller flere butikker.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62eeb29e348c558e8954f656b89d90792b0c347b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023528"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="89015-103"> Overføre produkter fra distribusjonssenter til butikk ved hjelp av sentralt innkjøp</span><span class="sxs-lookup"><span data-stu-id="89015-103">Push products from distribution center to store using buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="89015-104">Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle et sentralt innkjøp ved distribusjon av produkter fra en lokasjon til én eller flere butikker.</span><span class="sxs-lookup"><span data-stu-id="89015-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="89015-105">Brukeren kan definere flere konfigurasjoner og få systemet til å foreslå hvordan produktene skal distribueres, eller manuelt angi hvor produktene skal distribueres og hvor mye som skal distribueres til hver butikk.</span><span class="sxs-lookup"><span data-stu-id="89015-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="89015-106">Denne prosedyren inneholder ikke oppsettet av dataene som skal brukes i det sentrale innkjøpet, for eksempel etterfyllingsregler, organisasjonshierarkier og vekt.</span><span class="sxs-lookup"><span data-stu-id="89015-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="89015-107">Denne prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="89015-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="89015-108">Gå til Kjøp etter ordre.</span><span class="sxs-lookup"><span data-stu-id="89015-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="89015-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="89015-109">Click New.</span></span>
3. <span data-ttu-id="89015-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="89015-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="89015-111">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="89015-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="89015-112">I Lager-feltet angir eller velger du et lager som har produkter med lagerbeholdningsantall.</span><span class="sxs-lookup"><span data-stu-id="89015-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="89015-113">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="89015-113">Click Add.</span></span>
7. <span data-ttu-id="89015-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="89015-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="89015-115">Angi eller velg et produkt i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="89015-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="89015-116">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="89015-116">Click Add.</span></span>
10. <span data-ttu-id="89015-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="89015-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="89015-118">Angi eller velg et variantprodukt i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="89015-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="89015-119">Når du angir et variantprodukt, opprettes linjer for hver variant.</span><span class="sxs-lookup"><span data-stu-id="89015-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="89015-120">Merk en rad i listen.</span><span class="sxs-lookup"><span data-stu-id="89015-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="89015-121">I feltet Antall overførte skriver du inn hvor mye av det valgte produktet du vil distribuere.</span><span class="sxs-lookup"><span data-stu-id="89015-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="89015-122">I feltet Tilleggsantall som skal overføres angir du hvor mange produkter som har tilgjengelig antall for distribusjon.</span><span class="sxs-lookup"><span data-stu-id="89015-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="89015-123">Angi Lokasjonsvekt i feltet Distribusjon.</span><span class="sxs-lookup"><span data-stu-id="89015-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="89015-124">Du kan velge å bruke andre regler for distribusjon for de andre typene.</span><span class="sxs-lookup"><span data-stu-id="89015-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="89015-125">Angi eller velg en verdi i feltet Etterfyllingshierarki.</span><span class="sxs-lookup"><span data-stu-id="89015-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="89015-126">Velg Ja i feltet Respekter sortimenter.</span><span class="sxs-lookup"><span data-stu-id="89015-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="89015-127">Klikk Beregn antall og se gjennom antallene som legges til i radene, i Lager-delen.</span><span class="sxs-lookup"><span data-stu-id="89015-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="89015-128">Klikk Opprett ordre.</span><span class="sxs-lookup"><span data-stu-id="89015-128">Click Create order.</span></span>
20. <span data-ttu-id="89015-129">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="89015-129">Click Yes.</span></span>

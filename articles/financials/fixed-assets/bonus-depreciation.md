---
title: Bonusavskrivning
description: Denne artikkelen gir en oversikt over funksjonaliteten for bonusavskrivning.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e05c0c195ddb948547ae008d050686bbcdc6ed3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "323324"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="0947e-103">Bonusavskrivning</span><span class="sxs-lookup"><span data-stu-id="0947e-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0947e-104">Denne artikkelen gir en oversikt over funksjonaliteten for bonusavskrivning.</span><span class="sxs-lookup"><span data-stu-id="0947e-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="0947e-105">For bonusavskrivning kan du ta ekstra- eller bonusavskrivningsbeløp i det første året som anleggsmidlet brukes og avskrives.</span><span class="sxs-lookup"><span data-stu-id="0947e-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="0947e-106">Bonusavskrivning må utføres før alle andre avskrivningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="0947e-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="0947e-107">Derfor er det best å bruke bonusavskrivning med tablåer der funksjonen Poster i økonomimodul er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="0947e-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="0947e-108">Du kan bruke alternativet **Slett transaksjoner som ikke er postert til økonomimodulen** for å slette historiske transaksjoner for tablåer som ikke posterer til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="0947e-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="0947e-109">Du kan deretter bruke bonusavskrivning senere i livssyklusen til aktiva ved å slette avskrivningstransaksjoner som allerede er postert.</span><span class="sxs-lookup"><span data-stu-id="0947e-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="0947e-110">Du kan beregne bonusavskrivning ved hjelp av forslagsprosessen, eller du kan opprette manuelle bonusavskrivningstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0947e-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="0947e-111">Du kan ikke opprette bonusavskrivningstransaksjoner hvis det finnes avskrivningstransaksjoner eller avskrivningsjusteringstransaksjoner for dette tablået for anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="0947e-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="0947e-112">Når du bruker forslagsprosessen til å beregne bonusavskrivning, inkluderes alle eksisterende bonustransaksjoner i beregningen av grunnlaget.</span><span class="sxs-lookup"><span data-stu-id="0947e-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="0947e-113">Beregningen omfatter også alle tidligere bonusavskrivninger som du har angitt manuelt for anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="0947e-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="0947e-114">Hvis mer enn én bonusavskrivning skal utføres for et anleggsmiddel, tas det hensyn til prioritet.</span><span class="sxs-lookup"><span data-stu-id="0947e-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="0947e-115">Hver bonus reduserer anleggsmiddelgrunnlaget for den neste bonusen.</span><span class="sxs-lookup"><span data-stu-id="0947e-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="0947e-116">Restverdien vurderes ikke i anleggsmiddelgrunnlaget for beregning av bonusavskrivning, og avskrivningskonvensjonen gjelder ikke for bonusavskrivning.</span><span class="sxs-lookup"><span data-stu-id="0947e-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="0947e-117">I USA kvalifiserer noen eiendommer som Section 179-eiendom.</span><span class="sxs-lookup"><span data-stu-id="0947e-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="0947e-118">Ved å bruke Section 179-fradraget kan du gjenopprette hele eller deler av kostnaden for noen eiendommer, opptil en grense.</span><span class="sxs-lookup"><span data-stu-id="0947e-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="0947e-119">Du kan gjenopprette kostnaden ved å trekke det fra i året der du setter i drift eiendommen.</span><span class="sxs-lookup"><span data-stu-id="0947e-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="0947e-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0947e-120">Example</span></span>
<span data-ttu-id="0947e-121">Følgende bonusavskrivninger er knyttet til et tablå for anleggsmiddel:</span><span class="sxs-lookup"><span data-stu-id="0947e-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="0947e-122">**Section 179:** 1 000,00, Prioritet 1</span><span class="sxs-lookup"><span data-stu-id="0947e-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="0947e-123">**Liberty Zone:** 30 prosent, prioritet 2</span><span class="sxs-lookup"><span data-stu-id="0947e-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="0947e-124">Kostnaden for anleggsmiddelanskaffelse er 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="0947e-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="0947e-125">Når bonusavskrivning beregnes, er det første bonusavskrivningsbeløpet 1 000,00 for Section 179-avskrivningen.</span><span class="sxs-lookup"><span data-stu-id="0947e-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="0947e-126">Det neste bonusavskrivningsbeløpet for Liberty Zone-avskrvningen, beregnes som følger:</span><span class="sxs-lookup"><span data-stu-id="0947e-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="0947e-127">Anskaffelseskostnad – 1 000 (Section 179-avskrivning) × 30 prosent = 1 200</span><span class="sxs-lookup"><span data-stu-id="0947e-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="0947e-128">Hvis bonusavskrivningsbeløpet er større enn den gjenstående anskaffelseskostnaden, er bonusavskrivningsbeløpet resultatet av bonusavskrivningsberegningen eller den gjenværende anskaffelseskostnaden, eller det beløpet som er minst.</span><span class="sxs-lookup"><span data-stu-id="0947e-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="0947e-129">Hvis den gjenstående anskaffelseskostnaden er 0 (null) eller mindre, genereres det ikke bonusavskrivningstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0947e-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="0947e-130">Når bonusavskrivning beregnes ved av forslagsprosessen, opprettes det en bonusavskrivningstransaksjon for alle bonusavskrivningspostene som er tilknyttet tablået for anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="0947e-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="0947e-131">Du kan opprette et ubegrenset antall bonusavskrivningsposter.</span><span class="sxs-lookup"><span data-stu-id="0947e-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="0947e-132">Når du har tildelt disse postene til tablået for anleggsmiddelgruppe, brukes de for anleggsmiddeltablået.</span><span class="sxs-lookup"><span data-stu-id="0947e-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="0947e-133">Bonusavskrivning angis som en prosent eller et fast beløp.</span><span class="sxs-lookup"><span data-stu-id="0947e-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="0947e-134">Når du posterer avskrivningsforslag, posteres bonusavskrivningstransaksjoner til tablået som transaksjoner som er atskilte fra avskrivningstransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="0947e-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>




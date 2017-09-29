---
title: Partiattributter
description: "Denne artikkelen inneholder informasjon om bunkeattributter. Partiattributter er egenskaper til råvarer og ferdige produkter som utgjør lagerpartier. Artikkelen forklarer også hvordan du tilordner bunkeattributter, og hvordan du kan søke etter dem når du reserverer partier."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c3f5115377178941984e53749c18cc1c9179812
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="batch-attributes"></a><span data-ttu-id="b3a1d-105">Partiattributter</span><span class="sxs-lookup"><span data-stu-id="b3a1d-105">Batch attributes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b3a1d-106">Denne artikkelen inneholder informasjon om bunkeattributter.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-106">This article provides information about batch attributes.</span></span> <span data-ttu-id="b3a1d-107">Partiattributter er egenskaper til råvarer og ferdige produkter som utgjør lagerpartier.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="b3a1d-108">Artikkelen forklarer også hvordan du tilordner bunkeattributter, og hvordan du kan søke etter dem når du reserverer partier.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-108">The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="b3a1d-109">Partiattributter er egenskaper til råvarer og ferdige produkter som utgjør lagerpartier.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="b3a1d-110">Partiattributter kan variere, avhengig av en rekke faktorer, for eksempel miljøfaktorer eller kvaliteten på råvarene som er brukt til å produsere partiet, eller resultatet av det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="b3a1d-111">Antallet av og typene partiattributter som brukes, kan variere kraftig i de ulike bransjene.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="b3a1d-112">Her er to eksempler som viser hvordan du bruker partiattributter:</span><span class="sxs-lookup"><span data-stu-id="b3a1d-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="b3a1d-113">I osteindustrien kan melk, som er en av råvarene som brukes i produksjonen av ost, ha attributter som for eksempel fettinnhold og prosentvekt.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="b3a1d-114">Osten som produseres av melken, kan ha andre attributter, for eksempel fuktighet og alder.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="b3a1d-115">I stålindustrien kan jern som produseres, ha attributter som for eksempel prosenter av magnesiuminnhold, sølvinnhold og sinkinnhold.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="b3a1d-116">For å få bedre styring av antall og typer attributter, kan du bruke partiattributtgrupper.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="b3a1d-117">På denne måten trenger du ikke legge til hvert attributt individuelt.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="b3a1d-118">Tilordne partiattributter</span><span class="sxs-lookup"><span data-stu-id="b3a1d-118">Assign batch attributes</span></span>
<span data-ttu-id="b3a1d-119">Du kan tilordne partiattributter til individuelle produkter som er i lagerparti, eller du kan tilordne dem til produkter som er knyttet til bestemte kunder.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="b3a1d-120">Før du kan tilordne et partiattributt på kundenivå, må du tilordne det på produktnivå.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="b3a1d-121">Produktet må ha partidimensjonen satt til **Aktiv** i sporingsdimensjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="b3a1d-122">Hvis du vil tilordne et partiattributt til et enkelt produkt, kan du bruke produktspesifikk-siden.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="b3a1d-123">Hvis attributtet er spesifikt for et produkt for en kunde, bruker du kundespesifikk-siden.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="b3a1d-124">Når du legger til et attributt til et produkt, kan du også angi andre parametere.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="b3a1d-125">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="b3a1d-125">Here are some examples:</span></span>

-   <span data-ttu-id="b3a1d-126">Minimums- og maksimumsområdene for et attributt av typen **Heltall** eller **Brøk**.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="b3a1d-127">Toleransehandlinger for et attributt av typen **heltall** eller **brøk**.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="b3a1d-128">Hvis verdien til attributtet faller utenfor minimums- og maksimumsområdet, kan handlingen enten være en advarsel eller en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="b3a1d-129">Målverdien for attributtet.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-129">The target value for the attribute.</span></span> <span data-ttu-id="b3a1d-130">Denne verdien er den optimale verdien for attributtet, og den gjelder for alle attributtyper.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="b3a1d-131">Du kan få tilgang til sidene for produkter som du velger på siden **Frigitte produkter** i Behandling av produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="b3a1d-132">Når du har tilordnet partiattributter til et produkt, kan du legge til bestemte verdier i attributtene på siden **Lagerpartiattributter**.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="b3a1d-133">Reservere partier </span><span class="sxs-lookup"><span data-stu-id="b3a1d-133">Reserve batches</span></span>
<span data-ttu-id="b3a1d-134">Du kan søke i partiattributter når du utfører partireservasjoner for en salgsordre for å oppfylle en kundeordre, eller når du plukker og reserverer partier for en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-134">You can search on batch attributes when you do batch reservations for a sales order to fullfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="b3a1d-135">Søket bidrar til å finne et lagerparti som inneholder produktet som har partiattributtet du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="b3a1d-136">Når du har funnet partiet eller partiene, kan du reservere produktet til den opprinnelige lagertransaksjonslinjen.</span><span class="sxs-lookup"><span data-stu-id="b3a1d-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>





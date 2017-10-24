--- 
title: Opprette et ferdig produkt (bare februar 2016)
description: "Denne oppgaven fokuserer på å opprette et ferdig produkt."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5485c949e932572542ba22e052007e9625e20314
ms.openlocfilehash: a14b56b508e5d46bb2898828bd30fdf6c3c14023
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="4abbc-103">Opprette et ferdig produkt (bare februar 2016)</span><span class="sxs-lookup"><span data-stu-id="4abbc-103">Create a finished product (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4abbc-104">Denne oppgaven fokuserer på å opprette et ferdig produkt.</span><span class="sxs-lookup"><span data-stu-id="4abbc-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="4abbc-105">Det er den første oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="4abbc-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="4abbc-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="4abbc-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="4abbc-107">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="4abbc-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4abbc-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4abbc-108">Click New.</span></span>
3. <span data-ttu-id="4abbc-109">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="4abbc-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="4abbc-110">For demonstrasjonen skriver du inn BOM_1.</span><span class="sxs-lookup"><span data-stu-id="4abbc-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="4abbc-111">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="4abbc-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="4abbc-112">Velg STD.</span><span class="sxs-lookup"><span data-stu-id="4abbc-112">Select STD.</span></span> <span data-ttu-id="4abbc-113">STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="4abbc-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="4abbc-114">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="4abbc-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="4abbc-115">Velg for eksempel Lyd.</span><span class="sxs-lookup"><span data-stu-id="4abbc-115">For example, select Audio.</span></span> <span data-ttu-id="4abbc-116">Dette har ingen innvirkning på kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="4abbc-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="4abbc-117">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="4abbc-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4abbc-118">Velg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="4abbc-118">Select SiteWH.</span></span> <span data-ttu-id="4abbc-119">Bare Område og Lager blir brukt for demonstrasjon.</span><span class="sxs-lookup"><span data-stu-id="4abbc-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="4abbc-120">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="4abbc-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="4abbc-121">Sporingsdimensjoner vil ikke bli brukt i dette eksemplet, så velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="4abbc-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="4abbc-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4abbc-122">Click OK.</span></span>
9. <span data-ttu-id="4abbc-123">Klikk Administrer lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4abbc-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="4abbc-124">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="4abbc-124">Click Default order settings.</span></span>
11. <span data-ttu-id="4abbc-125">Velg Produksjon i feltet Standard ordretype.</span><span class="sxs-lookup"><span data-stu-id="4abbc-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="4abbc-126">Siden dette er et ferdig produkt som skal produseres, velger du Produksjon.</span><span class="sxs-lookup"><span data-stu-id="4abbc-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="4abbc-127">Angi eller velg en verdi i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="4abbc-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="4abbc-128">Til bruk i demonstrasjonen velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="4abbc-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="4abbc-129">Angi eller velg en verdi i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="4abbc-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="4abbc-130">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="4abbc-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="4abbc-131">Angi eller velg en verdi i feltet Salgssite.</span><span class="sxs-lookup"><span data-stu-id="4abbc-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="4abbc-132">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="4abbc-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="4abbc-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4abbc-133">Close the page.</span></span>



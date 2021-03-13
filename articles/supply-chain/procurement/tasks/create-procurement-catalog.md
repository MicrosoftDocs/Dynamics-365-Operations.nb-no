---
title: Opprette en innkjøpskatalog
description: Dette emnet forklarer hvordan du oppretter en innkjøpskatalog.
author: RichardLuan
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eaf8b8d8b369aa704344d6984a0f111af6e4285b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016483"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="269c5-103">Opprette en innkjøpskatalog</span><span class="sxs-lookup"><span data-stu-id="269c5-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="269c5-104">Dette emnet forklarer hvordan du oppretter en innkjøpskatalog.</span><span class="sxs-lookup"><span data-stu-id="269c5-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="269c5-105">Denne oppgaven vil vanligvis utføres av en innkjøpsansvarlig.</span><span class="sxs-lookup"><span data-stu-id="269c5-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="269c5-106">Du lærer også hvordan ansatte kan bruke katalogen når de oppretter en rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="269c5-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="269c5-107">Før du kan opprette en katalog, må det være et innkjøpskategorihierarki i systemet.</span><span class="sxs-lookup"><span data-stu-id="269c5-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="269c5-108">Hierarkiet arves av den nye katalogen, sammen med alle produktene som er i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="269c5-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="269c5-109">Du kan bruke denne veiledningen i demonstrasjonsdatafirmaet USMF, der innkjøpskategorihierarkiet er tilgjengelig, i tillegg til eksemplene som brukes i fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="269c5-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="269c5-110">Kontrollere at det finnes et innkjøpskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="269c5-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="269c5-111">Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Innkjøpskategorier**.</span><span class="sxs-lookup"><span data-stu-id="269c5-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="269c5-112">Et innkjøpskategorihierarki er tilgjengelig i demonstrasjonsdatafirmaet USMF, og produktene er lagt til kategorien **Kontormaskiner/datamaskiner**.</span><span class="sxs-lookup"><span data-stu-id="269c5-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="269c5-113">Hvis du kjører denne prosedyren som en oppgaveveiledning, må du låse opp veiledningen hvis du vil bla gjennom kategorien.</span><span class="sxs-lookup"><span data-stu-id="269c5-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="269c5-114">Hvis et hierarki ikke er tilgjengelig, kan du opprette det ved å klikke **Ny**.</span><span class="sxs-lookup"><span data-stu-id="269c5-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="269c5-115">Dette kan bare gjøre én gang.</span><span class="sxs-lookup"><span data-stu-id="269c5-115">This can only be done once.</span></span>  
2. <span data-ttu-id="269c5-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="269c5-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="269c5-117">Opprette en katalog</span><span class="sxs-lookup"><span data-stu-id="269c5-117">Create a catalog</span></span>
1. <span data-ttu-id="269c5-118">Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Kataloger > Innkjøpskataloger**.</span><span class="sxs-lookup"><span data-stu-id="269c5-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="269c5-119">Velg **Ny innkjøpskatalog** for å åpne dialogboksen for rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="269c5-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="269c5-120">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="269c5-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="269c5-121">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="269c5-121">Select **OK**.</span></span>
5. <span data-ttu-id="269c5-122">Vis **FIRMAINNKJØPSKATEGORIER** i treet.</span><span class="sxs-lookup"><span data-stu-id="269c5-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="269c5-123">Vis **KONTORMASKINER** i treet.</span><span class="sxs-lookup"><span data-stu-id="269c5-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="269c5-124">Velg **Datamaskiner** i treet.</span><span class="sxs-lookup"><span data-stu-id="269c5-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="269c5-125">Produktene fra innkjøpskategorien vises i listen.</span><span class="sxs-lookup"><span data-stu-id="269c5-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="269c5-126">Hvis du vil legge til et produkt i kategorien, må du gjøre dette på siden **Innkjøpskategorihierarki** eller **Varedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="269c5-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="269c5-127">**Standard** oppdateringstype bestemmer om nye produkter som er lagt til innkjøpskategorihierarkiet, umiddelbart vises i katalogen.</span><span class="sxs-lookup"><span data-stu-id="269c5-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="269c5-128">Hvis oppdateringstypen er satt til **Dynamisk**, vises endringene umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="269c5-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="269c5-129">Hvis oppdateringstypen er **Statisk**, vises nye produkter bare for personer som bruker katalogen etter at den er publisert på nytt.</span><span class="sxs-lookup"><span data-stu-id="269c5-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="269c5-130">**Publiser**-handlingen er tilgjengelig i handlingsruten øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="269c5-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="269c5-131">Hvis produkter er fjernet fra innkjøpskategorihierarkiet, vises endringen umiddelbart, uavhengig av verdien i feltet **Standard oppdateringstype**.</span><span class="sxs-lookup"><span data-stu-id="269c5-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="269c5-132">Velg **Kategorinavigering** i handlingsruten, og kontroller at **Aktiver** er valgt.</span><span class="sxs-lookup"><span data-stu-id="269c5-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="269c5-133">Velg **Aktiver katalog**.</span><span class="sxs-lookup"><span data-stu-id="269c5-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="269c5-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="269c5-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="269c5-135">Gjøre katalogen synlig</span><span class="sxs-lookup"><span data-stu-id="269c5-135">Make the catalog visible</span></span>
1. <span data-ttu-id="269c5-136">Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Oppsett > Policyer > Innkjøpspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="269c5-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="269c5-137">Velg **Policy for innkjøpspolicy for USMF**.</span><span class="sxs-lookup"><span data-stu-id="269c5-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="269c5-138">Du må velge innkjøpspolicyen for den juridiske enheten som arbeideren koblet til, som brukerprofilen kan bestille produkter i.</span><span class="sxs-lookup"><span data-stu-id="269c5-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="269c5-139">I USMF-demonstrasjonsdataene er administrasjonsbrukeren knyttet til arbeideren kalt **Julia Funderburk**, og hun bestiller produkter i USMF som standard.</span><span class="sxs-lookup"><span data-stu-id="269c5-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="269c5-140">Velg katalogen du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="269c5-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="269c5-141">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="269c5-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="269c5-142">Bruke katalogen</span><span class="sxs-lookup"><span data-stu-id="269c5-142">Use the catalog</span></span>
1. <span data-ttu-id="269c5-143">Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Innkjøpsrekvisisjoner > Alle innkjøpsrekvisisjoner**.</span><span class="sxs-lookup"><span data-stu-id="269c5-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="269c5-144">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="269c5-144">Select **New**.</span></span>
3. <span data-ttu-id="269c5-145">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="269c5-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="269c5-146">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="269c5-146">Select **OK**.</span></span>
5. <span data-ttu-id="269c5-147">Velg **Legg til produkter**.</span><span class="sxs-lookup"><span data-stu-id="269c5-147">Select **Add products**.</span></span>
6. <span data-ttu-id="269c5-148">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="269c5-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="269c5-149">Du kan bruke kategorihierarkiet til venstre eller filter øverst i listen for å filtrere produktene.</span><span class="sxs-lookup"><span data-stu-id="269c5-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="269c5-150">Velg **Tilføy til linjer**.</span><span class="sxs-lookup"><span data-stu-id="269c5-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="269c5-151">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="269c5-151">Select **OK**.</span></span>


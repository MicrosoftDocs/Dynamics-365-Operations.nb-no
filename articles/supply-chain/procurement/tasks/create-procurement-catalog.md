--- 
title: "Opprette en innkjøpskatalog"
description: "Denne veiledningen viser hvordan du oppretter en innkjøpskatalog."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="9d99b-103">Opprette en innkjøpskatalog</span><span class="sxs-lookup"><span data-stu-id="9d99b-103">Create a procurement catalog</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d99b-104">Denne veiledningen viser hvordan du oppretter en innkjøpskatalog.</span><span class="sxs-lookup"><span data-stu-id="9d99b-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="9d99b-105">Denne oppgaven vil vanligvis utføres av en innkjøpsansvarlig.</span><span class="sxs-lookup"><span data-stu-id="9d99b-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="9d99b-106">Du lærer også hvordan ansatte kan bruke katalogen når de oppretter en rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="9d99b-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="9d99b-107">Før du kan opprette en katalog, må det være et innkjøpskategorihierarki i systemet.</span><span class="sxs-lookup"><span data-stu-id="9d99b-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="9d99b-108">Hierarkiet arves av den nye katalogen, sammen med alle produktene som er i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="9d99b-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="9d99b-109">Du kan bruke denne veiledningen i demonstrasjonsdatafirmaet USMF, der innkjøpskategorihierarkiet er tilgjengelig, i tillegg til eksemplene som brukes i fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="9d99b-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="9d99b-110">Kontrollere at det finnes et innkjøpskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="9d99b-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="9d99b-111">Gå til Innkjøp og leverandører > Innkjøpskategorier.</span><span class="sxs-lookup"><span data-stu-id="9d99b-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="9d99b-112">Et innkjøpskategorihierarki er tilgjengelig i demonstrasjonsdatafirmaet USMF, og produktene er lagt til kategorien Kontormaskiner/datamaskiner.</span><span class="sxs-lookup"><span data-stu-id="9d99b-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="9d99b-113">Hvis du kjører denne prosedyren som en oppgaveveiledning, må du låse opp i veiledningen hvis du vil bla gjennom kategorien.</span><span class="sxs-lookup"><span data-stu-id="9d99b-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="9d99b-114">Hvis et hierarki ikke er tilgjengelig, kan du opprette det ved å klikke Ny.</span><span class="sxs-lookup"><span data-stu-id="9d99b-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="9d99b-115">Dette kan bare gjøre én gang.</span><span class="sxs-lookup"><span data-stu-id="9d99b-115">This can only be done once.</span></span>  
2. <span data-ttu-id="9d99b-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9d99b-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="9d99b-117">Opprette en katalog</span><span class="sxs-lookup"><span data-stu-id="9d99b-117">Create a catalog</span></span>
1. <span data-ttu-id="9d99b-118">Gå til Innkjøp og leverandører > Kataloger > Innkjøpskataloger.</span><span class="sxs-lookup"><span data-stu-id="9d99b-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="9d99b-119">Klikk Ny innkjøpskatalog for å åpne dialogboksen for rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="9d99b-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="9d99b-120">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9d99b-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9d99b-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9d99b-121">Click OK.</span></span>
5. <span data-ttu-id="9d99b-122">Vis FIRMAINNKJØPSKATEGORIER i treet.</span><span class="sxs-lookup"><span data-stu-id="9d99b-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="9d99b-123">Vis KONTORMASKINER i treet.</span><span class="sxs-lookup"><span data-stu-id="9d99b-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="9d99b-124">Velg Datamaskiner i treet .</span><span class="sxs-lookup"><span data-stu-id="9d99b-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="9d99b-125">Produktene fra innkjøpskategorien vises i listen.</span><span class="sxs-lookup"><span data-stu-id="9d99b-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="9d99b-126">Hvis du vil legge til et produkt i kategorien, må du gjøre dette på siden Innkjøpskategorihierarki eller Varedetaljer.</span><span class="sxs-lookup"><span data-stu-id="9d99b-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="9d99b-127">Standard oppdateringstype bestemmer om nye produkter som er lagt til innkjøpskategorihierarkiet, umiddelbart vises i katalogen.</span><span class="sxs-lookup"><span data-stu-id="9d99b-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="9d99b-128">Hvis oppdateringstypen er satt til Dynamisk, vises endringene umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="9d99b-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="9d99b-129">Hvis oppdateringstypen er Statisk, vises nye produkter bare for personer som bruker katalogen etter at den er publisert på nytt.</span><span class="sxs-lookup"><span data-stu-id="9d99b-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="9d99b-130">Publiser-handlingen er tilgjengelig i handlingsruten øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="9d99b-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="9d99b-131">Hvis produkter er fjernet fra innkjøpskategorihierarkiet, vises endringen umiddelbart, uavhengig av verdien i feltet Standard oppdateringstype.</span><span class="sxs-lookup"><span data-stu-id="9d99b-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="9d99b-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9d99b-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="9d99b-133">Klikk Skjul.</span><span class="sxs-lookup"><span data-stu-id="9d99b-133">Click Hide.</span></span>
10. <span data-ttu-id="9d99b-134">Klikk Kategorinavigering i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9d99b-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="9d99b-135">Klikk Deaktiver.</span><span class="sxs-lookup"><span data-stu-id="9d99b-135">Click Disable.</span></span>
12. <span data-ttu-id="9d99b-136">Klikk Kategorinavigering i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9d99b-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="9d99b-137">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="9d99b-137">Click Enable.</span></span>
14. <span data-ttu-id="9d99b-138">Klikk Aktiver katalog.</span><span class="sxs-lookup"><span data-stu-id="9d99b-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="9d99b-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9d99b-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="9d99b-140">Gjøre katalogen synlig</span><span class="sxs-lookup"><span data-stu-id="9d99b-140">Make the catalog visible</span></span>
1. <span data-ttu-id="9d99b-141">Gå til Innkjøp og leverandører > Oppsett > Policyer > Innkjøpspolicyer.</span><span class="sxs-lookup"><span data-stu-id="9d99b-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="9d99b-142">Velg Policy for innkjøpspolicy for USMF.</span><span class="sxs-lookup"><span data-stu-id="9d99b-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="9d99b-143">Du må velge innkjøpspolicyen for den juridiske enheten som arbeideren koblet til, som brukerprofilen kan bestille produkter i.</span><span class="sxs-lookup"><span data-stu-id="9d99b-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="9d99b-144">I USMF-demonstrasjonsdataene er administrasjonsbrukeren knyttet til arbeideren kalt Julia Funderburk, og hun bestiller produkter i USMF som standard.</span><span class="sxs-lookup"><span data-stu-id="9d99b-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="9d99b-145">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9d99b-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9d99b-146">Velg katalogen du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="9d99b-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="9d99b-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9d99b-147">Click OK.</span></span>
6. <span data-ttu-id="9d99b-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9d99b-148">Close the page.</span></span>
7. <span data-ttu-id="9d99b-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9d99b-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="9d99b-150">Bruke katalogen</span><span class="sxs-lookup"><span data-stu-id="9d99b-150">Use the catalog</span></span>
1. <span data-ttu-id="9d99b-151">Gå til Innkjøp og leverandører > Innkjøpsrekvisisjoner > Alle innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="9d99b-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="9d99b-152">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9d99b-152">Click New.</span></span>
3. <span data-ttu-id="9d99b-153">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9d99b-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9d99b-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9d99b-154">Click OK.</span></span>
5. <span data-ttu-id="9d99b-155">Klikk Legg til produkter.</span><span class="sxs-lookup"><span data-stu-id="9d99b-155">Click Add products.</span></span>
6. <span data-ttu-id="9d99b-156">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9d99b-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9d99b-157">Du kan bruke kategorihierarkiet til venstre eller filter øverst i listen for å filtrere produktene.</span><span class="sxs-lookup"><span data-stu-id="9d99b-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="9d99b-158">Klikk Tilføy til linjer.</span><span class="sxs-lookup"><span data-stu-id="9d99b-158">Click Add to lines.</span></span>
8. <span data-ttu-id="9d99b-159">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9d99b-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="9d99b-160">Klikk Tilføy til linjer.</span><span class="sxs-lookup"><span data-stu-id="9d99b-160">Click Add to lines.</span></span>
10. <span data-ttu-id="9d99b-161">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9d99b-161">Click OK.</span></span>



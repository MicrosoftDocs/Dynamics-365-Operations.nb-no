--- 
title: "Definere et innkjøpskategorihierarki"
description: "Denne prosedyren viser deg hvordan du oppretter nye noder i et innkjøpskategorihierarki og hvordan du konfigurerer en innkjøpskategori som skal brukes i en innkjøpsprosess."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 767fbe69eb918b6e37842ad1c393d08d11346e71
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="4f5a6-103">Definere et innkjøpskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="4f5a6-103">Set up a procurement category hierarchy</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f5a6-104">Denne prosedyren viser deg hvordan du oppretter nye noder i et innkjøpskategorihierarki og hvordan du konfigurerer en innkjøpskategori som skal brukes i en innkjøpsprosess.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="4f5a6-105">Disse oppgavene vil vanligvis utføres av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="4f5a6-106">Før du starter denne fremgangsmåten, må det være et kategorihierarki av typen Innkjøp.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="4f5a6-107">Hvis du bruker en demonstrasjonsdataselskap, kan du kjøre denne prosedyren i firmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="4f5a6-108">Legge til en ny innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="4f5a6-108">Add a new procurement category</span></span>
1. <span data-ttu-id="4f5a6-109">Gå til Innkjøp og leverandører > Innkjøpskategorier.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="4f5a6-110">Klikk Rediger kategorihierarki.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="4f5a6-111">Gjeldende innkjøpskategorihierarki vises til venstre på siden.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="4f5a6-112">Du er i ferd med å endre hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="4f5a6-113">Klikk Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-113">Click New category node.</span></span>
    * <span data-ttu-id="4f5a6-114">Den øverste noden velges som standard.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-114">The system selects the top node by default.</span></span> <span data-ttu-id="4f5a6-115">Hvis du bruker denne fremgangsmåten som oppgaveveiledning, kan du klikke knappen Lås opp og velge en annen overordnet node som du vil sette inn den ny noden i.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="4f5a6-116">Når det er gjort, låser du oppgaveveiledningen på nytt, og klikker deretter Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="4f5a6-117">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4f5a6-118">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="4f5a6-119">Skriv inn en verdi i feltet Egendefinert navn.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="4f5a6-120">Det egendefinerte navnet er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-120">The friendly name is optional.</span></span> <span data-ttu-id="4f5a6-121">Det vises i kategorioppslag sammen med navnet på kategorien.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="4f5a6-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="4f5a6-123">Legge til produkter i den nye innkjøpskategorien</span><span class="sxs-lookup"><span data-stu-id="4f5a6-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="4f5a6-124">Gå til Innkjøp og leverandører > Innkjøpskategorier.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="4f5a6-125">Merk noden du nettopp la til.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-125">Select the node you just added.</span></span> <span data-ttu-id="4f5a6-126">Hvis du kjører denne prosedyren som en oppgaveveiledning, må du kanskje låse opp i oppgaveveiledningen for å velge noden.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="4f5a6-127">Aktiver/deaktiver utvidelsen av delen Produkter.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="4f5a6-128">Klikk Legg til for å knytte produkter til innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="4f5a6-129">Velg produktet du vil legge til i innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="4f5a6-130">Klikk pilen for å velge produktet.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="4f5a6-131">Velg et annet produkt du vil legge til i innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="4f5a6-132">Klikk pilen for å velge produktet.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="4f5a6-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="4f5a6-134">Legge til godkjente og foretrukne leverandører</span><span class="sxs-lookup"><span data-stu-id="4f5a6-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="4f5a6-135">Aktiver/deaktiver utvidelsen av delen Leverandører.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="4f5a6-136">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-136">Click Add.</span></span>
    * <span data-ttu-id="4f5a6-137">Du kan legge til en leverandør i en innkjøpskategori og angi om en leverandør er foretrukket eller bare godkjent for kategorien.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="4f5a6-138">Når du sletter en leverandør fra en kategori, slettes ikke de historiske transaksjonene med leverandøren i kategorien.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="4f5a6-139">Søk etter leverandøren du vil legge til i kategorien.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="4f5a6-140">Klikk pilen for å velge leverandøren.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="4f5a6-141">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-141">Click OK.</span></span>
6. <span data-ttu-id="4f5a6-142">Velg leverandørraden som du vil endre.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="4f5a6-143">Velg et alternativ i Leverandørstatus-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="4f5a6-144">Innstillingen for leverandørvalg i kategoripolicyregelen styrer om foretrukne, godkjente, eller alle leverandører er tilgjengelige for innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="4f5a6-145">Legge til ytterligere informasjon i kategorien</span><span class="sxs-lookup"><span data-stu-id="4f5a6-145">Add additional information to the category</span></span>
1. <span data-ttu-id="4f5a6-146">Aktiver/deaktiver utvidelsen av delen Kriteriegrupper for leverandørevaluering.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="4f5a6-147">Med denne kategorien kan du definere hvilke kriterier leverandørene i innkjøpskategorien skal vurderes mot.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="4f5a6-148">Dette gjør du klikke Legg til og deretter velge en leverandørevalueringsgruppe som inneholder vilkårene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="4f5a6-149">Aktiver/deaktiver utvidelsen av delen Spørreskjemaer.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="4f5a6-150">Med denne kategorien kan du legge til spørreskjemaer som skal vises på rekvisisjonen, så lenge du angir aktivitetstypen som Rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="4f5a6-151">Bestilleren må deretter fylle ut et spørreskjema, før de sender en rekvisisjon for ett eller flere bestemte produkter i innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="4f5a6-152">Aktiver/deaktiver utvidelsen av delen Vare, mva-grupper.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="4f5a6-153">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4f5a6-154">Velg en mva-gruppe.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="4f5a6-155">Aktiver/deaktiver utvidelsen av delen Kategoriside.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="4f5a6-156">Kategorisider opprettes på siden Kategorihierarki.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="4f5a6-157">De inneholder informasjon om innkjøpskategorien, for eksempel informasjon om typen produkter i en kategori, bilder av produkter i en kategori, eller kunngjøringer, for eksempel om rabattene som finnes i en kategori.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="4f5a6-158">Informasjonen i en kategoriside vises på innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="4f5a6-159">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4f5a6-159">Close the page.</span></span>



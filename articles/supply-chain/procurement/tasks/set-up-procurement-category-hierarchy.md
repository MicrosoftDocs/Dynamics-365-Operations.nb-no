--- 
title: "Definere et innkjøpskategorihierarki"
description: "Denne prosedyren viser deg hvordan du oppretter nye noder i et innkjøpskategorihierarki og hvordan du konfigurerer en innkjøpskategori som skal brukes i en innkjøpsprosess."
author: mkirknel
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="6476e-103">Definere et innkjøpskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="6476e-103">Set up a procurement category hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6476e-104">Denne prosedyren viser deg hvordan du oppretter nye noder i et innkjøpskategorihierarki og hvordan du konfigurerer en innkjøpskategori som skal brukes i en innkjøpsprosess.</span><span class="sxs-lookup"><span data-stu-id="6476e-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="6476e-105">Disse oppgavene vil vanligvis utføres av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="6476e-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="6476e-106">Før du starter denne fremgangsmåten, må det være et kategorihierarki av typen Innkjøp.</span><span class="sxs-lookup"><span data-stu-id="6476e-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="6476e-107">Hvis du bruker en demonstrasjonsdataselskap, kan du kjøre denne prosedyren i firmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="6476e-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="6476e-108">Legge til en ny innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="6476e-108">Add a new procurement category</span></span>
1. <span data-ttu-id="6476e-109">Gå til Innkjøp og leverandører > </span><span class="sxs-lookup"><span data-stu-id="6476e-109">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="6476e-110">> Innkjøpskategorier.</span><span class="sxs-lookup"><span data-stu-id="6476e-110">> Procurement categories.</span></span>
2. <span data-ttu-id="6476e-111">Klikk Rediger kategorihierarki.</span><span class="sxs-lookup"><span data-stu-id="6476e-111">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="6476e-112">Gjeldende innkjøpskategorihierarki vises til venstre på siden.</span><span class="sxs-lookup"><span data-stu-id="6476e-112">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="6476e-113">Du er i ferd med å endre hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="6476e-113">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="6476e-114">Klikk Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="6476e-114">Click New category node.</span></span>
    * <span data-ttu-id="6476e-115">Den øverste noden velges som standard.</span><span class="sxs-lookup"><span data-stu-id="6476e-115">The system selects the top node by default.</span></span> <span data-ttu-id="6476e-116">Hvis du bruker denne fremgangsmåten som oppgaveveiledning, kan du klikke knappen Lås opp og velge en annen overordnet node som du vil sette inn den ny noden i.</span><span class="sxs-lookup"><span data-stu-id="6476e-116">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="6476e-117">Når det er gjort, låser du oppgaveveiledningen på nytt, og klikker deretter Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="6476e-117">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="6476e-118">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6476e-118">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6476e-119">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6476e-119">In the Description field, type a value.</span></span>
6. <span data-ttu-id="6476e-120">Skriv inn en verdi i feltet Egendefinert navn.</span><span class="sxs-lookup"><span data-stu-id="6476e-120">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="6476e-121">Det egendefinerte navnet er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="6476e-121">The friendly name is optional.</span></span> <span data-ttu-id="6476e-122">Det vises i kategorioppslag sammen med navnet på kategorien.</span><span class="sxs-lookup"><span data-stu-id="6476e-122">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="6476e-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6476e-123">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="6476e-124">Legge til produkter i den nye innkjøpskategorien</span><span class="sxs-lookup"><span data-stu-id="6476e-124">Add products to your new procurement category</span></span>
1. <span data-ttu-id="6476e-125">Gå til Innkjøp og leverandører > </span><span class="sxs-lookup"><span data-stu-id="6476e-125">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="6476e-126">> Innkjøpskategorier.</span><span class="sxs-lookup"><span data-stu-id="6476e-126">> Procurement categories.</span></span>
    * <span data-ttu-id="6476e-127">Merk noden du nettopp la til.</span><span class="sxs-lookup"><span data-stu-id="6476e-127">Select the node you just added.</span></span> <span data-ttu-id="6476e-128">Hvis du kjører denne prosedyren som en oppgaveveiledning, må du kanskje låse opp i oppgaveveiledningen for å velge noden.</span><span class="sxs-lookup"><span data-stu-id="6476e-128">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="6476e-129">Aktiver/deaktiver utvidelsen av delen Produkter.</span><span class="sxs-lookup"><span data-stu-id="6476e-129">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="6476e-130">Klikk Legg til for å knytte produkter til innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="6476e-130">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="6476e-131">Velg produktet du vil legge til i innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="6476e-131">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="6476e-132">Klikk pilen for å velge produktet.</span><span class="sxs-lookup"><span data-stu-id="6476e-132">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="6476e-133">Velg et annet produkt du vil legge til i innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="6476e-133">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="6476e-134">Klikk pilen for å velge produktet.</span><span class="sxs-lookup"><span data-stu-id="6476e-134">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="6476e-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6476e-135">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="6476e-136">Legge til godkjente og foretrukne leverandører</span><span class="sxs-lookup"><span data-stu-id="6476e-136">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="6476e-137">Aktiver/deaktiver utvidelsen av delen Leverandører.</span><span class="sxs-lookup"><span data-stu-id="6476e-137">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="6476e-138">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="6476e-138">Click Add.</span></span>
    * <span data-ttu-id="6476e-139">Du kan legge til en leverandør i en innkjøpskategori og angi om en leverandør er foretrukket eller bare godkjent for kategorien.</span><span class="sxs-lookup"><span data-stu-id="6476e-139">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="6476e-140">Når du sletter en leverandør fra en kategori, slettes ikke de historiske transaksjonene med leverandøren i kategorien.</span><span class="sxs-lookup"><span data-stu-id="6476e-140">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="6476e-141">Søk etter leverandøren du vil legge til i kategorien.</span><span class="sxs-lookup"><span data-stu-id="6476e-141">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="6476e-142">Klikk pilen for å velge leverandøren.</span><span class="sxs-lookup"><span data-stu-id="6476e-142">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="6476e-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="6476e-143">Click OK.</span></span>
6. <span data-ttu-id="6476e-144">Velg leverandørraden som du vil endre.</span><span class="sxs-lookup"><span data-stu-id="6476e-144">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="6476e-145">Velg et alternativ i Leverandørstatus-feltet.</span><span class="sxs-lookup"><span data-stu-id="6476e-145">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="6476e-146">Innstillingen for leverandørvalg i kategoripolicyregelen styrer om foretrukne, godkjente, eller alle leverandører er tilgjengelige for innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="6476e-146">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="6476e-147">Legge til ytterligere informasjon i kategorien</span><span class="sxs-lookup"><span data-stu-id="6476e-147">Add additional information to the category</span></span>
1. <span data-ttu-id="6476e-148">Aktiver/deaktiver utvidelsen av delen Kriteriegrupper for leverandørevaluering.</span><span class="sxs-lookup"><span data-stu-id="6476e-148">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="6476e-149">Med denne kategorien kan du definere hvilke kriterier leverandørene i innkjøpskategorien skal vurderes mot.</span><span class="sxs-lookup"><span data-stu-id="6476e-149">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="6476e-150">Dette gjør du klikke Legg til og deretter velge en leverandørevalueringsgruppe som inneholder vilkårene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="6476e-150">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="6476e-151">Aktiver/deaktiver utvidelsen av delen Spørreskjemaer.</span><span class="sxs-lookup"><span data-stu-id="6476e-151">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="6476e-152">Med denne kategorien kan du legge til spørreskjemaer som skal vises på rekvisisjonen, så lenge du angir aktivitetstypen som Rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="6476e-152">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="6476e-153">Bestilleren må deretter fylle ut et spørreskjema, før de sender en rekvisisjon for ett eller flere bestemte produkter i innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="6476e-153">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="6476e-154">Aktiver/deaktiver utvidelsen av delen Vare, mva-grupper.</span><span class="sxs-lookup"><span data-stu-id="6476e-154">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="6476e-155">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6476e-155">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6476e-156">Velg en mva-gruppe.</span><span class="sxs-lookup"><span data-stu-id="6476e-156">Select a sales tax group.</span></span>
6. <span data-ttu-id="6476e-157">Aktiver/deaktiver utvidelsen av delen Kategoriside.</span><span class="sxs-lookup"><span data-stu-id="6476e-157">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="6476e-158">Kategorisider opprettes på siden Kategorihierarki.</span><span class="sxs-lookup"><span data-stu-id="6476e-158">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="6476e-159">De inneholder informasjon om innkjøpskategorien, for eksempel informasjon om typen produkter i en kategori, bilder av produkter i en kategori, eller kunngjøringer, for eksempel om rabattene som finnes i en kategori.</span><span class="sxs-lookup"><span data-stu-id="6476e-159">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="6476e-160">Informasjonen i en kategoriside vises på innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="6476e-160">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="6476e-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6476e-161">Close the page.</span></span>



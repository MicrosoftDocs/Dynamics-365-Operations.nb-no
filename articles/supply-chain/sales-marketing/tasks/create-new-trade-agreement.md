--- 
title: Opprette en ny forretningsavtale
description: "Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0d0e5c5d680fcbac5407883a1d6365a4f312dda9
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="65f60-103">Opprette en ny forretningsavtale</span><span class="sxs-lookup"><span data-stu-id="65f60-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65f60-104">Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde.</span><span class="sxs-lookup"><span data-stu-id="65f60-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="65f60-105">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="65f60-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="65f60-106">Hvis du vil bruke dine egne data, må du før du starter denne veiledningen passe på at et navn på journal for forretningsavtale finnes der standardrelasjonen er satt til Pris (salg).</span><span class="sxs-lookup"><span data-stu-id="65f60-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="65f60-107">Opprette og postere en ny forretningsavtalejournal</span><span class="sxs-lookup"><span data-stu-id="65f60-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="65f60-108">Gå til Salg og markedsføring > Priser og rabatter > Forretningsavtalejournaler.</span><span class="sxs-lookup"><span data-stu-id="65f60-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="65f60-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="65f60-109">Click New.</span></span>
3. <span data-ttu-id="65f60-110">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="65f60-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="65f60-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="65f60-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="65f60-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="65f60-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="65f60-113">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="65f60-113">Click Lines.</span></span>
7. <span data-ttu-id="65f60-114">Velg Tabell i feltet Kontokode.</span><span class="sxs-lookup"><span data-stu-id="65f60-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="65f60-115">I dette eksemplet oppdaterer du prisen for en bestemt kunde, som betyr at du må velge Tabell.</span><span class="sxs-lookup"><span data-stu-id="65f60-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="65f60-116">Hvis du oppdaterer produktets listepris, velger du Alle, slik at den nye prisen gjelder for alle kunder.</span><span class="sxs-lookup"><span data-stu-id="65f60-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="65f60-117">Hvis du skal skille priser mellom ulike kundesegmenter, velger du deretter Gruppe.</span><span class="sxs-lookup"><span data-stu-id="65f60-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="65f60-118">For å merke Gruppe må du ha definert kundeprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="65f60-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="65f60-119">Klikk rullegardinknappen i feltet Kontovalg for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="65f60-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="65f60-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="65f60-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="65f60-121">Velg Tabell i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="65f60-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="65f60-122">Når du registrerer en forretningsavtale av typen Pris (salg), må du bare velge Tabell i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="65f60-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="65f60-123">Dette skyldes at en pris er en absolutt verdi og kan ikke være lik for alle produkter eller en gruppe produkter.</span><span class="sxs-lookup"><span data-stu-id="65f60-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="65f60-124">Klikk rullegardinknappen i feltet Varerelasjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="65f60-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="65f60-125">I listen velger du produktet du vil ha med i avtalen.</span><span class="sxs-lookup"><span data-stu-id="65f60-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="65f60-126">Noter hvilket produkt du har valgt.</span><span class="sxs-lookup"><span data-stu-id="65f60-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="65f60-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="65f60-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="65f60-128">Velg et minimumsantall i Fra-feltet.</span><span class="sxs-lookup"><span data-stu-id="65f60-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="65f60-129">Hvis kunden må bestille et minimumsantall av varen før de kan få tilgang til den nye prisen, må du angi antallet her.</span><span class="sxs-lookup"><span data-stu-id="65f60-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="65f60-130">Angi en verdi i feltet Til for å angi maksimalt antall som prisen for den avtalen ikke vil være gyldig over.</span><span class="sxs-lookup"><span data-stu-id="65f60-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="65f60-131">Hvis du tilbyr priser og rabatter som er basert på flere avbruddspunkt for antall, angir du hver antallsintervall som et par av minste og største antall i henholdsvis Fra- og Til-feltene.</span><span class="sxs-lookup"><span data-stu-id="65f60-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="65f60-132">Angi en pris i feltet Beløp i valuta.</span><span class="sxs-lookup"><span data-stu-id="65f60-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="65f60-133">I Fra dato-feltet angir du en dato som denne avtalen skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="65f60-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="65f60-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="65f60-134">Click Save.</span></span>
18. <span data-ttu-id="65f60-135">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="65f60-135">Click Validate.</span></span>
19. <span data-ttu-id="65f60-136">Klikk Valider valgte linjer.</span><span class="sxs-lookup"><span data-stu-id="65f60-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="65f60-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="65f60-137">Click OK.</span></span>
21. <span data-ttu-id="65f60-138">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="65f60-138">Click Post.</span></span>
22. <span data-ttu-id="65f60-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="65f60-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="65f60-140">Vise forretningsavtaler for et produkt</span><span class="sxs-lookup"><span data-stu-id="65f60-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="65f60-141">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="65f60-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="65f60-142">I listen finner og velger du produktet som du akkurat har oppdatert prisen for.</span><span class="sxs-lookup"><span data-stu-id="65f60-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="65f60-143">Klikk Selg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="65f60-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="65f60-144">Klikk Vis forretningsavtaler.</span><span class="sxs-lookup"><span data-stu-id="65f60-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="65f60-145">Se gjennom detaljene i forretningsavtalen for priser som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="65f60-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="65f60-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65f60-146">Close the page.</span></span>



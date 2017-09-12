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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="61765-103">Opprette en ny forretningsavtale</span><span class="sxs-lookup"><span data-stu-id="61765-103">Create a new trade agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61765-104">Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde.</span><span class="sxs-lookup"><span data-stu-id="61765-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="61765-105">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="61765-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="61765-106">Hvis du vil bruke dine egne data, må du før du starter denne veiledningen passe på at et navn på journal for forretningsavtale finnes der standardrelasjonen er satt til Pris (salg).</span><span class="sxs-lookup"><span data-stu-id="61765-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="61765-107">Opprette og postere en ny forretningsavtalejournal</span><span class="sxs-lookup"><span data-stu-id="61765-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="61765-108">Gå til Salg og markedsføring > Priser og rabatter > Forretningsavtalejournaler.</span><span class="sxs-lookup"><span data-stu-id="61765-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="61765-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="61765-109">Click New.</span></span>
3. <span data-ttu-id="61765-110">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="61765-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="61765-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="61765-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="61765-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="61765-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="61765-113">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="61765-113">Click Lines.</span></span>
7. <span data-ttu-id="61765-114">Velg Tabell i feltet Kontokode.</span><span class="sxs-lookup"><span data-stu-id="61765-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="61765-115">I dette eksemplet oppdaterer du prisen for en bestemt kunde, som betyr at du må velge Tabell.</span><span class="sxs-lookup"><span data-stu-id="61765-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="61765-116">Hvis du oppdaterer produktets listepris, velger du Alle, slik at den nye prisen gjelder for alle kunder.</span><span class="sxs-lookup"><span data-stu-id="61765-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="61765-117">Hvis du skal skille priser mellom ulike kundesegmenter, velger du deretter Gruppe.</span><span class="sxs-lookup"><span data-stu-id="61765-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="61765-118">For å merke Gruppe må du ha definert kundeprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="61765-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="61765-119">Klikk rullegardinknappen i feltet Kontovalg for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="61765-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="61765-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="61765-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="61765-121">Velg Tabell i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="61765-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="61765-122">Når du registrerer en forretningsavtale av typen Pris (salg), må du bare velge Tabell i Varekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="61765-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="61765-123">Dette skyldes at en pris er en absolutt verdi og kan ikke være lik for alle produkter eller en gruppe produkter.</span><span class="sxs-lookup"><span data-stu-id="61765-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="61765-124">Klikk rullegardinknappen i feltet Varerelasjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="61765-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="61765-125">I listen velger du produktet du vil ha med i avtalen.</span><span class="sxs-lookup"><span data-stu-id="61765-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="61765-126">Noter hvilket produkt du har valgt.</span><span class="sxs-lookup"><span data-stu-id="61765-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="61765-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="61765-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="61765-128">Velg et minimumsantall i Fra-feltet.</span><span class="sxs-lookup"><span data-stu-id="61765-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="61765-129">Hvis kunden må bestille et minimumsantall av varen før de kan få tilgang til den nye prisen, må du angi antallet her.</span><span class="sxs-lookup"><span data-stu-id="61765-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="61765-130">Angi en verdi i feltet Til for å angi maksimalt antall som prisen for den avtalen ikke vil være gyldig over.</span><span class="sxs-lookup"><span data-stu-id="61765-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="61765-131">Hvis du tilbyr priser og rabatter som er basert på flere avbruddspunkt for antall, angir du hver antallsintervall som et par av minste og største antall i henholdsvis Fra- og Til-feltene.</span><span class="sxs-lookup"><span data-stu-id="61765-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="61765-132">Angi en pris i feltet Beløp i valuta.</span><span class="sxs-lookup"><span data-stu-id="61765-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="61765-133">I Fra dato-feltet angir du en dato som denne avtalen skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="61765-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="61765-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="61765-134">Click Save.</span></span>
18. <span data-ttu-id="61765-135">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="61765-135">Click Validate.</span></span>
19. <span data-ttu-id="61765-136">Klikk Valider valgte linjer.</span><span class="sxs-lookup"><span data-stu-id="61765-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="61765-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="61765-137">Click OK.</span></span>
21. <span data-ttu-id="61765-138">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="61765-138">Click Post.</span></span>
22. <span data-ttu-id="61765-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="61765-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="61765-140">Vise forretningsavtaler for et produkt</span><span class="sxs-lookup"><span data-stu-id="61765-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="61765-141">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="61765-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="61765-142">I listen finner og velger du produktet som du akkurat har oppdatert prisen for.</span><span class="sxs-lookup"><span data-stu-id="61765-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="61765-143">Klikk Selg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="61765-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="61765-144">Klikk Vis forretningsavtaler.</span><span class="sxs-lookup"><span data-stu-id="61765-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="61765-145">Se gjennom detaljene i forretningsavtalen for priser som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="61765-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="61765-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="61765-146">Close the page.</span></span>



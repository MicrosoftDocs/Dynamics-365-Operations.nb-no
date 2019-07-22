---
title: Opprette en ny forretningsavtale
description: Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde.
author: omulvad
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42383b237a60d41d3b4e09ffbbe1c1bb5ebbfd7
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711207"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="89eaa-103">Opprette en ny forretningsavtale</span><span class="sxs-lookup"><span data-stu-id="89eaa-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89eaa-104">Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde.</span><span class="sxs-lookup"><span data-stu-id="89eaa-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="89eaa-105">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="89eaa-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="89eaa-106">Hvis du vil bruke dine egne data, må du før du starter denne veiledningen passe på at et navn på journal for forretningsavtale finnes der standardrelasjonen er satt til Pris (salg).</span><span class="sxs-lookup"><span data-stu-id="89eaa-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="89eaa-107">Opprette og postere en ny forretningsavtalejournal</span><span class="sxs-lookup"><span data-stu-id="89eaa-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="89eaa-108">Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Salg og markedsføring > Forretningsavtalejournaler**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="89eaa-109">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-109">Click **New**.</span></span>
3. <span data-ttu-id="89eaa-110">Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="89eaa-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="89eaa-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="89eaa-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="89eaa-112">I **Handlingsrute** klikker du på **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-112">On **Action pane**, click **Lines**.</span></span>
6. <span data-ttu-id="89eaa-113">Velg Tabell i **Kontokode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="89eaa-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="89eaa-114">I dette eksemplet oppdaterer du prisen for en bestemt kunde, som betyr at du må velge Tabell.</span><span class="sxs-lookup"><span data-stu-id="89eaa-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="89eaa-115">Hvis du oppdaterer produktets listepris, velger du Alle, slik at den nye prisen gjelder for alle kunder.</span><span class="sxs-lookup"><span data-stu-id="89eaa-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="89eaa-116">Hvis du skal skille priser mellom ulike kundesegmenter, velger du deretter Gruppe.</span><span class="sxs-lookup"><span data-stu-id="89eaa-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="89eaa-117">For å merke Gruppe må du ha definert kundeprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="89eaa-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="89eaa-118">Klikk på rullegardinknappen i **Kontovalg**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="89eaa-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="89eaa-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="89eaa-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="89eaa-120">Velg Tabell i **Varekode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="89eaa-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="89eaa-121">Når du registrerer en forretningsavtale av typen Pris (salg), må du bare velge Tabell i **Varekode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="89eaa-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="89eaa-122">Dette skyldes at en pris er en absolutt verdi og kan ikke være lik for alle produkter eller en gruppe produkter.</span><span class="sxs-lookup"><span data-stu-id="89eaa-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="89eaa-123">Klikk på rullegardinknappen i **Varerelasjon**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="89eaa-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="89eaa-124">I listen velger du produktet du vil ha med i avtalen.</span><span class="sxs-lookup"><span data-stu-id="89eaa-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="89eaa-125">Noter hvilket produkt du har valgt.</span><span class="sxs-lookup"><span data-stu-id="89eaa-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="89eaa-126">Velg et minimumsantall i **Fra**-feltet.</span><span class="sxs-lookup"><span data-stu-id="89eaa-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="89eaa-127">Hvis kunden må bestille et minimumsantall av varen før de kan få tilgang til den nye prisen, må du angi antallet her.</span><span class="sxs-lookup"><span data-stu-id="89eaa-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="89eaa-128">Angi en verdi i feltet **Til** for å angi maksimalt antall som prisen for den avtalen ikke vil være gyldig over.</span><span class="sxs-lookup"><span data-stu-id="89eaa-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="89eaa-129">Hvis du tilbyr priser og rabatter som er basert på flere avbruddspunkt for antall, angir du hver antallsintervall som et par av minste og største antall i henholdsvis **Fra**- og **Til**-feltene.</span><span class="sxs-lookup"><span data-stu-id="89eaa-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="89eaa-130">Angi en pris i feltet **Beløp i valuta**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="89eaa-131">Angi en dato som denne avtalen er gyldig fra, i **Fra dato**-feltet i **Detaljer**-delen.</span><span class="sxs-lookup"><span data-stu-id="89eaa-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="89eaa-132">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-132">Click **Save**.</span></span>
16. <span data-ttu-id="89eaa-133">Klikk på **Valider**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-133">Click **Validate**.</span></span>
17. <span data-ttu-id="89eaa-134">Klikk på **Valider valgte linjer**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="89eaa-135">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-135">Click **OK**.</span></span>
19. <span data-ttu-id="89eaa-136">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-136">Click **Post**.</span></span>
20. <span data-ttu-id="89eaa-137">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="89eaa-138">Vise forretningsavtaler for et produkt</span><span class="sxs-lookup"><span data-stu-id="89eaa-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="89eaa-139">Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="89eaa-140">I listen finner og velger du produktet som du akkurat har oppdatert prisen for.</span><span class="sxs-lookup"><span data-stu-id="89eaa-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="89eaa-141">I **Handlingsrute** klikker du på **Selg**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="89eaa-142">Klikk på **Vis forretningsavtaler**.</span><span class="sxs-lookup"><span data-stu-id="89eaa-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="89eaa-143">Se gjennom detaljene i forretningsavtalen for priser som du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="89eaa-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="89eaa-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89eaa-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89eaa-145">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="89eaa-145">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="89eaa-146">Fellesskapsblogger</span><span class="sxs-lookup"><span data-stu-id="89eaa-146">Community blogs</span></span>
- [<span data-ttu-id="89eaa-147">Salgspriser i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="89eaa-147">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)

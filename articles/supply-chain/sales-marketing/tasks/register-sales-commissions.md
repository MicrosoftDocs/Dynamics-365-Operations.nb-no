--- 
title: Registrere salgsprovisjoner
description: "Denne fremgangsmåten viser deg hvordan provisjoner beregnes og registreres."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="register-sales-commissions"></a><span data-ttu-id="06c29-103">Registrere salgsprovisjoner</span><span class="sxs-lookup"><span data-stu-id="06c29-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06c29-104">Denne fremgangsmåten viser deg hvordan provisjoner beregnes og registreres.</span><span class="sxs-lookup"><span data-stu-id="06c29-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="06c29-105">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="06c29-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="06c29-106">Før du starter denne veiledningen kjører du veiledningen kalt Definer regler for salgsprovisjon for å være sikker på at du har alt nødvendig provisjonsberegningsoppsett.</span><span class="sxs-lookup"><span data-stu-id="06c29-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="06c29-107">Noter kunde- og varenumrene du har valgt for provisjonsprosessen, og bruk dem når du blir spurt til å opprette en salgsordre i denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="06c29-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="06c29-108">Fakturere en salgsordre som kvalifiserer til en selger for en provisjon</span><span class="sxs-lookup"><span data-stu-id="06c29-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="06c29-109">Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="06c29-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="06c29-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="06c29-110">Click New.</span></span>
3. <span data-ttu-id="06c29-111">Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06c29-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="06c29-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="06c29-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="06c29-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="06c29-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="06c29-114">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="06c29-114">Click OK.</span></span>
7. <span data-ttu-id="06c29-115">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="06c29-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="06c29-116">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="06c29-116">Click Change view.</span></span>
9. <span data-ttu-id="06c29-117">Klikk Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="06c29-117">Click Header view.</span></span>
10. <span data-ttu-id="06c29-118">Utvid Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="06c29-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="06c29-119">Verdien i feltet Salgsgruppe representerer en gruppe med én eller flere selgere tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="06c29-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="06c29-120">Medlemmene av gruppen er de som skal motta provisjoner når ordren faktureres, i henhold til forhåndsdefinerte satser og distribusjon.</span><span class="sxs-lookup"><span data-stu-id="06c29-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="06c29-121">Verdien kopieres fra kundekortet, men du kan endre den hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="06c29-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="06c29-122">Salgsgruppen kopieres også til salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="06c29-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="06c29-123">Du kan endre den slik at den kan være forskjellig fra den i hodet og/eller mellom linjer.</span><span class="sxs-lookup"><span data-stu-id="06c29-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="06c29-124">Verdien i feltet Provisjonsgruppe representerer en gruppe som du har opprettet for én eller flere kunder med det formål å spore provisjoner.</span><span class="sxs-lookup"><span data-stu-id="06c29-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="06c29-125">Verdien kopieres fra kundekortet, men du kan endre den hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="06c29-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="06c29-126">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="06c29-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="06c29-127">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="06c29-127">Click Change view.</span></span>
13. <span data-ttu-id="06c29-128">Klikk Linjevisning.</span><span class="sxs-lookup"><span data-stu-id="06c29-128">Click Line view.</span></span>
14. <span data-ttu-id="06c29-129">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06c29-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="06c29-130">Velg varen du har definert for provisjon, i listen.</span><span class="sxs-lookup"><span data-stu-id="06c29-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="06c29-131">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="06c29-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="06c29-132">Noter linjens nettobeløp.</span><span class="sxs-lookup"><span data-stu-id="06c29-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="06c29-133">Det representerer salgsinntekter, som i dette eksemplet er grunnlaget for provisjonsberegningen.</span><span class="sxs-lookup"><span data-stu-id="06c29-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="06c29-134">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="06c29-134">Click Save.</span></span>
18. <span data-ttu-id="06c29-135">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="06c29-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="06c29-136">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="06c29-136">Click Invoice.</span></span>
20. <span data-ttu-id="06c29-137">Utvid seksjonen Parametere.</span><span class="sxs-lookup"><span data-stu-id="06c29-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="06c29-138">Velg Alle i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="06c29-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="06c29-139">Velg Ja i feltet Postering.</span><span class="sxs-lookup"><span data-stu-id="06c29-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="06c29-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="06c29-140">Click OK.</span></span>
24. <span data-ttu-id="06c29-141">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="06c29-141">Click OK.</span></span>
    * <span data-ttu-id="06c29-142">Det kan ta litt tid å postere transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="06c29-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="06c29-143">Tillat behandlingen å fullføre, og ikke lukk siden.</span><span class="sxs-lookup"><span data-stu-id="06c29-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="06c29-144">Gå gjennom de registrerte salgsprovisjonene</span><span class="sxs-lookup"><span data-stu-id="06c29-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="06c29-145">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="06c29-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="06c29-146">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="06c29-146">Click Invoice.</span></span>
3. <span data-ttu-id="06c29-147">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="06c29-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="06c29-148">Klikk Provisjonstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="06c29-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="06c29-149">Kategorien Oversikt viser linjer som viser provisjonsbeløpene som skal betales til selgere som er knyttet til den fakturerte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="06c29-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="06c29-150">La oss gå gjennom detaljene.</span><span class="sxs-lookup"><span data-stu-id="06c29-150">Let's review the details.</span></span>     
    * <span data-ttu-id="06c29-151">Hvis du brukte veiledningen Definer regler for salgsprovisjon til å definere provisjonssalgsgruppen, finnes det to selgere som skal motta en salgsprovisjon, og provisjonen deles likt mellom dem.</span><span class="sxs-lookup"><span data-stu-id="06c29-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="06c29-152">I dette eksemplet beregnes det totale provisjonsbeløpet som en prosent av salgsomsetning (nettobeløpet på ordrelinjen).</span><span class="sxs-lookup"><span data-stu-id="06c29-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="06c29-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="06c29-153">Close the page.</span></span>
6. <span data-ttu-id="06c29-154">Klikk Bilag.</span><span class="sxs-lookup"><span data-stu-id="06c29-154">Click Voucher.</span></span>
    * <span data-ttu-id="06c29-155">Du kan vise bilagstransaksjonene for provisjonsbeløpene som er postert til de forhåndsdefinerte provisjonsutgifts- og provisjonsbetalingskontoene.</span><span class="sxs-lookup"><span data-stu-id="06c29-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  



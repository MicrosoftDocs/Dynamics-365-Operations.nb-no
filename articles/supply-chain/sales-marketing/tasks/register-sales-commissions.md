---
title: Registrere salgsprovisjoner
description: Dette emnet forklarer hvordan salgsprovisjon beregnes og registreres.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c6dbccc3e2c33c8dfec2373bd21c7bd217a889b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203241"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="4f1c0-103">Registrere salgsprovisjoner</span><span class="sxs-lookup"><span data-stu-id="4f1c0-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f1c0-104">Dette emnet forklarer hvordan salgsprovisjon beregnes og registreres.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="4f1c0-105">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4f1c0-106">Før du starter denne veiledningen kjører du veiledningen kalt Definer regler for salgsprovisjon for å være sikker på at du har alt nødvendig provisjonsberegningsoppsett.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="4f1c0-107">Noter kunde- og varenumrene du har valgt for provisjonsprosessen, og bruk dem når du blir spurt til å opprette en salgsordre i denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="4f1c0-108">Fakturere en salgsordre som kvalifiserer til en selger for en provisjon</span><span class="sxs-lookup"><span data-stu-id="4f1c0-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="4f1c0-109">I navigasjonsruten går du til **Moduler > Salg og markedsføring > Salgsordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="4f1c0-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-110">Select **New**.</span></span>
3. <span data-ttu-id="4f1c0-111">Velg det ønskede oppslaget på rullegardinmenyen i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="4f1c0-112">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-112">Select **OK**.</span></span>
5. <span data-ttu-id="4f1c0-113">Velg **Alternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="4f1c0-114">Velg **Endre visning**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-114">Select **Change view**.</span></span>
7. <span data-ttu-id="4f1c0-115">Velg **Topptekstvisning**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-115">Select **Header view**.</span></span>
8. <span data-ttu-id="4f1c0-116">Utvid **Oppsett**-delen.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="4f1c0-117">Verdien i feltet **Salgsgruppe** representerer en gruppe med én eller flere selgere tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="4f1c0-118">Medlemmene av gruppen er de som skal motta provisjoner når ordren faktureres, i henhold til forhåndsdefinerte satser og distribusjon.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="4f1c0-119">Verdien kopieres fra kundekortet, men du kan endre den hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="4f1c0-120">Salgsgruppen kopieres også til salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="4f1c0-121">Du kan endre den slik at den kan være forskjellig fra den i hodet og/eller mellom linjer.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="4f1c0-122">Verdien i feltet **Provisjonsgruppe** representerer en gruppe som du har opprettet for én eller flere kunder med det formål å spore provisjoner.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="4f1c0-123">Verdien kopieres fra kundekortet, men du kan endre den hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="4f1c0-124">Velg **Alternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="4f1c0-125">Velg **Endre visning**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-125">Select **Change view**.</span></span>
11. <span data-ttu-id="4f1c0-126">Velg **Linjevisning**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-126">Select **Line view**.</span></span>
12. <span data-ttu-id="4f1c0-127">I rullegardinmenyen for **Varenummer**-feltet velger du varen du har definert for provisjoner.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="4f1c0-128">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="4f1c0-129">Noter linjens nettobeløp.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="4f1c0-130">Det representerer salgsinntekter, som i dette eksemplet er grunnlaget for provisjonsberegningen.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="4f1c0-131">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-131">Select **Save**.</span></span>
15. <span data-ttu-id="4f1c0-132">Velg **Faktura** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="4f1c0-133">Velg **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="4f1c0-134">Utvid seksjonen **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="4f1c0-135">Velg **Alle** i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="4f1c0-136">Velg **Ja** i feltet **Postering**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="4f1c0-137">Velg **OK**, og velg deretter **OK** i neste rute.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="4f1c0-138">Det kan ta litt tid å postere transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="4f1c0-139">Tillat behandlingen å fullføre, og ikke lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="4f1c0-140">Gå gjennom de registrerte salgsprovisjonene</span><span class="sxs-lookup"><span data-stu-id="4f1c0-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="4f1c0-141">I Handlingsvinduet, velg **Faktura**, og velg deretter **Faktura** igjen.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="4f1c0-142">I Handlingsvinduet, velg **Faktura**, og velg deretter **Provisjonstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="4f1c0-143">Kategorien **Oversikt** viser linjer som viser provisjonsbeløpene som skal betales til selgere som er knyttet til den fakturerte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="4f1c0-144">La oss gå gjennom detaljene.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-144">Let's review the details.</span></span>  
    - <span data-ttu-id="4f1c0-145">Hvis du brukte veiledningen Definer regler for salgsprovisjon til å definere gruppen **provisjonssalg**, finnes det to selgere som skal motta en salgsprovisjon, og provisjonen deles likt mellom dem.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="4f1c0-146">I dette eksemplet beregnes det totale provisjonsbeløpet som en prosent av salgsomsetning (nettobeløpet på ordrelinjen).</span><span class="sxs-lookup"><span data-stu-id="4f1c0-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="4f1c0-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-147">Close the page.</span></span>
4. <span data-ttu-id="4f1c0-148">Velg **Bilag**.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-148">Select **Voucher**.</span></span> <span data-ttu-id="4f1c0-149">Du kan vise bilagstransaksjonene for provisjonsbeløpene som er postert til de forhåndsdefinerte provisjonsutgifts- og provisjonsbetalingskontoene.</span><span class="sxs-lookup"><span data-stu-id="4f1c0-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


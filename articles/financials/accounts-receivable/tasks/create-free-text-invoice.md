--- 
title: Opprett en fritekstfaktura
description: Denne veiledningen beskriver hvordan du oppretter en fritekstfaktura.
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ca7c0f46f0cab298580e37c236bd10e4325e011b
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="1ea15-103">Opprett en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="1ea15-103">Create a free text invoice</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ea15-104">Denne veiledningen beskriver hvordan du oppretter en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="1ea15-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="1ea15-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="1ea15-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1ea15-106">Gå til Kunder > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="1ea15-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="1ea15-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="1ea15-107">Click New.</span></span>
3. <span data-ttu-id="1ea15-108">Velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ea15-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="1ea15-109">Fakturakontoen er som standard den samme kontoen som brukes for kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="1ea15-110">Regnskapsstatusen starter med Pågår hvis fakturaen ikke er postert.</span><span class="sxs-lookup"><span data-stu-id="1ea15-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="1ea15-111">Fakturanummeret tilordnes når fakturaen posteres.</span><span class="sxs-lookup"><span data-stu-id="1ea15-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="1ea15-112">Hvis du bruker SEPA-mandater, fylles avtalegiromandatet automatisk ut med et mandat når du velger kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="1ea15-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="1ea15-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1ea15-114">Angi et kontonummer uten dimensjoner i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ea15-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="1ea15-115">Du kan også angi ett eller flere tegn for hovedkontoen og bruke oppslaget til å finne kontoen din.</span><span class="sxs-lookup"><span data-stu-id="1ea15-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="1ea15-116">Du vil angi dimensjoner senere i denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="1ea15-117">Vis hurtigfanen Linjedetaljer slik at du kan legge til dimensjoner i hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="1ea15-118">Klikk kategorien Finansdimensjonslinje.</span><span class="sxs-lookup"><span data-stu-id="1ea15-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="1ea15-119">Dimensjonene gjelder bare for den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="1ea15-120">Mva-gruppen fylles ut fra kunden.</span><span class="sxs-lookup"><span data-stu-id="1ea15-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="1ea15-121">Hvis kunden ikke har en mva-gruppe, brukes mva-gruppen fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="1ea15-122">Mva-gruppen for varer fylles ut fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="1ea15-123">Hvis hovedkontoen ikke har en mva-gruppe for varer, brukes mva-gruppen for varer i mva-parameterne for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="1ea15-123">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="1ea15-124">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="1ea15-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1ea15-125">Antallet er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="1ea15-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="1ea15-126">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="1ea15-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="1ea15-127">Enhetsprisen er valgfri.</span><span class="sxs-lookup"><span data-stu-id="1ea15-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="1ea15-128">Beløpet beregnes som antallet ganger enhetsprisen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="1ea15-129">Du kan imidlertid overstyre dette, og angi et beløp.</span><span class="sxs-lookup"><span data-stu-id="1ea15-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="1ea15-130">Hvis du vil vise merverdiavgiften som er beregnet for fakturaen, klikker du Merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="1ea15-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="1ea15-131">Du kan vise mva-beløpene på denne siden, eller du kan overstyre beløpene i kategorien Justering.</span><span class="sxs-lookup"><span data-stu-id="1ea15-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="1ea15-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1ea15-132">Click OK.</span></span>
12. <span data-ttu-id="1ea15-133">Klikk Tillegg for å legge til et tillegg på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="1ea15-134">Skriv inn en verdi i Tilleggskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ea15-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="1ea15-135">Angi et tall i Gebyrverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ea15-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="1ea15-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1ea15-136">Close the page.</span></span>
16. <span data-ttu-id="1ea15-137">Klikk Totaler for å vise detaljer for sammendrag og totaler.</span><span class="sxs-lookup"><span data-stu-id="1ea15-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="1ea15-138">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="1ea15-138">Click Close.</span></span>
18. <span data-ttu-id="1ea15-139">Klikk Poster for å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-139">Click Post to post the invoice.</span></span> <span data-ttu-id="1ea15-140">Du kan avbryte før du posterer.</span><span class="sxs-lookup"><span data-stu-id="1ea15-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="1ea15-141">Slik endrer du når fakturaene skal skrives ut: Velg Gjeldende for å skrive ut hver faktura når den oppdateres, eller velg Etter for å skrive ut når alle fakturaene er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="1ea15-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="1ea15-142">Hvis du vil endre hvordan kundens kredittgrense kontrolleres før postering, kan du endre kredittgrensetypen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="1ea15-143">Velg Ja hvis du vil skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="1ea15-144">Velg Ja hvis du vil postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1ea15-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="1ea15-145">Du kan skrive ut fakturaen uten postering.</span><span class="sxs-lookup"><span data-stu-id="1ea15-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="1ea15-146">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1ea15-146">Click OK.</span></span>



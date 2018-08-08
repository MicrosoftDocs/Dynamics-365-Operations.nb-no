--- 
title: Opprett en fritekstfaktura
description: Denne artikkelen beskriver hvordan du oppretter en fritekstkundefaktura.
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="a017b-103">Opprett en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="a017b-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a017b-104">Denne artikkelen beskriver hvordan du oppretter en fritekstkundefaktura.</span><span class="sxs-lookup"><span data-stu-id="a017b-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="a017b-105">For denne fremgangsmåten må du bruke demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a017b-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="a017b-106">Opprett en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="a017b-106">Create a free text invoice</span></span>

1. <span data-ttu-id="a017b-107">Gå til Kunder > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="a017b-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="a017b-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a017b-108">Click New.</span></span>
3. <span data-ttu-id="a017b-109">Velg en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="a017b-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="a017b-110">Fakturakontoen er som standard den samme kontoen som brukes for kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="a017b-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="a017b-111">Regnskapsstatusen starter med Pågår hvis fakturaen ikke er postert.</span><span class="sxs-lookup"><span data-stu-id="a017b-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="a017b-112">Fakturanummeret tilordnes når fakturaen posteres.</span><span class="sxs-lookup"><span data-stu-id="a017b-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="a017b-113">Hvis du bruker SEPA-mandater, fylles avtalegiromandatet automatisk ut med et mandat når du velger kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="a017b-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="a017b-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a017b-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a017b-115">Angi et kontonummer uten dimensjoner i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="a017b-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="a017b-116">Du kan også angi ett eller flere tegn for hovedkontoen og bruke oppslaget til å finne kontoen din.</span><span class="sxs-lookup"><span data-stu-id="a017b-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="a017b-117">Du vil angi dimensjoner senere i denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="a017b-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="a017b-118">Vis hurtigfanen Linjedetaljer slik at du kan legge til dimensjoner i hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="a017b-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="a017b-119">Klikk kategorien Finansdimensjonslinje.</span><span class="sxs-lookup"><span data-stu-id="a017b-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="a017b-120">Dimensjonene gjelder bare for den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="a017b-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="a017b-121">Mva-gruppen fylles ut fra kunden.</span><span class="sxs-lookup"><span data-stu-id="a017b-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="a017b-122">Hvis kunden ikke har en mva-gruppe, brukes mva-gruppen fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="a017b-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="a017b-123">Mva-gruppen for varer fylles ut fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="a017b-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="a017b-124">Hvis hovedkontoen ikke har en mva-gruppe for varer, brukes mva-gruppen for varer i mva-parameterne for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="a017b-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="a017b-125">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="a017b-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a017b-126">Antallet er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="a017b-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="a017b-127">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="a017b-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="a017b-128">Enhetsprisen er valgfri.</span><span class="sxs-lookup"><span data-stu-id="a017b-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="a017b-129">Beløpet beregnes som antallet ganger enhetsprisen.</span><span class="sxs-lookup"><span data-stu-id="a017b-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="a017b-130">Du kan imidlertid overstyre dette, og angi et beløp.</span><span class="sxs-lookup"><span data-stu-id="a017b-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="a017b-131">Hvis du vil vise merverdiavgiften som er beregnet for fakturaen, klikker du Merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="a017b-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="a017b-132">Du kan vise mva-beløpene på denne siden, eller du kan overstyre beløpene i kategorien Justering.</span><span class="sxs-lookup"><span data-stu-id="a017b-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="a017b-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a017b-133">Click OK.</span></span>
12. <span data-ttu-id="a017b-134">Klikk Tillegg for å legge til et tillegg på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a017b-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="a017b-135">Skriv inn en verdi i Tilleggskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="a017b-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="a017b-136">Angi et tall i Gebyrverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="a017b-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="a017b-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a017b-137">Close the page.</span></span>
16. <span data-ttu-id="a017b-138">Klikk Totaler for å vise detaljer for sammendrag og totaler.</span><span class="sxs-lookup"><span data-stu-id="a017b-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="a017b-139">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="a017b-139">Click Close.</span></span>
18. <span data-ttu-id="a017b-140">Klikk Poster for å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a017b-140">Click Post to post the invoice.</span></span> <span data-ttu-id="a017b-141">Du kan avbryte før du posterer.</span><span class="sxs-lookup"><span data-stu-id="a017b-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="a017b-142">Slik endrer du når fakturaene skal skrives ut: Velg Gjeldende for å skrive ut hver faktura når den oppdateres, eller velg Etter for å skrive ut når alle fakturaene er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="a017b-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="a017b-143">Hvis du vil endre hvordan kundens kredittgrense kontrolleres før postering, kan du endre kredittgrensetypen.</span><span class="sxs-lookup"><span data-stu-id="a017b-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="a017b-144">Velg Ja hvis du vil skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a017b-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="a017b-145">Velg Ja hvis du vil postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a017b-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="a017b-146">Du kan skrive ut fakturaen uten postering.</span><span class="sxs-lookup"><span data-stu-id="a017b-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="a017b-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a017b-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="a017b-148">Kopier linjer</span><span class="sxs-lookup"><span data-stu-id="a017b-148">Copy lines</span></span>
<span data-ttu-id="a017b-149">Hvis du vil kopiere linjer på fritekstfakturaen, velger du én eller flere linjer og klikker deretter Kopier valgte linjer.</span><span class="sxs-lookup"><span data-stu-id="a017b-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="a017b-150">Du kan angi hvor mange kopier du vil lage, og du kan også kopiere notater og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a017b-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="a017b-151">Du kan kopiere distribusjonene eller la dem bli opprettet på nytt når du posterer.</span><span class="sxs-lookup"><span data-stu-id="a017b-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="a017b-152">Når du kopierer linjene, kan du redigere informasjonen etter behov.</span><span class="sxs-lookup"><span data-stu-id="a017b-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="a017b-153">Opprette en fritekstfaktura fra en mal</span><span class="sxs-lookup"><span data-stu-id="a017b-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="a017b-154">Du kan opprette en fritekstfaktura fra en mal.</span><span class="sxs-lookup"><span data-stu-id="a017b-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="a017b-155">Når du velger Ny fra mal i kategorien Faktura, kan du velge et malnavn og kundekontoen for den nye fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="a017b-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="a017b-156">Du kan også velge å standardverdier, for eksempel betalingsbetingelsene og betalingsmåten, fra kunden eller bruke verdier som ble lagret med malen.</span><span class="sxs-lookup"><span data-stu-id="a017b-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="a017b-157">Det opprettes en ny fritekstfaktura, og du kan redigere verdiene i denne fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a017b-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 



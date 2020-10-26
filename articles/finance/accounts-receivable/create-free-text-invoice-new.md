---
title: Opprett en fritekstfaktura
description: Dette emnet forklarer hvordan du oppretter fritekstfakturaer.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1ac06e7d702ffe3a8cdb6bd2823f2ffdc055c722
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976529"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="54bbb-103">Opprett en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="54bbb-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54bbb-104">Dette emnet forklarer hvordan du oppretter fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="54bbb-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="54bbb-105">For denne fremgangsmåten må du bruke demonstrasjonsfirmaet **USMF** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="54bbb-106">Opprett en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="54bbb-106">Create a free text invoice</span></span>

1. <span data-ttu-id="54bbb-107">Gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-107">Go to **Accounts receivable \> Invoices \> All free text invoices** .</span></span>
2. <span data-ttu-id="54bbb-108">Velg **Ny** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-108">Select **New** .</span></span>
3. <span data-ttu-id="54bbb-109">Velg en verdi i **Kundekonto** -feltet.</span><span class="sxs-lookup"><span data-stu-id="54bbb-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="54bbb-110">Kontoen som velges som kundekonto, brukes som standard som fakturakontoen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="54bbb-111">Regnskapsstatusen starter med **Pågår** hvis fakturaen ikke er postert.</span><span class="sxs-lookup"><span data-stu-id="54bbb-111">If the invoice isn't posted, the accounting status starts with **In process** .</span></span>
    * <span data-ttu-id="54bbb-112">Fakturanummeret tilordnes når fakturaen posteres.</span><span class="sxs-lookup"><span data-stu-id="54bbb-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="54bbb-113">Hvis du bruker mandater fra felles eurobetalingsområde (SEPA), fylles avtalegiromandatet automatisk ut når du velger kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="54bbb-114">Angi en verdi i feltet **Beskrivelse** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="54bbb-115">Angi et kontonummer uten dimensjoner i **Hovedkonto** -feltet.</span><span class="sxs-lookup"><span data-stu-id="54bbb-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="54bbb-116">Du setter inn dimensjoner senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="54bbb-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="54bbb-117">Du kan også angi ett eller flere tegn for hovedkontoen og bruke oppslaget til å finne kontoen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="54bbb-118">Velg hurtigfanen **Linjedetaljer** for å legge til dimensjoner i hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="54bbb-119">Velg kategorien **Finansdimensjonslinje** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="54bbb-120">Dimensjonene gjelder bare for den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="54bbb-121">Mva-gruppen fylles ut av kunden.</span><span class="sxs-lookup"><span data-stu-id="54bbb-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="54bbb-122">Hvis kunden ikke har en mva-gruppe, brukes mva-gruppen fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="54bbb-123">Mva-gruppen for varer fylles ut fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="54bbb-124">Hvis hovedkontoen ikke har en mva-gruppe for varer, brukes mva-gruppen for varer som er angitt i mva-parameterne i Økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="54bbb-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="54bbb-125">Du kan også angi et tall i feltet **Antall** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="54bbb-126">Valgfritt: Angi et tall i feltet **Enhetspris** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="54bbb-127">Beløpet beregnes som antallet ganger enhetsprisen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="54bbb-128">Du kan imidlertid overstyre dette ved å angi et beløp.</span><span class="sxs-lookup"><span data-stu-id="54bbb-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="54bbb-129">Hvis du vil vise merverdiavgiften som er beregnet for fakturaen, velger du **Merverdiavgift** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="54bbb-130">Du kan vise mva-beløpene på denne siden, eller du kan overstyre beløpene i kategorien **Justering** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="54bbb-131">Velg **OK** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-131">Select **OK** .</span></span>
12. <span data-ttu-id="54bbb-132">Klikk **Tillegg** for å legge til et tillegg på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="54bbb-133">Skriv inn en verdi i **Tilleggskode** -feltet.</span><span class="sxs-lookup"><span data-stu-id="54bbb-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="54bbb-134">Angi et tall i **Gebyrverdi** -feltet.</span><span class="sxs-lookup"><span data-stu-id="54bbb-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="54bbb-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="54bbb-135">Close the page.</span></span>
16. <span data-ttu-id="54bbb-136">Velg **Totaler** for å vise et sammendrag av fakturadetaljene og totaler.</span><span class="sxs-lookup"><span data-stu-id="54bbb-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="54bbb-137">Velg **Lukk** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-137">Select **Close** .</span></span>
18. <span data-ttu-id="54bbb-138">Velg **Poster** for å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="54bbb-139">Du vil fortsatt ha mulighet til å avbryte før du faktisk bokfører.</span><span class="sxs-lookup"><span data-stu-id="54bbb-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="54bbb-140">Du kan endre tidspunktet for fakturautskrifter.</span><span class="sxs-lookup"><span data-stu-id="54bbb-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="54bbb-141">Velg **Gjeldende** for å skrive ut hver faktura når den oppdateres.</span><span class="sxs-lookup"><span data-stu-id="54bbb-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="54bbb-142">Velg **Etter** for å skrive ut når alle fakturaene er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="54bbb-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="54bbb-143">Hvis du vil endre hvordan kundens kredittgrense kontrolleres før fakturaen er postert, kan du endre verdien i **Kredittmaks.type** -feltet.</span><span class="sxs-lookup"><span data-stu-id="54bbb-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="54bbb-144">Velg **Ja** for å skrive ut fakturaen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-144">To print the invoice, set the option to **Yes** .</span></span>
    * <span data-ttu-id="54bbb-145">Velg **Ja** for å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-145">To post the invoice, set the option to **Yes** .</span></span> <span data-ttu-id="54bbb-146">Du kan skrive ut fakturaen uten å postere den.</span><span class="sxs-lookup"><span data-stu-id="54bbb-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="54bbb-147">Velg **OK** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-147">Select **OK** .</span></span>

## <a name="copy-lines"></a><span data-ttu-id="54bbb-148">Kopier linjer</span><span class="sxs-lookup"><span data-stu-id="54bbb-148">Copy lines</span></span>
<span data-ttu-id="54bbb-149">Hvis du vil kopiere linjer på en fritekstfaktura, velger du én eller flere linjer og velger deretter **Kopier valgte linjer** .</span><span class="sxs-lookup"><span data-stu-id="54bbb-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines** .</span></span> <span data-ttu-id="54bbb-150">Du kan angi hvor mange kopier du vil lage, og du kan også kopiere notater og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="54bbb-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="54bbb-151">Du kan kopiere distribusjonene eller la dem bli opprettet på nytt når du posterer.</span><span class="sxs-lookup"><span data-stu-id="54bbb-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="54bbb-152">Når du har kopiert linjene, kan du redigere informasjonen etter behov.</span><span class="sxs-lookup"><span data-stu-id="54bbb-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="54bbb-153">Opprette en fritekstfaktura fra en mal</span><span class="sxs-lookup"><span data-stu-id="54bbb-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="54bbb-154">Du kan opprette en fritekstfaktura fra en mal.</span><span class="sxs-lookup"><span data-stu-id="54bbb-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="54bbb-155">Når du velger **Ny fra mal** i kategorien **Faktura** , kan du velge et malnavn og kundekontoen for den nye fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="54bbb-156">Standardverdier, for eksempel betalingsbetingelsene og betalingsmåten, kan fylles inn automatisk fra kunden, eller du kan bruke verdier som ble lagret i malen.</span><span class="sxs-lookup"><span data-stu-id="54bbb-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="54bbb-157">Det opprettes en ny fritekstfaktura, og du kan redigere verdiene etter behov.</span><span class="sxs-lookup"><span data-stu-id="54bbb-157">A new free text invoice is created, and you can edit the values as you require.</span></span>

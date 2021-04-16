---
title: Behandle eksempel på purring
description: Dette emnet går gjennom et eksempel som viser prosessen med å opprette, skrive ut og postere purringer.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1b80532463d86dd59b867fca2ee24675396ce717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826353"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="b4b6d-103">Behandle eksempel på purring</span><span class="sxs-lookup"><span data-stu-id="b4b6d-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4b6d-104">Dette emnet går gjennom et eksempel som viser prosessen med å opprette, skrive ut og postere purringer.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="b4b6d-105">Eksemplet er basert på alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** i Kreditt og purringer.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="b4b6d-106">Den bruker data i USOGRAFI-demofirmaet og en ny kunde, US-045.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="b4b6d-107">Du begynner ved å gå til **Kunder \> Kunder \> Alle kunder**, velg **Ny**, og angi deretter den obligatoriske inforamsjonen for å opprette US-045.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="b4b6d-108">Når du er ferdig, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="b4b6d-109">Gå til **Kreditt og innkrevinger \> Purring \> Definer purreforløp**, og definer purreforløpet som vist i tabellen nedenfor som er tilordnet kundeposteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="b4b6d-110">Purrekode</span><span class="sxs-lookup"><span data-stu-id="b4b6d-110">Collection   letter code</span></span>      |     <span data-ttu-id="b4b6d-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b4b6d-111">Description</span></span>                           |     <span data-ttu-id="b4b6d-112">Valuta.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-112">Currency</span></span>      |     <span data-ttu-id="b4b6d-113">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="b4b6d-113">Main   account</span></span>        |     <span data-ttu-id="b4b6d-114">Gebyr i valuta</span><span class="sxs-lookup"><span data-stu-id="b4b6d-114">Fee   in currency</span></span>     |     <span data-ttu-id="b4b6d-115">Minimum over</span><span class="sxs-lookup"><span data-stu-id="b4b6d-115">Minimum   over</span></span>        |     <span data-ttu-id="b4b6d-116">Dager   Blokker</span><span class="sxs-lookup"><span data-stu-id="b4b6d-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="b4b6d-117">Purring   brev 1</span><span class="sxs-lookup"><span data-stu-id="b4b6d-117">Collection   letter 1</span></span>         |     <span data-ttu-id="b4b6d-118">Andre   varsling med gebyr</span><span class="sxs-lookup"><span data-stu-id="b4b6d-118">Second   notification with fee</span></span>        |     <span data-ttu-id="b4b6d-119">USD</span><span class="sxs-lookup"><span data-stu-id="b4b6d-119">USD</span></span>           |                           |     <span data-ttu-id="b4b6d-120">0.00</span><span class="sxs-lookup"><span data-stu-id="b4b6d-120">0.00</span></span>                  |     <span data-ttu-id="b4b6d-121">0.00</span><span class="sxs-lookup"><span data-stu-id="b4b6d-121">0.00</span></span>                  |     <span data-ttu-id="b4b6d-122">2</span><span class="sxs-lookup"><span data-stu-id="b4b6d-122">2</span></span>                 |
|     <span data-ttu-id="b4b6d-123">Purring   brev 2</span><span class="sxs-lookup"><span data-stu-id="b4b6d-123">Collection   letter 2</span></span>         |     <span data-ttu-id="b4b6d-124">Andre   varsling med gebyr</span><span class="sxs-lookup"><span data-stu-id="b4b6d-124">Second   notification with fee</span></span>        |     <span data-ttu-id="b4b6d-125">USC</span><span class="sxs-lookup"><span data-stu-id="b4b6d-125">USC</span></span>           |     <span data-ttu-id="b4b6d-126">403150</span><span class="sxs-lookup"><span data-stu-id="b4b6d-126">403150</span></span>                |     <span data-ttu-id="b4b6d-127">20.00</span><span class="sxs-lookup"><span data-stu-id="b4b6d-127">20.00</span></span>                 |     <span data-ttu-id="b4b6d-128">10,00</span><span class="sxs-lookup"><span data-stu-id="b4b6d-128">10.00</span></span>                 |     <span data-ttu-id="b4b6d-129">3</span><span class="sxs-lookup"><span data-stu-id="b4b6d-129">3</span></span>                 |
|     <span data-ttu-id="b4b6d-130">Inkasso</span><span class="sxs-lookup"><span data-stu-id="b4b6d-130">Collection</span></span>                    |     <span data-ttu-id="b4b6d-131">Siste   varsling med gebyr</span><span class="sxs-lookup"><span data-stu-id="b4b6d-131">Final   notification with fee</span></span>         |     <span data-ttu-id="b4b6d-132">USD</span><span class="sxs-lookup"><span data-stu-id="b4b6d-132">USD</span></span>           |     <span data-ttu-id="b4b6d-133">403150</span><span class="sxs-lookup"><span data-stu-id="b4b6d-133">403150</span></span>                |     <span data-ttu-id="b4b6d-134">50.00</span><span class="sxs-lookup"><span data-stu-id="b4b6d-134">50.00</span></span>                 |     <span data-ttu-id="b4b6d-135">100.00</span><span class="sxs-lookup"><span data-stu-id="b4b6d-135">100.00</span></span>                |     <span data-ttu-id="b4b6d-136">15</span><span class="sxs-lookup"><span data-stu-id="b4b6d-136">15</span></span>                |

<span data-ttu-id="b4b6d-137">Illustrasjonen nedenfor viser informasjonen i tabellen slik den vil se ut på **purresiden**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="b4b6d-138">[![Definere en purresekvens](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="b4b6d-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="b4b6d-139">Nå må du definere de to parameterne som kreves for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="b4b6d-140">Gå til **Kreditt og innkreving \> Oppsett \> Kundeparametere** og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="b4b6d-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="b4b6d-141">I hurtigfanen **Innkrevinger** setter du alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="b4b6d-142">Kontroller at feltet **Opprett en purring per** er satt til **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="b4b6d-143">[![Angi Kundeparametere for kredittinnkrevinger](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="b4b6d-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="b4b6d-144">Gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer**, velg **Ny**, og gjør deretter følgende:</span><span class="sxs-lookup"><span data-stu-id="b4b6d-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="b4b6d-145">Velg **US-045** i feltet **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="b4b6d-146">I feltet **Fakturadata** angir du **15.01.2021**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="b4b6d-147">Angi **16.01.2021** i feltet **Forfallsdato**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="b4b6d-148">Angi **401100** i feltet **Hovedkonto** i hurtigfanen **Fakturalinjer**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="b4b6d-149">Angi **500.00** i **Enhetspris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="b4b6d-150">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-150">Select **Post**.</span></span>

    <span data-ttu-id="b4b6d-151">Du må nå angi to kreditnotaer for kunden.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="b4b6d-152">Velg **Ny**, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="b4b6d-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="b4b6d-153">Velg **US-045** i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="b4b6d-154">I feltet **Fakturadata** angir du **15.01.2021**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="b4b6d-155">Angi **16.01.2021** i feltet **Forfallsdato**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="b4b6d-156">Angi **401100** i feltet **Hovedkonto** i hurtigfanen **Fakturalinjer**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="b4b6d-157">Angi **-100,00** i feltet **Enhetspris**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="b4b6d-158">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-158">Select **Post**.</span></span>

5. <span data-ttu-id="b4b6d-159">Gjenta trinn 4, men angi **-200,00** i feltet **Enhetspris**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="b4b6d-160">Gå til **Kunder \> Kunder \> Alle kunder** og velg kunde **US-045**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="b4b6d-161">I handlingsruten velger du deretter **Transaksjoner \> Transaksjoner** for å gå gjennom kundetransaksjonene du posterte tidligere.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="b4b6d-162">[![Gå gjennom de posterte kundetransaksjonene](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="b4b6d-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="b4b6d-163">Du må nå opprette purringer for en kunde US-045.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="b4b6d-164">Gå til **Kreditt og innkreving \> Purring \> Opprett purringer**, og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="b4b6d-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="b4b6d-165">Sett alternativene **Faktura** og **Kreditnota** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="b4b6d-166">Som standrd må feltet **Purring** settes til **Purring per kunde**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="b4b6d-167">I feltet **Purredato** angir du **19.01.2021**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="b4b6d-168">I hurtigkategorien **Poster som skal inkluderes** velger du **Filter**, og deretter legger du til kunde **US-045** i feltet **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="b4b6d-169">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-169">Select **OK**.</span></span>
    5. <span data-ttu-id="b4b6d-170">Velg **OK** for å opprette purrebrev.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="b4b6d-171">Gå til **Kreditt og innkreving \> Purring \> Gjennomgå og behandle purrebrev**, og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="b4b6d-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="b4b6d-172">Legg merke til at purrekoden i både hodet og transaksjonslinjene er **Purring 1**, ettersom denne purringen er den første purringen i serien.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="b4b6d-173">(Hvis du vil vise transaksjonslinjene, må du kanskje velge hurtigfanen **Transaksjoner**.)</span><span class="sxs-lookup"><span data-stu-id="b4b6d-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="b4b6d-174">[![Kontrollere at samme purrekode vises i hodet og på linjene](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="b4b6d-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="b4b6d-175">Velg **Poster** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="b4b6d-176">I feltet **Posteringsdata** angir du **19.01.2021**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="b4b6d-177">Du må nå opprette purringer på nytt for kunde US-045.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="b4b6d-178">Gå til **Kreditt og innkreving \> Purring \> Opprett purringer**, og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="b4b6d-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="b4b6d-179">Sett alternativene **Faktura** og **Kreditnota** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="b4b6d-180">Som standrd må feltet **Purring** settes til **Purring per kunde**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="b4b6d-181">I feltet **Purredato** angir du **23.01.2021**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="b4b6d-182">I hurtigkategorien **Poster som skal inkluderes** velger du **Filter**, og deretter legger du til kunde **US-045** i feltet **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="b4b6d-183">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-183">Select **OK**.</span></span>
    5. <span data-ttu-id="b4b6d-184">Velg **OK** for å opprette purrebrev.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="b4b6d-185">Gå til **Kreditt og innkreving \> Purring \> Gjennomgå og behandle purrebrev**, og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="b4b6d-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="b4b6d-186">Legg merke til at purrekoden i hodet er **Purring 1**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="b4b6d-187">Koden på transaksjonslinjene er imidlertid **Purring 2**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="b4b6d-188">[![Kontrollerer at forskjellige purrekoder vises i hodet og på linjene](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="b4b6d-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="b4b6d-189">Kodene varierer fordi alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="b4b6d-190">Ikke poster dette purrebrevet.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="b4b6d-191">Gå til **Kreditt og innkreving \> Oppsett \> Kundeparametere**, og deretter setter du alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** til **Nei** i fanen **Purringer**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="b4b6d-192">[![Setter alternativet Ignorer betalinger og kreditnotaer ved beregning av purrekoden til Nei](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="b4b6d-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="b4b6d-193">Du må nå opprette purringer på nytt for kunde US-045.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="b4b6d-194">Gå til **Kreditt og innkreving \> Purring \> Opprett purringer**, og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="b4b6d-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="b4b6d-195">Sett alternativene **Faktura** og **Kreditnota** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="b4b6d-196">Som standrd må feltet **Purring** settes til **Purring per kunde**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="b4b6d-197">I feltet **Purredato** angir du **23.01.2021**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="b4b6d-198">I hurtigkategorien **Poster som skal inkluderes** velger du **Filter**, og deretter legger du til kunde **US-045** i feltet **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="b4b6d-199">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-199">Select **OK**.</span></span>
    5. <span data-ttu-id="b4b6d-200">Velg **OK** for å opprette purrebrev.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="b4b6d-201">Gå til **Kreditt og innkrevinger \> Purring \> Gå gjennom og behandle purrebrev**, og legg merke til at purrebrevkoden på både hodet og transaksjonslinene **Purrebrev 2**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="b4b6d-202">[![Viser på nytt at samme purrekode vises i hodet og på linjene](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="b4b6d-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="b4b6d-203">Den samme koden vises begge steder fordi alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** nå er satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="b4b6d-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>

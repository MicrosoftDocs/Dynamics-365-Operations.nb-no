---
title: Definere tilordningen for salgsordrens statuskolonner
description: Dette emnet beskriver hvordan du definerer salgsordrestatuskolonnene for dobbel skriving.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: cc70501d231390ea15104d508a36300a1b2cd44c
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744305"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="5dacf-103">Definere tilordningen for salgsordrens statuskolonner</span><span class="sxs-lookup"><span data-stu-id="5dacf-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5dacf-104">Kolonnene som angir salgsordrestatus, har forskjellige opplistingsverdier i Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="5dacf-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="5dacf-105">Det kreves tilleggsoppsett for å tilordne disse kolonnene med dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="5dacf-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="5dacf-106">Kolonner i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5dacf-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="5dacf-107">I Supply Chain Management viser to kolonner statusen for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="5dacf-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="5dacf-108">Kolonnene du må tilordne, er **Status** og **Dokumentstatus**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="5dacf-109">**Status**-opplistingen angir den totale statusen til ordren.</span><span class="sxs-lookup"><span data-stu-id="5dacf-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="5dacf-110">Denne statusen vises i ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="5dacf-110">This status is shown on the order header.</span></span>

<span data-ttu-id="5dacf-111">**Status**-opplistingen har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="5dacf-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="5dacf-112">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-112">Open Order</span></span>
- <span data-ttu-id="5dacf-113">Levert</span><span class="sxs-lookup"><span data-stu-id="5dacf-113">Delivered</span></span>
- <span data-ttu-id="5dacf-114">Fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-114">Invoiced</span></span>
- <span data-ttu-id="5dacf-115">Annullert</span><span class="sxs-lookup"><span data-stu-id="5dacf-115">Cancelled</span></span>

<span data-ttu-id="5dacf-116">**Dokumentstatus**-opplistingen angir det nyeste dokumentet som ble generert for ordren.</span><span class="sxs-lookup"><span data-stu-id="5dacf-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="5dacf-117">Hvis for eksempel ordren er bekreftet, er dette dokumentet en salgsordrebekreftelse.</span><span class="sxs-lookup"><span data-stu-id="5dacf-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="5dacf-118">Hvis en salgsordre er delvis fakturert, og den gjenværende linjen deretter blir bekreftet, forblir dokumentstatusen **Faktura**, fordi fakturaen genereres senere i prosessen.</span><span class="sxs-lookup"><span data-stu-id="5dacf-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="5dacf-119">**Dokumentstatus**-opplistingen har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="5dacf-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="5dacf-120">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="5dacf-120">Confirmation</span></span>
- <span data-ttu-id="5dacf-121">Plukkliste</span><span class="sxs-lookup"><span data-stu-id="5dacf-121">Picking List</span></span>
- <span data-ttu-id="5dacf-122">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="5dacf-122">Packing Slip</span></span>
- <span data-ttu-id="5dacf-123">Faktura</span><span class="sxs-lookup"><span data-stu-id="5dacf-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="5dacf-124">Kolonner i Salg</span><span class="sxs-lookup"><span data-stu-id="5dacf-124">columns in Sales</span></span>

<span data-ttu-id="5dacf-125">I Sales viser to kolonner statusen for ordren.</span><span class="sxs-lookup"><span data-stu-id="5dacf-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="5dacf-126">Kolonnene du må tilordne, er **Status** og **Behandlingsstatus**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="5dacf-127">**Status**-opplistingen angir den totale statusen til ordren.</span><span class="sxs-lookup"><span data-stu-id="5dacf-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="5dacf-128">Det har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="5dacf-128">It has the following values:</span></span>

- <span data-ttu-id="5dacf-129">Aktive</span><span class="sxs-lookup"><span data-stu-id="5dacf-129">Active</span></span>
- <span data-ttu-id="5dacf-130">Sendt inn</span><span class="sxs-lookup"><span data-stu-id="5dacf-130">Submitted</span></span>
- <span data-ttu-id="5dacf-131">Oppfylt</span><span class="sxs-lookup"><span data-stu-id="5dacf-131">Fulfilled</span></span>
- <span data-ttu-id="5dacf-132">Fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-132">Invoiced</span></span>
- <span data-ttu-id="5dacf-133">Annullert</span><span class="sxs-lookup"><span data-stu-id="5dacf-133">Cancelled</span></span>

<span data-ttu-id="5dacf-134">Opplistingen **Behandlingsstatus** ble innført, slik at statusen kan tilordnes mer nøyaktig ved hjelp av Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5dacf-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="5dacf-135">Følgende tabell viser tilordningen av **Behandlingsstatus** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5dacf-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="5dacf-136">Behandlingsstatus</span><span class="sxs-lookup"><span data-stu-id="5dacf-136">Processing Status</span></span>   | <span data-ttu-id="5dacf-137">Status i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5dacf-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="5dacf-138">Dokumentstatus i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5dacf-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="5dacf-139">Aktive</span><span class="sxs-lookup"><span data-stu-id="5dacf-139">Active</span></span>              | <span data-ttu-id="5dacf-140">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-140">Open Order</span></span>                        | <span data-ttu-id="5dacf-141">None</span><span class="sxs-lookup"><span data-stu-id="5dacf-141">None</span></span>                                       |
| <span data-ttu-id="5dacf-142">Bekreftet</span><span class="sxs-lookup"><span data-stu-id="5dacf-142">Confirmed</span></span>           | <span data-ttu-id="5dacf-143">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-143">Open Order</span></span>                        | <span data-ttu-id="5dacf-144">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="5dacf-144">Confirmation</span></span>                               |
| <span data-ttu-id="5dacf-145">Plukket</span><span class="sxs-lookup"><span data-stu-id="5dacf-145">Picked</span></span>              | <span data-ttu-id="5dacf-146">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-146">Open Order</span></span>                        | <span data-ttu-id="5dacf-147">Plukkliste</span><span class="sxs-lookup"><span data-stu-id="5dacf-147">Picking List</span></span>                               |
| <span data-ttu-id="5dacf-148">Delvis levert</span><span class="sxs-lookup"><span data-stu-id="5dacf-148">Partially Delivered</span></span> | <span data-ttu-id="5dacf-149">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-149">Open Order</span></span>                        | <span data-ttu-id="5dacf-150">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="5dacf-150">Packing Slip</span></span>                               |
| <span data-ttu-id="5dacf-151">Levert</span><span class="sxs-lookup"><span data-stu-id="5dacf-151">Delivered</span></span>           | <span data-ttu-id="5dacf-152">Levert</span><span class="sxs-lookup"><span data-stu-id="5dacf-152">Delivered</span></span>                         | <span data-ttu-id="5dacf-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="5dacf-153">Packing Slip</span></span>                               |
| <span data-ttu-id="5dacf-154">Delvis fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-154">Partially Invoiced</span></span>  | <span data-ttu-id="5dacf-155">Levert</span><span class="sxs-lookup"><span data-stu-id="5dacf-155">Delivered</span></span>                         | <span data-ttu-id="5dacf-156">Faktura</span><span class="sxs-lookup"><span data-stu-id="5dacf-156">Invoice</span></span>                                    |
| <span data-ttu-id="5dacf-157">Fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-157">Invoiced</span></span>            | <span data-ttu-id="5dacf-158">Fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-158">Invoiced</span></span>                          | <span data-ttu-id="5dacf-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="5dacf-159">Invoice</span></span>                                    |
| <span data-ttu-id="5dacf-160">Annullert</span><span class="sxs-lookup"><span data-stu-id="5dacf-160">Cancelled</span></span>           | <span data-ttu-id="5dacf-161">Annullert</span><span class="sxs-lookup"><span data-stu-id="5dacf-161">Cancelled</span></span>                         | <span data-ttu-id="5dacf-162">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="5dacf-162">Not applicable</span></span>                             |

<span data-ttu-id="5dacf-163">Følgende tabell viser tilordningen av **Behandlingsstatus** mellom Sales og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5dacf-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="5dacf-164">Behandlingsstatus</span><span class="sxs-lookup"><span data-stu-id="5dacf-164">Processing Status</span></span>   | <span data-ttu-id="5dacf-165">Status i Sales</span><span class="sxs-lookup"><span data-stu-id="5dacf-165">Status in Sales</span></span> | <span data-ttu-id="5dacf-166">Status i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5dacf-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="5dacf-167">Aktive</span><span class="sxs-lookup"><span data-stu-id="5dacf-167">Active</span></span>              | <span data-ttu-id="5dacf-168">Aktive</span><span class="sxs-lookup"><span data-stu-id="5dacf-168">Active</span></span>          | <span data-ttu-id="5dacf-169">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-169">Open Order</span></span>                        |
| <span data-ttu-id="5dacf-170">Bekreftet</span><span class="sxs-lookup"><span data-stu-id="5dacf-170">Confirmed</span></span>           | <span data-ttu-id="5dacf-171">Sendt inn</span><span class="sxs-lookup"><span data-stu-id="5dacf-171">Submitted</span></span>       | <span data-ttu-id="5dacf-172">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-172">Open Order</span></span>                        |
| <span data-ttu-id="5dacf-173">Plukket</span><span class="sxs-lookup"><span data-stu-id="5dacf-173">Picked</span></span>              | <span data-ttu-id="5dacf-174">Sendt inn</span><span class="sxs-lookup"><span data-stu-id="5dacf-174">Submitted</span></span>       | <span data-ttu-id="5dacf-175">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-175">Open Order</span></span>                        |
| <span data-ttu-id="5dacf-176">Delvis levert</span><span class="sxs-lookup"><span data-stu-id="5dacf-176">Partially Delivered</span></span> | <span data-ttu-id="5dacf-177">Aktive</span><span class="sxs-lookup"><span data-stu-id="5dacf-177">Active</span></span>          | <span data-ttu-id="5dacf-178">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-178">Open Order</span></span>                        |
| <span data-ttu-id="5dacf-179">Delvis fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-179">Partially Invoiced</span></span>  | <span data-ttu-id="5dacf-180">Aktive</span><span class="sxs-lookup"><span data-stu-id="5dacf-180">Active</span></span>          | <span data-ttu-id="5dacf-181">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="5dacf-181">Open Order</span></span>                        |
| <span data-ttu-id="5dacf-182">Delvis fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-182">Partially Invoiced</span></span>  | <span data-ttu-id="5dacf-183">Oppfylt</span><span class="sxs-lookup"><span data-stu-id="5dacf-183">Fulfilled</span></span>       | <span data-ttu-id="5dacf-184">Levert</span><span class="sxs-lookup"><span data-stu-id="5dacf-184">Delivered</span></span>                         |
| <span data-ttu-id="5dacf-185">Fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-185">Invoiced</span></span>            | <span data-ttu-id="5dacf-186">Fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-186">Invoiced</span></span>        | <span data-ttu-id="5dacf-187">Fakturert</span><span class="sxs-lookup"><span data-stu-id="5dacf-187">Invoiced</span></span>                          |
| <span data-ttu-id="5dacf-188">Annullert</span><span class="sxs-lookup"><span data-stu-id="5dacf-188">Cancelled</span></span>           | <span data-ttu-id="5dacf-189">Annullert</span><span class="sxs-lookup"><span data-stu-id="5dacf-189">Cancelled</span></span>       | <span data-ttu-id="5dacf-190">Annullert</span><span class="sxs-lookup"><span data-stu-id="5dacf-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="5dacf-191">Installasjon</span><span class="sxs-lookup"><span data-stu-id="5dacf-191">Setup</span></span>

<span data-ttu-id="5dacf-192">Hvis du vil konfigurere tilordningen for salgsordrestatuskolonnene, må du aktivere attributtene **IsSOPIntegrationEnabled** og **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="5dacf-193">Følg denne fremgangsmåten for å aktivere attributtet **IsSOPIntegrationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="5dacf-194">I en webleser kan du gå til `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="5dacf-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="5dacf-195">Erstatt **\<test-name\>** med firmaets kobling til Sales.</span><span class="sxs-lookup"><span data-stu-id="5dacf-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="5dacf-196">På siden som åpnes, finner du **organizationid**, og noter verdien.</span><span class="sxs-lookup"><span data-stu-id="5dacf-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Finne organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="5dacf-198">I Sales åpner du leserkonsollen og kjører følgende skript:</span><span class="sxs-lookup"><span data-stu-id="5dacf-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="5dacf-199">Bruk **organizationid**-verdien fra trinn 2.</span><span class="sxs-lookup"><span data-stu-id="5dacf-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kode i leserkonsollen](media/sales-map-script.png)

4. <span data-ttu-id="5dacf-201">Kontroller at **IsSOPIntegrationEnabled** er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="5dacf-202">Bruk URL-adressen fra trinn 1 til å kontrollere verdien.</span><span class="sxs-lookup"><span data-stu-id="5dacf-202">Use the URL from step 1 to check the value.</span></span>

    ![Kontroller at IsSOPIntegrationEnabled er satt til sann](media/sales-map-integration-enabled.png)

<span data-ttu-id="5dacf-204">Følg denne fremgangsmåten for å aktivere attributtet **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="5dacf-205">I Sales kan du gå til **Innstilling \> Tilpasning \> Tilpass systemet**, velge **Brukertabell** og deretter åpne **Skjema \> Bruker**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Åpne brukerskjemaet](media/sales-map-user.png)

2. <span data-ttu-id="5dacf-207">I Feltutforsker finner du **Modusen Integreringsbruker** og dobbeltklikker den for å legge den til i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="5dacf-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="5dacf-208">Lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="5dacf-208">Save your change.</span></span>

    ![Legge til kolonnen Integreringsbruker i skjemaet](media/sales-map-field-explorer.png)

3. <span data-ttu-id="5dacf-210">I Sales går du til **Innstilling \> Sikkerhet \> Brukere** og endrer visningen fra **Aktiverte brukere** til **Programbrukere**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Endre visning fra Aktiverte brukere til Programbrukere](media/sales-map-enabled-users.png)

4. <span data-ttu-id="5dacf-212">Velg de to oppføringene for **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Liste over programbrukere](media/sales-map-user-mode.png)

5. <span data-ttu-id="5dacf-214">Endre verdien for kolonnen **Integreringsbruker** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5dacf-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Endre verdien for kolonnen Integreringsbruker](media/sales-map-user-mode-yes.png)

<span data-ttu-id="5dacf-216">Salgsordrene er nå tilordnet.</span><span class="sxs-lookup"><span data-stu-id="5dacf-216">Your sales orders are now mapped.</span></span>

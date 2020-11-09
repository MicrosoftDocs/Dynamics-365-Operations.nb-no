---
title: Definere tilordningen for salgsordrestatusfeltene
description: Dette emnet beskriver hvordan du definerer salgsordrestatusfeltene for dobbelt skriving.
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
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997680"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="b24d1-103">Definere tilordningen for salgsordrestatusfeltene</span><span class="sxs-lookup"><span data-stu-id="b24d1-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b24d1-104">Feltene som angir salgsordrestatus, har forskjellige opplistingsverdier i Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b24d1-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="b24d1-105">Det kreves tilleggsoppsett for å tilordne disse feltene med dobbelt skriving.</span><span class="sxs-lookup"><span data-stu-id="b24d1-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="b24d1-106">Felt i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b24d1-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="b24d1-107">I Supply Chain Management viser to felt statusen for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b24d1-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="b24d1-108">Feltene du må tilordne, er **Status** og **Dokumentstatus**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="b24d1-109">**Status** -opplistingen angir den totale statusen til ordren.</span><span class="sxs-lookup"><span data-stu-id="b24d1-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="b24d1-110">Denne statusen vises i ordrehodet.</span><span class="sxs-lookup"><span data-stu-id="b24d1-110">This status is shown on the order header.</span></span>

<span data-ttu-id="b24d1-111">**Status** -opplistingen har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b24d1-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="b24d1-112">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-112">Open Order</span></span>
- <span data-ttu-id="b24d1-113">Levert</span><span class="sxs-lookup"><span data-stu-id="b24d1-113">Delivered</span></span>
- <span data-ttu-id="b24d1-114">Fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-114">Invoiced</span></span>
- <span data-ttu-id="b24d1-115">Annullert</span><span class="sxs-lookup"><span data-stu-id="b24d1-115">Cancelled</span></span>

<span data-ttu-id="b24d1-116">**Dokumentstatus** -opplistingen angir det nyeste dokumentet som ble generert for ordren.</span><span class="sxs-lookup"><span data-stu-id="b24d1-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="b24d1-117">Hvis for eksempel ordren er bekreftet, er dette dokumentet en salgsordrebekreftelse.</span><span class="sxs-lookup"><span data-stu-id="b24d1-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="b24d1-118">Hvis en salgsordre er delvis fakturert, og den gjenværende linjen deretter blir bekreftet, forblir dokumentstatusen **Faktura** , fordi fakturaen genereres senere i prosessen.</span><span class="sxs-lookup"><span data-stu-id="b24d1-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice** , because the invoice is generated later in the process.</span></span>

<span data-ttu-id="b24d1-119">**Dokumentstatus** -opplistingen har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b24d1-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="b24d1-120">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="b24d1-120">Confirmation</span></span>
- <span data-ttu-id="b24d1-121">Plukkliste</span><span class="sxs-lookup"><span data-stu-id="b24d1-121">Picking List</span></span>
- <span data-ttu-id="b24d1-122">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="b24d1-122">Packing Slip</span></span>
- <span data-ttu-id="b24d1-123">Faktura</span><span class="sxs-lookup"><span data-stu-id="b24d1-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="b24d1-124">Felt i Sales</span><span class="sxs-lookup"><span data-stu-id="b24d1-124">Fields in Sales</span></span>

<span data-ttu-id="b24d1-125">I Sales viser to felt statusen for ordren.</span><span class="sxs-lookup"><span data-stu-id="b24d1-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="b24d1-126">Feltene du må tilordne, er **Status** og **Behandlingsstatus**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="b24d1-127">**Status** -opplistingen angir den totale statusen til ordren.</span><span class="sxs-lookup"><span data-stu-id="b24d1-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="b24d1-128">Det har følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="b24d1-128">It has the following values:</span></span>

- <span data-ttu-id="b24d1-129">Aktive</span><span class="sxs-lookup"><span data-stu-id="b24d1-129">Active</span></span>
- <span data-ttu-id="b24d1-130">Sendt inn</span><span class="sxs-lookup"><span data-stu-id="b24d1-130">Submitted</span></span>
- <span data-ttu-id="b24d1-131">Oppfylt</span><span class="sxs-lookup"><span data-stu-id="b24d1-131">Fulfilled</span></span>
- <span data-ttu-id="b24d1-132">Fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-132">Invoiced</span></span>
- <span data-ttu-id="b24d1-133">Annullert</span><span class="sxs-lookup"><span data-stu-id="b24d1-133">Cancelled</span></span>

<span data-ttu-id="b24d1-134">Opplistingen **Behandlingsstatus** ble innført, slik at statusen kan tilordnes mer nøyaktig ved hjelp av Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b24d1-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="b24d1-135">Følgende tabell viser tilordningen av **Behandlingsstatus** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b24d1-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="b24d1-136">Behandlingsstatus</span><span class="sxs-lookup"><span data-stu-id="b24d1-136">Processing Status</span></span>   | <span data-ttu-id="b24d1-137">Status i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b24d1-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="b24d1-138">Dokumentstatus i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b24d1-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="b24d1-139">Aktive</span><span class="sxs-lookup"><span data-stu-id="b24d1-139">Active</span></span>              | <span data-ttu-id="b24d1-140">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-140">Open Order</span></span>                        | <span data-ttu-id="b24d1-141">None</span><span class="sxs-lookup"><span data-stu-id="b24d1-141">None</span></span>                                       |
| <span data-ttu-id="b24d1-142">Bekreftet</span><span class="sxs-lookup"><span data-stu-id="b24d1-142">Confirmed</span></span>           | <span data-ttu-id="b24d1-143">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-143">Open Order</span></span>                        | <span data-ttu-id="b24d1-144">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="b24d1-144">Confirmation</span></span>                               |
| <span data-ttu-id="b24d1-145">Plukket</span><span class="sxs-lookup"><span data-stu-id="b24d1-145">Picked</span></span>              | <span data-ttu-id="b24d1-146">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-146">Open Order</span></span>                        | <span data-ttu-id="b24d1-147">Plukkliste</span><span class="sxs-lookup"><span data-stu-id="b24d1-147">Picking List</span></span>                               |
| <span data-ttu-id="b24d1-148">Delvis levert</span><span class="sxs-lookup"><span data-stu-id="b24d1-148">Partially Delivered</span></span> | <span data-ttu-id="b24d1-149">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-149">Open Order</span></span>                        | <span data-ttu-id="b24d1-150">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="b24d1-150">Packing Slip</span></span>                               |
| <span data-ttu-id="b24d1-151">Levert</span><span class="sxs-lookup"><span data-stu-id="b24d1-151">Delivered</span></span>           | <span data-ttu-id="b24d1-152">Levert</span><span class="sxs-lookup"><span data-stu-id="b24d1-152">Delivered</span></span>                         | <span data-ttu-id="b24d1-153">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="b24d1-153">Packing Slip</span></span>                               |
| <span data-ttu-id="b24d1-154">Delvis fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-154">Partially Invoiced</span></span>  | <span data-ttu-id="b24d1-155">Levert</span><span class="sxs-lookup"><span data-stu-id="b24d1-155">Delivered</span></span>                         | <span data-ttu-id="b24d1-156">Faktura</span><span class="sxs-lookup"><span data-stu-id="b24d1-156">Invoice</span></span>                                    |
| <span data-ttu-id="b24d1-157">Fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-157">Invoiced</span></span>            | <span data-ttu-id="b24d1-158">Fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-158">Invoiced</span></span>                          | <span data-ttu-id="b24d1-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="b24d1-159">Invoice</span></span>                                    |
| <span data-ttu-id="b24d1-160">Annullert</span><span class="sxs-lookup"><span data-stu-id="b24d1-160">Cancelled</span></span>           | <span data-ttu-id="b24d1-161">Annullert</span><span class="sxs-lookup"><span data-stu-id="b24d1-161">Cancelled</span></span>                         | <span data-ttu-id="b24d1-162">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="b24d1-162">Not applicable</span></span>                             |

<span data-ttu-id="b24d1-163">Følgende tabell viser tilordningen av **Behandlingsstatus** mellom Sales og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b24d1-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="b24d1-164">Behandlingsstatus</span><span class="sxs-lookup"><span data-stu-id="b24d1-164">Processing Status</span></span>   | <span data-ttu-id="b24d1-165">Status i Sales</span><span class="sxs-lookup"><span data-stu-id="b24d1-165">Status in Sales</span></span> | <span data-ttu-id="b24d1-166">Status i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b24d1-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="b24d1-167">Aktive</span><span class="sxs-lookup"><span data-stu-id="b24d1-167">Active</span></span>              | <span data-ttu-id="b24d1-168">Aktive</span><span class="sxs-lookup"><span data-stu-id="b24d1-168">Active</span></span>          | <span data-ttu-id="b24d1-169">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-169">Open Order</span></span>                        |
| <span data-ttu-id="b24d1-170">Bekreftet</span><span class="sxs-lookup"><span data-stu-id="b24d1-170">Confirmed</span></span>           | <span data-ttu-id="b24d1-171">Sendt inn</span><span class="sxs-lookup"><span data-stu-id="b24d1-171">Submitted</span></span>       | <span data-ttu-id="b24d1-172">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-172">Open Order</span></span>                        |
| <span data-ttu-id="b24d1-173">Plukket</span><span class="sxs-lookup"><span data-stu-id="b24d1-173">Picked</span></span>              | <span data-ttu-id="b24d1-174">Sendt inn</span><span class="sxs-lookup"><span data-stu-id="b24d1-174">Submitted</span></span>       | <span data-ttu-id="b24d1-175">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-175">Open Order</span></span>                        |
| <span data-ttu-id="b24d1-176">Delvis levert</span><span class="sxs-lookup"><span data-stu-id="b24d1-176">Partially Delivered</span></span> | <span data-ttu-id="b24d1-177">Aktive</span><span class="sxs-lookup"><span data-stu-id="b24d1-177">Active</span></span>          | <span data-ttu-id="b24d1-178">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-178">Open Order</span></span>                        |
| <span data-ttu-id="b24d1-179">Delvis fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-179">Partially Invoiced</span></span>  | <span data-ttu-id="b24d1-180">Aktive</span><span class="sxs-lookup"><span data-stu-id="b24d1-180">Active</span></span>          | <span data-ttu-id="b24d1-181">Åpen ordre</span><span class="sxs-lookup"><span data-stu-id="b24d1-181">Open Order</span></span>                        |
| <span data-ttu-id="b24d1-182">Delvis fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-182">Partially Invoiced</span></span>  | <span data-ttu-id="b24d1-183">Oppfylt</span><span class="sxs-lookup"><span data-stu-id="b24d1-183">Fulfilled</span></span>       | <span data-ttu-id="b24d1-184">Levert</span><span class="sxs-lookup"><span data-stu-id="b24d1-184">Delivered</span></span>                         |
| <span data-ttu-id="b24d1-185">Fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-185">Invoiced</span></span>            | <span data-ttu-id="b24d1-186">Fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-186">Invoiced</span></span>        | <span data-ttu-id="b24d1-187">Fakturert</span><span class="sxs-lookup"><span data-stu-id="b24d1-187">Invoiced</span></span>                          |
| <span data-ttu-id="b24d1-188">Annullert</span><span class="sxs-lookup"><span data-stu-id="b24d1-188">Cancelled</span></span>           | <span data-ttu-id="b24d1-189">Annullert</span><span class="sxs-lookup"><span data-stu-id="b24d1-189">Cancelled</span></span>       | <span data-ttu-id="b24d1-190">Annullert</span><span class="sxs-lookup"><span data-stu-id="b24d1-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="b24d1-191">Installasjon</span><span class="sxs-lookup"><span data-stu-id="b24d1-191">Setup</span></span>

<span data-ttu-id="b24d1-192">Hvis du vil konfigurere tilordningen for salgsordrestatusfeltene, må du aktivere attributtene **IsSOPIntegrationEnabled** og **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="b24d1-193">Følg denne fremgangsmåten for å aktivere attributtet **IsSOPIntegrationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="b24d1-194">I en webleser kan du gå til `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="b24d1-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="b24d1-195">Erstatt **\<test-name\>** med firmaets kobling til Sales.</span><span class="sxs-lookup"><span data-stu-id="b24d1-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="b24d1-196">På siden som åpnes, finner du **organizationid** , og noter verdien.</span><span class="sxs-lookup"><span data-stu-id="b24d1-196">On the page that is opened, find **organizationid** , and make a note of the value.</span></span>

    ![Finne organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="b24d1-198">I Sales åpner du leserkonsollen og kjører følgende skript:</span><span class="sxs-lookup"><span data-stu-id="b24d1-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="b24d1-199">Bruk **organizationid** -verdien fra trinn 2.</span><span class="sxs-lookup"><span data-stu-id="b24d1-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kode i leserkonsollen](media/sales-map-script.png)

4. <span data-ttu-id="b24d1-201">Kontroller at **IsSOPIntegrationEnabled** er satt til **sann**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="b24d1-202">Bruk URL-adressen fra trinn 1 til å kontrollere verdien.</span><span class="sxs-lookup"><span data-stu-id="b24d1-202">Use the URL from step 1 to check the value.</span></span>

    ![Kontroller at IsSOPIntegrationEnabled er satt til sann](media/sales-map-integration-enabled.png)

<span data-ttu-id="b24d1-204">Følg denne fremgangsmåten for å aktivere attributtet **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="b24d1-205">I Sales kan du gå til **Innstilling \> Tilpasning \> Tilpass systemet** , velge **Brukerenhet** og deretter åpne **Skjema \> Bruker**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-205">In Sales, go to **Setting \> Customization \> Customize the System** , select **User entity** , and then open **Form \> User**.</span></span>

    ![Åpne brukerskjemaet](media/sales-map-user.png)

2. <span data-ttu-id="b24d1-207">I Feltutforsker finner du **Modusen Integreringsbruker** og dobbeltklikker den for å legge den til i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="b24d1-207">In Field Explorer, find **Integration user mode** , and double-click it to add it to the form.</span></span> <span data-ttu-id="b24d1-208">Lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="b24d1-208">Save your change.</span></span>

    ![Legge til feltet Integreringsbruker i skjemaet](media/sales-map-field-explorer.png)

3. <span data-ttu-id="b24d1-210">I Sales går du til **Innstilling \> Sikkerhet \> Brukere** og endrer visningen fra **Aktiverte brukere** til **Programbrukere**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-210">In Sales, go to **Setting \> Security \> Users** , and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Endre visning fra Aktiverte brukere til Programbrukere](media/sales-map-enabled-users.png)

4. <span data-ttu-id="b24d1-212">Velg de to oppføringene for **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Liste over programbrukere](media/sales-map-user-mode.png)

5. <span data-ttu-id="b24d1-214">Endre verdien for feltet **Integreringsbruker** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b24d1-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Endre verdien for feltet Integreringsbruker](media/sales-map-user-mode-yes.png)

<span data-ttu-id="b24d1-216">Salgsordrene er nå tilordnet.</span><span class="sxs-lookup"><span data-stu-id="b24d1-216">Your sales orders are now mapped.</span></span>

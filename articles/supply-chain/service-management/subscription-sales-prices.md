---
title: Salgspriser for abonnement
description: Når du oppretter et abonnement, avledes salgsprisen fra salgsprisoppsettet som ble opprettet i skjemaet Salgspris (abonnement).
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03efbbca4fc9da76c6ead7566457beb79c8c249
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434332"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="8006f-103">Salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="8006f-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8006f-104">Når du oppretter et abonnement, avledes salgsprisen fra salgsprisoppsettet som ble opprettet i skjemaet **Salgspris (abonnement)**.</span><span class="sxs-lookup"><span data-stu-id="8006f-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="8006f-105">I skjemaet **Salgspris (abonnement)** kan du opprette salgspriser for et bestemt abonnement, eller du kan opprette salgspriser som er mer generelle.</span><span class="sxs-lookup"><span data-stu-id="8006f-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="8006f-106">Før en salgspris kan brukes på et abonnement, må periodekoden og valutaen for abonnementet være identisk med periodekoden og valutaen for salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="8006f-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="8006f-107">Hvis periodekoden og valutaen er identiske for abonnementet og salgsprisen, velges salgspriser for abonnement på grunnlag av prioritetene som er angitt i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="8006f-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="8006f-108">En to celle i tabellen angir et tomt felt, og en X angir en verdi som er lik verdien i abonnementet der transaksjonen genereres fra.</span><span class="sxs-lookup"><span data-stu-id="8006f-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8006f-109">Prioritet </span><span class="sxs-lookup"><span data-stu-id="8006f-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="8006f-110"><strong>Kategori</strong></span><span class="sxs-lookup"><span data-stu-id="8006f-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="8006f-111"><strong>Prosjekt-ID</strong></span><span class="sxs-lookup"><span data-stu-id="8006f-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="8006f-112"><strong>Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="8006f-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="8006f-113"><strong>Salgsvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="8006f-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="8006f-114"><strong>Periodekode</strong></span><span class="sxs-lookup"><span data-stu-id="8006f-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8006f-115">1</span><span class="sxs-lookup"><span data-stu-id="8006f-115">1</span></span></p></td>
<td><p><span data-ttu-id="8006f-116">X</span><span class="sxs-lookup"><span data-stu-id="8006f-116">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-117">X</span><span class="sxs-lookup"><span data-stu-id="8006f-117">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-118">X</span><span class="sxs-lookup"><span data-stu-id="8006f-118">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-119">X</span><span class="sxs-lookup"><span data-stu-id="8006f-119">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-120">X</span><span class="sxs-lookup"><span data-stu-id="8006f-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8006f-121">2</span><span class="sxs-lookup"><span data-stu-id="8006f-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8006f-122">X</span><span class="sxs-lookup"><span data-stu-id="8006f-122">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-123">X</span><span class="sxs-lookup"><span data-stu-id="8006f-123">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-124">X</span><span class="sxs-lookup"><span data-stu-id="8006f-124">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-125">X</span><span class="sxs-lookup"><span data-stu-id="8006f-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8006f-126">3</span><span class="sxs-lookup"><span data-stu-id="8006f-126">3</span></span></p></td>
<td><p><span data-ttu-id="8006f-127">X</span><span class="sxs-lookup"><span data-stu-id="8006f-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8006f-128">X</span><span class="sxs-lookup"><span data-stu-id="8006f-128">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-129">X</span><span class="sxs-lookup"><span data-stu-id="8006f-129">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-130">X</span><span class="sxs-lookup"><span data-stu-id="8006f-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8006f-131">4</span><span class="sxs-lookup"><span data-stu-id="8006f-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8006f-132">X</span><span class="sxs-lookup"><span data-stu-id="8006f-132">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-133">X</span><span class="sxs-lookup"><span data-stu-id="8006f-133">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-134">X</span><span class="sxs-lookup"><span data-stu-id="8006f-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8006f-135">5</span><span class="sxs-lookup"><span data-stu-id="8006f-135">5</span></span></p></td>
<td><p><span data-ttu-id="8006f-136">X</span><span class="sxs-lookup"><span data-stu-id="8006f-136">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-137">X</span><span class="sxs-lookup"><span data-stu-id="8006f-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8006f-138">X</span><span class="sxs-lookup"><span data-stu-id="8006f-138">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-139">X</span><span class="sxs-lookup"><span data-stu-id="8006f-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8006f-140">6</span><span class="sxs-lookup"><span data-stu-id="8006f-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8006f-141">X</span><span class="sxs-lookup"><span data-stu-id="8006f-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8006f-142">X</span><span class="sxs-lookup"><span data-stu-id="8006f-142">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-143">X</span><span class="sxs-lookup"><span data-stu-id="8006f-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8006f-144">7</span><span class="sxs-lookup"><span data-stu-id="8006f-144">7</span></span></p></td>
<td><p><span data-ttu-id="8006f-145">X</span><span class="sxs-lookup"><span data-stu-id="8006f-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8006f-146">X</span><span class="sxs-lookup"><span data-stu-id="8006f-146">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-147">X</span><span class="sxs-lookup"><span data-stu-id="8006f-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8006f-148">8</span><span class="sxs-lookup"><span data-stu-id="8006f-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8006f-149">X</span><span class="sxs-lookup"><span data-stu-id="8006f-149">X</span></span></p></td>
<td><p><span data-ttu-id="8006f-150">X</span><span class="sxs-lookup"><span data-stu-id="8006f-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8006f-151">Når det opprettes en abonnementsavgift, velges salgsprisen med det største detaljnivået, som angitt i tabellen ovenfor, som salgsprisen for abonnement.</span><span class="sxs-lookup"><span data-stu-id="8006f-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="8006f-152">Oppdatere og indeksere salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="8006f-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="8006f-153">Du kan oppdatere salgsprisen for abonnement ved å oppdatere basisprisen eller indeksen.</span><span class="sxs-lookup"><span data-stu-id="8006f-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="8006f-154">Du kan oppdatere med en prosentverdi eller til en ny verdi.</span><span class="sxs-lookup"><span data-stu-id="8006f-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="8006f-155">Salgspriser for abonnementsavgift</span><span class="sxs-lookup"><span data-stu-id="8006f-155">Subscription fee sales prices</span></span>

<span data-ttu-id="8006f-156">Når du oppretter en abonnementsavgift, er salgsprisen basert på salgsprisoppsettet for abonnementet.</span><span class="sxs-lookup"><span data-stu-id="8006f-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="8006f-157">Du kan enten bruke basisprisen fra abonnementets prisoppsett eller opprette indekserte salgspriser.</span><span class="sxs-lookup"><span data-stu-id="8006f-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="8006f-158">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8006f-158">Example</span></span>

<span data-ttu-id="8006f-159">Du vil definere salgspriser for abonnement på EUR 500 for det nye prosjektet 9030.</span><span class="sxs-lookup"><span data-stu-id="8006f-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="8006f-160">I skjemaet **Salgspris (abonnement)** oppretter du en salgsprislinje for abonnement som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="8006f-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8006f-161">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="8006f-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="8006f-162">Kategori</span><span class="sxs-lookup"><span data-stu-id="8006f-162">Category</span></span></p></th>
<th><p><span data-ttu-id="8006f-163">Project</span><span class="sxs-lookup"><span data-stu-id="8006f-163">Project</span></span></p></th>
<th><p><span data-ttu-id="8006f-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="8006f-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8006f-165">Periodekode</span><span class="sxs-lookup"><span data-stu-id="8006f-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="8006f-166">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="8006f-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8006f-167">Salgspris</span><span class="sxs-lookup"><span data-stu-id="8006f-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8006f-168">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="8006f-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8006f-169">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8006f-170">Måned</span><span class="sxs-lookup"><span data-stu-id="8006f-170">Month</span></span></p></td>
<td><p><span data-ttu-id="8006f-171">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-172">500</span><span class="sxs-lookup"><span data-stu-id="8006f-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8006f-173">Legg merke til at feltene **Kategori** og **Abonnement** er tomme.</span><span class="sxs-lookup"><span data-stu-id="8006f-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="8006f-174">Deretter oppretter du følgende abonnementer:</span><span class="sxs-lookup"><span data-stu-id="8006f-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8006f-175">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="8006f-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="8006f-176">Project</span><span class="sxs-lookup"><span data-stu-id="8006f-176">Project</span></span></p></th>
<th><p><span data-ttu-id="8006f-177">Abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="8006f-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="8006f-178">Kategori</span><span class="sxs-lookup"><span data-stu-id="8006f-178">Category</span></span></p></th>
<th><p><span data-ttu-id="8006f-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="8006f-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="8006f-180">Periodekode</span><span class="sxs-lookup"><span data-stu-id="8006f-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8006f-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="8006f-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="8006f-182">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-182">9030</span></span></p></td>
<td><p><span data-ttu-id="8006f-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="8006f-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="8006f-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="8006f-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="8006f-185">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-186">Månedlig</span><span class="sxs-lookup"><span data-stu-id="8006f-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8006f-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="8006f-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="8006f-188">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-188">9030</span></span></p></td>
<td><p><span data-ttu-id="8006f-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="8006f-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="8006f-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="8006f-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8006f-191">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-192">Månedlig</span><span class="sxs-lookup"><span data-stu-id="8006f-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8006f-193">Nå oppretter du abonnementsavgifter for begge abonnementer i abonnementsgruppen Sub1:</span><span class="sxs-lookup"><span data-stu-id="8006f-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="8006f-194">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="8006f-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="8006f-195">I skjemaet **Abonnementsgrupper** klikker du **Funksjon** \> **Opprett abonnementsavgift**.</span><span class="sxs-lookup"><span data-stu-id="8006f-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="8006f-196">Angi aktuell informasjon i skjemaet **Opprett abonnementsavgift**.</span><span class="sxs-lookup"><span data-stu-id="8006f-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="8006f-197">Hvis du vil ha mer informasjon, kan du se [Opprette abonnementsgebyrtransaksjoner](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8006f-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="8006f-198">Abonnementsavgifter med en salgspris på EUR 500 opprettes for begge abonnementer, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="8006f-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8006f-199">Prosjektdato</span><span class="sxs-lookup"><span data-stu-id="8006f-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="8006f-200">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="8006f-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="8006f-201">Project</span><span class="sxs-lookup"><span data-stu-id="8006f-201">Project</span></span></p></th>
<th><p><span data-ttu-id="8006f-202">Kategori</span><span class="sxs-lookup"><span data-stu-id="8006f-202">Category</span></span></p></th>
<th><p><span data-ttu-id="8006f-203">Startdato</span><span class="sxs-lookup"><span data-stu-id="8006f-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="8006f-204">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="8006f-204">End date</span></span></p></th>
<th><p><span data-ttu-id="8006f-205">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="8006f-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8006f-206">Salgspris</span><span class="sxs-lookup"><span data-stu-id="8006f-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8006f-207">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="8006f-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="8006f-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="8006f-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="8006f-209">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-209">9030</span></span></p></td>
<td><p><span data-ttu-id="8006f-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="8006f-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="8006f-211">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="8006f-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="8006f-212">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="8006f-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="8006f-213">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-214">500</span><span class="sxs-lookup"><span data-stu-id="8006f-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8006f-215">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="8006f-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="8006f-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="8006f-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="8006f-217">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-217">9030</span></span></p></td>
<td><p><span data-ttu-id="8006f-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="8006f-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8006f-219">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="8006f-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="8006f-220">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="8006f-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="8006f-221">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-222">500</span><span class="sxs-lookup"><span data-stu-id="8006f-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8006f-223">Senere bestemmer du deg for at du vil angi salgspriser for kategorien SubCat1 for prosjekt 9030.</span><span class="sxs-lookup"><span data-stu-id="8006f-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="8006f-224">Derfor oppretter du en ny salgsprislinje som har en salgspris på EUR 550 for kombinasjonen av prosjekt 9030 og gebyrkategorien SubCat1.</span><span class="sxs-lookup"><span data-stu-id="8006f-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="8006f-225">Det finnes nå to salgsprislinjer for abonnement for prosjekt 9030, som vist i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="8006f-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8006f-226">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="8006f-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="8006f-227">Kategori</span><span class="sxs-lookup"><span data-stu-id="8006f-227">Category</span></span></p></th>
<th><p><span data-ttu-id="8006f-228">Project</span><span class="sxs-lookup"><span data-stu-id="8006f-228">Project</span></span></p></th>
<th><p><span data-ttu-id="8006f-229">Abonnement</span><span class="sxs-lookup"><span data-stu-id="8006f-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8006f-230">Periodekode</span><span class="sxs-lookup"><span data-stu-id="8006f-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="8006f-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="8006f-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="8006f-232">Salgspris</span><span class="sxs-lookup"><span data-stu-id="8006f-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8006f-233">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="8006f-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8006f-234">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8006f-235">Måned</span><span class="sxs-lookup"><span data-stu-id="8006f-235">Month</span></span></p></td>
<td><p><span data-ttu-id="8006f-236">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-237">500</span><span class="sxs-lookup"><span data-stu-id="8006f-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8006f-238">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="8006f-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="8006f-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="8006f-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="8006f-240">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8006f-241">Måned</span><span class="sxs-lookup"><span data-stu-id="8006f-241">Month</span></span></p></td>
<td><p><span data-ttu-id="8006f-242">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-243">550</span><span class="sxs-lookup"><span data-stu-id="8006f-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8006f-244">Du gjentar fremgangsmåten som er beskrevet ovenfor for å opprette abonnementsavgifter for begge abonnementer i abonnementsgruppen Sub1.</span><span class="sxs-lookup"><span data-stu-id="8006f-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="8006f-245">Tabellen nedenfor viser transaksjonene som opprettes for hvert abonnement som er knyttet til abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="8006f-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8006f-246">Prosjektdato</span><span class="sxs-lookup"><span data-stu-id="8006f-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="8006f-247">Abonnement</span><span class="sxs-lookup"><span data-stu-id="8006f-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8006f-248">Project</span><span class="sxs-lookup"><span data-stu-id="8006f-248">Project</span></span></p></th>
<th><p><span data-ttu-id="8006f-249">Kategori</span><span class="sxs-lookup"><span data-stu-id="8006f-249">Category</span></span></p></th>
<th><p><span data-ttu-id="8006f-250">Startdato</span><span class="sxs-lookup"><span data-stu-id="8006f-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="8006f-251">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="8006f-251">End date</span></span></p></th>
<th><p><span data-ttu-id="8006f-252">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="8006f-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8006f-253">Salgspris</span><span class="sxs-lookup"><span data-stu-id="8006f-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8006f-254">28.07.2007</span><span class="sxs-lookup"><span data-stu-id="8006f-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="8006f-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="8006f-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="8006f-256">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-256">9030</span></span></p></td>
<td><p><span data-ttu-id="8006f-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="8006f-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="8006f-258">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="8006f-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="8006f-259">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="8006f-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="8006f-260">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-261">550</span><span class="sxs-lookup"><span data-stu-id="8006f-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8006f-262">28.07.2008</span><span class="sxs-lookup"><span data-stu-id="8006f-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="8006f-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="8006f-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="8006f-264">9030</span><span class="sxs-lookup"><span data-stu-id="8006f-264">9030</span></span></p></td>
<td><p><span data-ttu-id="8006f-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="8006f-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8006f-266">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="8006f-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="8006f-267">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="8006f-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="8006f-268">EUR</span><span class="sxs-lookup"><span data-stu-id="8006f-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="8006f-269">500</span><span class="sxs-lookup"><span data-stu-id="8006f-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8006f-270">I den første transaksjonen for abonnement 00020\_135 er salgsprisen på EUR 550 avledet fra salgsprisen for abonnement som er definert for kombinasjonen av det bestemte prosjektet og kategorien.</span><span class="sxs-lookup"><span data-stu-id="8006f-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="8006f-271">I den andre transaksjonen for abonnement 00021\_135 brukes salgsprisen på EUR 500 som salgsprisen for prosjektabonnement, fordi det ikke er definert en pris for kombinasjonen av prosjekt 9030 og kategori SubCat2.</span><span class="sxs-lookup"><span data-stu-id="8006f-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="8006f-272">Se også</span><span class="sxs-lookup"><span data-stu-id="8006f-272">See also</span></span>

[<span data-ttu-id="8006f-273">Oppdatere og indeksere salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="8006f-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  



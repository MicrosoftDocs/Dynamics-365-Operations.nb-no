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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f4e3f3bdbdad7a48b89bad7da96d221f09bdb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974229"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="42edc-103">Salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="42edc-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="42edc-104">Når du oppretter et abonnement, avledes salgsprisen fra salgsprisoppsettet som ble opprettet i skjemaet **Salgspris (abonnement)**.</span><span class="sxs-lookup"><span data-stu-id="42edc-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="42edc-105">I skjemaet **Salgspris (abonnement)** kan du opprette salgspriser for et bestemt abonnement, eller du kan opprette salgspriser som er mer generelle.</span><span class="sxs-lookup"><span data-stu-id="42edc-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="42edc-106">Før en salgspris kan brukes på et abonnement, må periodekoden og valutaen for abonnementet være identisk med periodekoden og valutaen for salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="42edc-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="42edc-107">Hvis periodekoden og valutaen er identiske for abonnementet og salgsprisen, velges salgspriser for abonnement på grunnlag av prioritetene som er angitt i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="42edc-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="42edc-108">En to celle i tabellen angir et tomt felt, og en X angir en verdi som er lik verdien i abonnementet der transaksjonen genereres fra.</span><span class="sxs-lookup"><span data-stu-id="42edc-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="42edc-109">Prioritet </span><span class="sxs-lookup"><span data-stu-id="42edc-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="42edc-110"><strong>Kategori</strong></span><span class="sxs-lookup"><span data-stu-id="42edc-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="42edc-111"><strong>Prosjekt-ID</strong></span><span class="sxs-lookup"><span data-stu-id="42edc-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="42edc-112"><strong>Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="42edc-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="42edc-113"><strong>Salgsvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="42edc-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="42edc-114"><strong>Periodekode</strong></span><span class="sxs-lookup"><span data-stu-id="42edc-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42edc-115">1</span><span class="sxs-lookup"><span data-stu-id="42edc-115">1</span></span></p></td>
<td><p><span data-ttu-id="42edc-116">X</span><span class="sxs-lookup"><span data-stu-id="42edc-116">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-117">X</span><span class="sxs-lookup"><span data-stu-id="42edc-117">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-118">X</span><span class="sxs-lookup"><span data-stu-id="42edc-118">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-119">X</span><span class="sxs-lookup"><span data-stu-id="42edc-119">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-120">X</span><span class="sxs-lookup"><span data-stu-id="42edc-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42edc-121">2</span><span class="sxs-lookup"><span data-stu-id="42edc-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42edc-122">X</span><span class="sxs-lookup"><span data-stu-id="42edc-122">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-123">X</span><span class="sxs-lookup"><span data-stu-id="42edc-123">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-124">X</span><span class="sxs-lookup"><span data-stu-id="42edc-124">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-125">X</span><span class="sxs-lookup"><span data-stu-id="42edc-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42edc-126">3</span><span class="sxs-lookup"><span data-stu-id="42edc-126">3</span></span></p></td>
<td><p><span data-ttu-id="42edc-127">X</span><span class="sxs-lookup"><span data-stu-id="42edc-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42edc-128">X</span><span class="sxs-lookup"><span data-stu-id="42edc-128">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-129">X</span><span class="sxs-lookup"><span data-stu-id="42edc-129">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-130">X</span><span class="sxs-lookup"><span data-stu-id="42edc-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42edc-131">4</span><span class="sxs-lookup"><span data-stu-id="42edc-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42edc-132">X</span><span class="sxs-lookup"><span data-stu-id="42edc-132">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-133">X</span><span class="sxs-lookup"><span data-stu-id="42edc-133">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-134">X</span><span class="sxs-lookup"><span data-stu-id="42edc-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42edc-135">5</span><span class="sxs-lookup"><span data-stu-id="42edc-135">5</span></span></p></td>
<td><p><span data-ttu-id="42edc-136">X</span><span class="sxs-lookup"><span data-stu-id="42edc-136">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-137">X</span><span class="sxs-lookup"><span data-stu-id="42edc-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42edc-138">X</span><span class="sxs-lookup"><span data-stu-id="42edc-138">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-139">X</span><span class="sxs-lookup"><span data-stu-id="42edc-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42edc-140">6</span><span class="sxs-lookup"><span data-stu-id="42edc-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42edc-141">X</span><span class="sxs-lookup"><span data-stu-id="42edc-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42edc-142">X</span><span class="sxs-lookup"><span data-stu-id="42edc-142">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-143">X</span><span class="sxs-lookup"><span data-stu-id="42edc-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42edc-144">7</span><span class="sxs-lookup"><span data-stu-id="42edc-144">7</span></span></p></td>
<td><p><span data-ttu-id="42edc-145">X</span><span class="sxs-lookup"><span data-stu-id="42edc-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42edc-146">X</span><span class="sxs-lookup"><span data-stu-id="42edc-146">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-147">X</span><span class="sxs-lookup"><span data-stu-id="42edc-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42edc-148">8</span><span class="sxs-lookup"><span data-stu-id="42edc-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42edc-149">X</span><span class="sxs-lookup"><span data-stu-id="42edc-149">X</span></span></p></td>
<td><p><span data-ttu-id="42edc-150">X</span><span class="sxs-lookup"><span data-stu-id="42edc-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42edc-151">Når det opprettes en abonnementsavgift, velges salgsprisen med det største detaljnivået, som angitt i tabellen ovenfor, som salgsprisen for abonnement.</span><span class="sxs-lookup"><span data-stu-id="42edc-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="42edc-152">Oppdatere og indeksere salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="42edc-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="42edc-153">Du kan oppdatere salgsprisen for abonnement ved å oppdatere basisprisen eller indeksen.</span><span class="sxs-lookup"><span data-stu-id="42edc-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="42edc-154">Du kan oppdatere med en prosentverdi eller til en ny verdi.</span><span class="sxs-lookup"><span data-stu-id="42edc-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="42edc-155">Salgspriser for abonnementsavgift</span><span class="sxs-lookup"><span data-stu-id="42edc-155">Subscription fee sales prices</span></span>

<span data-ttu-id="42edc-156">Når du oppretter en abonnementsavgift, er salgsprisen basert på salgsprisoppsettet for abonnementet.</span><span class="sxs-lookup"><span data-stu-id="42edc-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="42edc-157">Du kan enten bruke basisprisen fra abonnementets prisoppsett eller opprette indekserte salgspriser.</span><span class="sxs-lookup"><span data-stu-id="42edc-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="42edc-158">Eksempel</span><span class="sxs-lookup"><span data-stu-id="42edc-158">Example</span></span>

<span data-ttu-id="42edc-159">Du vil definere salgspriser for abonnement på EUR 500 for det nye prosjektet 9030.</span><span class="sxs-lookup"><span data-stu-id="42edc-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="42edc-160">I skjemaet **Salgspris (abonnement)** oppretter du en salgsprislinje for abonnement som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="42edc-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="42edc-161">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="42edc-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="42edc-162">Kategori</span><span class="sxs-lookup"><span data-stu-id="42edc-162">Category</span></span></p></th>
<th><p><span data-ttu-id="42edc-163">Project</span><span class="sxs-lookup"><span data-stu-id="42edc-163">Project</span></span></p></th>
<th><p><span data-ttu-id="42edc-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="42edc-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="42edc-165">Periodekode</span><span class="sxs-lookup"><span data-stu-id="42edc-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="42edc-166">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="42edc-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="42edc-167">Salgspris</span><span class="sxs-lookup"><span data-stu-id="42edc-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42edc-168">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="42edc-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="42edc-169">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="42edc-170">Måned</span><span class="sxs-lookup"><span data-stu-id="42edc-170">Month</span></span></p></td>
<td><p><span data-ttu-id="42edc-171">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-172">500</span><span class="sxs-lookup"><span data-stu-id="42edc-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42edc-173">Legg merke til at feltene **Kategori** og **Abonnement** er tomme.</span><span class="sxs-lookup"><span data-stu-id="42edc-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="42edc-174">Deretter oppretter du følgende abonnementer:</span><span class="sxs-lookup"><span data-stu-id="42edc-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="42edc-175">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="42edc-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="42edc-176">Project</span><span class="sxs-lookup"><span data-stu-id="42edc-176">Project</span></span></p></th>
<th><p><span data-ttu-id="42edc-177">Abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="42edc-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="42edc-178">Kategori</span><span class="sxs-lookup"><span data-stu-id="42edc-178">Category</span></span></p></th>
<th><p><span data-ttu-id="42edc-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="42edc-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="42edc-180">Periodekode</span><span class="sxs-lookup"><span data-stu-id="42edc-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42edc-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="42edc-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="42edc-182">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-182">9030</span></span></p></td>
<td><p><span data-ttu-id="42edc-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="42edc-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="42edc-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="42edc-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="42edc-185">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-186">Månedlig</span><span class="sxs-lookup"><span data-stu-id="42edc-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42edc-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="42edc-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="42edc-188">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-188">9030</span></span></p></td>
<td><p><span data-ttu-id="42edc-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="42edc-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="42edc-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="42edc-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="42edc-191">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-192">Månedlig</span><span class="sxs-lookup"><span data-stu-id="42edc-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42edc-193">Nå oppretter du abonnementsavgifter for begge abonnementer i abonnementsgruppen Sub1:</span><span class="sxs-lookup"><span data-stu-id="42edc-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="42edc-194">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="42edc-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="42edc-195">I skjemaet **Abonnementsgrupper** klikker du **Funksjon** \> **Opprett abonnementsavgift**.</span><span class="sxs-lookup"><span data-stu-id="42edc-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="42edc-196">Angi aktuell informasjon i skjemaet **Opprett abonnementsavgift**.</span><span class="sxs-lookup"><span data-stu-id="42edc-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="42edc-197">Hvis du vil ha mer informasjon, kan du se [Opprette abonnementsgebyrtransaksjoner](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="42edc-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="42edc-198">Abonnementsavgifter med en salgspris på EUR 500 opprettes for begge abonnementer, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="42edc-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="42edc-199">Prosjektdato</span><span class="sxs-lookup"><span data-stu-id="42edc-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="42edc-200">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="42edc-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="42edc-201">Project</span><span class="sxs-lookup"><span data-stu-id="42edc-201">Project</span></span></p></th>
<th><p><span data-ttu-id="42edc-202">Kategori</span><span class="sxs-lookup"><span data-stu-id="42edc-202">Category</span></span></p></th>
<th><p><span data-ttu-id="42edc-203">Startdato</span><span class="sxs-lookup"><span data-stu-id="42edc-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="42edc-204">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="42edc-204">End date</span></span></p></th>
<th><p><span data-ttu-id="42edc-205">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="42edc-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="42edc-206">Salgspris</span><span class="sxs-lookup"><span data-stu-id="42edc-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42edc-207">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="42edc-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="42edc-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="42edc-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="42edc-209">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-209">9030</span></span></p></td>
<td><p><span data-ttu-id="42edc-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="42edc-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="42edc-211">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="42edc-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="42edc-212">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="42edc-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="42edc-213">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-214">500</span><span class="sxs-lookup"><span data-stu-id="42edc-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42edc-215">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="42edc-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="42edc-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="42edc-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="42edc-217">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-217">9030</span></span></p></td>
<td><p><span data-ttu-id="42edc-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="42edc-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="42edc-219">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="42edc-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="42edc-220">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="42edc-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="42edc-221">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-222">500</span><span class="sxs-lookup"><span data-stu-id="42edc-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42edc-223">Senere bestemmer du deg for at du vil angi salgspriser for kategorien SubCat1 for prosjekt 9030.</span><span class="sxs-lookup"><span data-stu-id="42edc-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="42edc-224">Derfor oppretter du en ny salgsprislinje som har en salgspris på EUR 550 for kombinasjonen av prosjekt 9030 og gebyrkategorien SubCat1.</span><span class="sxs-lookup"><span data-stu-id="42edc-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="42edc-225">Det finnes nå to salgsprislinjer for abonnement for prosjekt 9030, som vist i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="42edc-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="42edc-226">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="42edc-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="42edc-227">Kategori</span><span class="sxs-lookup"><span data-stu-id="42edc-227">Category</span></span></p></th>
<th><p><span data-ttu-id="42edc-228">Project</span><span class="sxs-lookup"><span data-stu-id="42edc-228">Project</span></span></p></th>
<th><p><span data-ttu-id="42edc-229">Abonnement</span><span class="sxs-lookup"><span data-stu-id="42edc-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="42edc-230">Periodekode</span><span class="sxs-lookup"><span data-stu-id="42edc-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="42edc-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="42edc-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="42edc-232">Salgspris</span><span class="sxs-lookup"><span data-stu-id="42edc-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42edc-233">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="42edc-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="42edc-234">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="42edc-235">Måned</span><span class="sxs-lookup"><span data-stu-id="42edc-235">Month</span></span></p></td>
<td><p><span data-ttu-id="42edc-236">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-237">500</span><span class="sxs-lookup"><span data-stu-id="42edc-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42edc-238">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="42edc-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="42edc-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="42edc-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="42edc-240">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="42edc-241">Måned</span><span class="sxs-lookup"><span data-stu-id="42edc-241">Month</span></span></p></td>
<td><p><span data-ttu-id="42edc-242">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-243">550</span><span class="sxs-lookup"><span data-stu-id="42edc-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42edc-244">Du gjentar fremgangsmåten som er beskrevet ovenfor for å opprette abonnementsavgifter for begge abonnementer i abonnementsgruppen Sub1.</span><span class="sxs-lookup"><span data-stu-id="42edc-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="42edc-245">Tabellen nedenfor viser transaksjonene som opprettes for hvert abonnement som er knyttet til abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="42edc-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="42edc-246">Prosjektdato</span><span class="sxs-lookup"><span data-stu-id="42edc-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="42edc-247">Abonnement</span><span class="sxs-lookup"><span data-stu-id="42edc-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="42edc-248">Project</span><span class="sxs-lookup"><span data-stu-id="42edc-248">Project</span></span></p></th>
<th><p><span data-ttu-id="42edc-249">Kategori</span><span class="sxs-lookup"><span data-stu-id="42edc-249">Category</span></span></p></th>
<th><p><span data-ttu-id="42edc-250">Startdato</span><span class="sxs-lookup"><span data-stu-id="42edc-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="42edc-251">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="42edc-251">End date</span></span></p></th>
<th><p><span data-ttu-id="42edc-252">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="42edc-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="42edc-253">Salgspris</span><span class="sxs-lookup"><span data-stu-id="42edc-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42edc-254">28.07.2007</span><span class="sxs-lookup"><span data-stu-id="42edc-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="42edc-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="42edc-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="42edc-256">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-256">9030</span></span></p></td>
<td><p><span data-ttu-id="42edc-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="42edc-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="42edc-258">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="42edc-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="42edc-259">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="42edc-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="42edc-260">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-261">550</span><span class="sxs-lookup"><span data-stu-id="42edc-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42edc-262">28.07.2008</span><span class="sxs-lookup"><span data-stu-id="42edc-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="42edc-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="42edc-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="42edc-264">9030</span><span class="sxs-lookup"><span data-stu-id="42edc-264">9030</span></span></p></td>
<td><p><span data-ttu-id="42edc-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="42edc-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="42edc-266">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="42edc-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="42edc-267">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="42edc-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="42edc-268">EUR</span><span class="sxs-lookup"><span data-stu-id="42edc-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="42edc-269">500</span><span class="sxs-lookup"><span data-stu-id="42edc-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="42edc-270">I den første transaksjonen for abonnement 00020\_135 er salgsprisen på EUR 550 avledet fra salgsprisen for abonnement som er definert for kombinasjonen av det bestemte prosjektet og kategorien.</span><span class="sxs-lookup"><span data-stu-id="42edc-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="42edc-271">I den andre transaksjonen for abonnement 00021\_135 brukes salgsprisen på EUR 500 som salgsprisen for prosjektabonnement, fordi det ikke er definert en pris for kombinasjonen av prosjekt 9030 og kategori SubCat2.</span><span class="sxs-lookup"><span data-stu-id="42edc-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="42edc-272">Se også</span><span class="sxs-lookup"><span data-stu-id="42edc-272">See also</span></span>

[<span data-ttu-id="42edc-273">Oppdatere og indeksere salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="42edc-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  



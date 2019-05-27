---
title: Salgspriser for abonnement
description: Når du oppretter et abonnement, avledes salgsprisen fra salgsprisoppsettet som ble opprettet i skjemaet Salgspris (abonnement).
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560695"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="d3e5b-103">Salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="d3e5b-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d3e5b-104">Når du oppretter et abonnement, avledes salgsprisen fra salgsprisoppsettet som ble opprettet i skjemaet **Salgspris (abonnement)**.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="d3e5b-105">I skjemaet **Salgspris (abonnement)** kan du opprette salgspriser for et bestemt abonnement, eller du kan opprette salgspriser som er mer generelle.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="d3e5b-106">Før en salgspris kan brukes på et abonnement, må periodekoden og valutaen for abonnementet være identisk med periodekoden og valutaen for salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="d3e5b-107">Hvis periodekoden og valutaen er identiske for abonnementet og salgsprisen, velges salgspriser for abonnement på grunnlag av prioritetene som er angitt i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="d3e5b-108">En to celle i tabellen angir et tomt felt, og en X angir en verdi som er lik verdien i abonnementet der transaksjonen genereres fra.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="d3e5b-109">Prioritet </span><span class="sxs-lookup"><span data-stu-id="d3e5b-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-110"><strong>Kategori</strong></span><span class="sxs-lookup"><span data-stu-id="d3e5b-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="d3e5b-111"><strong>Prosjekt-ID</strong></span><span class="sxs-lookup"><span data-stu-id="d3e5b-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="d3e5b-112"><strong>Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="d3e5b-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="d3e5b-113"><strong>Salgsvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="d3e5b-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="d3e5b-114"><strong>Periodekode</strong></span><span class="sxs-lookup"><span data-stu-id="d3e5b-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-115">1</span><span class="sxs-lookup"><span data-stu-id="d3e5b-115">1</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-116">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-116">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-117">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-117">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-118">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-118">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-119">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-119">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-120">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3e5b-121">2</span><span class="sxs-lookup"><span data-stu-id="d3e5b-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d3e5b-122">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-122">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-123">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-123">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-124">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-124">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-125">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-126">3</span><span class="sxs-lookup"><span data-stu-id="d3e5b-126">3</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-127">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d3e5b-128">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-128">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-129">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-129">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-130">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3e5b-131">4</span><span class="sxs-lookup"><span data-stu-id="d3e5b-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d3e5b-132">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-132">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-133">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-133">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-134">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-135">5</span><span class="sxs-lookup"><span data-stu-id="d3e5b-135">5</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-136">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-136">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-137">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d3e5b-138">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-138">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-139">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3e5b-140">6</span><span class="sxs-lookup"><span data-stu-id="d3e5b-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d3e5b-141">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d3e5b-142">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-142">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-143">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-144">7</span><span class="sxs-lookup"><span data-stu-id="d3e5b-144">7</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-145">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d3e5b-146">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-146">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-147">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3e5b-148">8</span><span class="sxs-lookup"><span data-stu-id="d3e5b-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d3e5b-149">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-149">X</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-150">X</span><span class="sxs-lookup"><span data-stu-id="d3e5b-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d3e5b-151">Når det opprettes en abonnementsavgift, velges salgsprisen med det største detaljnivået, som angitt i tabellen ovenfor, som salgsprisen for abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="d3e5b-152">Oppdatere og indeksere salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="d3e5b-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="d3e5b-153">Du kan oppdatere salgsprisen for abonnement ved å oppdatere basisprisen eller indeksen.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="d3e5b-154">Du kan oppdatere med en prosentverdi eller til en ny verdi.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="d3e5b-155">Salgspriser for abonnementsavgift</span><span class="sxs-lookup"><span data-stu-id="d3e5b-155">Subscription fee sales prices</span></span>

<span data-ttu-id="d3e5b-156">Når du oppretter en abonnementsavgift, er salgsprisen basert på salgsprisoppsettet for abonnementet.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="d3e5b-157">Du kan enten bruke basisprisen fra abonnementets prisoppsett eller opprette indekserte salgspriser.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="d3e5b-158">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d3e5b-158">Example</span></span>

<span data-ttu-id="d3e5b-159">Du vil definere salgspriser for abonnement på EUR 500 for det nye prosjektet 9030.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="d3e5b-160">I skjemaet **Salgspris (abonnement)** oppretter du en salgsprislinje for abonnement som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="d3e5b-161">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="d3e5b-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-162">Kategori</span><span class="sxs-lookup"><span data-stu-id="d3e5b-162">Category</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-163">Project</span><span class="sxs-lookup"><span data-stu-id="d3e5b-163">Project</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="d3e5b-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-165">Periodekode</span><span class="sxs-lookup"><span data-stu-id="d3e5b-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-166">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="d3e5b-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-167">Salgspris</span><span class="sxs-lookup"><span data-stu-id="d3e5b-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-168">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="d3e5b-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d3e5b-169">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d3e5b-170">Måned</span><span class="sxs-lookup"><span data-stu-id="d3e5b-170">Month</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-171">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-172">500</span><span class="sxs-lookup"><span data-stu-id="d3e5b-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d3e5b-173">Legg merke til at feltene **Kategori** og **Abonnement** er tomme.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="d3e5b-174">Deretter oppretter du følgende abonnementer:</span><span class="sxs-lookup"><span data-stu-id="d3e5b-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="d3e5b-175">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="d3e5b-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-176">Project</span><span class="sxs-lookup"><span data-stu-id="d3e5b-176">Project</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-177">Abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="d3e5b-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-178">Kategori</span><span class="sxs-lookup"><span data-stu-id="d3e5b-178">Category</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="d3e5b-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-180">Periodekode</span><span class="sxs-lookup"><span data-stu-id="d3e5b-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="d3e5b-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-182">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-182">9030</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="d3e5b-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d3e5b-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-185">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-186">Månedlig</span><span class="sxs-lookup"><span data-stu-id="d3e5b-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3e5b-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="d3e5b-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-188">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-188">9030</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="d3e5b-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d3e5b-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-191">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-192">Månedlig</span><span class="sxs-lookup"><span data-stu-id="d3e5b-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d3e5b-193">Nå oppretter du abonnementsavgifter for begge abonnementer i abonnementsgruppen Sub1:</span><span class="sxs-lookup"><span data-stu-id="d3e5b-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="d3e5b-194">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="d3e5b-195">I skjemaet **Abonnementsgrupper** klikker du **Funksjon** \> **Opprett abonnementsavgift**.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="d3e5b-196">Angi aktuell informasjon i skjemaet **Opprett abonnementsavgift**.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="d3e5b-197">Hvis du vil ha mer informasjon, kan du se [Opprette abonnementsgebyrtransaksjoner](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="d3e5b-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="d3e5b-198">Abonnementsavgifter med en salgspris på EUR 500 opprettes for begge abonnementer, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="d3e5b-199">Prosjektdato</span><span class="sxs-lookup"><span data-stu-id="d3e5b-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-200">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="d3e5b-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-201">Project</span><span class="sxs-lookup"><span data-stu-id="d3e5b-201">Project</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-202">Kategori</span><span class="sxs-lookup"><span data-stu-id="d3e5b-202">Category</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-203">Startdato</span><span class="sxs-lookup"><span data-stu-id="d3e5b-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-204">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="d3e5b-204">End date</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-205">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="d3e5b-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-206">Salgspris</span><span class="sxs-lookup"><span data-stu-id="d3e5b-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-207">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="d3e5b-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="d3e5b-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-209">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-209">9030</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d3e5b-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-211">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="d3e5b-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-212">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="d3e5b-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-213">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-214">500</span><span class="sxs-lookup"><span data-stu-id="d3e5b-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3e5b-215">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="d3e5b-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="d3e5b-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-217">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-217">9030</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d3e5b-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-219">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="d3e5b-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-220">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="d3e5b-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-221">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-222">500</span><span class="sxs-lookup"><span data-stu-id="d3e5b-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d3e5b-223">Senere bestemmer du deg for at du vil angi salgspriser for kategorien SubCat1 for prosjekt 9030.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="d3e5b-224">Derfor oppretter du en ny salgsprislinje som har en salgspris på EUR 550 for kombinasjonen av prosjekt 9030 og gebyrkategorien SubCat1.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="d3e5b-225">Det finnes nå to salgsprislinjer for abonnement for prosjekt 9030, som vist i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="d3e5b-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="d3e5b-226">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="d3e5b-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-227">Kategori</span><span class="sxs-lookup"><span data-stu-id="d3e5b-227">Category</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-228">Project</span><span class="sxs-lookup"><span data-stu-id="d3e5b-228">Project</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-229">Abonnement</span><span class="sxs-lookup"><span data-stu-id="d3e5b-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-230">Periodekode</span><span class="sxs-lookup"><span data-stu-id="d3e5b-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="d3e5b-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-232">Salgspris</span><span class="sxs-lookup"><span data-stu-id="d3e5b-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-233">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="d3e5b-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d3e5b-234">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d3e5b-235">Måned</span><span class="sxs-lookup"><span data-stu-id="d3e5b-235">Month</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-236">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-237">500</span><span class="sxs-lookup"><span data-stu-id="d3e5b-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3e5b-238">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="d3e5b-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d3e5b-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-240">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d3e5b-241">Måned</span><span class="sxs-lookup"><span data-stu-id="d3e5b-241">Month</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-242">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-243">550</span><span class="sxs-lookup"><span data-stu-id="d3e5b-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d3e5b-244">Du gjentar fremgangsmåten som er beskrevet ovenfor for å opprette abonnementsavgifter for begge abonnementer i abonnementsgruppen Sub1.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="d3e5b-245">Tabellen nedenfor viser transaksjonene som opprettes for hvert abonnement som er knyttet til abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="d3e5b-246">Prosjektdato</span><span class="sxs-lookup"><span data-stu-id="d3e5b-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-247">Abonnement</span><span class="sxs-lookup"><span data-stu-id="d3e5b-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-248">Project</span><span class="sxs-lookup"><span data-stu-id="d3e5b-248">Project</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-249">Kategori</span><span class="sxs-lookup"><span data-stu-id="d3e5b-249">Category</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-250">Startdato</span><span class="sxs-lookup"><span data-stu-id="d3e5b-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-251">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="d3e5b-251">End date</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-252">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="d3e5b-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d3e5b-253">Salgspris</span><span class="sxs-lookup"><span data-stu-id="d3e5b-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3e5b-254">28.07.2007</span><span class="sxs-lookup"><span data-stu-id="d3e5b-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="d3e5b-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-256">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-256">9030</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d3e5b-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-258">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="d3e5b-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-259">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="d3e5b-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-260">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-261">550</span><span class="sxs-lookup"><span data-stu-id="d3e5b-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3e5b-262">28.07.2008</span><span class="sxs-lookup"><span data-stu-id="d3e5b-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="d3e5b-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-264">9030</span><span class="sxs-lookup"><span data-stu-id="d3e5b-264">9030</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="d3e5b-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-266">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="d3e5b-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-267">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="d3e5b-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-268">EUR</span><span class="sxs-lookup"><span data-stu-id="d3e5b-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="d3e5b-269">500</span><span class="sxs-lookup"><span data-stu-id="d3e5b-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d3e5b-270">I den første transaksjonen for abonnement 00020\_135 er salgsprisen på EUR 550 avledet fra salgsprisen for abonnement som er definert for kombinasjonen av det bestemte prosjektet og kategorien.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="d3e5b-271">I den andre transaksjonen for abonnement 00021\_135 brukes salgsprisen på EUR 500 som salgsprisen for prosjektabonnement, fordi det ikke er definert en pris for kombinasjonen av prosjekt 9030 og kategori SubCat2.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3e5b-272">Se også</span><span class="sxs-lookup"><span data-stu-id="d3e5b-272">See also</span></span>

[<span data-ttu-id="d3e5b-273">Oppdatere og indeksere salgspriser for abonnement</span><span class="sxs-lookup"><span data-stu-id="d3e5b-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  



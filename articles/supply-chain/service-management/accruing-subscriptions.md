---
title: Avsetning av abonnementer
description: Med serviceabonnementer kan du manuelt avsette omsetning i periodene etter datoen da du fakturerte en gebyrtransaksjon.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a183e17749c04b407eb17155ecb1363e96ade18a
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="accruing-subscriptions"></a><span data-ttu-id="2c3d3-103">Avsetning av abonnementer</span><span class="sxs-lookup"><span data-stu-id="2c3d3-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2c3d3-104">Med serviceabonnementer kan du manuelt avsette omsetning i periodene etter datoen da du fakturerte en gebyrtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="2c3d3-105">Det opprettes avsetningsperioder for fakturaperioden du har definert for abonnementsgebyret, og avsetningsperiodene er basert på periodekoden for abonnementet.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="2c3d3-106">Du kan avsette og tilbakeføre påløpt omsetning.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="2c3d3-107">Tilbakefør avsetninger av kreditbeløp</span><span class="sxs-lookup"><span data-stu-id="2c3d3-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="2c3d3-108">Hvis du krediterer fakturerte abonnementsbeløp, kan du bruke to metoder for å tilbakeføre de påløpte beløpene:</span><span class="sxs-lookup"><span data-stu-id="2c3d3-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="2c3d3-109">Du kan tilbakeføre hvert påløpte inntektstransaksjon enkeltvis før du oppretter et kreditnotaforslag for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="2c3d3-110">Dette er den manuelle metoden.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-110">This is the manual method.</span></span> <span data-ttu-id="2c3d3-111">(manuell)</span><span class="sxs-lookup"><span data-stu-id="2c3d3-111">(manual)</span></span>

  - <span data-ttu-id="2c3d3-112">Du kan få de påløpte beløpene tilbakeført på datoen når kreditnotaen posteres eller på den opprinnelige posteringsdatoen for avsetningen.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="2c3d3-113">Hvis du vil ha mer informasjon, kan du se [Abonnementsparametere (skjema)](https://technet.microsoft.com/en-us/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="2c3d3-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/en-us/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="2c3d3-114">Installasjonskrav</span><span class="sxs-lookup"><span data-stu-id="2c3d3-114">Setup requirements</span></span>

<span data-ttu-id="2c3d3-115">Hvis du vil avsette omsetning, må du sørge for at følgende datakravene oppfylles:</span><span class="sxs-lookup"><span data-stu-id="2c3d3-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="2c3d3-116">Kontooppsett</span><span class="sxs-lookup"><span data-stu-id="2c3d3-116">Account setup</span></span>

<span data-ttu-id="2c3d3-117">Kontoene **VIA – abonnement** og **Påløpt inntekt – abonnement** må være konfigurert i **Prosjekt**-modulen.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="2c3d3-118">Når du posterer påløpt omsetning, debiteres kontoen **VIA – abonnement** med det påløpte beløpet, og kontoen **Påløpt inntekt – abonnement** krediteres med det påløpte beløpet.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="2c3d3-119">Definere kontoer for avsetning av abonnementsomsetning</span><span class="sxs-lookup"><span data-stu-id="2c3d3-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="2c3d3-120">Klikk på **Prosjektstyring og regnskap** \> **Oppsett** \> **Postering** \> **Finansposteringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="2c3d3-121">Klikk på fanen **Inntektskontoer**, og velg **VIA – abonnement** eller **Påløpt inntekt – abonnement** for å konfigurere kontoene.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="2c3d3-122">Oppsett for abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="2c3d3-122">Subscription group setup</span></span>

<span data-ttu-id="2c3d3-123">For å kunne avsette inntekt for abonnementer må det være merket av for **Avsett inntekt**.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="2c3d3-124">Dette finnes i skjemaet **Abonnementsgrupper** for gruppen som er knyttet til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="2c3d3-125">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="2c3d3-126">Aktivere omsetningsavsetning på en abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="2c3d3-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="2c3d3-127">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="2c3d3-128">Perioder</span><span class="sxs-lookup"><span data-stu-id="2c3d3-128">Periods</span></span>

<span data-ttu-id="2c3d3-129">Du må definere en periodekode for fakturering.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="2c3d3-130">Med mindre du vil avsette omsetning i de samme tidsintervallene du bruker for fakturering, må du også definere en avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="2c3d3-131">I følgende tabell får du en oversikt over hvilke avsetningsperioder du kan definere for hver faktureringsperiode:</span><span class="sxs-lookup"><span data-stu-id="2c3d3-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c3d3-132">Faktureringstermin</span><span class="sxs-lookup"><span data-stu-id="2c3d3-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="2c3d3-133">Avsetningsperiode</span><span class="sxs-lookup"><span data-stu-id="2c3d3-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c3d3-134"><strong>År</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2c3d3-135"><strong>År</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="2c3d3-136"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="2c3d3-137"><strong>Måned</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="2c3d3-138"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c3d3-139"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2c3d3-140"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="2c3d3-141"><strong>Måned</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="2c3d3-142"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c3d3-143"><strong>Måned</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2c3d3-144"><strong>Måned</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="2c3d3-145"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c3d3-146"><strong>Uke</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2c3d3-147"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c3d3-148"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="2c3d3-149"><strong>Dag</strong></span><span class="sxs-lookup"><span data-stu-id="2c3d3-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2c3d3-150">Definering av faktureringsperioden er en obligatorisk del av det totale oppsettet for abonnementsgrupper.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="2c3d3-151">Du kan bestemme om du vil også definere en avsetningsperiode for abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="2c3d3-152">Hvis du definerer en avsetningsperiode for abonnementsgruppen, foreslås denne perioden i **Periodekode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="2c3d3-153">Dette feltet finnes i skjemaet **Avsett abonnementsomsetning** når du avsetter abonnementsomsetning.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="2c3d3-154">Avsetningsperioden er imidlertid valgfri informasjon om abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2c3d3-155">Bruk følgende bane til å åpne skjemaet <STRONG>Avsett abonnementsomsetning</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="2c3d3-156">Klikk på <STRONG>Servicestyring</STRONG> &gt; <STRONG>Periodisk</STRONG> &gt; <STRONG>Serviceabonnementer</STRONG> &gt; <STRONG>Avsett abonnementsomsetning</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="2c3d3-157">Transaksjoner</span><span class="sxs-lookup"><span data-stu-id="2c3d3-157">Transactions</span></span>

<span data-ttu-id="2c3d3-158">Du kan styre antallet finanstransaksjoner som opprettes når du posterer påløpt inntekt.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="2c3d3-159">For abonnementer kan du definere om finanstransaksjoner skal opprettes som en total eller per linje.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="2c3d3-160">Angi nivået av posteringsdetaljer som skal vises for avsatte transaksjoner</span><span class="sxs-lookup"><span data-stu-id="2c3d3-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="2c3d3-161">Klikk på **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="2c3d3-162">På fanen **Økonomisk** i **Faktura**-feltet velger du **Total** eller **Linje**.</span><span class="sxs-lookup"><span data-stu-id="2c3d3-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="2c3d3-163">Se også</span><span class="sxs-lookup"><span data-stu-id="2c3d3-163">See also</span></span>

[<span data-ttu-id="2c3d3-164">Avsett abonnementsomsetning</span><span class="sxs-lookup"><span data-stu-id="2c3d3-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  




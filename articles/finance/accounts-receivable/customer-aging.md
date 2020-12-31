---
title: Aldersfordelt saldoliste for kunder
description: Rapport for aldersfordeling for kunde for kunder viser saldoene som forfaller fra kunder, sortert etter dato intervall eller periode for aldersfordelings.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/15/2020
ms.locfileid: "4446563"
---
# <a name="customer-aging-report"></a><span data-ttu-id="0c193-103">Aldersfordelt saldoliste for kunder</span><span class="sxs-lookup"><span data-stu-id="0c193-103">Customer aging report</span></span> 

<span data-ttu-id="0c193-104">**Rapport for aldersfordeling for kunde** viser saldoene som forfaller fra kunder, sortert etter dato intervall eller periode for aldersfordelings.</span><span class="sxs-lookup"><span data-stu-id="0c193-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="0c193-105">Når du genererer denne rapporten, vises standardparametrene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="0c193-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="0c193-106">Du kan bruke disse parametrene til å filtrere dataene som skal vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c193-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="0c193-107">Hvis du vil ha mer informasjon, kan du se [Definere innkreving](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="0c193-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c193-108">Felt</span><span class="sxs-lookup"><span data-stu-id="0c193-108">Field</span></span></p></th>
<th><p><span data-ttu-id="0c193-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0c193-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c193-110"><strong>Faktureringsklassifisering</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-111">Velg én eller flere faktureringsklassifiseringer som skal tas med i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c193-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="0c193-112">**Obs!** Denne kontrollen er bare tilgjengelig hvis konfigurasjonsnøkkelen for <STRONG>offentlig sektor</STRONG> er valgt.</span><span class="sxs-lookup"><span data-stu-id="0c193-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c193-113"><strong>Inkluder transaksjoner uten faktureringsklassifisering</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-114">Hvis det er merket av for dette, vises alle transaksjoner som ikke er tilordnet en faktureringsklassifisering, i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c193-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="0c193-115">**Obs!** Denne kontrollen er bare tilgjengelig hvis konfigurasjonsnøkkelen for <STRONG>offentlig sektor</STRONG> er valgt.</span><span class="sxs-lookup"><span data-stu-id="0c193-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c193-116"><strong>Aldersfordeling per</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-117">Angi datoen som brukes i gjeldende aldersfordelingen.</span><span class="sxs-lookup"><span data-stu-id="0c193-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c193-118"><strong>Saldo per</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-119">Skriv inn en dato du vil vise kundesaldo for.</span><span class="sxs-lookup"><span data-stu-id="0c193-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="0c193-120">Dette kalles også en frist for transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0c193-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c193-121"><strong>Startdato</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-122">Angi datoen som er i første periodeintervall eller aldersfordelingsperiode som skal tas med i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c193-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c193-123"><strong>Vilkår</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-124">Velg datotypen som rapporten skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="0c193-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="0c193-125"><strong>Transaksjonsdato</strong> – Posteringsdatoen for de valgte transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="0c193-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="0c193-126">Dette kan for eksempel være en fakturadato som er grunnlaget for beregningen av forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="0c193-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="0c193-127"><strong>Forfallsdato</strong> – Forfallsdatoen til transaksjonene basert på betalingsbetingelsene.</span><span class="sxs-lookup"><span data-stu-id="0c193-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="0c193-128"><strong>Dokumentdato</strong> – En brukerdefinert dokumentdato som er grunnlaget for beregning av forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="0c193-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c193-129"><strong>Definisjon av aldersfordelingsperiode</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-130">Velg en definisjon av aldersfordelingsperiode.</span><span class="sxs-lookup"><span data-stu-id="0c193-130">Select an aging period definition.</span></span> <span data-ttu-id="0c193-131"><strong>Intervall</strong>-feltet brukes ikke hvis du velger en definisjon av aldersfordelingsperiode.</span><span class="sxs-lookup"><span data-stu-id="0c193-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="0c193-132">Definisjoner for aldersfordelingsperiode som har mer enn seks aldersfordelingsperioder, kan ikke brukes på den utskrevne rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c193-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="0c193-133">**Obs!** Du kan definere aldersfordelingsperioder på siden <STRONG>Definisjoner av aldersfordelingsperiode</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0c193-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c193-134"><strong>Skriv ut beskrivelse for aldersfordelingsperiode</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-135">Velg <strong>Ja</strong> for å inkludere beskrivelser av aldersfordelingsperiode øverst på hver kolonne for aldersfordelingsperiode i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c193-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="0c193-136">Velg <strong>Nei</strong> for å skrive ut rapporten uten kolonneoverskrifter.</span><span class="sxs-lookup"><span data-stu-id="0c193-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c193-137"><strong>Intervall</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-138">Definer perioden som skal brukes, ved å angi nummeret på dagen eller månedsenheter i hver periode.</span><span class="sxs-lookup"><span data-stu-id="0c193-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="0c193-139">Hvis du for eksempel vil vise aldersfordelingsinformasjon etter uke, angir du 7 i dette feltet og velger <strong>Dag</strong> i <strong>Dag/mnd</strong>-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c193-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="0c193-140">**Obs!** Informasjonen du har angitt i dette feltet, brukes bare hvis du ikke har valgt en definisjon av aldersfordelingsperiode.</span><span class="sxs-lookup"><span data-stu-id="0c193-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="0c193-141">Hvis ikke defineres utskriftsretningen på definisjon av aldersfordelingsperiode.</span><span class="sxs-lookup"><span data-stu-id="0c193-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c193-142"><strong>Dag/mnd</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-143">Velg enheten, enten <strong>Dag</strong> eller <strong>Måned</strong>, som brukes til å definere perioden i <strong>Intervall</strong>-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c193-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c193-144"><strong>Utskriftsretning</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-145">Velg om du skal beregne saldoer og skrive ut rapport for aldersfordeling for tidligere eller fremtidige perioder.</span><span class="sxs-lookup"><span data-stu-id="0c193-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="0c193-146">Datoene evalueres i forhold til datoen som er valgt i <strong>Saldo per</strong>-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c193-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="0c193-147">Velg <strong>Bakover</strong> for å vise informasjon for tidligere perioder.</span><span class="sxs-lookup"><span data-stu-id="0c193-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="0c193-148">Velg <strong>Forover</strong> for å vise informasjon for fremtidige perioder.</span><span class="sxs-lookup"><span data-stu-id="0c193-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="0c193-149">
  
<STRONG>Obs!</STRONG> Informasjonen du har angitt i dette feltet, brukes bare hvis du ikke har valgt en definisjon av aldersfordelingsperiode.</span><span class="sxs-lookup"><span data-stu-id="0c193-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c193-150"><strong>Detaljer</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-151">Velg å vise en liste over transaksjoner som er inkludert i saldoene som vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c193-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c193-152"><strong>Inkluder beløp i transaksjonsvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-153">Velg for å ta med beløp i transaksjonsvalutaen i tillegg til beløp i regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="0c193-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="0c193-154">Hvis det ikke er merket av i denne boksen, vises beløpene i rapporten bare i regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="0c193-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c193-155"><strong>Negativ saldo</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-156">Velg dette for å ta med kundekontoer med negative saldoer.</span><span class="sxs-lookup"><span data-stu-id="0c193-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c193-157"><strong>Ekskluder null saldo-kontoer</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-158">Velg dette for å utelate kundekontoer med null i saldo.</span><span class="sxs-lookup"><span data-stu-id="0c193-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c193-159"><strong>Betalingsposisjonering</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="0c193-160">Velg for å vise betalinger som ikke er utlignet.</span><span class="sxs-lookup"><span data-stu-id="0c193-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="0c193-161">Disse vises i den første kolonnen i rapporten.</span><span class="sxs-lookup"><span data-stu-id="0c193-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>


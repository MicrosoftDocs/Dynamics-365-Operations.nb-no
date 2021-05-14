---
title: Avgift beregnes ikke eller avgiftsbeløpet er null
description: Dette emnet gir feilsøkingsinformasjon som kan hjelpe når avgiftsbeløpet er 0 (null) eller avgift ikke beregnes.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947686"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="0cc58-103">Avgift beregnes ikke eller avgiftsbeløpet er null</span><span class="sxs-lookup"><span data-stu-id="0cc58-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cc58-104">En transaksjon kan ha et linjebeløp som ikke er 0 (null), men enten beregnes ikke avgift eller beregnet avgiftsbeløp er 0.</span><span class="sxs-lookup"><span data-stu-id="0cc58-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="0cc58-105">Hvis du vil feilsøke dette problemet, følger du trinnene i de følgende delene etter behov.</span><span class="sxs-lookup"><span data-stu-id="0cc58-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="0cc58-106">Kontroller at avgiftskoder er riktig valgt av transaksjonen</span><span class="sxs-lookup"><span data-stu-id="0cc58-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="0cc58-107">Hvis transaksjonen ikke velger de riktige avgiftskodene, eller hvis den ikke velger noen avgiftskoder, blir det ikke beregnet avgifter på den.</span><span class="sxs-lookup"><span data-stu-id="0cc58-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="0cc58-108">Følg disse trinnene for å kontrollere at avgiftskoder er riktig valgt av transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc58-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="0cc58-109">I hurtigfanen **Linjedetaljer** i kategorien **Oppsett** i **Merverdiavgift**-delen kontrollerer du at riktig avgiftsgruppe er valgt i feltene **Varens mva-gruppe** og **Merverdiavgiftsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="0cc58-110">Hvis riktig avgiftsgruppe ikke er valgt, velger du dem.</span><span class="sxs-lookup"><span data-stu-id="0cc58-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="0cc58-111">[![Feltene Varens mva-gruppe og Merverdiavgiftsgruppe](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="0cc58-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="0cc58-112">Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-grupper**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="0cc58-113">Velg den aktuelle mva-gruppen, og noter deg avgiftskoden i **Mva-kode**-feltet i the **Oppsett**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="0cc58-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="0cc58-114">[![Siden Mva-grupper](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="0cc58-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="0cc58-115">Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Vare, mva-grupper**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="0cc58-116">Velg den riktige mva-gruppen for vare, og kontroller deretter at mva-koden i **Mva-kode**-feltet samsvarer med mva-koden i mva-gruppen i **Oppsett**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="0cc58-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="0cc58-117">[![Siden Vare, mva-grupper](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="0cc58-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="0cc58-118">Hvis avgiftskodene ikke samsvarer, oppdaterer du mva-koden for én av gruppene.</span><span class="sxs-lookup"><span data-stu-id="0cc58-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="0cc58-119">Kontroller at de valgte avgiftskodene ikke er fritatt, og at de har riktig mva-satsverdi.</span><span class="sxs-lookup"><span data-stu-id="0cc58-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="0cc58-120">Hvis avgiftskodene er fritatt, eller hvis mva-satsen er 0 (null), blir resultatet av avgiftsberegningen 0.</span><span class="sxs-lookup"><span data-stu-id="0cc58-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="0cc58-121">Følg denne fremgangsmåten for å finne ut om de valgte avgiftskodene er fritatt, og kontrollere at riktig mva-sats brukes på dem.</span><span class="sxs-lookup"><span data-stu-id="0cc58-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="0cc58-122">Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-grupper**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="0cc58-123">Velg den riktige mva-gruppen, og kontroller deretter at det ikke er merket av for **Avgiftsfri** i **Oppsett**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="0cc58-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="0cc58-124">Hvis du har merket av for dette feltet, fjerner du merket.</span><span class="sxs-lookup"><span data-stu-id="0cc58-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="0cc58-125">[![Avmerkingsboksen Avgiftsfri på Mva-grupper-siden](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="0cc58-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="0cc58-126">Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="0cc58-127">Velg den riktige mva-koden, og kontroller deretter at mva-satsverdien i **Verdi**-feltet ikke har verdien 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0cc58-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="0cc58-128">Hvis feltet er 0, må du oppdatere feltet slik at det settes til riktig avgiftssats.</span><span class="sxs-lookup"><span data-stu-id="0cc58-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="0cc58-129">[![Verdi-felt på siden Verdier for merverdiavgiftskode](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="0cc58-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="0cc58-130">Bestem om null er riktig mva-beløp</span><span class="sxs-lookup"><span data-stu-id="0cc58-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="0cc58-131">I noen scenarier er et mva-beløp på 0 (null) riktig.</span><span class="sxs-lookup"><span data-stu-id="0cc58-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="0cc58-132">Følg denne fremgangsmåten for å finne ut om 0 er det riktige avgiftsbeløpet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc58-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="0cc58-133">Gå til **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="0cc58-134">Kontroller at **Total** er valgt i **Beregningsmetode**-feltet i kategorien **Merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="0cc58-135">[![Beregningsmetode-felt på siden Parametere for økonomimodul](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="0cc58-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="0cc58-136">Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="0cc58-137">Velg den riktige mva-koden, velg **Beregning** \> **Grensegrunnlag**, og kontroller at grensegrunnlaget er satt til **Nettobeløp på fakturasaldo** eller **Fakturatotal inkl. andre mva-beløp**.</span><span class="sxs-lookup"><span data-stu-id="0cc58-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="0cc58-138">Hvis du vil ha mer informasjon, kan du se [Fakturatotal inkl. andre mva-beløp](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="0cc58-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="0cc58-139">Hvis de riktige verdiene er angitt i trinn 2 og 4, må du bestemme om totalbeløpet for transaksjonen er 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0cc58-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="0cc58-140">Hvis totalbeløpet er 0, er et mva-beløp på 0 det forventede resultatet.</span><span class="sxs-lookup"><span data-stu-id="0cc58-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="0cc58-141">Fordi avgiftsberegningen er basert på det totale beløpet på fakturasaldoen, og dette beløpet ikke er linje etter linje, vil mva-beløpet på 0 bli tilordnet til hver linje etter avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="0cc58-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="0cc58-142">Fastslå om det finnes tilpasning</span><span class="sxs-lookup"><span data-stu-id="0cc58-142">Determine whether customization exists</span></span>

<span data-ttu-id="0cc58-143">Hvis du har fullført trinnene i de forrige delene, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning.</span><span class="sxs-lookup"><span data-stu-id="0cc58-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="0cc58-144">Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.</span><span class="sxs-lookup"><span data-stu-id="0cc58-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

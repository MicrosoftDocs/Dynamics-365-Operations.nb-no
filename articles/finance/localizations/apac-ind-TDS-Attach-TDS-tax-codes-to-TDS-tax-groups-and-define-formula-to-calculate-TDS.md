---
title: Knytte TDS-avgiftskoder til TDS-avgiftsgrupper og definere formelen for beregning av TDS
description: Dette emnet forklarer hvordan du konfigurerer TDS-avgiftsgrupper (Tax Deducted at Source) og knytter TDS-avgiftskoder til TDS-avgiftsgrupper. For å kunne beregne TDS for en TDS-avgiftsgruppe må du definere formelen for TDS-avgiftskoder som er knyttet til den.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023487"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="ca676-104">Knytte TDS-avgiftskoder til TDS-avgiftsgrupper og definere formelen for beregning av TDS</span><span class="sxs-lookup"><span data-stu-id="ca676-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca676-105">Dette emnet forklarer hvordan du konfigurerer TDS-avgiftsgrupper (Tax Deducted at Source) og knytter TDS-avgiftskoder til TDS-avgiftsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ca676-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="ca676-106">For å kunne beregne TDS for en TDS-avgiftsgruppe må du definere formelen for TDS-avgiftskoder som er knyttet til den.</span><span class="sxs-lookup"><span data-stu-id="ca676-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="ca676-107">Følg denne fremgangsmåten for å konfigurere en TDS-avgiftsgruppe, knytte TDS-avgiftskoder til den og definere formelen for beregning av TDS.</span><span class="sxs-lookup"><span data-stu-id="ca676-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="ca676-108">Gå til **Avgift \> Indirekte avgifter \> Kildeskatt \> Kildeskattgrupper**.</span><span class="sxs-lookup"><span data-stu-id="ca676-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="ca676-109">[![Siden Kildeskattgrupper](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="ca676-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="ca676-110">Velg **Ny** i handlingsruten for å opprette en kildeskattgruppe for TDS, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="ca676-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="ca676-111">I feltet **Avgiftstype** velger du **TDS**.</span><span class="sxs-lookup"><span data-stu-id="ca676-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="ca676-112">I hurtigfanen **Oppsett** velger du **Legg til** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="ca676-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="ca676-113">Velg TDS-avgiftskoden for TDS-avgiftsgruppen i feltet **Kildeskattkode**.</span><span class="sxs-lookup"><span data-stu-id="ca676-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="ca676-114">Feltet **Navn på kildeskatt** viser navnet på TDS-avgiftskoden, og **Verdi**-feltet viser verdien.</span><span class="sxs-lookup"><span data-stu-id="ca676-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="ca676-115">Hvis du vil ignorere terskelgrensen og unntaksterskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til TDS-avgiftskoden i TDS-transaksjoner, merker du av for **Overse terskel**.</span><span class="sxs-lookup"><span data-stu-id="ca676-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="ca676-116">Merk av for **Avgiftsfri** hvis du vil unngå at avgiftsgruppen beregnes i transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ca676-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="ca676-117">Velg **Utforming** i handlingsruten for å åpne formeldesigneren, slik at du kan definere formelen for beregning av TDS for TDS-avgiftsgruppen.</span><span class="sxs-lookup"><span data-stu-id="ca676-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="ca676-118">**Avgifter**-fanen på **Utforming**-siden viser TDS-avgiftskodene som er valgt for TDS-avgiftsgruppen.</span><span class="sxs-lookup"><span data-stu-id="ca676-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="ca676-119">[![Utforming-siden](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="ca676-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="ca676-120">Trykk på **ALT+N** i **Beregning**-fanen for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="ca676-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="ca676-121">**ID**-feltet viser den automatisk genererte prioritets-ID-en for TDS-beregningen.</span><span class="sxs-lookup"><span data-stu-id="ca676-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="ca676-122">Velg TDS-avgiftskoden som formelen skal defineres for, i **Avgiftskode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca676-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="ca676-123">Alle TDS-avgiftskodene som er valgt for TDS-avgiftsgruppen, kan velges i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="ca676-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="ca676-124">I feltet **Skattbart grunnlag** velger du grunnlaget for beregning av TDS:</span><span class="sxs-lookup"><span data-stu-id="ca676-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="ca676-125">**Bruttobeløp** – Beregn TDS basert på bruttotransaksjonsbeløpet (det vil si fakturabeløpet) ved hjelp av beregningsuttrykket som er definert for avgiftskoden.</span><span class="sxs-lookup"><span data-stu-id="ca676-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="ca676-126">**Ekskl. bruttobeløp** – Beregn TDS basert på beregningsuttrykket som er definert for avgiftskoden.</span><span class="sxs-lookup"><span data-stu-id="ca676-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca676-127">Feltet **Skattbart grunnlag** kan ikke settes til **Ekskl. bruttobeløp** for TDS-avgiftskoden som har prioritets-ID-en **1**.</span><span class="sxs-lookup"><span data-stu-id="ca676-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="ca676-128">TDS-beregningen er basert på formelen som er definert i feltet **Beregningsuttrykk** for hver avgiftskode som er knyttet til TDS-avgiftsgruppen.</span><span class="sxs-lookup"><span data-stu-id="ca676-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="ca676-129">Velg plusstegnet (**+**), minustegnet (**-**), multiplikasjonstegnet (**\**_) eller divisjonstegnet (_*/**) for å angi beregningsuttrykket for den valgte TDS-avgiftskoden i feltet **Beregningsuttrykk**.</span><span class="sxs-lookup"><span data-stu-id="ca676-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca676-130">Ingen beregningsuttrykk kan defineres for TDS-avgiftskoden som har prioritets-ID-en **1**.</span><span class="sxs-lookup"><span data-stu-id="ca676-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="ca676-131">Hvis du vil definere beregningsuttrykk for TDS-avgiftskoden i feltet **Beregningsuttrykk**, legger du til TDS-avgiftskoder som er tilgjengelige i **Avgifter**-fanen. Hvis du vil legge til TDS-avgiftskoder i feltet **Beregningsuttrykk**, kan du bruke en av følgende metoder:</span><span class="sxs-lookup"><span data-stu-id="ca676-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="ca676-132">Dra den nødvendige avgiftskoden fra **Avgifter**-fanen til feltet **Beregningsuttrykk**.</span><span class="sxs-lookup"><span data-stu-id="ca676-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="ca676-133">Dobbelttrykk (eller dobbeltklikk) på den nødvendige avgiftskoden i **Avgifter**-fanen.</span><span class="sxs-lookup"><span data-stu-id="ca676-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="ca676-134">Velg og hold (eller høyreklikk på) den nødvendige avgiftskoden i **Avgifter**-fanen, og velg deretter **Legg til avgiftskode**.</span><span class="sxs-lookup"><span data-stu-id="ca676-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca676-135">Sett inn et beregningsuttrykk før hver TDS-avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="ca676-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="ca676-136">TDS-avgiftskodene som er lagt til i beregningsuttrykket, vises i hakeparenteser (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="ca676-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="ca676-137">Hvis du vil fjerne beregningsuttrykket som er definert for en avgiftskode i feltet **Beregningsuttrykk**, velger du **C**-knappen.</span><span class="sxs-lookup"><span data-stu-id="ca676-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="ca676-138">Hvis du vil slette en post i **Beregning**-fanen, velger du **Slett**.</span><span class="sxs-lookup"><span data-stu-id="ca676-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="ca676-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca676-139">Close the page.</span></span>

---
title: Beregne TDS for fakturaer ved hjelp av journaler
description: Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for journaler.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023492"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="eb505-103">Beregne TDS for fakturaer ved hjelp av journaler</span><span class="sxs-lookup"><span data-stu-id="eb505-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb505-104">Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for journaler.</span><span class="sxs-lookup"><span data-stu-id="eb505-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="eb505-105">Begynn ved å åpne **Økonomijournaler**-siden (**Økonomimodul > Journaloppføringer > Økonomijournaler**).</span><span class="sxs-lookup"><span data-stu-id="eb505-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="eb505-106">[![Økonomijournaler](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="eb505-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="eb505-107">Opprett journallinjer ved hjelp av journalskjemaene som vises i tabellen.</span><span class="sxs-lookup"><span data-stu-id="eb505-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="eb505-108">Velg kontotypen og motkontotypen, og angi beløpet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="eb505-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="eb505-109">Velg **Finn bilag** på siden **Fakturagodkjenningsjournal**, og velg fakturaer du vil beregne TDS for.</span><span class="sxs-lookup"><span data-stu-id="eb505-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="eb505-110">Vis fakturaene som er opprettet på siden **Ankomstregistrering** eller **Finn bilag**-siden.</span><span class="sxs-lookup"><span data-stu-id="eb505-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="eb505-111">Vis eller endre standard TDS-gruppe som er definert for leverandøren eller kunden, i feltet **TDS-gruppe** i **Oversikt**-fanen på **Journalbilag**-siden.</span><span class="sxs-lookup"><span data-stu-id="eb505-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="eb505-112">TDS-beløpet som beregnes på journallinjer, er basert på formelen som er definert for TDS-avgiftskodene i feltet **TDS-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="eb505-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="eb505-113">Feltene **Kildeskattgruppe** og **TCS-gruppe** blir utilgjengelige når du velger en TDS-gruppe i feltet **TDS-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="eb505-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="eb505-114">Feltet **Kildeskattgruppe** er bare tilgjengelig på siden **Økonomijournal**.</span><span class="sxs-lookup"><span data-stu-id="eb505-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="eb505-115">TDS beregnes bare hvis det er merket av for **Beregn kildeskatt** for leverandøren eller kunden på siden **Alle leverandører** eller **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="eb505-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="eb505-116">Velg fanen **Avgiftsinformasjon**. Velg de alternative adressene til et selskap som er konfigurert for selskapet i dette feltet, hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="eb505-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="eb505-117">Du kan vise selskapsnavnet i **Navn**-feltet, som er i feltgruppen **Selskapsopplysninger**.</span><span class="sxs-lookup"><span data-stu-id="eb505-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="eb505-118">Vis kategorien for skattebetalertype for leverandøren eller kunden i feltet **Skattebetalertype**, som er i feltgruppen **Kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="eb505-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="eb505-119">Vis TAN-nummeret til det valgte selskapsnavnet som vises, i feltet **TAN-nummer** (**Tax Account Number**).</span><span class="sxs-lookup"><span data-stu-id="eb505-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="eb505-120">Velg **Kildeskatt** på **Kildeskatt**-menyen for å åpne siden **Midlertidige kildeskattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="eb505-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="eb505-121">Følgende felter vises i den øvre ruten på siden **Midlertidige kildeskattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="eb505-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="eb505-122">**Kildeskattbeløp totalt** – Det totale TDS-beløpet som ble beregnet for transaksjonen for TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb505-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="eb505-123">**Verdi** – Den totale prosentsatsen som brukes til å beregne TDS for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="eb505-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="eb505-124">Den totale prosentsatsen er basert på formelen som er definert for TDS-avgiftskoder knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb505-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="eb505-125">**Justert kildeskattbeløp totalt** – Det totale justerte TDS-beløpet for alle avgiftskodene i TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb505-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="eb505-126">**TDS** – Hvis dette er valgt, knyttes en TDS-gruppe til transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="eb505-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="eb505-127">Feltene i fanen **Oversikt**, **Generelt** og **Justering** på siden **Midlertidige kildeskattransaksjoner** viser det beregnede TDS-beløpet og de justerte TDS-beløpsdetaljene for hver TDS-avgiftskode som er knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb505-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="eb505-128">Velg **Terskel** for å åpne **Terskel**-siden.</span><span class="sxs-lookup"><span data-stu-id="eb505-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="eb505-129">Vis terskelgrensen og unntaksterskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til en bestemt TDS-avgiftskode på denne siden.</span><span class="sxs-lookup"><span data-stu-id="eb505-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="eb505-130">Velg **Formeldesigner** for å åpne **Formeldesigner**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="eb505-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="eb505-131">Vis formelen som er definert for en bestemt TDS-avgiftskode på denne siden.</span><span class="sxs-lookup"><span data-stu-id="eb505-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="eb505-132">Lukk sidene **Formeldesigner** og **Midlertidige kildeskattransaksjoner** for å gå tilbake til **Journalbilag**-siden.</span><span class="sxs-lookup"><span data-stu-id="eb505-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="eb505-133">Angi de andre nødvendige opplysningene.</span><span class="sxs-lookup"><span data-stu-id="eb505-133">Enter the other required details.</span></span> <span data-ttu-id="eb505-134">Valider og poster journalen.</span><span class="sxs-lookup"><span data-stu-id="eb505-134">Validate and post the journal.</span></span> <span data-ttu-id="eb505-135">TDS-beløpet som er beregnet for innkjøpsfakturaer, posteres på leverandørreskontroen.</span><span class="sxs-lookup"><span data-stu-id="eb505-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="eb505-136">TDS-beløpet som beregnes for salgsfakturaer, posteres på kundereskontroen som er definert for hver TDS-avgiftskode i TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb505-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="eb505-137">Leverandørreskontroene eller kundereskontroene for TDS-avgiftskoder defineres på siden **Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="eb505-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="eb505-138">Velg **Postert kildeskatt** for å åpne siden **Kildeskattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="eb505-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="eb505-139">I **Verdi**-feltet vises den totale prosentsatsen som brukes til å beregne TDS for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="eb505-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="eb505-140">Feltene i fanene **Oversikt**, **Generelt** og **Beløp** på siden Kildeskattransaksjoner viser det beregnede TDS-beløpet og de justerte TDS-beløpsdetaljene for hver TDS-avgiftskode som er knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb505-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

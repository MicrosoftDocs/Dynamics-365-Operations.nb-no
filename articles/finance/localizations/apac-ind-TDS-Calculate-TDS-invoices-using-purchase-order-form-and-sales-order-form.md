---
title: Beregne TDS-fakturaer ved hjelp av bestillingsskjema og salgsordreskjema
description: Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for ulike fakturatyper.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023468"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="0c090-103">Beregne TDS-fakturaer ved hjelp av bestillingsskjema og salgsordreskjema</span><span class="sxs-lookup"><span data-stu-id="0c090-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c090-104">Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for ulike fakturatyper ved hjelp av sidene **Bestilling**, **Innkjøpsjournal**, **Rammebestilling** og **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="0c090-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="0c090-105">Opprett en bestilling, innkjøpsjournal, rammebestilling eller salgsordre ved hjelp av siden som vises.</span><span class="sxs-lookup"><span data-stu-id="0c090-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="0c090-106">Angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="0c090-106">Enter the required details.</span></span>

2. <span data-ttu-id="0c090-107">Velg **Oppsett**-fanen for å vise skattebetalertypen for leverandøren eller kunden.</span><span class="sxs-lookup"><span data-stu-id="0c090-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="0c090-108">Denne informasjonen vises i feltet **Skattebetalertype** i feltgruppen **Kildeskattgruppe**.</span><span class="sxs-lookup"><span data-stu-id="0c090-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="0c090-109">Vis eller endre standard TDS-gruppe som er definert for leverandøren eller kunden, i feltet **TDS-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="0c090-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0c090-110">Feltet **TCS-gruppe** er ikke tilgjengelig når du velger en TDS-gruppe i feltet **TDS-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="0c090-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="0c090-111">TDS beregnes bare hvis det er merket av for **Beregn kildeskatt** for leverandøren eller kunden på siden **Alle leverandører** eller **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="0c090-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="0c090-112">Opprett varelinjer i **Linjer**-fanen, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="0c090-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="0c090-113">Velg **Oppsett**-fanen (linjenivå) for å vise eller endre TDS-gruppen som er definert på hodenivået.</span><span class="sxs-lookup"><span data-stu-id="0c090-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="0c090-114">TDS-gruppen vises i feltet **TDS-gruppe**, som er i feltgruppen **Kildeskattgruppe**.</span><span class="sxs-lookup"><span data-stu-id="0c090-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="0c090-115">Velg fanen **Avgiftsinformasjon**, og velg alternative adresser som er konfigurert for selskapsnavnet som vises i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="0c090-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="0c090-116">Selskapsnavnet vises i **Navn**-feltet, som er i feltgruppen **Selskapsopplysninger**.</span><span class="sxs-lookup"><span data-stu-id="0c090-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="0c090-117">TAN-nummeret for det valgte selskapsnavnet vises i feltet **TAN-nummer** (**Tax Account Number**) i feltgruppen **Kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="0c090-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="0c090-118">Velg **Kildeskatt** for å åpne siden **Midlertidige kildeskattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="0c090-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="0c090-119">Vis følgende felter i den øvre ruten på siden **Midlertidige kildeskattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="0c090-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="0c090-120">**Kildeskattbeløp** **totalt** – Det totale TDS-beløpet som ble beregnet for transaksjonen for TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="0c090-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="0c090-121">**Verdi** – Den totale prosentsatsen som brukes til å beregne TDS for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0c090-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="0c090-122">Den totale prosentsatsen er basert på formelen som er definert for TDS-avgiftskoder knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="0c090-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="0c090-123">**Justert kildeskattbeløp totalt** – Det totale justerte TDS-beløpet for alle avgiftskodene i TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="0c090-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="0c090-124">**TDS** – Hvis dette er valgt, knyttes en TDS-gruppe til transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0c090-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="0c090-125">Feltene i fanen **Oversikt**, **Generelt** og **Justering** på siden **Midlertidige kildeskattransaksjoner** viser det beregnede TDS-beløpet og de justerte TDS-beløpsdetaljene for hver TDS-avgiftskode som er knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="0c090-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="0c090-126">Velg **Terskel** for å åpne **Terskel**-siden.</span><span class="sxs-lookup"><span data-stu-id="0c090-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="0c090-127">Vis terskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til en bestemt TDS-avgiftskode på denne siden.</span><span class="sxs-lookup"><span data-stu-id="0c090-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="0c090-128">Velg **Formeldesigner** for å åpne **Formeldesigner**-siden.</span><span class="sxs-lookup"><span data-stu-id="0c090-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="0c090-129">Vis formelen som er definert for en bestemt TDS-avgiftskode på denne siden.</span><span class="sxs-lookup"><span data-stu-id="0c090-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="0c090-130">Poster fakturaen.</span><span class="sxs-lookup"><span data-stu-id="0c090-130">Post the invoice.</span></span> <span data-ttu-id="0c090-131">TDS-beløpet som beregnes for innkjøpsfakturaer, posteres på leverandørreskontroen, og TDS-beløpet som beregnes for salgsfakturaer, posteres på kundereskontroen som er definert for hver TDS-avgiftskode i TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="0c090-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="0c090-132">Leverandørreskontroene eller kundereskontroene for TDS-avgiftskoder defineres på siden **Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="0c090-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="0c090-133">Velg **Forespørsel**-knappen **> Faktura > Postert kildeskatt**-knappen for å åpne siden **Kildeskattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="0c090-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="0c090-134">Du kan vise den totale prosentsatsen som brukes til å beregne TDS for transaksjonen, i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c090-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="0c090-135">Feltene i fanene **Oversikt**, **Generelt** og **Beløp** på siden **Kildeskattransaksjoner** viser informasjon om TDS som er beregnet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0c090-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="0c090-136">Vis TDS-beregningsinformasjonen for hver TDS-avgiftskode knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="0c090-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>

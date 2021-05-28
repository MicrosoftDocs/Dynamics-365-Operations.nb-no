---
title: TDS-beregning for fakturaer fra siden Fritekstfaktura
description: Dette emnet forklarer hvordan du beregner TDS (Tax Deducted at Source) for fakturaer ved hjelp av siden Fritekstfaktura.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023484"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="cfeb5-103">TDS-beregning for fakturaer fra siden Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="cfeb5-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfeb5-104">Dette emnet forklarer hvordan du beregner TDS (Tax Deducted at Source) for fakturaer ved hjelp av siden **Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="cfeb5-105">Gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="cfeb5-106">[![Siden Fritekstfaktura](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="cfeb5-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="cfeb5-107">Velg **Ny** for å opprette en fritekstfaktura, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="cfeb5-108">Velg **Faktura**-fanen. Feltet **Skattebetalertype** i delen **Kildeskattgruppe** viser kategorien for skattebetalertype for leverandøren eller kunden.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="cfeb5-109">Gå gjennom eller endre standard TDS-gruppe som er definert for kunden, i feltet **TDS-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cfeb5-110">Når du velger en verdi i feltet **TDS-gruppe**, blir feltet **TCS-gruppe** utilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="cfeb5-111">TDS beregnes bare hvis alternativet **Beregn kildeskatt** er satt til **Ja** for kunden på siden **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="cfeb5-112">Velg selskapsnavnet for en alternativ adresse som er konfigurert for selskapet, i **Navn**-feltet i delen **Selskapsopplysninger** i fanen **Avgiftsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="cfeb5-113">Feltet **TAN-nummer (Tax Account Number)** i **Kildeskatt**-delen viser TAN-nummeret for det valgte selskapet.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="cfeb5-114">Opprett fakturalinjer i **Fakturalinjer**-fanen, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="cfeb5-115">Feltet **TAN-nummer (Tax Account Number)** i delen **Kildeskattgruppe** viser TAN-nummeret, og feltet **TDS-gruppe** viser TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="cfeb5-116">Velg **Kildeskatt** for å åpne siden **Midlertidige kildeskattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="cfeb5-117">Den øvre delen av denne siden inneholder følgende felter:</span><span class="sxs-lookup"><span data-stu-id="cfeb5-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="cfeb5-118">**Kildeskattbeløp totalt** – Det totale TDS-beløpet som ble beregnet for transaksjonen for TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="cfeb5-119">**Verdi** – Den totale prosentsatsen som ble brukt til å beregne TDS for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="cfeb5-120">Den totale prosentsatsen er basert på formelen som er definert for TDS-avgiftskodene og er knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="cfeb5-121">**Justert kildeskattbeløp totalt** – Det totale justerte TDS-beløpet for alle avgiftskodene i TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="cfeb5-122">**TDS** – En avmerket avmerkingsboks angir at en TDS-gruppe er knyttet til transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="cfeb5-123">Feltene i fanen **Oversikt**, **Generelt** og **Justering** viser det beregnede TDS-beløpet og detaljene for det justerte TDS-beløpet for hver TDS-avgiftskode som er knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="cfeb5-124">Velg **Terskel** for å åpne **Terskel**-siden, der du kan gå gjennom terskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til en bestemt TDS-avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="cfeb5-125">Velg **Formeldesigner** for å åpne **Formeldesigner**-siden, der du kan gå gjennom formelen som er definert for en bestemt TDS-avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="cfeb5-126">Poster fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-126">Post the free text invoice.</span></span> <span data-ttu-id="cfeb5-127">TDS-beløpet som beregnes for fritekstfakturaen, posteres på kundereskontroen som er definert for hver TDS-avgiftskode i TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="cfeb5-128">Kundereskontroene for TDS-avgiftskoder defineres på siden **Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="cfeb5-129">Velg **Postert kildeskatt** for å åpne siden **Kildeskattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="cfeb5-130">**Verdi**-feltet viser den totale prosentsatsen som ble brukt til å beregne TDS for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="cfeb5-131">Feltene i fanene **Oversikt**, **Generelt** og **Beløp** viser TDS-beløpene som ble beregnet på fakturalinjene.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="cfeb5-132">Gå gjennom TDS-beregningsinformasjonen for hver TDS-avgiftskode som er knyttet til TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfeb5-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>

---
title: Definere kildeskattkoder for TDS-avgiftstypen
description: Dette emnet forklarer hvordan du konfigurerer avgiftskoder for TDS-funksjonen (Tax Deducted at Source).
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023490"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="e5239-103">Definere kildeskattkoder for TDS-avgiftstypen</span><span class="sxs-lookup"><span data-stu-id="e5239-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5239-104">Dette emnet forklarer hvordan du konfigurerer avgiftskoder for TDS-funksjonen (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="e5239-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="e5239-105">Gå til **Avgift \> > Indirekte avgifter \> > Kildeskatt \> > Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="e5239-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="e5239-106">[![Siden Kildeskattkoder](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="e5239-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="e5239-107">Velg **Ny** i handlingsruten for å opprette en kildeskattkode for TDS, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="e5239-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="e5239-108">Velg **TDS** i **Mva-type**-feltet i kategorien **Generelt** for å kategorisere avgiftskoden som en TDS-avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="e5239-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="e5239-109">I feltet **Utligningsperiode** velger du TDS-utligningsperioden for TDS-avgiftskoden.</span><span class="sxs-lookup"><span data-stu-id="e5239-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="e5239-110">I feltet **Hovedkonto** velger du finanskontoen som TDS-beløpet skal posteres til.</span><span class="sxs-lookup"><span data-stu-id="e5239-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="e5239-111">I feltet for **kundekonto** velger du kundekontoen som TDS-beløpet som er trukket fra i salgstransaksjoner, skal posteres til.</span><span class="sxs-lookup"><span data-stu-id="e5239-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="e5239-112">Feltet **Opprinnelse** settes automatisk til **Prosent av bruttobeløp**, og verdien kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="e5239-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e5239-113">Du kan ikke angi opprinnelsen til **Prosent av nettobeløp** for avgiftskoder av TDS-avgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="e5239-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="e5239-114">I feltet **Komponenter for kildeskatt** velger du TDS-komponentgruppen for TDS-kildekode.</span><span class="sxs-lookup"><span data-stu-id="e5239-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="e5239-115">Velg **Verdier** i handlingsruten for å åpne siden **Withholding tax-verdier**.</span><span class="sxs-lookup"><span data-stu-id="e5239-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="e5239-116">I **Fra dato**-feltet angir du startdatoen for TDS-verdien.</span><span class="sxs-lookup"><span data-stu-id="e5239-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="e5239-117">I **Til dato**-feltet angir du sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="e5239-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e5239-118">Feltene **Minimumsgrense**, **Øvre grense** og **Ekskluder %** er ikke tilgjengelige for avgiftskoder av TDS-avgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="e5239-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="e5239-119">Angi prosenten for TDS for TDS-avgiftskoden i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e5239-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="e5239-120">Lukk siden **Kildeskattverdier** for å gå tilbake til siden **Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="e5239-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e5239-121">**Grenser**-knappen på siden **Kildeskattkoder** er ikke tilgjengelig for avgiftskoder av TDS-avgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="e5239-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="e5239-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e5239-122">Close the page.</span></span>

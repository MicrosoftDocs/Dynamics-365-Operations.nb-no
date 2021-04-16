---
title: Fjerne et anleggsmiddel som svinn
description: Emnet beskriver prosessen med å eliminere transaksjoner for et anleggsmiddel som er fjernet som svinn.
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 413847d350ca6b2bdd6153a598ea5b3f34a33818
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826281"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="99e2e-103">Fjerne et anleggsmiddel som svinn</span><span class="sxs-lookup"><span data-stu-id="99e2e-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99e2e-104">Emnet beskriver prosessen med å eliminere transaksjoner for et anleggsmiddel som er fjernet som svinn.</span><span class="sxs-lookup"><span data-stu-id="99e2e-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="99e2e-105">Transaksjonstypene som kan elimineres, omfatter transaksjoner for innkjøpsprisen og den akkumulerte avskrivningen for et aktivum og andre transaksjoner for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="99e2e-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="99e2e-106">Eliminering av disse transaksjonene påvirker balansekontoer, for eksempel kontoer for anskaffelse, justering, avskrivningsjustering, revaluering, oppskrivning og nedskrivning.</span><span class="sxs-lookup"><span data-stu-id="99e2e-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="99e2e-107">Transaksjon</span><span class="sxs-lookup"><span data-stu-id="99e2e-107">Transaction</span></span>                                         | <span data-ttu-id="99e2e-108">Debet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="99e2e-108">Debit (Dr.)</span></span> | <span data-ttu-id="99e2e-109">Kredit (Kred.)</span><span class="sxs-lookup"><span data-stu-id="99e2e-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="99e2e-110">Dr. akkumulert avskrivning</span><span class="sxs-lookup"><span data-stu-id="99e2e-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="99e2e-111">X</span><span class="sxs-lookup"><span data-stu-id="99e2e-111">X</span></span>           |              |
| <span data-ttu-id="99e2e-112">Kred. resultat for anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="99e2e-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="99e2e-113">X</span><span class="sxs-lookup"><span data-stu-id="99e2e-113">X</span></span>            |
| <span data-ttu-id="99e2e-114">Dr. resultat for anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="99e2e-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="99e2e-115">X</span><span class="sxs-lookup"><span data-stu-id="99e2e-115">X</span></span>           |              |
| <span data-ttu-id="99e2e-116">Kred. konto for anskaffelse av anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="99e2e-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="99e2e-117">X</span><span class="sxs-lookup"><span data-stu-id="99e2e-117">X</span></span>            |
| <span data-ttu-id="99e2e-118">Dr. resultat for anleggsmidler (netto bokført verdi \[NBV\])</span><span class="sxs-lookup"><span data-stu-id="99e2e-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="99e2e-119">X</span><span class="sxs-lookup"><span data-stu-id="99e2e-119">X</span></span>           |              |
| <span data-ttu-id="99e2e-120">Kred. resultat for anleggsmiddel (netto bokført verdi)</span><span class="sxs-lookup"><span data-stu-id="99e2e-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="99e2e-121">X</span><span class="sxs-lookup"><span data-stu-id="99e2e-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="99e2e-122">Vi anbefaler at du samarbeider tett med firmaets økonomisjef eller revisor for å identifisere de riktige kontoene som skal brukes for hver transaksjonstype, og også kontrollere at avhendingsprosessen og transaksjonene som genereres, oppdaterer disse kontoene på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="99e2e-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="99e2e-123">Før du avhender et anleggsmiddel som svinn, må du opprette finanskontoer som er knyttet til anleggsmiddelets anskaffelsesverdi, avskrivning for inneværende år, avskrivning for tidligere år og netto bokført verdi for anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="99e2e-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="99e2e-124">Transaksjonstypene for anleggsmiddel vises på siden **Posteringsprofil for anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="99e2e-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="99e2e-125">Gå til **Anleggsmidler \> Oppsett \> Posteringsprofiler for anleggsmidler**, and deretter velger du **Svinn** i feltet over rutenettet i hurtigfanen **Avhending**.</span><span class="sxs-lookup"><span data-stu-id="99e2e-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="99e2e-126">Illustrasjonen nedenfor viser en liste over transaksjonstyper for anleggsmidler på siden **Posteringsprofiler for anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="99e2e-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="99e2e-127">[![Avhende et anleggsmiddel som svinn, fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="99e2e-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="99e2e-128">I eksemplet nedenfor ble et anleggsmiddel anskaffet 1. januar 2018, og det blir kassert 31. mars 2019.</span><span class="sxs-lookup"><span data-stu-id="99e2e-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="99e2e-129">**Anskaffelsespris**: 24 000,00 amerikanske dollar (USD)</span><span class="sxs-lookup"><span data-stu-id="99e2e-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="99e2e-130">**Levetid**: To år</span><span class="sxs-lookup"><span data-stu-id="99e2e-130">**Service life:** Two years</span></span>
- <span data-ttu-id="99e2e-131">**Avskrivningsmetode**: Lineær levetid</span><span class="sxs-lookup"><span data-stu-id="99e2e-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="99e2e-132">**Avskrivningsbeløp**: 1 000,00 amerikanske dollar per måned</span><span class="sxs-lookup"><span data-stu-id="99e2e-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="99e2e-133">Netto bokført verdi for et anleggsmiddel beregnes med følgende formel:</span><span class="sxs-lookup"><span data-stu-id="99e2e-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="99e2e-134">Netto bokført verdi = anskaffelsespris – avskrivning</span><span class="sxs-lookup"><span data-stu-id="99e2e-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="99e2e-135">I dette eksemplet ble anleggsmiddelet anskaffet og avskrevet i 15 måneder, fra januar 2018 til mars 2019.</span><span class="sxs-lookup"><span data-stu-id="99e2e-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="99e2e-136">Derfor er netto bokført verdi for anleggsmiddelet 9 000,00 USD (24 000,00 USD – 15 000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="99e2e-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="99e2e-137">[![Eksempel på avskrivning av anleggsmiddel](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="99e2e-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="99e2e-138">Hvis du vil opprette en avhendingsjournal, går du til **Anleggsmidler \> Journaloppføringer \> Anleggsmiddeljournal** og velger **Linjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="99e2e-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="99e2e-139">Velg **Avhending – svinn**, og velg deretter en ID for anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="99e2e-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="99e2e-140">Hvis du ikke avhende anleggsmiddelet fullstendig, angir du ikke en verdi i **Debet**- eller **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="99e2e-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="99e2e-141">[![Anleggsmiddeljournal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="99e2e-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="99e2e-142">Svinntransaksjonen for avhending av anleggsmidler endrer feltverdiene for anleggsmiddeltablået på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="99e2e-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="99e2e-143">I **Saldo**-delen oppdateres **Status**-feltet til **Kassert**.</span><span class="sxs-lookup"><span data-stu-id="99e2e-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="99e2e-144">I **Avgang**-delen blir feltet **Avhendingsdato** satt til datoen da anleggsmiddelet ble kassert.</span><span class="sxs-lookup"><span data-stu-id="99e2e-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="99e2e-145">[![Detaljer i anleggsmiddeljournal](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="99e2e-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="99e2e-146">Illustrasjonen nedenfor viser anleggsmiddelsaldoen.</span><span class="sxs-lookup"><span data-stu-id="99e2e-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="99e2e-147">[![Anleggsmiddelsaldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="99e2e-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="99e2e-148">Illustrasjonen nedenfor viser bilaget som er postert.</span><span class="sxs-lookup"><span data-stu-id="99e2e-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="99e2e-149">[![Netto bokført verdi](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="99e2e-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
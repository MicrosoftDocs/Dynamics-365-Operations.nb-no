---
title: Kildeskatt i kjøpstransaksjoner
description: For leverandører med kildeskatt, kan du tilordne standard **Kildeskattgruppe** på siden **Alle leverandører**.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: faeaf0746532875d3517a208c9c338c112bf2c77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816889"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="592b2-103">Kildeskatt i kjøpstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="592b2-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="592b2-104">For leverandører med kildeskatt, kan du tilordne standard **Kildeskattgruppe** på siden **Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="592b2-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="592b2-105">Gå til **Navigasjonsruten > Moduler > Leverandører > Leverandører > Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="592b2-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="592b2-106">Klikk den aktuelle leverandørkontoen, og klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="592b2-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="592b2-107">I kategorien **Faktura og levering** setter du feltet **Beregn kildeskatt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="592b2-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="592b2-108">Kildeskatt beregnes ikke hvis **Beregn kildeskatt** ikke er aktivert for denne leverandøren i dataene.</span><span class="sxs-lookup"><span data-stu-id="592b2-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="592b2-109">Velg en kildeskattgruppe i **Kildeskattgruppe**.</span><span class="sxs-lookup"><span data-stu-id="592b2-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="592b2-110">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="592b2-110">Click **Save**.</span></span>

<span data-ttu-id="592b2-111">For varer/tjenester som er pålagt kildeskatt, kan du tilordne standard **Kildeskattegrupper for vare** i **Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="592b2-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="592b2-112">Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="592b2-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="592b2-113">Klikk det aktuelle varenummeret, og klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="592b2-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="592b2-114">I kategorien **Kjøp** klikker du **Beregn kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="592b2-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="592b2-115">Kildeskatt beregnes ikke hvis **Beregn kildeskatt** ikke er satt til **Ja** for denne varen i kategorien **Kjøp** på siden **Frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="592b2-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="592b2-116">Velg en kildeskattgruppe i listen **Kildeskattegrupper for vare**.</span><span class="sxs-lookup"><span data-stu-id="592b2-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="592b2-117">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="592b2-117">Click **Save**.</span></span>

<span data-ttu-id="592b2-118">Kildeskattgrupper og kildeskattgrupper for vare kan tilordnes på sidene:</span><span class="sxs-lookup"><span data-stu-id="592b2-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="592b2-119">**Bestilling**</span><span class="sxs-lookup"><span data-stu-id="592b2-119">**Purchase order**</span></span>
- <span data-ttu-id="592b2-120">**Leverandørfaktura**</span><span class="sxs-lookup"><span data-stu-id="592b2-120">**Vendor invoice**</span></span>
- <span data-ttu-id="592b2-121">**Fakturajournal**</span><span class="sxs-lookup"><span data-stu-id="592b2-121">**Invoice journal**</span></span>

<span data-ttu-id="592b2-122">Standard kildeskattgruppe og kildeskattgrupper for vare føres inn på linjene ved oppretting av **Bestillinger** og/eller **Ventende leverandørfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="592b2-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="592b2-123">For **Fakturajournal leverandør** kan du aktivere **Beregn kildeskatt** og velge **Kildeskattegrupper for vare** i kategorien **Generelt** i journalen.</span><span class="sxs-lookup"><span data-stu-id="592b2-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="592b2-124">Det midlertidige beløpet for kildeskatt er tilgjengelig i feltet **Justert kildeskatt** i kategorien **Totaler** på siden **Bestilling**.</span><span class="sxs-lookup"><span data-stu-id="592b2-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Kildeskatt er inkludert i bestillingen](media/withholding-tax-adjusted.png)

<span data-ttu-id="592b2-126">Kildeskatt beregnes på **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="592b2-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="592b2-127">Du kan justere gjeldende kildeskattkoder manuelt og de faktiske kildeskattbeløpene i kategorien **Kildeskatt** på siden **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="592b2-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Kildeskatt kan justeres manuelt på siden Utlign transaksjoner](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="592b2-129">Det avledede kildeskattbeløpet blir trukket fra leverandørbetalingen og postert til **Kildeskattkonto** i et tilknyttet bilag.</span><span class="sxs-lookup"><span data-stu-id="592b2-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Kildeskattkonto som viser et tilknyttet bilag](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
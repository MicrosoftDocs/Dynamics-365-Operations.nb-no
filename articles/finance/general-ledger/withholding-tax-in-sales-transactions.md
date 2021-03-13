---
title: Kildeskatt i salgstransaksjoner
description: Dette emnet viser en liste over trinnene for å unngå beregning av kildeskatt for valgte kunder. For kunder som angir kildeskatt i betalingene sine, kan du tilordne standard kildeskattgruppe.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060776"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="f7d5f-104">Kildeskatt i salgstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="f7d5f-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="f7d5f-105">Dette emnet viser en liste over trinnene for å unngå beregning av kildeskatt for valgte kunder.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="f7d5f-106">For kunder som angir kildeskatt i betalingene sine, kan du tilordne standard **Kildeskattgruppe** på siden **Kunder**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="f7d5f-107">Gå til **Navigasjonsrute > Moduler > Kunder > Kunder > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="f7d5f-108">Klikk den aktuelle kundekontoen, og klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="f7d5f-109">I kategorien **Faktura og levering** setter du feltet **Beregn kildeskatt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f7d5f-110">Kildeskatt beregnes ikke hvis **Beregn kildeskatt** ikke er aktivert for denne kunden i hoveddataene.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="f7d5f-111">Velg en kildeskattgruppe i **Kildeskattgruppe**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="f7d5f-112">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-112">Click **Save**.</span></span>

<span data-ttu-id="f7d5f-113">For varer/tjenester som er pålagt kildeskatt, kan du tilordne standard **Kildeskattegrupper for vare** i **Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="f7d5f-114">Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="f7d5f-115">Klikk det aktuelle varenummeret, og klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="f7d5f-116">I kategorien **Salg** klikker du **Beregn kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f7d5f-117">Kildeskatt beregnes ikke hvis **Beregn kildeskatt** ikke er satt til **Ja** for denne varen i kategorien **Salg** på siden **Frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="f7d5f-118">Velg en kildeskattgruppe i listen **Kildeskattegrupper for vare**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="f7d5f-119">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-119">Click **Save**.</span></span>

<span data-ttu-id="f7d5f-120">Kildeskattgrupper og kildeskattegrupper for vare kan tilordnes ved hjelp siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="f7d5f-121">Standard kildeskattgruppe og kildeskattgruppe for varer blir brukt som standardoppføringer på salgsordrelinjer når du oppretter en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="f7d5f-122">Kildeskatt beregnes og posteres med **Kundebetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="f7d5f-123">Du kan justere den gjeldende kildeskattkoden manuelt og det faktiske kildeskattbeløpet i kategorien **Kildeskatt** på siden **Utlign transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="f7d5f-124">Det beregnede kildeskattbeløpet blir trukket fra kundebetalingen og postert til **Kildeskattmotkonto** i et tilknyttet bilag.</span><span class="sxs-lookup"><span data-stu-id="f7d5f-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>

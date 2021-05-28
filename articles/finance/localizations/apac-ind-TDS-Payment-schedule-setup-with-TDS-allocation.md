---
title: Konfigurere betalingsplaner med TDS-tildeling
description: Dette emnet forklarer hvordan du konfigurerer betalingsplaner med TDS-tildeling (Tax Deducted at Source).
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023486"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="8bc41-103">Konfigurere betalingsplaner med TDS-tildeling</span><span class="sxs-lookup"><span data-stu-id="8bc41-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bc41-104">Dette emnet forklarer hvordan du konfigurerer betalingsplaner med TDS-tildeling (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="8bc41-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="8bc41-105">Gå til **Leverandører \> Betalingsoppsett \> Betalingsplaner**.</span><span class="sxs-lookup"><span data-stu-id="8bc41-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="8bc41-106">[![Siden Betalingsplaner](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="8bc41-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="8bc41-107">Velg **Ny** i handlingsruten for å opprette en betalingsplan, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="8bc41-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="8bc41-108">Velg metoden du vil bruke til å tildele betalingen for betalingsplanen, i **Tildeling**-feltet:</span><span class="sxs-lookup"><span data-stu-id="8bc41-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="8bc41-109">Totalsum</span><span class="sxs-lookup"><span data-stu-id="8bc41-109">Total</span></span>
    - <span data-ttu-id="8bc41-110">Fast beløp</span><span class="sxs-lookup"><span data-stu-id="8bc41-110">Fixed amount</span></span>
    - <span data-ttu-id="8bc41-111">Fast antall</span><span class="sxs-lookup"><span data-stu-id="8bc41-111">Fixed quantity</span></span>
    - <span data-ttu-id="8bc41-112">Angitt</span><span class="sxs-lookup"><span data-stu-id="8bc41-112">Specified</span></span>

    <span data-ttu-id="8bc41-113">Feltet **Tildeling av kildeskatt** viser TDS-tildelingsmetoden for betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="8bc41-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="8bc41-114">Hvis du velger **Totalsum** i **Tildeling**-feltet, settes feltet **Tildeling av kildeskatt** automatisk til **Totalsum**.</span><span class="sxs-lookup"><span data-stu-id="8bc41-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="8bc41-115">Hvis du velger **Fast beløp**, **Fast antall** eller **Angitt** i **Tildeling**-feltet, settes feltet **Tildeling av kildeskatt** automatisk til **Proporsjonalt**.</span><span class="sxs-lookup"><span data-stu-id="8bc41-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8bc41-116">Hvis feltet **Tildeling av kildeskatt** er satt til **Totalsum**, beregnes betalingsavdragene basert på bruttobeløpet, som omfatter TDS-beløpet.</span><span class="sxs-lookup"><span data-stu-id="8bc41-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="8bc41-117">Hvis feltet **Tildeling av kildeskatt** er satt til **Proporsjonalt**, beregnes betalingsavdragene basert på netto fakturabeløp etter at TDS-beløpet er trukket fra.</span><span class="sxs-lookup"><span data-stu-id="8bc41-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="8bc41-118">Angi de andre nødvendige detaljene, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="8bc41-118">Enter the other required details, and then close the page.</span></span>

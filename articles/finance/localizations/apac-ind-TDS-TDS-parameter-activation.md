---
title: Angi TDS-parameterne
description: Dette emnet forklarer hvordan du angir parametere for å aktivere TDS-funksjonaliteten (Tax Deducted at Source) i bestemte transaksjoner. Dette er et nødvendig trinn for å bruke TDS-funksjonen (Tax Deducted at Source).
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023476"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="e30e6-104">Angi TDS-parameterne</span><span class="sxs-lookup"><span data-stu-id="e30e6-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e30e6-105">Dette emnet forklarer hvordan du angir parametere for å aktivere TDS-funksjonaliteten (Tax Deducted at Source) i bestemte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="e30e6-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="e30e6-106">Dette er et nødvendig trinn for å bruke TDS-funksjonen (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="e30e6-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="e30e6-107">Gå til **Økonomimodul \> Finansoppsett \> Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="e30e6-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="e30e6-108">Sett alternativet **Aktiver TDS** til **Ja** i delen **TDS (Tax Deducted at Source)** i fanen **Direkte avgifter** for å aktivere TDS-funksjonaliteten og sidene og feltene som brukes for det.</span><span class="sxs-lookup"><span data-stu-id="e30e6-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="e30e6-109">Sett alternativet **Faktura** til **Ja** for å aktivere feltene som brukes til å beregne og trekke fra TDS på fakturanivå.</span><span class="sxs-lookup"><span data-stu-id="e30e6-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="e30e6-110">Sett alternativet **Betaling** til **Ja** for å aktivere feltene som brukes til å beregne og trekke fra TDS på betalingsnivået.</span><span class="sxs-lookup"><span data-stu-id="e30e6-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="e30e6-111">[![Fanen Direkte avgifter](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="e30e6-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="e30e6-112">Finn raden der **Referanse**-feltet er satt til **Kildeskattbetaling** i fanen **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="e30e6-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="e30e6-113">Velg nummerseriekoden i feltet **Nummerseriekode** for raden.</span><span class="sxs-lookup"><span data-stu-id="e30e6-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="e30e6-114">Nummerseriekoden brukes til å generere bilagsnumre for den periodiske TDS-utligningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="e30e6-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e30e6-115">Hvis du vil kjøre den periodiske TDS-utligningsprosessen, går du til **Avgift \> Deklareringer \> Kildeskatt \> Kildeskattbetaling**.</span><span class="sxs-lookup"><span data-stu-id="e30e6-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="e30e6-116">[![Fanen Nummerserier](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="e30e6-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="e30e6-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e30e6-117">Close the page.</span></span>

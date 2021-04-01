---
title: Opprette en mva-betaling
description: Jobbprosedyren Utlign og poster merverdiavgift utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9523ef75953bdca36f509f596c51c08b12b3fdb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254469"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="34d05-103">Opprette en mva-betaling</span><span class="sxs-lookup"><span data-stu-id="34d05-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34d05-104">Jobbprosedyren Utlign og poster merverdiavgift utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.</span><span class="sxs-lookup"><span data-stu-id="34d05-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="34d05-105">Gå til **Avgift > Deklareringer > Merverdiavgift > Utlign og poster merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="34d05-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="34d05-106">Klikk på rullegardinknappen i **Utligningsperiode**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="34d05-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="34d05-107">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="34d05-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="34d05-108">Angi en dato i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="34d05-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="34d05-109">Hvis du ikke velger alternativet **Ta med rettelser** på siden **Parametere for økonomimodul**, kan utligningen behandles for forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="34d05-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="34d05-110">Original er den første utligningen for et periodeintervall og kan bare behandles én gang for et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="34d05-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="34d05-111">De nyeste rettelsene utligner mva-transaksjoner som er postert etter at den opprinnelige versjonen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="34d05-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="34d05-112">Angi en dato i feltet **Transaksjonsdato**.</span><span class="sxs-lookup"><span data-stu-id="34d05-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="34d05-113">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="34d05-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
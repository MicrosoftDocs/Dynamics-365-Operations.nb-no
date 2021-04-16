---
title: Opprette en mva-betaling
description: Jobbprosedyren Utlign og poster merverdiavgift utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5066689fb85dd176da1ca1561614e443cb87d816
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832760"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="c654d-103">Opprette en mva-betaling</span><span class="sxs-lookup"><span data-stu-id="c654d-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c654d-104">Jobbprosedyren Utlign og poster merverdiavgift utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.</span><span class="sxs-lookup"><span data-stu-id="c654d-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="c654d-105">Gå til **Avgift > Deklareringer > Merverdiavgift > Utlign og poster merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="c654d-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="c654d-106">Klikk på rullegardinknappen i **Utligningsperiode**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c654d-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c654d-107">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c654d-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c654d-108">Angi en dato i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c654d-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="c654d-109">Hvis du ikke velger alternativet **Ta med rettelser** på siden **Parametere for økonomimodul**, kan utligningen behandles for forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="c654d-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="c654d-110">Original er den første utligningen for et periodeintervall og kan bare behandles én gang for et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="c654d-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="c654d-111">De nyeste rettelsene utligner mva-transaksjoner som er postert etter at den opprinnelige versjonen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="c654d-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="c654d-112">Angi en dato i feltet **Transaksjonsdato**.</span><span class="sxs-lookup"><span data-stu-id="c654d-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="c654d-113">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c654d-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
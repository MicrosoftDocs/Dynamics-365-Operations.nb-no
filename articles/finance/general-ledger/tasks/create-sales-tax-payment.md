---
title: Opprette en mva-betaling
description: Utlign og poster merverdiavgift-jobben utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e41217d26239cf704709d1d48666c382e1e2e824
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985714"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="137ea-103">Opprette en mva-betaling</span><span class="sxs-lookup"><span data-stu-id="137ea-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="137ea-104">Utlign og poster merverdiavgift-jobben utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.</span><span class="sxs-lookup"><span data-stu-id="137ea-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="137ea-105">Gå til Avgift > Deklareringer > Merverdiavgift > Utlign og poster merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="137ea-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="137ea-106">Klikk rullegardinknappen i Utligningsperiode-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="137ea-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="137ea-107">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="137ea-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="137ea-108">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="137ea-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="137ea-109">Hvis alternativet Ta med rettelser ikke velges på siden for parametere for økonomimodulen, kan utligningen behandles for forskjellige versjoner.</span><span class="sxs-lookup"><span data-stu-id="137ea-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="137ea-110">Originalen er den første utligningen for et periodeintervall og kan bare behandles én gang for et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="137ea-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="137ea-111">Seneste rettelser utligner mva-transaksjoner som er postert etter at den opprinnelige versjonen er opprettet.</span><span class="sxs-lookup"><span data-stu-id="137ea-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="137ea-112">Angi en dato i feltet Transaksjonsdato.</span><span class="sxs-lookup"><span data-stu-id="137ea-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="137ea-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="137ea-113">Click OK.</span></span>


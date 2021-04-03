---
title: Utligne en etterdatert sjekk for en leverandør
description: Utlign en etterdatert sjekk som er utstedt til en leverandør, når banken har avregnet sjekktransaksjonen etter at sjekken er forfalt og avregnet av banken.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d66caa83df693445c1b1d40ffdc11e8d10cf7426
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239633"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="be263-103">Utligne en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="be263-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be263-104">Utlign en etterdatert sjekk som er utstedt til en leverandør, når banken har avregnet sjekktransaksjonen etter at sjekken er forfalt og avregnet av banken.</span><span class="sxs-lookup"><span data-stu-id="be263-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="be263-105">Fullfør den følgende prosedyren før du starter en ny.</span><span class="sxs-lookup"><span data-stu-id="be263-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="be263-106">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="be263-106">Set up postdated checks</span></span>

2) <span data-ttu-id="be263-107">Registrere og postere en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="be263-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="be263-108">Rollen til denne prosedyren er kasserer.</span><span class="sxs-lookup"><span data-stu-id="be263-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="be263-109">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="be263-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="be263-110">Gå til Leverandører > Betalinger > Etterdaterte sjekker for leverandør.</span><span class="sxs-lookup"><span data-stu-id="be263-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="be263-111">Klikk Utlign.</span><span class="sxs-lookup"><span data-stu-id="be263-111">Click Settle.</span></span>
3. <span data-ttu-id="be263-112">Klikk Utligne avregningsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="be263-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="be263-113">Utlign leverandørkontoen for sjekktransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="be263-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="be263-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="be263-114">Close the page.</span></span>
5. <span data-ttu-id="be263-115">Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.</span><span class="sxs-lookup"><span data-stu-id="be263-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="be263-116">Velg Alle i Vis-feltet.</span><span class="sxs-lookup"><span data-stu-id="be263-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="be263-117">Merk eller fjern merket for Bare vis brukeropprettet.</span><span class="sxs-lookup"><span data-stu-id="be263-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="be263-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="be263-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="be263-119">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="be263-119">Click Lines.</span></span>
10. <span data-ttu-id="be263-120">Klikk Bilag.</span><span class="sxs-lookup"><span data-stu-id="be263-120">Click Voucher.</span></span>
11. <span data-ttu-id="be263-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="be263-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46b419ab613425ae2d758f80105ac94f1ec5cc2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565978"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="9e82f-103">Utligne en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="9e82f-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e82f-104">Utlign en etterdatert sjekk som er utstedt til en leverandør, når banken har avregnet sjekktransaksjonen etter at sjekken er forfalt og avregnet av banken.</span><span class="sxs-lookup"><span data-stu-id="9e82f-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="9e82f-105">Fullfør den følgende prosedyren før du starter en ny.</span><span class="sxs-lookup"><span data-stu-id="9e82f-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="9e82f-106">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="9e82f-106">Set up postdated checks</span></span>

2) <span data-ttu-id="9e82f-107">Registrere og postere en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="9e82f-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="9e82f-108">Rollen til denne prosedyren er kasserer.</span><span class="sxs-lookup"><span data-stu-id="9e82f-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="9e82f-109">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="9e82f-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="9e82f-110">Gå til Leverandører > Betalinger > Etterdaterte sjekker for leverandør.</span><span class="sxs-lookup"><span data-stu-id="9e82f-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="9e82f-111">Klikk Utlign.</span><span class="sxs-lookup"><span data-stu-id="9e82f-111">Click Settle.</span></span>
3. <span data-ttu-id="9e82f-112">Klikk Utligne avregningsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="9e82f-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="9e82f-113">Utlign leverandørkontoen for sjekktransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="9e82f-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="9e82f-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9e82f-114">Close the page.</span></span>
5. <span data-ttu-id="9e82f-115">Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.</span><span class="sxs-lookup"><span data-stu-id="9e82f-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="9e82f-116">Velg Alle i Vis-feltet.</span><span class="sxs-lookup"><span data-stu-id="9e82f-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="9e82f-117">Merk eller fjern merket for Bare vis brukeropprettet.</span><span class="sxs-lookup"><span data-stu-id="9e82f-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="9e82f-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9e82f-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9e82f-119">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="9e82f-119">Click Lines.</span></span>
10. <span data-ttu-id="9e82f-120">Klikk Bilag.</span><span class="sxs-lookup"><span data-stu-id="9e82f-120">Click Voucher.</span></span>
11. <span data-ttu-id="9e82f-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9e82f-121">Close the page.</span></span>


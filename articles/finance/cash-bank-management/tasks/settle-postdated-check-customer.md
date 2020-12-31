---
title: Utligne en etterdatert sjekk fra en kunde
description: Du kan utligne en etterdatert sjekk etter at sjekken har blitt avregnet av banken.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc6f90e7adb3facdfa1facb50fecb0de4ccb04d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446460"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="8f7cf-103">Utligne en etterdatert sjekk fra en kunde</span><span class="sxs-lookup"><span data-stu-id="8f7cf-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f7cf-104">Du kan utligne en etterdatert sjekk etter at sjekken har blitt avregnet av banken.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="8f7cf-105">Denne økonomiske transaksjonen avregner også mellomkontotransaksjonen for den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="8f7cf-106">Følgende oppgaver må være fullført før du starter denne.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="8f7cf-107">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="8f7cf-107">Set up postdated checks</span></span>

2) <span data-ttu-id="8f7cf-108">Registrere og postere en etterdatert sjekk for en kunde</span><span class="sxs-lookup"><span data-stu-id="8f7cf-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="8f7cf-109">Rollen til denne oppgaveveiledningen er kasserer.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="8f7cf-110">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="8f7cf-111">Gå til Kreditt og innkreving > Forespørsler og rapporter > Betalinger > Etterdaterte sjekker for kunde.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="8f7cf-112">Klikk Utlign.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-112">Click Settle.</span></span>
3. <span data-ttu-id="8f7cf-113">Klikk Utligne avregningsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="8f7cf-114">Utlign kundekontoen for sjekktransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="8f7cf-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-115">Close the page.</span></span>
5. <span data-ttu-id="8f7cf-116">Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="8f7cf-117">Velg et alternativ i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="8f7cf-118">Merk eller fjern merket for Bare vis brukeropprettet.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="8f7cf-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="8f7cf-120">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-120">Click Lines.</span></span>
10. <span data-ttu-id="8f7cf-121">Klikk Bilag.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-121">Click Voucher.</span></span>
11. <span data-ttu-id="8f7cf-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8f7cf-122">Close the page.</span></span>


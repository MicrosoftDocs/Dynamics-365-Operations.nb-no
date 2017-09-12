--- 
title: Definere etterdaterte sjekker
description: "Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1d05580684b9e8bef3cfa84e8af5b8a71f655084
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="fbbea-103">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="fbbea-103">Set up postdated checks</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbbea-104">Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="fbbea-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="fbbea-105">Du kan også angi avregningskontoer for utstedte sjekker, mottatte sjekker og kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="fbbea-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="fbbea-106">Etterdaterte sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="fbbea-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="fbbea-107">Du kan angi om sjekken skal gjenspeiles i regnskapet før forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="fbbea-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="fbbea-108">Rollen til denne prosedyren er kasserer.</span><span class="sxs-lookup"><span data-stu-id="fbbea-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="fbbea-109">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="fbbea-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="fbbea-110">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="fbbea-110">Set up postdated checks</span></span>
1. <span data-ttu-id="fbbea-111">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="fbbea-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="fbbea-112">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="fbbea-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="fbbea-113">Merk av eller fjern merket i avmerkingsboksen Aktiver etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="fbbea-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="fbbea-114">Merk av eller fjern merket i avmerkingsboksen Poster journaloppføringer for etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="fbbea-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="fbbea-115">Angi ønskede verdier i feltet Avregningskonto for utstedte sjekker.</span><span class="sxs-lookup"><span data-stu-id="fbbea-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="fbbea-116">Angi ønskede verdier i feltet Avregningskonto for mottatte sjekker.</span><span class="sxs-lookup"><span data-stu-id="fbbea-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="fbbea-117">Skriv inn en verdi i feltet Økonomijournal for klarering av oppføringer.</span><span class="sxs-lookup"><span data-stu-id="fbbea-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="fbbea-118">Skriv inn en verdi i feltet Overfør etterdaterte sjekker til denne leverandørbetalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="fbbea-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="fbbea-119">Angir ønskede verdier feltet Clearingkonto for kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="fbbea-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="fbbea-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fbbea-120">Click Save.</span></span>
11. <span data-ttu-id="fbbea-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fbbea-121">Close the page.</span></span>
12. <span data-ttu-id="fbbea-122">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="fbbea-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="fbbea-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fbbea-123">Click New.</span></span>
14. <span data-ttu-id="fbbea-124">Skriv inn en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="fbbea-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="fbbea-125">Velg alternativet Etterdatert sjekklareringspostering for å indikere at sjekkbeløpet posteres til en avregningskonto.</span><span class="sxs-lookup"><span data-stu-id="fbbea-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="fbbea-126">Velg Bank i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="fbbea-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="fbbea-127">Motkontoen for betalingsmetoden vil være en bank.</span><span class="sxs-lookup"><span data-stu-id="fbbea-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="fbbea-128">Angi ønskede verdier i feltet Betalingskonto.</span><span class="sxs-lookup"><span data-stu-id="fbbea-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="fbbea-129">Velg bankkontoen som brukes til å trekke fakturabeløpet.</span><span class="sxs-lookup"><span data-stu-id="fbbea-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="fbbea-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fbbea-130">Close the page.</span></span>
19. <span data-ttu-id="fbbea-131">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="fbbea-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="fbbea-132">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fbbea-132">Click New.</span></span>
21. <span data-ttu-id="fbbea-133">Skriv inn en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="fbbea-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="fbbea-134">Velg alternativet Etterdatert sjekklareringspostering for å indikere at sjekkbeløpet posteres til en avregningskonto.</span><span class="sxs-lookup"><span data-stu-id="fbbea-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="fbbea-135">Velg Bank i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="fbbea-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="fbbea-136">Motkontoen for betalingsmetoden vil være en bank.</span><span class="sxs-lookup"><span data-stu-id="fbbea-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="fbbea-137">Angi ønskede verdier i feltet Betalingskonto.</span><span class="sxs-lookup"><span data-stu-id="fbbea-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="fbbea-138">Velg bankkontoen som brukes til å trekke fakturabeløpet.</span><span class="sxs-lookup"><span data-stu-id="fbbea-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="fbbea-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fbbea-139">Close the page.</span></span>



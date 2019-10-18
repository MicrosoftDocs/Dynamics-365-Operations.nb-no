---
title: Definere etterdaterte sjekker
description: Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 035f6e3b0268f8ee4c9006ca5f0527133cf2771c
ms.sourcegitcommit: 69f8233e86b32347474a25d83b4ac5920f60407d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2019
ms.locfileid: "2538484"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="d33ff-103">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="d33ff-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d33ff-104">Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="d33ff-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="d33ff-105">Du kan også angi avregningskontoer for utstedte sjekker, mottatte sjekker og kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="d33ff-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="d33ff-106">Etterdaterte sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="d33ff-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="d33ff-107">Du kan angi om sjekken skal gjenspeiles i regnskapet før forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d33ff-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="d33ff-108">Rollen til denne prosedyren er kasserer.</span><span class="sxs-lookup"><span data-stu-id="d33ff-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="d33ff-109">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="d33ff-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="d33ff-110">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="d33ff-110">Set up postdated checks</span></span>
1. <span data-ttu-id="d33ff-111">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="d33ff-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="d33ff-112">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="d33ff-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="d33ff-113">Merk av eller fjern merket i avmerkingsboksen Aktiver etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="d33ff-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="d33ff-114">Merk av eller fjern merket i avmerkingsboksen Poster journaloppføringer for etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="d33ff-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="d33ff-115">Angi ønskede verdier i feltet Avregningskonto for utstedte sjekker.</span><span class="sxs-lookup"><span data-stu-id="d33ff-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="d33ff-116">Angi ønskede verdier i feltet Avregningskonto for mottatte sjekker.</span><span class="sxs-lookup"><span data-stu-id="d33ff-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="d33ff-117">Skriv inn en verdi i feltet Økonomijournal for klarering av oppføringer.</span><span class="sxs-lookup"><span data-stu-id="d33ff-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="d33ff-118">Skriv inn en verdi i feltet Overfør etterdaterte sjekker til denne leverandørbetalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="d33ff-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="d33ff-119">Angir ønskede verdier feltet Clearingkonto for kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="d33ff-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="d33ff-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d33ff-120">Click Save.</span></span>
11. <span data-ttu-id="d33ff-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d33ff-121">Close the page.</span></span>
12. <span data-ttu-id="d33ff-122">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="d33ff-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="d33ff-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d33ff-123">Click New.</span></span>
14. <span data-ttu-id="d33ff-124">Skriv inn en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="d33ff-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="d33ff-125">Velg alternativet Etterdatert sjekklareringspostering for å indikere at sjekkbeløpet posteres til en avregningskonto.</span><span class="sxs-lookup"><span data-stu-id="d33ff-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="d33ff-126">Velg Bank i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="d33ff-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="d33ff-127">Motkontoen for betalingsmetoden vil være en bank.</span><span class="sxs-lookup"><span data-stu-id="d33ff-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="d33ff-128">Angi ønskede verdier i feltet Betalingskonto.</span><span class="sxs-lookup"><span data-stu-id="d33ff-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="d33ff-129">Velg bankkontoen som brukes til å trekke fakturabeløpet.</span><span class="sxs-lookup"><span data-stu-id="d33ff-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="d33ff-130">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d33ff-130">Click Save.</span></span>
19. <span data-ttu-id="d33ff-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d33ff-131">Close the page.</span></span>


---
title: Definere etterdaterte sjekker
description: Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adb8b969a6e86becaa3c0a3b59d8f8f259e5a64
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834602"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="c349f-103">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="c349f-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c349f-104">Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="c349f-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="c349f-105">Du kan også angi avregningskontoer for utstedte sjekker, mottatte sjekker og kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="c349f-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="c349f-106">Etterdaterte sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="c349f-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="c349f-107">Du kan angi om sjekken skal gjenspeiles i regnskapet før forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="c349f-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="c349f-108">Rollen til denne prosedyren er kasserer.</span><span class="sxs-lookup"><span data-stu-id="c349f-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="c349f-109">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="c349f-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="c349f-110">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="c349f-110">Set up postdated checks</span></span>
1. <span data-ttu-id="c349f-111">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="c349f-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="c349f-112">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="c349f-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="c349f-113">Merk av eller fjern merket i avmerkingsboksen Aktiver etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="c349f-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="c349f-114">Merk av eller fjern merket i avmerkingsboksen Poster journaloppføringer for etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="c349f-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="c349f-115">Angi ønskede verdier i feltet Avregningskonto for utstedte sjekker.</span><span class="sxs-lookup"><span data-stu-id="c349f-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="c349f-116">Angi ønskede verdier i feltet Avregningskonto for mottatte sjekker.</span><span class="sxs-lookup"><span data-stu-id="c349f-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="c349f-117">Skriv inn en verdi i feltet Økonomijournal for klarering av oppføringer.</span><span class="sxs-lookup"><span data-stu-id="c349f-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="c349f-118">Skriv inn en verdi i feltet Overfør etterdaterte sjekker til denne leverandørbetalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="c349f-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="c349f-119">Angir ønskede verdier feltet Clearingkonto for kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="c349f-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="c349f-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c349f-120">Click Save.</span></span>
11. <span data-ttu-id="c349f-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c349f-121">Close the page.</span></span>
12. <span data-ttu-id="c349f-122">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="c349f-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="c349f-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c349f-123">Click New.</span></span>
14. <span data-ttu-id="c349f-124">Skriv inn en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="c349f-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="c349f-125">Velg alternativet Etterdatert sjekklareringspostering for å indikere at sjekkbeløpet posteres til en avregningskonto.</span><span class="sxs-lookup"><span data-stu-id="c349f-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="c349f-126">Velg Bank i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="c349f-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="c349f-127">Motkontoen for betalingsmetoden vil være en bank.</span><span class="sxs-lookup"><span data-stu-id="c349f-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="c349f-128">Angi ønskede verdier i feltet Betalingskonto.</span><span class="sxs-lookup"><span data-stu-id="c349f-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="c349f-129">Velg bankkontoen som brukes til å trekke fakturabeløpet.</span><span class="sxs-lookup"><span data-stu-id="c349f-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="c349f-130">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c349f-130">Click Save.</span></span>
19. <span data-ttu-id="c349f-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c349f-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
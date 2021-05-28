---
title: Ytelse for avgiftsberegning påvirker transaksjoner
description: Dette emnet inneholder feilsøkingsinformasjon som er relatert til ytelse for avgiftsberegning og innvirkningen på transaksjoner.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020145"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="4b3b1-103">Ytelse for avgiftsberegning påvirker transaksjoner</span><span class="sxs-lookup"><span data-stu-id="4b3b1-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b3b1-104">Noen ganger påvirkes en transaksjon av ytelsesproblemer som avgiftsberegningen har.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="4b3b1-105">Hvis du vil feilsøke dette problemet, følger du trinnene i de følgende delene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="4b3b1-106">Gå gjennom linjeantallet i transaksjonen</span><span class="sxs-lookup"><span data-stu-id="4b3b1-106">Review the transaction line count</span></span>

<span data-ttu-id="4b3b1-107">Bestem om transaksjonen har et stort antall linjer (for eksempel mer enn flere hundre).</span><span class="sxs-lookup"><span data-stu-id="4b3b1-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="4b3b1-108">Hvis den ikke gjør det, kan du gå videre til den neste delen.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="4b3b1-109">Hvis transaksjonen har flere hundre linjer, utsetter du avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="4b3b1-110">Hvis du vil ha mer informasjon, kan du se [Aktivere forsinket avgiftsberegning i journaler](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="4b3b1-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="4b3b1-111">Deretter kan du fastslå om en av følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="4b3b1-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="4b3b1-112">Det finnes importtransaksjoner fra store filer.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="4b3b1-113">Flere økter behandler samme beregning av transaksjonsavgift samtidig.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="4b3b1-114">Transaksjonen har flere linjer, og visningene oppdateres i sanntid.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="4b3b1-115">Feltet **Beregnet mva-beløp i journalen** på **Økonomijournal**-siden oppdateres for eksempel i sanntid når en linjes felt endres.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="4b3b1-116">[![Feltet Beregnet mva-beløp i journalen på Journalbilag-siden](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="4b3b1-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="4b3b1-117">Hvis noen av disse betingelsene oppfylles, utsetter du avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="4b3b1-118">Gå gjennom samtalestakken</span><span class="sxs-lookup"><span data-stu-id="4b3b1-118">Review the call stack</span></span>

<span data-ttu-id="4b3b1-119">Gå gjennom samtalestakken for å fastslå om avgiftsberegning kalles flere ganger.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="4b3b1-120">Hvis den ikke gjør det, kan du gå videre til den neste delen.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="4b3b1-121">Hvis samtalestakken kalles flere ganger, følger du denne fremgangsmåten for å redusere beregningstider for skatt.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="4b3b1-122">Hvis journalen har vurdert transaksjonen, kan du utsette avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="4b3b1-123">Hvis du vil ha mer informasjon, kan du se [Aktivere forsinket avgiftsberegning i journaler](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="4b3b1-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="4b3b1-124">Hvis transaksjonen er en bestilling, og programversjonen er senere enn 10.0.15, kan du utsette avgiftsberegningen til den endelige beregningen ved å aktivere testversjoneringen for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="4b3b1-125">Gå gjennom tidslinjen for samtalestakken</span><span class="sxs-lookup"><span data-stu-id="4b3b1-125">Review the call stack timeline</span></span>

<span data-ttu-id="4b3b1-126">Gå gjennom tidslinjen for samtalestakk for å finne ut om følgende problemer finnes.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="4b3b1-127">Hvis de gjør det, må du aktivere testversjoneringen for **TaxUncommittedDoIsolateScopeFlighting** for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="4b3b1-128">Transaksjonen fører til at systemet slutter å svare til økten slutter.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="4b3b1-129">Transaksjonen kan derfor ikke beregne mva-resultatet.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="4b3b1-130">Illustrasjonen nedenfor viser meldingsboksen "Økt avsluttet" som du mottar.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="4b3b1-131">[![Melding om avsluttet økt](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="4b3b1-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="4b3b1-132">**TaxUncommitted**-metodene tar mer tid enn andre metoder.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="4b3b1-133">I følgende illustrasjon tar for eksempel metoden **TaxUncommitted::updateTaxUncommitted()** 43,34742 sekunder, mens andre metoder 0,09 sekunder.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="4b3b1-134">[![Metodevarigheter](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="4b3b1-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="4b3b1-135">Tilpasse og kalle avgiftsberegning</span><span class="sxs-lookup"><span data-stu-id="4b3b1-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="4b3b1-136">Når du tilpasser, må du ikke kalle avgiftsberegning på metoden **insert()** eller **update()** for hver linje.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="4b3b1-137">Avgiftsberegning bør kalles på transaksjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="4b3b1-138">Fastslå om det finnes tilpasning</span><span class="sxs-lookup"><span data-stu-id="4b3b1-138">Determine whether customization exists</span></span>

<span data-ttu-id="4b3b1-139">Hvis du har fullført trinnene i de forrige delene, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="4b3b1-140">Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.</span><span class="sxs-lookup"><span data-stu-id="4b3b1-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

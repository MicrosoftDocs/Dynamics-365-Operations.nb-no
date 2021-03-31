---
title: Behandle tildelinger
description: Denne artikkelen inneholder informasjon om tildelinger, alternativene for behandling av dem i Microsoft Dynamics 365 Finance, og hvordan de kan brukes i planleggingen av budsjettet. Tildelinger brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti. De bidrar til å sikre at utgifter eller inntekter belastes til riktig objekt i regnskapet.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b13496e764f907201a23f0dd6772ee22efffb250
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204984"
---
# <a name="process-allocations"></a><span data-ttu-id="15de4-105">Behandle tildelinger</span><span class="sxs-lookup"><span data-stu-id="15de4-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15de4-106">Denne artikkelen inneholder informasjon om tildelinger, alternativene for behandling av dem og hvordan de kan brukes i planleggingen av budsjettet.</span><span class="sxs-lookup"><span data-stu-id="15de4-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="15de4-107">Tildelinger brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti.</span><span class="sxs-lookup"><span data-stu-id="15de4-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="15de4-108">De bidrar til å sikre at utgifter eller inntekter belastes til riktig objekt i regnskapet.</span><span class="sxs-lookup"><span data-stu-id="15de4-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="15de4-109">Følgende funksjoner støtter denne prosessen:</span><span class="sxs-lookup"><span data-stu-id="15de4-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="15de4-110">Fordel transaksjonsbeløpene manuelt ved hjelp av Del-handlingen regnskapsdistribusjoner, eller ved å bruke standardmaler for finansdimensjon på et dokument.</span><span class="sxs-lookup"><span data-stu-id="15de4-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="15de4-111">Hvis du vil ha mer informasjon, kan du se [Regnskapsdistribusjoner](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="15de4-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="15de4-112">Fordel transaksjonsbeløp automatisk basert på fordelingsbetingelser som er definert på den individuelle hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="15de4-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="15de4-113">Tildelingskontooppføringer genereres for hver journal basert på prosentandelen og finanskontoen når en regnskapsoppføring oppfyller vilkårene som er definert som kildefinanskontoen.</span><span class="sxs-lookup"><span data-stu-id="15de4-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="15de4-114">Hvis du vil ha mer informasjon, kan du se [Tildelingsbetingelser for hovedkonto](../general-ledger/main-account-allocation-terms.md).</span><span class="sxs-lookup"><span data-stu-id="15de4-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="15de4-115">Fordel finanssaldoer eller faste beløp automatisk basert på finansfordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="15de4-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="15de4-116">Finansfordelingsreglene behandles på periodisk basis ved hjelp av fordelingsjournaler.</span><span class="sxs-lookup"><span data-stu-id="15de4-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="15de4-117">Hvis du vil ha mer informasjon, kan du se [Tilordningsregler](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="15de4-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="15de4-118">Fordelinger i budsjettplanlegging</span><span class="sxs-lookup"><span data-stu-id="15de4-118">Allocations in budget planning</span></span>

<span data-ttu-id="15de4-119">Finansfordelingsregler kan brukes for budsjettplaner.</span><span class="sxs-lookup"><span data-stu-id="15de4-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="15de4-120">Når du bruker finansfordelingsregler i budsjettplanlegging, fungerer fordelingsreglene på samme måte som de hadde gjort i Finans, men kildedataene og måldataene kommer fra budsjettplanen.</span><span class="sxs-lookup"><span data-stu-id="15de4-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="15de4-121">Du kan manuelt velge finansfordelingsregler som skal brukes for budsjettplaner.</span><span class="sxs-lookup"><span data-stu-id="15de4-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="15de4-122">Alternativt kan du bruke en fordelingsplan som kjører som en del av en arbeidsflytprosess.</span><span class="sxs-lookup"><span data-stu-id="15de4-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="15de4-123">Du kan ikke bruke konserinterne finansfordelingsregler for budsjettplanlegging.</span><span class="sxs-lookup"><span data-stu-id="15de4-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
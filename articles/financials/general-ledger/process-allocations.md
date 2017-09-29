---
title: Behandle tildelinger
description: "Denne artikkelen inneholder informasjon om tildelinger, alternativene for behandling av dem i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, og hvordan de kan brukes i planleggingen av budsjettet. Tildelinger brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti. De bidrar til å garantere at utgifter eller inntekter belastes til riktig objekt i regnskapet."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 8859359f70132e9116e6a2d534a0f5f1d0bfeb80
ms.contentlocale: nb-no
ms.lasthandoff: 06/29/2017


---

# <a name="process-allocations"></a><span data-ttu-id="afd8d-105">Behandle tildelinger</span><span class="sxs-lookup"><span data-stu-id="afd8d-105">Process allocations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="afd8d-106">Denne artikkelen inneholder informasjon om tildelinger, alternativene for behandling av dem i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, og hvordan de kan brukes i planleggingen av budsjettet.</span><span class="sxs-lookup"><span data-stu-id="afd8d-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and how they can be used in budget planning.</span></span> <span data-ttu-id="afd8d-107">Tildelinger brukes til å distribuere beløp på tvers av flere kombinasjoner av finanskonti.</span><span class="sxs-lookup"><span data-stu-id="afd8d-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="afd8d-108">De bidrar til å garantere at utgifter eller inntekter belastes til riktig objekt i regnskapet.</span><span class="sxs-lookup"><span data-stu-id="afd8d-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="afd8d-109">Microsoft Dynamics 365 for Finance and Operations har følgende funksjonalitet for å støtte denne prosessen:</span><span class="sxs-lookup"><span data-stu-id="afd8d-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="afd8d-110">Fordel transaksjonsbeløpene manuelt ved hjelp av Del-handlingen regnskapsdistribusjoner, eller ved å bruke standardmaler for finansdimensjon på et dokument.</span><span class="sxs-lookup"><span data-stu-id="afd8d-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="afd8d-111">Hvis du vil ha mer informasjon, kan du se [Regnskapsdistribusjoner](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="afd8d-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="afd8d-112">Fordel transaksjonsbeløp automatisk basert på fordelingsbetingelser som er definert på den individuelle hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="afd8d-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="afd8d-113">Tildelingskontooppføringer genereres for hver journal basert på prosentandelen og finanskontoen når en regnskapsoppføring oppfyller vilkårene som er definert som kildefinanskontoen.</span><span class="sxs-lookup"><span data-stu-id="afd8d-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="afd8d-114">Fordel finanssaldoer eller faste beløp automatisk basert på finansfordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="afd8d-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="afd8d-115">Finansfordelingsreglene behandles på periodisk basis ved hjelp av fordelingsjournaler.</span><span class="sxs-lookup"><span data-stu-id="afd8d-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="afd8d-116">Fordelinger i budsjettplanlegging</span><span class="sxs-lookup"><span data-stu-id="afd8d-116">Allocations in budget planning</span></span>

<span data-ttu-id="afd8d-117">Finansfordelingsregler kan brukes for budsjettplaner.</span><span class="sxs-lookup"><span data-stu-id="afd8d-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="afd8d-118">Når du bruker finansfordelingsregler i budsjettplanlegging, fungerer fordelingsreglene på samme måte som de hadde gjort i Finans, men kildedataene og måldataene kommer fra budsjettplanen.</span><span class="sxs-lookup"><span data-stu-id="afd8d-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="afd8d-119">Du kan manuelt velge finansfordelingsregler som skal brukes for budsjettplaner.</span><span class="sxs-lookup"><span data-stu-id="afd8d-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="afd8d-120">Alternativt kan du bruke en fordelingsplan som kjører som en del av en arbeidsflytprosess.</span><span class="sxs-lookup"><span data-stu-id="afd8d-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="afd8d-121">Du kan ikke bruke konserinterne finansfordelingsregler for budsjettplanlegging.</span><span class="sxs-lookup"><span data-stu-id="afd8d-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>







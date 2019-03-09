---
title: Opprette et budsjett fra transaksjonskontoer og totalkontoer
description: Denne artikkelen inneholder en oversikt over prosessen for å opprette budsjetter basert på totalkontoer. Den beskriver også hvordan du aktiverer budsjettkontroll for totalkontoer, hvis budsjettkontroll er nødvendig.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6129a5431cba22ea656e4d6f473a4e93a81131ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "331719"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="0a9b0-104">Opprette et budsjett fra transaksjonskontoer og totalkontoer</span><span class="sxs-lookup"><span data-stu-id="0a9b0-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a9b0-105">Denne artikkelen inneholder en oversikt over prosessen for å opprette budsjetter basert på totalkontoer.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="0a9b0-106">Den beskriver også hvordan du aktiverer budsjettkontroll for totalkontoer, hvis budsjettkontroll er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="0a9b0-107">Både dokumenter for budsjettplan og for budsjettregisteroppføring tillater budsjettering på hovedkontoer som har en hovedkonto av typen **Total**.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="0a9b0-108">Faktiske beløp kan bare posteres til transaksjonshovedkontoer.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="0a9b0-109">Når det gjelder den periodiske prosessen **Generer budsjettplan fra økonomimodul**, kan du angi **Total**-hovedkontotypen som et kriterium i **Kilde**-fanen.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="0a9b0-110">I dette tilfellet blir hver totalhovedkonto tatt med i målbudsjettplanen, og beløpet svarer til totalbeløpet for de utvalgte hovedkontoene.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="0a9b0-111">Du kan aktivere budsjettkontroll for hovedkontoer av **Total**-typen.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="0a9b0-112">Denne funksjonaliteten støttes gjennom bruk av budsjettgrupper.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="0a9b0-113">For hver totalhovedkonto må budsjettet som skal kontrolleres for en budsjettgruppe, opprettes på siden **Budsjettkontrollkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="0a9b0-114">Kriteriene du angir, må inneholde totalhovedkontoen og kontoområdet.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="0a9b0-115">Hvis du vil opprette budsjettgrupper raskere, kan du bruke dataenheten Budsjettkontrollgrupper.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="0a9b0-116">Når et budsjett brukes i rapportering, for eksempel i et regnskapsoppgjør, består budsjettsummen for totalkontoen av følgende beløp:</span><span class="sxs-lookup"><span data-stu-id="0a9b0-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="0a9b0-117">Budsjettene som er opprettet fra hver finanskonto for transaksjon, i intervallet til totalkontoen.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="0a9b0-118">Budsjettbeløpet som er angitt direkte i totalkontoen</span><span class="sxs-lookup"><span data-stu-id="0a9b0-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="0a9b0-119">Derfor kan du opprette egne budsjetter for de viktigste transaksjonskontoene i intervallet til totalkontoen og deretter legge til det tilgjengelige budsjettbeløpet i totalkontoen.</span><span class="sxs-lookup"><span data-stu-id="0a9b0-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




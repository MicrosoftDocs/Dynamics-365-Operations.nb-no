---
title: Opprette et foreløpig budsjett for offentlig sektor
description: Du kan opprette foreløpige budsjettregisteroppføringer for en bestemt budsjettmodell og dimensjonsverdier.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98968b0025ff5c3b9723dc6cc8a8eae799a4eb43
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557194"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="e7f1f-103">Opprette et foreløpig budsjett for offentlig sektor</span><span class="sxs-lookup"><span data-stu-id="e7f1f-103">Create a preliminary budget for Public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7f1f-104">Du kan opprette foreløpige budsjettregisteroppføringer for en bestemt budsjettmodell og dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="e7f1f-105">Når budsjettet er godkjent, kan du opprette opprinnelige budsjettregisteroppføringer.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="e7f1f-106">Denne prosedyren ble opprettet med demonstrasjonsfirmadataene for PSUS i partisjonen for offentlig sektor.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="e7f1f-107">Gå til Budsjettering > Budsjettregisteroppføringer.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="e7f1f-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-108">Click New.</span></span>
3. <span data-ttu-id="e7f1f-109">Klikk rullegardinknappen i Budsjettmodell-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e7f1f-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e7f1f-111">Klikk rullegardinknappen i Budsjettkode-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e7f1f-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e7f1f-113">Klikk rullegardinknappen i Årsakskode-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e7f1f-114">Klikk ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="e7f1f-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-115">Click Save.</span></span>
10. <span data-ttu-id="e7f1f-116">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-116">Click Add line.</span></span>
    * <span data-ttu-id="e7f1f-117">Valgfritt: Hvis du vil endre datoen fra den som står i hodet, angir du en ny dato.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="e7f1f-118">Denne datoen bestemmer regnskapsperioden budsjettett registreres på.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="e7f1f-119">Når du viser oppgaveveiledningen for å fylle ut andre felt, klikker du Lås opp øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="e7f1f-120">Klikk rullegardinknappen i feltet Kontostruktur for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="e7f1f-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="e7f1f-122">Angi de ønskede verdiene i Dimensjonsverdier-feltet.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="e7f1f-123">Angi et tall i Beløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="e7f1f-124">Du kan også angi beløpstype.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="e7f1f-125">Klikk rullegardinknappen i Valuta-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="e7f1f-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="e7f1f-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-127">Click Save.</span></span>
18. <span data-ttu-id="e7f1f-128">Klikk Oppdater budsjettsaldoer.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="e7f1f-129">Klikk Oppdater.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-129">Click Update.</span></span>
    * <span data-ttu-id="e7f1f-130">Hvis du vil se resultatene av oppdateringen, klikker du Meldingsdetaljer på den blå linjen.</span><span class="sxs-lookup"><span data-stu-id="e7f1f-130">To see the results of the update, click Message details on the blue bar.</span></span>  


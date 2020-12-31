---
title: Opprette et opprinnelig budsjett og deretter tilbakeføre foreløpige budsjettposter i offentlig sektor
description: Når du oppretter en opprinnelig budsjettpost og bruker budsjettmodellen og dimensjonsverdiene som inneholder de foreløpige budsjettbeløpene, kan de foreløpige budsjettbeløpene tilbakeføres.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32d89216d49a743729de8910f738276cbddcd8bb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446488"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="b19c3-103">Opprette et opprinnelig budsjett og deretter tilbakeføre foreløpige budsjettposter i offentlig sektor</span><span class="sxs-lookup"><span data-stu-id="b19c3-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b19c3-104">Når du oppretter en opprinnelig budsjettpost og bruker budsjettmodellen og dimensjonsverdiene som inneholder de foreløpige budsjettbeløpene, kan de foreløpige budsjettbeløpene tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="b19c3-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="b19c3-105">Denne prosedyren ble opprettet med demonstrasjonsfirmadataene for PSUS i partisjonen for offentlig sektor.</span><span class="sxs-lookup"><span data-stu-id="b19c3-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="b19c3-106">Gå til Budsjettering > Budsjettregisteroppføringer.</span><span class="sxs-lookup"><span data-stu-id="b19c3-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="b19c3-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b19c3-107">Click New.</span></span>
3. <span data-ttu-id="b19c3-108">Klikk rullegardinknappen i Budsjettmodell-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b19c3-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b19c3-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b19c3-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b19c3-110">Klikk rullegardinknappen i Budsjettkode-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b19c3-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b19c3-111">Klikk Opprinnelig budsjett i listen.</span><span class="sxs-lookup"><span data-stu-id="b19c3-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="b19c3-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b19c3-112">Click Save.</span></span>
8. <span data-ttu-id="b19c3-113">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="b19c3-113">Click Add line.</span></span>
9. <span data-ttu-id="b19c3-114">Valgfritt: Hvis du vil endre datoen fra den som står i hodet, angir du en ny dato.</span><span class="sxs-lookup"><span data-stu-id="b19c3-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="b19c3-115">Denne datoen bestemmer regnskapsperioden budsjettett registreres på.</span><span class="sxs-lookup"><span data-stu-id="b19c3-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="b19c3-116">Klikk rullegardinknappen i feltet Kontostruktur for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b19c3-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b19c3-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b19c3-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b19c3-118">Angi de ønskede verdiene i Dimensjonsverdier-feltet.</span><span class="sxs-lookup"><span data-stu-id="b19c3-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="b19c3-119">Angi et tall i Beløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="b19c3-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="b19c3-120">Klikk rullegardinknappen i Valuta-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b19c3-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b19c3-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b19c3-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b19c3-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b19c3-122">Click Save.</span></span>
17. <span data-ttu-id="b19c3-123">Klikk Oppdater budsjettsaldoer.</span><span class="sxs-lookup"><span data-stu-id="b19c3-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="b19c3-124">Valgfritt: Du kan velge alternativet for å tilbakeføre foreløpig budsjett.</span><span class="sxs-lookup"><span data-stu-id="b19c3-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="b19c3-125">Vær oppmerksom på at du kan tilbakeføre alle foreløpige budsjettposter, eller bare de foreløpige budsjettpostene med budsjettkoden du angir.</span><span class="sxs-lookup"><span data-stu-id="b19c3-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="b19c3-126">Klikk Lås opp-ikonet øverst på siden for å gjøre valgfrie valg.</span><span class="sxs-lookup"><span data-stu-id="b19c3-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="b19c3-127">Klikk Oppdater.</span><span class="sxs-lookup"><span data-stu-id="b19c3-127">Click Update.</span></span>


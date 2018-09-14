--- 
title: Opprette og tilordne avanserte regelstrukturer
description: "Denne oppgaveveiledningen viser trinn for å opprette og tilordne en avansert regelstruktur til en kontostruktur."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="26c6a-103">Opprette og tilordne avanserte regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="26c6a-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26c6a-104">Denne oppgaveveiledningen viser trinn for å opprette og tilordne en avansert regelstruktur til en kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="26c6a-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="26c6a-105">Denne veiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="26c6a-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="26c6a-106">Opprett en avansert regelstruktur</span><span class="sxs-lookup"><span data-stu-id="26c6a-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="26c6a-107">Gå til Økonomimodul > Kontoplan > Strukturer > Avanserte regelstrukturer.</span><span class="sxs-lookup"><span data-stu-id="26c6a-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="26c6a-108">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="26c6a-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="26c6a-109">I feltet Avansert regelstruktur skriver du inn et navn som beskriver strukturen for regelen.</span><span class="sxs-lookup"><span data-stu-id="26c6a-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="26c6a-110">Skriv inn en verdi for å beskrive strukturen, i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="26c6a-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="26c6a-111">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="26c6a-111">Click OK.</span></span>
6. <span data-ttu-id="26c6a-112">Klikk Legg til segment.</span><span class="sxs-lookup"><span data-stu-id="26c6a-112">Click Add segment.</span></span>
7. <span data-ttu-id="26c6a-113">Velg en finansdimensjon i listen over segmenter.</span><span class="sxs-lookup"><span data-stu-id="26c6a-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="26c6a-114">For eksempel Butikk.</span><span class="sxs-lookup"><span data-stu-id="26c6a-114">For example, Store.</span></span>  
8. <span data-ttu-id="26c6a-115">Klikk Legg til segment.</span><span class="sxs-lookup"><span data-stu-id="26c6a-115">Click Add segment.</span></span>
9. <span data-ttu-id="26c6a-116">Klikk koblingen for den avanserte regelstrukturen for å vise den, i listen.</span><span class="sxs-lookup"><span data-stu-id="26c6a-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="26c6a-117">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="26c6a-117">Click Activate.</span></span>
11. <span data-ttu-id="26c6a-118">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="26c6a-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="26c6a-119">Bruke en avansert regelstruktur for en kontostruktur</span><span class="sxs-lookup"><span data-stu-id="26c6a-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="26c6a-120">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="26c6a-120">Close the form.</span></span>
2. <span data-ttu-id="26c6a-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="26c6a-121">Close the page.</span></span>
3. <span data-ttu-id="26c6a-122">Gå til Økonomimodul > Kontoplan > Strukturer > Konfigurer kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="26c6a-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="26c6a-123">I listen, Finn og Merk kontostrukturen du vil bruke den avanserte regelen for.</span><span class="sxs-lookup"><span data-stu-id="26c6a-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="26c6a-124">Klikk navnet på kontostrukturen å åpne den.</span><span class="sxs-lookup"><span data-stu-id="26c6a-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="26c6a-125">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="26c6a-125">Click Edit.</span></span>
    * <span data-ttu-id="26c6a-126">Du kan også klikke Avanserte regler, og du blir bedt om å plassere kontostrukturen i utkastmodus.</span><span class="sxs-lookup"><span data-stu-id="26c6a-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="26c6a-127">Klikk Avanserte regler.</span><span class="sxs-lookup"><span data-stu-id="26c6a-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="26c6a-128">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="26c6a-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="26c6a-129">Skriv inn en verdi i feltet Avansert regel.</span><span class="sxs-lookup"><span data-stu-id="26c6a-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="26c6a-130">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="26c6a-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="26c6a-131">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="26c6a-131">Click Create.</span></span>
12. <span data-ttu-id="26c6a-132">Klikk Legg til nye kriterier.</span><span class="sxs-lookup"><span data-stu-id="26c6a-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="26c6a-133">Velg hovedkontoen eller en finansdimensjon i feltet Hvor.</span><span class="sxs-lookup"><span data-stu-id="26c6a-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="26c6a-134">Velg et alternativ, for eksempel er mellom og inkluderer i Operator-feltet.</span><span class="sxs-lookup"><span data-stu-id="26c6a-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="26c6a-135">Skriv inn en verdi i Verdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="26c6a-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="26c6a-136">Skriv inn en verdi i feltet via.</span><span class="sxs-lookup"><span data-stu-id="26c6a-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="26c6a-137">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="26c6a-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="26c6a-138">I listen finner du den avanserte regelstrukturen du vil bruke når kriteriene du angav er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="26c6a-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="26c6a-139">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="26c6a-139">Click Add.</span></span>
20. <span data-ttu-id="26c6a-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="26c6a-140">Close the page.</span></span>
21. <span data-ttu-id="26c6a-141">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="26c6a-141">Click Activate.</span></span>
22. <span data-ttu-id="26c6a-142">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="26c6a-142">Click Activate.</span></span>



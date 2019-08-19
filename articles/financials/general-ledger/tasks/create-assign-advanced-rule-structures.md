---
title: Opprette og tilordne avanserte regelstrukturer
description: Dette emnet forklarer hvordan du oppretter og tilordner en avansert regelstruktur til en kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834904"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="378c9-103">Opprette og tilordne avanserte regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="378c9-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="378c9-104">Dette emnet forklarer hvordan du oppretter og tilordner en avansert regelstruktur til en kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="378c9-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="378c9-105">Denne veiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="378c9-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="378c9-106">Opprett en avansert regelstruktur</span><span class="sxs-lookup"><span data-stu-id="378c9-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="378c9-107">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Strukturer > Avanserte regelstrukturer**.</span><span class="sxs-lookup"><span data-stu-id="378c9-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="378c9-108">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="378c9-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="378c9-109">I feltet **Avansert regelstruktur** skriver du inn et navn som beskriver strukturen for regelen.</span><span class="sxs-lookup"><span data-stu-id="378c9-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="378c9-110">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="378c9-110">Select **OK**.</span></span>
5. <span data-ttu-id="378c9-111">Velg **Legg til segment**.</span><span class="sxs-lookup"><span data-stu-id="378c9-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="378c9-112">Velg en finansdimensjon i listen over segmenter.</span><span class="sxs-lookup"><span data-stu-id="378c9-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="378c9-113">For eksempel **Butikk**.</span><span class="sxs-lookup"><span data-stu-id="378c9-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="378c9-114">Velg **Legg til segment**.</span><span class="sxs-lookup"><span data-stu-id="378c9-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="378c9-115">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="378c9-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="378c9-116">Bruke en avansert regelstruktur for en kontostruktur</span><span class="sxs-lookup"><span data-stu-id="378c9-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="378c9-117">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Strukturer > Konfigurer kontostrukturer**.</span><span class="sxs-lookup"><span data-stu-id="378c9-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="378c9-118">I listen, Finn og Merk kontostrukturen du vil bruke den avanserte regelen for.</span><span class="sxs-lookup"><span data-stu-id="378c9-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="378c9-119">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="378c9-119">Select **Edit**.</span></span> <span data-ttu-id="378c9-120">Du kan også velge **Avanserte regler**, og du blir bedt om å plassere kontostrukturen i **utkastmodus**.</span><span class="sxs-lookup"><span data-stu-id="378c9-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="378c9-121">Velg **Avanserte regler**.</span><span class="sxs-lookup"><span data-stu-id="378c9-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="378c9-122">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="378c9-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="378c9-123">Skriv inn en verdi i feltet **Avansert regel**.</span><span class="sxs-lookup"><span data-stu-id="378c9-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="378c9-124">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="378c9-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="378c9-125">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="378c9-125">Select **Create**.</span></span>
9. <span data-ttu-id="378c9-126">Velg **Legg til nye kriterier**.</span><span class="sxs-lookup"><span data-stu-id="378c9-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="378c9-127">Velg hovedkontoen eller en finansdimensjon i feltet **Hvor**.</span><span class="sxs-lookup"><span data-stu-id="378c9-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="378c9-128">Velg et alternativ, for eksempel **er mellom** og **inkluderer** i **Operator**-feltet.</span><span class="sxs-lookup"><span data-stu-id="378c9-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="378c9-129">Skriv inn en verdi i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="378c9-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="378c9-130">Skriv inn en verdi i feltet **via**.</span><span class="sxs-lookup"><span data-stu-id="378c9-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="378c9-131">Velg **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="378c9-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="378c9-132">I listen finner du den avanserte regelstrukturen du vil bruke når kriteriene du angav er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="378c9-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="378c9-133">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="378c9-133">Select **Add**.</span></span>
17. <span data-ttu-id="378c9-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="378c9-134">Close the page.</span></span>
18. <span data-ttu-id="378c9-135">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="378c9-135">Select **Activate**.</span></span>


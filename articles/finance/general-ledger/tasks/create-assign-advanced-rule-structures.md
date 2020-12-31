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
ms.openlocfilehash: cb18b96d6d7db84262f8fcfadb15afa80e2fa3d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446278"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="89254-103">Opprette og tilordne avanserte regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="89254-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89254-104">Dette emnet forklarer hvordan du oppretter og tilordner en avansert regelstruktur til en kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="89254-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="89254-105">Denne veiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="89254-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="89254-106">Opprett en avansert regelstruktur</span><span class="sxs-lookup"><span data-stu-id="89254-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="89254-107">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Strukturer > Avanserte regelstrukturer**.</span><span class="sxs-lookup"><span data-stu-id="89254-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="89254-108">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="89254-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="89254-109">I feltet **Avansert regelstruktur** skriver du inn et navn som beskriver strukturen for regelen.</span><span class="sxs-lookup"><span data-stu-id="89254-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="89254-110">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="89254-110">Select **OK**.</span></span>
5. <span data-ttu-id="89254-111">Velg **Legg til segment**.</span><span class="sxs-lookup"><span data-stu-id="89254-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="89254-112">Velg en finansdimensjon i listen over segmenter.</span><span class="sxs-lookup"><span data-stu-id="89254-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="89254-113">For eksempel **Butikk**.</span><span class="sxs-lookup"><span data-stu-id="89254-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="89254-114">Velg **Legg til segment**.</span><span class="sxs-lookup"><span data-stu-id="89254-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="89254-115">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="89254-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="89254-116">Bruke en avansert regelstruktur for en kontostruktur</span><span class="sxs-lookup"><span data-stu-id="89254-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="89254-117">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Strukturer > Konfigurer kontostrukturer**.</span><span class="sxs-lookup"><span data-stu-id="89254-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="89254-118">I listen, Finn og Merk kontostrukturen du vil bruke den avanserte regelen for.</span><span class="sxs-lookup"><span data-stu-id="89254-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="89254-119">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="89254-119">Select **Edit**.</span></span> <span data-ttu-id="89254-120">Du kan også velge **Avanserte regler**, og du blir bedt om å plassere kontostrukturen i **utkastmodus**.</span><span class="sxs-lookup"><span data-stu-id="89254-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="89254-121">Velg **Avanserte regler**.</span><span class="sxs-lookup"><span data-stu-id="89254-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="89254-122">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="89254-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="89254-123">Skriv inn en verdi i feltet **Avansert regel**.</span><span class="sxs-lookup"><span data-stu-id="89254-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="89254-124">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="89254-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="89254-125">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="89254-125">Select **Create**.</span></span>
9. <span data-ttu-id="89254-126">Velg **Legg til nye kriterier**.</span><span class="sxs-lookup"><span data-stu-id="89254-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="89254-127">Velg hovedkontoen eller en finansdimensjon i feltet **Hvor**.</span><span class="sxs-lookup"><span data-stu-id="89254-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="89254-128">Velg et alternativ, for eksempel **er mellom** og **inkluderer** i **Operator**-feltet.</span><span class="sxs-lookup"><span data-stu-id="89254-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="89254-129">Skriv inn en verdi i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="89254-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="89254-130">Skriv inn en verdi i feltet **via**.</span><span class="sxs-lookup"><span data-stu-id="89254-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="89254-131">Velg **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="89254-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="89254-132">I listen finner du den avanserte regelstrukturen du vil bruke når kriteriene du angav er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="89254-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="89254-133">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="89254-133">Select **Add**.</span></span>
17. <span data-ttu-id="89254-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89254-134">Close the page.</span></span>
18. <span data-ttu-id="89254-135">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="89254-135">Select **Activate**.</span></span>


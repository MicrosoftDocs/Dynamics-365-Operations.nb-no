---
title: Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter
description: Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cf0efeac2851e6ead6fc5e15a016370dfa620bc
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914913"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="aee19-103">Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="aee19-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aee19-104">Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="aee19-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="aee19-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="aee19-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="aee19-106">Den nye produktnummerterminologien tilordnes til produktdimensjonsgruppen farge og størrelse.</span><span class="sxs-lookup"><span data-stu-id="aee19-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="aee19-107">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="aee19-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="aee19-108">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="aee19-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="aee19-109">Velg **Definisjon av produktvariantmodell**.</span><span class="sxs-lookup"><span data-stu-id="aee19-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="aee19-110">Velg **Produktnummerterminologi**.</span><span class="sxs-lookup"><span data-stu-id="aee19-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="aee19-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aee19-111">Select **New**.</span></span>
4. <span data-ttu-id="aee19-112">I **Navn**-feltet angir du et terminologinavn som hjelper deg med å identifisere målproduktdimensjonsgruppen, for eksempel `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="aee19-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="aee19-113">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="aee19-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="aee19-114">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="aee19-114">Select **Add**.</span></span>
7. <span data-ttu-id="aee19-115">Velg **Produktstandardnummer**.</span><span class="sxs-lookup"><span data-stu-id="aee19-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="aee19-116">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="aee19-116">Select **Add**.</span></span>
9. <span data-ttu-id="aee19-117">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="aee19-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="aee19-118">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="aee19-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="aee19-119">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="aee19-119">Select **Add**.</span></span>
12. <span data-ttu-id="aee19-120">Velg **Farge**.</span><span class="sxs-lookup"><span data-stu-id="aee19-120">Select **Color**.</span></span>
13. <span data-ttu-id="aee19-121">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="aee19-121">Select **Add**.</span></span>
14. <span data-ttu-id="aee19-122">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="aee19-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="aee19-123">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="aee19-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="aee19-124">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="aee19-124">Select **Add**.</span></span>
17. <span data-ttu-id="aee19-125">Velg **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="aee19-125">Select **Size**.</span></span>
18. <span data-ttu-id="aee19-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="aee19-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="aee19-127">Tilordne terminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="aee19-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="aee19-128">Velg **Produktdimensjonsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="aee19-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="aee19-129">Velg **produktdimensjonsgruppen SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="aee19-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="aee19-130">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="aee19-130">Select **Edit**.</span></span>
4. <span data-ttu-id="aee19-131">Velg **Ja** i feltet **Bruk nomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="aee19-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="aee19-132">Angi eller velg en verdi i feltet **Produktvariantnummerterminologi**.</span><span class="sxs-lookup"><span data-stu-id="aee19-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="aee19-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="aee19-133">Close the page.</span></span>


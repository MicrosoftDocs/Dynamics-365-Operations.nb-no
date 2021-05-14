---
title: Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter
description: Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920663"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="d823e-103">Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="d823e-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d823e-104">Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d823e-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="d823e-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d823e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d823e-106">Den nye produktnummerterminologien tilordnes til produktdimensjonsgruppen farge og størrelse.</span><span class="sxs-lookup"><span data-stu-id="d823e-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="d823e-107">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="d823e-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="d823e-108">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="d823e-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="d823e-109">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktterminologi**.</span><span class="sxs-lookup"><span data-stu-id="d823e-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="d823e-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d823e-110">Select **New**.</span></span>
1. <span data-ttu-id="d823e-111">I **Navn**-feltet angir du et terminologinavn som hjelper deg med å identifisere målproduktdimensjonsgruppen, for eksempel `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="d823e-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="d823e-112">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d823e-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="d823e-113">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="d823e-113">Select **Add**.</span></span>
1. <span data-ttu-id="d823e-114">Velg **Produktstandardnummer**.</span><span class="sxs-lookup"><span data-stu-id="d823e-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="d823e-115">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="d823e-115">Select **Add**.</span></span>
1. <span data-ttu-id="d823e-116">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="d823e-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="d823e-117">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d823e-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d823e-118">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="d823e-118">Select **Add**.</span></span>
1. <span data-ttu-id="d823e-119">Velg **Farge**.</span><span class="sxs-lookup"><span data-stu-id="d823e-119">Select **Color**.</span></span>
1. <span data-ttu-id="d823e-120">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="d823e-120">Select **Add**.</span></span>
1. <span data-ttu-id="d823e-121">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="d823e-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="d823e-122">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d823e-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d823e-123">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="d823e-123">Select **Add**.</span></span>
1. <span data-ttu-id="d823e-124">Velg **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="d823e-124">Select **Size**.</span></span>
1. <span data-ttu-id="d823e-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d823e-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="d823e-126">Tilordne terminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="d823e-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="d823e-127">Velg **Produktdimensjonsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="d823e-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="d823e-128">Velg **produktdimensjonsgruppen SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="d823e-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="d823e-129">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d823e-129">Select **Edit**.</span></span>
4. <span data-ttu-id="d823e-130">Velg **Ja** i feltet **Bruk nomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="d823e-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="d823e-131">Angi eller velg en verdi i feltet **Produktvariantnummerterminologi**.</span><span class="sxs-lookup"><span data-stu-id="d823e-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="d823e-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d823e-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Vedlikeholdsattributtyper
description: Dette emnet forklarer hvordan du oppretter attributtyper i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783482"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="4932b-103">Vedlikeholdsattributtyper</span><span class="sxs-lookup"><span data-stu-id="4932b-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4932b-104">Dette emnet forklarer hvordan du oppretter attributtyper i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="4932b-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="4932b-105">Attributter brukes til å beskrive egenskapene til ulike elementer.</span><span class="sxs-lookup"><span data-stu-id="4932b-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="4932b-106">Du kan angi attributter for følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="4932b-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="4932b-107">Arbeidsstedstyper</span><span class="sxs-lookup"><span data-stu-id="4932b-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="4932b-108">Arbeidssteder</span><span class="sxs-lookup"><span data-stu-id="4932b-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="4932b-109">Aktivatyper</span><span class="sxs-lookup"><span data-stu-id="4932b-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="4932b-110">Aktiva</span><span class="sxs-lookup"><span data-stu-id="4932b-110">Assets</span></span>

<span data-ttu-id="4932b-111">Attributtene du kan definere, varierer avhengig av elementet.</span><span class="sxs-lookup"><span data-stu-id="4932b-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="4932b-112">Hvis du for eksempel vil ha et arbeidssted, kan du definere attributter for konfigurasjonen og den fysiske størrelsen på stedet.</span><span class="sxs-lookup"><span data-stu-id="4932b-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="4932b-113">For en aktivatype eller et aktivum kan du definere attributter for motorvolum, strømforbruk og maksimal lastekapasitet under ulike forhold.</span><span class="sxs-lookup"><span data-stu-id="4932b-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="4932b-114">Opprette attributtyper</span><span class="sxs-lookup"><span data-stu-id="4932b-114">Create attribute types</span></span>

<span data-ttu-id="4932b-115">Du kan opprette dine egne attributtyper.</span><span class="sxs-lookup"><span data-stu-id="4932b-115">You can create your own attribute types.</span></span> <span data-ttu-id="4932b-116">I tillegg kan du overføre produktdimensjoner fra Microsoft Dynamics 365 for Finance and Operations til siden **Attributtyper**.</span><span class="sxs-lookup"><span data-stu-id="4932b-116">Additionally, you can transfer product dimensions from Microsoft Dynamics 365 for Finance and Operations to the **Attribute types** page.</span></span>

1. <span data-ttu-id="4932b-117">Velg **Aktivastyring** \> **Oppsett** \> **Attributtyper**.</span><span class="sxs-lookup"><span data-stu-id="4932b-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="4932b-118">Første gang du definerer attributtverdier, velger du **Opprett produktdimensjoner** for å overføre standard Finance and Operations-produktdimensjoner automatisk.</span><span class="sxs-lookup"><span data-stu-id="4932b-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard Finance and Operations product dimensions.</span></span>
3. <span data-ttu-id="4932b-119">Velg **Ny** for å opprette en ny attributtype.</span><span class="sxs-lookup"><span data-stu-id="4932b-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="4932b-120">I **Attributtype**-feltet angir du et navn på attributtypen.</span><span class="sxs-lookup"><span data-stu-id="4932b-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="4932b-121">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4932b-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="4932b-122">I **Enhet**-feltet velger du den aktuelle attributtenheten etter behov.</span><span class="sxs-lookup"><span data-stu-id="4932b-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="4932b-123">I **Datatype**-feltet velger du en datatype for enheten.</span><span class="sxs-lookup"><span data-stu-id="4932b-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="4932b-124">Hvis du valgte **Streng** som datatype, følger du denne fremgangsmåten for å opprette verdier for attributtypen:</span><span class="sxs-lookup"><span data-stu-id="4932b-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="4932b-125">Velg attributtypen, og velg deretter **Verdier**.</span><span class="sxs-lookup"><span data-stu-id="4932b-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="4932b-126">I **Attributtverdier**-feltet velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4932b-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="4932b-127">Velg en attributtype (dimensjon) i **Attributtype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4932b-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="4932b-128">Angi en relatert verdi i feltet **Verdi**.</span><span class="sxs-lookup"><span data-stu-id="4932b-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="4932b-129">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4932b-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="4932b-130">Lagre posten.</span><span class="sxs-lookup"><span data-stu-id="4932b-130">Save the record.</span></span>
    7. <span data-ttu-id="4932b-131">Gå tilbake til siden **Attributtyper**.</span><span class="sxs-lookup"><span data-stu-id="4932b-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="4932b-132">Lagre posten.</span><span class="sxs-lookup"><span data-stu-id="4932b-132">Save the record.</span></span>

    <span data-ttu-id="4932b-133">Feltet **Arbeidsstedstyper** viser antall arbeidssteder som bruker attributtypen.</span><span class="sxs-lookup"><span data-stu-id="4932b-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="4932b-134">Feltet **Aktivatyper** viser antall aktivatyper som bruker den.</span><span class="sxs-lookup"><span data-stu-id="4932b-134">The **Asset types** field shows the number of asset types that are using it.</span></span>

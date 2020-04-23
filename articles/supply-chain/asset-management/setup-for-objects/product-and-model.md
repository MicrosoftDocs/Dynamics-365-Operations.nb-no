---
title: Aktivaprodusenter og -modeller
description: Dette emnet forklarer hvordan du definerer aktivaprodusenter og beslektede modeller i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2ef8a9afc007ce7e453f5e9cadfb912490545c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205121"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="14602-103">Aktivaprodusenter og -modeller</span><span class="sxs-lookup"><span data-stu-id="14602-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="14602-104">Dette emnet forklarer hvordan du definerer aktivaprodusenter og beslektede modeller i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="14602-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="14602-105">Modeller kan være relatert til aktivatyper.</span><span class="sxs-lookup"><span data-stu-id="14602-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="14602-106">Definere relasjoner mellom produkter og modeller</span><span class="sxs-lookup"><span data-stu-id="14602-106">Set up product-model relations</span></span>

1. <span data-ttu-id="14602-107">Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Produsent og modell**.</span><span class="sxs-lookup"><span data-stu-id="14602-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="14602-108">Velg **Ny** for å opprette et nytt produkt.</span><span class="sxs-lookup"><span data-stu-id="14602-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="14602-109">I feltet **Produsent** angir du et navn på aktivaprodusenten.</span><span class="sxs-lookup"><span data-stu-id="14602-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="14602-110">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="14602-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="14602-111">På hurtigfanen **Modeller** velger du **Legg til** for å opprette en aktivamodell som skal være relatert til aktivaprodusenten.</span><span class="sxs-lookup"><span data-stu-id="14602-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="14602-112">I feltet **Modell** angir du et navn på aktivamodellen.</span><span class="sxs-lookup"><span data-stu-id="14602-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="14602-113">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="14602-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="14602-114">I feltet **Aktivatype** velger du aktivatypen som produsentmodellen skal være knyttet til.</span><span class="sxs-lookup"><span data-stu-id="14602-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14602-115">Du kan også definere relasjoner for aktivatyper, -produsenter og -modeller i oppslaget **Aktivatyper**.</span><span class="sxs-lookup"><span data-stu-id="14602-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="14602-116">Hvis du vil ha mer informasjon, kan du se [Aktivatyper](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="14602-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="14602-117">På hurtigfanen **Detaljer** viser **Modeller**-feltet antallet aktivamodeller som er definert for den valgte aktivaprodusenten.</span><span class="sxs-lookup"><span data-stu-id="14602-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="14602-118">**Aktiva**-feltet viser antall aktiva som bruker den valgte produsenten.</span><span class="sxs-lookup"><span data-stu-id="14602-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="14602-119">**Aktiva**-feltet viser antall objekter som bruker produsentmodellen.</span><span class="sxs-lookup"><span data-stu-id="14602-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="14602-120">En aktivatype kan ikke ha relasjoner mellom aktivaprodusent og -modell, den kan være relatert til én aktivaprodusentmodell, eller den kan være relatert til flere aktivaprodusentmodeller.</span><span class="sxs-lookup"><span data-stu-id="14602-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="14602-121">Hvis en aktivatype er knyttet til minst én produsentmodell, kan bare kombinasjonene som er definert i oppslaget **Produsentmodell** velges på disse Aktivastyring-sidene, der en kombinasjon av en aktivatype, -produsent og -modell kan defineres.</span><span class="sxs-lookup"><span data-stu-id="14602-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="14602-122">Disse sidene omfatter **Alle aktiva**, **Tjenestenivåer for aktiva**, **Jobbtypestandarder** og **Vedlikeholdsbudsjettlinjer**.</span><span class="sxs-lookup"><span data-stu-id="14602-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="14602-123">Hvis enkelte aktivatyper ikke er knyttet til noen produsentmodell, vises bare disse aktivatypene og produsentmodellene som heller ikke har en relasjon til aktivatyper, på sidene.</span><span class="sxs-lookup"><span data-stu-id="14602-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="14602-124">Velge en produsent og modell på et objekt</span><span class="sxs-lookup"><span data-stu-id="14602-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="14602-125">Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="14602-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="14602-126">Velg koblingen for aktivumet i **Aktiva**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="14602-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="14602-127">Siden **Detaljer** vises.</span><span class="sxs-lookup"><span data-stu-id="14602-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="14602-128">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="14602-128">Select **Edit**.</span></span>
4. <span data-ttu-id="14602-129">På hurtigfanen **Generelt** velger du verdier i feltene **Produsent** og **Modell**.</span><span class="sxs-lookup"><span data-stu-id="14602-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>

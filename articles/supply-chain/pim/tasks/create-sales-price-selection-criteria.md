---
title: Opprette valgkriterier for salgspris
description: Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920537"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="7a2f4-103">Opprette valgkriterier for salgspris</span><span class="sxs-lookup"><span data-stu-id="7a2f4-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a2f4-104">Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="7a2f4-105">Denne prosedyren krever at minst én salgsprismodell er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="7a2f4-106">Dette eksemplet bruker prismodellen for salgsprismodellen for høyttalerløsningen i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="7a2f4-107">Produktsjefen bruker vanligvis denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="7a2f4-108">Legge til et nytt kriterium for en eksisterende salgsprismodell</span><span class="sxs-lookup"><span data-stu-id="7a2f4-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="7a2f4-109">Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="7a2f4-110">I listen velger du raden for produktmodellen for høyttalerløsningen, men ikke velg koblingen for modellnavnet.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="7a2f4-111">Velg **Modell** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="7a2f4-112">Velg **Prismodellkriterier**.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="7a2f4-113">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-113">Select **New**.</span></span>
1. <span data-ttu-id="7a2f4-114">I **Navn**-feltet skriver du inn Kundegruppe 10.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="7a2f4-115">Navnet på prismodellkriteriet brukes til å identifisere de underliggende valgkriteriene.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="7a2f4-116">Angi eller velg en verdi i feltet **Prismodell**.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="7a2f4-117">Velg **Salgsordre** i feltet *Ordretype*.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="7a2f4-118">Ordretypen bestemmer databasefeltene som vil være tilgjengelige for valgspørringen.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="7a2f4-119">Angi en dato i **Gyldig fra**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="7a2f4-120">Angi en dato i **Utløp innen**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="7a2f4-121">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="7a2f4-122">Opprette spørringen for valgkriteriene</span><span class="sxs-lookup"><span data-stu-id="7a2f4-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="7a2f4-123">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-123">Select **Edit**.</span></span>
2. <span data-ttu-id="7a2f4-124">Velg **Kunder** i feltet *Tabell*.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="7a2f4-125">Velg **Kundegruppe** i *Felt*-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="7a2f4-126">I dette eksemplet bruker vi en spesifikk kundegruppe for valgkriteriene.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="7a2f4-127">Velg **Kundegruppe 10** i *Kriterier*-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="7a2f4-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a2f4-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
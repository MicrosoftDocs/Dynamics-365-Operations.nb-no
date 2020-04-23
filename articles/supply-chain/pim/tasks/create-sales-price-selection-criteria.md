---
title: Opprette valgkriterier for salgspris
description: Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d1385a83da5b6448a9c753d7469979796043b60
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203785"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="67f1b-103">Opprette valgkriterier for salgspris</span><span class="sxs-lookup"><span data-stu-id="67f1b-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67f1b-104">Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller.</span><span class="sxs-lookup"><span data-stu-id="67f1b-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="67f1b-105">Denne prosedyren krever at minst én salgsprismodell er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="67f1b-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="67f1b-106">Dette eksemplet bruker prismodellen for salgsprismodellen for høyttalerløsningen i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="67f1b-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="67f1b-107">Produktsjefen bruker vanligvis denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="67f1b-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="67f1b-108">Legge til et nytt kriterium for en eksisterende salgsprismodell</span><span class="sxs-lookup"><span data-stu-id="67f1b-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="67f1b-109">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="67f1b-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="67f1b-110">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="67f1b-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="67f1b-111">I listen velger du raden for produktmodellen for høyttalerløsningen, men ikke klikk koblingen for modellnavnet.</span><span class="sxs-lookup"><span data-stu-id="67f1b-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="67f1b-112">Klikk Modell i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="67f1b-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="67f1b-113">Klikk Prismodellkriterier.</span><span class="sxs-lookup"><span data-stu-id="67f1b-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="67f1b-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="67f1b-114">Click New.</span></span>
7. <span data-ttu-id="67f1b-115">I Navn-feltet skriver du inn Kundegruppe 10.</span><span class="sxs-lookup"><span data-stu-id="67f1b-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="67f1b-116">Navnet på prismodellkriteriet brukes til å identifisere de underliggende valgkriteriene.</span><span class="sxs-lookup"><span data-stu-id="67f1b-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="67f1b-117">Angi eller velg en verdi i feltet Prismodell.</span><span class="sxs-lookup"><span data-stu-id="67f1b-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="67f1b-118">Velg Salgsordre i feltet Ordretype.</span><span class="sxs-lookup"><span data-stu-id="67f1b-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="67f1b-119">Ordretypen bestemmer databasefeltene som vil være tilgjengelige for valgspørringen.</span><span class="sxs-lookup"><span data-stu-id="67f1b-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="67f1b-120">Angi en dato i Gyldig fra-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f1b-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="67f1b-121">Angi en dato i Utløp innen-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f1b-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="67f1b-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="67f1b-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="67f1b-123">Opprette spørringen for valgkriteriene</span><span class="sxs-lookup"><span data-stu-id="67f1b-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="67f1b-124">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="67f1b-124">Click Edit.</span></span>
2. <span data-ttu-id="67f1b-125">Velg Kunder i feltet Tabell.</span><span class="sxs-lookup"><span data-stu-id="67f1b-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="67f1b-126">Velg Kundegruppe i Felt-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f1b-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="67f1b-127">I dette eksemplet bruker vi en spesifikk kundegruppe for valgkriteriene.</span><span class="sxs-lookup"><span data-stu-id="67f1b-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="67f1b-128">Velg Kundegruppe 10 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="67f1b-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="67f1b-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="67f1b-129">Click OK.</span></span>


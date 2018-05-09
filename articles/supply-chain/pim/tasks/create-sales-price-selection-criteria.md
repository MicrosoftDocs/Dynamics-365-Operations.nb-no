--- 
title: Opprette valgkriterier for salgspris
description: "Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cbc442724e85f7e03cf28471c850f034101c12c2
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="ed0b7-103">Opprette valgkriterier for salgspris</span><span class="sxs-lookup"><span data-stu-id="ed0b7-103">Create sales price selection criteria</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ed0b7-104">Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="ed0b7-105">Denne prosedyren krever at minst én salgsprismodell er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="ed0b7-106">Dette eksemplet bruker prismodellen for salgsprismodellen for høyttalerløsningen i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="ed0b7-107">Produktsjefen bruker vanligvis denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="ed0b7-108">Legge til et nytt kriterium for en eksisterende salgsprismodell</span><span class="sxs-lookup"><span data-stu-id="ed0b7-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="ed0b7-109">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ed0b7-110">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="ed0b7-111">I listen velger du raden for produktmodellen for høyttalerløsningen, men ikke klikk koblingen for modellnavnet.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-111">In the list, select the row for the Speaker solution product model, but don’t click the link for the model name.</span></span>
4. <span data-ttu-id="ed0b7-112">Klikk Modell i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="ed0b7-113">Klikk Prismodellkriterier.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="ed0b7-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-114">Click New.</span></span>
7. <span data-ttu-id="ed0b7-115">I Navn-feltet skriver du inn Kundegruppe 10.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-115">In the Name field, type ‘Customer group 10’.</span></span>
    * <span data-ttu-id="ed0b7-116">Navnet på prismodellkriteriet brukes til å identifisere de underliggende valgkriteriene.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="ed0b7-117">Angi eller velg en verdi i feltet Prismodell.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="ed0b7-118">Velg Salgsordre i feltet Ordretype.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="ed0b7-119">Ordretypen bestemmer databasefeltene som vil være tilgjengelige for valgspørringen.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="ed0b7-120">Angi en dato i Gyldig fra-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="ed0b7-121">Angi en dato i Utløp innen-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="ed0b7-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="ed0b7-123">Opprette spørringen for valgkriteriene</span><span class="sxs-lookup"><span data-stu-id="ed0b7-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="ed0b7-124">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-124">Click Edit.</span></span>
2. <span data-ttu-id="ed0b7-125">Velg Kunder i feltet Tabell.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="ed0b7-126">Velg Kundegruppe i Felt-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="ed0b7-127">I dette eksemplet bruker vi en spesifikk kundegruppe for valgkriteriene.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="ed0b7-128">Velg Kundegruppe 10 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="ed0b7-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ed0b7-129">Click OK.</span></span>



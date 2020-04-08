---
title: Opprette en ny Kanban-regel ved å duplisere en eksisterende Kanban-regel
description: Denne prosedyren fokuserer på å opprette en kopi av en eksisterende kanban-regel.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc65dd80221cedd25890037afcb3d2617f22793
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149215"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="5832f-103">Opprette en ny Kanban-regel ved å duplisere en eksisterende Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="5832f-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5832f-104">Denne prosedyren fokuserer på å opprette en kopi av en eksisterende kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="5832f-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="5832f-105">Dette er nyttig hvis du vil opprette nye kanban-regler basert på eksisterende kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="5832f-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="5832f-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5832f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5832f-107">Denne fremgangsmåten er ment for prosessingeniøren eller verdistrømlederen når de klargjør produksjon for en endret produksjonsflyt eller en ny etterfyllingsregel.</span><span class="sxs-lookup"><span data-stu-id="5832f-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="5832f-108">Velge en Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="5832f-108">Select a kanban rule</span></span>
1. <span data-ttu-id="5832f-109">Gå til Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="5832f-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="5832f-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5832f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5832f-111">Velg Kanban-regel 000017 for produkt M0006.</span><span class="sxs-lookup"><span data-stu-id="5832f-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="5832f-112">Duplisere en Kanban-regel</span><span class="sxs-lookup"><span data-stu-id="5832f-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="5832f-113">Klikk Dupliser Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="5832f-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="5832f-114">Når du dupliserer en kanban-regel, er det mulig å endre type, datoer, aktiviteter og produktvalget.</span><span class="sxs-lookup"><span data-stu-id="5832f-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="5832f-115">Endre produktet for denne prosedyren i neste trinn.</span><span class="sxs-lookup"><span data-stu-id="5832f-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="5832f-116">Angi eller velg en verdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="5832f-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="5832f-117">Velg M0007.</span><span class="sxs-lookup"><span data-stu-id="5832f-117">Select M0007.</span></span>  
3. <span data-ttu-id="5832f-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5832f-118">Click OK.</span></span>
    * <span data-ttu-id="5832f-119">Legg merke til at det opprettes en kopi av Kanban-regel 000017.</span><span class="sxs-lookup"><span data-stu-id="5832f-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    


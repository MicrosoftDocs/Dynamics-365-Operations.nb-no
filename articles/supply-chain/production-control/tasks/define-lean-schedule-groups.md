---
title: Definere lean-planleggingsgrupper
description: Lean-planleggingsgrupper defineres for å gruppere og skille produkter i kanban-planleggingen.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9ad470d81d94a0af1c4c4dc6c5072354cfd96d2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975854"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="32260-103">Definere lean-planleggingsgrupper</span><span class="sxs-lookup"><span data-stu-id="32260-103">Define lean schedule groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32260-104">Lean-planleggingsgrupper defineres for å gruppere og skille produkter i kanban-planleggingen.</span><span class="sxs-lookup"><span data-stu-id="32260-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="32260-105">Grupperingen kan utføres som generisk tilknytning per firma eller spesifikk for en arbeidscelle.</span><span class="sxs-lookup"><span data-stu-id="32260-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="32260-106">Hver gruppe har en fargekode tilordnet for visuell indikasjon på listesiden for kanban-planlegging.</span><span class="sxs-lookup"><span data-stu-id="32260-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="32260-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="32260-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="32260-108">Definere lean-planleggingsgruppe</span><span class="sxs-lookup"><span data-stu-id="32260-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="32260-109">Gå til Behandling av produktinformasjon > Lean manufacturing > Lean-planleggingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="32260-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="32260-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="32260-110">Click New.</span></span>
3. <span data-ttu-id="32260-111">Skriv inn en verdi i feltet Tidsplangruppe.</span><span class="sxs-lookup"><span data-stu-id="32260-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="32260-112">En planleggingsgruppegruppe kan defineres som global gruppe eller spesifikk for en arbeidscelle.</span><span class="sxs-lookup"><span data-stu-id="32260-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="32260-113">I dette enkle eksemplet definerer vi en global gruppe, og arbeidscellen beholdes tom.</span><span class="sxs-lookup"><span data-stu-id="32260-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="32260-114">Innstillingene for denne gruppen gjelder for alle arbeidsceller som ikke har bestemte planleggingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="32260-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="32260-115">Velg en farge fra fargevalget.</span><span class="sxs-lookup"><span data-stu-id="32260-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="32260-116">Fargene brukes til å utheve jobbene på listesiden for Kanban-tidsplan eller Kanban-prosesstavlen.</span><span class="sxs-lookup"><span data-stu-id="32260-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="32260-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32260-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="32260-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32260-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="32260-119">Tilknytte produkt</span><span class="sxs-lookup"><span data-stu-id="32260-119">Associate product</span></span>
1. <span data-ttu-id="32260-120">Tilknytte et bestemt produkt</span><span class="sxs-lookup"><span data-stu-id="32260-120">Associate a specific product</span></span>
    * <span data-ttu-id="32260-121">Produkter kan knyttes til lean-planleggingsgrupper på to måter. Enten som et bestemt produkt (varerelasjonstype = vare) eller som en del av en varefordelingsnøkkel (varerelasjonstype = gruppe).</span><span class="sxs-lookup"><span data-stu-id="32260-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="32260-122">Velg Vare i feltet Type varerelasjon</span><span class="sxs-lookup"><span data-stu-id="32260-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="32260-123">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="32260-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="32260-124">Angi et tall i feltet Produksjonsforhold.</span><span class="sxs-lookup"><span data-stu-id="32260-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="32260-125">Standard produksjonsforhold er 1, som betyr at de tilknyttede produktene forbruker nøyaktig den kapasiteten som er angitt i prosessaktivitetene for produksjonsflytene.</span><span class="sxs-lookup"><span data-stu-id="32260-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="32260-126">Produksjonsforhold > 1 definerer en høyere ressursforbruk, Produksjonsforhold < 1 definerer en lavere ressursforbruk.</span><span class="sxs-lookup"><span data-stu-id="32260-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="32260-127">Forholdet brukes i kostnadsberegningen og i beregningen av Kanban-jobbforbruket.</span><span class="sxs-lookup"><span data-stu-id="32260-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="32260-128">Tilknytte varefordelingsnøkkel</span><span class="sxs-lookup"><span data-stu-id="32260-128">Associate item allocation key</span></span>
1. <span data-ttu-id="32260-129">Tilknytte en varefordelingsnøkkel</span><span class="sxs-lookup"><span data-stu-id="32260-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="32260-130">Legg til en tilknytning i en varetildelingsnøkkel ved hjelp av varerelasjonstypen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="32260-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="32260-131">Legg merke til at for denne prosessen må du ha en en varefordelingsnøkkel for prognose definert i dataene.</span><span class="sxs-lookup"><span data-stu-id="32260-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="32260-132">Velg Gruppe i feltet Type varerelasjon</span><span class="sxs-lookup"><span data-stu-id="32260-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="32260-133">Klikk rullegardinknappen i feltet Varefordelingsnøkkel for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="32260-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="32260-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32260-134">In the list, click the link in the selected row.</span></span>


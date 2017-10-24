--- 
title: 'Ferdigmelde til en skiltkontrollert lokasjon '
description: "Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert."
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 34fac03a0ff3d71a2349b66f8f85e4e124dcd708
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a><span data-ttu-id="bb3d3-103">Ferdigmelde til en skiltkontrollert lokasjon </span><span class="sxs-lookup"><span data-stu-id="bb3d3-103">Report as finished to a plate-controlled location</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb3d3-104">Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="bb3d3-105">En gjeldende arbeidspolicy er en forutsetning for denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="bb3d3-106">En tidligere oppgaveveiledning viste oppsettet av arbeidspolicyen.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="bb3d3-107">Denne oppgaveveiledningen krever Dynamics AX 7.0.1 eller senere.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="bb3d3-108">Definere en utleveringslokasjon</span><span class="sxs-lookup"><span data-stu-id="bb3d3-108">Set up an output location</span></span>
1. <span data-ttu-id="bb3d3-109">Gå til Organisasjonsstyring > Ressurser > Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="bb3d3-110">Velg ressursgruppe 5102 i listen.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="bb3d3-111">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-111">Click Edit.</span></span>
4. <span data-ttu-id="bb3d3-112">Angi 51 i feltet Utleveringslager.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="bb3d3-113">Angi 001 i feltet Utleveringslokasjon.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="bb3d3-114">Lokasjonen 001 er ikke en nummerskiltkontrollert lokasjon.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="bb3d3-115">Du kan definere en utleveringslokasjon uten nummerskilt hvis det finnes en gjeldende arbeidspolicy for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="bb3d3-116">Opprette en produksjonsordre og rapportere den som avsluttet</span><span class="sxs-lookup"><span data-stu-id="bb3d3-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="bb3d3-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-117">Close the page.</span></span>
2. <span data-ttu-id="bb3d3-118">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="bb3d3-119">Klikk Ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-119">Click New production order.</span></span>
4. <span data-ttu-id="bb3d3-120">Angi L0101 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="bb3d3-121">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-121">Click Create.</span></span>
6. <span data-ttu-id="bb3d3-122">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="bb3d3-123">Klikk Estimer.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-123">Click Estimate.</span></span>
8. <span data-ttu-id="bb3d3-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-124">Click OK.</span></span>
9. <span data-ttu-id="bb3d3-125">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-125">Click Start.</span></span>
10. <span data-ttu-id="bb3d3-126">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-126">Click the General tab.</span></span>
11. <span data-ttu-id="bb3d3-127">Velg Aldri i feltet Automatisk stykklisteforbruk.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="bb3d3-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-128">Click OK.</span></span>
13. <span data-ttu-id="bb3d3-129">Klikk Rapporter som fullført.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-129">Click Report as finished.</span></span>
14. <span data-ttu-id="bb3d3-130">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-130">Click the General tab.</span></span>
15. <span data-ttu-id="bb3d3-131">Velg Ja i feltet Godtar feil.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="bb3d3-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-132">Click OK.</span></span>
17. <span data-ttu-id="bb3d3-133">Klikk Lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="bb3d3-134">Klikk Arbeidsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-134">Click Work details.</span></span>
    * <span data-ttu-id="bb3d3-135">Når produksjonsordren ble rapportert som fullført, ble det ikke generert arbeid for plassering.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="bb3d3-136">Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet L0101 rapporteres som ferdig til lokasjon 001.</span><span class="sxs-lookup"><span data-stu-id="bb3d3-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  



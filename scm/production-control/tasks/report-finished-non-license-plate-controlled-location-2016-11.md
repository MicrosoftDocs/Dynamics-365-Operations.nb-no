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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a14efeda12cdb677bf9e82f251d1cb91e36337fb
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a><span data-ttu-id="f1395-103">Ferdigmelde til en skiltkontrollert lokasjon </span><span class="sxs-lookup"><span data-stu-id="f1395-103">Report as finished to a plate-controlled location</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1395-104">Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="f1395-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="f1395-105">En gjeldende arbeidspolicy er en forutsetning for denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="f1395-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="f1395-106">En tidligere oppgaveveiledning viste oppsettet av arbeidspolicyen.</span><span class="sxs-lookup"><span data-stu-id="f1395-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="f1395-107">Denne oppgaveveiledningen krever Dynamics AX 7.0.1 eller senere.</span><span class="sxs-lookup"><span data-stu-id="f1395-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="f1395-108">Definere en utleveringslokasjon</span><span class="sxs-lookup"><span data-stu-id="f1395-108">Set up an output location</span></span>
1. <span data-ttu-id="f1395-109">Gå til Organisasjonsstyring > Ressurser > Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="f1395-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="f1395-110">Velg ressursgruppe 5102 i listen.</span><span class="sxs-lookup"><span data-stu-id="f1395-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="f1395-111">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="f1395-111">Click Edit.</span></span>
4. <span data-ttu-id="f1395-112">Angi 51 i feltet Utleveringslager.</span><span class="sxs-lookup"><span data-stu-id="f1395-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="f1395-113">Angi 001 i feltet Utleveringslokasjon.</span><span class="sxs-lookup"><span data-stu-id="f1395-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="f1395-114">Lokasjonen 001 er ikke en nummerskiltkontrollert lokasjon.</span><span class="sxs-lookup"><span data-stu-id="f1395-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="f1395-115">Du kan definere en utleveringslokasjon uten nummerskilt hvis det finnes en gjeldende arbeidspolicy for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="f1395-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="f1395-116">Opprette en produksjonsordre og rapportere den som avsluttet</span><span class="sxs-lookup"><span data-stu-id="f1395-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="f1395-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f1395-117">Close the page.</span></span>
2. <span data-ttu-id="f1395-118">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="f1395-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="f1395-119">Klikk Ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="f1395-119">Click New production order.</span></span>
4. <span data-ttu-id="f1395-120">Angi L0101 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="f1395-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="f1395-121">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="f1395-121">Click Create.</span></span>
6. <span data-ttu-id="f1395-122">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f1395-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="f1395-123">Klikk Estimer.</span><span class="sxs-lookup"><span data-stu-id="f1395-123">Click Estimate.</span></span>
8. <span data-ttu-id="f1395-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1395-124">Click OK.</span></span>
9. <span data-ttu-id="f1395-125">Klikk Start.</span><span class="sxs-lookup"><span data-stu-id="f1395-125">Click Start.</span></span>
10. <span data-ttu-id="f1395-126">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="f1395-126">Click the General tab.</span></span>
11. <span data-ttu-id="f1395-127">Velg Aldri i feltet Automatisk stykklisteforbruk.</span><span class="sxs-lookup"><span data-stu-id="f1395-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="f1395-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1395-128">Click OK.</span></span>
13. <span data-ttu-id="f1395-129">Klikk Rapporter som fullført.</span><span class="sxs-lookup"><span data-stu-id="f1395-129">Click Report as finished.</span></span>
14. <span data-ttu-id="f1395-130">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="f1395-130">Click the General tab.</span></span>
15. <span data-ttu-id="f1395-131">Velg Ja i feltet Godtar feil.</span><span class="sxs-lookup"><span data-stu-id="f1395-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="f1395-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1395-132">Click OK.</span></span>
17. <span data-ttu-id="f1395-133">Klikk Lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f1395-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="f1395-134">Klikk Arbeidsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="f1395-134">Click Work details.</span></span>
    * <span data-ttu-id="f1395-135">Når produksjonsordren ble rapportert som fullført, ble det ikke generert arbeid for plassering.</span><span class="sxs-lookup"><span data-stu-id="f1395-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="f1395-136">Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet L0101 rapporteres som ferdig til lokasjon 001.</span><span class="sxs-lookup"><span data-stu-id="f1395-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  



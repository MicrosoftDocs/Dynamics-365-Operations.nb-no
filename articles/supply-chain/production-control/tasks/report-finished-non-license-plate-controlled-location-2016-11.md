---
title: Rapportere som ferdig til en lokasjon som ikke er kontrollert av nummerskilt (program, mai 2016)
description: Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9aeac631e32876d6c19cb964f28e65491137049a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204502"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="b4380-103">Rapportere som ferdig til en lokasjon som ikke er kontrollert av nummerskilt (program, mai 2016)</span><span class="sxs-lookup"><span data-stu-id="b4380-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4380-104">Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="b4380-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="b4380-105">En gjeldende arbeidspolicy er en forutsetning for denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="b4380-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="b4380-106">En tidligere oppgaveveiledning viste oppsettet av arbeidspolicyen.</span><span class="sxs-lookup"><span data-stu-id="b4380-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="b4380-107">Denne oppgaveveiledningen krever Dynamics AX 7.0.1 eller senere.</span><span class="sxs-lookup"><span data-stu-id="b4380-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="b4380-108">Definere en utleveringslokasjon</span><span class="sxs-lookup"><span data-stu-id="b4380-108">Set up an output location</span></span>
1. <span data-ttu-id="b4380-109">Gå til Organisasjonsstyring > Ressurser > Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="b4380-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="b4380-110">Velg ressursgruppe 5102 i listen.</span><span class="sxs-lookup"><span data-stu-id="b4380-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="b4380-111">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="b4380-111">Click Edit.</span></span>
4. <span data-ttu-id="b4380-112">Angi 51 i feltet Utleveringslager.</span><span class="sxs-lookup"><span data-stu-id="b4380-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="b4380-113">Angi 001 i feltet Utleveringslokasjon.</span><span class="sxs-lookup"><span data-stu-id="b4380-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="b4380-114">Lokasjonen 001 er ikke en nummerskiltkontrollert lokasjon.</span><span class="sxs-lookup"><span data-stu-id="b4380-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="b4380-115">Du kan definere en utleveringslokasjon uten nummerskilt hvis det finnes en gjeldende arbeidspolicy for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="b4380-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="b4380-116">Opprette en produksjonsordre og rapportere den som avsluttet</span><span class="sxs-lookup"><span data-stu-id="b4380-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="b4380-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b4380-117">Close the page.</span></span>
2. <span data-ttu-id="b4380-118">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="b4380-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="b4380-119">Klikk på Ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="b4380-119">Click New production order.</span></span>
4. <span data-ttu-id="b4380-120">Angi L0101 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="b4380-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="b4380-121">Klikk på Opprett.</span><span class="sxs-lookup"><span data-stu-id="b4380-121">Click Create.</span></span>
6. <span data-ttu-id="b4380-122">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4380-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="b4380-123">Klikk på Estimer.</span><span class="sxs-lookup"><span data-stu-id="b4380-123">Click Estimate.</span></span>
8. <span data-ttu-id="b4380-124">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="b4380-124">Click OK.</span></span>
9. <span data-ttu-id="b4380-125">Klikk på Start.</span><span class="sxs-lookup"><span data-stu-id="b4380-125">Click Start.</span></span>
10. <span data-ttu-id="b4380-126">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="b4380-126">Click the General tab.</span></span>
11. <span data-ttu-id="b4380-127">Velg Aldri i feltet Automatisk stykklisteforbruk.</span><span class="sxs-lookup"><span data-stu-id="b4380-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="b4380-128">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="b4380-128">Click OK.</span></span>
13. <span data-ttu-id="b4380-129">Klikk på Rapporter som fullført.</span><span class="sxs-lookup"><span data-stu-id="b4380-129">Click Report as finished.</span></span>
14. <span data-ttu-id="b4380-130">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="b4380-130">Click the General tab.</span></span>
15. <span data-ttu-id="b4380-131">Velg Ja i feltet Godtar feil.</span><span class="sxs-lookup"><span data-stu-id="b4380-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="b4380-132">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="b4380-132">Click OK.</span></span>
17. <span data-ttu-id="b4380-133">Klikk på Lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b4380-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="b4380-134">Klikk på Arbeidsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="b4380-134">Click Work details.</span></span>
    * <span data-ttu-id="b4380-135">Når produksjonsordren ble rapportert som fullført, ble det ikke generert arbeid for plassering.</span><span class="sxs-lookup"><span data-stu-id="b4380-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="b4380-136">Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet L0101 rapporteres som ferdig til lokasjon 001.</span><span class="sxs-lookup"><span data-stu-id="b4380-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
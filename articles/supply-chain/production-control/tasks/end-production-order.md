---
title: Avslutte en produksjonsordre
description: "Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9cb20294e4abbccd0016e7188a2610796e75b26
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="end-a-production-order"></a><span data-ttu-id="e46fd-103">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="e46fd-103">End a production order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e46fd-104">Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="e46fd-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="e46fd-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e46fd-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e46fd-106">Dette er den siste fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="e46fd-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="e46fd-107">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="e46fd-107">End a production order</span></span>
1. <span data-ttu-id="e46fd-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="e46fd-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="e46fd-109">Velg en produksjonsordre med statusen Ferdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="e46fd-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="e46fd-110">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e46fd-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="e46fd-111">Klikk Avslutt.</span><span class="sxs-lookup"><span data-stu-id="e46fd-111">Click End.</span></span>
    * <span data-ttu-id="e46fd-112">På denne siden kan du bekrefte at du vil avslutte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="e46fd-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="e46fd-113">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="e46fd-113">Click the General tab.</span></span>
5. <span data-ttu-id="e46fd-114">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="e46fd-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="e46fd-115">Velg "Tildeling" i feltet Svinnmetode.</span><span class="sxs-lookup"><span data-stu-id="e46fd-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="e46fd-116">Når du velger metoden Tildeling, legges kostnadene fra de kasserte materialene til de ferdige varene.</span><span class="sxs-lookup"><span data-stu-id="e46fd-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="e46fd-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e46fd-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="e46fd-118">Validere beregningsresultater</span><span class="sxs-lookup"><span data-stu-id="e46fd-118">Validate calculation results</span></span>
1. <span data-ttu-id="e46fd-119">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e46fd-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="e46fd-120">Klikk Vis kostnadssammenligning.</span><span class="sxs-lookup"><span data-stu-id="e46fd-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="e46fd-121">Når du har avsluttet produksjonsordren, kan du sammenligne den estimerte kostprisen mot den realiserte kostprisen for å få en oversikt over produksjonsavvikene.</span><span class="sxs-lookup"><span data-stu-id="e46fd-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  


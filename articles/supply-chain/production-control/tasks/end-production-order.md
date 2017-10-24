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
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 75b91ea330258a5b57e9e58cb32539d57e458f28
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="end-a-production-order"></a><span data-ttu-id="3f55c-103">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="3f55c-103">End a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f55c-104">Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="3f55c-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="3f55c-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3f55c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3f55c-106">Dette er den siste fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="3f55c-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="3f55c-107">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="3f55c-107">End a production order</span></span>
1. <span data-ttu-id="3f55c-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="3f55c-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="3f55c-109">Velg en produksjonsordre med statusen Ferdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="3f55c-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="3f55c-110">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3f55c-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="3f55c-111">Klikk Avslutt.</span><span class="sxs-lookup"><span data-stu-id="3f55c-111">Click End.</span></span>
    * <span data-ttu-id="3f55c-112">På denne siden kan du bekrefte at du vil avslutte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="3f55c-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="3f55c-113">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="3f55c-113">Click the General tab.</span></span>
5. <span data-ttu-id="3f55c-114">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="3f55c-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="3f55c-115">Velg "Tildeling" i feltet Svinnmetode.</span><span class="sxs-lookup"><span data-stu-id="3f55c-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="3f55c-116">Når du velger metoden Tildeling, legges kostnadene fra de kasserte materialene til de ferdige varene.</span><span class="sxs-lookup"><span data-stu-id="3f55c-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="3f55c-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3f55c-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="3f55c-118">Validere beregningsresultater</span><span class="sxs-lookup"><span data-stu-id="3f55c-118">Validate calculation results</span></span>
1. <span data-ttu-id="3f55c-119">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3f55c-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="3f55c-120">Klikk Vis kostnadssammenligning.</span><span class="sxs-lookup"><span data-stu-id="3f55c-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="3f55c-121">Når du har avsluttet produksjonsordren, kan du sammenligne den estimerte kostprisen mot den realiserte kostprisen for å få en oversikt over produksjonsavvikene.</span><span class="sxs-lookup"><span data-stu-id="3f55c-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  



---
title: Avslutte en produksjonsordre
description: Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f3e121fdc0f69ace15e0fa08bde0af739ef7d28
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977819"
---
# <a name="end-a-production-order"></a><span data-ttu-id="631a0-103">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="631a0-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="631a0-104">Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="631a0-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="631a0-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="631a0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="631a0-106">Dette er den siste fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="631a0-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="631a0-107">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="631a0-107">End a production order</span></span>
1. <span data-ttu-id="631a0-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="631a0-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="631a0-109">Velg en produksjonsordre med statusen Ferdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="631a0-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="631a0-110">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="631a0-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="631a0-111">Klikk på Avslutt.</span><span class="sxs-lookup"><span data-stu-id="631a0-111">Click End.</span></span>
    * <span data-ttu-id="631a0-112">På denne siden kan du bekrefte at du vil avslutte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="631a0-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="631a0-113">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="631a0-113">Click the General tab.</span></span>
5. <span data-ttu-id="631a0-114">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="631a0-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="631a0-115">Velg "Tildeling" i feltet Svinnmetode.</span><span class="sxs-lookup"><span data-stu-id="631a0-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="631a0-116">Når du velger metoden Tildeling, legges kostnadene fra de kasserte materialene til de ferdige varene.</span><span class="sxs-lookup"><span data-stu-id="631a0-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="631a0-117">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="631a0-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="631a0-118">Validere beregningsresultater</span><span class="sxs-lookup"><span data-stu-id="631a0-118">Validate calculation results</span></span>
1. <span data-ttu-id="631a0-119">Klikk på Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="631a0-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="631a0-120">Klikk på Vis kostnadssammenligning.</span><span class="sxs-lookup"><span data-stu-id="631a0-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="631a0-121">Når du har avsluttet produksjonsordren, kan du sammenligne den estimerte kostprisen mot den realiserte kostprisen for å få en oversikt over produksjonsavvikene.</span><span class="sxs-lookup"><span data-stu-id="631a0-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  

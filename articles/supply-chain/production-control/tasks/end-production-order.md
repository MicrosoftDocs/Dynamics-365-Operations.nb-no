---
title: Avslutte en produksjonsordre
description: Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 577b026c950885524b726b09eb4df1ee7cf06837
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828688"
---
# <a name="end-a-production-order"></a><span data-ttu-id="d37dd-103">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="d37dd-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d37dd-104">Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="d37dd-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="d37dd-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d37dd-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d37dd-106">Dette er den siste fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="d37dd-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="d37dd-107">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="d37dd-107">End a production order</span></span>
1. <span data-ttu-id="d37dd-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="d37dd-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="d37dd-109">Velg en produksjonsordre med statusen Ferdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="d37dd-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="d37dd-110">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d37dd-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="d37dd-111">Klikk på Avslutt.</span><span class="sxs-lookup"><span data-stu-id="d37dd-111">Click End.</span></span>
    * <span data-ttu-id="d37dd-112">På denne siden kan du bekrefte at du vil avslutte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="d37dd-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="d37dd-113">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="d37dd-113">Click the General tab.</span></span>
5. <span data-ttu-id="d37dd-114">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="d37dd-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="d37dd-115">Velg "Tildeling" i feltet Svinnmetode.</span><span class="sxs-lookup"><span data-stu-id="d37dd-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="d37dd-116">Når du velger metoden Tildeling, legges kostnadene fra de kasserte materialene til de ferdige varene.</span><span class="sxs-lookup"><span data-stu-id="d37dd-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="d37dd-117">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="d37dd-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="d37dd-118">Validere beregningsresultater</span><span class="sxs-lookup"><span data-stu-id="d37dd-118">Validate calculation results</span></span>
1. <span data-ttu-id="d37dd-119">Klikk på Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d37dd-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="d37dd-120">Klikk på Vis kostnadssammenligning.</span><span class="sxs-lookup"><span data-stu-id="d37dd-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="d37dd-121">Når du har avsluttet produksjonsordren, kan du sammenligne den estimerte kostprisen mot den realiserte kostprisen for å få en oversikt over produksjonsavvikene.</span><span class="sxs-lookup"><span data-stu-id="d37dd-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
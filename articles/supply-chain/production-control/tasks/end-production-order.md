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
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434107"
---
# <a name="end-a-production-order"></a><span data-ttu-id="03f08-103">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="03f08-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03f08-104">Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="03f08-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="03f08-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="03f08-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="03f08-106">Dette er den siste fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="03f08-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="03f08-107">Avslutte en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="03f08-107">End a production order</span></span>
1. <span data-ttu-id="03f08-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="03f08-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="03f08-109">Velg en produksjonsordre med statusen Ferdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="03f08-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="03f08-110">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="03f08-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="03f08-111">Klikk Avslutt.</span><span class="sxs-lookup"><span data-stu-id="03f08-111">Click End.</span></span>
    * <span data-ttu-id="03f08-112">På denne siden kan du bekrefte at du vil avslutte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="03f08-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="03f08-113">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="03f08-113">Click the General tab.</span></span>
5. <span data-ttu-id="03f08-114">Angi en dato i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="03f08-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="03f08-115">Velg "Tildeling" i feltet Svinnmetode.</span><span class="sxs-lookup"><span data-stu-id="03f08-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="03f08-116">Når du velger metoden Tildeling, legges kostnadene fra de kasserte materialene til de ferdige varene.</span><span class="sxs-lookup"><span data-stu-id="03f08-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="03f08-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="03f08-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="03f08-118">Validere beregningsresultater</span><span class="sxs-lookup"><span data-stu-id="03f08-118">Validate calculation results</span></span>
1. <span data-ttu-id="03f08-119">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="03f08-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="03f08-120">Klikk Vis kostnadssammenligning.</span><span class="sxs-lookup"><span data-stu-id="03f08-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="03f08-121">Når du har avsluttet produksjonsordren, kan du sammenligne den estimerte kostprisen mot den realiserte kostprisen for å få en oversikt over produksjonsavvikene.</span><span class="sxs-lookup"><span data-stu-id="03f08-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  

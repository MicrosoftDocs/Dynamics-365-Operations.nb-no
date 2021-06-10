---
title: Opprette en plan for et område
description: Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d84fcd0012d4f7d87e2bc0769261fbe5f5139670
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102668"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="729dd-103">Opprette en plan for et område</span><span class="sxs-lookup"><span data-stu-id="729dd-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="729dd-104">Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="729dd-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="729dd-105">Når forespørselsforslagene er opprettet, finner vedkommende ordrene på området som planlegges, og bekrefter ordrene, fra og med de som haster.</span><span class="sxs-lookup"><span data-stu-id="729dd-105">After the sourcing suggestions are created, they find the orders at the site for which they are planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="729dd-106">De viktigste ordrene er de som skal bekreftes på gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="729dd-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="729dd-107">Bruk USMF-demodatafirmaet til å utføre disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="729dd-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="729dd-108">Opprette en material- og kapasitetsplan for en vare</span><span class="sxs-lookup"><span data-stu-id="729dd-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="729dd-109">Klikk på Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="729dd-109">Click Master planning.</span></span>
    * <span data-ttu-id="729dd-110">Du må gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="729dd-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="729dd-111">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="729dd-111">Click Run.</span></span>
3. <span data-ttu-id="729dd-112">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="729dd-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="729dd-113">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="729dd-113">Click Filter.</span></span>
5. <span data-ttu-id="729dd-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="729dd-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="729dd-115">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="729dd-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="729dd-116">Eksempel: D0001</span><span class="sxs-lookup"><span data-stu-id="729dd-116">Example: D0001</span></span>  
7. <span data-ttu-id="729dd-117">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="729dd-117">Click OK.</span></span>
8. <span data-ttu-id="729dd-118">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="729dd-118">Click OK.</span></span>
    * <span data-ttu-id="729dd-119">Dette kan ta noen minutter.</span><span class="sxs-lookup"><span data-stu-id="729dd-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="729dd-120">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="729dd-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="729dd-121">Identifisere viktige planlagte bestillinger for varen</span><span class="sxs-lookup"><span data-stu-id="729dd-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="729dd-122">Åpne kolonnefilter for varenummer.</span><span class="sxs-lookup"><span data-stu-id="729dd-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="729dd-123">Bruk et filter på feltet "Varenummer" , med verdien "D0001", ved hjelp av filteroperatoren "begynner med".</span><span class="sxs-lookup"><span data-stu-id="729dd-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="729dd-124">Åpne kolonnefilteret Bestillingsdato.</span><span class="sxs-lookup"><span data-stu-id="729dd-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="729dd-125">Bruke et filter i feltet "Bestillingsdato" med en verdi for gjeldende dato, ved hjelp av filteroperatoren "er nøyaktig".</span><span class="sxs-lookup"><span data-stu-id="729dd-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="729dd-126">Bekrefte alle viktige bestillinger for varen</span><span class="sxs-lookup"><span data-stu-id="729dd-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="729dd-127">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="729dd-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="729dd-128">Klikk på Bekreft.</span><span class="sxs-lookup"><span data-stu-id="729dd-128">Click Firm.</span></span>
3. <span data-ttu-id="729dd-129">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="729dd-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
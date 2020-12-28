---
title: Opprette en plan for et område
description: Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52721d948554d4853f9e1d4dec45e45e619a4829
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434426"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="3850d-103">Opprette en plan for et område</span><span class="sxs-lookup"><span data-stu-id="3850d-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3850d-104">Produksjonsplanleggeren beregner material- og kapasitetsbehovene for produksjonen av en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="3850d-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="3850d-105">Når du har opprettet forespørselsforslagene, finner han ordrene på området som han planlegger og bekrefter ordrene, fra de som haster.</span><span class="sxs-lookup"><span data-stu-id="3850d-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="3850d-106">De viktigste ordrene er de som skal bekreftes på gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="3850d-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="3850d-107">Bruk USMF-demodatafirmaet til å utføre disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="3850d-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="3850d-108">Opprette en material- og kapasitetsplan for en vare</span><span class="sxs-lookup"><span data-stu-id="3850d-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="3850d-109">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="3850d-109">Click Master planning.</span></span>
    * <span data-ttu-id="3850d-110">Du må gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="3850d-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="3850d-111">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="3850d-111">Click Run.</span></span>
3. <span data-ttu-id="3850d-112">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="3850d-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="3850d-113">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="3850d-113">Click Filter.</span></span>
5. <span data-ttu-id="3850d-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3850d-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="3850d-115">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="3850d-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3850d-116">Eksempel: D0001</span><span class="sxs-lookup"><span data-stu-id="3850d-116">Example: D0001</span></span>  
7. <span data-ttu-id="3850d-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3850d-117">Click OK.</span></span>
8. <span data-ttu-id="3850d-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3850d-118">Click OK.</span></span>
    * <span data-ttu-id="3850d-119">Dette kan ta noen minutter.</span><span class="sxs-lookup"><span data-stu-id="3850d-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="3850d-120">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="3850d-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="3850d-121">Identifisere viktige planlagte bestillinger for varen</span><span class="sxs-lookup"><span data-stu-id="3850d-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="3850d-122">Åpne kolonnefilter for varenummer.</span><span class="sxs-lookup"><span data-stu-id="3850d-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="3850d-123">Bruk et filter på feltet "Varenummer" , med verdien "D0001", ved hjelp av filteroperatoren "begynner med".</span><span class="sxs-lookup"><span data-stu-id="3850d-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="3850d-124">Åpne kolonnefilteret Bestillingsdato.</span><span class="sxs-lookup"><span data-stu-id="3850d-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="3850d-125">Bruke et filter i feltet "Bestillingsdato" med en verdi for gjeldende dato, ved hjelp av filteroperatoren "er nøyaktig".</span><span class="sxs-lookup"><span data-stu-id="3850d-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="3850d-126">Bekrefte alle viktige bestillinger for varen</span><span class="sxs-lookup"><span data-stu-id="3850d-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="3850d-127">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="3850d-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="3850d-128">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="3850d-128">Click Firm.</span></span>
3. <span data-ttu-id="3850d-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3850d-129">Click OK.</span></span>


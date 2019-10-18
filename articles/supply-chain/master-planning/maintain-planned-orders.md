---
title: Vedlikeholde planlagte ordrer
description: Dette emnet gir informasjon om hvordan du behandler planlagte ordrer. Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993446"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="5d628-104">Vedlikeholde planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="5d628-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d628-105">Dette emnet gir informasjon om hvordan du behandler planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="5d628-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="5d628-106">Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="5d628-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="5d628-107">Du kan administrere planlagte bestillinger fra arbeidsområdet **Hovedplanlegging**, listen **Planlagt bestilling** eller listene **Planlagte produksjonsordrer**, **Planlagte bestillinger** og **Overføringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="5d628-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="5d628-108">Status for planlagt ordre</span><span class="sxs-lookup"><span data-stu-id="5d628-108">Planned order status</span></span>
<span data-ttu-id="5d628-109">Du kan bruke **Status**-feltet til å spore fremdriften.</span><span class="sxs-lookup"><span data-stu-id="5d628-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="5d628-110">Følgende verdier brukes:</span><span class="sxs-lookup"><span data-stu-id="5d628-110">The following values are used:</span></span>

-   <span data-ttu-id="5d628-111">Når hovedplanlegging genererer planlagte ordrer, har de planlagte ordrene statusen **Ubehandlet**.</span><span class="sxs-lookup"><span data-stu-id="5d628-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="5d628-112">Hvis du velger ikke å autorisere en planlagt bestilling, kan du gi den statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="5d628-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="5d628-113">Hvis du vil autorisere en planlagt ordre, kan du endre statusen til **Godkjent**.</span><span class="sxs-lookup"><span data-stu-id="5d628-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="5d628-114">Planlagte ordrer med **Godkjent**-status overholdes av hovedplanlegging, slik at de ikke blir endret eller slettet.</span><span class="sxs-lookup"><span data-stu-id="5d628-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="5d628-115">Autorisere planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="5d628-115">Firming planned orders</span></span> 
<span data-ttu-id="5d628-116">Ved å autorisere planlagte ordre opprettes det reelle ordrer.</span><span class="sxs-lookup"><span data-stu-id="5d628-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="5d628-117">Disse kalles også *frigitte* eller *åpne ordrer*.</span><span class="sxs-lookup"><span data-stu-id="5d628-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="5d628-118">Når en planlagt bestilling autoriseres, flyttes den til bestillingsdelen i den aktuelle modulen.</span><span class="sxs-lookup"><span data-stu-id="5d628-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="5d628-119">Du kan velge to autorisasjonsalternativer fra siden **Planlagte ordrer**:</span><span class="sxs-lookup"><span data-stu-id="5d628-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="5d628-120">**Autoriser** – Dette vil autorisere én eller flere valgte, planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="5d628-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="5d628-121">**Autoriser alle** – Dette vil autorisere alle planlagte ordrer i filteret.</span><span class="sxs-lookup"><span data-stu-id="5d628-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="5d628-122">Hvis du bruker **Autoriser alle** trenger du ikke velge den planlagte ordren. Alle planlagte ordrer i filteret bli autorisert.</span><span class="sxs-lookup"><span data-stu-id="5d628-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="5d628-123">Dette alternativet kan være nyttig hvis du autoriserer et stort antall planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="5d628-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="5d628-124">Du kan spore en planlagt ordre som ble autorisert fra **Autorisasjonshistorikk** under **skjemaet Planlagte ordrer > Vis > Autorisasjonshistorikk**.</span><span class="sxs-lookup"><span data-stu-id="5d628-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="5d628-125">Parallelliser autorisasjon</span><span class="sxs-lookup"><span data-stu-id="5d628-125">Parallelize firming</span></span>
<span data-ttu-id="5d628-126">Hvis du planlegger å autorisere mange ordrer samtidig, kan parallellisering av kjøringen forbedre kjøretiden eller ytelsen.</span><span class="sxs-lookup"><span data-stu-id="5d628-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="5d628-127">Dette alternativet er tilgjengelig ved autorisering av flere planlagte orderer med **Autoriser** eller **Autoriser alle**.</span><span class="sxs-lookup"><span data-stu-id="5d628-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="5d628-128">Følgende parametere er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="5d628-128">The following parameters are available:</span></span>

-   <span data-ttu-id="5d628-129">**Parallellisering av autorisering** – Hvis **Ja**, vil autoriseringsprosessen parallelliseres med antallet tråder som er definert i **Antall tråder**.</span><span class="sxs-lookup"><span data-stu-id="5d628-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="5d628-130">**Antall tråder** – Bestemmer antall tråder som brukes til å parallellisere autoriseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="5d628-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="5d628-131">Parameteren vises bare når **Parallellisering av autorisering** er satt til **Ja.**</span><span class="sxs-lookup"><span data-stu-id="5d628-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="5d628-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5d628-132">Additional resources</span></span>
--------

[<span data-ttu-id="5d628-133">Hovedplaner</span><span class="sxs-lookup"><span data-stu-id="5d628-133">Master plans</span></span>](master-plans.md)




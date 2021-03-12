---
title: Vedlikeholde planlagte ordrer
description: Dette emnet gir informasjon om hvordan du behandler planlagte ordrer. Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 039fce86ac9649989df1eaa6179c79dd98b8ae3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967078"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="6fab4-104">Vedlikeholde planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="6fab4-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fab4-105">Dette emnet gir informasjon om hvordan du behandler planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="6fab4-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="6fab4-106">Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="6fab4-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="6fab4-107">Du kan administrere planlagte bestillinger fra arbeidsområdet **Hovedplanlegging**, listen **Planlagt bestilling** eller listene **Planlagte produksjonsordrer**, **Planlagte bestillinger** og **Overføringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="6fab4-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="6fab4-108">Status for planlagt ordre</span><span class="sxs-lookup"><span data-stu-id="6fab4-108">Planned order status</span></span>
<span data-ttu-id="6fab4-109">Du kan bruke **Status**-feltet til å spore fremdriften.</span><span class="sxs-lookup"><span data-stu-id="6fab4-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="6fab4-110">Følgende verdier brukes:</span><span class="sxs-lookup"><span data-stu-id="6fab4-110">The following values are used:</span></span>

-   <span data-ttu-id="6fab4-111">Når hovedplanlegging genererer planlagte ordrer, har de planlagte ordrene statusen **Ubehandlet**.</span><span class="sxs-lookup"><span data-stu-id="6fab4-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="6fab4-112">Hvis du velger ikke å autorisere en planlagt bestilling, kan du gi den statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="6fab4-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="6fab4-113">Hvis du vil autorisere en planlagt ordre, kan du endre statusen til **Godkjent**.</span><span class="sxs-lookup"><span data-stu-id="6fab4-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="6fab4-114">Planlagte ordrer med **Godkjent**-status overholdes av hovedplanlegging, slik at de ikke blir endret eller slettet under en senere kjøring av hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="6fab4-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="6fab4-115">For å oppnå dette kopierer planleggingslogikken de **godkjente** planlagte bestillingene fra den gamle planversjonen til den nye planversjonen under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="6fab4-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="6fab4-116">Autorisere planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="6fab4-116">Firming planned orders</span></span> 
<span data-ttu-id="6fab4-117">Ved å autorisere planlagte ordre opprettes det reelle ordrer.</span><span class="sxs-lookup"><span data-stu-id="6fab4-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="6fab4-118">Disse kalles også *frigitte* eller *åpne ordrer*.</span><span class="sxs-lookup"><span data-stu-id="6fab4-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="6fab4-119">Når en planlagt bestilling autoriseres, flyttes den til bestillingsdelen i den aktuelle modulen.</span><span class="sxs-lookup"><span data-stu-id="6fab4-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="6fab4-120">Du kan velge to autorisasjonsalternativer fra siden **Planlagte ordrer**:</span><span class="sxs-lookup"><span data-stu-id="6fab4-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="6fab4-121">**Autoriser** – Dette vil autorisere én eller flere valgte, planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="6fab4-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="6fab4-122">**Autoriser alle** – Dette vil autorisere alle planlagte ordrer i filteret.</span><span class="sxs-lookup"><span data-stu-id="6fab4-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="6fab4-123">Hvis du bruker **Autoriser alle** trenger du ikke velge den planlagte ordren. Alle planlagte ordrer i filteret bli autorisert.</span><span class="sxs-lookup"><span data-stu-id="6fab4-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="6fab4-124">Dette alternativet kan være nyttig hvis du autoriserer et stort antall planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="6fab4-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="6fab4-125">Du kan spore en planlagt ordre som ble autorisert fra **Autorisasjonshistorikk** under **skjemaet Planlagte ordrer > Vis > Autorisasjonshistorikk**.</span><span class="sxs-lookup"><span data-stu-id="6fab4-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="6fab4-126">Parallelliser autorisasjon</span><span class="sxs-lookup"><span data-stu-id="6fab4-126">Parallelize firming</span></span>
<span data-ttu-id="6fab4-127">Hvis du planlegger å autorisere mange ordrer samtidig, kan parallellisering av kjøringen forbedre kjøretiden eller ytelsen.</span><span class="sxs-lookup"><span data-stu-id="6fab4-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="6fab4-128">Dette alternativet er tilgjengelig ved autorisering av flere planlagte orderer med **Autoriser** eller **Autoriser alle**.</span><span class="sxs-lookup"><span data-stu-id="6fab4-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="6fab4-129">Følgende parametere er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="6fab4-129">The following parameters are available:</span></span>

-   <span data-ttu-id="6fab4-130">**Parallellisering av autorisering** – Hvis **Ja**, vil autoriseringsprosessen parallelliseres med antallet tråder som er definert i **Antall tråder**.</span><span class="sxs-lookup"><span data-stu-id="6fab4-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="6fab4-131">**Antall tråder** – Bestemmer antall tråder som brukes til å parallellisere autoriseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="6fab4-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="6fab4-132">Parameteren vises bare når **Parallellisering av autorisering** er satt til **Ja.**</span><span class="sxs-lookup"><span data-stu-id="6fab4-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="6fab4-133">Alternativet for **Parallelliser autorisasjon** vises bare når du har mer enn én planlagt bestilling som er valgt for autorisasjon.</span><span class="sxs-lookup"><span data-stu-id="6fab4-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6fab4-134">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6fab4-134">Additional resources</span></span>
--------

[<span data-ttu-id="6fab4-135">Oversikt over hovedplaner</span><span class="sxs-lookup"><span data-stu-id="6fab4-135">Master plans overview</span></span>](master-plans.md)




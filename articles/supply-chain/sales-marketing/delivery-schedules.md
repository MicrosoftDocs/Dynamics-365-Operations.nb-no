---
title: Leveringsplaner
description: Med leveringsplaner kan du spore ordrelinjeantallet når du bruker flere leveringer for en enkelt salgsordre, et salgstilbud eller en bestilling.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfc9467e6c7df70ce749f531bab447513ea3349e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998584"
---
# <a name="delivery-schedules"></a><span data-ttu-id="54d4f-103">Leveringsplaner</span><span class="sxs-lookup"><span data-stu-id="54d4f-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54d4f-104">Med leveringsplaner kan du spore ordrelinjeantallet når du bruker flere leveringer for en enkelt salgsordre, et salgstilbud eller en bestilling.</span><span class="sxs-lookup"><span data-stu-id="54d4f-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="54d4f-105">Bruk en leveringsplan når det totale antallet i en ordre eller en tilbudslinje må leveres i flere leveranser.</span><span class="sxs-lookup"><span data-stu-id="54d4f-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="54d4f-106">Individuelle forsendelser representeres av leveringslinjer.</span><span class="sxs-lookup"><span data-stu-id="54d4f-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="54d4f-107">To eller flere leveringslinjer utgjør én leveringsplan.</span><span class="sxs-lookup"><span data-stu-id="54d4f-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="54d4f-108">Leveringslinjene kan ha andre leveringsdatoer, antall, leveringsmåter og lagerdimensjoner, for eksempel område og lager.</span><span class="sxs-lookup"><span data-stu-id="54d4f-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="54d4f-109">**Eksempel på en leveringsplan**</span><span class="sxs-lookup"><span data-stu-id="54d4f-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="54d4f-110">Totalbestilling (opprinnelig ordrelinje)</span><span class="sxs-lookup"><span data-stu-id="54d4f-110">Total order (original order line)</span></span> | <span data-ttu-id="54d4f-111">600 stoler</span><span class="sxs-lookup"><span data-stu-id="54d4f-111">600 chairs</span></span>                               |
| <span data-ttu-id="54d4f-112">Ønsket leveringsplan</span><span class="sxs-lookup"><span data-stu-id="54d4f-112">Requested delivery schedule</span></span>       | <span data-ttu-id="54d4f-113">100 stoler per måned</span><span class="sxs-lookup"><span data-stu-id="54d4f-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="54d4f-114">Forespurt tidsramme for levering</span><span class="sxs-lookup"><span data-stu-id="54d4f-114">Requested time frame for delivery</span></span> | <span data-ttu-id="54d4f-115">6 måneder, den første dagen i hver måned</span><span class="sxs-lookup"><span data-stu-id="54d4f-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="54d4f-116">I dette scenariet ber kunden ber om levering av 600 stoler i partier på 100 stoler over en periode på seks måneder.</span><span class="sxs-lookup"><span data-stu-id="54d4f-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="54d4f-117">For å holde oversikt over kravene til levering oppretter du en leveringsplan.</span><span class="sxs-lookup"><span data-stu-id="54d4f-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="54d4f-118">På siden for leveringstidsplan oppretter du seks separate leveringslinjer.</span><span class="sxs-lookup"><span data-stu-id="54d4f-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="54d4f-119">Hver leveringslinje inneholder 100 stoler og angir leveringsdatoen for disse 100 stolene.</span><span class="sxs-lookup"><span data-stu-id="54d4f-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="54d4f-120">I dette tilfellet motposteres hver linje den første dagen i måneden i seks måneder etter hverandre.</span><span class="sxs-lookup"><span data-stu-id="54d4f-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="54d4f-121">Når du oppretter en leveringsplan, endres automatisk den opprinnelige ordrelinjen til **Bestillingslinje med flere leveringer**.</span><span class="sxs-lookup"><span data-stu-id="54d4f-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="54d4f-122">En linje av denne typen kalles en kommersielle linje og merkes med et ikon.</span><span class="sxs-lookup"><span data-stu-id="54d4f-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="54d4f-123">Leveringslinjen er merket med et annet ikon.</span><span class="sxs-lookup"><span data-stu-id="54d4f-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="54d4f-124">Hvis du endrer et antall på en leveringslinje, oppdateres den kommersielle linjen til det totale antallet i leveringsplanen.</span><span class="sxs-lookup"><span data-stu-id="54d4f-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="54d4f-125">Hvis en forretningsavtale har definert en sluttrabatt for ordren, sikrer leveringsplanen at bestillingen er kvalifisert for sluttrabatten, selv om ordren er delt inn i separate leveranser.</span><span class="sxs-lookup"><span data-stu-id="54d4f-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="54d4f-126">Ordrer som har en leveringsplan, behandles mot leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="54d4f-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="54d4f-127">Behandling inkluderer postering av følgesedler, produktkvitteringer og fakturering.</span><span class="sxs-lookup"><span data-stu-id="54d4f-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="54d4f-128">Dokumentutskrifter av ordrer og tilbud som har en leveringsplan, viser bare leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="54d4f-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="54d4f-129">De vises ikke de opprinnelige linjene (kommersielle linjer).</span><span class="sxs-lookup"><span data-stu-id="54d4f-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="54d4f-130">**Merk:** I tillegg vises bare leveringslinjene når du utfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="54d4f-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="54d4f-131">Poster</span><span class="sxs-lookup"><span data-stu-id="54d4f-131">Post</span></span>
-   <span data-ttu-id="54d4f-132">Kopier side</span><span class="sxs-lookup"><span data-stu-id="54d4f-132">Copy pages</span></span>
-   <span data-ttu-id="54d4f-133">Bla gjennom listesider og rapporter</span><span class="sxs-lookup"><span data-stu-id="54d4f-133">Browse list pages and reports</span></span>

<span data-ttu-id="54d4f-134">Når du bekrefter salgstilbud, viser de resulterende salgsordrene hele leveringsplanen, også ordrelinjene som har flere leveringer.</span><span class="sxs-lookup"><span data-stu-id="54d4f-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="54d4f-135">I tillegg vises hele leveringsplanen på alle de viktige sidene, for eksempel salgsordrer, salgstilbud og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="54d4f-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>




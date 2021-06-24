---
title: Leveringsplaner
description: Med leveringsplaner kan du spore ordrelinjeantallet når du bruker flere leveringer for en enkelt salgsordre, et salgstilbud eller en bestilling.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193788"
---
# <a name="delivery-schedules"></a><span data-ttu-id="f2cb9-103">Leveringsplaner</span><span class="sxs-lookup"><span data-stu-id="f2cb9-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2cb9-104">Med leveringsplaner kan du spore ordrelinjeantallet når du bruker flere leveringer for en enkelt salgsordre, et salgstilbud eller en bestilling.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="f2cb9-105">Bruk en leveringsplan når det totale antallet i en ordre eller en tilbudslinje må leveres i flere leveranser.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="f2cb9-106">Individuelle forsendelser representeres av leveringslinjer.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="f2cb9-107">To eller flere leveringslinjer utgjør én leveringsplan.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="f2cb9-108">Leveringslinjene kan ha andre leveringsdatoer, antall, leveringsmåter og lagerdimensjoner, for eksempel område og lager.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="f2cb9-109">**Eksempel på en leveringsplan**</span><span class="sxs-lookup"><span data-stu-id="f2cb9-109">**Example of a delivery schedule**</span></span>

| <span data-ttu-id="f2cb9-110">Element</span><span class="sxs-lookup"><span data-stu-id="f2cb9-110">Item</span></span>                              | <span data-ttu-id="f2cb9-111">Verdi</span><span class="sxs-lookup"><span data-stu-id="f2cb9-111">Value</span></span>                                    |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="f2cb9-112">Totalbestilling (opprinnelig ordrelinje)</span><span class="sxs-lookup"><span data-stu-id="f2cb9-112">Total order (original order line)</span></span> | <span data-ttu-id="f2cb9-113">600 stoler</span><span class="sxs-lookup"><span data-stu-id="f2cb9-113">600 chairs</span></span>                               |
| <span data-ttu-id="f2cb9-114">Ønsket leveringsplan</span><span class="sxs-lookup"><span data-stu-id="f2cb9-114">Requested delivery schedule</span></span>       | <span data-ttu-id="f2cb9-115">100 stoler per måned</span><span class="sxs-lookup"><span data-stu-id="f2cb9-115">100 chairs per month</span></span>                     |
| <span data-ttu-id="f2cb9-116">Forespurt tidsramme for levering</span><span class="sxs-lookup"><span data-stu-id="f2cb9-116">Requested time frame for delivery</span></span> | <span data-ttu-id="f2cb9-117">6 måneder, den første dagen i hver måned</span><span class="sxs-lookup"><span data-stu-id="f2cb9-117">6 months, on the first day of each month</span></span> |

<span data-ttu-id="f2cb9-118">I dette scenariet ber kunden ber om levering av 600 stoler i partier på 100 stoler over en periode på seks måneder.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-118">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="f2cb9-119">For å holde oversikt over kravene til levering oppretter du en leveringsplan.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-119">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="f2cb9-120">På siden for leveringstidsplan oppretter du seks separate leveringslinjer.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-120">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="f2cb9-121">Hver leveringslinje inneholder 100 stoler og angir leveringsdatoen for disse 100 stolene.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-121">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="f2cb9-122">I dette tilfellet motposteres hver linje den første dagen i måneden i seks måneder etter hverandre.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-122">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="f2cb9-123">Når du oppretter en leveringsplan, endres automatisk den opprinnelige ordrelinjen til **Bestillingslinje med flere leveringer**.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-123">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="f2cb9-124">En linje av denne typen kalles en kommersielle linje og merkes med et ikon.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-124">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="f2cb9-125">Leveringslinjen er merket med et annet ikon.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-125">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="f2cb9-126">Hvis du endrer et antall på en leveringslinje, oppdateres den kommersielle linjen til det totale antallet i leveringsplanen.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-126">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="f2cb9-127">Hvis en forretningsavtale har definert en sluttrabatt for ordren, sikrer leveringsplanen at bestillingen er kvalifisert for sluttrabatten, selv om ordren er delt inn i separate leveranser.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-127">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="f2cb9-128">Ordrer som har en leveringsplan, behandles mot leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-128">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="f2cb9-129">Behandling inkluderer postering av følgesedler, produktkvitteringer og fakturering.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-129">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="f2cb9-130">Dokumentutskrifter av ordrer og tilbud som har en leveringsplan, viser bare leveringslinjene.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-130">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="f2cb9-131">De vises ikke de opprinnelige linjene (kommersielle linjer).</span><span class="sxs-lookup"><span data-stu-id="f2cb9-131">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="f2cb9-132">**Merk:** I tillegg vises bare leveringslinjene når du utfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="f2cb9-132">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="f2cb9-133">Poster</span><span class="sxs-lookup"><span data-stu-id="f2cb9-133">Post</span></span>
-   <span data-ttu-id="f2cb9-134">Kopier side</span><span class="sxs-lookup"><span data-stu-id="f2cb9-134">Copy pages</span></span>
-   <span data-ttu-id="f2cb9-135">Bla gjennom listesider og rapporter</span><span class="sxs-lookup"><span data-stu-id="f2cb9-135">Browse list pages and reports</span></span>

<span data-ttu-id="f2cb9-136">Når du bekrefter salgstilbud, viser de resulterende salgsordrene hele leveringsplanen, også ordrelinjene som har flere leveringer.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-136">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="f2cb9-137">I tillegg vises hele leveringsplanen på alle de viktige sidene, for eksempel salgsordrer, salgstilbud og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-137">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
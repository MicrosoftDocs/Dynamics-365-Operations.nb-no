--- 
title: Sende salgsordrer uten lagerstyring
description: "Denne veiledningen beskriver hvordan du oppdaterer en salgsordre når produkter sendes til kunden."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: ae70e09dbc4da90b7d1802d076384eae2d00da0e
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="19a9c-103">Sende salgsordrer uten lagerstyring</span><span class="sxs-lookup"><span data-stu-id="19a9c-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19a9c-104">Denne veiledningen beskriver hvordan du oppdaterer en salgsordre når produkter sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="19a9c-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="19a9c-105">Veiledningen er tilgjengelig for fullføringsflyten som ikke er definert for lagerstyring (verken grunnleggende eller avansert lagerstyring), og krever derfor ikke at produktplukking registreres før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="19a9c-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="19a9c-106">Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="19a9c-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="19a9c-107">I begge tilfeller før du starter oppgaven, oppretter du en salgsordre for en lagerført vare med et antall som er større enn 1.</span><span class="sxs-lookup"><span data-stu-id="19a9c-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="19a9c-108">For å unngå en posteringsfeil må du kontrollere at produktets lagerbeholdning i området og lageret som du har valgt, dekker ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="19a9c-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="19a9c-109">Postere følgeseddel for en ordre</span><span class="sxs-lookup"><span data-stu-id="19a9c-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="19a9c-110">Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="19a9c-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="19a9c-111">Finn og velg ordren du har opprettet for denne oppgaven, i listen.</span><span class="sxs-lookup"><span data-stu-id="19a9c-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="19a9c-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="19a9c-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="19a9c-113">Klikk Plukk og pakk i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="19a9c-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="19a9c-114">Klikk Poster følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="19a9c-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="19a9c-115">Vis eller skjul delen Parametere.</span><span class="sxs-lookup"><span data-stu-id="19a9c-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="19a9c-116">Velg Alle i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="19a9c-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="19a9c-117">Andre alternativer omfatter Lever nå og Plukket.</span><span class="sxs-lookup"><span data-stu-id="19a9c-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="19a9c-118">Hvis ordrelinjen skal leveres delvis og Lever nå-feltet på ordrelinjen som inneholder et antall, velger du Lever nå.</span><span class="sxs-lookup"><span data-stu-id="19a9c-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="19a9c-119">Hvis organisasjonens fullføringsflyt inkluderer plukking som en egen prosess som administreres av og er registrert i en plukkliste, velger du Plukket.</span><span class="sxs-lookup"><span data-stu-id="19a9c-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="19a9c-120">Kontroller at alternativet Postering er satt til Ja.</span><span class="sxs-lookup"><span data-stu-id="19a9c-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="19a9c-121">Velg Ja for alternativet Skriv ut følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="19a9c-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="19a9c-122">Kategorien Oversikt viser en liste med følgesedler som skal genereres i denne posteringen.</span><span class="sxs-lookup"><span data-stu-id="19a9c-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="19a9c-123">Hvis du leverer en enkelt ordre, vil det vanligvis være én følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="19a9c-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="19a9c-124">Men hvis den ordrelinjer skal sendes fra forskjellige områder, vil postering automatisk deles inn i det aktuelle antallet dokumenter.</span><span class="sxs-lookup"><span data-stu-id="19a9c-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="19a9c-125">Dette er en obligatorisk betingelse som ikke kan endres.</span><span class="sxs-lookup"><span data-stu-id="19a9c-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="19a9c-126">På samme måte bokføringen også deles i flere dokumenter hvis ordrens linjer skal leveres til forskjellige leveringsadresser, og policyen for levering settes opp slik at det kreves en deling.</span><span class="sxs-lookup"><span data-stu-id="19a9c-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="19a9c-127">Merk raden for ordrelinjen som skal leveres, i kategorien Linjer.</span><span class="sxs-lookup"><span data-stu-id="19a9c-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="19a9c-128">Angi et tall som er lavere enn det opprinnelige antallet i feltet Oppdater.</span><span class="sxs-lookup"><span data-stu-id="19a9c-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="19a9c-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="19a9c-129">Click OK.</span></span>
12. <span data-ttu-id="19a9c-130">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="19a9c-130">Click Yes.</span></span>
13. <span data-ttu-id="19a9c-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="19a9c-131">Close the page.</span></span>
14. <span data-ttu-id="19a9c-132">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="19a9c-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="19a9c-133">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="19a9c-133">Click Change view.</span></span>
16. <span data-ttu-id="19a9c-134">Klikk Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="19a9c-134">Click Header view.</span></span>
    * <span data-ttu-id="19a9c-135">Hvis alle linjene i ordren er levert, endres ordrestatusen fra Åpen til Levert.</span><span class="sxs-lookup"><span data-stu-id="19a9c-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="19a9c-136">I dette eksemplet er ordrelinjen levert delvis.</span><span class="sxs-lookup"><span data-stu-id="19a9c-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="19a9c-137">Dette er grunnen til at ordrestatusen er Åpen.</span><span class="sxs-lookup"><span data-stu-id="19a9c-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="19a9c-138">Dokumentstatus-feltet er satt til Følgeseddel, fordi minst én av bestillingslinjene er levert.</span><span class="sxs-lookup"><span data-stu-id="19a9c-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="19a9c-139">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="19a9c-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="19a9c-140">Velg Linjeantall.</span><span class="sxs-lookup"><span data-stu-id="19a9c-140">Click Line quantity.</span></span>
19. <span data-ttu-id="19a9c-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="19a9c-141">Close the page.</span></span>
20. <span data-ttu-id="19a9c-142">Klikk Plukk og pakk i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="19a9c-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="19a9c-143">Klikk Følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="19a9c-143">Click Packing slip.</span></span>
    * <span data-ttu-id="19a9c-144">Siden Følgeseddeljournal inneholder alle følgeseddeldokumentene som ble generert for ordren.</span><span class="sxs-lookup"><span data-stu-id="19a9c-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="19a9c-145">Du kan se nærmere på detaljene for hvert dokument og skrive dem ut, hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="19a9c-145">You can review details of each document and print them, if you wish.</span></span>  



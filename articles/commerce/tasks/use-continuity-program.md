---
title: Bruke kontinuitetsprogram
description: Denne fremgangsmåten hjelper med å selge et kontinuitetsprogram og behandle tilknyttede salgsordrer.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd0bfcd99a23e4c639a6317adefb41a947a487a5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023520"
---
# <a name="using-continuity-program"></a><span data-ttu-id="ad13b-103">Bruke kontinuitetsprogram</span><span class="sxs-lookup"><span data-stu-id="ad13b-103">Using continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ad13b-104">Denne fremgangsmåten hjelper med å selge et kontinuitetsprogram og behandle tilknyttede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ad13b-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="ad13b-105">For å fullføre denne prosedyren, må brukeren være definert som telefonsenterbruker.</span><span class="sxs-lookup"><span data-stu-id="ad13b-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="ad13b-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="ad13b-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="ad13b-107">Gå til Retail og Commerce > Kunder > Kundestøtte.</span><span class="sxs-lookup"><span data-stu-id="ad13b-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="ad13b-108">I Søketekst-feltet skriver du inn Karin og trykker deretter Tab-tasten.</span><span class="sxs-lookup"><span data-stu-id="ad13b-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="ad13b-109">Avansert søk-dialogboksen skal vises.</span><span class="sxs-lookup"><span data-stu-id="ad13b-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="ad13b-110">Hvis ikke, klikker du Søk til høyre for dette feltet.</span><span class="sxs-lookup"><span data-stu-id="ad13b-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="ad13b-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ad13b-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ad13b-112">Det skal bare være én rad som vises med Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="ad13b-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="ad13b-113">Merk raden ved å klikke på avmerkingskolonnen helt til venstre i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="ad13b-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="ad13b-114">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="ad13b-114">Click Select.</span></span>
5. <span data-ttu-id="ad13b-115">Klikk Ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="ad13b-115">Click New sales order.</span></span>
    * <span data-ttu-id="ad13b-116">Det er lurt å notere seg salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="ad13b-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="ad13b-117">Du vil trenge det senere i prosedyren.</span><span class="sxs-lookup"><span data-stu-id="ad13b-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="ad13b-118">I Varenummer-feltet skriver du inn 88000 og trykker deretter Tab-tasten.</span><span class="sxs-lookup"><span data-stu-id="ad13b-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="ad13b-119">Dette er en kontinuitetsvare i demonstrasjonsdataene for USRT.</span><span class="sxs-lookup"><span data-stu-id="ad13b-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="ad13b-120">Klikk Fullført.</span><span class="sxs-lookup"><span data-stu-id="ad13b-120">Click Complete.</span></span>
8. <span data-ttu-id="ad13b-121">Angi Visa i Betalingsmetode-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad13b-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="ad13b-122">Klikk Legg til kredittkort.</span><span class="sxs-lookup"><span data-stu-id="ad13b-122">Click Add credit card.</span></span>
    * <span data-ttu-id="ad13b-123">Angi den nødvendige kredittkortinformasjonen på denne siden.</span><span class="sxs-lookup"><span data-stu-id="ad13b-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="ad13b-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ad13b-124">Click OK.</span></span>
11. <span data-ttu-id="ad13b-125">Vid delen Betaling.</span><span class="sxs-lookup"><span data-stu-id="ad13b-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="ad13b-126">Hvis du vil sende en telefonsenterordre, må betalinger angis for ordren.</span><span class="sxs-lookup"><span data-stu-id="ad13b-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="ad13b-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ad13b-127">Click OK.</span></span>
13. <span data-ttu-id="ad13b-128">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="ad13b-128">Click Submit.</span></span>
    * <span data-ttu-id="ad13b-129">Du er ferdig med å opprette en ny kontinuitetsordre.</span><span class="sxs-lookup"><span data-stu-id="ad13b-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="ad13b-130">Nå skal du kjøre to satsvise prosesser som brukes til å behandle kontinuitetsordrene.</span><span class="sxs-lookup"><span data-stu-id="ad13b-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="ad13b-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ad13b-131">Close the page.</span></span>
15. <span data-ttu-id="ad13b-132">Gå til Retail og Commerce > Kontinuitet > Behandle kontinuitetsbetalinger.</span><span class="sxs-lookup"><span data-stu-id="ad13b-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="ad13b-133">I Kontinuitetsvare-feltet skriver du inn 88000 og trykker deretter Tab-tasten.</span><span class="sxs-lookup"><span data-stu-id="ad13b-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="ad13b-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ad13b-134">Click OK.</span></span>
18. <span data-ttu-id="ad13b-135">Gå til Retail og Commerce > Kontinuitet > Opprett underordnede kontinuitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="ad13b-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="ad13b-136">Denne prosessen oppretter nye salgsordrer basert på innstillingene for kontinuitetsprogrammene dine.</span><span class="sxs-lookup"><span data-stu-id="ad13b-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="ad13b-137">I Kontinuitetsvare-feltet skriver du inn 88000 og trykker deretter Tab-tasten.</span><span class="sxs-lookup"><span data-stu-id="ad13b-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="ad13b-138">Vare 88000 er en kontinuitetsvare i demonstrasjonsdataene for USRT.</span><span class="sxs-lookup"><span data-stu-id="ad13b-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="ad13b-139">Angi eller velg en verdi i feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="ad13b-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="ad13b-140">Angi salgsordrenummeret du noterte deg tidligere i denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ad13b-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="ad13b-141">Dette vil holde behandlingstiden nede på et minimum for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="ad13b-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="ad13b-142">Salgsordre-feltet er valgfritt – du kan behandle alle ordrer for et hvilken som helst program.</span><span class="sxs-lookup"><span data-stu-id="ad13b-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="ad13b-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ad13b-143">Click OK.</span></span>

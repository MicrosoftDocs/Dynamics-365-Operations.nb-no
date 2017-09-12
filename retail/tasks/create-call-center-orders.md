--- 
title: " Opprette telefonsenterordrer"
description: "Denne prosedyren hjelper med å slå opp en kunde, opprette en ny ordre, søke etter et produkt og hente inn betaling fra kunden."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 62f88cc2e28405a9d2eb43819fb09d83a64658b6
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="01e6c-103"> Opprette telefonsenterordrer</span><span class="sxs-lookup"><span data-stu-id="01e6c-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="01e6c-104">Denne prosedyren hjelper med å slå opp en kunde, opprette en ny ordre, søke etter et produkt og hente inn betaling fra kunden.</span><span class="sxs-lookup"><span data-stu-id="01e6c-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="01e6c-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT og er ment for selgere.</span><span class="sxs-lookup"><span data-stu-id="01e6c-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="01e6c-106">Forhåndskrav: Brukeren som utfører prosedyren, er satt opp som telefonsenterbrukere og katalogen for Fabrikam annethvert år publiseres med minst én kildekode.</span><span class="sxs-lookup"><span data-stu-id="01e6c-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="01e6c-107">Gå til Detaljhandel og handel > Kunder > Kundestøtte.</span><span class="sxs-lookup"><span data-stu-id="01e6c-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="01e6c-108">Angi søkekriteriene for å slå opp kunden, i Søketekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="01e6c-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="01e6c-109">I denne eksempelprosedyren skriver du inn Karin og trykker TAB.</span><span class="sxs-lookup"><span data-stu-id="01e6c-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="01e6c-110">Klikk Søk.</span><span class="sxs-lookup"><span data-stu-id="01e6c-110">Click Search.</span></span>
    * <span data-ttu-id="01e6c-111">Siden det bare finnes én kunde med navnet Karin i demonstrasjonsdataene, velges de automatisk.</span><span class="sxs-lookup"><span data-stu-id="01e6c-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="01e6c-112">Klikk Ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="01e6c-112">Click New sales order.</span></span>
5. <span data-ttu-id="01e6c-113">Vis eller skjul delen Salgsordrehode.</span><span class="sxs-lookup"><span data-stu-id="01e6c-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="01e6c-114">Velg kildekoden for katalogen.</span><span class="sxs-lookup"><span data-stu-id="01e6c-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="01e6c-115">Hvis det ikke finnes aktive kildekoder, kan du lukke Kilde-feltet og hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="01e6c-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="01e6c-116">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="01e6c-116">Click Add line.</span></span>
8. <span data-ttu-id="01e6c-117">I Varenummer-feltet angir du varesøkeordet.</span><span class="sxs-lookup"><span data-stu-id="01e6c-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="01e6c-118">I denne eksempelprosedyren angir du et delvis varenummer, 8111, og trykker TAB.</span><span class="sxs-lookup"><span data-stu-id="01e6c-118">For this sample procedure enter a partial item number of '8111' and press tab.</span></span> <span data-ttu-id="01e6c-119">Søkevinduet vil dermed vises.</span><span class="sxs-lookup"><span data-stu-id="01e6c-119">This will pop up the item search window.</span></span>  
9. <span data-ttu-id="01e6c-120">Velg produktet som skal legges til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="01e6c-120">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="01e6c-121">Angi salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="01e6c-121">Enter the sales quantity.</span></span>
11. <span data-ttu-id="01e6c-122">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="01e6c-122">Click Create.</span></span>
12. <span data-ttu-id="01e6c-123">Klikk Fullfør for å registrere kundebetalingen.</span><span class="sxs-lookup"><span data-stu-id="01e6c-123">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="01e6c-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="01e6c-124">Click Add.</span></span>
    * <span data-ttu-id="01e6c-125">Koblingen Legg til er i Betalinger-fanen.</span><span class="sxs-lookup"><span data-stu-id="01e6c-125">The Add link is in the Payments tab.</span></span> <span data-ttu-id="01e6c-126">Vis Betalinger-fanen hvis den er skjult.</span><span class="sxs-lookup"><span data-stu-id="01e6c-126">Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="01e6c-127">Velg betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="01e6c-127">Select the payment method.</span></span>
    * <span data-ttu-id="01e6c-128">Velg kontantbetalingsmåten for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="01e6c-128">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="01e6c-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="01e6c-129">Close the page.</span></span>
16. <span data-ttu-id="01e6c-130">Angi beløpet.</span><span class="sxs-lookup"><span data-stu-id="01e6c-130">Enter the amount.</span></span>
    * <span data-ttu-id="01e6c-131">I denne prosedyren angir du et beløp som er likt ordresaldoen som vises på sammendragssiden for salgsordren til venstre i beløpsfeltet.</span><span class="sxs-lookup"><span data-stu-id="01e6c-131">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="01e6c-132">Dermed kan du fullføre ordren som fullt betalt.</span><span class="sxs-lookup"><span data-stu-id="01e6c-132">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="01e6c-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="01e6c-133">Click OK.</span></span>
18. <span data-ttu-id="01e6c-134">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="01e6c-134">Click Submit.</span></span>



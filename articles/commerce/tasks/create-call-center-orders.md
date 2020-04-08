---
title: " Opprette telefonsenterordrer"
description: Denne prosedyren hjelper med å slå opp en kunde, opprette en ny ordre, søke etter et produkt og hente inn betaling fra kunden.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ec10e0f79e4eca7f51ba48c679dcf6fe745eb29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141436"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="60c76-103"> Opprette telefonsenterordrer</span><span class="sxs-lookup"><span data-stu-id="60c76-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60c76-104">Denne prosedyren hjelper med å slå opp en kunde, opprette en ny ordre, søke etter et produkt og hente inn betaling fra kunden.</span><span class="sxs-lookup"><span data-stu-id="60c76-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="60c76-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT og er ment for selgere.</span><span class="sxs-lookup"><span data-stu-id="60c76-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="60c76-106">Forhåndskrav: Brukeren som utfører prosedyren, er satt opp som telefonsenterbrukere og katalogen for Fabrikam annethvert år publiseres med minst én kildekode.</span><span class="sxs-lookup"><span data-stu-id="60c76-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="60c76-107">Gå til Retail og Commerce > Kunder > Kundestøtte.</span><span class="sxs-lookup"><span data-stu-id="60c76-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="60c76-108">Angi søkekriteriene for å slå opp kunden, i Søketekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="60c76-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="60c76-109">I denne eksempelprosedyren skriver du inn Karin og trykker TAB.</span><span class="sxs-lookup"><span data-stu-id="60c76-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="60c76-110">Klikk Søk.</span><span class="sxs-lookup"><span data-stu-id="60c76-110">Click Search.</span></span>
    * <span data-ttu-id="60c76-111">Siden det bare finnes én kunde med navnet Karin i demonstrasjonsdataene, velges de automatisk.</span><span class="sxs-lookup"><span data-stu-id="60c76-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="60c76-112">Klikk Ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="60c76-112">Click New sales order.</span></span>
5. <span data-ttu-id="60c76-113">Vis eller skjul delen Salgsordrehode.</span><span class="sxs-lookup"><span data-stu-id="60c76-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="60c76-114">Velg kildekoden for katalogen.</span><span class="sxs-lookup"><span data-stu-id="60c76-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="60c76-115">Hvis det ikke finnes aktive kildekoder, kan du lukke Kilde-feltet og hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="60c76-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="60c76-116">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="60c76-116">Click Add line.</span></span>
8. <span data-ttu-id="60c76-117">I Varenummer-feltet angir du varesøkeordet.</span><span class="sxs-lookup"><span data-stu-id="60c76-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="60c76-118">I denne eksempelprosedyren angir du et delvis varenummer, 8111, og trykker TAB. Søkevinduet vil dermed vises.</span><span class="sxs-lookup"><span data-stu-id="60c76-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="60c76-119">Velg produktet som skal legges til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="60c76-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="60c76-120">Angi salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="60c76-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="60c76-121">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="60c76-121">Click Create.</span></span>
12. <span data-ttu-id="60c76-122">Klikk Fullfør for å registrere kundebetalingen.</span><span class="sxs-lookup"><span data-stu-id="60c76-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="60c76-123">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="60c76-123">Click Add.</span></span>
    * <span data-ttu-id="60c76-124">Koblingen Legg til er i Betalinger-fanen. Vis Betalinger-fanen hvis den er skjult.</span><span class="sxs-lookup"><span data-stu-id="60c76-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="60c76-125">Velg betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="60c76-125">Select the payment method.</span></span>
    * <span data-ttu-id="60c76-126">Velg kontantbetalingsmåten for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="60c76-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="60c76-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="60c76-127">Close the page.</span></span>
16. <span data-ttu-id="60c76-128">Angi beløpet.</span><span class="sxs-lookup"><span data-stu-id="60c76-128">Enter the amount.</span></span>
    * <span data-ttu-id="60c76-129">I denne prosedyren angir du et beløp som er likt ordresaldoen som vises på sammendragssiden for salgsordren til venstre i beløpsfeltet.</span><span class="sxs-lookup"><span data-stu-id="60c76-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="60c76-130">Dermed kan du fullføre ordren som fullt betalt.</span><span class="sxs-lookup"><span data-stu-id="60c76-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="60c76-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="60c76-131">Click OK.</span></span>
18. <span data-ttu-id="60c76-132">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="60c76-132">Click Submit.</span></span>


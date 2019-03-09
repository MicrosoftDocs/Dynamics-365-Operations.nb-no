---
title: Avstemme frakt manuelt
description: Denne fremgangsmåten viser hvordan du avstemmer frakt manuelt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee2d114b0a725b947add3e155cc6445021fee998
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "351890"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="576e7-103">Avstemme frakt manuelt</span><span class="sxs-lookup"><span data-stu-id="576e7-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="576e7-104">Denne fremgangsmåten viser hvordan du avstemmer frakt manuelt.</span><span class="sxs-lookup"><span data-stu-id="576e7-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="576e7-105">Dette gjøres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="576e7-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="576e7-106">Du kan bruke prosedyren i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="576e7-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="576e7-107">Velge en last for avstemming</span><span class="sxs-lookup"><span data-stu-id="576e7-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="576e7-108">Gå til Transportstyring > Planlegging > Arbeidsområde for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="576e7-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="576e7-109">Fjern merket for Skjul sendt og mottatt.</span><span class="sxs-lookup"><span data-stu-id="576e7-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="576e7-110">I listen velger du lasten som har last-ID 00006.</span><span class="sxs-lookup"><span data-stu-id="576e7-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="576e7-111">Opprette en transportørfaktura</span><span class="sxs-lookup"><span data-stu-id="576e7-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="576e7-112">Hvis du avstemmer frakt manuelt og ikke mottar transportørfakturaer automatisk, kan du opprette en faktura basert på fraktbrevet.</span><span class="sxs-lookup"><span data-stu-id="576e7-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="576e7-113">Klikk Relatert informasjon.</span><span class="sxs-lookup"><span data-stu-id="576e7-113">Click Related information.</span></span>
2. <span data-ttu-id="576e7-114">Klikk Detaljer for fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="576e7-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="576e7-115">Klikk Generer fraktbrevfaktura.</span><span class="sxs-lookup"><span data-stu-id="576e7-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="576e7-116">Skriv inn en verdi i Faktura-feltet.</span><span class="sxs-lookup"><span data-stu-id="576e7-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="576e7-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="576e7-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="576e7-118">Avstemme fakturaen</span><span class="sxs-lookup"><span data-stu-id="576e7-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="576e7-119">Når du avstemmer en transportørfaktura og et fraktbrev, gjøres dette linje for linje.</span><span class="sxs-lookup"><span data-stu-id="576e7-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="576e7-120">Klikk Samsvar fraktbrev og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="576e7-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="576e7-121">Vis delen Fakturadetaljer.</span><span class="sxs-lookup"><span data-stu-id="576e7-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="576e7-122">Utvid delen Detaljer for ikke-samsvart fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="576e7-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="576e7-123">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="576e7-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="576e7-124">Klikk Samsvar.</span><span class="sxs-lookup"><span data-stu-id="576e7-124">Click Match.</span></span>
6. <span data-ttu-id="576e7-125">Utvid delen Detaljer for samsvart fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="576e7-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="576e7-126">Send fakturaen til godkjenning</span><span class="sxs-lookup"><span data-stu-id="576e7-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="576e7-127">Klikk Send til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="576e7-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="576e7-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="576e7-128">Close the page.</span></span>
3. <span data-ttu-id="576e7-129">Fjern merket for Skjul godkjent.</span><span class="sxs-lookup"><span data-stu-id="576e7-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="576e7-130">Klikk Leverandørfakturajournaler.</span><span class="sxs-lookup"><span data-stu-id="576e7-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="576e7-131">Klikk for å følge koblingen i Referansejournalnummeret-feltet.</span><span class="sxs-lookup"><span data-stu-id="576e7-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="576e7-132">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="576e7-132">Click Lines.</span></span>


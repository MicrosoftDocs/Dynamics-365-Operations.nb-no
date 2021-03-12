---
title: Avstemme frakt manuelt
description: Denne fremgangsmåten viser hvordan du avstemmer frakt manuelt.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8679a729dc17e3ee85468b459da3956a92160ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974066"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="acb8d-103">Avstemme frakt manuelt</span><span class="sxs-lookup"><span data-stu-id="acb8d-103">Reconcile freight manually</span></span>

<span data-ttu-id="acb8d-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="acb8d-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="acb8d-105">Denne fremgangsmåten viser hvordan du avstemmer frakt manuelt.</span><span class="sxs-lookup"><span data-stu-id="acb8d-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="acb8d-106">Dette gjøres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="acb8d-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="acb8d-107">Du kan bruke prosedyren i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="acb8d-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="acb8d-108">Velge en last for avstemming</span><span class="sxs-lookup"><span data-stu-id="acb8d-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="acb8d-109">Gå til Transportstyring > Planlegging > Arbeidsområde for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="acb8d-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="acb8d-110">Fjern merket for Skjul sendt og mottatt.</span><span class="sxs-lookup"><span data-stu-id="acb8d-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="acb8d-111">I listen velger du lasten som har last-ID 00006.</span><span class="sxs-lookup"><span data-stu-id="acb8d-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="acb8d-112">Opprette en transportørfaktura</span><span class="sxs-lookup"><span data-stu-id="acb8d-112">Create a carrier invoice</span></span>
<span data-ttu-id="acb8d-113">Hvis du avstemmer frakt manuelt og ikke mottar transportørfakturaer automatisk, kan du opprette en faktura basert på fraktbrevet.</span><span class="sxs-lookup"><span data-stu-id="acb8d-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="acb8d-114">Klikk på Relatert informasjon.</span><span class="sxs-lookup"><span data-stu-id="acb8d-114">Click Related information.</span></span>
2. <span data-ttu-id="acb8d-115">Klikk på Detaljer for fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="acb8d-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="acb8d-116">Klikk på Generer fraktbrevfaktura.</span><span class="sxs-lookup"><span data-stu-id="acb8d-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="acb8d-117">Skriv inn en verdi i Faktura-feltet.</span><span class="sxs-lookup"><span data-stu-id="acb8d-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="acb8d-118">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="acb8d-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="acb8d-119">Avstemme fakturaen</span><span class="sxs-lookup"><span data-stu-id="acb8d-119">Reconcile the invoice</span></span>
<span data-ttu-id="acb8d-120">Når du avstemmer en transportørfaktura og et fraktbrev, gjøres dette linje for linje.</span><span class="sxs-lookup"><span data-stu-id="acb8d-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="acb8d-121">Klikk på Samsvar fraktbrev og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="acb8d-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="acb8d-122">Vis delen Fakturadetaljer.</span><span class="sxs-lookup"><span data-stu-id="acb8d-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="acb8d-123">Utvid delen Detaljer for ikke-samsvart fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="acb8d-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="acb8d-124">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="acb8d-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="acb8d-125">Klikk på Samsvar.</span><span class="sxs-lookup"><span data-stu-id="acb8d-125">Click Match.</span></span>
6. <span data-ttu-id="acb8d-126">Utvid delen Detaljer for samsvart fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="acb8d-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="acb8d-127">Send fakturaen til godkjenning</span><span class="sxs-lookup"><span data-stu-id="acb8d-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="acb8d-128">Klikk på Send til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="acb8d-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="acb8d-129">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="acb8d-129">Close the page.</span></span>
3. <span data-ttu-id="acb8d-130">Fjern merket for Skjul godkjent.</span><span class="sxs-lookup"><span data-stu-id="acb8d-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="acb8d-131">Klikk på Leverandørfakturajournaler.</span><span class="sxs-lookup"><span data-stu-id="acb8d-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="acb8d-132">Klikk på for å følge koblingen i Referansejournalnummeret-feltet.</span><span class="sxs-lookup"><span data-stu-id="acb8d-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="acb8d-133">Klikk på Linjer.</span><span class="sxs-lookup"><span data-stu-id="acb8d-133">Click Lines.</span></span>


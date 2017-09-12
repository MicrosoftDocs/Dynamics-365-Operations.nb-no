--- 
title: Avstemme frakt manuelt
description: "Denne fremgangsmåten viser hvordan du avstemmer frakt manuelt."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="10e4a-103">Avstemme frakt manuelt</span><span class="sxs-lookup"><span data-stu-id="10e4a-103">Reconcile freight manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10e4a-104">Denne fremgangsmåten viser hvordan du avstemmer frakt manuelt.</span><span class="sxs-lookup"><span data-stu-id="10e4a-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="10e4a-105">Dette gjøres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="10e4a-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="10e4a-106">Du kan bruke prosedyren i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="10e4a-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="10e4a-107">Velge en last for avstemming</span><span class="sxs-lookup"><span data-stu-id="10e4a-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="10e4a-108">Gå til Transportstyring > Planlegging > Arbeidsområde for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="10e4a-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="10e4a-109">Fjern merket for Skjul sendt og mottatt.</span><span class="sxs-lookup"><span data-stu-id="10e4a-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="10e4a-110">I listen velger du lasten som har last-ID 00006.</span><span class="sxs-lookup"><span data-stu-id="10e4a-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="10e4a-111">Opprette en transportørfaktura</span><span class="sxs-lookup"><span data-stu-id="10e4a-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="10e4a-112">Hvis du avstemmer frakt manuelt og ikke mottar transportørfakturaer automatisk, kan du opprette en faktura basert på fraktbrevet.</span><span class="sxs-lookup"><span data-stu-id="10e4a-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="10e4a-113">Klikk Relatert informasjon.</span><span class="sxs-lookup"><span data-stu-id="10e4a-113">Click Related information.</span></span>
2. <span data-ttu-id="10e4a-114">Klikk Detaljer for fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="10e4a-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="10e4a-115">Klikk Generer fraktbrevfaktura.</span><span class="sxs-lookup"><span data-stu-id="10e4a-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="10e4a-116">Skriv inn en verdi i Faktura-feltet.</span><span class="sxs-lookup"><span data-stu-id="10e4a-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="10e4a-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="10e4a-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="10e4a-118">Avstemme fakturaen</span><span class="sxs-lookup"><span data-stu-id="10e4a-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="10e4a-119">Når du avstemmer en transportørfaktura og et fraktbrev, gjøres dette linje for linje.</span><span class="sxs-lookup"><span data-stu-id="10e4a-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="10e4a-120">Klikk Samsvar fraktbrev og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="10e4a-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="10e4a-121">Vis delen Fakturadetaljer.</span><span class="sxs-lookup"><span data-stu-id="10e4a-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="10e4a-122">Utvid delen Detaljer for ikke-samsvart fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="10e4a-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="10e4a-123">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="10e4a-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="10e4a-124">Klikk Samsvar.</span><span class="sxs-lookup"><span data-stu-id="10e4a-124">Click Match.</span></span>
6. <span data-ttu-id="10e4a-125">Utvid delen Detaljer for samsvart fraktbrev.</span><span class="sxs-lookup"><span data-stu-id="10e4a-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="10e4a-126">Send fakturaen til godkjenning</span><span class="sxs-lookup"><span data-stu-id="10e4a-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="10e4a-127">Klikk Send til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="10e4a-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="10e4a-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="10e4a-128">Close the page.</span></span>
3. <span data-ttu-id="10e4a-129">Fjern merket for Skjul godkjent.</span><span class="sxs-lookup"><span data-stu-id="10e4a-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="10e4a-130">Klikk Leverandørfakturajournaler.</span><span class="sxs-lookup"><span data-stu-id="10e4a-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="10e4a-131">Klikk for å følge koblingen i Referansejournalnummeret-feltet.</span><span class="sxs-lookup"><span data-stu-id="10e4a-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="10e4a-132">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="10e4a-132">Click Lines.</span></span>



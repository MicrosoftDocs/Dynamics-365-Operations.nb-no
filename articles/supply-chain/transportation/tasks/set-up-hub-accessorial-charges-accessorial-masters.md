---
title: Definere gebyrer for hubtilbehør og tilbehørsmaler
description: Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9959c20f9a8fd07cbf0cfd76f7760b44d7b5cae1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560077"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="5870a-103">Definere gebyrer for hubtilbehør og tilbehørsmaler</span><span class="sxs-lookup"><span data-stu-id="5870a-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5870a-104">Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør.</span><span class="sxs-lookup"><span data-stu-id="5870a-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="5870a-105">Fremgangsmåten bruker USMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="5870a-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="5870a-106">Dette oppsettet utføres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="5870a-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="5870a-107">Definere en hubmal</span><span class="sxs-lookup"><span data-stu-id="5870a-107">Set up a hub master</span></span>
1. <span data-ttu-id="5870a-108">Gå til Transportstyring > Oppsett > Vurdering > Tilbehørsmaler.</span><span class="sxs-lookup"><span data-stu-id="5870a-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="5870a-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5870a-109">Click New.</span></span>
3. <span data-ttu-id="5870a-110">Angi en verdi i Tilbehørsmal-feltet.</span><span class="sxs-lookup"><span data-stu-id="5870a-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="5870a-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5870a-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5870a-112">Velg Hub i Tilbehørstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="5870a-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="5870a-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5870a-113">Click Save.</span></span>
7. <span data-ttu-id="5870a-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5870a-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="5870a-115">Definer et gebyr for hubtilbehør</span><span class="sxs-lookup"><span data-stu-id="5870a-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="5870a-116">Gå til Transportstyring > Oppsett > Vurdering > Gebyrer for hubtilbehøret.</span><span class="sxs-lookup"><span data-stu-id="5870a-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="5870a-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5870a-117">Click New.</span></span>
3. <span data-ttu-id="5870a-118">Skriv inn en verdi i feltet ID for hubtilbehør.</span><span class="sxs-lookup"><span data-stu-id="5870a-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="5870a-119">Klikk rullegardinknappen i Hub-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5870a-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5870a-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5870a-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="5870a-121">Velg et alternativ i feltet Hubposisjon.</span><span class="sxs-lookup"><span data-stu-id="5870a-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="5870a-122">Du kan opprette tillegget som en henting eller levering.</span><span class="sxs-lookup"><span data-stu-id="5870a-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="5870a-123">Avhengig av valget gjelder tillegget for det tilsvarende transportsegmentet i din rute.</span><span class="sxs-lookup"><span data-stu-id="5870a-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="5870a-124">Klikk rullegardinknappen i feltet Tilbehørsmal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5870a-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5870a-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5870a-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5870a-126">Velg malen du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="5870a-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="5870a-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5870a-127">Click Save.</span></span>
10. <span data-ttu-id="5870a-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5870a-128">Close the page.</span></span>


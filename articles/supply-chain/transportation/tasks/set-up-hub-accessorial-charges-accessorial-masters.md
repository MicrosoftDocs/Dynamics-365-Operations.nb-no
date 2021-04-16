---
title: Definere gebyrer for hubtilbehør og tilbehørsmaler
description: Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f4c0d3af96e6ef6735b01165a49c1450b3b633b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837572"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="b8fae-103">Definere gebyrer for hubtilbehør og tilbehørsmaler</span><span class="sxs-lookup"><span data-stu-id="b8fae-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8fae-104">Denne fremgangsmåten viser hvordan du oppretter en tilbehørsmal for en hub og bruker denne malen til å opprette et gebyr for hubtilbehør.</span><span class="sxs-lookup"><span data-stu-id="b8fae-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="b8fae-105">Fremgangsmåten bruker USMF-datasettet.</span><span class="sxs-lookup"><span data-stu-id="b8fae-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="b8fae-106">Dette oppsettet utføres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="b8fae-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="b8fae-107">Definere en hubmal</span><span class="sxs-lookup"><span data-stu-id="b8fae-107">Set up a hub master</span></span>
1. <span data-ttu-id="b8fae-108">Gå til Transportstyring > Oppsett > Vurdering > Tilbehørsmaler.</span><span class="sxs-lookup"><span data-stu-id="b8fae-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="b8fae-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b8fae-109">Click New.</span></span>
3. <span data-ttu-id="b8fae-110">Angi en verdi i Tilbehørsmal-feltet.</span><span class="sxs-lookup"><span data-stu-id="b8fae-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="b8fae-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b8fae-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b8fae-112">Velg Hub i Tilbehørstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="b8fae-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="b8fae-113">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="b8fae-113">Click Save.</span></span>
7. <span data-ttu-id="b8fae-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b8fae-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="b8fae-115">Definer et gebyr for hubtilbehør</span><span class="sxs-lookup"><span data-stu-id="b8fae-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="b8fae-116">Gå til Transportstyring > Oppsett > Vurdering > Gebyrer for hubtilbehøret.</span><span class="sxs-lookup"><span data-stu-id="b8fae-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="b8fae-117">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b8fae-117">Click New.</span></span>
3. <span data-ttu-id="b8fae-118">Skriv inn en verdi i feltet ID for hubtilbehør.</span><span class="sxs-lookup"><span data-stu-id="b8fae-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="b8fae-119">Klikk på rullegardinknappen i Hub-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b8fae-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b8fae-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b8fae-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b8fae-121">Velg et alternativ i feltet Hubposisjon.</span><span class="sxs-lookup"><span data-stu-id="b8fae-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="b8fae-122">Du kan opprette tillegget som en henting eller levering.</span><span class="sxs-lookup"><span data-stu-id="b8fae-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="b8fae-123">Avhengig av valget gjelder tillegget for det tilsvarende transportsegmentet i din rute.</span><span class="sxs-lookup"><span data-stu-id="b8fae-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="b8fae-124">Klikk på rullegardinknappen i feltet Tilbehørsmal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b8fae-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b8fae-125">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b8fae-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b8fae-126">Velg malen du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="b8fae-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="b8fae-127">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="b8fae-127">Click Save.</span></span>
10. <span data-ttu-id="b8fae-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b8fae-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
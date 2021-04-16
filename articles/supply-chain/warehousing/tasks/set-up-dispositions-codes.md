---
title: Definere disposisjonskoder
description: Denne prosedyren fokuserer på oppsettet for en disposisjonskode som kan brukes på en mobil enhet for mottaksprosessen for returordren.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16458f709788e538d036cc4d3b3239f4ffa3c42e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830936"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="85946-103">Definere disposisjonskoder</span><span class="sxs-lookup"><span data-stu-id="85946-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85946-104">Denne prosedyren fokuserer på oppsettet for en disposisjonskode som kan brukes på en mobil enhet for mottaksprosessen for returordren.</span><span class="sxs-lookup"><span data-stu-id="85946-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="85946-105">Disposisjonskoder er en samling regler som kan brukes når varer mottas.</span><span class="sxs-lookup"><span data-stu-id="85946-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="85946-106">Når du arbeidet bruker en mobil enhet for å motta varer som har blitt skadet, må brukeren for eksempel skanne en disposisjonskode for skadede elementer.</span><span class="sxs-lookup"><span data-stu-id="85946-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="85946-107">Beholdningsstatusen for mottatte varer, arbeidsmalen og lokasjonsdirektivet kan beregnes fra den skannede disposisjonskoden.</span><span class="sxs-lookup"><span data-stu-id="85946-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="85946-108">For mottaksprosessen for bestilling og ferdigmeldingsprosessen for produksjonsordren er bruk av en disposisjonskode valgfritt.</span><span class="sxs-lookup"><span data-stu-id="85946-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="85946-109">Hvis varene er registrert ved hjelp av en mobil enhet for mottaksprosessen for salgsordreretur, er bruken av disposisjonskoden obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="85946-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="85946-110">Denne veiledningen ble opprettet med demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="85946-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="85946-111">Denne fremgangsmåten er ment for lagersjef.</span><span class="sxs-lookup"><span data-stu-id="85946-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="85946-112">Gå til Lagerstyring > Oppsett > Mobilenhet > Disposisjonskoder.</span><span class="sxs-lookup"><span data-stu-id="85946-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="85946-113">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="85946-113">Click New.</span></span>
    * <span data-ttu-id="85946-114">Opprett en ny disposisjonskode som skal brukes for kundereturer.</span><span class="sxs-lookup"><span data-stu-id="85946-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="85946-115">Skriv inn en verdi i Disposisjonskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="85946-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="85946-116">Velg en beholdningsstatus i Beholdningsstatus-feltet der det er lagerblokkering.</span><span class="sxs-lookup"><span data-stu-id="85946-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="85946-117">Hvis du bruker USMF, velger du Blokkering.</span><span class="sxs-lookup"><span data-stu-id="85946-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="85946-118">Du kan legge til en beholdningsstatus i disposisjonskoden for å overstyre standardstatus på ordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="85946-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="85946-119">Angi en verdi i feltet Arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="85946-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="85946-120">Valgfritt: Velg en arbeidsmalkode som er tilknyttet en returordre.</span><span class="sxs-lookup"><span data-stu-id="85946-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="85946-121">Hvis ingen verdi er angitt, blir arbeidsmalen løst ved hjelp av standardreglene som er konfigurert i systemet.</span><span class="sxs-lookup"><span data-stu-id="85946-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="85946-122">Hvis du velger en mal for arbeid, begrenser du prosessene som denne disposisjonskoden kan brukes med.</span><span class="sxs-lookup"><span data-stu-id="85946-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="85946-123">Hvis for eksempel en disposisjonskode er en mal for arbeid med en Arbeidsordre av typen Bestilling, kan den ikke brukes til å registrere varer som returneres av kunder.</span><span class="sxs-lookup"><span data-stu-id="85946-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="85946-124">Skriv inn en verdi i Returdisposisjonskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="85946-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="85946-125">Returdisposisjonskoden bestemmer resten av ordrereturprosessen for varene som er registrert.</span><span class="sxs-lookup"><span data-stu-id="85946-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="85946-126">Kunden skal motta en kreditnota i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="85946-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="85946-127">Legg til en disposisjonskode for returer som inneholder en kredithandling.</span><span class="sxs-lookup"><span data-stu-id="85946-127">Add a returns disposition code that contains an action Credit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
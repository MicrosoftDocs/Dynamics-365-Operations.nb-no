--- 
title: " Butikkonfigurasjoner for detaljhandelsutdrag"
description: "Denne prosedyren beskriver konfigurasjoner for detaljhandelsbutikken som påvirker hvordan detaljhandelsutdrag opprettes og posteres."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 45aa0caf6fcef4cc49952557a251dd78f816125e
ms.contentlocale: nb-no
ms.lasthandoff: 11/14/2017

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="031db-103"> Butikkonfigurasjoner for detaljhandelsutdrag</span><span class="sxs-lookup"><span data-stu-id="031db-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="031db-104">Denne prosedyren beskriver konfigurasjoner for detaljhandelsbutikken som påvirker hvordan detaljhandelsutdrag opprettes og posteres.</span><span class="sxs-lookup"><span data-stu-id="031db-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="031db-105">Finansdimensjoner i detaljhandelsbutikker dekkes i en annen prosedyre.</span><span class="sxs-lookup"><span data-stu-id="031db-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="031db-106">Denne prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="031db-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="031db-107">Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="031db-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="031db-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="031db-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="031db-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="031db-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="031db-110">Innstillingene i delen Utdrag/avslutning kan påvirke opprettingen av utdrag, validering og postering for butikken.</span><span class="sxs-lookup"><span data-stu-id="031db-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="031db-111">Åpne delen Utdrag/avslutning.</span><span class="sxs-lookup"><span data-stu-id="031db-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="031db-112">Velg metoden du vil bruke for å gruppere utdragslinjene.</span><span class="sxs-lookup"><span data-stu-id="031db-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="031db-113">Velg Ja hvis det bare skal opprettes ett utdrag per dag når utdrag opprettes fra den satsvise jobben for utdragsoppretting.</span><span class="sxs-lookup"><span data-stu-id="031db-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="031db-114">Feltet Beregning av kasseoppgjør definerer om kasseoppgjør skal legges sammen, eller om den siste skal brukes.</span><span class="sxs-lookup"><span data-stu-id="031db-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="031db-115">Velg finanskontoen som avrundingsdifferanser skal posteres mot.</span><span class="sxs-lookup"><span data-stu-id="031db-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="031db-116">I feltet for maksimal avrundingsdifferanse kan du angi maksimalt tillatt avrundingsdifferanse.</span><span class="sxs-lookup"><span data-stu-id="031db-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="031db-117">Du kan angi den maksimale totale posteringsdifferansen som er tillatt for et utdrag, i Postering-feltet.</span><span class="sxs-lookup"><span data-stu-id="031db-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="031db-118">Du kan angi den maksimale totale differansen i et skift i et utdrag, i Skift-feltet.</span><span class="sxs-lookup"><span data-stu-id="031db-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="031db-119">I Transaksjon-feltet kan du angi den maksimale totale differansen i en utdragslinje.</span><span class="sxs-lookup"><span data-stu-id="031db-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="031db-120">I feltet Avslutningsmetode kan du definere om transaksjonene som skal inkluderes i et utdrag, skal være en del av en lukket skift, eller om de kan være enhver transaksjon i det definerte dato-/klokkeslettintervallet.</span><span class="sxs-lookup"><span data-stu-id="031db-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="031db-121">I feltet Slutt på arbeidsdag kan du angi et tidspunkt hvis transaksjoner som skjer etter midnatt, skal posteres på forrige dag.</span><span class="sxs-lookup"><span data-stu-id="031db-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="031db-122">Velg Ja hvis transaksjoner som skjer etter midnatt, skal posteres som en del av dagen før.</span><span class="sxs-lookup"><span data-stu-id="031db-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="031db-123">Velg Ja hvis du vil at utdrag skal opprettes for hver definerte utdragsmetode.</span><span class="sxs-lookup"><span data-stu-id="031db-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="031db-124">Dette kan være nyttig hvis resultatet av posteringen må forbedres for butikker med høye transaksjonsvolumer siden det vil opprette mange mindre utdrag som kan behandles parallelt.</span><span class="sxs-lookup"><span data-stu-id="031db-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="031db-125">I feltet Standardkunde kan du velge kundekontoen som skal brukes for salg til kunder som kommer inn i butikken.</span><span class="sxs-lookup"><span data-stu-id="031db-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  



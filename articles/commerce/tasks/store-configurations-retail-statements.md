---
title: " Butikkonfigurasjoner for detaljhandelsutdrag"
description: Denne prosedyren beskriver konfigurasjoner for butikken som påvirker hvordan Commerce-utdrag opprettes og posteres.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57081b9e737373641cd9d884919d03dcf62a2ffe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140661"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="fbc1b-103"> Butikkonfigurasjoner for detaljhandelsutdrag</span><span class="sxs-lookup"><span data-stu-id="fbc1b-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbc1b-104">Denne prosedyren beskriver konfigurasjoner for butikken som påvirker hvordan Commerce-utdrag opprettes og posteres.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="fbc1b-105">Finansdimensjoner i butikker dekkes i en annen prosedyre.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="fbc1b-106">Denne prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="fbc1b-107">I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Kanaler > Butikker > Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-107">In the **Navgiation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="fbc1b-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fbc1b-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fbc1b-110">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-110">Click **Edit**.</span></span>
5. <span data-ttu-id="fbc1b-111">Innstillingene i hurtigfanen **Utdrag/avslutning** kan påvirke opprettingen av utdrag, validering og postering for butikken.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="fbc1b-112">Utvid hurtigfanen **Utdrag/avslutning**.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="fbc1b-113">Velg metoden du vil bruke for å gruppere utdragslinjene, i **Utdragsmetode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="fbc1b-114">Velg Ja i **Ett utdrag per dag** hvis det bare skal opprettes ett utdrag per dag når utdrag opprettes fra den satsvise jobben for utdragsoppretting.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="fbc1b-115">Feltet **Beregning av kasseoppgjør** definerer om kasseoppgjør skal legges sammen, eller om den siste skal brukes.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="fbc1b-116">Velg finanskontoen som avrundingsdifferanser skal posteres mot, i **Avrunding**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="fbc1b-117">I feltet **Maksimal avrundingsdifferanse** angir du maksimalt tillatt avrundingsdifferanse.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="fbc1b-118">Angi den maksimale totale posteringsdifferansen som er tillatt for et utdrag, i **Postering**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="fbc1b-119">Angi den maksimale totale differansen i et skift i et utdrag, i **Skift**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="fbc1b-120">I **Transaksjon**-feltet angir du den maksimale totale differansen i en utdragslinje.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="fbc1b-121">I feltet **Avslutningsmetode** definerer du om transaksjonene som skal inkluderes i et utdrag, skal være en del av en lukket skift, eller om de kan være enhver transaksjon i det definerte dato-/klokkeslettintervallet.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="fbc1b-122">I feltet **Slutt på arbeidsdag** angir du et tidspunkt hvis transaksjoner som skjer etter midnatt, skal posteres på forrige dag.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="fbc1b-123">Velg Ja i **Poster som arbeidsdag** hvis transaksjoner som skjer etter midnatt, skal posteres som en del av dagen før.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="fbc1b-124">Velg Ja i **Del etter utdragsmetode** hvis du vil at utdrag skal opprettes for hver definerte utdragsmetode.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="fbc1b-125">Dette kan være nyttig hvis resultatet av posteringen må forbedres for butikker med høye transaksjonsvolumer siden det vil opprette mange mindre utdrag som kan behandles parallelt.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="fbc1b-126">I hurtigfanen **Generelt** i feltet **Standardkunde** kan du velge kundekontoen som skal brukes for salg til kunder som kommer inn i butikken.</span><span class="sxs-lookup"><span data-stu-id="fbc1b-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  


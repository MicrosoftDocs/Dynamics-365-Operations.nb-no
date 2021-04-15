---
title: " Butikkonfigurasjoner for detaljhandelsutdrag"
description: Denne prosedyren beskriver konfigurasjoner for butikken som påvirker hvordan Commerce-utdrag opprettes og posteres.
author: jashanno
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da862af25df241ad42b7e1ade3fdca19f6280278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804119"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="77f7c-103"> Butikkonfigurasjoner for detaljhandelsutdrag</span><span class="sxs-lookup"><span data-stu-id="77f7c-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77f7c-104">Denne prosedyren beskriver konfigurasjoner for butikken som påvirker hvordan Commerce-utdrag opprettes og posteres.</span><span class="sxs-lookup"><span data-stu-id="77f7c-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="77f7c-105">Finansdimensjoner i butikker dekkes i en annen prosedyre.</span><span class="sxs-lookup"><span data-stu-id="77f7c-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="77f7c-106">Denne prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="77f7c-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="77f7c-107">I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Kanaler > Butikker > Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="77f7c-107">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="77f7c-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="77f7c-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="77f7c-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="77f7c-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="77f7c-110">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="77f7c-110">Click **Edit**.</span></span>
5. <span data-ttu-id="77f7c-111">Innstillingene i hurtigfanen **Utdrag/avslutning** kan påvirke opprettingen av utdrag, validering og postering for butikken.</span><span class="sxs-lookup"><span data-stu-id="77f7c-111">The settings in the **Statement/closing** FastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="77f7c-112">Utvid hurtigfanen **Utdrag/avslutning**.</span><span class="sxs-lookup"><span data-stu-id="77f7c-112">Expand the **Statement/closing** FastTab.</span></span>  
6. <span data-ttu-id="77f7c-113">Velg metoden du vil bruke for å gruppere utdragslinjene, i **Utdragsmetode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="77f7c-113">In the **Statement method** field, select the method you want to use to group the statement lines by.</span></span>  
7. <span data-ttu-id="77f7c-114">Velg Ja i **Ett utdrag per dag** hvis det bare skal opprettes ett utdrag per dag når utdrag opprettes fra den satsvise jobben for utdragsoppretting.</span><span class="sxs-lookup"><span data-stu-id="77f7c-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="77f7c-115">Feltet **Beregning av kasseoppgjør** definerer om kasseoppgjør skal legges sammen, eller om den siste skal brukes.</span><span class="sxs-lookup"><span data-stu-id="77f7c-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="77f7c-116">Velg finanskontoen som avrundingsdifferanser skal posteres mot, i **Avrunding**-feltet.</span><span class="sxs-lookup"><span data-stu-id="77f7c-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="77f7c-117">I feltet **Maksimal avrundingsdifferanse** angir du maksimalt tillatt avrundingsdifferanse.</span><span class="sxs-lookup"><span data-stu-id="77f7c-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="77f7c-118">Angi den maksimale totale posteringsdifferansen som er tillatt for et utdrag, i **Postering**-feltet.</span><span class="sxs-lookup"><span data-stu-id="77f7c-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="77f7c-119">Angi den maksimale totale differansen i et skift i et utdrag, i **Skift**-feltet.</span><span class="sxs-lookup"><span data-stu-id="77f7c-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="77f7c-120">I **Transaksjon**-feltet angir du den maksimale totale differansen i en utdragslinje.</span><span class="sxs-lookup"><span data-stu-id="77f7c-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="77f7c-121">I feltet **Avslutningsmetode** definerer du om transaksjonene som skal inkluderes i et utdrag, skal være en del av en lukket skift, eller om de kan være enhver transaksjon i det definerte dato-/klokkeslettintervallet.</span><span class="sxs-lookup"><span data-stu-id="77f7c-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="77f7c-122">I feltet **Slutt på arbeidsdag** angir du et tidspunkt hvis transaksjoner som skjer etter midnatt, skal posteres på forrige dag.</span><span class="sxs-lookup"><span data-stu-id="77f7c-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="77f7c-123">Velg Ja i **Poster som arbeidsdag** hvis transaksjoner som skjer etter midnatt, skal posteres som en del av dagen før.</span><span class="sxs-lookup"><span data-stu-id="77f7c-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="77f7c-124">Velg Ja i **Del etter utdragsmetode** hvis du vil at utdrag skal opprettes for hver definerte utdragsmetode.</span><span class="sxs-lookup"><span data-stu-id="77f7c-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="77f7c-125">Dette kan være nyttig hvis resultatet av posteringen må forbedres for butikker med høye transaksjonsvolumer siden det vil opprette mange mindre utdrag som kan behandles parallelt.</span><span class="sxs-lookup"><span data-stu-id="77f7c-125">This action can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="77f7c-126">I hurtigfanen **Generelt** i feltet **Standardkunde** kan du velge kundekontoen som skal brukes for salg til kunder som kommer inn i butikken.</span><span class="sxs-lookup"><span data-stu-id="77f7c-126">In the **General** FastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
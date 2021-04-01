---
title: Initialisere lagernivåer i lageret
description: Denne prosedyren viser hvordan du får lagerbeholdningen oppdatert manuelt ved hjelp av en varetilgangsjournal.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c1e5ca96919acde7e850292a73ebd00185f1f7a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244481"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="72ad7-103">Initialisere lagernivåer i lageret</span><span class="sxs-lookup"><span data-stu-id="72ad7-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72ad7-104">Denne prosedyren viser hvordan du får lagerbeholdningen oppdatert manuelt ved hjelp av en varetilgangsjournal.</span><span class="sxs-lookup"><span data-stu-id="72ad7-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="72ad7-105">(Det er også mulig å oppdatere lagerbeholdningen ved å importere transaksjonene i data-enheter.) Du kan kjøre denne veiledningen i demonstrasjonsdataselskapet USMF der alle forutsetninger som journalnavn, vareoppsett, posteringsprofiler, og kontoer er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="72ad7-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="72ad7-106">Veiledningen foreslår bestemte verdier for varen og dimensjonene som brukes.</span><span class="sxs-lookup"><span data-stu-id="72ad7-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="72ad7-107">Hvis du velger en annen vare, må du kanskje angi verdier for forskjellige dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="72ad7-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="72ad7-108">Gå til Lagerstyring > Journaloppføringer > Varer > Bevegelse.</span><span class="sxs-lookup"><span data-stu-id="72ad7-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="72ad7-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="72ad7-109">Click New.</span></span>
3. <span data-ttu-id="72ad7-110">Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="72ad7-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="72ad7-111">Velg IMov.</span><span class="sxs-lookup"><span data-stu-id="72ad7-111">Select IMov.</span></span>
    * <span data-ttu-id="72ad7-112">Det er lurt å bruke forskjellige journalnavnmaler for forskjellige forretningsformål.</span><span class="sxs-lookup"><span data-stu-id="72ad7-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="72ad7-113">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="72ad7-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="72ad7-114">Angi verdiene 140200 i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="72ad7-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="72ad7-115">Dette er motkontoen som skal være standardkonto på journallinjene.</span><span class="sxs-lookup"><span data-stu-id="72ad7-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="72ad7-116">Det er mulig å overstyre standarden for å tilordne forskjellige motkontoer per linje.</span><span class="sxs-lookup"><span data-stu-id="72ad7-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="72ad7-117">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="72ad7-117">Click OK.</span></span>
8. <span data-ttu-id="72ad7-118">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="72ad7-118">Click New.</span></span>
9. <span data-ttu-id="72ad7-119">Klikk på rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="72ad7-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="72ad7-120">Velg vare A0001.</span><span class="sxs-lookup"><span data-stu-id="72ad7-120">Select item A0001.</span></span>
11. <span data-ttu-id="72ad7-121">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="72ad7-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="72ad7-122">Klikk på fanen Lagerdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="72ad7-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="72ad7-123">Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="72ad7-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="72ad7-124">Velg område 1.</span><span class="sxs-lookup"><span data-stu-id="72ad7-124">Select site 1.</span></span>
15. <span data-ttu-id="72ad7-125">Klikk på rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="72ad7-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="72ad7-126">Velg lager 13.</span><span class="sxs-lookup"><span data-stu-id="72ad7-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="72ad7-127">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="72ad7-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="72ad7-128">Klikk på rullegardinknappen i Lokasjon-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="72ad7-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="72ad7-129">Velg lokasjon 13.</span><span class="sxs-lookup"><span data-stu-id="72ad7-129">Select location 13.</span></span>
20. <span data-ttu-id="72ad7-130">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="72ad7-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="72ad7-131">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="72ad7-131">Click Save.</span></span>
22. <span data-ttu-id="72ad7-132">Klikk på Poster.</span><span class="sxs-lookup"><span data-stu-id="72ad7-132">Click Post.</span></span>
23. <span data-ttu-id="72ad7-133">Merk av eller fjern merket i boksen Overfør alle posteringsfeil til en ny journal.</span><span class="sxs-lookup"><span data-stu-id="72ad7-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="72ad7-134">Hvis du aktiverer dette alternativet, kopieres eventuelle linjer som ikke kan posteres, til en ny journal.</span><span class="sxs-lookup"><span data-stu-id="72ad7-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="72ad7-135">Du kan bruke informasjonen i loggen til å rette opp problemene og deretter postere linjene på nytt.</span><span class="sxs-lookup"><span data-stu-id="72ad7-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="72ad7-136">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="72ad7-136">Click OK.</span></span>
25. <span data-ttu-id="72ad7-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="72ad7-137">Close the page.</span></span>
26. <span data-ttu-id="72ad7-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="72ad7-138">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Opprette telefonsenterkanaler og definere kanalattributter
description: Dette hjelper med å opprette en ny detaljhandelkanal og definere kanalattributter.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4b6db1bfdaf17cd857a0a08515f1e0413994bd6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023541"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="ddecd-103">Opprette telefonsenterkanaler og definere kanalattributter</span><span class="sxs-lookup"><span data-stu-id="ddecd-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ddecd-104">Dette hjelper med å opprette en ny handelskanal og definere kanalattributter.</span><span class="sxs-lookup"><span data-stu-id="ddecd-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="ddecd-105">Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="ddecd-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="ddecd-106">Denne fremgangsmåten er ment for rollen IT for handel.</span><span class="sxs-lookup"><span data-stu-id="ddecd-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="ddecd-107">Opprett ny butikk</span><span class="sxs-lookup"><span data-stu-id="ddecd-107">Create new store</span></span>
1. <span data-ttu-id="ddecd-108">Gå til Alle arbeidsområder > Kanaldistribusjon.</span><span class="sxs-lookup"><span data-stu-id="ddecd-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="ddecd-109">Klikk på Ny kanal.</span><span class="sxs-lookup"><span data-stu-id="ddecd-109">Click New channel.</span></span>
3. <span data-ttu-id="ddecd-110">Klikk på Butikk.</span><span class="sxs-lookup"><span data-stu-id="ddecd-110">Click Store.</span></span>
4. <span data-ttu-id="ddecd-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ddecd-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ddecd-112">Skriv inn en verdi i feltet Butikknummer.</span><span class="sxs-lookup"><span data-stu-id="ddecd-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="ddecd-113">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ddecd-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ddecd-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ddecd-116">Velg et alternativ i feltet Tidssone for butikk.</span><span class="sxs-lookup"><span data-stu-id="ddecd-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="ddecd-117">Klikk rullegardinknappen i feltet Kanalprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ddecd-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ddecd-119">Klikk rullegardinknappen i feltet Språk for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="ddecd-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="ddecd-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="ddecd-122">Klikk rullegardinknappen i feltet Mva-gruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="ddecd-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ddecd-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ddecd-125">Klikk rullegardinknappen i feltet Adressebok for kunde for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ddecd-126">Velg adresseboken som brukes til å knytte kunder til denne butikken.</span><span class="sxs-lookup"><span data-stu-id="ddecd-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="ddecd-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="ddecd-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="ddecd-129">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="ddecd-129">Click Select.</span></span>
22. <span data-ttu-id="ddecd-130">Klikk rullegardinknappen i feltet Adressebok for ansatt for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ddecd-131">Velg adresseboken som brukes til å knytte kasserere til denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="ddecd-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="ddecd-133">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="ddecd-134">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="ddecd-134">Click Select.</span></span>
26. <span data-ttu-id="ddecd-135">Klikk rullegardinknappen i feltet Standardkunde for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="ddecd-136">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="ddecd-137">Vis eller skjul delen Skjermoppsett.</span><span class="sxs-lookup"><span data-stu-id="ddecd-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="ddecd-138">Klikk rullegardinknappen i feltet Skjermoppsett-ID for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ddecd-139">Velg standard POS-skjermoppsettet for denne butikken.</span><span class="sxs-lookup"><span data-stu-id="ddecd-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="ddecd-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="ddecd-141">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="ddecd-142">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ddecd-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="ddecd-143">Klikk på Kanalattributter.</span><span class="sxs-lookup"><span data-stu-id="ddecd-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="ddecd-144">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ddecd-144">Click New.</span></span>
35. <span data-ttu-id="ddecd-145">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="ddecd-146">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="ddecd-147">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="ddecd-148">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ddecd-148">Click Save.</span></span>
39. <span data-ttu-id="ddecd-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ddecd-149">Close the page.</span></span>
40. <span data-ttu-id="ddecd-150">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ddecd-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="ddecd-151">Klikk Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="ddecd-151">Click Payment methods.</span></span>
42. <span data-ttu-id="ddecd-152">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ddecd-152">Click New.</span></span>
43. <span data-ttu-id="ddecd-153">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="ddecd-154">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="ddecd-155">Vis eller skjul delen Postering.</span><span class="sxs-lookup"><span data-stu-id="ddecd-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="ddecd-156">Angi ønskede verdier i Kontonummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="ddecd-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="ddecd-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ddecd-157">Click Save.</span></span>
48. <span data-ttu-id="ddecd-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ddecd-158">Close the page.</span></span>
49. <span data-ttu-id="ddecd-159">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ddecd-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="ddecd-160">Klikk på Kontantoppgjør.</span><span class="sxs-lookup"><span data-stu-id="ddecd-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="ddecd-161">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ddecd-161">Click New.</span></span>
52. <span data-ttu-id="ddecd-162">Angi et tall i feltet Beløp i transaksjonsvaluta.</span><span class="sxs-lookup"><span data-stu-id="ddecd-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="ddecd-163">Klikk rullegardinknappen i Valuta-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="ddecd-164">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="ddecd-165">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="ddecd-166">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ddecd-166">Click Save.</span></span>
57. <span data-ttu-id="ddecd-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ddecd-167">Close the page.</span></span>
58. <span data-ttu-id="ddecd-168">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ddecd-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="ddecd-169">Klikk på Tilordning av butikklokatorgruppe.</span><span class="sxs-lookup"><span data-stu-id="ddecd-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="ddecd-170">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ddecd-170">Click New.</span></span>
61. <span data-ttu-id="ddecd-171">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="ddecd-172">Klikk rullegardinknappen i feltet Lokatorgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ddecd-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="ddecd-173">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="ddecd-174">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ddecd-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="ddecd-175">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ddecd-175">Click Save.</span></span>
66. <span data-ttu-id="ddecd-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ddecd-176">Close the page.</span></span>


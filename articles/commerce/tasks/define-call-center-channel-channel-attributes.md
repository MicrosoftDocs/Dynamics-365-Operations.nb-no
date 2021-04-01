---
title: Opprette telefonsenterkanaler og definere kanalattributter
description: Dette hjelper med å opprette en ny kanal og definere kanalattributter.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e4ef84abcfd0948c46c5312078f2a940840144
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256955"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="baca2-103">Opprette telefonsenterkanaler og definere kanalattributter</span><span class="sxs-lookup"><span data-stu-id="baca2-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="baca2-104">Dette hjelper med å opprette en ny handelskanal og definere kanalattributter.</span><span class="sxs-lookup"><span data-stu-id="baca2-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="baca2-105">Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="baca2-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="baca2-106">Denne fremgangsmåten er ment for rollen IT for handel.</span><span class="sxs-lookup"><span data-stu-id="baca2-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="baca2-107">Opprett ny butikk</span><span class="sxs-lookup"><span data-stu-id="baca2-107">Create new store</span></span>
1. <span data-ttu-id="baca2-108">Gå til Alle arbeidsområder > Kanaldistribusjon.</span><span class="sxs-lookup"><span data-stu-id="baca2-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="baca2-109">Klikk på Ny kanal.</span><span class="sxs-lookup"><span data-stu-id="baca2-109">Click New channel.</span></span>
3. <span data-ttu-id="baca2-110">Klikk på Butikk.</span><span class="sxs-lookup"><span data-stu-id="baca2-110">Click Store.</span></span>
4. <span data-ttu-id="baca2-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="baca2-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="baca2-112">Skriv inn en verdi i feltet Butikknummer.</span><span class="sxs-lookup"><span data-stu-id="baca2-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="baca2-113">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="baca2-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="baca2-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="baca2-116">Velg et alternativ i feltet Tidssone for butikk.</span><span class="sxs-lookup"><span data-stu-id="baca2-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="baca2-117">Klikk rullegardinknappen i feltet Kanalprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="baca2-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="baca2-119">Klikk rullegardinknappen i feltet Språk for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="baca2-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="baca2-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="baca2-122">Klikk rullegardinknappen i feltet Mva-gruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="baca2-123">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="baca2-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="baca2-125">Klikk rullegardinknappen i feltet Adressebok for kunde for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="baca2-126">Velg adresseboken som brukes til å knytte kunder til denne butikken.</span><span class="sxs-lookup"><span data-stu-id="baca2-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="baca2-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="baca2-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="baca2-129">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="baca2-129">Click Select.</span></span>
22. <span data-ttu-id="baca2-130">Klikk rullegardinknappen i feltet Adressebok for ansatt for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="baca2-131">Velg adresseboken som brukes til å knytte kasserere til denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="baca2-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="baca2-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="baca2-133">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="baca2-134">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="baca2-134">Click Select.</span></span>
26. <span data-ttu-id="baca2-135">Klikk rullegardinknappen i feltet Standardkunde for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="baca2-136">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="baca2-137">Vis eller skjul delen Skjermoppsett.</span><span class="sxs-lookup"><span data-stu-id="baca2-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="baca2-138">Klikk rullegardinknappen i feltet Skjermoppsett-ID for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="baca2-139">Velg standard POS-skjermoppsettet for denne butikken.</span><span class="sxs-lookup"><span data-stu-id="baca2-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="baca2-140">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="baca2-141">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="baca2-142">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="baca2-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="baca2-143">Klikk på Kanalattributter.</span><span class="sxs-lookup"><span data-stu-id="baca2-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="baca2-144">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="baca2-144">Click New.</span></span>
35. <span data-ttu-id="baca2-145">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="baca2-146">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="baca2-147">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="baca2-148">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="baca2-148">Click Save.</span></span>
39. <span data-ttu-id="baca2-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="baca2-149">Close the page.</span></span>
40. <span data-ttu-id="baca2-150">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="baca2-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="baca2-151">Klikk Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="baca2-151">Click Payment methods.</span></span>
42. <span data-ttu-id="baca2-152">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="baca2-152">Click New.</span></span>
43. <span data-ttu-id="baca2-153">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="baca2-154">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="baca2-155">Vis eller skjul delen Postering.</span><span class="sxs-lookup"><span data-stu-id="baca2-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="baca2-156">Angi ønskede verdier i Kontonummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="baca2-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="baca2-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="baca2-157">Click Save.</span></span>
48. <span data-ttu-id="baca2-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="baca2-158">Close the page.</span></span>
49. <span data-ttu-id="baca2-159">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="baca2-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="baca2-160">Klikk på Kontantoppgjør.</span><span class="sxs-lookup"><span data-stu-id="baca2-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="baca2-161">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="baca2-161">Click New.</span></span>
52. <span data-ttu-id="baca2-162">Angi et tall i feltet Beløp i transaksjonsvaluta.</span><span class="sxs-lookup"><span data-stu-id="baca2-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="baca2-163">Klikk rullegardinknappen i Valuta-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="baca2-164">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="baca2-165">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="baca2-166">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="baca2-166">Click Save.</span></span>
57. <span data-ttu-id="baca2-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="baca2-167">Close the page.</span></span>
58. <span data-ttu-id="baca2-168">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="baca2-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="baca2-169">Klikk på Tilordning av butikklokatorgruppe.</span><span class="sxs-lookup"><span data-stu-id="baca2-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="baca2-170">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="baca2-170">Click New.</span></span>
61. <span data-ttu-id="baca2-171">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="baca2-172">Klikk rullegardinknappen i feltet Lokatorgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="baca2-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="baca2-173">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="baca2-174">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="baca2-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="baca2-175">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="baca2-175">Click Save.</span></span>
66. <span data-ttu-id="baca2-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="baca2-176">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: " Definere fordelsprogrammer"
description: Denne prosedyren viser hvordan du konfigurerer et fordelsprogram med to fordelslag.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b178f1c6a71b34b70db4dbcd1765117215a4d2a1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023538"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="511da-103"> Definere fordelsprogrammer</span><span class="sxs-lookup"><span data-stu-id="511da-103">Define loyalty programs</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="511da-104">Denne prosedyren viser hvordan du konfigurerer et fordelsprogram med to fordelslag.</span><span class="sxs-lookup"><span data-stu-id="511da-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="511da-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="511da-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="511da-106">Gå til Detaljhandel og handel > ...</span><span class="sxs-lookup"><span data-stu-id="511da-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="511da-107">> Fordelsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="511da-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="511da-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="511da-108">Click New.</span></span>
3. <span data-ttu-id="511da-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="511da-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="511da-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="511da-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="511da-111">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="511da-111">Click Add line.</span></span>
6. <span data-ttu-id="511da-112">Angi et nummer i Nivå-feltet.</span><span class="sxs-lookup"><span data-stu-id="511da-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="511da-113">Angi et navn på fordelslaget i Lag-feltet.</span><span class="sxs-lookup"><span data-stu-id="511da-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="511da-114">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="511da-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="511da-115">Klikk rullegardinknappen i feltet Datointervall for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="511da-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="511da-116">Dette datointervallet må være frem i tid.</span><span class="sxs-lookup"><span data-stu-id="511da-116">This date interval should extend into the future.</span></span> <span data-ttu-id="511da-117">Hvis datointervallet som er valgt for gullnivå, for eksempel er en periode på ett år, kan kunder som kvalifiserer for gullnivået motta fordelene som er tilordnet gullnivået, i ett år.</span><span class="sxs-lookup"><span data-stu-id="511da-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="511da-118">Hvis kunder kvalifiserer seg for gullnivået på nytt mens de er på dette nivået, utsettes utløpsdatoen for nivået med enda et år fra den dagen de kvalifiserer seg på nytt.</span><span class="sxs-lookup"><span data-stu-id="511da-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="511da-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="511da-120">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="511da-120">Click Add line.</span></span>
12. <span data-ttu-id="511da-121">Angi et nummer i Nivå-feltet.</span><span class="sxs-lookup"><span data-stu-id="511da-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="511da-122">Angi et navn på fordelslaget i Lag-feltet.</span><span class="sxs-lookup"><span data-stu-id="511da-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="511da-123">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="511da-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="511da-124">Klikk rullegardinknappen i feltet Datointervall for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="511da-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="511da-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="511da-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="511da-126">Click Save.</span></span>
18. <span data-ttu-id="511da-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="511da-128">Lagregler definerer det minste antallet fordelspoeng som må være opptjent i en tidsperiode for å kvalifisere for laget.</span><span class="sxs-lookup"><span data-stu-id="511da-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="511da-129">Aktiver/deaktiver utvidelsen av delen Regler for lag.</span><span class="sxs-lookup"><span data-stu-id="511da-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="511da-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="511da-130">Click New.</span></span>
    * <span data-ttu-id="511da-131">Du kan ha mer enn én lagregel per lag.</span><span class="sxs-lookup"><span data-stu-id="511da-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="511da-132">Du kan for eksempel har tre ulike kriterier for å oppnå et lag: ved å bruke 500 kroner på én måned, ved å bruke 1000 kroner over ett år og ved å ha 20 transaksjoner på ett år.</span><span class="sxs-lookup"><span data-stu-id="511da-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="511da-133">Hvis du vil gjøre dette, må du opprette tre lagregler.</span><span class="sxs-lookup"><span data-stu-id="511da-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="511da-134">Klikk rullegardinknappen i feltet Fordelspoeng for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="511da-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="511da-135">Dette bør være fordelspoeng som ikke kan innløses.</span><span class="sxs-lookup"><span data-stu-id="511da-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="511da-136">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="511da-137">Angi et nummer i feltet Minimalt antall utstedte poeng.</span><span class="sxs-lookup"><span data-stu-id="511da-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="511da-138">For det laveste nivålaget angir du 0 hvis alle kunder kvalifiserer seg bare ved å delta i programmet.</span><span class="sxs-lookup"><span data-stu-id="511da-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="511da-139">Klikk rullegardinknappen i feltet Datointervall for evaluering for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="511da-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="511da-140">Dette datointervallet må strekke seg bakover i tid.</span><span class="sxs-lookup"><span data-stu-id="511da-140">This date interval should extend into the past.</span></span> <span data-ttu-id="511da-141">Bare poeng som opptjenes i dette datointervallet skal telles mot en oppnåelse av verdien for minimalt antall utstedte poeng.</span><span class="sxs-lookup"><span data-stu-id="511da-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="511da-142">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="511da-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="511da-143">Click Save.</span></span>
27. <span data-ttu-id="511da-144">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="511da-145">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="511da-145">Click New.</span></span>
29. <span data-ttu-id="511da-146">Klikk rullegardinknappen i feltet Fordelspoeng for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="511da-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="511da-147">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="511da-148">Angi et nummer i feltet Minimalt antall utstedte poeng.</span><span class="sxs-lookup"><span data-stu-id="511da-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="511da-149">Klikk rullegardinknappen i feltet Datointervall for evaluering for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="511da-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="511da-150">Dette datointervallet må strekke seg bakover i tid.</span><span class="sxs-lookup"><span data-stu-id="511da-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="511da-151">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="511da-152">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="511da-152">Click Save.</span></span>
35. <span data-ttu-id="511da-153">Klikk Prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="511da-153">Click Price groups.</span></span>
    * <span data-ttu-id="511da-154">Hvis du vil gi lojale kunder rabatter,</span><span class="sxs-lookup"><span data-stu-id="511da-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="511da-155">må du tilordne én eller flere prisgrupper til fordelsprogrammet og tilordne prisgruppene til rabatter.</span><span class="sxs-lookup"><span data-stu-id="511da-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="511da-156">Det er lurt ikke å blande prisgrupper på tvers av forskjellige typer rabattenheter.</span><span class="sxs-lookup"><span data-stu-id="511da-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="511da-157">Ikke bruk for eksempel den samme prisgruppen for en fordelsrabatt og en kanalrabatt.</span><span class="sxs-lookup"><span data-stu-id="511da-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="511da-158">Klikk rullegardinknappen i Prisgruppe-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="511da-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="511da-159">Prisgruppekoblingen øverst på siden er til fordelsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="511da-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="511da-160">Prisgruppekoblingen i hurtigfanen Programnivåer er bare for et bestemt fordelslag.</span><span class="sxs-lookup"><span data-stu-id="511da-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="511da-161">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="511da-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="511da-162">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="511da-162">Click Save.</span></span>
39. <span data-ttu-id="511da-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="511da-163">Close the page.</span></span>
40. <span data-ttu-id="511da-164">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="511da-164">Click Save.</span></span>


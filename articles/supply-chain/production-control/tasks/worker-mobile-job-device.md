--- 
title: Konfigurere en arbeider som bruker den mobile jobbenheten
description: Denne prosedyren viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 449c8411b06303a470aba279f85fb904ca1ad3c2
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="692ed-103">Konfigurere en arbeider som bruker den mobile jobbenheten</span><span class="sxs-lookup"><span data-stu-id="692ed-103">Configure a worker using the mobile job device</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="692ed-104">Denne prosedyren viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.</span><span class="sxs-lookup"><span data-stu-id="692ed-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="692ed-105">Tilordne roller til brukerkonto</span><span class="sxs-lookup"><span data-stu-id="692ed-105">Assign roles to user account</span></span>
1. <span data-ttu-id="692ed-106">Gå til Systemadministrasjon > Brukere > Brukere.</span><span class="sxs-lookup"><span data-stu-id="692ed-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="692ed-107">Bruke hurtigfilteret til å filtrere på navnet på en arbeider der brukerkontoen er knyttet til maskinoperatørrollen.</span><span class="sxs-lookup"><span data-stu-id="692ed-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="692ed-108">I eksempeldataene er navnet Shannon.</span><span class="sxs-lookup"><span data-stu-id="692ed-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="692ed-109">Merk brukerkontooppføringen.</span><span class="sxs-lookup"><span data-stu-id="692ed-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="692ed-110">Klikk koblingen Navn i den merkede raden i listen for å vise detaljene om brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="692ed-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="692ed-111">Velg Roller\Maskinoperatør i treet.</span><span class="sxs-lookup"><span data-stu-id="692ed-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="692ed-112">Lukk siden med brukerkontodetaljer.</span><span class="sxs-lookup"><span data-stu-id="692ed-112">Close the user account details page.</span></span>
7. <span data-ttu-id="692ed-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="692ed-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="692ed-114">Konfigurer brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="692ed-114">Configure worker account.</span></span>
1. <span data-ttu-id="692ed-115">Gå til Personale > Arbeidere > Arbeidere.</span><span class="sxs-lookup"><span data-stu-id="692ed-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="692ed-116">Bruke hurtigfilteret til å filtrere på navnet på en arbeider der brukerkontoen er knyttet til maskinoperatørrollen.</span><span class="sxs-lookup"><span data-stu-id="692ed-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="692ed-117">I eksempeldataene er navnet Shannon.</span><span class="sxs-lookup"><span data-stu-id="692ed-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="692ed-118">Merk brukerkontooppføringen.</span><span class="sxs-lookup"><span data-stu-id="692ed-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="692ed-119">Klikk koblingen Navn i den merkede raden i listen for å vise detaljene om brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="692ed-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="692ed-120">Klikk kategorien Ansettelse.</span><span class="sxs-lookup"><span data-stu-id="692ed-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="692ed-121">Utvid hurtigfanen Tidsregistrering og klikk Aktiver på registreringsterminaler.</span><span class="sxs-lookup"><span data-stu-id="692ed-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="692ed-122">Klikk Aktiver på registreringsterminaler.</span><span class="sxs-lookup"><span data-stu-id="692ed-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="692ed-123">Angi eller velg en verdi i Beregningsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="692ed-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="692ed-124">Angi eller velg en verdi i feltet Standard beregningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="692ed-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="692ed-125">Angi eller velg en verdi i Godkjenningsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="692ed-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="692ed-126">Angi eller velg en verdi i Godkjenningsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="692ed-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="692ed-127">Angi eller velg en verdi i Profilgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="692ed-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="692ed-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="692ed-128">Click OK.</span></span>
14. <span data-ttu-id="692ed-129">Klikk Rediger for å angi et kortnummer for den nye tidsregistreringsarbeideren.</span><span class="sxs-lookup"><span data-stu-id="692ed-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="692ed-130">Skriv inn en verdi i feltet Kort-ID.</span><span class="sxs-lookup"><span data-stu-id="692ed-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="692ed-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="692ed-131">Click Save.</span></span>
17. <span data-ttu-id="692ed-132">Bruk snarveien for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="692ed-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="692ed-133">Lukk siden med arbeiderdetaljene.</span><span class="sxs-lookup"><span data-stu-id="692ed-133">Close the worker details page.</span></span>
19. <span data-ttu-id="692ed-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="692ed-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="692ed-135">Tilordne arbeider til enhetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="692ed-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="692ed-136">Gå til Produksjonskontroll > Oppsett > Produksjonsutførelse > Konfigurer jobbkort for enheter.</span><span class="sxs-lookup"><span data-stu-id="692ed-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="692ed-137">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="692ed-137">Click Add.</span></span>
3. <span data-ttu-id="692ed-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="692ed-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="692ed-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="692ed-139">Click OK.</span></span>
5. <span data-ttu-id="692ed-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="692ed-140">Click Edit.</span></span>
6. <span data-ttu-id="692ed-141">Du kan angi standardfilteret for arbeideren i Produksjonsenhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="692ed-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="692ed-142">Dette sikrer at bare produksjonsjobber for den valgte produksjonsenheten vises når arbeideren logger på enheten.</span><span class="sxs-lookup"><span data-stu-id="692ed-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="692ed-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="692ed-143">Close the page.</span></span>


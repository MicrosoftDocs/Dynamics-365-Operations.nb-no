---
title: Konfigurere en arbeider som bruker den mobile jobbenheten
description: Denne prosedyren viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "327395"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="3df96-103">Konfigurere en arbeider som bruker den mobile jobbenheten</span><span class="sxs-lookup"><span data-stu-id="3df96-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3df96-104">Denne prosedyren viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.</span><span class="sxs-lookup"><span data-stu-id="3df96-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="3df96-105">Tilordne roller til brukerkonto</span><span class="sxs-lookup"><span data-stu-id="3df96-105">Assign roles to user account</span></span>
1. <span data-ttu-id="3df96-106">Gå til Systemadministrasjon > Brukere > Brukere.</span><span class="sxs-lookup"><span data-stu-id="3df96-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="3df96-107">Bruke hurtigfilteret til å filtrere på navnet på en arbeider der brukerkontoen er knyttet til maskinoperatørrollen.</span><span class="sxs-lookup"><span data-stu-id="3df96-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="3df96-108">I eksempeldataene er navnet Shannon.</span><span class="sxs-lookup"><span data-stu-id="3df96-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="3df96-109">Merk brukerkontooppføringen.</span><span class="sxs-lookup"><span data-stu-id="3df96-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="3df96-110">Klikk koblingen Navn i den merkede raden i listen for å vise detaljene om brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="3df96-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="3df96-111">Velg Roller\Maskinoperatør i treet.</span><span class="sxs-lookup"><span data-stu-id="3df96-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="3df96-112">Lukk siden med brukerkontodetaljer.</span><span class="sxs-lookup"><span data-stu-id="3df96-112">Close the user account details page.</span></span>
7. <span data-ttu-id="3df96-113">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3df96-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="3df96-114">Konfigurer brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="3df96-114">Configure worker account.</span></span>
1. <span data-ttu-id="3df96-115">Gå til Personale > Arbeidere > Arbeidere.</span><span class="sxs-lookup"><span data-stu-id="3df96-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="3df96-116">Bruke hurtigfilteret til å filtrere på navnet på en arbeider der brukerkontoen er knyttet til maskinoperatørrollen.</span><span class="sxs-lookup"><span data-stu-id="3df96-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="3df96-117">I eksempeldataene er navnet Shannon.</span><span class="sxs-lookup"><span data-stu-id="3df96-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="3df96-118">Merk brukerkontooppføringen.</span><span class="sxs-lookup"><span data-stu-id="3df96-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="3df96-119">Klikk koblingen Navn i den merkede raden i listen for å vise detaljene om brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="3df96-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="3df96-120">Klikk kategorien Ansettelse.</span><span class="sxs-lookup"><span data-stu-id="3df96-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="3df96-121">Utvid hurtigfanen Tidsregistrering og klikk Aktiver på registreringsterminaler.</span><span class="sxs-lookup"><span data-stu-id="3df96-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="3df96-122">Klikk Aktiver på registreringsterminaler.</span><span class="sxs-lookup"><span data-stu-id="3df96-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="3df96-123">Angi eller velg en verdi i Beregningsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="3df96-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="3df96-124">Angi eller velg en verdi i feltet Standard beregningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3df96-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="3df96-125">Angi eller velg en verdi i Godkjenningsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="3df96-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="3df96-126">Angi eller velg en verdi i Godkjenningsgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="3df96-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="3df96-127">Angi eller velg en verdi i Profilgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="3df96-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="3df96-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3df96-128">Click OK.</span></span>
14. <span data-ttu-id="3df96-129">Klikk Rediger for å angi et kortnummer for den nye tidsregistreringsarbeideren.</span><span class="sxs-lookup"><span data-stu-id="3df96-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="3df96-130">Skriv inn en verdi i feltet Kort-ID.</span><span class="sxs-lookup"><span data-stu-id="3df96-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="3df96-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3df96-131">Click Save.</span></span>
17. <span data-ttu-id="3df96-132">Bruk snarveien for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="3df96-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="3df96-133">Lukk siden med arbeiderdetaljene.</span><span class="sxs-lookup"><span data-stu-id="3df96-133">Close the worker details page.</span></span>
19. <span data-ttu-id="3df96-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3df96-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="3df96-135">Tilordne arbeider til enhetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3df96-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="3df96-136">Gå til Produksjonskontroll > Oppsett > Produksjonsutførelse > Konfigurer jobbkort for enheter.</span><span class="sxs-lookup"><span data-stu-id="3df96-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="3df96-137">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="3df96-137">Click Add.</span></span>
3. <span data-ttu-id="3df96-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3df96-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3df96-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3df96-139">Click OK.</span></span>
5. <span data-ttu-id="3df96-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="3df96-140">Click Edit.</span></span>
6. <span data-ttu-id="3df96-141">Du kan angi standardfilteret for arbeideren i Produksjonsenhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="3df96-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="3df96-142">Dette sikrer at bare produksjonsjobber for den valgte produksjonsenheten vises når arbeideren logger på enheten.</span><span class="sxs-lookup"><span data-stu-id="3df96-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="3df96-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3df96-143">Close the page.</span></span>


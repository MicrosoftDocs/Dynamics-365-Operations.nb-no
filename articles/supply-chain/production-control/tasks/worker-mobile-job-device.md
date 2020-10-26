---
title: Konfigurere en arbeider som bruker den mobile jobbenheten
description: Dette emnet viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ada42a98a8a87e377f939d063b17f9904f6b3408
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978240"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="8491f-103">Konfigurere en arbeider som bruker den mobile jobbenheten</span><span class="sxs-lookup"><span data-stu-id="8491f-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8491f-104">Dette emnet viser hvordan du kan tilordne riktige roller til brukerkontoen til en arbeider, og deretter la arbeideren foreta registreringer med Shop Floor.</span><span class="sxs-lookup"><span data-stu-id="8491f-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="8491f-105">Kontrollere at en arbeider er tilordnet en bestemt rolle</span><span class="sxs-lookup"><span data-stu-id="8491f-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="8491f-106">I dette eksemplet må du kontrollere at brukeren "SHANNON" er tilordnet maskinoperatørrollen før du konfigurerer arbeiderkontoen.</span><span class="sxs-lookup"><span data-stu-id="8491f-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="8491f-107">Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Brukere > Brukere** .</span><span class="sxs-lookup"><span data-stu-id="8491f-107">Go to **Navigation pane > Modules > System administration > Users > Users** .</span></span>
2. <span data-ttu-id="8491f-108">Søk etter en bruker i hurtigfilteret.</span><span class="sxs-lookup"><span data-stu-id="8491f-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="8491f-109">I dette eksemplet angir du `shannon`.</span><span class="sxs-lookup"><span data-stu-id="8491f-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="8491f-110">Velg koblingen i kolonnen **bruker-ID** for brukerkontoen som vises.</span><span class="sxs-lookup"><span data-stu-id="8491f-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="8491f-111">I **Brukerroller** -treet velger du **Roller > Maskinoperatør** .</span><span class="sxs-lookup"><span data-stu-id="8491f-111">In the **User's roles** tree, select **Roles > Machine operator** .</span></span>
5. <span data-ttu-id="8491f-112">Lukk sidene **Brukerdetaljer** og **Brukere** for å gå tilbake til hjemmesiden.</span><span class="sxs-lookup"><span data-stu-id="8491f-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="8491f-113">Konfigurere brukerkonto</span><span class="sxs-lookup"><span data-stu-id="8491f-113">Configure worker account</span></span>
1. <span data-ttu-id="8491f-114">Gå til **Navigasjonsrute > Moduler > Personale > Arbeidere > Arbeidere** .</span><span class="sxs-lookup"><span data-stu-id="8491f-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers** .</span></span>
2. <span data-ttu-id="8491f-115">Søk etter en bruker i hurtigfilteret.</span><span class="sxs-lookup"><span data-stu-id="8491f-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="8491f-116">I dette eksemplet angir du `shannon`.</span><span class="sxs-lookup"><span data-stu-id="8491f-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="8491f-117">Velg koblingen i kolonnen **Navn** for brukerkontoen som vises.</span><span class="sxs-lookup"><span data-stu-id="8491f-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="8491f-118">Velg kategorien **Tidsregistrering** .</span><span class="sxs-lookup"><span data-stu-id="8491f-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="8491f-119">Velg **Aktiver på registreringsterminaler** .</span><span class="sxs-lookup"><span data-stu-id="8491f-119">Select **Activate on registration terminals** .</span></span>
6. <span data-ttu-id="8491f-120">Angi eller velg verdier i følgende felt:</span><span class="sxs-lookup"><span data-stu-id="8491f-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="8491f-121">**Beregningsgruppe**</span><span class="sxs-lookup"><span data-stu-id="8491f-121">**Calculation group**</span></span>  
    - <span data-ttu-id="8491f-122">**Standard beregningsgruppe**</span><span class="sxs-lookup"><span data-stu-id="8491f-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="8491f-123">**Godkjenningsgruppe**</span><span class="sxs-lookup"><span data-stu-id="8491f-123">**Approval group**</span></span>  
    - <span data-ttu-id="8491f-124">**Standardprofil**</span><span class="sxs-lookup"><span data-stu-id="8491f-124">**Standard profile**</span></span>  
    - <span data-ttu-id="8491f-125">**Profilgruppe**</span><span class="sxs-lookup"><span data-stu-id="8491f-125">**Profile group**</span></span>  

7. <span data-ttu-id="8491f-126">Velg **OK** .</span><span class="sxs-lookup"><span data-stu-id="8491f-126">Select **OK** .</span></span>
8. <span data-ttu-id="8491f-127">Velg **Rediger** for å angi et kortnummer for den nye tidsregistreringsarbeideren.</span><span class="sxs-lookup"><span data-stu-id="8491f-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="8491f-128">Angi en verdi i feltet **Kort-ID** .</span><span class="sxs-lookup"><span data-stu-id="8491f-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="8491f-129">Velg **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="8491f-129">Select **Save** .</span></span>
10. <span data-ttu-id="8491f-130">Lukk sidene **Arbeiderdetaljer** og **Arbeidere** .</span><span class="sxs-lookup"><span data-stu-id="8491f-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="8491f-131">Tilordne arbeider til enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="8491f-131">Assign worker to device group</span></span>
1. <span data-ttu-id="8491f-132">Gå til **Produksjonskontroll > Oppsett > Produksjonsutførelse > Konfigurer jobbkort for enheter** .</span><span class="sxs-lookup"><span data-stu-id="8491f-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices** .</span></span>
2. <span data-ttu-id="8491f-133">Velg **Legg til** .</span><span class="sxs-lookup"><span data-stu-id="8491f-133">Select **Add** .</span></span>
3. <span data-ttu-id="8491f-134">Velg ønsket arbeider i listen.</span><span class="sxs-lookup"><span data-stu-id="8491f-134">In the list, select the desired worker.</span></span> <span data-ttu-id="8491f-135">I dette eksemplet velger du **SHANNON** .</span><span class="sxs-lookup"><span data-stu-id="8491f-135">For this example, select **SHANNON** .</span></span>
4. <span data-ttu-id="8491f-136">Velg **OK** .</span><span class="sxs-lookup"><span data-stu-id="8491f-136">Select **OK** .</span></span>
5. <span data-ttu-id="8491f-137">Velg **Rediger** .</span><span class="sxs-lookup"><span data-stu-id="8491f-137">Select **Edit** .</span></span>
6. <span data-ttu-id="8491f-138">Du kan angi standardfilteret for arbeideren i **Produksjonsenhet** -feltet.</span><span class="sxs-lookup"><span data-stu-id="8491f-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="8491f-139">Dette sikrer at bare produksjonsjobber for den valgte produksjonsenheten vises når arbeideren logger på enheten.</span><span class="sxs-lookup"><span data-stu-id="8491f-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="8491f-140">Angi den ønskede verdien.</span><span class="sxs-lookup"><span data-stu-id="8491f-140">Enter the desired value.</span></span>
7. <span data-ttu-id="8491f-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8491f-141">Close the page.</span></span>


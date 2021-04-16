---
title: Oppsett av dobbel skriving fra Lifecycle Services
description: Dette emnet forklarer hvordan du konfigurerer en tilkobling med dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e51b4ef1e309e5f89dc82a3776b88c505dc6593d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748547"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="73510-103">Oppsett av dobbel skriving fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="73510-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="73510-104">Dette emnet forklarer hvordan du konfigurerer en dobbel skriving-tilkobling mellom et nytt Finance and Operations-miljø og et nytt Dataverse-miljø fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="73510-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="73510-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="73510-105">Prerequisites</span></span>

<span data-ttu-id="73510-106">Du må være administrator for å kunne konfigurere en tilkobling med dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="73510-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="73510-107">Du må ha tilgang til leieren.</span><span class="sxs-lookup"><span data-stu-id="73510-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="73510-108">Du må være administrator i både Finance and Operations-miljøer og Dataverse-miljøer.</span><span class="sxs-lookup"><span data-stu-id="73510-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="73510-109">Konfigurere en tilkobling med dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="73510-109">Set up a dual-write connection</span></span>

<span data-ttu-id="73510-110">Hvis du vil konfigurere en tilkobling med dobbel skriving, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="73510-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="73510-111">Gå til prosjektet I LCS.</span><span class="sxs-lookup"><span data-stu-id="73510-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="73510-112">Velg **Konfigurer** for å distribuere et nytt miljø.</span><span class="sxs-lookup"><span data-stu-id="73510-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="73510-113">Velg versjonen.</span><span class="sxs-lookup"><span data-stu-id="73510-113">Select the version.</span></span> 
4. <span data-ttu-id="73510-114">Velg topologien.</span><span class="sxs-lookup"><span data-stu-id="73510-114">Select the topology.</span></span> <span data-ttu-id="73510-115">Hvis bare én topologi er tilgjengelig, velges den automatisk.</span><span class="sxs-lookup"><span data-stu-id="73510-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="73510-116">Fullfør de første trinnene i veiviseren for **distribusjonsinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="73510-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="73510-117">Følg deretter at av disse trinnene i fanen **Dataverse**:</span><span class="sxs-lookup"><span data-stu-id="73510-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="73510-118">Hvis et Dataverse-miljø allerede er klargjort for leieren, kan du velge det.</span><span class="sxs-lookup"><span data-stu-id="73510-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="73510-119">Sett alternativet **Konfigurere Dataverse** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="73510-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="73510-120">I kolonnen **Tilgjengelige miljøer** velger du miljøet som skal integreres med Finance and Operations-dataene.</span><span class="sxs-lookup"><span data-stu-id="73510-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="73510-121">Listen inneholder alle miljøer der du har administrative rettigheter.</span><span class="sxs-lookup"><span data-stu-id="73510-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="73510-122">Merk av for **Godta** for å angi at du godtar vilkårene og betingelsene.</span><span class="sxs-lookup"><span data-stu-id="73510-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse-fanen når et Dataverse-miljø allerede er klargjort for leieren](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="73510-124">Hvis leieren ikke allerede har et Dataverse-miljø, blir et nytt miljø klargjort.</span><span class="sxs-lookup"><span data-stu-id="73510-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="73510-125">Sett alternativet **Konfigurere Dataverse** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="73510-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="73510-126">Skriv inn et navn for Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="73510-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="73510-127">Velg regionen som miljøet skal distribueres i.</span><span class="sxs-lookup"><span data-stu-id="73510-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="73510-128">Velg standard språk og valuta for miljøet.</span><span class="sxs-lookup"><span data-stu-id="73510-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="73510-129">Du kan ikke endre språket og valutaen senere.</span><span class="sxs-lookup"><span data-stu-id="73510-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="73510-130">Merk av for **Godta** for å angi at du godtar vilkårene og betingelsene.</span><span class="sxs-lookup"><span data-stu-id="73510-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse-fanen når leieren ikke allerede har et Dataverse-miljø](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="73510-132">Fullfør resten av trinnene i veiviseren for **Distribusjonsinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="73510-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="73510-133">Når miljøet har statusen **Distribuert**, åpner du siden for miljødetaljer.</span><span class="sxs-lookup"><span data-stu-id="73510-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="73510-134">Delen **Power Platform-integrering** viser navnene på Finance and Operations-miljøet og Dataverse-miljøet som er koblet sammen.</span><span class="sxs-lookup"><span data-stu-id="73510-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Delen Power Platform-integrering](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="73510-136">En administrator av Finance and Operations-miljøet må logge på LCS og velge **Kobling til CDS for apper** for å fullføre koblingen.</span><span class="sxs-lookup"><span data-stu-id="73510-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="73510-137">Siden for miljødetaljer viser administratorens kontaktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="73510-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="73510-138">Når koblingen er fullført, oppdateres statusen til **Miljøkoblingen er fullført**.</span><span class="sxs-lookup"><span data-stu-id="73510-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="73510-139">Hvis du vil åpne arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet og kontrollere hvilke maler som er tilgjengelige, velger du **Kobling til CDS for apper**.</span><span class="sxs-lookup"><span data-stu-id="73510-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Knappen Kobling til CDS for apper i delen Power Platform-integrering](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="73510-141">Du kan ikke koble fra miljøer ved hjelp av LCS.</span><span class="sxs-lookup"><span data-stu-id="73510-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="73510-142">Hvis du vil oppheve koblingen til et miljø, åpner du arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet, og deretter velger du **Koble fra**.</span><span class="sxs-lookup"><span data-stu-id="73510-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
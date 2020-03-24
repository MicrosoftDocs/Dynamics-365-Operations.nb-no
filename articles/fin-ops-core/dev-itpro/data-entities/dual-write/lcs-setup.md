---
title: Oppsett av dobbel skriving fra Lifecycle Services
description: Dette emnet forklarer hvordan du konfigurerer en dobbel skriving-tilkobling mellom et nytt Finance and Operations-miljø og et nytt Common Data Service-miljø fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 75765c0cc03c64030fac6bc656f57a143828b85b
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112494"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="74724-103">Oppsett av dobbel skriving fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="74724-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="74724-104">Dette emnet forklarer hvordan du konfigurerer en dobbel skriving-tilkobling mellom et nytt Finance and Operations-miljø og et nytt Common Data Service-miljø fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="74724-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="74724-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="74724-105">Prerequisites</span></span>

<span data-ttu-id="74724-106">Du må være administrator for å kunne konfigurere en tilkobling med dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="74724-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="74724-107">Du må ha tilgang til leieren.</span><span class="sxs-lookup"><span data-stu-id="74724-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="74724-108">Du må være administrator i både Finance and Operations-miljøer og Common Data Service-miljøer.</span><span class="sxs-lookup"><span data-stu-id="74724-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="74724-109">Konfigurere en tilkobling med dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="74724-109">Set up a dual-write connection</span></span>

<span data-ttu-id="74724-110">Hvis du vil konfigurere en tilkobling med dobbel skriving, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="74724-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="74724-111">Gå til prosjektet I LCS.</span><span class="sxs-lookup"><span data-stu-id="74724-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="74724-112">Velg **Konfigurer** for å distribuere et nytt miljø.</span><span class="sxs-lookup"><span data-stu-id="74724-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="74724-113">Velg versjonen.</span><span class="sxs-lookup"><span data-stu-id="74724-113">Select the version.</span></span> 
4. <span data-ttu-id="74724-114">Velg topologien.</span><span class="sxs-lookup"><span data-stu-id="74724-114">Select the topology.</span></span> <span data-ttu-id="74724-115">Hvis bare én topologi er tilgjengelig, velges den automatisk.</span><span class="sxs-lookup"><span data-stu-id="74724-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="74724-116">Fullfør de første trinnene i veiviseren for **distribusjonsinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="74724-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="74724-117">Følg deretter at av disse trinnene i fanen **Common Data Service**:</span><span class="sxs-lookup"><span data-stu-id="74724-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="74724-118">Hvis et Common Data Service-miljø allerede er klargjort for leieren, kan du velge det.</span><span class="sxs-lookup"><span data-stu-id="74724-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="74724-119">Sett alternativet **Konfigurere Common Data Service** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="74724-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="74724-120">I feltet **tilgjengelige miljøer** velger du miljøet som skal integreres med Finance and Operations-dataene.</span><span class="sxs-lookup"><span data-stu-id="74724-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="74724-121">Listen inneholder alle miljøer der du har administrative rettigheter.</span><span class="sxs-lookup"><span data-stu-id="74724-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="74724-122">Merk av for **Godta** for å angi at du godtar vilkårene og betingelsene.</span><span class="sxs-lookup"><span data-stu-id="74724-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service-fanen når et Common Data Service-miljø allerede er klargjort for leieren](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="74724-124">Hvis leieren ikke allerede har et Common Data Service-miljø, blir et nytt miljø klargjort.</span><span class="sxs-lookup"><span data-stu-id="74724-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="74724-125">Sett alternativet **Konfigurere Common Data Service** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="74724-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="74724-126">Skriv inn et navn for Common Data Service-miljøet.</span><span class="sxs-lookup"><span data-stu-id="74724-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="74724-127">Velg regionen som miljøet skal distribueres i.</span><span class="sxs-lookup"><span data-stu-id="74724-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="74724-128">Velg standard språk og valuta for miljøet.</span><span class="sxs-lookup"><span data-stu-id="74724-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="74724-129">Du kan ikke endre språket og valutaen senere.</span><span class="sxs-lookup"><span data-stu-id="74724-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="74724-130">Merk av for **Godta** for å angi at du godtar vilkårene og betingelsene.</span><span class="sxs-lookup"><span data-stu-id="74724-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service-kategorien når leieren ikke allerede har et Common Data Service-miljø](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="74724-132">Fullfør resten av trinnene i veiviseren for **Distribusjonsinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="74724-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="74724-133">Når miljøet har statusen **Distribuert**, åpner du siden for miljødetaljer.</span><span class="sxs-lookup"><span data-stu-id="74724-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="74724-134">Delen **Common Data Service-miljøinformasjon** viser navnene på Finance and Operations-miljøet og Common Data Service-miljøet som er koblet.</span><span class="sxs-lookup"><span data-stu-id="74724-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Delen Common Data Service-miljøinformasjon](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="74724-136">En administrator av Finance and Operations-miljøet må logge på LCS og velge **Kobling til CDS for apper** for å fullføre koblingen.</span><span class="sxs-lookup"><span data-stu-id="74724-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="74724-137">Siden for miljødetaljer viser administratorens kontaktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="74724-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="74724-138">Når koblingen er fullført, oppdateres statusen til **Miljøkoblingen er fullført**.</span><span class="sxs-lookup"><span data-stu-id="74724-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="74724-139">Hvis du vil åpne arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet og kontrollere hvilke maler som er tilgjengelige, velger du **Kobling til CDS for apper**.</span><span class="sxs-lookup"><span data-stu-id="74724-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Knappen Kobling til CDS for apper i delen Common Data Service-miljøinformasjon](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="74724-141">Du kan ikke koble fra miljøer ved hjelp av LCS.</span><span class="sxs-lookup"><span data-stu-id="74724-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="74724-142">Hvis du vil oppheve koblingen til et miljø, åpner du arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet, og deretter velger du **Koble fra**.</span><span class="sxs-lookup"><span data-stu-id="74724-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

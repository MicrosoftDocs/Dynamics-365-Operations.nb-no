---
title: Oppsett av dobbel skriving fra Lifecycle Services
description: Dette emnet forklarer hvordan du konfigurerer en tilkobling med dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103575"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="9a0ba-103">Oppsett av dobbel skriving fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="9a0ba-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9a0ba-104">Dette emnet forklarer hvordan du aktiverer dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9a0ba-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9a0ba-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="9a0ba-105">Prerequisites</span></span>

<span data-ttu-id="9a0ba-106">Du må fullføre Power Platform-integreringen som beskrevet i følgende emner:</span><span class="sxs-lookup"><span data-stu-id="9a0ba-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="9a0ba-107">Power Platform-integrering - Aktiver under miljødistribusjon</span><span class="sxs-lookup"><span data-stu-id="9a0ba-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="9a0ba-108">Power Platform-integrering - Konfigurere etter miljødistribusjon</span><span class="sxs-lookup"><span data-stu-id="9a0ba-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="9a0ba-109">Konfigurere dobbel skriving for nye Dataverse-miljøer</span><span class="sxs-lookup"><span data-stu-id="9a0ba-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="9a0ba-110">Følg denne fremgangsmåten for å konfigurere en dobbelt skriving fra LCS-siden **Miljødetaljer**:</span><span class="sxs-lookup"><span data-stu-id="9a0ba-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="9a0ba-111">På siden **Miljødetaljer** utvides delen **Power Platform-integrering**.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="9a0ba-112">Velg knappen for **App med dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform-integrering](media/powerplat_integration_step2.png)

3. <span data-ttu-id="9a0ba-114">Gå gjennom vilkårene og betingelsene, og merk deretter av for **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="9a0ba-115">Velg **OK** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="9a0ba-116">Du kan overvåke fremdriften ved å oppdatere siden med miljødetaljer regelmessig.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="9a0ba-117">Oppsettet tar vanligvis 30 minutter eller mindre.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="9a0ba-118">Når installasjonen er fullført, får du en melding om prosessen var vellykket eller om det oppstod en feil.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="9a0ba-119">Hvis installasjonen mislyktes, vises det en relatert feilmelding.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="9a0ba-120">Du må korrigere eventuelle feil før du går til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="9a0ba-121">Velg **Koble til Power Platform-miljø** for å opprette en kobling mellom Dataverse og databasene for det gjeldende miljøet.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="9a0ba-122">Dette tar vanligvis 5 minutter eller mindre.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Koble til Power Platform-miljø":::

8. <span data-ttu-id="9a0ba-124">Når koblingen er fullført, vises en hyperkobling.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="9a0ba-125">Bruk koblingen til å logge deg på administrasjonsområdet for dobbel skriving i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="9a0ba-126">Derfra kan du definere enhetstilordninger.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="9a0ba-127">Konfigurere dobbel skriving for et eksisterende Dataverse-miljø</span><span class="sxs-lookup"><span data-stu-id="9a0ba-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="9a0ba-128">Hvis du vil definere skrivetilgang for et eksisterende Dataverse-miljø, må du opprette en Microsoft [støtteforespørsel](../../lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="9a0ba-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="9a0ba-129">Denne forespørselen må inneholde følgende:</span><span class="sxs-lookup"><span data-stu-id="9a0ba-129">The ticket must include:</span></span>

+ <span data-ttu-id="9a0ba-130">Finance and Operations-miljø-ID.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="9a0ba-131">Miljønavnet fra Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="9a0ba-132">Dataverse-organisasjons-IDen eller Power Platform-miljø-IDen fra Power Platform-administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="9a0ba-133">Be om at IDen er forekomsten som brukes for Power Platform-integrering, i forespørselen.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="9a0ba-134">Du kan ikke koble fra miljøer ved hjelp av LCS.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="9a0ba-135">Hvis du vil oppheve koblingen til et miljø, åpner du arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet, og deretter velger du **Koble fra**.</span><span class="sxs-lookup"><span data-stu-id="9a0ba-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

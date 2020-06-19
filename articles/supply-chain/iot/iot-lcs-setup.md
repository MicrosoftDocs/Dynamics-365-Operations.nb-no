---
title: Installere tillegget for IoT-intelligens i LCS
description: Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386545"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="41f23-103">Installere tillegget for IoT-intelligens i LCS</span><span class="sxs-lookup"><span data-stu-id="41f23-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41f23-104">Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="41f23-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="41f23-105">Før du kan installere tillegget, må du [opprette Azure-ressursene](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="41f23-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="41f23-106">Definere LCS-miljøet</span><span class="sxs-lookup"><span data-stu-id="41f23-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="41f23-107">Åpne LCS og gå til Microsoft Dynamics 365 Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="41f23-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="41f23-108">Bla til delen **Miljøtillegg**.</span><span class="sxs-lookup"><span data-stu-id="41f23-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="41f23-109">Velg **Installer et nytt tillegg** for å vise listen over tillegg som er aktivert for miljøet.</span><span class="sxs-lookup"><span data-stu-id="41f23-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="41f23-110">I dialogboksen **Velg et tillegg som skal installeres** velger du **IoT-intelligens**.</span><span class="sxs-lookup"><span data-stu-id="41f23-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="41f23-111">I dialogboksen **Konfigurer tillegg** angir du detaljene for IoT-huben og Redis-bufferen.</span><span class="sxs-lookup"><span data-stu-id="41f23-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="41f23-112">Du kan finne de nødvendige verdiene i nøkkelhvelvet du opprettet i [Opprett Azure-ressurser](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="41f23-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="41f23-113">**Leier-ID** – Gå til nøkkelhvelvet i Azure-portalen, og velg deretter **Oversikt** i navigasjonsruten til venstre og kopier verdien **Katalog-ID**.</span><span class="sxs-lookup"><span data-stu-id="41f23-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="41f23-114">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="41f23-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="41f23-115">**URI for nøkkelhvelv for hub-kompatibelt endepunkt for IoT-hendelse** – Gå til nøkkelhvelvet, og velg deretter **Oversikt** i navigasjonsruten til venstre, og kopier verdien **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="41f23-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="41f23-116">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="41f23-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="41f23-117">**Hemmelig navn for hub-kompatibelt endepunkt for IoT-hendelse** – Gå til nøkkelhvelvet, og deretter velger du **Hemmeligheter** i navigasjonsruten til venstre, og kopierer navnet på hemmeligheten der tilkoblingsstrengen for hendelseshuben for IoT-huben er lagret.</span><span class="sxs-lookup"><span data-stu-id="41f23-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="41f23-118">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="41f23-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="41f23-119">**URI for nøkkelhvelv for Redis-buffer** – Gå til nøkkelhvelvet, og velg deretter **Oversikt** i navigasjonsruten til venstre, og kopier verdien **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="41f23-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="41f23-120">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="41f23-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="41f23-121">**Hemmelig navn for endepunkt for Redis-buffer** – Gå til nøkkelhvelvet, og deretter velger du **Hemmeligheter** i navigasjonsruten til venstre, og kopierer navnet på hemmeligheten der tilkoblingsstrengen for Redis-bufferen er lagret.</span><span class="sxs-lookup"><span data-stu-id="41f23-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="41f23-122">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="41f23-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="41f23-123">Merk av i avmerkingsboksen for å godta vilkårene og betingelsene.</span><span class="sxs-lookup"><span data-stu-id="41f23-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="41f23-124">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="41f23-124">Select **Install**.</span></span>
8. <span data-ttu-id="41f23-125">Det vises en melding som sier at tillegget ble utløst for installasjon.</span><span class="sxs-lookup"><span data-stu-id="41f23-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="41f23-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="41f23-126">Select **OK**.</span></span>

<span data-ttu-id="41f23-127">LCS-installasjonen er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="41f23-127">LCS setup is now completed.</span></span> <span data-ttu-id="41f23-128">Det neste trinnet er å [definere scenarioene](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="41f23-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="41f23-129">Avinstallere tillegget</span><span class="sxs-lookup"><span data-stu-id="41f23-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="41f23-130">I Supply Chain Management [deaktiverer du scenarioene](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="41f23-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="41f23-131">I LCS går du til detaljene for Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="41f23-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="41f23-132">Bla til delen **Miljøtillegg**.</span><span class="sxs-lookup"><span data-stu-id="41f23-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="41f23-133">Velg **Avinstaller** for tillegget for IoT-intelligens.</span><span class="sxs-lookup"><span data-stu-id="41f23-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
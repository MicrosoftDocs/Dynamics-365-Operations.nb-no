---
title: Installere tillegget for IoT-intelligens i LCS
description: Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d1cc9a7535be05a3e466c27e53047d694cf0160
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826449"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="7cca0-103">Installere tillegget for IoT-intelligens i LCS</span><span class="sxs-lookup"><span data-stu-id="7cca0-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7cca0-104">Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7cca0-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7cca0-105">Legg merke til at tillegg ikke kan installeres i et demo-/prøvemiljø.</span><span class="sxs-lookup"><span data-stu-id="7cca0-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="7cca0-106">Før du kan installere tillegget, må du [opprette Azure-ressursene](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="7cca0-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="7cca0-107">Definere LCS-miljøet</span><span class="sxs-lookup"><span data-stu-id="7cca0-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="7cca0-108">Åpne LCS og gå til Microsoft Dynamics 365 Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="7cca0-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="7cca0-109">Bla til delen **Miljøtillegg**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="7cca0-110">Velg **Installer et nytt tillegg** for å vise listen over tillegg som er aktivert for miljøet.</span><span class="sxs-lookup"><span data-stu-id="7cca0-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="7cca0-111">I dialogboksen **Velg et tillegg som skal installeres** velger du **IoT-intelligens**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="7cca0-112">I dialogboksen **Konfigurer tillegg** angir du detaljene for IoT-huben og Redis-bufferen.</span><span class="sxs-lookup"><span data-stu-id="7cca0-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="7cca0-113">Du kan finne de nødvendige verdiene i nøkkelhvelvet du opprettet i [Opprett Azure-ressurser](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="7cca0-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="7cca0-114">**Leier-ID** – Gå til nøkkelhvelvet i Azure-portalen, og velg deretter **Oversikt** i navigasjonsruten til venstre og kopier verdien **Katalog-ID**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="7cca0-115">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="7cca0-116">**URI for nøkkelhvelv for hub-kompatibelt endepunkt for IoT-hendelse** – Gå til nøkkelhvelvet, og velg deretter **Oversikt** i navigasjonsruten til venstre, og kopier verdien **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="7cca0-117">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="7cca0-118">**Hemmelig navn for hub-kompatibelt endepunkt for IoT-hendelse** – Gå til nøkkelhvelvet, og deretter velger du **Hemmeligheter** i navigasjonsruten til venstre, og kopierer navnet på hemmeligheten der tilkoblingsstrengen for hendelseshuben for IoT-huben er lagret.</span><span class="sxs-lookup"><span data-stu-id="7cca0-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="7cca0-119">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="7cca0-120">**URI for nøkkelhvelv for Redis-buffer** – Gå til nøkkelhvelvet, og velg deretter **Oversikt** i navigasjonsruten til venstre, og kopier verdien **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="7cca0-121">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="7cca0-122">**Hemmelig navn for endepunkt for Redis-buffer** – Gå til nøkkelhvelvet, og deretter velger du **Hemmeligheter** i navigasjonsruten til venstre, og kopierer navnet på hemmeligheten der tilkoblingsstrengen for Redis-bufferen er lagret.</span><span class="sxs-lookup"><span data-stu-id="7cca0-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="7cca0-123">Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="7cca0-124">Merk av i avmerkingsboksen for å godta vilkårene og betingelsene.</span><span class="sxs-lookup"><span data-stu-id="7cca0-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="7cca0-125">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-125">Select **Install**.</span></span>
8. <span data-ttu-id="7cca0-126">Det vises en melding som sier at tillegget ble utløst for installasjon.</span><span class="sxs-lookup"><span data-stu-id="7cca0-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="7cca0-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-127">Select **OK**.</span></span>

<span data-ttu-id="7cca0-128">LCS-installasjonen er nå fullført.</span><span class="sxs-lookup"><span data-stu-id="7cca0-128">LCS setup is now completed.</span></span> <span data-ttu-id="7cca0-129">Det neste trinnet er å [definere scenarioene](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="7cca0-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="7cca0-130">Avinstallere tillegget</span><span class="sxs-lookup"><span data-stu-id="7cca0-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="7cca0-131">I Supply Chain Management [deaktiverer du scenarioene](iot-scenario-setup.md#disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="7cca0-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="7cca0-132">I LCS går du til detaljene for Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="7cca0-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="7cca0-133">Bla til delen **Miljøtillegg**.</span><span class="sxs-lookup"><span data-stu-id="7cca0-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="7cca0-134">Velg **Avinstaller** for tillegget for IoT-intelligens.</span><span class="sxs-lookup"><span data-stu-id="7cca0-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
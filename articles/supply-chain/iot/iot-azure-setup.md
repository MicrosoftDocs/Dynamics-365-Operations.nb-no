---
title: Konfigurere Azure-ressurser for IoT-intelligens
description: Dette emnet forklarer hvordan du oppretter og konfigurerer Microsoft Azure-ressursene du krever for IoT-intelligens.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f728f3b5736bc7368ffb39bf2be398fb91fb373e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224960"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="eb2f0-103">Konfigurere Azure-ressurser for IoT-intelligens</span><span class="sxs-lookup"><span data-stu-id="eb2f0-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb2f0-104">Dette emnet forklarer hvordan du oppretter og konfigurerer Microsoft Azure-ressursene du krever for IoT-intelligens.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="eb2f0-105">Opprette Azure-ressurser</span><span class="sxs-lookup"><span data-stu-id="eb2f0-105">Create Azure resources</span></span>

<span data-ttu-id="eb2f0-106">Følg denne fremgangsmåten for å opprette en IoT-hub, en Redis-buffer og et nøkkelhvelv som Microsoft kan få tilgang til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="eb2f0-107">Kontrollerer at ID-en for førstepartsappen for Microsoft Dynamics ERP Microservices er i leieren din</span><span class="sxs-lookup"><span data-stu-id="eb2f0-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="eb2f0-108">Hvis du vil kontrollere at ID-en for førstepartsappen for Microsoft Dynamics ERP Microservices er i leieren din, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="eb2f0-109">Logg på Azure-portalen på <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="eb2f0-110">Gå til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="eb2f0-111">Gå til **Enterprise-apper**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="eb2f0-112">I feltet **Apptype** velger du **Microsoft-apper**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="eb2f0-113">I søkefeltet angir du **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="eb2f0-114">Kontroller at **Microsoft Dynamics ERP Microservices** er i listen.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="eb2f0-115">Andre apper har lignende navn.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-115">Other applications have similar names.</span></span> <span data-ttu-id="eb2f0-116">Kontroller derfor at du finner riktig app.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="eb2f0-117">App-ID-en er **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="eb2f0-118">Hvis appen ikke finnes i listen, må du legge den til i leieren din:</span><span class="sxs-lookup"><span data-stu-id="eb2f0-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="eb2f0-119">På verktøylinjen i Azure-portalen velger du knappen for å åpne Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="eb2f0-120">Kjør kommandoen **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="eb2f0-121">Angi **Y** for å installere modulen.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="eb2f0-122">Kjør kommandoen **Get-InstalledModule -Name "AzureAD"** for å kontrollere at modulen er installert.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="eb2f0-123">Kjør kommandoen **Connect-AzureAD -Confirm** for å kjøre godkjenningen.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="eb2f0-124">Kjør kommandoen **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="eb2f0-125">Du kan nå gjenta trinn 1 til og med 6 for å kontrollere at app-ID-en er i leieren.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="eb2f0-126">Opprette en nøkkelhvelvressurs</span><span class="sxs-lookup"><span data-stu-id="eb2f0-126">Create a key vault resource</span></span>

<span data-ttu-id="eb2f0-127">Hvis du vil opprette en nøkkelhvelvressurs, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="eb2f0-128">Opprett eller gå til en ressursgruppe i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="eb2f0-129">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-129">Select **Add**.</span></span>
3. <span data-ttu-id="eb2f0-130">På siden **Ny** i søkefeltet angir du **Nøkkelhvelv**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="eb2f0-131">Velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-131">Then select **Create**.</span></span>
4. <span data-ttu-id="eb2f0-132">På siden **Opprett nøkkelhvelv** i feltet **Navn på nøkkelhvelv** angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="eb2f0-133">Gå gjennom standardverdiene, og velg deretter **Se gjennom + Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="eb2f0-134">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-134">Select **Create**.</span></span>

<span data-ttu-id="eb2f0-135">Nøkkelhvelvet blir opprettet i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="eb2f0-136">Opprette en IoT-hubressurs</span><span class="sxs-lookup"><span data-stu-id="eb2f0-136">Create an IoT hub resource</span></span>

<span data-ttu-id="eb2f0-137">Hvis du vil opprette en IoT-ressurs, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="eb2f0-138">Opprett eller gå til en ressursgruppe.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="eb2f0-139">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-139">Select **Add**.</span></span>
3. <span data-ttu-id="eb2f0-140">På siden **Ny** i søkefeltet angir du **IoT-hub**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="eb2f0-141">Velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-141">Then select **Create**.</span></span>
4. <span data-ttu-id="eb2f0-142">I feltet **Navn på IoT-hub** angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="eb2f0-143">Gå gjennom standardverdiene, og velg deretter **Se gjennom + Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="eb2f0-144">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-144">Select **Create**.</span></span>

<span data-ttu-id="eb2f0-145">IoT-huben blir opprettet i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="eb2f0-146">Det anbefales at du oppretter bare én IoT-hubressurs per miljø.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="eb2f0-147">Opprette en ressurs for Redis-buffer</span><span class="sxs-lookup"><span data-stu-id="eb2f0-147">Create a Redis cache resource</span></span>

<span data-ttu-id="eb2f0-148">Hvis du vil opprette en ressurs for Redis-buffer, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="eb2f0-149">Opprett eller gå til en ressursgruppe.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="eb2f0-150">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-150">Select **Add**.</span></span>
3. <span data-ttu-id="eb2f0-151">På siden **Ny** i søkefeltet angir du **Azure-buffer for Redis**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="eb2f0-152">Velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-152">Then select **Create**.</span></span>
4. <span data-ttu-id="eb2f0-153">I feltet **DNS-navn** angir du et navn.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="eb2f0-154">Gå gjennom standardverdiene, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="eb2f0-155">Redis-bufferen blir opprettet i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="eb2f0-156">Det anbefales at du oppretter bare én Redis-buffer per miljø.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="eb2f0-157">Alle ressursene er nå opprettet.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="eb2f0-158">Konfigurere Azure-ressursene</span><span class="sxs-lookup"><span data-stu-id="eb2f0-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="eb2f0-159">Konfigurere IoT-huben</span><span class="sxs-lookup"><span data-stu-id="eb2f0-159">Configure the IoT hub</span></span>

<span data-ttu-id="eb2f0-160">Hvis du vil konfigurere IOT-huben, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="eb2f0-161">Velg IoT-hubressursen i ressursene.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="eb2f0-162">I navigasjonsruten til venstre velger du **Innebygde endepunkter**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="eb2f0-163">Under **Forbrukergrupper** limer du inn følgende forbrukergrupper.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="eb2f0-164">Disse forbrukergruppene samsvarer med de bruksklare scenarioene.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="eb2f0-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="eb2f0-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="eb2f0-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="eb2f0-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="eb2f0-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="eb2f0-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="eb2f0-168">Konfigurere nøkkelhvelvet</span><span class="sxs-lookup"><span data-stu-id="eb2f0-168">Configure the key vault</span></span>

<span data-ttu-id="eb2f0-169">Hvis du vil konfigurere nøkkelhvelvet, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="eb2f0-170">Velg ressursen for nøkkelhvelv i ressursene.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="eb2f0-171">Velg **Tilgangspolicyer** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="eb2f0-172">Velg **Legg til en tilgangspolicy**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="eb2f0-173">På siden **Legg til tilgangspolicy** velger du **Hent** og **Liste** i feltet **Velg tillatelser**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="eb2f0-174">Klikk på i **Velg oppdragsgiver**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="eb2f0-175">I dialogboksen **Oppdragsgiver** søke rdu etter og velger **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="eb2f0-176">Velg deretter **Velg**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-176">Then select **Select**.</span></span>
7. <span data-ttu-id="eb2f0-177">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-177">Select **Add**.</span></span>
8. <span data-ttu-id="eb2f0-178">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-178">Select **Save**.</span></span>

<span data-ttu-id="eb2f0-179">Appen har nå tilgang til hemmelighetene i nøkkelhvelvet.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="eb2f0-180">Lagre hemmeligheten for tilkoblingsstrengen for IoT-huben</span><span class="sxs-lookup"><span data-stu-id="eb2f0-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="eb2f0-181">Hvis du vil lagre hemmeligheten for tilkoblingsstrengen for IoT-huben, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="eb2f0-182">Velg IoT-hubressursen i ressursene.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="eb2f0-183">I navigasjonsruten til venstre velger du **Innebygde endepunkter**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="eb2f0-184">Kopier verdien i feltet **Hub-kompatibelt endepunkt for hendelse**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="eb2f0-185">Gå til ressursen for nøkkelhvelv.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="eb2f0-186">Velg **Hemmeligheter** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="eb2f0-187">Velg **Generer/Importer**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="eb2f0-188">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="eb2f0-189">I feltet **Verdi** limer du inn endepunktverdien du kopierte tidligere.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="eb2f0-190">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="eb2f0-191">Lagre hemmeligheten for tilkoblingsstrengen for Redis-bufferen</span><span class="sxs-lookup"><span data-stu-id="eb2f0-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="eb2f0-192">Hvis du vil lagre hemmeligheten for tilkoblingsstrengen for Redis-bufferen, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="eb2f0-193">Velg ressursen for Redis-buffer i ressursene.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="eb2f0-194">Velg **Tilgangstaster**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="eb2f0-195">Kopier verdien i feltet **Primær tilkoblingsstreng**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="eb2f0-196">Gå til ressursen for nøkkelhvelv.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="eb2f0-197">Velg **Hemmeligheter** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="eb2f0-198">Velg **Generer/Importer**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="eb2f0-199">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="eb2f0-200">I feltet **Verdi** limer du inn tilkoblingsstrengen du kopierte tidligere.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="eb2f0-201">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="eb2f0-202">Når du oppdaterer en av tilkoblingsstrengene, må du også oppdatere de hemmelige verdiene.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="eb2f0-203">Du har nå fullført klargjøringen av de obligatoriske Azure-ressursene.</span><span class="sxs-lookup"><span data-stu-id="eb2f0-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="eb2f0-204">Neste trinn er å [installere tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="eb2f0-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
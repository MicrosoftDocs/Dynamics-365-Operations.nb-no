---
title: Tillegg for lagersynlighet
description: Dette emnet beskriver hvordan du installerer og konfigurerer tillegget for lagersynlighet for Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114676"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="1b548-103">Tillegg for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="1b548-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="1b548-104">Tillegget for lagersynlighet er en uavhengig og høyt skalerbar mikrotjeneste som aktiverer beholdningssporing i sanntid, og gir dermed en global visning av lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="1b548-105">All informasjon som er relatert til lagerbeholdningen, eksporteres til tjenesten via i SQL-integrasjon med minimal forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="1b548-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="1b548-106">Eksterne systemer får tilgang til tjenesten via RESTful-API-er for spørring om lagerbeholdningsinformasjon for gitte sett med dimensjoner, og dermed hente en liste over tilgjengelige lagerbeholdninger.</span><span class="sxs-lookup"><span data-stu-id="1b548-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="1b548-107">Lagersynlighet er en mikrotjeneste som er bygd på Microsoft Dataverse, som betyr at du kan utvide den ved å bygge Power Apps og bruke Power BI til å oppgi egendefinert funksjonalitet som dekker dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="1b548-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="1b548-108">Det er også mulig å oppgradere indeksen for å utføre lagerspørringer.</span><span class="sxs-lookup"><span data-stu-id="1b548-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="1b548-109">Lagersynlighet inneholder konfigurasjonsalternativer som gjør at den kan integreres med flere tredjepartssystemer.</span><span class="sxs-lookup"><span data-stu-id="1b548-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="1b548-110">Den støtter den standardiserte lagerdimensjonen, egendefinert utvidelse og standardisert beregnet antall som kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="1b548-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="1b548-111">Dette emnet beskriver hvordan du installerer og konfigurerer tillegget for lagersynlighet for Dynamics 365 Supply Chain Management, og hvordan du bruker app-programmeringsgrensesnittet (API).</span><span class="sxs-lookup"><span data-stu-id="1b548-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="1b548-112">Installer tillegget for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="1b548-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="1b548-113">Du må installere tillegget for lagersynlighet ved hjelp av Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1b548-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="1b548-114">LCS er en samarbeidsportal som gir et miljø og et sett med jevnlig oppdaterte tjenester som hjelper deg med å administrere applivssyklusen til Dynamics 365 Finance and Operations-appene dine.</span><span class="sxs-lookup"><span data-stu-id="1b548-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="1b548-115">Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="1b548-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1b548-116">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="1b548-116">Prerequisites</span></span>

<span data-ttu-id="1b548-117">Før du kan installere tillegget for lagersynlighet, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="1b548-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="1b548-118">Hent et LCS-implementeringsprosjekt med minst ett miljø som er distribuert.</span><span class="sxs-lookup"><span data-stu-id="1b548-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="1b548-119">Generer betanøklene for tilbudet i LCS.</span><span class="sxs-lookup"><span data-stu-id="1b548-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="1b548-120">Aktiver betanøklene for tilbudet for brukeren din i LCS.</span><span class="sxs-lookup"><span data-stu-id="1b548-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="1b548-121">Kontakt produktteamet for Microsoft-lagersynlighet, og oppgi en miljø-ID der du vil distribuere tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="1b548-122">Hvis du har spørsmål om disse forutsetningene, kan du ta kontakt med produktteamet for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="1b548-123">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="1b548-123">Install the add-in</span></span>

<span data-ttu-id="1b548-124">Hvis du vil installere tillegget for lagersynlighet, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="1b548-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="1b548-125">Logg på [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)-portalen.</span><span class="sxs-lookup"><span data-stu-id="1b548-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="1b548-126">På hjemmesiden velger du prosjektet der miljøet er distribuert.</span><span class="sxs-lookup"><span data-stu-id="1b548-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="1b548-127">På prosjektsiden velger du miljøet du vil installere tillegget i.</span><span class="sxs-lookup"><span data-stu-id="1b548-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="1b548-128">Rull ned til du ser delen **Miljøtillegg** på miljøsiden.</span><span class="sxs-lookup"><span data-stu-id="1b548-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="1b548-129">Hvis delen ikke er synlig, må du kontrollere at de nødvendige betanøklene er fullstendig behandlet.</span><span class="sxs-lookup"><span data-stu-id="1b548-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="1b548-130">I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="1b548-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="1b548-131">![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")</span><span class="sxs-lookup"><span data-stu-id="1b548-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="1b548-132">Velg koblingen **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="1b548-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="1b548-133">En liste over tilgjengelige tillegg åpnes.</span><span class="sxs-lookup"><span data-stu-id="1b548-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="1b548-134">Velg **Lagertjeneste** fra listen.</span><span class="sxs-lookup"><span data-stu-id="1b548-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="1b548-135">(Merk at det nå er oppført som **Tillegg for lagersynlighets for Dynamics 365 Supply Chain Management**.)</span><span class="sxs-lookup"><span data-stu-id="1b548-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="1b548-136">Angi verdier for følgende felter i miljøet:</span><span class="sxs-lookup"><span data-stu-id="1b548-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="1b548-137">**App-ID for AAD**</span><span class="sxs-lookup"><span data-stu-id="1b548-137">**AAD application ID**</span></span>
    - <span data-ttu-id="1b548-138">**Leier-ID for AAD**</span><span class="sxs-lookup"><span data-stu-id="1b548-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="1b548-139">![Legg til i konfigurasjon-side](media/inventory-visibility-setup.png "Legg til i konfigurasjon-side")</span><span class="sxs-lookup"><span data-stu-id="1b548-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="1b548-140">Godta vilkåret og betingelsen ved å merke av for **Vilkår og betingelser**.</span><span class="sxs-lookup"><span data-stu-id="1b548-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="1b548-141">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="1b548-141">Select **Install**.</span></span> <span data-ttu-id="1b548-142">Statusen for tillegget vil vises som **Installerer**.</span><span class="sxs-lookup"><span data-stu-id="1b548-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="1b548-143">Når du er ferdig, oppdaterer du siden for å se status endre til **Installert**.</span><span class="sxs-lookup"><span data-stu-id="1b548-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="1b548-144">Hent et token for sikkerhetstjeneste</span><span class="sxs-lookup"><span data-stu-id="1b548-144">Get a security service token</span></span>

<span data-ttu-id="1b548-145">Hent et token for sikkerhetstjeneste ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="1b548-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="1b548-146">Logg deg på Azure-portalen, og bruk det til å finne `clientId` og `clientSecret` for programmet Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1b548-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="1b548-147">Hent et Azure Active Directory-token (`aadToken`) ved å sende en HTTP-forespørsel med følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="1b548-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="1b548-148">**URL-adresse** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="1b548-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="1b548-149">**Metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="1b548-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="1b548-150">**Meldingstekst (skjemadata)**:</span><span class="sxs-lookup"><span data-stu-id="1b548-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="1b548-151">nøkkel</span><span class="sxs-lookup"><span data-stu-id="1b548-151">key</span></span> | <span data-ttu-id="1b548-152">verdi</span><span class="sxs-lookup"><span data-stu-id="1b548-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="1b548-153">client_id</span><span class="sxs-lookup"><span data-stu-id="1b548-153">client_id</span></span> | <span data-ttu-id="1b548-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="1b548-154">${aadAppId}</span></span> |
        | <span data-ttu-id="1b548-155">client_secret</span><span class="sxs-lookup"><span data-stu-id="1b548-155">client_secret</span></span> | <span data-ttu-id="1b548-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="1b548-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="1b548-157">grant_type</span><span class="sxs-lookup"><span data-stu-id="1b548-157">grant_type</span></span> | <span data-ttu-id="1b548-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="1b548-158">client_credentials</span></span> |
        | <span data-ttu-id="1b548-159">resource</span><span class="sxs-lookup"><span data-stu-id="1b548-159">resource</span></span> | <span data-ttu-id="1b548-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="1b548-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="1b548-161">Du skal motta et `aadToken` som svar, som ligner på følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="1b548-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="1b548-162">Formuler en JSON-forespørsel som ligner på følgende:</span><span class="sxs-lookup"><span data-stu-id="1b548-162">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="1b548-163">Der:</span><span class="sxs-lookup"><span data-stu-id="1b548-163">Where:</span></span>
    - <span data-ttu-id="1b548-164">Verdien for `client_assertion` må være `aadToken` du mottok i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="1b548-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="1b548-165">Verdien for `context` må være miljø-ID-en der du vil implementere tillegget.</span><span class="sxs-lookup"><span data-stu-id="1b548-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="1b548-166">Angi alle andre verdier som vist i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="1b548-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="1b548-167">Send en HTTP-forespørsel med følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="1b548-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="1b548-168">**URL-adresse** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="1b548-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="1b548-169">**Metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="1b548-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="1b548-170">**HTTP-hode** - Ta med API-versjonen (nøkkelen er `Api-Version` og verdien er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="1b548-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="1b548-171">**Meldingstekst** - Ta med JSON-forespørselen du opprettet i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="1b548-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="1b548-172">Du får et `access_token` som svar.</span><span class="sxs-lookup"><span data-stu-id="1b548-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="1b548-173">Dette er det du trenger som bærertoken for å kalle opp lagersynlighets-API-en.</span><span class="sxs-lookup"><span data-stu-id="1b548-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="1b548-174">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="1b548-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="1b548-175">Avinstallere tillegget</span><span class="sxs-lookup"><span data-stu-id="1b548-175">Uninstall the add-in</span></span>

<span data-ttu-id="1b548-176">Velg **Avinstaller** tillegget for å avinstallere tillegget.</span><span class="sxs-lookup"><span data-stu-id="1b548-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="1b548-177">Oppdater LCS så fjernes tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="1b548-178">Avinstallasjonsprosessen vil fjerne registreringen av tillegget, og også starte en jobb for å rydde opp i alle forretningsdataene som er lagret i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="1b548-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="1b548-179">Offentlig API for tillegget for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="1b548-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="1b548-180">Den offentlige REST-API-en i tillegget for lagersynlighet viser flere spesifikke endepunkter for integrering.</span><span class="sxs-lookup"><span data-stu-id="1b548-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="1b548-181">Det støtter tre hovedtyper for samhandling:</span><span class="sxs-lookup"><span data-stu-id="1b548-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="1b548-182">Postering av beholdningsendringer i tillegget fra et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="1b548-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="1b548-183">Spørring etter gjeldende antall i beholdningen fra et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="1b548-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="1b548-184">Automatisk synkronisering med Supply Chain Management tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="1b548-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="1b548-185">Den automatiske synkroniseringen er ikke en del av den offentlige API-en, men blir i stedet behandlet i bakgrunnen for miljøer som har aktivert tillegget for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="1b548-186">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="1b548-186">Authentication</span></span>

<span data-ttu-id="1b548-187">Platformsikkerhetstoken brukes til å kalle opp tillegget for lagersynlighet, så du må generere et Azure Active Directory-token ved hjelp av Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="1b548-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="1b548-188">Hvis du vil ha mer informasjon om hvordan du får tak i sikkerhetstokenet, kan du se [Installer tillegget for lagersynlighet](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="1b548-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="1b548-189">Konfigurer API-en for lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="1b548-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="1b548-190">Før du bruker tjenesten, må du fullføre konfigurasjonene som er beskrevet i følgende underavsnitt.</span><span class="sxs-lookup"><span data-stu-id="1b548-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="1b548-191">Konfigurasjonen kan variere avhengig av detaljene i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="1b548-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="1b548-192">Den inneholder hovedsakelig fire deler:</span><span class="sxs-lookup"><span data-stu-id="1b548-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="1b548-193">Partisjonering</span><span class="sxs-lookup"><span data-stu-id="1b548-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="1b548-194">Dimensjonskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="1b548-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="1b548-195">Indeksering</span><span class="sxs-lookup"><span data-stu-id="1b548-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="1b548-196">Egendefinert mål</span><span class="sxs-lookup"><span data-stu-id="1b548-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="1b548-197">Partisjonering</span><span class="sxs-lookup"><span data-stu-id="1b548-197">Partitioning</span></span>

<span data-ttu-id="1b548-198">Partisjonering kan påvirke ytelsen betydelig for API-en for lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="1b548-199">Det er en god idé å definere et oppsett som tillater små grupperinger av data, samtidig som du tillater meningsfulle dataspørringer samtidig.</span><span class="sxs-lookup"><span data-stu-id="1b548-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="1b548-200">`organizationId` (`dataAreaId` i Supply Chain Management) vil alltid være en del av partisjonen, og standard lagersynlighet er satt til partisjonering per dimensjon som *Område + sted*.</span><span class="sxs-lookup"><span data-stu-id="1b548-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="1b548-201">Dette betyr at tjenesten alltid må spørres med disse dimensjonene som er definert i filtrene.</span><span class="sxs-lookup"><span data-stu-id="1b548-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="1b548-202">*Område* og *Sted* er to generelle standarddimensjoner i lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="1b548-203">I Supply Chain Management kalles disse dimensjonene *Område* (`InventSiteId`) og *Lager* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="1b548-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="1b548-204">Dimensjonskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="1b548-204">Dimension configurations</span></span>

<span data-ttu-id="1b548-205">Lagersynlighet inneholder en liste over generelle standarddimensjoner for å aktivere systemintegrasjon med flere kilder.</span><span class="sxs-lookup"><span data-stu-id="1b548-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="1b548-206">Tabellen nedenfor viser hvilke lagerdimensjoner som skal være standard dimensjonsnavn i lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="1b548-207">Dimensjonstype</span><span class="sxs-lookup"><span data-stu-id="1b548-207">Dimension type</span></span> | <span data-ttu-id="1b548-208">Dimensjonsnavn</span><span class="sxs-lookup"><span data-stu-id="1b548-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="1b548-209">Produkt</span><span class="sxs-lookup"><span data-stu-id="1b548-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="1b548-210">Produkt</span><span class="sxs-lookup"><span data-stu-id="1b548-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="1b548-211">Produkt</span><span class="sxs-lookup"><span data-stu-id="1b548-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="1b548-212">Produkt</span><span class="sxs-lookup"><span data-stu-id="1b548-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="1b548-213">Sporing</span><span class="sxs-lookup"><span data-stu-id="1b548-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="1b548-214">Sporing</span><span class="sxs-lookup"><span data-stu-id="1b548-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="1b548-215">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="1b548-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="1b548-216">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="1b548-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="1b548-217">Lagerstatus</span><span class="sxs-lookup"><span data-stu-id="1b548-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="1b548-218">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="1b548-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="1b548-219">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="1b548-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="1b548-220">Lagerspesifikk</span><span class="sxs-lookup"><span data-stu-id="1b548-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="1b548-221">Dimensjonstypen som er oppført i den forrige tabellen, er bare for referanse.</span><span class="sxs-lookup"><span data-stu-id="1b548-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="1b548-222">Du trenger ikke definere dimensjonstypen i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="1b548-223">Hvis det finnes en egendefinert dimensjon som må flyte til en standardverdi når det brukes av lagersynlighet, kan du konfigurere navnet **Egendefinert dimensjon** i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="1b548-224">Eksterne systemer har tilgang til lagersynlighet via RESTful-API-er som gir deg beholdningsinformasjon om gitte dimensjoner som det skal spørres om.</span><span class="sxs-lookup"><span data-stu-id="1b548-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="1b548-225">Ved integreringen kan du bruke Lagersynlighet til å konfigurere den *eksterne kanaldatakilden* og kildedimensjonen til *måldimensjonene* i Lagersynlighet.</span><span class="sxs-lookup"><span data-stu-id="1b548-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="1b548-226">Måldimensjonene må være ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="1b548-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="1b548-227">Standarddimensjoner i Lagersynlighet</span><span class="sxs-lookup"><span data-stu-id="1b548-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="1b548-228">Egendefinerte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="1b548-228">Custom dimensions</span></span>

<span data-ttu-id="1b548-229">Formålet med dimensjonskonfigurasjon er å standardisere integreringen med flere systemer for spørringen på dimensjoner og posteringshendelsen med dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1b548-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="1b548-230">Indeksering</span><span class="sxs-lookup"><span data-stu-id="1b548-230">Indexing</span></span>

<span data-ttu-id="1b548-231">Vanligvis vil ikke lagerbeholdningsspørringen bare være på det høyeste totale nivået, men du vil kanskje se resultater som er aggregert basert på lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="1b548-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="1b548-232">Lagersynlighet gir fleksibilitet ved å la deg definere indeksene som er basert på dimensjonen eller kombinasjonen av dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="1b548-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="1b548-233">For øyeblikket kan du bare konfigurere indekser til maksimalt fem.</span><span class="sxs-lookup"><span data-stu-id="1b548-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="1b548-234">Du må nøye vurdere hvilken dimensjon eller dimensjonskombinasjon du vil bruke før implementeringen for å sikre at den oppfyller dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="1b548-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="1b548-235">Hvis du for eksempel vil spørre etter produkter som følger:</span><span class="sxs-lookup"><span data-stu-id="1b548-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="1b548-236">Forespør den aggregerte produktbeholdningen etter dimensjonene *Farge* og *Størrelse*.</span><span class="sxs-lookup"><span data-stu-id="1b548-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="1b548-237">I noen tilfeller vil du bare spørre om produktet totalt.</span><span class="sxs-lookup"><span data-stu-id="1b548-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="1b548-238">Du har to indekser definert som følgende:</span><span class="sxs-lookup"><span data-stu-id="1b548-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="1b548-239">Den tomme parentesen samles, basert på produkt-ID-en i partisjonen.</span><span class="sxs-lookup"><span data-stu-id="1b548-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="1b548-240">Indekseringen definerer hvordan du kan gruppere resultatene basert på `groupBy`-spørringsinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="1b548-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="1b548-241">I dette tilfellet hvis du ikke definerer noen `groupBy`-verdier, får du totaler etter `productid`.</span><span class="sxs-lookup"><span data-stu-id="1b548-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="1b548-242">Hvis ikke hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId` vil du få flere linjer returnert, basert på de ulike kombinasjonene mellom farger og størrelser i systemet.</span><span class="sxs-lookup"><span data-stu-id="1b548-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="1b548-243">Du kan legge spørringskriteriene i brødteksten for forespørselen.</span><span class="sxs-lookup"><span data-stu-id="1b548-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="1b548-244">Her er en eksempelspørring på produktet med farge- og størrelseskombinasjon.</span><span class="sxs-lookup"><span data-stu-id="1b548-244">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="1b548-245">Egendefinert mål</span><span class="sxs-lookup"><span data-stu-id="1b548-245">Custom measurement</span></span>

<span data-ttu-id="1b548-246">Standard målantall er koblet til Supply Chain Management, men du vil kanskje ha et antall som består av en kombinasjon av standardmålene.</span><span class="sxs-lookup"><span data-stu-id="1b548-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="1b548-247">Hvis du vil gjøre dette, kan du ha en konfigurasjon av egendefinert antall, som vil bli lagt til i utdataene i lagerbeholdningsspørringene.</span><span class="sxs-lookup"><span data-stu-id="1b548-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="1b548-248">Ved hjelp av funksjonaliteten kan du bare definere et sett med mål som skal legges til, eller et sett med mål som skal trekkes fra, for å kunne lage det egendefinerte målet.</span><span class="sxs-lookup"><span data-stu-id="1b548-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="1b548-249">Med følgende spørringsvilkår vil du for eksempel konfigurere det egendefinerte målantallet som `MyCustomAvailableforReservation` som skal brukes av forbrukssystemet.</span><span class="sxs-lookup"><span data-stu-id="1b548-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="1b548-250">Forbrukssystem</span><span class="sxs-lookup"><span data-stu-id="1b548-250">Consumption system</span></span> | <span data-ttu-id="1b548-251">Beregnede mål</span><span class="sxs-lookup"><span data-stu-id="1b548-251">Calculated measurers</span></span> | <span data-ttu-id="1b548-252">Datakilde</span><span class="sxs-lookup"><span data-stu-id="1b548-252">Data source</span></span> | <span data-ttu-id="1b548-253">Modifikator</span><span class="sxs-lookup"><span data-stu-id="1b548-253">Modifier</span></span> | <span data-ttu-id="1b548-254">Beregningstype for modifikator</span><span class="sxs-lookup"><span data-stu-id="1b548-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="1b548-255">Tillegg</span><span class="sxs-lookup"><span data-stu-id="1b548-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="1b548-256">Tillegg</span><span class="sxs-lookup"><span data-stu-id="1b548-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="1b548-257">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="1b548-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="1b548-258">Tillegg</span><span class="sxs-lookup"><span data-stu-id="1b548-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="1b548-259">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="1b548-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="1b548-260">Tillegg</span><span class="sxs-lookup"><span data-stu-id="1b548-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="1b548-261">Tillegg</span><span class="sxs-lookup"><span data-stu-id="1b548-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="1b548-262">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="1b548-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="1b548-263">Subtraksjon</span><span class="sxs-lookup"><span data-stu-id="1b548-263">Subtraction</span></span> |

<span data-ttu-id="1b548-264">Med dette vil spørringen på det egendefinerte målantallet returnere følgende utdata.</span><span class="sxs-lookup"><span data-stu-id="1b548-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="1b548-265">`MyCustomAvailableforReservation`-utdataene er basert på beregningsinnstillingen i de egendefinerte målene som:</span><span class="sxs-lookup"><span data-stu-id="1b548-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="1b548-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="1b548-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="1b548-267">Postere lagerendringer</span><span class="sxs-lookup"><span data-stu-id="1b548-267">Posting on-hand changes</span></span>

<span data-ttu-id="1b548-268">Den nøyaktige URL-adressen som hendelsen vil bli postert til, avhenger av det geografiske området.</span><span class="sxs-lookup"><span data-stu-id="1b548-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="1b548-269">Den tar følgende form:</span><span class="sxs-lookup"><span data-stu-id="1b548-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="1b548-270">Når den er godkjent, kan denne URL-adressen brukes sammen med HTTP `POST`-metoden til å sende lagerbeholdningshendelser til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="1b548-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="1b548-271">En spesiell topptekst brukes til å kommunisere med Dynamics 365-tjenester via HTTP-forespørsler, og angir miljø-ID-en til Supply Chain Management-forkomten dataene er koblet til.</span><span class="sxs-lookup"><span data-stu-id="1b548-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="1b548-272">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="1b548-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="1b548-273">Postere spørringer om lagerendringer eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1b548-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="1b548-274">I dette eksemplet vises det et scenario der du kan definere dimensjonskonfigurasjonen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="1b548-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="1b548-275">Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="1b548-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="1b548-276">Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene.</span><span class="sxs-lookup"><span data-stu-id="1b548-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="1b548-277">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1b548-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="1b548-278">Postere spørringer om lagerendringer eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1b548-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="1b548-279">Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="1b548-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="1b548-280">Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet er null, tomt eller mellomrom.</span><span class="sxs-lookup"><span data-stu-id="1b548-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="1b548-281">Feltegenskaper for JSON-dokument</span><span class="sxs-lookup"><span data-stu-id="1b548-281">JSON document field properties</span></span>

<span data-ttu-id="1b548-282">Feltene fra JSON-spørringseksemplene som ble angitt tidligere, har egenskapene som er oppført i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="1b548-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="1b548-283">Felt-ID</span><span class="sxs-lookup"><span data-stu-id="1b548-283">Field ID</span></span> | <span data-ttu-id="1b548-284">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1b548-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="1b548-285">En unik ID for den bestemte endringshendelsen.</span><span class="sxs-lookup"><span data-stu-id="1b548-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="1b548-286">Denne ID-en brukes til å sikre at hvis kommunikasjon med tjenesten mislykkes under posteringen, vil sendingen av hendelsen ikke resultere i at samme hendelse telles to ganger i systemet.</span><span class="sxs-lookup"><span data-stu-id="1b548-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="1b548-287">Identifikatoren til organisasjonen som er koblet til hendelsen.</span><span class="sxs-lookup"><span data-stu-id="1b548-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="1b548-288">Dette tilordner til ID-er til Supply Chain Management-organisasjoner eller dataområder.</span><span class="sxs-lookup"><span data-stu-id="1b548-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="1b548-289">Identifikatoren til produktet det gjelder.</span><span class="sxs-lookup"><span data-stu-id="1b548-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="1b548-290">Antallet som lagerbeholdningen må endres med.</span><span class="sxs-lookup"><span data-stu-id="1b548-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="1b548-291">Hvis for eksempel ti nye bagels er lagt til i en hylle, vil denne verdien være 10.</span><span class="sxs-lookup"><span data-stu-id="1b548-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="1b548-292">Hvis tre bagels deretter ble fjernet fra hyllen eller solgt, ville denne verdien være –3.</span><span class="sxs-lookup"><span data-stu-id="1b548-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="1b548-293">Datakilden for dimensjonene som brukes i posteringsendringshendelsen og -spørringen.</span><span class="sxs-lookup"><span data-stu-id="1b548-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="1b548-294">Hvis du angir datakilden, kan du bruke de egendefinerte dimensjonene fra den angitte datakilden.</span><span class="sxs-lookup"><span data-stu-id="1b548-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="1b548-295">Med dimensjonskonfigurasjonen kan Lagersynlighet tilordne de egendefinerte dimensjonene til de generelle standarddimensjonene.</span><span class="sxs-lookup"><span data-stu-id="1b548-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="1b548-296">Hvis `dimensionDataSource` ikke er angitt, kan du bare bruke de generelle standarddimensjonene i spørringene.</span><span class="sxs-lookup"><span data-stu-id="1b548-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="1b548-297">En dynamisk samling med nøkkel/verdi-par.</span><span class="sxs-lookup"><span data-stu-id="1b548-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="1b548-298">Disse vil tilordnes noen av dimensjonene i Supply Chain Management, men du kan også legge til egendefinerte dimensjoner (som *Kilde*) som kan angi om hendelsen kommer fra Supply Chain Management eller et eksternt system.</span><span class="sxs-lookup"><span data-stu-id="1b548-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="1b548-299">Spørring om aktuell lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="1b548-299">Querying current on-hand</span></span>

<span data-ttu-id="1b548-300">Endepunktet for spørringer av gjeldende lagerbeholdning vil ha en lignende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="1b548-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="1b548-301">Det blir spurt med HTTP `POST`-metoden.</span><span class="sxs-lookup"><span data-stu-id="1b548-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="1b548-302">Gjeldende beholdningsspørring, eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1b548-302">Current on-hand query example 1</span></span>

<span data-ttu-id="1b548-303">I dette eksemplet vises det et scenario der du allerede har fullført dimensjonskonfigurasjonen i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="1b548-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="1b548-304">Bruk følgende spørring til å konfigurere dimensjonstilordningen i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="1b548-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="1b548-305">Nå kan du angi `dimensionDataSource` og bruke egendefinerte dimensjoner i spørringene.</span><span class="sxs-lookup"><span data-stu-id="1b548-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="1b548-306">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1b548-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="1b548-307">Du kan angi `DimensionDataSource` i `filters` og angi egendefinerte dimensjoner i både `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="1b548-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="1b548-308">Systemet konverterer automatisk egendefinerte dimensjoner til basisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1b548-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="1b548-309">Gjeldende beholdningsspørring, eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1b548-309">Current on-hand query example 2</span></span>

<span data-ttu-id="1b548-310">Dette eksemplet viser et scenario der ingen tilordninger er definert for dimensjonskonfigurasjonen i Power Apps, slik at posteringen også bør bruke basisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="1b548-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="1b548-311">Alle dimensjoner må være basisdimensjoner når `dimensionDataSource`-feltet, under `filters`, er null, tomt eller mellomrom.</span><span class="sxs-lookup"><span data-stu-id="1b548-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="1b548-312">Eksempel på returresultat</span><span class="sxs-lookup"><span data-stu-id="1b548-312">Example return result</span></span>

<span data-ttu-id="1b548-313">Spørringene som vises i eksemplene ovenfor, kan returnere et resultat som dette.</span><span class="sxs-lookup"><span data-stu-id="1b548-313">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="1b548-314">Legg merke til at antall-feltene er strukturert som en ordliste for mål og tilknyttede verdier.</span><span class="sxs-lookup"><span data-stu-id="1b548-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>

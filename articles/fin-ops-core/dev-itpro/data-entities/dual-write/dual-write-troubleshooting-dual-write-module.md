---
title: Feilsøke problemer med dobbel skriving-modulen i Finance and Operations-apper
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer med dobbel skriving-modulen i Finance and Operations-apper.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997380"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="ad550-103">Feilsøke problemer med dobbel skriving-modulen i Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="ad550-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad550-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ad550-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="ad550-105">Mer spesifikt gir det informasjon som kan hjelpe deg med å løse problemer med **Dobbel skriving** -modulen i Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="ad550-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad550-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="ad550-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="ad550-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="ad550-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="ad550-108">Du kan ikke laste inn dobbel skriving-modulen i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="ad550-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="ad550-109">Hvis du ikke kan åpne **Dobbel skriving** -siden ved å velge **Dobbel skriving** -flisen i **Databehandling** -arbeidsområdet, er dataintegrasjonstjenesten sannsynligvis nede.</span><span class="sxs-lookup"><span data-stu-id="ad550-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="ad550-110">Opprett en støtteforespørsel for å be om omstart av dataintegrasjonstjenesten.</span><span class="sxs-lookup"><span data-stu-id="ad550-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="ad550-111">Feil når du prøver å opprette en ny enhetstilordning</span><span class="sxs-lookup"><span data-stu-id="ad550-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="ad550-112">**Påkrevd legitimasjon for å løse problemet:** Den samme brukeren som konfigurere dobbelt skriving.</span><span class="sxs-lookup"><span data-stu-id="ad550-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="ad550-113">Du kan få følgende feilmelding når du prøver å konfigurere en ny enhet for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="ad550-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="ad550-114">Den eneste brukeren som kan opprette en tilordning, er brukeren som konfigurere dobbelt skriving-forbindelsen.</span><span class="sxs-lookup"><span data-stu-id="ad550-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="ad550-115">*Svarstatuskoden indikerer ikke fullført: 401 (uautorisert)*</span><span class="sxs-lookup"><span data-stu-id="ad550-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="ad550-116">Feil når du åpner bruker grensesnittet for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="ad550-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="ad550-117">Du kan få følgende feilmelding når du prøver å få tilgang til dobbel skriving fra arbeidsområdet **Databehandling** :</span><span class="sxs-lookup"><span data-stu-id="ad550-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="ad550-118">*login.microsoftonline.com kunne ikke koble til.*</span><span class="sxs-lookup"><span data-stu-id="ad550-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="ad550-119">Du kan løse problemet ved å logge på ved å bruke et InPrivate-vindu i Microsoft Edge, et inkognito-vindu i Chromium, eller et inkognito-vindu i Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="ad550-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="ad550-120">Du må også oppheve blokkeringen eller fjerne tredjeparts informasjonskapsler.</span><span class="sxs-lookup"><span data-stu-id="ad550-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="ad550-121">Feil når du kobler miljøet for dobbel skriving eller legger til en ny enhetstilordning</span><span class="sxs-lookup"><span data-stu-id="ad550-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="ad550-122">**Nødvendig rolle for å løse problemet:** Systemadministrator i både Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ad550-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="ad550-123">Du kan støte på følgende feilmelding når du kobler eller oppretter tilordninger:</span><span class="sxs-lookup"><span data-stu-id="ad550-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="ad550-124">*Svarstatuskoden indikerer ikke fullført: 403 (tokenexchange).<br> Økt-ID: \<your session id\><br> Rotaktivitet-ID: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="ad550-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="ad550-125">Denne feilen kan oppstå hvis du ikke har tilstrekkelige tillatelser til å koble dobbel skriving eller opprette tilordninger.</span><span class="sxs-lookup"><span data-stu-id="ad550-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="ad550-126">Denne feilen kan også oppstå hvis Common Data Service-miljøet ble tilbakestilt uten å koble fra dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="ad550-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="ad550-127">Alle brukere med rollen systemansvarlig i både Finance and Operations-apper og Common Data Service kan koble sammen miljøer.</span><span class="sxs-lookup"><span data-stu-id="ad550-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="ad550-128">Bare brukeren som har konfigurerte av dobbel skriving-tilkobling, kan legge til nye enhetstilordninger.</span><span class="sxs-lookup"><span data-stu-id="ad550-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="ad550-129">Etter installasjonen kan alle brukere med rollen systemansvarlig overvåke statusen og redigere tilordningene.</span><span class="sxs-lookup"><span data-stu-id="ad550-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="ad550-130">Feil når du stopper enhetstilordningen</span><span class="sxs-lookup"><span data-stu-id="ad550-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="ad550-131">Du kan få følgende feilmelding når du prøver å stoppe enhetstilordningene:</span><span class="sxs-lookup"><span data-stu-id="ad550-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="ad550-132">*\[Forbudt\], \[{"status":403,"kilde":"","melding":"Feil fra token-utveksling: Brukeren har ikke tilgang til tilkoblingen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Den eksterne serveren returnerte en feil: (403) Forbidden.*</span><span class="sxs-lookup"><span data-stu-id="ad550-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="ad550-133">Denne feilen oppstår når det koblede Common Data Service-miljøet ikke er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ad550-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="ad550-134">Du kan løse problemet ved å opprette en støtteforespørsel for data integrasjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="ad550-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="ad550-135">Knytt til nettverkssporingen slik at dataintegrasjonsgruppen kan merke tilordningene som **Kjører ikke** i serverdelen.</span><span class="sxs-lookup"><span data-stu-id="ad550-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="ad550-136">Feil under forsøk på å starte en enhetstilordning</span><span class="sxs-lookup"><span data-stu-id="ad550-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="ad550-137">Det kan hende du får en feilmelding som nedenfor når du forsøker å angi denne tilstanden for en tilordning til **Kjører** :</span><span class="sxs-lookup"><span data-stu-id="ad550-137">You might receive an error like the following when you try to set that state of a mapping to **Running** :</span></span>

<span data-ttu-id="ad550-138">*Kan ikke fullføre den opprinnelige datasynkroniseringen. Feil: dobbelt skriving feil - registrering av plugin-modul mislyktes: kan ikke opprette metadata for oppslag med dobbel skriving. Feilobjektreferanse er ikke satt til en forekomst av et objekt.*</span><span class="sxs-lookup"><span data-stu-id="ad550-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="ad550-139">Hurtigreparasjonen for denne feilen er avhengig av årsaken til feilen:</span><span class="sxs-lookup"><span data-stu-id="ad550-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="ad550-140">Hvis tilordningen har avhengige tilordninger, må du sørge for å aktivere de avhengige tilordningene for denne enhetstilordningen.</span><span class="sxs-lookup"><span data-stu-id="ad550-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="ad550-141">Tilordningen kan mangle kilde- eller målfelt.</span><span class="sxs-lookup"><span data-stu-id="ad550-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="ad550-142">Hvis et felt i Finance and Operations-appen mangler, følger du trinnene i delen [Problem med manglende enhetsfelt på tilordninger](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="ad550-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="ad550-143">Hvis det mangler et felt i Common Data Service, klikker du **Oppdater enheter** -knappen på tilordning slik at feltene automatisk fylles tilbake til tilordningen.</span><span class="sxs-lookup"><span data-stu-id="ad550-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>

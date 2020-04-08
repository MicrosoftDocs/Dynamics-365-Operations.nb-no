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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172766"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="f4d6e-103">Feilsøke problemer med dobbel skriving-modulen i Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="f4d6e-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f4d6e-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="f4d6e-105">Mer spesifikt gir det informasjon som kan hjelpe deg med å løse problemer med **Dobbel skriving**-modulen i Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4d6e-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="f4d6e-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="f4d6e-108">Du kan ikke laste inn dobbel skriving-modulen i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="f4d6e-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="f4d6e-109">Hvis du ikke kan åpne **Dobbel skriving**-siden ved å velge **Dobbel skriving**-flisen i **Databehandling**-arbeidsområdet, er dataintegrasjonstjenesten sannsynligvis nede.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="f4d6e-110">Opprett en støtteforespørsel for å be om omstart av dataintegrasjonstjenesten.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="f4d6e-111">Feil når du prøver å opprette en ny enhetstilordning</span><span class="sxs-lookup"><span data-stu-id="f4d6e-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="f4d6e-112">**Nødvendig legitimasjon for å løse problemet:** Azure AD-leieradministrator</span><span class="sxs-lookup"><span data-stu-id="f4d6e-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="f4d6e-113">Du kan få følgende feilmelding når du prøver å konfigurere en ny enhet for dobbel skriving:</span><span class="sxs-lookup"><span data-stu-id="f4d6e-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="f4d6e-114">*Svarstatuskoden indikerer ikke fullført: 401 (uautorisert)*</span><span class="sxs-lookup"><span data-stu-id="f4d6e-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="f4d6e-115">Denne feilen oppstår fordi bare en Azure AD-leieradministrator kan legge til en ny enhetstilordning.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="f4d6e-116">Du kan løse problemet ved å logge på Finance and Operations-appen som en Azure AD-administratorleier.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="f4d6e-117">Du må også gå til web.PowerApps.com og validere tilkoblingen på nytt.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="f4d6e-118">Feil når du åpner bruker grensesnittet for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="f4d6e-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="f4d6e-119">Du kan få følgende feilmelding når du prøver å få tilgang til dobbel skriving fra arbeidsområdet **Databehandling**:</span><span class="sxs-lookup"><span data-stu-id="f4d6e-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="f4d6e-120">*login.microsoftonline.com kunne ikke koble til.*</span><span class="sxs-lookup"><span data-stu-id="f4d6e-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="f4d6e-121">Du kan løse problemet ved å logge på ved å bruke et InPrivate-vindu i Microsoft Edge, et inkognito-vindu i Chromium, eller et inkognito-vindu i Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="f4d6e-122">Du må også oppheve blokkeringen eller fjerne tredjeparts informasjonskapsler.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="f4d6e-123">Feil når du kobler miljøet for dobbel skriving eller legger til en ny enhetstilordning</span><span class="sxs-lookup"><span data-stu-id="f4d6e-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="f4d6e-124">**Nødvendig legitimasjon for å løse problemet:** Azure AD-leieradministrator</span><span class="sxs-lookup"><span data-stu-id="f4d6e-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="f4d6e-125">Du kan støte på følgende feilmelding når du kobler eller oppretter tilordninger:</span><span class="sxs-lookup"><span data-stu-id="f4d6e-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="f4d6e-126">*Svarstatuskoden indikerer ikke fullført: 403 (tokenexchange).<br> Økt-ID: \<din økt-id\><br> Rotaktivitet-ID: \<din rotaktivitet-id\>*</span><span class="sxs-lookup"><span data-stu-id="f4d6e-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="f4d6e-127">Denne feilen kan oppstå hvis du ikke har tilstrekkelige tillatelser til å koble dobbel skriving eller opprette tilordninger.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="f4d6e-128">Du må bruke en Azure AD-leieradministratorkonto for å koble miljøer og legge til nye enhetstilordninger.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="f4d6e-129">Etter installasjonen kan du imidlertid bruke en ikke-administratorkonto til å overvåke status og redigere tilordningene.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="f4d6e-130">Feil når du stopper enhetstilordningen</span><span class="sxs-lookup"><span data-stu-id="f4d6e-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="f4d6e-131">Du kan få følgende feilmelding når du prøver å stoppe enhetstilordningene:</span><span class="sxs-lookup"><span data-stu-id="f4d6e-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="f4d6e-132">*\[Forbudt\], \[{"status":403,"kilde":"","melding":"Feil fra token-utveksling: Brukeren har ikke tilgang til tilkoblingen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Den eksterne serveren returnerte en feil: (403) Forbidden.*</span><span class="sxs-lookup"><span data-stu-id="f4d6e-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="f4d6e-133">Denne feilen oppstår når det koblede Common Data Service-miljøet ikke er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="f4d6e-134">Du kan løse problemet ved å opprette en støtteforespørsel for data integrasjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="f4d6e-135">Knytt til nettverkssporingen slik at dataintegrasjonsgruppen kan merke tilordningene som **Kjører ikke** i serverdelen.</span><span class="sxs-lookup"><span data-stu-id="f4d6e-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

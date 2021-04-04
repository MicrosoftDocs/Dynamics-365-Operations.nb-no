---
title: Feilsøke problemer under førstegangsinstallasjon
description: Dette emnet inneholder informasjon som kan hjelpe deg å løse problemer som oppstår under første konfigurasjon av integrering med dobbel skriving.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6ff9a304de8a94b86e6866d6d2cb65fbfdfb02f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561184"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="967c3-103">Feilsøke problemer under førstegangsinstallasjon</span><span class="sxs-lookup"><span data-stu-id="967c3-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="967c3-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="967c3-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="967c3-105">Dette emnet inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under det første oppsettet av integrering med dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="967c3-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="967c3-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="967c3-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="967c3-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="967c3-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="967c3-108">Du kan ikke koble en Finance and Operations-app til Dataverse</span><span class="sxs-lookup"><span data-stu-id="967c3-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="967c3-109">**Nødvendig rolle for å konfigurere dobbel skriving:** Systemadministrator i Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="967c3-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="967c3-110">Feil på **oppsett-koblingen til Dataverse**-siden skyldes vanligvis ufullstendige oppsetts- eller tillatelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="967c3-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="967c3-111">Kontroller at hele tilstandskontrollen bestås på **Oppsett-koblingen til Dataverse**-siden, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="967c3-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="967c3-112">Du kan ikke koble til dobbel skriving med mindre hele tilstandssjekken bestås.</span><span class="sxs-lookup"><span data-stu-id="967c3-112">You can't link dual-write unless the whole health check passes.</span></span>

![Vellykket tilstandssjekk](media/health_check.png)

<span data-ttu-id="967c3-114">Du må ha legitimasjon for Azure AD-leieradministrator for å koble til Finance and Operations- og Dataverse-miljøene.</span><span class="sxs-lookup"><span data-stu-id="967c3-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="967c3-115">Når du har koblet til miljøene, kan brukere logge på ved hjelp av kontolegitimasjonen og oppdatere en eksisterende tabelltilordning.</span><span class="sxs-lookup"><span data-stu-id="967c3-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="967c3-116">Feil når du åpner Kobling til Dataverse-siden</span><span class="sxs-lookup"><span data-stu-id="967c3-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="967c3-117">**Nødvendig legitimasjon for å løse problemet:** Azure AD-leieradministrator</span><span class="sxs-lookup"><span data-stu-id="967c3-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="967c3-118">Du kan få følgende feilmelding når du prøver å åpne **Kobling til Dataverse**-siden i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="967c3-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="967c3-119">*Svarstatuskoden indikerer ikke fullført: 404 (ikke funnet).*</span><span class="sxs-lookup"><span data-stu-id="967c3-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="967c3-120">Denne feilen oppstår når samtykketrinnet ikke er fullført.</span><span class="sxs-lookup"><span data-stu-id="967c3-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="967c3-121">Hvis du vil validere om samtykketrinnet er fullført, logger du på portal.Azure.com ved hjelp av kontoen for Azure AD-leieradministrator og ser om tredjepartsappen som har IDen **33976c19-1db5-4c02-810e-c243db79efde** vises i listen Azure AD **Enterprise-programmer**.</span><span class="sxs-lookup"><span data-stu-id="967c3-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="967c3-122">Hvis den ikke gjør det, må du gi appsamtykke.</span><span class="sxs-lookup"><span data-stu-id="967c3-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="967c3-123">Følg denne fremgangsmåten for å gi samtykke for appen.</span><span class="sxs-lookup"><span data-stu-id="967c3-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="967c3-124">Åpne følgende URL-adresse ved hjelp av administratorlegitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="967c3-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="967c3-125">Du skal bli bedt om samtykke.</span><span class="sxs-lookup"><span data-stu-id="967c3-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="967c3-126">Velg **Godta** for å angi at du gir ditt samtykke til å installere appen som har ID-en **33976c19-1db5-4c02-810e-c243db79efde** i leieren.</span><span class="sxs-lookup"><span data-stu-id="967c3-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="967c3-127">Denne appen er nødvendig for å koble til Dataverse- og Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="967c3-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="967c3-128">Hvis du har problemer med dette trinnet, åpner du nettleseren i inkognitomodus (i Google Chrome) eller InPrivate-modus (i Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="967c3-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="967c3-129">Kontroller at firmadata og team med dobbel skriving er riktig konfigurert under kobling</span><span class="sxs-lookup"><span data-stu-id="967c3-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="967c3-130">For å sikre at dobbeltskriving fungerer som det skal, opprettes firmaene du velger under konfigurasjonen, i Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="967c3-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="967c3-131">Som standard er disse firmaene skrivebeskyttet, og egenskapen **IsDualWriteEnable** er satt til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="967c3-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="967c3-132">I tillegg opprettes standard eier av forretningsenheten og teamet og inkluderer firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="967c3-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="967c3-133">Før du aktiverer tilordningene, må du kontrollere at standard teameier er angitt.</span><span class="sxs-lookup"><span data-stu-id="967c3-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="967c3-134">Gjør følgende for å finne tabellen **Firmaer (CDM\_Firma)**.</span><span class="sxs-lookup"><span data-stu-id="967c3-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="967c3-135">Velg filteret øverst til høyre i den modelldrevne appen i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="967c3-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="967c3-136">Velg **Firma** fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="967c3-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="967c3-137">Velg **Kjør** for å se resultatene.</span><span class="sxs-lookup"><span data-stu-id="967c3-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="967c3-138">Velg firmaet som var koblet da du konfigurerte dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="967c3-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="967c3-139">Kontroller at kolonnen **Standard eiende team** har en verdi.</span><span class="sxs-lookup"><span data-stu-id="967c3-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="967c3-140">I illustrasjonen nedenfor er kolonnen **Standard eiende team** satt til **USMF Dual Write**.</span><span class="sxs-lookup"><span data-stu-id="967c3-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![Kontrollere standard eiende team](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="967c3-142">Finn grensen for antall juridiske tabeller eller firmaer som kan kobles til for dobbeltskriving</span><span class="sxs-lookup"><span data-stu-id="967c3-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="967c3-143">Du kan få følgende feilmelding når du prøver å aktivere tilordninger:</span><span class="sxs-lookup"><span data-stu-id="967c3-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="967c3-144">*Dobbel skriving-feil - Plugin-registrering mislyktes: \[(Kan ikke få partisjonskart for prosjektet DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Feil Overskrider de maksimale partisjonene som er tillatt for tilordning av DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Det oppstod en eller flere feil.*</span><span class="sxs-lookup"><span data-stu-id="967c3-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="967c3-145">Gjeldende grense når du kobler miljøene er omtrent 40 juridiske tabeller.</span><span class="sxs-lookup"><span data-stu-id="967c3-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="967c3-146">Denne feilen oppstår hvis du prøver å aktivere tilordninger, og flere enn 40 juridiske tabeller er koblet mellom miljøene.</span><span class="sxs-lookup"><span data-stu-id="967c3-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
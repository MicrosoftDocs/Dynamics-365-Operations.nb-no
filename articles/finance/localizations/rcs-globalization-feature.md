---
title: Regulatory Configuration Services (RCS) – globaliseringsfunksjoner
description: Dette emnet forklarer hvordan du bruker Microsoft RCS (Regulatory Configuration Services) og det globale repositoriet for å opprette og bruke globaliseringstjenester.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: cbb1d9a53a7a09ab525532f08553898c4e40223a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822787"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="f1765-103">Regulatory Configuration Services (RCS) – globaliseringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f1765-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1765-104">Du kan bruke RCS (Microsoft Regulatory Configuration Services) til å opprette en globaliseringsfunksjon som kan brukes i globaliseringstjenester som for eksempel en e-faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="f1765-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="f1765-105">Med RCS kan du utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="f1765-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="f1765-106">Definere relaterte komponenter for en funksjon.</span><span class="sxs-lookup"><span data-stu-id="f1765-106">Define related components of a feature.</span></span>
- <span data-ttu-id="f1765-107">Administrere funksjonens livssyklus via statusen til en funksjon.</span><span class="sxs-lookup"><span data-stu-id="f1765-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="f1765-108">Gjøre en funksjon tilgjengelig for definerte miljøer.</span><span class="sxs-lookup"><span data-stu-id="f1765-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="f1765-109">Dele en funksjon med andre organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="f1765-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="f1765-110">Fremgangsmåtene nedenfor forklarer hvordan en bruker i RCS kan legge til en globaliseringsfunksjon og relaterte komponenter, oppdatere funksjonens status og gjøre funksjonen tilgjengelig slik at den kan brukes i globaliseringstjenester.</span><span class="sxs-lookup"><span data-stu-id="f1765-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="f1765-111">Før du fullfører prosedyrene, må du fullføre trinnene som gjelder for følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="f1765-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="f1765-112">Åpne en RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f1765-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="f1765-113">Opprette og aktivere en konfigurasjonsleverandør.</span><span class="sxs-lookup"><span data-stu-id="f1765-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="f1765-114">Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f1765-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="f1765-115">I Finance and Operations-appforekomster følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f1765-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="f1765-116">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f1765-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f1765-117">Hvis et RCS-miljø ikke er klargjort for firmaet ditt, velger du **Regulatory Services – Konfigurasjon**, og deretter følger du instruksjonene for å klargjøre et miljø.</span><span class="sxs-lookup"><span data-stu-id="f1765-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="f1765-118">Hvis et RCS-miljø allerede er klargjort for ditt firma, bruker du URL-adressen for siden til å få tilgang til miljøet ved å velge alternativet for pålogging.</span><span class="sxs-lookup"><span data-stu-id="f1765-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="f1765-119">Aktivere globaliseringsfunksjonene</span><span class="sxs-lookup"><span data-stu-id="f1765-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="f1765-120">I RCS-forekomsten velger du **Funksjonsbehandling**-flisen.</span><span class="sxs-lookup"><span data-stu-id="f1765-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="f1765-121">I **Funksjonsbehandling**-arbeidsområdet velger du **Globaliseringsfunksjoner** i listen, og deretter velger du **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="f1765-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Globaliseringsfunksjoner i funksjonsbehandling](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="f1765-123">Globaliseringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f1765-123">Globalization features</span></span>

<span data-ttu-id="f1765-124">Hvis du vil bruke en globaliseringsfunksjon, må du først importere den fra det globale repositoriet og opprette din egen versjon av den.</span><span class="sxs-lookup"><span data-stu-id="f1765-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="f1765-125">Det finnes to måter å legge til globaliseringsfunksjoner på:</span><span class="sxs-lookup"><span data-stu-id="f1765-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="f1765-126">Legg til en avledet funksjon som er basert på en eksisterende funksjon som er publisert eller delt.</span><span class="sxs-lookup"><span data-stu-id="f1765-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="f1765-127">Legg til en ny funksjon som du har opprettet fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="f1765-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="f1765-128">Få tilgang til globaliseringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f1765-128">Access Globalization features</span></span>

1. <span data-ttu-id="f1765-129">Kontroller at **Globaliseringsfunksjoner** er aktivert i Funksjonsbehandling, som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f1765-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="f1765-130">Åpne det nye arbeidsområdet for **Globaliseringsfunksjoner**, gå til **Funksjoner** og velg flisen **E-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="f1765-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Arbeidsområde for globale funksjoner](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="f1765-132">Siden **E-faktureringsfunksjoner** er åpen.</span><span class="sxs-lookup"><span data-stu-id="f1765-132">The **e-Invoicing Features** page is opened.</span></span>

    ![E-faktureringsfunksjoner-siden](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="f1765-134">Legg til en avledet globaliseringsfunksjon</span><span class="sxs-lookup"><span data-stu-id="f1765-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="f1765-135">Du kan legge til en ny globaliseringsfunksjon ved å avlede den fra en eksisterende funksjon som er publisert eller delt.</span><span class="sxs-lookup"><span data-stu-id="f1765-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="f1765-136">Velg **Importer** for å åpne **Importer en funksjon fra et global repositorium**-siden.</span><span class="sxs-lookup"><span data-stu-id="f1765-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Importer en funksjon fra en global repositoriumsside](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="f1765-138">Velg **Synkroniser** for å få de nyeste funksjonene.</span><span class="sxs-lookup"><span data-stu-id="f1765-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="f1765-139">Den synkroniserte listen inneholder funksjoner som er tilgjengelige for deg, enten fordi de er publisert av Microsoft eller fordi de ble delt med deg av en annen konfigurasjonsleverandør.</span><span class="sxs-lookup"><span data-stu-id="f1765-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Synkronisert liste over funksjoner](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="f1765-141">I listen velger du funksjonene som skal importeres, og deretter velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="f1765-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="f1765-142">Du får en melding når de valgte funksjonene er importert.</span><span class="sxs-lookup"><span data-stu-id="f1765-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Melding om vellykket importering](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="f1765-144">Velg **Legg til**, og merk deretter av for **Basert på eksisterende versjon** i rullegardinmenyen i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f1765-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="f1765-145">Angi et navn og en beskrivelse for funksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="f1765-146">Velg den grunnleggende versjonen av funksjonen i listen over tilgjengelige funksjoner, og velg deretter **Opprett funksjon**.</span><span class="sxs-lookup"><span data-stu-id="f1765-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Legge til en avledet funksjon](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="f1765-148">Funksjonen du la til, er opprettet og har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="f1765-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![En avledet funksjon som har Utkast-status](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="f1765-150">Gå gjennom funksjonskomponentene for å finne ut om oppdateringer kreves:</span><span class="sxs-lookup"><span data-stu-id="f1765-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="f1765-151">Gå gjennom konfigurasjonene i tilfelle du må tilpasse formatene for elektronisk rapportering (ER) og binde dem sammen med formattilordninger for funksjonsversjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="f1765-152">Gå gjennom oppsettet i tilfelle du trenger å tilpasse **Handlinger**-kategorien, **Gyldighetsregler**-kategorien eller **Variabler**-kategorien for funksjonsversjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="f1765-153">I **Versjoner**-kategorien velger du en **Gyldig fra**-dato, og angir en beskrivelse hvis **Beskrivelse**-feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="f1765-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="f1765-154">Velg **Endre status** for å fullføre funksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="f1765-155">Fullførte funksjoner kan gjøres tilgjengelige for et bestemt miljø, slik at de kan brukes i globaliseringstjenester, eller de kan publiseres til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="f1765-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="f1765-156">Funksjoner som har **Funksjonsversjonstatus**-verdien **Publisert**, kan deles med eksterne organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="f1765-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="f1765-157">Legge til en ny globaliseringsfunksjon</span><span class="sxs-lookup"><span data-stu-id="f1765-157">Add a new Globalization feature</span></span>

<span data-ttu-id="f1765-158">Du kan legge til en ny globaliseringsfunksjon ved å opprette den fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="f1765-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="f1765-159">På **Importer funksjon fra globalt repositorium**-siden velger du **Legg til**, og velger deretter **Ny funksjon**-alternativet i rullegardinmenyen for dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f1765-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="f1765-160">Angi et navn og en beskrivelse for funksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="f1765-161">Velg **Opprett funksjon**.</span><span class="sxs-lookup"><span data-stu-id="f1765-161">Select **Create feature**.</span></span>

    ![Legge til en ny funksjon](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="f1765-163">I **Versjoner**-kategorien velger du en **Gyldig fra**-dato, og deretter velger du **Endre status** for å fullføre funksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="f1765-164">Fullførte funksjoner kan gjøres tilgjengelige for et bestemt miljø, slik at de kan brukes i globaliseringstjenester, eller de kan publiseres til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="f1765-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="f1765-165">Funksjoner som har **Funksjonsversjonstatus**-verdien **Publisert**, kan deles med eksterne organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="f1765-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="f1765-166">Oversikt over funksjonskomponent</span><span class="sxs-lookup"><span data-stu-id="f1765-166">Feature component overview</span></span>

<span data-ttu-id="f1765-167">Globaliseringsfunksjoner består av flere komponenter:</span><span class="sxs-lookup"><span data-stu-id="f1765-167">Globalization features have several components:</span></span>

- <span data-ttu-id="f1765-168">**Versjon** – denne komponenten støtter administrasjon av funksjonens livssyklus og lar brukere administrere statusen for ulike versjoner av funksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="f1765-169">**Konfigurasjoner** – Ved hjelp av denne komponenten kan brukere behandle, vise og redigere relaterte ER-formater og formattilordninger.</span><span class="sxs-lookup"><span data-stu-id="f1765-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="f1765-170">**Oppsett** – denne komponenten gjør det mulig for brukere av globaliseringstjenester, for eksempel en e-faktureringstjeneste, å styre oppsettet av den relaterte funksjonsversjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="f1765-171">Derfor støtter den den fleksible konstruksjonen av kommunikasjons- og svarregler.</span><span class="sxs-lookup"><span data-stu-id="f1765-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="f1765-172">**Miljø** – med denne komponenten kan brukere av globaliseringstjenester som for eksempel en e-faktureringstjeneste, administrere miljøet der funksjonsversjonsoppsettet brukes, og gi godkjenning til brukerne som skal ha tilgang til det.</span><span class="sxs-lookup"><span data-stu-id="f1765-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="f1765-173">**Organisasjoner** – denne komponenten gjør det mulig for brukere å dele funksjonen med eksterne organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="f1765-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="f1765-174">Konfigurere funksjonskomponenter</span><span class="sxs-lookup"><span data-stu-id="f1765-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="f1765-175">Versjon og status</span><span class="sxs-lookup"><span data-stu-id="f1765-175">Version and status</span></span>

<span data-ttu-id="f1765-176">Versjonen brukes til å administrere globaliseringsfunksjonens livssyklus.</span><span class="sxs-lookup"><span data-stu-id="f1765-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="f1765-177">Statusen kan endres i **Status**-feltet i **Versjon**-kategorien. Følgende statuser er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f1765-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="f1765-178">**Utkast** – funksjonen kan bare redigeres når den er i denne statusen.</span><span class="sxs-lookup"><span data-stu-id="f1765-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="f1765-179">**Fullført** – funksjonen og alle relaterte komponenter er sluttført (fullført), og kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="f1765-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="f1765-180">**Publisert** – funksjonen og alle relaterte komponenter har blitt publisert til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="f1765-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="f1765-181">**Delt** – funksjonen og alle relaterte komponenter er delt med eksterne organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="f1765-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="f1765-182">**Aktivert** – funksjonen og alle relaterte komponenter har blitt aktivert for bruk i en globaliseringstjeneste som for eksempel en e-faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="f1765-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="f1765-183">Funksjoner må gå sekvensielt gjennom noen av disse statusene.</span><span class="sxs-lookup"><span data-stu-id="f1765-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="f1765-184">Derfor er kanskje ikke hver enkelt status tilgjengelig for hvert eneste stadium i livssyklusen.</span><span class="sxs-lookup"><span data-stu-id="f1765-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="f1765-185">Konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="f1765-185">Configurations</span></span>

<span data-ttu-id="f1765-186">Følgende handlinger er tilgjengelige for konfigurasjoner:</span><span class="sxs-lookup"><span data-stu-id="f1765-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="f1765-187">**Vis** – Vis de underliggende funksjonskonfigurasjonene som ikke krever noen oppdatering.</span><span class="sxs-lookup"><span data-stu-id="f1765-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="f1765-188">**Rediger** – Opprett en utkastversjon av en valgt konfigurasjon slik at du kan redigere formatet eller formattilordningen i Formatutforming-programmet.</span><span class="sxs-lookup"><span data-stu-id="f1765-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="f1765-189">**Slett** – Slett en valgt konfigurasjon fra funksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="f1765-190">**Rebaser** – baser funksjonen på nytt.</span><span class="sxs-lookup"><span data-stu-id="f1765-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="f1765-191">Hvis du vil ha mer informasjon, kan du se [Rebasere avledede globaliseringsfunksjoner](#rebase)-delen senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f1765-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="f1765-192">Oppsett</span><span class="sxs-lookup"><span data-stu-id="f1765-192">Setups</span></span>

<span data-ttu-id="f1765-193">Følgende handlinger er tilgjengelige for konfigurasjon av funksjoner:</span><span class="sxs-lookup"><span data-stu-id="f1765-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="f1765-194">**Legg til** – Opprett en ny funksjonskonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f1765-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="f1765-195">Dette funksjonsoppsettet kan avledes fra et eksisterende funksjonsoppsett eller opprettes fra bunnen av.</span><span class="sxs-lookup"><span data-stu-id="f1765-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="f1765-196">**Slett** – Slett en valgt funksjonskonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f1765-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="f1765-197">**Vis** – Vis et underliggende funksjonsoppsett som ikke krever noen endringer.</span><span class="sxs-lookup"><span data-stu-id="f1765-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="f1765-198">**Rediger** – Opprett, slett eller endre attributtene for de tre hovedkomponentene i et funksjonsoppsett:</span><span class="sxs-lookup"><span data-stu-id="f1765-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="f1765-199">Handlinger og parametrene deres</span><span class="sxs-lookup"><span data-stu-id="f1765-199">Actions and their parameters</span></span>
    - <span data-ttu-id="f1765-200">Relevansregler</span><span class="sxs-lookup"><span data-stu-id="f1765-200">Applicability rules</span></span>
    - <span data-ttu-id="f1765-201">Variabler</span><span class="sxs-lookup"><span data-stu-id="f1765-201">Variables</span></span>

![Konfigurasjonsside for funksjonsversjon](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="f1765-203">Miljøer</span><span class="sxs-lookup"><span data-stu-id="f1765-203">Environments</span></span>

<span data-ttu-id="f1765-204">Følgende handlinger er tilgjengelige for miljøer:</span><span class="sxs-lookup"><span data-stu-id="f1765-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="f1765-205">**Aktiver** – for en valgt funksjonsversjon velger du et publisert miljø, og velger en **Gyldig fra**-dato når den skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f1765-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="f1765-206">Hvis du vil ha mer informasjon, kan du se [Konfigurere miljøer for aktivering](#configureenvironment)-delen senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f1765-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="f1765-207">**Avbryt** – Fjern et miljø for et funksjonsoppsett.</span><span class="sxs-lookup"><span data-stu-id="f1765-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="f1765-208">Organisasjoner</span><span class="sxs-lookup"><span data-stu-id="f1765-208">Organizations</span></span>

<span data-ttu-id="f1765-209">Følg disse trinnene for å dele en globaliseringsfunksjon med en ekstern organisasjon.</span><span class="sxs-lookup"><span data-stu-id="f1765-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="f1765-210">På **E-faktureringsfunksjoner**-siden velger du funksjonen og funksjonsversjonen som skal deles.</span><span class="sxs-lookup"><span data-stu-id="f1765-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="f1765-211">I **Organisasjoner**-kategorien velger du **Del med**, og angir deretter organisasjonens domenenavn i rullegardinmenyen for dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f1765-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="f1765-212">Velg **Del**.</span><span class="sxs-lookup"><span data-stu-id="f1765-212">Select **Share**.</span></span>

    ![Dele en funksjon med en organisasjon](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="f1765-214">Funksjonen deles med den valgte organisasjonen, og er tilgjengelig for den organisasjonen i det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="f1765-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="f1765-215">Derfra kan funksjonen importeres til organisasjonens forekomst av RCS eller Dynamics 365 Finance, slik at den kan brukes.</span><span class="sxs-lookup"><span data-stu-id="f1765-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="f1765-216">Rebaser avledede globaliseringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f1765-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="f1765-217">Du kan rebasere en avledet globaliseringsfunksjon til den nye eller oppdaterte basefunksjonsversjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="f1765-218">På denne måten kan endringer som er utført i baseversjonen, oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="f1765-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="f1765-219">Den oppdaterte basefunksjonsversjonen opprettes av den opprinnelige konfigurasjonsleverandøren, og den blir deretter publisert eller delt.</span><span class="sxs-lookup"><span data-stu-id="f1765-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Oppdatert grunnleggende funksjonsversjon](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="f1765-221">Hvis du for eksempel vil rebasere den avledede versjonen av en funksjon du har opprettet, får du først den siste versjonen av funksjonen ved å importere den fra det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="f1765-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="f1765-222">På siden **E-faktureringsfunksjoner** velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="f1765-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="f1765-223">Velg **Synkroniser** for å få de nyeste funksjonene.</span><span class="sxs-lookup"><span data-stu-id="f1765-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="f1765-224">I listen over funksjoner velger du funksjonene som skal importeres, og deretter velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="f1765-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Importere den nyeste versjonen av en funksjon](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="f1765-226">I listen over funksjoner velger du funksjonen som skal rebaseres.</span><span class="sxs-lookup"><span data-stu-id="f1765-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="f1765-227">I **Versjon**-kategorien velger du **Ny** for å opprette en utkastversjon.</span><span class="sxs-lookup"><span data-stu-id="f1765-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Ny utkastversjon opprettet](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="f1765-229">Velg **Rebaser**.</span><span class="sxs-lookup"><span data-stu-id="f1765-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="f1765-230">I **Rebaser**-dialogboksen velger du den siste versjonen av funksjonen du vil rebasere til.</span><span class="sxs-lookup"><span data-stu-id="f1765-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Dialogboksen Rebaser](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="f1765-232">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1765-232">Select **OK**.</span></span>
9. <span data-ttu-id="f1765-233">Se gjennom funksjonskomponentene, og foreta eventuelle endringer etter behov.</span><span class="sxs-lookup"><span data-stu-id="f1765-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="f1765-234">Velg **Endre status** for å fullføre den rebaserte funksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1765-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="f1765-235">Når rebaseringen er fullført, kan du utføre flere handlinger.</span><span class="sxs-lookup"><span data-stu-id="f1765-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="f1765-236">Du kan for eksempel publisere funksjonen og gjøre den tilgjengelig for bruk i globaliseringstjenester.</span><span class="sxs-lookup"><span data-stu-id="f1765-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Funksjonsstatusen oppdateres til Fullført](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="f1765-238">Konfigurere miljøer for globaliseringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f1765-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="f1765-239">Brukere av globaliseringstjenester kan styre miljøet for å definere en globaliseringsfunksjon og gi autorisasjon til andre brukere som får tilgang til den.</span><span class="sxs-lookup"><span data-stu-id="f1765-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="f1765-240">I **Globaliseringsfunksjoner**-arbeidsområdet, under **Miljøer**, velger du flisen **E-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="f1765-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Arbeidsområde for globaliseringsfunksjoner](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="f1765-242">Velg **Nøkkelhvelv-parametere** og deretter **Ny** for å opprette en hemmelighet for Azure Nøkkelhvelv.</span><span class="sxs-lookup"><span data-stu-id="f1765-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="f1765-243">Angi et navn og en beskrivelse for Nøkkelhvelv, gå til **URI for nøkkelhvelv**-feltet og angi URL-adressen som identifiserer Nøkkelhvelv-ressursen i Azure.</span><span class="sxs-lookup"><span data-stu-id="f1765-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="f1765-244">I **Sertifikater**-hurtigkategorien velger du **Legg til** for å legge til sertifikatet, og skriv deretter inn et navn og en beskrivelse for hvert sertifikat.</span><span class="sxs-lookup"><span data-stu-id="f1765-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Sertifikat lagt til](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="f1765-246">Velg **Ny** for å opprette et nytt miljø.</span><span class="sxs-lookup"><span data-stu-id="f1765-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="f1765-247">Angi et navn, en beskrivelse og tokenet for signaturkode for delt tilgang som kreves for å lagre.</span><span class="sxs-lookup"><span data-stu-id="f1765-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="f1765-248">I **Brukere**-hurtigkategorien velger du **Ny** for å legge til en bruker som skal ha tilgangstillatelse til dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="f1765-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="f1765-249">Angi brukerens bruker-ID og e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="f1765-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="f1765-250">Gjenta trinn 7 og 8 for å legge til flere brukere.</span><span class="sxs-lookup"><span data-stu-id="f1765-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="f1765-251">Velg **Publiser** for å publisere miljøet.</span><span class="sxs-lookup"><span data-stu-id="f1765-251">Select **Publish** to publish the environment.</span></span>

    ![Publisert miljø](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
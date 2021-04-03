---
title: Klargjøre et evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du klargjør et evalueringsmiljø for Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a57cc02c6d62f288f14b65191c2f4927a019963c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478170"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="999c3-103">Klargjøre et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="999c3-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="999c3-104">Dette emnet forklarer hvordan du klargjør et evalueringsmiljø for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="999c3-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="999c3-105">Før du begynner, anbefaler vi at du tar en rask titt på dette emnet for å få en pekepinn på hva prosessen krever.</span><span class="sxs-lookup"><span data-stu-id="999c3-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="999c3-106">Commerce-evalueringsmiljøer er ikke generelt tilgjengelige, og gis til partnere og kunder på et per forespørsel-grunnlag.</span><span class="sxs-lookup"><span data-stu-id="999c3-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="999c3-107">Hvis du vil ha mer informasjon, ta kontakt med din Microsoft-partnerkontakten din.</span><span class="sxs-lookup"><span data-stu-id="999c3-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="999c3-108">For å kunne klargjøre et Commerce-evalueringsmiljø må du opprette et prosjekt som har et bestemt produktnavn og type.</span><span class="sxs-lookup"><span data-stu-id="999c3-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="999c3-109">Miljøet og Commerce Scale Unit (CSU) har også bestemte parametere du må bruke når du forventer å klargjøre e-handel senere.</span><span class="sxs-lookup"><span data-stu-id="999c3-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="999c3-110">Instruksjonene i dette emnet beskriver alle nødvendige trinn som må fullføres for å klargjøre, og parameterne du må bruke.</span><span class="sxs-lookup"><span data-stu-id="999c3-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="999c3-111">Når klargjøringen av Commerce-evalueringsmiljøet er fullført, er det noen få trinn du må ta i etterkant for å klargjøre det for bruk.</span><span class="sxs-lookup"><span data-stu-id="999c3-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="999c3-112">Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil evaluere.</span><span class="sxs-lookup"><span data-stu-id="999c3-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="999c3-113">Du kan alltid fullføre de valgfrie trinnene senere.</span><span class="sxs-lookup"><span data-stu-id="999c3-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="999c3-114">Hvis du vil ha informasjon om hvordan du konfigurerer Commerce-evalueringsmiljøet etter klargjøring, kan du se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="999c3-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="999c3-115">Hvis du vil ha informasjon om hvordan du konfigurerer valgfrie funksjoner for Commerce-evalueringsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-evalueringsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="999c3-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="999c3-116">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="999c3-116">Prerequisites</span></span>

<span data-ttu-id="999c3-117">Følgende forutsetninger må være på plass før du kan klargjøre Commerce-evalueringsmiljøet:</span><span class="sxs-lookup"><span data-stu-id="999c3-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="999c3-118">Du er introdusert til evalueringsprogrammet og tildelt kapasitet for et evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="999c3-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="999c3-119">Du har tilgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).</span><span class="sxs-lookup"><span data-stu-id="999c3-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="999c3-120">Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan opprette et Dynamics 365 Commerce-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="999c3-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="999c3-121">Du har administratortilgang til Microsoft Azure-abonnementet, eller du er i kontakt med en abonnementsadministrator som kan hjelpe deg hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="999c3-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="999c3-122">Du har Azure Active Directory (Azure AD) tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="999c3-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="999c3-123">Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som systemadministratorgruppe for e-handel, og du har ID-en tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="999c3-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="999c3-124">Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som moderatorgruppe for vurderinger og omtaler, og du har ID-en tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="999c3-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="999c3-125">(Denne sikkerhetsgruppen kan være den samme som systemadministrasjonsgruppen for e-handel.)</span><span class="sxs-lookup"><span data-stu-id="999c3-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="999c3-126">Legg merke til at denne listen ikke er fullstendig.</span><span class="sxs-lookup"><span data-stu-id="999c3-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="999c3-127">Hvis du opplever problemer, kontakter du Microsoft-partnerkontakten for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="999c3-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="999c3-128">Klargjøre Commerce-evalueringsmiljøet</span><span class="sxs-lookup"><span data-stu-id="999c3-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="999c3-129">Disse prosedyrene forklarer hvordan du klargjør et Commerce-evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="999c3-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="999c3-130">Når du har fullført dem, vil evalueringsmiljøet for Commerce være klart for konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="999c3-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="999c3-131">Alle aktivitetene som beskrives her, skjer i LCS-portalen.</span><span class="sxs-lookup"><span data-stu-id="999c3-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="999c3-132">Opprett nytt prosjekt</span><span class="sxs-lookup"><span data-stu-id="999c3-132">Create a new project</span></span>

<span data-ttu-id="999c3-133">Hvis du vil opprette et nytt prosjekt i LCS, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="999c3-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="999c3-134">På LCS-startsiden velger du plusstegnet (**+**) for å opprette et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="999c3-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="999c3-135">I den høyre ruten følger du ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="999c3-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="999c3-136">Hvis du er en partner, velger du **Overfør, opprett løsninger og finn ut mer om**.</span><span class="sxs-lookup"><span data-stu-id="999c3-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="999c3-137">Hvis du er kunde, velger du **Potensielt førsalg**.</span><span class="sxs-lookup"><span data-stu-id="999c3-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="999c3-138">Angi navn, beskrivelse og bransje.</span><span class="sxs-lookup"><span data-stu-id="999c3-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="999c3-139">I **Produktnavn**-feltet velger du **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="999c3-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="999c3-140">I **Produktversjon**-feltet velger du **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="999c3-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="999c3-141">I **Metodologi**-feltet velger du **Implementeringsmetodologi for Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="999c3-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="999c3-142">Valgfritt: Du kan importere roller og brukere fra et eksisterende prosjekt.</span><span class="sxs-lookup"><span data-stu-id="999c3-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="999c3-143">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="999c3-143">Select **Create**.</span></span> <span data-ttu-id="999c3-144">Prosjektvisningen vises.</span><span class="sxs-lookup"><span data-stu-id="999c3-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="999c3-145">Legge til Azure-koblingen</span><span class="sxs-lookup"><span data-stu-id="999c3-145">Add the Azure Connector</span></span>

<span data-ttu-id="999c3-146">Hvis du vil legge til Azure-kobling i LCS-prosjektet, følger du fremgangsmåten i [Fullføre jobbintroduksjon for Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="999c3-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="999c3-147">Distribuere miljøet</span><span class="sxs-lookup"><span data-stu-id="999c3-147">Deploy the environment</span></span>

<span data-ttu-id="999c3-148">Gjør følgende for å distribuere miljøet.</span><span class="sxs-lookup"><span data-stu-id="999c3-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="999c3-149">Det kan hende du ikke trenger å fullføre trinn 6, 7 og/eller 8 fordi sider som har et enkelt alternativ, hoppes over.</span><span class="sxs-lookup"><span data-stu-id="999c3-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="999c3-150">Når du er i **Miljøparametere**-visningen, bekrefter du at teksten **Dynamics 365 Commerce - demo (10.0.* x* med Platform update *xx*)\*\* vises rett over **Miljønavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="999c3-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="999c3-151">For mer informasjon, se illustrasjonen som vises etter trinn 8.</span><span class="sxs-lookup"><span data-stu-id="999c3-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="999c3-152">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="999c3-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="999c3-153">Klikk **Legg til** for å legge til et miljø.</span><span class="sxs-lookup"><span data-stu-id="999c3-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="999c3-154">I feltet **Programversjon** velger du den nyeste versjonen.</span><span class="sxs-lookup"><span data-stu-id="999c3-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="999c3-155">Hvis du har et bestemt behov for å velge en annen programversjon enn den nyeste versjonen, må du ikke velge en tidligere versjon enn **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="999c3-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="999c3-156">I **Plattformversjon**-feltet bruker du plattformversjonen som automatisk velges for den valgte programversjonen.</span><span class="sxs-lookup"><span data-stu-id="999c3-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Velge program- og plattformversjoner](./media/project1.png)

1. <span data-ttu-id="999c3-158">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="999c3-158">Select **Next**.</span></span>
1. <span data-ttu-id="999c3-159">Velg **Demo** som miljøtopologien.</span><span class="sxs-lookup"><span data-stu-id="999c3-159">Select **Demo** as the environment topology.</span></span>

    ![Velge miljøtopologien 1](./media/project2.png)

1. <span data-ttu-id="999c3-161">På **Distribusjonsmiljø**-siden angir du et miljønavn.</span><span class="sxs-lookup"><span data-stu-id="999c3-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="999c3-162">La Avanserte innstillinger stå som de er.</span><span class="sxs-lookup"><span data-stu-id="999c3-162">Leave the advanced settings as they are.</span></span>

    ![Distribusjonsmiljø-siden](./media/project4.png)

1. <span data-ttu-id="999c3-164">Juster VM-størrelsen etter behov.</span><span class="sxs-lookup"><span data-stu-id="999c3-164">Adjust the VM size as required.</span></span> <span data-ttu-id="999c3-165">(Vi anbefaler VM-lagerenhet \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="999c3-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="999c3-166">Se gjennom vilkårene for prising og lisensiering, og merk deretter av i avmerkingsboksen for å angi at du godtar dem.</span><span class="sxs-lookup"><span data-stu-id="999c3-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="999c3-167">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="999c3-167">Select **Next**.</span></span>
1. <span data-ttu-id="999c3-168">Klikk **Distribuer** på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige.</span><span class="sxs-lookup"><span data-stu-id="999c3-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="999c3-169">Du kommer tilbake til visningen **Skybaserte miljøer**, og miljøet skal vises i listen.</span><span class="sxs-lookup"><span data-stu-id="999c3-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="999c3-170">Det forespurte miljøet vil vises som en kø og deretter distribueres.</span><span class="sxs-lookup"><span data-stu-id="999c3-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="999c3-171">Miljøarbeidsflytene vil ta litt tid å fullføre.</span><span class="sxs-lookup"><span data-stu-id="999c3-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="999c3-172">Kom derfor tilbake etter ca seks til ni timer.</span><span class="sxs-lookup"><span data-stu-id="999c3-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="999c3-173">Før du fortsetter må du kontrollere at miljøstatusen er **Distribuert**.</span><span class="sxs-lookup"><span data-stu-id="999c3-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="999c3-174">Initialisere Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="999c3-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="999c3-175">For å initialisere CSU-en, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="999c3-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="999c3-176">Velg miljøet ditt fra listen i visningen **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="999c3-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="999c3-177">Klikk **Detaljerte opplysninger** i miljøvisningen til høyre.</span><span class="sxs-lookup"><span data-stu-id="999c3-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="999c3-178">Detaljerte opplysninger for miljø vises.</span><span class="sxs-lookup"><span data-stu-id="999c3-178">The environment details view appears.</span></span>
1. <span data-ttu-id="999c3-179">Klikk **Behandle** under **Miljøfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="999c3-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="999c3-180">Velg **Initialiser** i kategorien **Handel**.</span><span class="sxs-lookup"><span data-stu-id="999c3-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="999c3-181">Visningen av parametere for CSU-initialisering vises.</span><span class="sxs-lookup"><span data-stu-id="999c3-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="999c3-182">I **Område**-feltet velger du det samme området eller et område nær der du distribuerte miljøet til.</span><span class="sxs-lookup"><span data-stu-id="999c3-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="999c3-183">La **Versjon**-feltet være slik det er.</span><span class="sxs-lookup"><span data-stu-id="999c3-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="999c3-184">Velg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="999c3-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="999c3-185">Klikk **Ja** på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige.</span><span class="sxs-lookup"><span data-stu-id="999c3-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="999c3-186">Visningen **Handelsadministrasjon** vises på nytt med kategorien **Handel** valgt.</span><span class="sxs-lookup"><span data-stu-id="999c3-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="999c3-187">CSU-en din er lagt i kø for klargjøring.</span><span class="sxs-lookup"><span data-stu-id="999c3-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="999c3-188">Før du fortsetter må du kontrollere at miljøstatusen til CSU er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="999c3-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="999c3-189">Initialiseringen tar omtrent to til fem timer.</span><span class="sxs-lookup"><span data-stu-id="999c3-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="999c3-190">Hvis du ikke finner **Behandle**-koblingen i miljødetaljvisningen, kontakter du Microsoft-kontakten for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="999c3-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="999c3-191">Under distribusjonsprosessen kan du få følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="999c3-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="999c3-192">Evalueringsmiljøer (demo/test) må registrere programmet for skaleringsenhetstilkobling \<application ID\> på hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="999c3-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="999c3-193">Hvis CSU-initialiseringen mislykkes og du får denne feilmeldingen, noterer du deg program-IDen, som er en globalt unik ID (ASSE), og følger deretter trinnene i den neste delen for å registrere CSU-distribusjonsprogrammet i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="999c3-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="999c3-194">Registrere CSU-distribusjonsprogrammet i Commerce Headquarters (om nødvendig)</span><span class="sxs-lookup"><span data-stu-id="999c3-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="999c3-195">For å registrere CSU-distribusjonsprogrammet i Commerce Headquarters, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="999c3-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="999c3-196">I Commerce headquarters kan du gå til **Systemadministrasjon \> Oppsett \> Azure Active Directory-programmer**.</span><span class="sxs-lookup"><span data-stu-id="999c3-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="999c3-197">Angi **Klient-ID**-kolonnen, angi program-ID fra CSU-initialiseringsfeilmeldingen du mottok.</span><span class="sxs-lookup"><span data-stu-id="999c3-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="999c3-198">I **Navn**-kolonnen angir du en beskrivende tekst (for eksempel **CSU-eval**).</span><span class="sxs-lookup"><span data-stu-id="999c3-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="999c3-199">I kolonnen **Bruker-ID** angir du **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="999c3-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="999c3-200">Forsøk på CSU-initialisering og distribusjon fra LCS.</span><span class="sxs-lookup"><span data-stu-id="999c3-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="999c3-201">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="999c3-201">Initialize e-Commerce</span></span>

<span data-ttu-id="999c3-202">Hvis du vil initialisere e-handel, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="999c3-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="999c3-203">I kategorien **E-handel** ser du gjennom samtykket for evalueringen, og velg deretter **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="999c3-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="999c3-204">Angi et navn i feltet for **Navn på e-handelsmiljø**.</span><span class="sxs-lookup"><span data-stu-id="999c3-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="999c3-205">Vær oppmerksom på at dette navnet vil vises i noen av URL-adressene som peker til e-handelsforekomsten.</span><span class="sxs-lookup"><span data-stu-id="999c3-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="999c3-206">I feltet **Commerce Scale Unit-navn** velger du CSU-en i listen.</span><span class="sxs-lookup"><span data-stu-id="999c3-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="999c3-207">(Listen bør bare ha ett alternativ.)</span><span class="sxs-lookup"><span data-stu-id="999c3-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="999c3-208">Feltet **Geografi for e-handel** angis automatisk.</span><span class="sxs-lookup"><span data-stu-id="999c3-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="999c3-209">Klikk **Neste** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="999c3-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="999c3-210">I feltet **Støttede vertsnavn** angir du et gyldig domene, for eksempel `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="999c3-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="999c3-211">Feltet **AAD-sikkerhetsgruppe for systemadministrasjon** angir de første bokstavene i navnet på sikkerhetsgruppen du vil bruke, og deretter velger du forstørrelsesglassymbolet for å vise søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="999c3-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="999c3-212">Velg riktig sikkerhetsgruppe i listen.</span><span class="sxs-lookup"><span data-stu-id="999c3-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="999c3-213">Feltet **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir de første bokstavene i navnet på sikkerhetsgruppen du vil bruke, og deretter velger du forstørrelsesglassymbolet for å vise søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="999c3-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="999c3-214">Velg riktig sikkerhetsgruppe i listen.</span><span class="sxs-lookup"><span data-stu-id="999c3-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="999c3-215">La alternativet **Aktiver tjenesten for vurderinger og omtale** settes til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="999c3-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="999c3-216">Velg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="999c3-216">Select **Initialize**.</span></span> <span data-ttu-id="999c3-217">Visningen **Handelsadministrasjon** vises på nytt med kategorien **E-handel** valgt.</span><span class="sxs-lookup"><span data-stu-id="999c3-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="999c3-218">Initialiseringen av e-handel har startet.</span><span class="sxs-lookup"><span data-stu-id="999c3-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="999c3-219">Før du fortsetter må du vente til initialiseringsstatusen for e-handel er **Initialisering vellykket**.</span><span class="sxs-lookup"><span data-stu-id="999c3-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="999c3-220">Under **Koblinger** ned til høyre noterer du URL-adressene for følgende koblinger:</span><span class="sxs-lookup"><span data-stu-id="999c3-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="999c3-221">**E-handelsområde** – koblingen til roten for e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="999c3-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="999c3-222">**Commerce-områdebygger** – koblingen til verktøyet for områdeadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="999c3-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="999c3-223">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="999c3-223">Next steps</span></span>

<span data-ttu-id="999c3-224">Hvis du vil fortsette prosessen for å klargjøre og konfigurere Commerce-evalueringsmiljøet, kan du se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="999c3-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="999c3-225">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="999c3-225">Additional resources</span></span>

[<span data-ttu-id="999c3-226">Oversikt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="999c3-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="999c3-227">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="999c3-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="999c3-228">Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="999c3-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="999c3-229">Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="999c3-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="999c3-230">Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="999c3-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="999c3-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="999c3-231">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="999c3-232">Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="999c3-232">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="999c3-233">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="999c3-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="999c3-234">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="999c3-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

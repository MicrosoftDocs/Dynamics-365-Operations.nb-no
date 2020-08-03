---
title: Klargjøre et evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-evalueringsmiljø.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e5ce2002c66a1c36d5647d3c76684b394fc1ff79
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599856"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="17d6d-103">Klargjøre et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="17d6d-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17d6d-104">Dette emnet forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="17d6d-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="17d6d-105">Før du begynner, anbefaler vi at du tar en rask titt på dette emnet for å få en pekepinn på hva prosessen krever.</span><span class="sxs-lookup"><span data-stu-id="17d6d-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="17d6d-106">Commerce-evalueringsmiljøer er ikke generelt tilgjengelige, og gis til partnere og kunder på et per forespørsel-grunnlag.</span><span class="sxs-lookup"><span data-stu-id="17d6d-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="17d6d-107">Hvis du vil ha mer informasjon, ta kontakt med din Microsoft-partnerkontakten din.</span><span class="sxs-lookup"><span data-stu-id="17d6d-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="17d6d-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="17d6d-108">Overview</span></span>

<span data-ttu-id="17d6d-109">For å kunne klargjøre et Commerce-evalueringsmiljø må du opprette et prosjekt som har et bestemt produktnavn og type.</span><span class="sxs-lookup"><span data-stu-id="17d6d-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="17d6d-110">Miljøet og Commerce Scale Unit (CSU) har også bestemte parametere du må bruke når du forventer å klargjøre e-handel senere.</span><span class="sxs-lookup"><span data-stu-id="17d6d-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="17d6d-111">Instruksjonene i dette emnet beskriver alle nødvendige trinn som må fullføres for å klargjøre, og parameterne du må bruke.</span><span class="sxs-lookup"><span data-stu-id="17d6d-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="17d6d-112">Når klargjøringen av Commerce-evalueringsmiljøet er fullført, er det noen få trinn du må ta i etterkant for å klargjøre det for bruk.</span><span class="sxs-lookup"><span data-stu-id="17d6d-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="17d6d-113">Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil evaluere.</span><span class="sxs-lookup"><span data-stu-id="17d6d-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="17d6d-114">Du kan alltid fullføre de valgfrie trinnene senere.</span><span class="sxs-lookup"><span data-stu-id="17d6d-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="17d6d-115">Hvis du vil ha informasjon om hvordan du konfigurerer Commerce-evalueringsmiljøet etter klargjøring, kan du se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="17d6d-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="17d6d-116">Hvis du vil ha informasjon om hvordan du konfigurerer valgfrie funksjoner for Commerce-evalueringsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-evalueringsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="17d6d-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="17d6d-117">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="17d6d-117">Prerequisites</span></span>

<span data-ttu-id="17d6d-118">Følgende forutsetninger må være på plass før du kan klargjøre Commerce-evalueringsmiljøet:</span><span class="sxs-lookup"><span data-stu-id="17d6d-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="17d6d-119">Du har tilgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).</span><span class="sxs-lookup"><span data-stu-id="17d6d-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="17d6d-120">Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan opprette et Dynamics 365 Commerce-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="17d6d-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="17d6d-121">Du har administratortilgang til Microsoft Azure-abonnementet, eller du er i kontakt med en abonnementsadministrator som kan hjelpe deg hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="17d6d-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="17d6d-122">Du har Azure Active Directory (Azure AD) tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="17d6d-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="17d6d-123">Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som systemadministratorgruppe for e-handel, og du har ID-en tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="17d6d-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="17d6d-124">Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som moderatorgruppe for vurderinger og omtaler, og du har ID-en tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="17d6d-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="17d6d-125">(Denne sikkerhetsgruppen kan være den samme som systemadministrasjonsgruppen for e-handel.)</span><span class="sxs-lookup"><span data-stu-id="17d6d-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="17d6d-126">Legg merke til at denne listen ikke er fullstendig.</span><span class="sxs-lookup"><span data-stu-id="17d6d-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="17d6d-127">Hvis du opplever problemer, kontakter du Microsoft-partnerkontakten for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="17d6d-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="17d6d-128">Klargjøre Commerce-evalueringsmiljøet</span><span class="sxs-lookup"><span data-stu-id="17d6d-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="17d6d-129">Disse prosedyrene forklarer hvordan du klargjør et Commerce-evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="17d6d-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="17d6d-130">Når du har fullført dem, vil evalueringsmiljøet for Commerce være klart for konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="17d6d-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="17d6d-131">Alle aktivitetene som beskrives her, skjer i LCS-portalen.</span><span class="sxs-lookup"><span data-stu-id="17d6d-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="17d6d-132">Opprett nytt prosjekt</span><span class="sxs-lookup"><span data-stu-id="17d6d-132">Create a new project</span></span>

<span data-ttu-id="17d6d-133">Hvis du vil opprette et nytt prosjekt i LCS, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="17d6d-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="17d6d-134">På LCS-startsiden velger du plusstegnet (**+**) for å opprette et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="17d6d-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="17d6d-135">I den høyre ruten følger du ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="17d6d-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="17d6d-136">Hvis du er en partner, velger du **Overfør, opprett løsninger og finn ut mer om**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="17d6d-137">Hvis du er kunde, velger du **Potensielt førsalg**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="17d6d-138">Angi navn, beskrivelse og bransje.</span><span class="sxs-lookup"><span data-stu-id="17d6d-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="17d6d-139">I **Produktnavn**-feltet velger du **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="17d6d-140">I **Produktversjon**-feltet velger du **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="17d6d-141">I **Metodologi**-feltet velger du **Implementeringsmetodologi for Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="17d6d-142">Valgfritt: Du kan importere roller og brukere fra et eksisterende prosjekt.</span><span class="sxs-lookup"><span data-stu-id="17d6d-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="17d6d-143">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-143">Select **Create**.</span></span> <span data-ttu-id="17d6d-144">Prosjektvisningen vises.</span><span class="sxs-lookup"><span data-stu-id="17d6d-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="17d6d-145">Legge til Azure-koblingen</span><span class="sxs-lookup"><span data-stu-id="17d6d-145">Add the Azure Connector</span></span>

<span data-ttu-id="17d6d-146">Hvis du vil legge til Azure-kobling i LCS-prosjektet, følger du fremgangsmåten i [Fullføre jobbintroduksjon for Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="17d6d-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="17d6d-147">Distribuere miljøet</span><span class="sxs-lookup"><span data-stu-id="17d6d-147">Deploy the environment</span></span>

<span data-ttu-id="17d6d-148">Gjør følgende for å distribuere miljøet.</span><span class="sxs-lookup"><span data-stu-id="17d6d-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="17d6d-149">Det kan hende du ikke trenger å fullføre trinn 6, 7 og/eller 8 fordi sider som har et enkelt alternativ, hoppes over.</span><span class="sxs-lookup"><span data-stu-id="17d6d-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="17d6d-150">Når du er i **Miljøparametere**-visningen, bekrefter du at teksten **Dynamics 365 Commerce - demo (10.0.* x* med Platform update *xx*)\*\* vises rett over **Miljønavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="17d6d-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="17d6d-151">For mer informasjon, se illustrasjonen som vises etter trinn 8.</span><span class="sxs-lookup"><span data-stu-id="17d6d-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="17d6d-152">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="17d6d-153">Klikk **Legg til** for å legge til et miljø.</span><span class="sxs-lookup"><span data-stu-id="17d6d-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="17d6d-154">I feltet **Programversjon** velger du den nyeste versjonen.</span><span class="sxs-lookup"><span data-stu-id="17d6d-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="17d6d-155">Hvis du har et bestemt behov for å velge en annen programversjon enn den nyeste versjonen, må du ikke velge en tidligere versjon enn **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="17d6d-156">I **Plattformversjon**-feltet bruker du plattformversjonen som automatisk velges for den valgte programversjonen.</span><span class="sxs-lookup"><span data-stu-id="17d6d-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Velge program- og plattformversjoner](./media/project1.png)

1. <span data-ttu-id="17d6d-158">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-158">Select **Next**.</span></span>
1. <span data-ttu-id="17d6d-159">Velg **Demo** som miljøtopologien.</span><span class="sxs-lookup"><span data-stu-id="17d6d-159">Select **Demo** as the environment topology.</span></span>

    ![Velge miljøtopologien 1](./media/project2.png)

1. <span data-ttu-id="17d6d-161">På **Distribusjonsmiljø**-siden angir du et miljønavn.</span><span class="sxs-lookup"><span data-stu-id="17d6d-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="17d6d-162">La Avanserte innstillinger stå som de er.</span><span class="sxs-lookup"><span data-stu-id="17d6d-162">Leave the advanced settings as they are.</span></span>

    ![Distribusjonsmiljø-siden](./media/project4.png)

1. <span data-ttu-id="17d6d-164">Juster VM-størrelsen etter behov.</span><span class="sxs-lookup"><span data-stu-id="17d6d-164">Adjust the VM size as required.</span></span> <span data-ttu-id="17d6d-165">(Vi anbefaler VM-lagerenhet \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="17d6d-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="17d6d-166">Se gjennom vilkårene for prising og lisensiering, og merk deretter av i avmerkingsboksen for å angi at du godtar dem.</span><span class="sxs-lookup"><span data-stu-id="17d6d-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="17d6d-167">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-167">Select **Next**.</span></span>
1. <span data-ttu-id="17d6d-168">Klikk **Distribuer**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige.</span><span class="sxs-lookup"><span data-stu-id="17d6d-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="17d6d-169">Du kommer tilbake til visningen **Skybaserte miljøer**, og miljøet skal vises i listen.</span><span class="sxs-lookup"><span data-stu-id="17d6d-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="17d6d-170">Det forespurte miljøet vil vises som en kø og deretter distribueres.</span><span class="sxs-lookup"><span data-stu-id="17d6d-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="17d6d-171">Miljøarbeidsflytene vil ta litt tid å fullføre.</span><span class="sxs-lookup"><span data-stu-id="17d6d-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="17d6d-172">Kom derfor tilbake etter ca seks til ni timer.</span><span class="sxs-lookup"><span data-stu-id="17d6d-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="17d6d-173">Før du fortsetter må du kontrollere at miljøstatusen er **Distribuert**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="17d6d-174">Initialisere Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="17d6d-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="17d6d-175">Hvis du vil initialisere en CSU-adresse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="17d6d-175">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="17d6d-176">Velg miljøet ditt fra listen i visningen **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="17d6d-177">Klikk **Detaljerte opplysninger** i miljøvisningen til høyre.</span><span class="sxs-lookup"><span data-stu-id="17d6d-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="17d6d-178">Detaljerte opplysninger for miljø vises.</span><span class="sxs-lookup"><span data-stu-id="17d6d-178">The environment details view appears.</span></span>
1. <span data-ttu-id="17d6d-179">Klikk **Behandle** under **Miljøfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="17d6d-180">Velg **Initialiser** i kategorien **Handel**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="17d6d-181">Visningen av parametere for CSU-initialisering vises.</span><span class="sxs-lookup"><span data-stu-id="17d6d-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="17d6d-182">I **Område**-feltet velger du det samme området eller et område nær der du distribuerte miljøet til.</span><span class="sxs-lookup"><span data-stu-id="17d6d-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="17d6d-183">La **Versjon**-feltet være slik det er.</span><span class="sxs-lookup"><span data-stu-id="17d6d-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="17d6d-184">Velg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="17d6d-185">Klikk **Ja**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige.</span><span class="sxs-lookup"><span data-stu-id="17d6d-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="17d6d-186">Visningen **Handelsadministrasjon** vises på nytt med kategorien **Handel** valgt.</span><span class="sxs-lookup"><span data-stu-id="17d6d-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="17d6d-187">CSU-en din er lagt i kø for klargjøring.</span><span class="sxs-lookup"><span data-stu-id="17d6d-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="17d6d-188">Før du fortsetter må du kontrollere at miljøstatusen til CSU er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="17d6d-189">Initialiseringen tar omtrent to til fem timer.</span><span class="sxs-lookup"><span data-stu-id="17d6d-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="17d6d-190">Hvis du ikke finner **Behandle**-koblingen i miljødetaljvisningen, kontakter du Microsoft-kontakten for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="17d6d-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="17d6d-191">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="17d6d-191">Initialize e-Commerce</span></span>

<span data-ttu-id="17d6d-192">Hvis du vil initialisere e-handel, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="17d6d-192">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="17d6d-193">I kategorien **E-handel** ser du gjennom samtykket for evalueringen, og velg deretter **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-193">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="17d6d-194">Angi et navn i feltet for **Navn på e-handelsmiljø**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-194">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="17d6d-195">Vær oppmerksom på at dette navnet vil vises i noen av URL-adressene som peker til e-handelsforekomsten.</span><span class="sxs-lookup"><span data-stu-id="17d6d-195">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="17d6d-196">I feltet **Commerce Scale Unit-navn** velger du CSU-en i listen.</span><span class="sxs-lookup"><span data-stu-id="17d6d-196">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="17d6d-197">(Listen bør bare ha ett alternativ.)</span><span class="sxs-lookup"><span data-stu-id="17d6d-197">(The list should have only one option.)</span></span>

    <span data-ttu-id="17d6d-198">Feltet **Geografi for e-handel** angis automatisk.</span><span class="sxs-lookup"><span data-stu-id="17d6d-198">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="17d6d-199">Klikk **Neste** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="17d6d-199">Select **Next** to continue.</span></span>
1. <span data-ttu-id="17d6d-200">I feltet **Støttede vertsnavn** angir du et gyldig domene, for eksempel `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="17d6d-200">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="17d6d-201">Feltet **AAD-sikkerhetsgruppe for systemadministrasjon** angir de første bokstavene i navnet på sikkerhetsgruppen du vil bruke, og deretter velger du forstørrelsesglassymbolet for å vise søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="17d6d-201">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="17d6d-202">Velg riktig sikkerhetsgruppe i listen.</span><span class="sxs-lookup"><span data-stu-id="17d6d-202">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="17d6d-203">Feltet **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir de første bokstavene i navnet på sikkerhetsgruppen du vil bruke, og deretter velger du forstørrelsesglassymbolet for å vise søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="17d6d-203">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="17d6d-204">Velg riktig sikkerhetsgruppe i listen.</span><span class="sxs-lookup"><span data-stu-id="17d6d-204">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="17d6d-205">La alternativet **Aktiver tjenesten for vurderinger og omtale** settes til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-205">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="17d6d-206">Velg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-206">Select **Initialize**.</span></span> <span data-ttu-id="17d6d-207">Visningen **Handelsadministrasjon** vises på nytt med kategorien **E-handel** valgt.</span><span class="sxs-lookup"><span data-stu-id="17d6d-207">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="17d6d-208">Initialiseringen av e-handel har startet.</span><span class="sxs-lookup"><span data-stu-id="17d6d-208">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="17d6d-209">Før du fortsetter må du vente til initialiseringsstatusen for e-handel er **Initialisering vellykket**.</span><span class="sxs-lookup"><span data-stu-id="17d6d-209">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="17d6d-210">Under **Koblinger** ned til høyre noterer du URL-adressene for følgende koblinger:</span><span class="sxs-lookup"><span data-stu-id="17d6d-210">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="17d6d-211">**E-handelsområde** – koblingen til roten for e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="17d6d-211">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="17d6d-212">**Commerce-områdebygger** – koblingen til verktøyet for områdeadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="17d6d-212">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="17d6d-213">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="17d6d-213">Next steps</span></span>

<span data-ttu-id="17d6d-214">Hvis du vil fortsette prosessen for å klargjøre og konfigurere Commerce-evalueringsmiljøet, kan du se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="17d6d-214">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17d6d-215">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="17d6d-215">Additional resources</span></span>

[<span data-ttu-id="17d6d-216">Oversikt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="17d6d-216">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="17d6d-217">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="17d6d-217">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="17d6d-218">Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="17d6d-218">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="17d6d-219">Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="17d6d-219">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="17d6d-220">Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="17d6d-220">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="17d6d-221">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="17d6d-221">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="17d6d-222">Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="17d6d-222">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="17d6d-223">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="17d6d-223">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="17d6d-224">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="17d6d-224">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

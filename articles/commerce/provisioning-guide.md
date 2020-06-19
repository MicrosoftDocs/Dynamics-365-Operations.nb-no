---
title: Klargjøre et miljø for forhåndsvisning av Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du klargjør et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø.
author: psimolin
manager: annbe
ms.date: 06/02/2020
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
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426471"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="ab246-103">Klargjøre et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ab246-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ab246-104">Dette emnet forklarer hvordan du klargjør et Dynamics 365 Commerce-forhåndsvisningsmiljø.</span><span class="sxs-lookup"><span data-stu-id="ab246-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="ab246-105">Før du begynner, anbefaler vi at du tar en rask titt på dette emnet for å få en pekepinn på hva prosessen krever.</span><span class="sxs-lookup"><span data-stu-id="ab246-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="ab246-106">Hvis du ikke har fått tilgang til Dynamics 365 Commerce-forhåndsvisningen, kan du be om forhåndsvisningstilgang fra [Dynamics 365 Commerce-nettstedet](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="ab246-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="ab246-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ab246-107">Overview</span></span>

<span data-ttu-id="ab246-108">For å kunne klargjøre Commerce Preview-miljøet må du opprette et prosjekt som har et bestemt produktnavn og type.</span><span class="sxs-lookup"><span data-stu-id="ab246-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="ab246-109">Miljøet og Commerce Scale Unit (CSU) har også bestemte parametere du må bruke når du skal klargjøre e-handel senere.</span><span class="sxs-lookup"><span data-stu-id="ab246-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="ab246-110">Instruksjonene i dette emnet beskriver alle nødvendige trinn for å fullføre klargjøringen og parameterne du må bruke.</span><span class="sxs-lookup"><span data-stu-id="ab246-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="ab246-111">Når klargjøringen av Commerce-forhåndsvisningsmiljøet er fullført, er det noen få trinn du må ta i etterkant for å klargjøre det.</span><span class="sxs-lookup"><span data-stu-id="ab246-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="ab246-112">Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil evaluere.</span><span class="sxs-lookup"><span data-stu-id="ab246-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="ab246-113">Du kan alltid fullføre de valgfrie trinnene senere.</span><span class="sxs-lookup"><span data-stu-id="ab246-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="ab246-114">Hvis du vil ha informasjon om hvordan du konfigurerer Commerce-forhåndsvisningsmiljøet etter klargjøring, kan du se [Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="ab246-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="ab246-115">Hvis du vil ha informasjon om hvordan du konfigurerer valgfrie funksjoner for Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="ab246-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="ab246-116">Hvis du har spørsmål om klargjøringstrinnene eller du får problemer, kan du fortelle Microsoft i [Yammer-gruppen for Microsoft Dynamics 365 Commerce-forhåndsvisningen](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="ab246-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ab246-117">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="ab246-117">Prerequisites</span></span>

<span data-ttu-id="ab246-118">Følgende forutsetninger må være på plass før du kan klargjøre Commerce-forhåndsvisningsmiljøet:</span><span class="sxs-lookup"><span data-stu-id="ab246-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="ab246-119">Du har tilgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).</span><span class="sxs-lookup"><span data-stu-id="ab246-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="ab246-120">Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan opprette et Dynamics 365 Commerce-prosjekt.</span><span class="sxs-lookup"><span data-stu-id="ab246-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="ab246-121">Du er godtatt i Dynamics 365 Commerce-forhåndsvisningsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="ab246-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="ab246-122">Du har de nødvendige tillatelsene til å opprette et prosjekt for **Overfør, opprett løsninger og finn ut mer om**.</span><span class="sxs-lookup"><span data-stu-id="ab246-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="ab246-123">Du er medlem av **Miljøadministrator**- eller **Prosjekteier**-rollen i prosjektet der du skal klargjøre miljøet.</span><span class="sxs-lookup"><span data-stu-id="ab246-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="ab246-124">Du har administratortilgang til Microsoft Azure-abonnementet eller kontakt med en abonnementsadministrator som kan utføre de to trinnene som krever administratortillatelser på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="ab246-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="ab246-125">Du har Azure Active Directory (Azure AD) tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ab246-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="ab246-126">Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som systemadministratorgruppe for e-handel, og du har ID-en tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ab246-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="ab246-127">Du har opprettet en Azure AD-sikkerhetsgruppe som skal brukes som moderatorgruppe for vurderinger og omtaler, og du har ID-en tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ab246-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="ab246-128">(Denne sikkerhetsgruppen kan være den samme som systemadministrasjonsgruppen for e-handel.)</span><span class="sxs-lookup"><span data-stu-id="ab246-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="ab246-129">Klargjøre Commerce-forhåndsvisningsmiljøet</span><span class="sxs-lookup"><span data-stu-id="ab246-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="ab246-130">Disse prosedyrene forklarer hvordan du klargjør et Commerce-forhåndsvisningsmiljø.</span><span class="sxs-lookup"><span data-stu-id="ab246-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="ab246-131">Når du har fullført dem, vil forhåndsvisningsmiljøet for Commerce være klart for konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="ab246-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="ab246-132">Alle aktivitetene som beskrives her, skjer i LCS-portalen.</span><span class="sxs-lookup"><span data-stu-id="ab246-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab246-133">Forhåndsvisningstilgang er knyttet til LCS-kontoen og organisasjonen du angav i Commerce-forhåndsvisningsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="ab246-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="ab246-134">Du må bruke samme konto for å klargjøre Commerce-forhåndsvisningsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="ab246-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="ab246-135">Hvis du må bruke en annen LCS-konto eller leier for Commerce-forhåndsvisningsmiljøet, må du oppgi disse detaljene til Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ab246-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="ab246-136">Hvis du vil ha kontaktinformasjon, kan du se delen [Støtte for Commerce-forhåndsvisningsmiljøet](#commerce-preview-environment-support) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="ab246-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="ab246-137">Kontroller at forhåndsvisningsfunksjonene er tilgjengelige og aktivert i LCS</span><span class="sxs-lookup"><span data-stu-id="ab246-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="ab246-138">Gjør følgende for å kontrollere at forhåndsvisningsfunksjonene er tilgjengelige og aktivert i LCS.</span><span class="sxs-lookup"><span data-stu-id="ab246-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="ab246-139">Logg på [LCS-portalen](https://lcs.dynamics.com) ved hjelp av samme LCS-konto du brukte til å be om tilgang til forhåndsvisningen.</span><span class="sxs-lookup"><span data-stu-id="ab246-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="ab246-140">På LCS-startsiden ruller du helt til høyre og klikker på flisen **Administrasjon av forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="ab246-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Fanen Forhåndsversjonsstyring](./media/preview1.png)

1. <span data-ttu-id="ab246-142">Bla ned til **Private forhåndsvisningsfunksjoner**, og kontroller at følgende funksjoner er tilgjengelige og aktivert:</span><span class="sxs-lookup"><span data-stu-id="ab246-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="ab246-143">E-handelsevaluering</span><span class="sxs-lookup"><span data-stu-id="ab246-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="ab246-144">Programmiljøer for Commerce-forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="ab246-144">Commerce Preview Program Environments</span></span>

    ![Private forhåndsvisningsfunksjoner](./media/preview2.png)

1. <span data-ttu-id="ab246-146">Hvis disse funksjonene ikke vises i listen, kontakter du Microsoft og angir e-postadresse for arbeid, LCS-konto og leierinformasjon.</span><span class="sxs-lookup"><span data-stu-id="ab246-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="ab246-147">Hvis du vil ha kontaktinformasjon, kan du se delen [Støtte for Commerce-forhåndsvisningsmiljøet](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="ab246-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="ab246-148">Opprett nytt prosjekt</span><span class="sxs-lookup"><span data-stu-id="ab246-148">Create a new project</span></span>

<span data-ttu-id="ab246-149">Hvis du vil opprette et nytt prosjekt i LCS, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="ab246-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="ab246-150">På LCS-startsiden velger du plusstegnet (**+**) for å opprette et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="ab246-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="ab246-151">I den høyre ruten følger du ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="ab246-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="ab246-152">Hvis du er en partner, velger du **Overfør, opprett løsninger og finn ut mer om**.</span><span class="sxs-lookup"><span data-stu-id="ab246-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="ab246-153">Hvis du er kunde, velger du **Potensielt førsalg**.</span><span class="sxs-lookup"><span data-stu-id="ab246-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="ab246-154">Angi navn, beskrivelse og bransje.</span><span class="sxs-lookup"><span data-stu-id="ab246-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="ab246-155">I **Produktnavn**-feltet velger du **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="ab246-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="ab246-156">I **Produktversjon**-feltet velger du **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="ab246-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="ab246-157">I **Metodologi**-feltet velger du **Implementeringsmetodologi for Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="ab246-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="ab246-158">Valgfritt: Du kan importere roller og brukere fra et eksisterende prosjekt.</span><span class="sxs-lookup"><span data-stu-id="ab246-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="ab246-159">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="ab246-159">Select **Create**.</span></span> <span data-ttu-id="ab246-160">Prosjektvisningen vises.</span><span class="sxs-lookup"><span data-stu-id="ab246-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="ab246-161">Legge til Azure-koblingen</span><span class="sxs-lookup"><span data-stu-id="ab246-161">Add the Azure Connector</span></span>

<span data-ttu-id="ab246-162">Hvis du vil legge til Azure-koblingen i LCS-prosjektet, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ab246-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="ab246-163">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="ab246-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="ab246-164">Hvis du er en partner, velger du **Prosjektinnstillinger**-flisen helt til høyre.</span><span class="sxs-lookup"><span data-stu-id="ab246-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="ab246-165">Hvis du er en kunde, velger du **Prosjektinnstillinger** fra den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="ab246-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="ab246-166">Velg **Azure-koblinger**.</span><span class="sxs-lookup"><span data-stu-id="ab246-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="ab246-167">Klikk **Legg til** for å legge til Azure-koblingen.</span><span class="sxs-lookup"><span data-stu-id="ab246-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="ab246-168">Skriv inn et navn.</span><span class="sxs-lookup"><span data-stu-id="ab246-168">Enter a name.</span></span>
1. <span data-ttu-id="ab246-169">Angi ID for Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab246-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="ab246-170">Aktiver alternativet **Konfigurer til å bruke ARM (Azure Resource Manager)**.</span><span class="sxs-lookup"><span data-stu-id="ab246-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="ab246-171">Kontroller at verdien for **AAD-leierdomene (eller ID) for Azure-abonnement** er riktig.</span><span class="sxs-lookup"><span data-stu-id="ab246-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="ab246-172">Kontakt om nødvendig Azure-abonnementsadministratoren.</span><span class="sxs-lookup"><span data-stu-id="ab246-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="ab246-173">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="ab246-173">Select **Next**.</span></span>
1. <span data-ttu-id="ab246-174">Følg instruksjonene på siden for å gi de nødvendige programmene tilgang til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="ab246-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="ab246-175">Kontakt om nødvendig Azure-abonnementsadministratoren.</span><span class="sxs-lookup"><span data-stu-id="ab246-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="ab246-176">Logg på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="ab246-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="ab246-177">Kontroller at riktig katalog er valgt, og velg deretter **Abonnementer** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="ab246-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="ab246-178">Finn det riktige abonnementet fra listen, og velg det.</span><span class="sxs-lookup"><span data-stu-id="ab246-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="ab246-179">Bruk søkefunksjonaliteten etter behov.</span><span class="sxs-lookup"><span data-stu-id="ab246-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="ab246-180">Velg **Tilgangskontroll (IAM)** på menyen.</span><span class="sxs-lookup"><span data-stu-id="ab246-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="ab246-181">Klikk **Legg til** under **Legg til rolletilordning** på høyre side.</span><span class="sxs-lookup"><span data-stu-id="ab246-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="ab246-182">**Legg til rolletilordning**-ruten åpnes.</span><span class="sxs-lookup"><span data-stu-id="ab246-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="ab246-183">I **Rolle**-feltet velger du **Bidragsyter**.</span><span class="sxs-lookup"><span data-stu-id="ab246-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="ab246-184">I feltet **Tilordne tilgang til** beholder du standardverdien, **Azure AD-bruker, -gruppe eller -tjenestekontohaver.**</span><span class="sxs-lookup"><span data-stu-id="ab246-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="ab246-185">Under **Velg** angir du **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="ab246-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="ab246-186">Velg **Dynamics-distribusjonstjenester \[wsfed-aktivert\]** fra listen.</span><span class="sxs-lookup"><span data-stu-id="ab246-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="ab246-187">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ab246-187">Select **Save**.</span></span>

1. <span data-ttu-id="ab246-188">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="ab246-188">Select **Next**.</span></span>
1. <span data-ttu-id="ab246-189">Følg instruksjonene på siden for å gi de nødvendige programmene tilgang til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="ab246-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="ab246-190">Kontakt om nødvendig Azure-abonnementsadministratoren.</span><span class="sxs-lookup"><span data-stu-id="ab246-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="ab246-191">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="ab246-191">Select **Next**.</span></span>
1. <span data-ttu-id="ab246-192">I **Azure-område**-feltet velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.</span><span class="sxs-lookup"><span data-stu-id="ab246-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="ab246-193">Velg **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="ab246-193">Select **Connect**.</span></span> <span data-ttu-id="ab246-194">Din Azure-kobling skal vises i listen.</span><span class="sxs-lookup"><span data-stu-id="ab246-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="ab246-195">Importere miljøer for e-handelsforhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="ab246-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="ab246-196">Følg denne fremgangsmåten for å importere miljøer for e-handelsforhåndsvisning til prosjektet ditt.</span><span class="sxs-lookup"><span data-stu-id="ab246-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="ab246-197">Åpne startsiden for prosjektet ved å velge prosjektnavnet øverst.</span><span class="sxs-lookup"><span data-stu-id="ab246-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="ab246-198">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="ab246-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="ab246-199">Hvis du er en partner, velger du **Aktivabibliotek**-flisen helt til høyre.</span><span class="sxs-lookup"><span data-stu-id="ab246-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="ab246-200">Hvis du er en kunde, velger du **Aktivabibliotek** fra den øverste menyen.</span><span class="sxs-lookup"><span data-stu-id="ab246-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="ab246-201">Velg **Distribuerbar programvarepakke** fra listen til venstre.</span><span class="sxs-lookup"><span data-stu-id="ab246-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="ab246-202">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="ab246-202">Select **Import**.</span></span>
1. <span data-ttu-id="ab246-203">Velg **Miljøer for e-handelsforhåndsvisning** fra listen over aktiva under **Delt aktivabibliotek**.</span><span class="sxs-lookup"><span data-stu-id="ab246-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="ab246-204">Velg **Plukk**.</span><span class="sxs-lookup"><span data-stu-id="ab246-204">Select **Pick**.</span></span> <span data-ttu-id="ab246-205">Du kommer tilbake til aktivabiblioteket, og du skal se utvidelsen i listen.</span><span class="sxs-lookup"><span data-stu-id="ab246-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="ab246-206">Illustrasjonen nedenfor viser handlingene som må utføres på LCS-siden **Aktivabibliotek**.</span><span class="sxs-lookup"><span data-stu-id="ab246-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Importere miljøer for e-handelsforhåndsvisning](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="ab246-208">Distribuere miljøet</span><span class="sxs-lookup"><span data-stu-id="ab246-208">Deploy the environment</span></span>

<span data-ttu-id="ab246-209">Gjør følgende for å distribuere miljøet.</span><span class="sxs-lookup"><span data-stu-id="ab246-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="ab246-210">Det kan hende du ikke trenger å fullføre trinn 6, 7 og/eller 8 fordi sider som har et enkelt alternativ, hoppes over.</span><span class="sxs-lookup"><span data-stu-id="ab246-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="ab246-211">Når du er i **Miljøparametere**-visningen, bekrefter du at teksten **Dynamics 365 Commerce - demo (10.0.* x* med Platform update *xx*)\*\* vises rett over **Miljønavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ab246-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="ab246-212">For mer informasjon, se illustrasjonen som vises etter trinn 8.</span><span class="sxs-lookup"><span data-stu-id="ab246-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="ab246-213">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="ab246-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="ab246-214">Klikk **Legg til** for å legge til et miljø.</span><span class="sxs-lookup"><span data-stu-id="ab246-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="ab246-215">I feltet **Programversjon** velger du den nyeste versjonen.</span><span class="sxs-lookup"><span data-stu-id="ab246-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="ab246-216">Hvis du har et bestemt behov for å velge en annen programversjon enn den nyeste versjonen, må du ikke velge en tidligere versjon enn **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="ab246-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="ab246-217">I **Plattformversjon**-feltet bruker du plattformversjonen som automatisk velges for den valgte programversjonen.</span><span class="sxs-lookup"><span data-stu-id="ab246-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Velge program- og plattformversjoner](./media/project1.png)

1. <span data-ttu-id="ab246-219">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="ab246-219">Select **Next**.</span></span>
1. <span data-ttu-id="ab246-220">Velg **Demo** som miljøtopologien.</span><span class="sxs-lookup"><span data-stu-id="ab246-220">Select **Demo** as the environment topology.</span></span>

    ![Velge miljøtopologien 1](./media/project2.png)

1. <span data-ttu-id="ab246-222">Velg **Dynamics 365 Commerce - Demo** som miljøtopologien.</span><span class="sxs-lookup"><span data-stu-id="ab246-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="ab246-223">Hvis du konfigurerte en enkelt Azure-kobling tidligere, vil den bli brukt for dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="ab246-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="ab246-224">Hvis du konfigurerte flere Azure-koblinger, kan du velge hvilken kontakt som skal brukes: **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.</span><span class="sxs-lookup"><span data-stu-id="ab246-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="ab246-225">(For den beste ende-til-ende-ytelsen anbefaler vi at du velger **USA vest 2**.)</span><span class="sxs-lookup"><span data-stu-id="ab246-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Velge miljøtopologien 2](./media/project3.png)

1. <span data-ttu-id="ab246-227">På **Distribusjonsmiljø**-siden angir du et miljønavn.</span><span class="sxs-lookup"><span data-stu-id="ab246-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="ab246-228">La Avanserte innstillinger stå som de er.</span><span class="sxs-lookup"><span data-stu-id="ab246-228">Leave the advanced settings as they are.</span></span>

    ![Distribusjonsmiljø-siden](./media/project4.png)

1. <span data-ttu-id="ab246-230">Juster VM-størrelsen etter behov.</span><span class="sxs-lookup"><span data-stu-id="ab246-230">Adjust the VM size as required.</span></span> <span data-ttu-id="ab246-231">(Vi anbefaler VM-lagerenhet \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="ab246-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="ab246-232">Se gjennom vilkårene for prising og lisensiering, og merk deretter av i avmerkingsboksen for å angi at du godtar dem.</span><span class="sxs-lookup"><span data-stu-id="ab246-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="ab246-233">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="ab246-233">Select **Next**.</span></span>
1. <span data-ttu-id="ab246-234">Klikk **Distribuer**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige.</span><span class="sxs-lookup"><span data-stu-id="ab246-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="ab246-235">Du kommer tilbake til visningen **Skybaserte miljøer**, og miljøet skal vises i listen.</span><span class="sxs-lookup"><span data-stu-id="ab246-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="ab246-236">Det forespurte miljøet vil vises som en kø og deretter distribueres.</span><span class="sxs-lookup"><span data-stu-id="ab246-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="ab246-237">Miljøarbeidsflytene vil ta litt tid å fullføre.</span><span class="sxs-lookup"><span data-stu-id="ab246-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="ab246-238">Kom derfor tilbake etter ca seks til ni timer.</span><span class="sxs-lookup"><span data-stu-id="ab246-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="ab246-239">Før du fortsetter må du kontrollere at miljøstatusen er **Distribuert**.</span><span class="sxs-lookup"><span data-stu-id="ab246-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="ab246-240">Initialisere Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="ab246-240">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="ab246-241">Hvis du vil initialisere en CSU-adresse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="ab246-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="ab246-242">Velg miljøet ditt fra listen i visningen **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="ab246-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="ab246-243">Klikk **Detaljerte opplysninger** i miljøvisningen til høyre.</span><span class="sxs-lookup"><span data-stu-id="ab246-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="ab246-244">Detaljerte opplysninger for miljø vises.</span><span class="sxs-lookup"><span data-stu-id="ab246-244">The environment details view appears.</span></span>
1. <span data-ttu-id="ab246-245">Klikk **Behandle** under **Miljøfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="ab246-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="ab246-246">Velg **Initialiser** i kategorien **Handel**.</span><span class="sxs-lookup"><span data-stu-id="ab246-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="ab246-247">Visningen av parametere for CSU-initialisering vises.</span><span class="sxs-lookup"><span data-stu-id="ab246-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="ab246-248">I **Område**-feltet velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.</span><span class="sxs-lookup"><span data-stu-id="ab246-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="ab246-249">I **Versjon**-feltet velger du **Angi en versjon** i listen, og deretter angir du **9.18.20014.4** i feltet som vises.</span><span class="sxs-lookup"><span data-stu-id="ab246-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="ab246-250">Pass på at du angir nøyaktig hvilken versjon som er angitt her.</span><span class="sxs-lookup"><span data-stu-id="ab246-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="ab246-251">Ellers må du oppdatere RCSU til korrekt versjon senere.</span><span class="sxs-lookup"><span data-stu-id="ab246-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="ab246-252">Aktiver alternativet **Bruk utvidelse**.</span><span class="sxs-lookup"><span data-stu-id="ab246-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="ab246-253">Velg **Miljøer for e-handelsforhåndsvisning** fra listen over utvidelser.</span><span class="sxs-lookup"><span data-stu-id="ab246-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="ab246-254">Velg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="ab246-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="ab246-255">Klikk **Ja**på bekreftelsessiden for distribusjon når du har bekreftet at detaljene er riktige.</span><span class="sxs-lookup"><span data-stu-id="ab246-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="ab246-256">Visningen **Handelsadministrasjon** vises på nytt med kategorien **Handel** valgt.</span><span class="sxs-lookup"><span data-stu-id="ab246-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="ab246-257">CSU-en din er lagt i kø for klargjøring.</span><span class="sxs-lookup"><span data-stu-id="ab246-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="ab246-258">Før du fortsetter må du kontrollere at miljøstatusen til CSU er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="ab246-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="ab246-259">Initialiseringen tar omtrent to til fem timer.</span><span class="sxs-lookup"><span data-stu-id="ab246-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="ab246-260">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="ab246-260">Initialize e-Commerce</span></span>

<span data-ttu-id="ab246-261">Hvis du vil initialisere e-handel, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="ab246-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ab246-262">I kategorien **E-handel** ser du gjennom samtykket for forhåndsvisning, og velger deretter **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="ab246-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="ab246-263">Angi et navn i feltet **Navn på e-handelsleier**.</span><span class="sxs-lookup"><span data-stu-id="ab246-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="ab246-264">Vær imidlertid oppmerksom på at dette navnet vil vises i noen av URL-adressene som peker til e-handelsforekomsten.</span><span class="sxs-lookup"><span data-stu-id="ab246-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="ab246-265">I feltet **Commerce Scale Unit-navn** velger du CSU-en i listen.</span><span class="sxs-lookup"><span data-stu-id="ab246-265">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="ab246-266">(Listen bør bare ha ett alternativ.)</span><span class="sxs-lookup"><span data-stu-id="ab246-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="ab246-267">Feltet **Geografi for e-handel** angis automatisk, og verdien kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="ab246-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="ab246-268">Klikk **Neste** for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="ab246-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="ab246-269">I feltet **Støttede vertsnavn** angir du et gyldig domene, for eksempel `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="ab246-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="ab246-270">I feltet **AAD sikkerhetsgruppe for systemadministrasjon** angir du de første bokstavene i navnet på sikkerhetsgruppen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="ab246-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="ab246-271">Velg forstørrelsesglass-ikonet for å vise søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="ab246-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="ab246-272">Velg riktig sikkerhetsgruppe fra listen.</span><span class="sxs-lookup"><span data-stu-id="ab246-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="ab246-273">I feltet **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir du de første bokstavene i navnet på sikkerhetsgruppen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="ab246-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="ab246-274">Velg forstørrelsesglass-ikonet for å vise søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="ab246-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="ab246-275">Velg riktig sikkerhetsgruppe fra listen.</span><span class="sxs-lookup"><span data-stu-id="ab246-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="ab246-276">La alternativet **Aktiver tjenesten for vurderinger og omtale** være aktivert.</span><span class="sxs-lookup"><span data-stu-id="ab246-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="ab246-277">Velg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="ab246-277">Select **Initialize**.</span></span> <span data-ttu-id="ab246-278">Visningen **Handelsadministrasjon** vises på nytt med kategorien **E-handel** valgt.</span><span class="sxs-lookup"><span data-stu-id="ab246-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="ab246-279">Initialiseringen av e-handel har startet.</span><span class="sxs-lookup"><span data-stu-id="ab246-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="ab246-280">Før du fortsetter må du vente til initialiseringsstatusen for e-handel er **Initialisering vellykket**.</span><span class="sxs-lookup"><span data-stu-id="ab246-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="ab246-281">Under **Koblinger** ned til høyre noterer du URL-adressene for følgende koblinger:</span><span class="sxs-lookup"><span data-stu-id="ab246-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="ab246-282">**E-handelsområde** – koblingen til roten for e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="ab246-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="ab246-283">**Verktøy for administrasjon av e-handel-området** – koblingen til verktøyet for områdeadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="ab246-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="ab246-284">Støtte for Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="ab246-284">Commerce preview environment support</span></span>

<span data-ttu-id="ab246-285">Hvis det oppstår problemer under utføring av klargjøringstrinnene, kan du gå til [Yammer-gruppen for Microsoft Dynamics 365 Commerce forhåndsvisning](https://aka.ms/Dynamics365CommercePreviewYammer) for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="ab246-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ab246-286">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="ab246-286">Next steps</span></span>

<span data-ttu-id="ab246-287">Hvis du vil fortsette prosessen for å klargjøre og konfigurere Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere et Commerce-forhåndsvisningsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="ab246-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab246-288">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ab246-288">Additional resources</span></span>

[<span data-ttu-id="ab246-289">Oversikt over miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ab246-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ab246-290">Konfigurere et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ab246-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="ab246-291">Konfigurere valgfrie funksjoner for et miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ab246-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="ab246-292">Vanlige spørsmål om miljø for forhåndsvisning av Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ab246-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ab246-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ab246-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ab246-294">Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="ab246-294">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ab246-295">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="ab246-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ab246-296">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="ab246-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


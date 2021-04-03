---
title: Definere en B2C-leier i Commerce
description: Dette emnet beskriver hvordan du konfigurerer Azure Active Directory (Azure AD) bedrift-til-kunde (B2C)-leietakere for godkjenning av brukerområde i Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ee667bb49e70e0c881a2db1248b3f0c7fc017ce
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478146"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="65e7f-103">Definere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="65e7f-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65e7f-104">Dette emnet beskriver hvordan du konfigurerer Azure Active Directory (Azure AD) bedrift-til-kunde (B2C)-leietakere for godkjenning av brukerområde i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="65e7f-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="65e7f-105">Dynamics 365 Commerce bruker Azure AD B2C til å støtte brukerlegitimasjon og godkjenningsflyt.</span><span class="sxs-lookup"><span data-stu-id="65e7f-105">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="65e7f-106">En bruker kan registrere seg, logge inn og tilbakestille passordet ved hjelp av disse flytene.</span><span class="sxs-lookup"><span data-stu-id="65e7f-106">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="65e7f-107">Azure AD B2C lagrer sensitiv brukergodkjenningsinformasjon, for eksempel brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="65e7f-107">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="65e7f-108">Brukerposten i B2C-leieren vil lagre enten en B2C-post for lokal forretningsforbindelse eller en B2C-post for sosial identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="65e7f-108">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="65e7f-109">Disse B2C-postene vil koble tilbake til kundeoppføringen i Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-109">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="65e7f-110">Opprett eller koble til en eksisterende AAD B2C-leier i Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="65e7f-110">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="65e7f-111">Logg på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="65e7f-111">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="65e7f-112">Velg **Opprett en ressurs** fra menyen for Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="65e7f-112">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="65e7f-113">Pass på at du bruker abonnementet og katalogen som skal kobles til Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-113">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Opprette en ressurs i Azure-portalen](./media/B2CImage_1.png)

1. <span data-ttu-id="65e7f-115">Gå til **Identitet \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-115">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="65e7f-116">På siden **Opprett ny B2C-leier eller koble til en eksisterende leier** bruker du et av alternativene nedenfor som passer best til firmaets behov:</span><span class="sxs-lookup"><span data-stu-id="65e7f-116">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="65e7f-117">**Opprett en ny Azure AD B2C-leier**: Bruk dette alternativet til å opprette en ny AAD B2C-leier.</span><span class="sxs-lookup"><span data-stu-id="65e7f-117">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="65e7f-118">Velg **Opprett en ny Azure AD B2C-leier**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-118">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="65e7f-119">Under **Organisasjonsnavn** angir du organisasjonsnavnet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-119">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="65e7f-120">Skriv inn det opprinnelige domenenavnet under **Opprinnelig domenenavn**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-120">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="65e7f-121">For **Land eller område** velger du aktuelt land eller område.</span><span class="sxs-lookup"><span data-stu-id="65e7f-121">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="65e7f-122">Velg **Opprett** for å opprette leieren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-122">Select **Create** to create the tenant.</span></span>

     ![Opprette en ny Azure AD-leier](./media/B2CImage_2.png)

     - <span data-ttu-id="65e7f-124">**Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet**: Bruk dette alternativet hvis du allerede har en Azure AD B2C-leier du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="65e7f-124">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="65e7f-125">Velg **Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-125">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="65e7f-126">For **Azure AD B2C-leier** velger du den riktige B2C-leieren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-126">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="65e7f-127">Hvis det vises en melding i valgboksen om at det ikke ble funnet noen kvalifiserte B2C-leiere, har du ikke en eksisterende kvalifisert B2C-leier, og må opprette en ny.</span><span class="sxs-lookup"><span data-stu-id="65e7f-127">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="65e7f-128">For **Ressursgruppe** velger du **Opprett ny**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-128">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="65e7f-129">Angi et **navn** på ressursgruppen som skal inneholde leieren, velg **ressursgruppelokasjonen**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-129">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet](./media/B2CImage_3.png)

1. <span data-ttu-id="65e7f-131">Når den nye Azure AD B2C-katalogen er opprettet (dette kan ta litt tid), vil det vises en kobling til den nye katalogen på instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-131">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="65e7f-132">Denne koblingen fører deg til siden "Velkommen til Azure Active Directory B2C".</span><span class="sxs-lookup"><span data-stu-id="65e7f-132">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Kobling til ny AAD-katalog](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="65e7f-134">Hvis du har flere abonnementer i Azure-kontoen eller har konfigurert B2C-leieren uten å koble til et aktivt abonnement, vil et **Feilsøking**-banner gi deg beskjed om å koble leieren til et abonnement.</span><span class="sxs-lookup"><span data-stu-id="65e7f-134">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="65e7f-135">Velg feilsøkingsmeldingen, og følg instruksjonene for å løse problemet med abonnement.</span><span class="sxs-lookup"><span data-stu-id="65e7f-135">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="65e7f-136">Bildet nedenfor viser et eksempel på et Azure AD B2C **Feilsøking**-banner.</span><span class="sxs-lookup"><span data-stu-id="65e7f-136">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Advarsel som viser at katalogen ikke har et aktivt abonnement](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="65e7f-138">Opprette B2C-programmet</span><span class="sxs-lookup"><span data-stu-id="65e7f-138">Create the B2C application</span></span>

<span data-ttu-id="65e7f-139">Når B2C-leieren er opprettet, oppretter du et B2C-program i leieren for å samhandle med Commerce-handlingene.</span><span class="sxs-lookup"><span data-stu-id="65e7f-139">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="65e7f-140">Hvis du vil opprette B2C-programmet, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="65e7f-140">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-141">Velg **Programmer (eldre)** i Azure-portalen, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-141">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="65e7f-142">Under **Navn** angir du navnet på det ønskede AAD B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-142">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="65e7f-143">Under **Webapp/Web-API** for **Inkluder webapp / web-API** velger du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-143">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="65e7f-144">For **Tillat implisitt flyt** velger du **Ja** (standardverdien).</span><span class="sxs-lookup"><span data-stu-id="65e7f-144">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="65e7f-145">Under **Svar-URL** angir du de dedikerte svar-URL-adressene.</span><span class="sxs-lookup"><span data-stu-id="65e7f-145">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="65e7f-146">Se [URL-adresser for svar](#reply-urls) nedenfor for informasjon om URL-adresser for svar, og hvordan du kan formatere dem her.</span><span class="sxs-lookup"><span data-stu-id="65e7f-146">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="65e7f-147">Velg **Nei** for **Inkluder opprinnelig klient** (standardverdi).</span><span class="sxs-lookup"><span data-stu-id="65e7f-147">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="65e7f-148">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-148">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="65e7f-149">URL-adresser for svar</span><span class="sxs-lookup"><span data-stu-id="65e7f-149">Reply URLs</span></span>

<span data-ttu-id="65e7f-150">Svar-URL-adresser er viktige, fordi de gir en tillatelsesliste for returdomener når området kaller Azure AD B2C for å godkjenne en bruker.</span><span class="sxs-lookup"><span data-stu-id="65e7f-150">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="65e7f-151">Dette tillater retur av den godkjente brukeren til domenet de logger seg på fra (områdedomenet).</span><span class="sxs-lookup"><span data-stu-id="65e7f-151">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="65e7f-152">I boksen **Svar-URL** på skjermen **Azure AD B2C-programmer \> Nytt program** må du legge til separate linjer for både områdedomet og (når miljøet er klargjort) den Commerce-genererte URL-en.</span><span class="sxs-lookup"><span data-stu-id="65e7f-152">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="65e7f-153">Disse URL-adressene må alltid bruke et gyldig URL-format og må være basis-URLer (ingen etterfølgende skråstreker eller baner).</span><span class="sxs-lookup"><span data-stu-id="65e7f-153">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="65e7f-154">Strengen ``/_msdyn365/authresp`` må deretter legges til de primære URL-adressene, som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="65e7f-154">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="65e7f-155">``https://www.fabrikam.com/_msdyn365/authresp`` (Domenet skal samsvare med hele e-handelsdomenet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-155">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="65e7f-156">Hvis du har flere domener, må du legge til denne URL-adressen for hvert domene.)</span><span class="sxs-lookup"><span data-stu-id="65e7f-156">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="65e7f-157">Opprette brukerflytpolicyer</span><span class="sxs-lookup"><span data-stu-id="65e7f-157">Create user flow policies</span></span>

<span data-ttu-id="65e7f-158">Brukerflyter er policyene som Azure AD B2C bruker for å gi sikker pålogging, registrering, redigering av profil og brukeopplevelser ved glemt passord.</span><span class="sxs-lookup"><span data-stu-id="65e7f-158">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="65e7f-159">Dynamics 365 Commerce bruker disse flytene til å utføre policyhandlinger for å kommunisere med Azure AD B2C-leieren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-159">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="65e7f-160">Når en bruker samhandler med disse policyene, omdirigeres de til Azure AD B2C-leieren for å utføre handlingene.</span><span class="sxs-lookup"><span data-stu-id="65e7f-160">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="65e7f-161">Azure AD B2C gir tre enkle flyttyper for brukere:</span><span class="sxs-lookup"><span data-stu-id="65e7f-161">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="65e7f-162">Registrering og pålogging</span><span class="sxs-lookup"><span data-stu-id="65e7f-162">Sign up and sign in</span></span>
- <span data-ttu-id="65e7f-163">Profilredigering</span><span class="sxs-lookup"><span data-stu-id="65e7f-163">Profile editing</span></span>
- <span data-ttu-id="65e7f-164">Tilbakestill passord</span><span class="sxs-lookup"><span data-stu-id="65e7f-164">Password reset</span></span>

<span data-ttu-id="65e7f-165">Du kan velge å bruke standard brukerflyter i Azure AD, som vil vise en side som ligger på AAD-B2C.</span><span class="sxs-lookup"><span data-stu-id="65e7f-165">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="65e7f-166">Du kan også opprette en HTML-side for å kontrollere utseendet og funksjonaliteten til brukerflytopplevelsene.</span><span class="sxs-lookup"><span data-stu-id="65e7f-166">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="65e7f-167">Hvis du vil tilpasse brukerpolicysidene for Dynamics 365 Commerce, kan du se [Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="65e7f-167">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="65e7f-168">Hvis du vil ha mer informasjon, se [Tilpasse grensesnittet til brukeropplevelser i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="65e7f-168">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="65e7f-169">Opprette en brukerflytpolicy for registrering og pålogging</span><span class="sxs-lookup"><span data-stu-id="65e7f-169">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="65e7f-170">Følg denne fremgangsmåten for å opprette en brukerflytpolicy for registrering og pålogging.</span><span class="sxs-lookup"><span data-stu-id="65e7f-170">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-171">Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-171">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="65e7f-172">På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-172">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="65e7f-173">Velg **Registrering og pålogging** i fanen **Anbefalt**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-173">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="65e7f-174">Under **Navn** skriver du inn et policynavn.</span><span class="sxs-lookup"><span data-stu-id="65e7f-174">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="65e7f-175">Dette navnet vil vises etterpå med et prefiks som portalen tilordner (for eksempel "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="65e7f-175">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="65e7f-176">Under **Identitetsleverandører** merker du av for den aktuelle avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-176">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="65e7f-177">Velg ønsket valg for firmaet under **Godkjenning med flere faktorer**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-177">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="65e7f-178">Under **Brukerattributter og krav** velger du alternativer for å samle attributter eller returkrav etter behov.</span><span class="sxs-lookup"><span data-stu-id="65e7f-178">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="65e7f-179">Commerce krever følgende standard alternativer:</span><span class="sxs-lookup"><span data-stu-id="65e7f-179">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="65e7f-180">**Innhent attributt**</span><span class="sxs-lookup"><span data-stu-id="65e7f-180">**Collect  attribute**</span></span> | <span data-ttu-id="65e7f-181">**Returkrav**</span><span class="sxs-lookup"><span data-stu-id="65e7f-181">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="65e7f-182">E-postadresse</span><span class="sxs-lookup"><span data-stu-id="65e7f-182">Email Address</span></span>          | <span data-ttu-id="65e7f-183">E-postadresser</span><span class="sxs-lookup"><span data-stu-id="65e7f-183">Email Addresses</span></span>   |
    | <span data-ttu-id="65e7f-184">Gitt navn</span><span class="sxs-lookup"><span data-stu-id="65e7f-184">Given Name</span></span>             | <span data-ttu-id="65e7f-185">Gitt navn</span><span class="sxs-lookup"><span data-stu-id="65e7f-185">Given Name</span></span>        |
    |                        | <span data-ttu-id="65e7f-186">Identitetsleverandør</span><span class="sxs-lookup"><span data-stu-id="65e7f-186">Identity Provider</span></span> |
    | <span data-ttu-id="65e7f-187">Etternavn</span><span class="sxs-lookup"><span data-stu-id="65e7f-187">Surname</span></span>                | <span data-ttu-id="65e7f-188">Etternavn</span><span class="sxs-lookup"><span data-stu-id="65e7f-188">Surname</span></span>           |
    |                        | <span data-ttu-id="65e7f-189">Brukers objekt-ID</span><span class="sxs-lookup"><span data-stu-id="65e7f-189">User’s Object ID</span></span>  |

1. <span data-ttu-id="65e7f-190">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-190">Select **Create**.</span></span>

<span data-ttu-id="65e7f-191">Bildet nedenfor er et eksempel på brukerflyt for Azure AD B2C registrering og pålogging.</span><span class="sxs-lookup"><span data-stu-id="65e7f-191">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Policyinnstillinger for registrering og pålogging](./media/B2CImage_11.png)

<span data-ttu-id="65e7f-193">Bildet nedenfor viser alternativet **Kjør brukerflyt** i brukerflyten Azure AD B2C registering og pålogging.</span><span class="sxs-lookup"><span data-stu-id="65e7f-193">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Kjør brukerflyt-alternativet policyflyt](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="65e7f-195">Opprette en brukerflytpolicy for profilredigering</span><span class="sxs-lookup"><span data-stu-id="65e7f-195">Create a profile editing user flow policy</span></span>

<span data-ttu-id="65e7f-196">Følg denne fremgangsmåten for å opprette en brukerflytpolicy for profilredigering.</span><span class="sxs-lookup"><span data-stu-id="65e7f-196">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-197">Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-197">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="65e7f-198">På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-198">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="65e7f-199">Velg **Profilredigering** i fanen **Anbefalt**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-199">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="65e7f-200">Under **Navn** angir du brukerflyten for profilredigering.</span><span class="sxs-lookup"><span data-stu-id="65e7f-200">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="65e7f-201">Dette navnet vil vises etterpå med et prefiks som portalen tilordner (for eksempel "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="65e7f-201">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="65e7f-202">Under **Identitetsleverandører** velger du **Logg på lokal konto**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-202">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="65e7f-203">Under **Brukerattributter** merker du av følgende avmerkingsbokser:</span><span class="sxs-lookup"><span data-stu-id="65e7f-203">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="65e7f-204">**E-postadresser** (bare **Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="65e7f-204">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="65e7f-205">**Gitt navn** (**Innhent attributt** og **Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="65e7f-205">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="65e7f-206">**Identitetsleverandør** (bare **Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="65e7f-206">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="65e7f-207">**Etternavn** (**Innhent attributt** og **Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="65e7f-207">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="65e7f-208">**Brukers objekt-ID** (**bare Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="65e7f-208">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="65e7f-209">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-209">Select **Create**.</span></span>

<span data-ttu-id="65e7f-210">Det følgende bildet viser et eksempel på brukerflyten for Azure AD B2C-profilredigering.</span><span class="sxs-lookup"><span data-stu-id="65e7f-210">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Opprette brukerflyten for profilredigering](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="65e7f-212">Opprette en brukerflytpolicy for tilbakestilling av passord</span><span class="sxs-lookup"><span data-stu-id="65e7f-212">Create a password reset user flow policy</span></span>

<span data-ttu-id="65e7f-213">Følg denne fremgangsmåten for å opprette en brukerflytpolicy for tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="65e7f-213">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-214">Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-214">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="65e7f-215">På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-215">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="65e7f-216">Velg **Tilbakestill passord** i fanen **Anbefalt**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-216">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="65e7f-217">Under **Navn** skriver du inn et navn på brukerflyten for tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="65e7f-217">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="65e7f-218">Under **Identitetsleverandører** velger du **Tilbakestill passord ved hjelp av e-postadresse**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-218">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="65e7f-219">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-219">Select **Create**.</span></span>
1. <span data-ttu-id="65e7f-220">Under **Programkrav** merker du av følgende avmerkingsbokser:</span><span class="sxs-lookup"><span data-stu-id="65e7f-220">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="65e7f-221">**E-postadresser**</span><span class="sxs-lookup"><span data-stu-id="65e7f-221">**Email addresses**</span></span>
    - <span data-ttu-id="65e7f-222">**Gitt navn**</span><span class="sxs-lookup"><span data-stu-id="65e7f-222">**Given Name**</span></span>
    - <span data-ttu-id="65e7f-223">**Etternavn**</span><span class="sxs-lookup"><span data-stu-id="65e7f-223">**Surname**</span></span>
    - <span data-ttu-id="65e7f-224">**Brukers objekt-ID**</span><span class="sxs-lookup"><span data-stu-id="65e7f-224">**User's Object ID**</span></span>
1. <span data-ttu-id="65e7f-225">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-225">Select **Create**.</span></span>

<span data-ttu-id="65e7f-226">Det følgende bildet viser hvor du kan angi at **passordet skal tilbakestilles ved å bruke e-postadresse** i brukerflyten for tilbakestilling av passord i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="65e7f-226">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Angi Tilbakestill passord med e-postadresse i policy for tilbakestilling av passord](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="65e7f-228">Legg til leverandører av sosiale identiteter (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="65e7f-228">Add social identity providers (Optional)</span></span>

<span data-ttu-id="65e7f-229">Leverandører av sosiale identiteter gjør det mulig for brukere å bruke sine sosiale kontoer for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="65e7f-229">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="65e7f-230">Det er valgfritt å legge til leverandør for godkjenning av sosiale identiteter i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="65e7f-230">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="65e7f-231">Hvis godkjenning av sosial identitetsleverandør ikke er lagt til, vil standard Azure AD B2C-profiler være hovedprofilene til brukerbasen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-231">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="65e7f-232">Brukerne velger sine egne brukernavn (foretrukket e-postadresse) og angir et passord.</span><span class="sxs-lookup"><span data-stu-id="65e7f-232">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="65e7f-233">Azure AD B2C vil godkjenne brukere direkte.</span><span class="sxs-lookup"><span data-stu-id="65e7f-233">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="65e7f-234">Hvis godkjenning av sosial identitetsleverandør er lagt til og en bruker velger en av de tilbudte sosiale identitetsleverandørene, opprettes fremdeles en enhet i Azure AD B2C-leieren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-234">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="65e7f-235">Azure AD B2C vil deretter godkjenne brukerens legitimasjonsbeskrivelser med den sosiale identitetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-235">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="65e7f-236">Påloggingen av identitetsleverandøren oppretter en post i B2C-leieren, men i et annet format enn lokale kontoer, ettersom den kaller den eksterne referansen for sosial identitetsleverandør for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="65e7f-236">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="65e7f-237">Brukeren kan bruke samme e-postadresse på tvers av sosiale identitetsleverandører, som betyr at e-postbrukernavnet som brukes til godkjenning, ikke kan være unikt for leieren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-237">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="65e7f-238">Azure AD B2C vil bare sørge for at brukere har en unik e-postadresse på lokale B2C-kontoer.</span><span class="sxs-lookup"><span data-stu-id="65e7f-238">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="65e7f-239">Før du kan legge til en sosial identitetsleverandør for godkjenning, må du gå til identitetsleverandørens portal og konfigurere et identitetsleverandørprogram som beskrevet i Azure AD i B2C-dokumentasjonen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-239">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="65e7f-240">Nedenfor finner du en liste over koblinger til dokumentasjonen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-240">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="65e7f-241">Amazon</span><span class="sxs-lookup"><span data-stu-id="65e7f-241">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="65e7f-242">Azure AD (Én leier)</span><span class="sxs-lookup"><span data-stu-id="65e7f-242">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="65e7f-243">Microsoft-konto</span><span class="sxs-lookup"><span data-stu-id="65e7f-243">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="65e7f-244">Facebook</span><span class="sxs-lookup"><span data-stu-id="65e7f-244">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="65e7f-245">GitHub</span><span class="sxs-lookup"><span data-stu-id="65e7f-245">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="65e7f-246">Google</span><span class="sxs-lookup"><span data-stu-id="65e7f-246">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="65e7f-247">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="65e7f-247">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="65e7f-248">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="65e7f-248">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="65e7f-249">Twitter</span><span class="sxs-lookup"><span data-stu-id="65e7f-249">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="65e7f-250">Legge til og konfigurere en leverandør av sosiale identiteter</span><span class="sxs-lookup"><span data-stu-id="65e7f-250">Add and set up a social identity provider</span></span>

<span data-ttu-id="65e7f-251">Følg denne fremgangsmåten for å legge til og konfigurere en leverandør av sosiale identiteter.</span><span class="sxs-lookup"><span data-stu-id="65e7f-251">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="65e7f-252">I Azure-portalen går du til **Identitetsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-252">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="65e7f-253">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-253">Select **Add**.</span></span> <span data-ttu-id="65e7f-254">Skjermbildet **Legg til identitetsleverandør** vises.</span><span class="sxs-lookup"><span data-stu-id="65e7f-254">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="65e7f-255">Under **Navn** skriver du inn navnet som skal vises for brukere på påloggingsskjermen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-255">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="65e7f-256">Under **Type identitetsleverandør** velger du en identitetsleverandør fra listen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-256">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="65e7f-257">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-257">Select **OK**.</span></span>
1. <span data-ttu-id="65e7f-258">Velg **Konfigurer denne identitetsleverandøren** for å få tilgang til skjermbildet for **oppsett av sosial identitetsleverandør** .</span><span class="sxs-lookup"><span data-stu-id="65e7f-258">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="65e7f-259">Under **Klient-ID** angir du klient-IDen som hentes fra oppsettet for identitetsleverandørprogram.</span><span class="sxs-lookup"><span data-stu-id="65e7f-259">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="65e7f-260">Under **Klienthemmelighet** angir du klienthemmeligheten som hentes fra oppsettet for identitetsleverandørprogram.</span><span class="sxs-lookup"><span data-stu-id="65e7f-260">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="65e7f-261">Tilknytt brukerflyt for policyer for pålogging/registrering:</span><span class="sxs-lookup"><span data-stu-id="65e7f-261">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="65e7f-262">Gå til **Azure AD B2C – brukerflyter (policyer) \> {policyen for pålogging/registrering} \> Identitetsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-262">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="65e7f-263">Hvis du vil tilknytte brukerflytpolicyen for pålogging/registrering, velger du hver identitetsleverandør du har angitt for kontoen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-263">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="65e7f-264">Hvis du vil teste disse, velger du **Kjør brukerflyt** for hver identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="65e7f-264">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="65e7f-265">En ny kategori viser påloggingssiden som viser den nye valgboksen for identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="65e7f-265">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="65e7f-266">Følgende bilde viser eksempler på skjermbildene **Legg til identitetsleverandør** og **Konfigurere sosial identitetsleverandør** i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="65e7f-266">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Legge til en leverandør av sosiale identiteter i programmet](./media/B2CImage_14.png)

<span data-ttu-id="65e7f-268">Det følgende bildet viser et eksempel på hvordan du kan velge identitetsleverandører på siden Azure AD B2C **identitetsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-268">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Velg hver sosial identitetsleverandør du vil aktivere for policyen](./media/B2CImage_16.png)

<span data-ttu-id="65e7f-270">Bildet nedenfor viser et eksempel på et standard påloggingsskjermbilde med en påloggingsknapp for sosial identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="65e7f-270">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Eksempel på standard påloggingsskjerm med påloggingsknappen for sosial identitetsleverandør](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="65e7f-272">Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen</span><span class="sxs-lookup"><span data-stu-id="65e7f-272">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="65e7f-273">Når Azure AD B2C-klargjøringstrinnene ovenfor er fullført, må Azure AD B2C-programmet registreres i Dynamics 365 Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-273">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="65e7f-274">Følg denne fremgangsmåten for å oppdatere Headquarters med den nye Azure AD B2C-informasjonen:</span><span class="sxs-lookup"><span data-stu-id="65e7f-274">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-275">I Commerce går du til **Delte handelsparametere** og velger **Identitetsleverandører** på den venstre menyen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-275">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="65e7f-276">Under **Identitetsleverandører** gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="65e7f-276">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="65e7f-277">I **Utsteder**-boksen angir du URL-adressen til utstederen av identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="65e7f-277">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="65e7f-278">Du finner utstederens URL-adresse ved å se [Hent utsteders URL-adresse](#obtain-issuer-url) nedenfor.</span><span class="sxs-lookup"><span data-stu-id="65e7f-278">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="65e7f-279">I **Navn**-boksen angir du et navn på utstederposten.</span><span class="sxs-lookup"><span data-stu-id="65e7f-279">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="65e7f-280">I **Type**-boksen angir du **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-280">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="65e7f-281">Gjør følgende med ovenstående element for B2C-identitetsleverandør valgt under **Beroende parter**:</span><span class="sxs-lookup"><span data-stu-id="65e7f-281">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="65e7f-282">I **Klient-ID**-boksen skriver du inn B2C-program-IDen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-282">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="65e7f-283">Du finner dette i **Program-ID**-boksen på egenskapssiden for B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-283">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="65e7f-284">I **Type**-boksen angir du **Offentlig**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-284">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="65e7f-285">I **Brukertype**-boksen angir du **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-285">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="65e7f-286">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="65e7f-286">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="65e7f-287">I Commerce-søkeboksen søker du etter **Distribusjonsplan**</span><span class="sxs-lookup"><span data-stu-id="65e7f-287">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="65e7f-288">I den venstre navigasjonsmenyen på siden **Distribusjonsplaner** velger du jobben **1110 Global konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-288">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="65e7f-289">Velg **Kjør nå** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="65e7f-289">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="65e7f-290">Hente utsteders URL-adresse</span><span class="sxs-lookup"><span data-stu-id="65e7f-290">Obtain issuer URL</span></span>

<span data-ttu-id="65e7f-291">Følg denne fremgangsmåten for å hente URL-adressen for utsteder av identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="65e7f-291">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-292">Opprett en URL-adresse for metadata i følgende format ved hjelp av B2C-leieren og-policyen: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="65e7f-292">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="65e7f-293">Eksempel: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="65e7f-293">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="65e7f-294">Angi URL-adressen for metadata på adresselinjen i en leser.</span><span class="sxs-lookup"><span data-stu-id="65e7f-294">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="65e7f-295">I metadataene kopierer du URL-adressen for utsteder av identitetsleverandør (verdien for **"utsteder"**).</span><span class="sxs-lookup"><span data-stu-id="65e7f-295">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="65e7f-296">Eksempel: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="65e7f-296">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="65e7f-297">Konfigurere B2C-leieren i områdebygger for Commerce</span><span class="sxs-lookup"><span data-stu-id="65e7f-297">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="65e7f-298">Når installasjonen av Azure AD B2C-leieren er fullført, må du konfigurere B2C-leieren i områdebyggeren for Commerce.</span><span class="sxs-lookup"><span data-stu-id="65e7f-298">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="65e7f-299">Ved hjelp av konfigurasjonstrinnene kan du samle inn B2C-programinformasjon fra Azure-portalen, angi B2C-programinformasjon i områdebyggeren, og deretter knytte B2C-programmet til området og kanalen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-299">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="65e7f-300">Samle inn nødvendig programinformasjon</span><span class="sxs-lookup"><span data-stu-id="65e7f-300">Collect the required application information</span></span>

<span data-ttu-id="65e7f-301">Følg denne fremgangsmåten for å samle inn nødvendig programinformasjon.</span><span class="sxs-lookup"><span data-stu-id="65e7f-301">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-302">I Azure-portalen går du til **Hjem \> Azure AD B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-302">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="65e7f-303">Velg programmet, og velg deretter **Egenskaper** i navigasjonsruten til venstre for å hente programdetaljene.</span><span class="sxs-lookup"><span data-stu-id="65e7f-303">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="65e7f-304">I **Program-ID**-boksen samler du inn program-IDen til B2C-programmet som ble opprettet i B2C-leieren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-304">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="65e7f-305">Dette vil senere angis som **Klient-GUID** i områdebygger.</span><span class="sxs-lookup"><span data-stu-id="65e7f-305">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="65e7f-306">Under **Svar-URL** samler du inn URL-adressen for svar.</span><span class="sxs-lookup"><span data-stu-id="65e7f-306">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="65e7f-307">Gå til **Hjem \> Azure AD B2C – brukerflyter (policyer)**, og hent deretter navnene på hver brukerflytpolicy.</span><span class="sxs-lookup"><span data-stu-id="65e7f-307">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="65e7f-308">Bildet nedenfor viser et eksempel på siden **Azure AD B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-308">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Gå til B2C-programmet i leieren](./media/B2CImage_19.png)

<span data-ttu-id="65e7f-310">Bildet nedenfor viser et eksempel på et programs **Egenskaper**-side i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="65e7f-310">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Kopier program-IDen fra egenskapene for B2C-programmet](./media/B2CImage_21.png)

<span data-ttu-id="65e7f-312">Bildet nedenfor viser et eksempel på brukerflytpolicyer på siden **Azure AD B2C – brukerflyter (policyer)**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-312">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Samle navnene på hver B2C-policyflyt](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="65e7f-314">Skriv inn programinformasjon om AAD-B2C-leieren i Commerce</span><span class="sxs-lookup"><span data-stu-id="65e7f-314">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="65e7f-315">Du må angi detaljer for Azure AD B2C-leieren i Commerce-områdebygger før du knytter B2C-leieren til områdene.</span><span class="sxs-lookup"><span data-stu-id="65e7f-315">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="65e7f-316">Følg denne fremgangsmåten for å legge til programinformasjon om AAD-B2C-leier i Commerce.</span><span class="sxs-lookup"><span data-stu-id="65e7f-316">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-317">Logg på som administrator for Commerce-områdebygger for miljøet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-317">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="65e7f-318">Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="65e7f-318">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="65e7f-319">Velg **B2C-innstillinger** under **Leierinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-319">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="65e7f-320">Velg **Behandle** i hovedvinduet ved siden av **B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-320">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="65e7f-321">(Hvis leieren vises i listen over B2C-programmer, var den allerede lagt til av en administrator.</span><span class="sxs-lookup"><span data-stu-id="65e7f-321">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="65e7f-322">Kontroller at elementene i trinn 6 nedenfor samsvarer med B2C-programmet.)</span><span class="sxs-lookup"><span data-stu-id="65e7f-322">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="65e7f-323">Velg **Legg til B2C-program**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-323">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="65e7f-324">Skriv inn følgende obligatoriske elementer i skjemaet som vises, ved hjelp av verdier fra B2C-leieren og -programmet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-324">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="65e7f-325">Felt som ikke er påkrevd (de uten en stjerne) kan være tomme.</span><span class="sxs-lookup"><span data-stu-id="65e7f-325">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="65e7f-326">**Programnavn**: Navnet på B2C-programmet, for eksempel "Fabrikam B2C".</span><span class="sxs-lookup"><span data-stu-id="65e7f-326">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="65e7f-327">**Navn på leietaker**: Navnet på B2C-leieren din (bruk for eksempel "fabrikam" hvis domenet vises som "fabrikam.onmicrosoft.com" for B2C-leieren).</span><span class="sxs-lookup"><span data-stu-id="65e7f-327">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="65e7f-328">**Policy-ID for glemt passord**: Brukerflytpolicy-ID for glemt passord, for eksempel "B2C_1_PasswordReset".</span><span class="sxs-lookup"><span data-stu-id="65e7f-328">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="65e7f-329">**Policy-ID for registrering/pålogging**: Brukerflytpolicy-ID for registrering/pålogging, for eksempel "B2C_1_signup_signin".</span><span class="sxs-lookup"><span data-stu-id="65e7f-329">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="65e7f-330">**Klient-GUID**: ID for B2C-program, for eksempel "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span><span class="sxs-lookup"><span data-stu-id="65e7f-330">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="65e7f-331">**Rediger profilpolicy-ID**: Brukerflytpolicy-ID for profilredigering, for eksempel "B2C_1A_ProfileEdit".</span><span class="sxs-lookup"><span data-stu-id="65e7f-331">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="65e7f-332">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-332">Select **OK**.</span></span> <span data-ttu-id="65e7f-333">Du skal nå se navnet på B2C-programmet ditt i listen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-333">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="65e7f-334">Velg **Lagre** for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="65e7f-334">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="65e7f-335">Knytte B2C-programmet til området og kanalen</span><span class="sxs-lookup"><span data-stu-id="65e7f-335">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="65e7f-336">Hvis området allerede er knyttet til et B2C-program, vil endring i et annet B2C-program fjerne gjeldende referanser som er opprettet for brukere som allerede er registrert i dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-336">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="65e7f-337">Hvis de er endret, vil ingen av legitimasjoner som er knyttet til det tilordnede B2C-programmet, være tilgjengelig for brukerne.</span><span class="sxs-lookup"><span data-stu-id="65e7f-337">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="65e7f-338">Bare oppdater B2C-programmet hvis du konfigurerer kanalens B2C-program for første gang, eller hvis du vil at brukere skal registrere seg på nytt med ny legitimasjon for denne kanalen med det nye B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="65e7f-338">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="65e7f-339">Vær forsiktig når du knytter kanaler til B2C-programmer, og navngi programmer tydelig.</span><span class="sxs-lookup"><span data-stu-id="65e7f-339">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="65e7f-340">Hvis en kanal ikke er knyttet til et B2C-program i trinnene nedenfor, vil brukere som logger seg på den kanalen for området, bli lagt inn i B2C-programmet og vises som **standard** i listen **Leierinnstillinger \> B2C-innstillinger** for B2C-programmer.</span><span class="sxs-lookup"><span data-stu-id="65e7f-340">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="65e7f-341">Følg denne fremgangsmåten for å knytte B2C-programmet til området og kanalen.</span><span class="sxs-lookup"><span data-stu-id="65e7f-341">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="65e7f-342">Naviger til området i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="65e7f-342">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="65e7f-343">Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="65e7f-343">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="65e7f-344">Velg **Kanaler** under **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-344">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="65e7f-345">Velg din kanal i hovedvinduet under **Kanaler**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-345">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="65e7f-346">I ruten kanalegenskaper til høyre velger du B2C-programnavnet fra rullegardinmenyen **Velg B2C-program**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-346">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="65e7f-347">Velg **Lukk**, og velg deretter **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="65e7f-347">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="65e7f-348">Ekstra B2C-informasjon</span><span class="sxs-lookup"><span data-stu-id="65e7f-348">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="65e7f-349">Kundeoverføring</span><span class="sxs-lookup"><span data-stu-id="65e7f-349">Customer migration</span></span>

<span data-ttu-id="65e7f-350">Hvis du vurderer å overføre kundeposter fra en tidligere identitetsleverandørplattform, kan du arbeide med Dynamics 365 Commerce-teamet for å gjennomgå kundeoverføringsbehovene dine.</span><span class="sxs-lookup"><span data-stu-id="65e7f-350">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="65e7f-351">Hvis du vil ha mer Azure AD B2C-dokumentasjon om kundeoverføring, kan du se [Overføre brukere til Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="65e7f-351">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="65e7f-352">Egendefinerte policyer</span><span class="sxs-lookup"><span data-stu-id="65e7f-352">Custom policies</span></span>

<span data-ttu-id="65e7f-353">Hvis du vil ha mer informasjon om tilpassing av Azure AD B2C-samhandlinger og policyflyter utover hva som tilbys av B2C-standardpolicyer, kan du se [Egendefinerte policyer i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="65e7f-353">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="65e7f-354">Sekundær administrator</span><span class="sxs-lookup"><span data-stu-id="65e7f-354">Secondary admin</span></span>

<span data-ttu-id="65e7f-355">En valgfri, sekundær administratorkonto kan legges til i **Brukere**-delen av B2C-leieren.</span><span class="sxs-lookup"><span data-stu-id="65e7f-355">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="65e7f-356">Dette kan være en direkte konto eller en generell konto.</span><span class="sxs-lookup"><span data-stu-id="65e7f-356">This can be a direct account or a general account.</span></span> <span data-ttu-id="65e7f-357">Hvis du må dele en konto på tvers av teamressurser, kan du også opprette en felles konto.</span><span class="sxs-lookup"><span data-stu-id="65e7f-357">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="65e7f-358">På grunn av følsomheten til dataene som er lagret i Azure AD B2C, bør en felles konto overvåkes nøye i henhold til firmaets sikkerhetspraksis.</span><span class="sxs-lookup"><span data-stu-id="65e7f-358">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65e7f-359">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="65e7f-359">Additional resources</span></span>

[<span data-ttu-id="65e7f-360">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="65e7f-360">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="65e7f-361">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="65e7f-361">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="65e7f-362">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="65e7f-362">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="65e7f-363">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="65e7f-363">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="65e7f-364">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="65e7f-364">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

<span data-ttu-id="65e7f-365">[Last opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)Tilknytt et Dynamics 365 Commerce-område med en nettkanal</span><span class="sxs-lookup"><span data-stu-id="65e7f-365">[Upload URL redirects in bulk](upload-bulk-redirects.md)Associate a Dynamics 365 Commerce site with an online channel</span></span>

[<span data-ttu-id="65e7f-366">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="65e7f-366">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="65e7f-367">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="65e7f-367">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="65e7f-368">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="65e7f-368">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="65e7f-369">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="65e7f-369">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

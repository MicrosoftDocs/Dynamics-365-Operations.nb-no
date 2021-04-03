---
title: Definere egendefinerte sider for brukerpålogginger
description: Dette emnet beskriver hvordan du bygger egendefinerte sider i Microsoft Dynamics 365 Commerce som håndterer tilpassede pålogginger for brukere av Azure Active Directory (Azure AD)-forretning-til-forbruker-leiere (B2C).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477954"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="fd125-103">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="fd125-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd125-104">Dette emnet beskriver hvordan du bygger egendefinerte sider i Microsoft Dynamics 365 Commerce som håndterer tilpassede pålogginger for brukere av Azure Active Directory (Azure AD)-forretning-til-forbruker-leiere (B2C).</span><span class="sxs-lookup"><span data-stu-id="fd125-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="fd125-105">Hvis du vil bruke egendefinerte sider som er forfattet i Dynamics 365 Commerce, til å håndtere brukerpåloggingsflyter, må du definere Azure AD-policyene som det skal refereres til i handelsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="fd125-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="fd125-106">Du kan konfigurere Azure AD B2C-policyer for registrering og pålogging, profilredigering og tilbakestilling av passord ved hjelp av Azure AD B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="fd125-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="fd125-107">Azure AD B2C-leieren og policynavnene kan deretter refereres til under klargjøringsprosessen som utføres for handelsmiljøet, ved å bruke Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fd125-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="fd125-108">De egendefinerte handelssidene kan bygges ved hjelp av modulen for pålogging, registrering, kontoprofilredigering og tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="fd125-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="fd125-109">Det bør deretter refereres til side-URL-adressene som publiseres for disse egendefinerte sidene, i Azure AD B2C-policykonfigurasjoner på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="fd125-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="fd125-110">Definere B2C-policyer</span><span class="sxs-lookup"><span data-stu-id="fd125-110">Set up B2C policies</span></span>

<span data-ttu-id="fd125-111">Når du konfigurerer Azure AD B2C-leieren og knytter den til handelsmiljøet, går du til **Azure AD B2C**-siden i Azure-portalen, og deretter, på menyen under **Policyer**, velger du **Brukerflyter (policyer)**.</span><span class="sxs-lookup"><span data-stu-id="fd125-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Brukerflyter (policyer)-kommandoen på menyen](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="fd125-113">Nå kan du konfigurere brukerpåloggingsflytene for registrering og pålogging, profilredigering og tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="fd125-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="fd125-114">Konfigurere policy for registrering og pålogging</span><span class="sxs-lookup"><span data-stu-id="fd125-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="fd125-115">Følg denne fremgangsmåten for å konfigurere policyen for registrering og pålogging</span><span class="sxs-lookup"><span data-stu-id="fd125-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="fd125-116">Velg **Ny brukerflyt**, og deretter, på fanen **Anbefalt**, velger du policyen for **Registrering og pålogging**.</span><span class="sxs-lookup"><span data-stu-id="fd125-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="fd125-117">Angi et navn for policyen (for eksempel **B2C\_1\_RegistreringPålogging**).</span><span class="sxs-lookup"><span data-stu-id="fd125-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="fd125-118">I delen **Identitetsleverandører** velger du ID-leverandørene som skal brukes for policyen.</span><span class="sxs-lookup"><span data-stu-id="fd125-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="fd125-119">Som et minimum må **E-postregistrering** velges.</span><span class="sxs-lookup"><span data-stu-id="fd125-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="fd125-120">I kolonnen **Innhent attributt** merker du av for avmerkingsboksene for **E-postadresse**, **Gitt navn** og **Etternavn**.</span><span class="sxs-lookup"><span data-stu-id="fd125-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="fd125-121">I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Identitetsleverandør**, **Etternavn** og **Brukers objekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="fd125-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Valgte attributter og krav](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="fd125-123">Velg **OK** for å opprette policyen.</span><span class="sxs-lookup"><span data-stu-id="fd125-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="fd125-124">Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="fd125-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="fd125-125">Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.</span><span class="sxs-lookup"><span data-stu-id="fd125-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Egenskapsside for den nye policyen](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="fd125-127">Policynavnet blir fullstendig referert til i handelsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="fd125-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="fd125-128">(**B2C\_1\_** vil bli inkludert i referansen.) Policyer kan ikke endres etter at de er opprettet.</span><span class="sxs-lookup"><span data-stu-id="fd125-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="fd125-129">Hvis du erstatter en eksisterende policy for handelsmiljøet ditt, kan du slette den opprinnelige policyen og bygge en ny policy som har samme navn.</span><span class="sxs-lookup"><span data-stu-id="fd125-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="fd125-130">Hvis miljøet allerede er klargjort, er det også mulig å sende det nye policynavnet via en tjenesteforespørsel.</span><span class="sxs-lookup"><span data-stu-id="fd125-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="fd125-131">Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene.</span><span class="sxs-lookup"><span data-stu-id="fd125-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="fd125-132">Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="fd125-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="fd125-133">Konfigurere policyen for profilredigering</span><span class="sxs-lookup"><span data-stu-id="fd125-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="fd125-134">Hvis du vil konfigurere policyen for profilredigering, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="fd125-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="fd125-135">Velg **Ny brukerflyt**, og deretter, på fanen **Anbefalt**, velger du policyen for **Profilredigering**.</span><span class="sxs-lookup"><span data-stu-id="fd125-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="fd125-136">Angi et navn for policyen (for eksempel **B2C\_1\_RedigerProfil**).</span><span class="sxs-lookup"><span data-stu-id="fd125-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="fd125-137">I delen **Identitetsleverandører** velger du ID-leverandørene som skal brukes for policyen.</span><span class="sxs-lookup"><span data-stu-id="fd125-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="fd125-138">Du må minimum velge **Logg på lokal konto**.</span><span class="sxs-lookup"><span data-stu-id="fd125-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="fd125-139">I kolonnen **Innhent attributt** merker du av for **E-postadresser** og **Etternavn**.</span><span class="sxs-lookup"><span data-stu-id="fd125-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="fd125-140">I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Identitetsleverandør**, **Etternavn** og **Brukers objekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="fd125-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="fd125-141">Velg **OK** for å opprette policyen.</span><span class="sxs-lookup"><span data-stu-id="fd125-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="fd125-142">Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="fd125-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="fd125-143">Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.</span><span class="sxs-lookup"><span data-stu-id="fd125-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="fd125-144">Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene.</span><span class="sxs-lookup"><span data-stu-id="fd125-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="fd125-145">Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="fd125-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="fd125-146">Konfigurere policyen for tilbakestilling av passord</span><span class="sxs-lookup"><span data-stu-id="fd125-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="fd125-147">Hvis du vil konfigurere policyen for tilbakestilling av passord, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="fd125-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="fd125-148">Velg **Ny brukerflyt**, og deretter, på fanen **Forhåndsvisning**, velger du policyen for **Tilbakestilling av passord v1.1**.</span><span class="sxs-lookup"><span data-stu-id="fd125-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Policy for tilbakestilling av passord v1.1 valgt i kategorien Forhåndsvisning](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="fd125-150">Angi et navn for policyen (for eksempel **B2C\_1\_GlemPassord**).</span><span class="sxs-lookup"><span data-stu-id="fd125-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="fd125-151">I delen **Identitetsleverandører** velger du **Tilbakestill passord ved hjelp av e-postadresse**.</span><span class="sxs-lookup"><span data-stu-id="fd125-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="fd125-152">I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Etternavn** og **Brukers objekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="fd125-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valgte krav](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="fd125-154">Velg **OK** for å opprette policyen.</span><span class="sxs-lookup"><span data-stu-id="fd125-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="fd125-155">Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="fd125-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="fd125-156">Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.</span><span class="sxs-lookup"><span data-stu-id="fd125-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="fd125-157">Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene.</span><span class="sxs-lookup"><span data-stu-id="fd125-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="fd125-158">Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="fd125-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="fd125-159">Utarbeide de egendefinerte sidene</span><span class="sxs-lookup"><span data-stu-id="fd125-159">Build the custom pages</span></span>

<span data-ttu-id="fd125-160">Følg denne fremgangsmåten for å bygge egendefinerte sider for å håndtere brukerpålogginger.</span><span class="sxs-lookup"><span data-stu-id="fd125-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="fd125-161">Gå til området ditt i redigeringsverktøyene for handel.</span><span class="sxs-lookup"><span data-stu-id="fd125-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="fd125-162">Lag følgende fem maler og fem sider:</span><span class="sxs-lookup"><span data-stu-id="fd125-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="fd125-163">En mal og side for **Registrering** som bruker registreringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="fd125-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="fd125-164">En mal og side for **Pålogging** som bruker påloggingsmodulen.</span><span class="sxs-lookup"><span data-stu-id="fd125-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="fd125-165">En mal og side for **Tilbakestill passord** som bruker modulen for tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="fd125-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="fd125-166">En mal og side for **Tilbakestill passord-kontroll** som bruker modulen for kontroll av tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="fd125-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="fd125-167">En mal og side for **Profilredigering** som bruker modulen for profilredigering av konto</span><span class="sxs-lookup"><span data-stu-id="fd125-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="fd125-168">Følg disse retningslinjene når du bygger sidene:</span><span class="sxs-lookup"><span data-stu-id="fd125-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="fd125-169">Bruk oppsettet og stilen som passer best til dine forretningsbehov, for hver side eller modul.</span><span class="sxs-lookup"><span data-stu-id="fd125-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="fd125-170">Publiser alle sider og URL-adresser som må brukes i Azure AD B2C-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="fd125-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="fd125-171">Når sidene og URL-adressene er publisert, samler du inn URL-adressene som må brukes for Azure AD B2C-policykonfigurasjonene.</span><span class="sxs-lookup"><span data-stu-id="fd125-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="fd125-172">Et **?preloadscripts=true**-suffiks blir lagt til hver URL-adresse når den brukes.</span><span class="sxs-lookup"><span data-stu-id="fd125-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd125-173">Ikke bruk universelle topptekster og bunntekster som har relative koblinger, på nytt.</span><span class="sxs-lookup"><span data-stu-id="fd125-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="fd125-174">Siden disse sidene vil være vert på Azure AD B2C-domenet når de brukes, bør bare absolutte URL-adresser brukes for alle koblinger.</span><span class="sxs-lookup"><span data-stu-id="fd125-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="fd125-175">Konfigurere Azure AD B2C-policyer med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="fd125-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="fd125-176">I Azure-portal går du tilbake til **Azure AD B2C**-siden og deretter, på menyen, under **Policyer**, velger du **Brukerflyter (policyer)**.</span><span class="sxs-lookup"><span data-stu-id="fd125-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="fd125-177">Oppdater policyen for registrering og pålogging med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="fd125-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="fd125-178">Følg disse trinnene for å oppdatere policyen for registrering og pålogging med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="fd125-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="fd125-179">I policyen for **Pålogging og registrering** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="fd125-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="fd125-180">Velg oppsettet for **Side for enhetlig registrering og pålogging**.</span><span class="sxs-lookup"><span data-stu-id="fd125-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="fd125-181">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fd125-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="fd125-182">I feltet **Egendefinert side-URI** angir du URL-adressen for full pålogging.</span><span class="sxs-lookup"><span data-stu-id="fd125-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="fd125-183">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="fd125-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="fd125-184">Skriv for eksempel inn ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="fd125-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="fd125-185">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="fd125-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="fd125-186">Velg oppsettet **Registreringsside for lokal konto**.</span><span class="sxs-lookup"><span data-stu-id="fd125-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="fd125-187">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fd125-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="fd125-188">I feltet **Egendefinert side-URI** angir du URL-adressen for full registrering.</span><span class="sxs-lookup"><span data-stu-id="fd125-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="fd125-189">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="fd125-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="fd125-190">Skriv for eksempel inn ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="fd125-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="fd125-191">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="fd125-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="fd125-192">I delen **Brukerattributter** følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="fd125-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="fd125-193">For attributtene **E-postadresse**, **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Krever godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="fd125-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="fd125-194">For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Valgfri**.</span><span class="sxs-lookup"><span data-stu-id="fd125-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Konfigurasjon av policy for registreringsside for lokal konto](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="fd125-196">Oppdater policyen for profilredigering med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="fd125-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="fd125-197">Følg disse trinnene for å oppdatere policyen for profilredigering med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="fd125-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="fd125-198">I policyen for **Profilredigering** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="fd125-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="fd125-199">Velg oppsettet **Profilredigeringsside**.</span><span class="sxs-lookup"><span data-stu-id="fd125-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="fd125-200">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fd125-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="fd125-201">I feltet **Egendefinert side-URI** angir du URL-adressen for profilredigering.</span><span class="sxs-lookup"><span data-stu-id="fd125-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="fd125-202">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="fd125-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="fd125-203">Skriv for eksempel inn ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="fd125-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="fd125-204">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="fd125-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="fd125-205">I delen **Brukerattributter** følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="fd125-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="fd125-206">For attributtene **E-postadresse**, **Gitt navn** velger du **Nei** i feltet **Krever godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="fd125-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="fd125-207">For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Valgfri**.</span><span class="sxs-lookup"><span data-stu-id="fd125-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="fd125-208">Oppdater policyen for tilbakestilling av passord med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="fd125-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="fd125-209">Følg disse trinnene for å oppdatere policyen for tilbakestilling av passord med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="fd125-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="fd125-210">I policyen for **Tilbakestilling av passord** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="fd125-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="fd125-211">Velg oppsettet **Side for nytt passord**.</span><span class="sxs-lookup"><span data-stu-id="fd125-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="fd125-212">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fd125-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="fd125-213">I feltet **Egendefinert side-URI** angir du URL-adressen for fullstendig tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="fd125-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="fd125-214">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="fd125-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="fd125-215">Skriv for eksempel inn ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="fd125-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="fd125-216">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="fd125-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="fd125-217">Velg oppsettet **Side for kontoverifisering**.</span><span class="sxs-lookup"><span data-stu-id="fd125-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="fd125-218">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fd125-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="fd125-219">I feltet **Egendefinert side-URI** angir du URL-adressen for fullstendig verifisering av passord.</span><span class="sxs-lookup"><span data-stu-id="fd125-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="fd125-220">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="fd125-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="fd125-221">Skriv for eksempel inn ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="fd125-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="fd125-222">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="fd125-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="fd125-223">Tilpasse standard tekststrenger for etiketter og beskrivelser</span><span class="sxs-lookup"><span data-stu-id="fd125-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="fd125-224">I modulbiblioteket er påloggingsmoduler forhåndsutfylt med standard tekststrenger for etikettene og beskrivelsene.</span><span class="sxs-lookup"><span data-stu-id="fd125-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="fd125-225">Du kan tilpasse disse strengene i programvareutviklingssettet (SDK) ved å oppdatere verdiene i global.json-filen for påloggingsmodulen.</span><span class="sxs-lookup"><span data-stu-id="fd125-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="fd125-226">Standardteksten for den glemte passordkoblingen er **Glemt passordet?**.</span><span class="sxs-lookup"><span data-stu-id="fd125-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="fd125-227">Nedenfor vises denne standardteksten på påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="fd125-227">The following shows this default text on the sign-in page.</span></span>

![Standardtekst for koblingen for glemt passord på påloggingssiden](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="fd125-229">I global.json-filen for påloggingsmodulen for modulbiblioteket kan du redigere teksten til **Glemt passord?**, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="fd125-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Oppdatere koblingstekst i påloggingsmodulens global.json-fil](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="fd125-231">Når du har oppdatert global.json-filen og publisert endringene, vises den nye koblingsteksten i påloggingsmodulen både på Commerce-siden og på den aktive påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="fd125-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd125-232">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fd125-232">Additional resources</span></span>

[<span data-ttu-id="fd125-233">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="fd125-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fd125-234">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="fd125-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="fd125-235">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="fd125-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="fd125-236">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="fd125-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="fd125-237">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="fd125-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="fd125-238">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="fd125-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="fd125-239">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="fd125-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="fd125-240">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="fd125-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="fd125-241">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="fd125-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="fd125-242">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="fd125-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

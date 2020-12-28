---
title: Definere egendefinerte sider for brukerpålogginger
description: Dette emnet beskriver hvordan du bygger egendefinerte sider i Microsoft Dynamics 365 Commerce som håndterer tilpassede pålogginger for brukere av Azure Active Directory (Azure AD)-firma-til-kunde-leiere (B2C).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5d9f2febc912b35897b063019146d219cadea1fa
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517238"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="62b9d-103">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="62b9d-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="62b9d-104">Dette emnet beskriver hvordan du bygger egendefinerte sider i Microsoft Dynamics 365 Commerce som håndterer tilpassede pålogginger for brukere av Azure Active Directory (Azure AD)-firma-til-kunde-leiere (B2C).</span><span class="sxs-lookup"><span data-stu-id="62b9d-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="62b9d-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="62b9d-105">Overview</span></span>

<span data-ttu-id="62b9d-106">Hvis du vil bruke egendefinerte sider som er forfattet i Dynamics 365 Commerce, til å håndtere brukerpåloggingsflyter, må du definere Azure AD-policyene som det skal refereres til i handelsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="62b9d-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="62b9d-107">Du kan konfigurere Azure AD B2C-policyer for registrering og pålogging, profilredigering og tilbakestilling av passord ved hjelp av Azure AD B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="62b9d-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="62b9d-108">Azure AD B2C-leieren og policynavnene kan deretter refereres til under klargjøringsprosessen som utføres for handelsmiljøet, ved å bruke Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="62b9d-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="62b9d-109">De egendefinerte handelssidene kan bygges ved hjelp av modulen for pålogging, registrering, kontoprofilredigering og tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="62b9d-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="62b9d-110">Det bør deretter refereres til side-URL-adressene som publiseres for disse egendefinerte sidene, i Azure AD B2C-policykonfigurasjoner på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="62b9d-111">Definere B2C-policyer</span><span class="sxs-lookup"><span data-stu-id="62b9d-111">Set up B2C policies</span></span>

<span data-ttu-id="62b9d-112">Når du konfigurerer Azure AD B2C-leieren og knytter den til handelsmiljøet, går du til **Azure AD B2C**-siden i Azure-portalen, og deretter, på menyen under **Policyer**, velger du **Brukerflyter (policyer)**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Brukerflyter (policyer)-kommandoen på menyen](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="62b9d-114">Nå kan du konfigurere brukerpåloggingsflytene for registrering og pålogging, profilredigering og tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="62b9d-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="62b9d-115">Konfigurere policy for registrering og pålogging</span><span class="sxs-lookup"><span data-stu-id="62b9d-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="62b9d-116">Følg denne fremgangsmåten for å konfigurere policyen for registrering og pålogging</span><span class="sxs-lookup"><span data-stu-id="62b9d-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="62b9d-117">Velg **Ny brukerflyt**, og deretter, på fanen **Anbefalt**, velger du policyen for **Registrering og pålogging**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="62b9d-118">Angi et navn for policyen (for eksempel **B2C\_1\_RegistreringPålogging**).</span><span class="sxs-lookup"><span data-stu-id="62b9d-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="62b9d-119">I delen **Identitetsleverandører** velger du ID-leverandørene som skal brukes for policyen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="62b9d-120">Som et minimum må **E-postregistrering** velges.</span><span class="sxs-lookup"><span data-stu-id="62b9d-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="62b9d-121">I kolonnen **Innhent attributt** merker du av for avmerkingsboksene for **E-postadresse**, **Gitt navn** og **Etternavn**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="62b9d-122">I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Identitetsleverandør**, **Etternavn** og **Brukers objekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Valgte attributter og krav](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="62b9d-124">Velg **OK** for å opprette policyen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="62b9d-125">Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="62b9d-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="62b9d-126">Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Egenskapsside for den nye policyen](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="62b9d-128">Policynavnet blir fullstendig referert til i handelsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="62b9d-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="62b9d-129">(**B2C\_1\_** vil bli inkludert i referansen.) Policyer kan ikke endres etter at de er opprettet.</span><span class="sxs-lookup"><span data-stu-id="62b9d-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="62b9d-130">Hvis du erstatter en eksisterende policy for handelsmiljøet ditt, kan du slette den opprinnelige policyen og bygge en ny policy som har samme navn.</span><span class="sxs-lookup"><span data-stu-id="62b9d-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="62b9d-131">Hvis miljøet allerede er klargjort, er det også mulig å sende det nye policynavnet via en tjenesteforespørsel.</span><span class="sxs-lookup"><span data-stu-id="62b9d-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="62b9d-132">Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene.</span><span class="sxs-lookup"><span data-stu-id="62b9d-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="62b9d-133">Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="62b9d-134">Konfigurere policyen for profilredigering</span><span class="sxs-lookup"><span data-stu-id="62b9d-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="62b9d-135">Hvis du vil konfigurere policyen for profilredigering, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="62b9d-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="62b9d-136">Velg **Ny brukerflyt**, og deretter, på fanen **Anbefalt**, velger du policyen for **Profilredigering**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="62b9d-137">Angi et navn for policyen (for eksempel **B2C\_1\_RedigerProfil**).</span><span class="sxs-lookup"><span data-stu-id="62b9d-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="62b9d-138">I delen **Identitetsleverandører** velger du ID-leverandørene som skal brukes for policyen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="62b9d-139">Du må minimum velge **Logg på lokal konto**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="62b9d-140">I kolonnen **Innhent attributt** merker du av for **E-postadresser** og **Etternavn**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="62b9d-141">I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Identitetsleverandør**, **Etternavn** og **Brukers objekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="62b9d-142">Velg **OK** for å opprette policyen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="62b9d-143">Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="62b9d-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="62b9d-144">Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="62b9d-145">Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene.</span><span class="sxs-lookup"><span data-stu-id="62b9d-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="62b9d-146">Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="62b9d-147">Konfigurere policyen for tilbakestilling av passord</span><span class="sxs-lookup"><span data-stu-id="62b9d-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="62b9d-148">Hvis du vil konfigurere policyen for tilbakestilling av passord, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="62b9d-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="62b9d-149">Velg **Ny brukerflyt**, og deretter, på fanen **Forhåndsvisning**, velger du policyen for **Tilbakestilling av passord v1.1**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Policy for tilbakestilling av passord v1.1 valgt i kategorien Forhåndsvisning](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="62b9d-151">Angi et navn for policyen (for eksempel **B2C\_1\_GlemPassord**).</span><span class="sxs-lookup"><span data-stu-id="62b9d-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="62b9d-152">I delen **Identitetsleverandører** velger du **Tilbakestill passord ved hjelp av e-postadresse**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="62b9d-153">I kolonnen **Returkrav** merker du av for **E-postadresser**, **Gitt navn**, **Etternavn** og **Brukers objekt-ID**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valgte krav](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="62b9d-155">Velg **OK** for å opprette policyen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="62b9d-156">Dobbeltklikk det nye policynavnet, og velg deretter **Egenskaper** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="62b9d-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="62b9d-157">Sett alternativet for **Aktiver JavaScript-valg av sideoppsett (forhåndsvisning)** til **På**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="62b9d-158">Du kommer tilbake til denne policyen for å fullføre oppsettet etter at du har bygget de egendefinerte sidene.</span><span class="sxs-lookup"><span data-stu-id="62b9d-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="62b9d-159">Foreløpig lukker du policyen for å gå tilbake til siden **Brukerflyt (policyer)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="62b9d-160">Utarbeide de egendefinerte sidene</span><span class="sxs-lookup"><span data-stu-id="62b9d-160">Build the custom pages</span></span>

<span data-ttu-id="62b9d-161">Følg denne fremgangsmåten for å bygge egendefinerte sider for å håndtere brukerpålogginger.</span><span class="sxs-lookup"><span data-stu-id="62b9d-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="62b9d-162">Gå til området ditt i redigeringsverktøyene for handel.</span><span class="sxs-lookup"><span data-stu-id="62b9d-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="62b9d-163">Lag følgende fem maler og fem sider:</span><span class="sxs-lookup"><span data-stu-id="62b9d-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="62b9d-164">En mal og side for **Registrering** som bruker registreringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="62b9d-165">En mal og side for **Pålogging** som bruker påloggingsmodulen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="62b9d-166">En mal og side for **Tilbakestill passord** som bruker modulen for tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="62b9d-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="62b9d-167">En mal og side for **Tilbakestill passord-kontroll** som bruker modulen for kontroll av tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="62b9d-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="62b9d-168">En mal og side for **Profilredigering** som bruker modulen for profilredigering av konto</span><span class="sxs-lookup"><span data-stu-id="62b9d-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="62b9d-169">Følg disse retningslinjene når du bygger sidene:</span><span class="sxs-lookup"><span data-stu-id="62b9d-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="62b9d-170">Bruk oppsettet og stilen som passer best til dine forretningsbehov, for hver side eller modul.</span><span class="sxs-lookup"><span data-stu-id="62b9d-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="62b9d-171">Publiser alle sider og URL-adresser som må brukes i Azure AD B2C-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="62b9d-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="62b9d-172">Når sidene og URL-adressene er publisert, samler du inn URL-adressene som må brukes for Azure AD B2C-policykonfigurasjonene.</span><span class="sxs-lookup"><span data-stu-id="62b9d-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="62b9d-173">Et **?preloadscripts=true**-suffiks blir lagt til hver URL-adresse når den brukes.</span><span class="sxs-lookup"><span data-stu-id="62b9d-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62b9d-174">Ikke bruk universelle topptekster og bunntekster som har relative koblinger, på nytt.</span><span class="sxs-lookup"><span data-stu-id="62b9d-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="62b9d-175">Siden disse sidene vil være vert på Azure AD B2C-domenet når de brukes, bør bare absolutte URL-adresser brukes for alle koblinger.</span><span class="sxs-lookup"><span data-stu-id="62b9d-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="62b9d-176">Konfigurere Azure AD B2C-policyer med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="62b9d-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="62b9d-177">I Azure-portal går du tilbake til **Azure AD B2C**-siden og deretter, på menyen, under **Policyer**, velger du **Brukerflyter (policyer)**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="62b9d-178">Oppdater policyen for registrering og pålogging med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="62b9d-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="62b9d-179">Følg disse trinnene for å oppdatere policyen for registrering og pålogging med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="62b9d-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="62b9d-180">I policyen for **Pålogging og registrering** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="62b9d-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="62b9d-181">Velg oppsettet for **Side for enhetlig registrering og pålogging**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="62b9d-182">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62b9d-183">I feltet **Egendefinert side-URI** angir du URL-adressen for full pålogging.</span><span class="sxs-lookup"><span data-stu-id="62b9d-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="62b9d-184">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62b9d-185">Skriv for eksempel inn ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="62b9d-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62b9d-186">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="62b9d-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="62b9d-187">Velg oppsettet **Registreringsside for lokal konto**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="62b9d-188">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62b9d-189">I feltet **Egendefinert side-URI** angir du URL-adressen for full registrering.</span><span class="sxs-lookup"><span data-stu-id="62b9d-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="62b9d-190">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62b9d-191">Skriv for eksempel inn ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="62b9d-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62b9d-192">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="62b9d-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="62b9d-193">I delen **Brukerattributter** følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="62b9d-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="62b9d-194">For attributtene **E-postadresse**, **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Krever godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="62b9d-195">For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Valgfri**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Konfigurasjon av policy for registreringsside for lokal konto](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="62b9d-197">Oppdater policyen for profilredigering med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="62b9d-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="62b9d-198">Følg disse trinnene for å oppdatere policyen for profilredigering med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="62b9d-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="62b9d-199">I policyen for **Profilredigering** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="62b9d-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="62b9d-200">Velg oppsettet **Profilredigeringsside**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="62b9d-201">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62b9d-202">I feltet **Egendefinert side-URI** angir du URL-adressen for profilredigering.</span><span class="sxs-lookup"><span data-stu-id="62b9d-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="62b9d-203">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62b9d-204">Skriv for eksempel inn ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="62b9d-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62b9d-205">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="62b9d-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="62b9d-206">I delen **Brukerattributter** følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="62b9d-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="62b9d-207">For attributtene **E-postadresse**, **Gitt navn** velger du **Nei** i feltet **Krever godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="62b9d-208">For attributtene **Gitt navn** og **Etternavn** velger du **Nei** i feltet **Valgfri**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="62b9d-209">Oppdater policyen for tilbakestilling av passord med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="62b9d-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="62b9d-210">Følg disse trinnene for å oppdatere policyen for tilbakestilling av passord med egendefinert sideinformasjon</span><span class="sxs-lookup"><span data-stu-id="62b9d-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="62b9d-211">I policyen for **Tilbakestilling av passord** som du konfigurerte tidligere, velger du **Sideoppsett** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="62b9d-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="62b9d-212">Velg oppsettet **Side for nytt passord**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="62b9d-213">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62b9d-214">I feltet **Egendefinert side-URI** angir du URL-adressen for fullstendig tilbakestilling av passord.</span><span class="sxs-lookup"><span data-stu-id="62b9d-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="62b9d-215">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62b9d-216">Skriv for eksempel inn ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="62b9d-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62b9d-217">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="62b9d-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="62b9d-218">Velg oppsettet **Side for kontoverifisering**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="62b9d-219">Sett alternativet **Bruk egendefinert sideoppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62b9d-220">I feltet **Egendefinert side-URI** angir du URL-adressen for fullstendig verifisering av passord.</span><span class="sxs-lookup"><span data-stu-id="62b9d-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="62b9d-221">Inkluder suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62b9d-222">Skriv for eksempel inn ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="62b9d-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62b9d-223">I feltet for **Sideoppsettversjon (forhåndsvisning)** velger du **1.2.0** .</span><span class="sxs-lookup"><span data-stu-id="62b9d-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="62b9d-224">Tilpasse standard tekststrenger for etiketter og beskrivelser</span><span class="sxs-lookup"><span data-stu-id="62b9d-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="62b9d-225">I modulbiblioteket er påloggingsmoduler forhåndsutfylt med standard tekststrenger for etikettene og beskrivelsene.</span><span class="sxs-lookup"><span data-stu-id="62b9d-225">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="62b9d-226">Du kan tilpasse disse strengene i programvareutviklingssettet (SDK) ved å oppdatere verdiene i global.json-filen for påloggingsmodulen.</span><span class="sxs-lookup"><span data-stu-id="62b9d-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="62b9d-227">Standardteksten for den glemte passordkoblingen er **Glemt passordet?**.</span><span class="sxs-lookup"><span data-stu-id="62b9d-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="62b9d-228">Nedenfor vises denne standardteksten på påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="62b9d-228">The following shows this default text on the sign-in page.</span></span>

![Standardtekst for koblingen for glemt passord på påloggingssiden](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="62b9d-230">I global.json-filen for påloggingsmodulen for modulbiblioteket kan du redigere teksten til **Glemt passord?**, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="62b9d-230">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Oppdatere koblingstekst i påloggingsmodulens global.json-fil](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="62b9d-232">Når du har oppdatert global.json-filen og publisert endringene, vises den nye koblingsteksten i påloggingsmodulen både på Commerce-siden og på den aktive påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="62b9d-232">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62b9d-233">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="62b9d-233">Additional resources</span></span>

[<span data-ttu-id="62b9d-234">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="62b9d-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="62b9d-235">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="62b9d-235">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="62b9d-236">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="62b9d-236">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="62b9d-237">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="62b9d-237">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="62b9d-238">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="62b9d-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="62b9d-239">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="62b9d-239">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="62b9d-240">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="62b9d-240">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="62b9d-241">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="62b9d-241">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="62b9d-242">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="62b9d-242">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="62b9d-243">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="62b9d-243">Enable location-based store detection</span></span>](enable-store-detection.md)

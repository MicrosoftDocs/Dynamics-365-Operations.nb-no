---
title: Konfigurere flere B2C-leiere i et Commerce-miljø
description: Dette emnet beskriver når og hvordan du definerer flere per kanals Microsoft Azure Active Directory (Azure AD) B2C-leiere for brukergodkjenning i et dedikert Dynamics 365 Commerce-miljø.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4e50855368a3fa86c38c756492fc7e6cd518f497
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796105"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="97c0c-103">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="97c0c-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97c0c-104">Dette emnet beskriver når og hvordan du definerer flere per kanals Microsoft Azure Active Directory (Azure AD) B2C-leiere for brukergodkjenning i et dedikert Dynamics 365 Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="97c0c-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="97c0c-105">Dynamics 365 Commerce bruker identitetstjenesten Azure AD B2C til å støtte brukerlegitimasjon og godkjenningsflyt.</span><span class="sxs-lookup"><span data-stu-id="97c0c-105">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="97c0c-106">Brukere kan bruke godkjenningsflyt til å registrere seg, logge inn og tilbakestille passordet.</span><span class="sxs-lookup"><span data-stu-id="97c0c-106">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="97c0c-107">Azure AD B2C lagrer sensitiv brukergodkjenningsinformasjon, for eksempel brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="97c0c-107">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="97c0c-108">Brukerposten er unik for hver B2C-leier og bruker enten brukernavn (e-postadresse) eller legitimasjon for sosial identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="97c0c-108">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="97c0c-109">I de fleste tilfeller brukes en enkelt Azure AD B2C-leier i et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="97c0c-109">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="97c0c-110">Commerce-kunder kan deretter opprette og publisere flere områder i samme Commerce-miljø, og samme kundelegitimasjon vil bli brukt på tvers av disse områdene.</span><span class="sxs-lookup"><span data-stu-id="97c0c-110">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="97c0c-111">Hvis imidlertid områdene i miljøet skal behandles som ulike merker og vises for brukere som separate firmaer, kan en B2C-leier konfigureres for kanalen som brukes for området/merke-skillet.</span><span class="sxs-lookup"><span data-stu-id="97c0c-111">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="97c0c-112">Betraktninger når flere B2C-leiere settes opp per kanal</span><span class="sxs-lookup"><span data-stu-id="97c0c-112">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="97c0c-113">Når hver kanal eller hvert område behandles som et separat firma, er det ofte best å bruke egne juridiske enheter med hensyn til brukergodkjenningsflyter i Commerce.</span><span class="sxs-lookup"><span data-stu-id="97c0c-113">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="97c0c-114">Hvis du imidlertid vil beholde hver kanal/hvert område i samme miljø og juridisk enhet, men vil ha separate brukergodkjenninger for hvert område, er det viktig at du vurderer følgende punkter før du fortsetter:</span><span class="sxs-lookup"><span data-stu-id="97c0c-114">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="97c0c-115">Brukerne vil ha egne legitimasjonsbeskrivelser for hver kanal/hvert område.</span><span class="sxs-lookup"><span data-stu-id="97c0c-115">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="97c0c-116">Samme person kan ha to separate kontoer per kanal/område, fordi hver konto vil være en unik oppføring i en separat B2C-leier.</span><span class="sxs-lookup"><span data-stu-id="97c0c-116">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="97c0c-117">I Microsoft Dynamics-miljøet returneres separate kundeoppføringer for søk etter globale poster.</span><span class="sxs-lookup"><span data-stu-id="97c0c-117">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="97c0c-118">Hvis en bruker bruker samme e-postadresse på tvers av kanaler/områder, returnerer det globale kundesøket resultater for hver kanal/hvert område.</span><span class="sxs-lookup"><span data-stu-id="97c0c-118">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="97c0c-119">(Det vises en kanalindikator.)</span><span class="sxs-lookup"><span data-stu-id="97c0c-119">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="97c0c-120">Adresseboken kan brukes til å gruppere brukere, slik at de kan spores per kanal.</span><span class="sxs-lookup"><span data-stu-id="97c0c-120">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="97c0c-121">Antallet kundeposter per kanal kan øke, og denne økningen kan påvirke ytelsen til globale kundesøk.</span><span class="sxs-lookup"><span data-stu-id="97c0c-121">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="97c0c-122">B2C-leiere må nøye tilordnes til en kanal for å hindre situasjoner der kunder registrerer seg for å finne en feil leier.</span><span class="sxs-lookup"><span data-stu-id="97c0c-122">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="97c0c-123">Ellers kan forvirring eller sporingsproblemer oppstå.</span><span class="sxs-lookup"><span data-stu-id="97c0c-123">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="97c0c-124">Følgende illustrasjon viser flere B2C-leiere i et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="97c0c-124">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Flere B2C-leiere i et Commerce-miljø](media/MultiB2C_In_Environment.png)

<span data-ttu-id="97c0c-126">Hvis du finner ut at bedriften krever forskjellige B2C-leiere per kanal i samme Commerce-miljø, må du utføre fremgangsmåtene i de følgende delene for å be om denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="97c0c-126">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="97c0c-127">Konfigurere B2C-leiere i ditt miljø</span><span class="sxs-lookup"><span data-stu-id="97c0c-127">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="97c0c-128">Hvis du vil konfigurere B2C-leiere i miljøet ditt, fullfører du de relevante fremgangsmåtene i denne delen.</span><span class="sxs-lookup"><span data-stu-id="97c0c-128">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="97c0c-129">Legge til en Azure AD B2C-leier</span><span class="sxs-lookup"><span data-stu-id="97c0c-129">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="97c0c-130">Følg denne fremgangsmåten for å legge til en Azure AD B2C-leier i miljøet.</span><span class="sxs-lookup"><span data-stu-id="97c0c-130">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="97c0c-131">Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="97c0c-131">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="97c0c-132">Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="97c0c-132">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="97c0c-133">Velg **B2C-innstillinger**, og velg deretter **Behandle**.</span><span class="sxs-lookup"><span data-stu-id="97c0c-133">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="97c0c-134">Velg **Legg til B2C-program**, og angi deretter følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="97c0c-134">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="97c0c-135">**Programnavn**: Angi navnet som skal brukes for programmet i konteksten for administrasjon av det i Commerce.</span><span class="sxs-lookup"><span data-stu-id="97c0c-135">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="97c0c-136">Vi anbefaler at du bruker programnavnet du valgte da du konfigurerte Azure AD B2C-programmet i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="97c0c-136">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="97c0c-137">På denne måten kan du bidra til å redusere forvirring når du administrerer B2C-leiere i Commerce.</span><span class="sxs-lookup"><span data-stu-id="97c0c-137">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="97c0c-138">**Navn på leietaker**: Angi navnet på B2C-leieren slik det vises i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="97c0c-138">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="97c0c-139">**Policy-ID for glemt passord**: Angi policy-IDen (navnet på policyen i Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="97c0c-139">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="97c0c-140">**Policy-ID for registrering/pålogging**: Angi policy-IDen (navnet på policyen i Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="97c0c-140">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="97c0c-141">**Klient-GUID**: Angi Azure AD B2C-leier-IDen slik den vises i Azure-portalen (ikke program-IDen for B2C-leieren).</span><span class="sxs-lookup"><span data-stu-id="97c0c-141">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="97c0c-142">**Policy-ID for redigering av profil**: Angi policy-IDen (navnet på policyen i Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="97c0c-142">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="97c0c-143">Når du er ferdig med å angi denne informasjonen, velger du **OK** for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="97c0c-143">When you've finished entering this information, select **OK** to save your changes.</span></span> <span data-ttu-id="97c0c-144">Den nye Azure AD B2C-leieren skal nå vises i listen under **Behandle B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="97c0c-144">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

> [!NOTE]
> <span data-ttu-id="97c0c-145">Du bør la felt som **Omfang**, **Ikke-interaktiv policy-ID**, **Ikke-interaktiv klient-ID**, **Egendefinert domene for pålogging** og **Policy-ID for registrering** stå tomme, med mindre Dynamics 365 Commerce-teamet instruerer deg om å angi dem.</span><span class="sxs-lookup"><span data-stu-id="97c0c-145">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="97c0c-146">Administrere eller slette en Azure AD B2C-leier</span><span class="sxs-lookup"><span data-stu-id="97c0c-146">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="97c0c-147">Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="97c0c-147">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="97c0c-148">Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="97c0c-148">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="97c0c-149">Velg **B2C-innstillinger**, og velg deretter **Behandle**.</span><span class="sxs-lookup"><span data-stu-id="97c0c-149">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="97c0c-150">Hvis du vil redigere en B2C-leier, velger du blyantsymbolet ved siden av den.</span><span class="sxs-lookup"><span data-stu-id="97c0c-150">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="97c0c-151">Hvis du vil slette en B2C-leier, velger du papirkurvsymbolet ved siden av.</span><span class="sxs-lookup"><span data-stu-id="97c0c-151">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="97c0c-152">Velg **Lagre**, og velg deretter **Publiser** for å aktivere endringene.</span><span class="sxs-lookup"><span data-stu-id="97c0c-152">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="97c0c-153">Når en B2C-leier er konfigurert for et aktivt/publisert område, kan brukere ha registrert seg ved å bruke kontoer som finnes på leieren.</span><span class="sxs-lookup"><span data-stu-id="97c0c-153">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="97c0c-154">Hvis du sletter en konfigurert leier på menyen **Leierinnstillinger \> B2C-leier**, fjerner du tilknytningen av B2C-leieren fra områder som er knyttet til en hvilken som helst kanal i leieren.</span><span class="sxs-lookup"><span data-stu-id="97c0c-154">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="97c0c-155">I dette tilfellet kan det hende at brukerne ikke lenger kan logge på kontoene sine.</span><span class="sxs-lookup"><span data-stu-id="97c0c-155">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="97c0c-156">Vær derfor svært forsiktig når du sletter en konfigurert leier.</span><span class="sxs-lookup"><span data-stu-id="97c0c-156">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="97c0c-157">Når en konfigurert leier slettes, vil B2C-leieren og -postene fortsatt bli opprettholdt, men Commerce-systemkonfigurasjonen for denne leieren vil bli endret eller fjernet.</span><span class="sxs-lookup"><span data-stu-id="97c0c-157">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="97c0c-158">Brukere som prøver å registrere seg eller logge på området, vil opprette en ny forretningsforbindelsesoppføring i den standard eller nylig tilknyttede B2C-leieren som er konfigurert for kanalen på området.</span><span class="sxs-lookup"><span data-stu-id="97c0c-158">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>

## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="97c0c-159">Konfigurere kanalen med en B2C-leier</span><span class="sxs-lookup"><span data-stu-id="97c0c-159">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="97c0c-160">Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="97c0c-160">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="97c0c-161">Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="97c0c-161">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="97c0c-162">Velg **Kanaler**, og velg deretter kanalen som skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="97c0c-162">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="97c0c-163">I egenskaper-ruten til høyre i feltet **Velg B2C-program** velger du den konfigurerte Azure AD B2C-leieren som skal brukes for denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="97c0c-163">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="97c0c-164">Velg **Lagre og publiser** på kommandolinjen for å utføre den nye eller oppdaterte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="97c0c-164">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="97c0c-165">Hvis du endrer B2C-programmet som er tilordnet til kanalen, fjerner du de gjeldende referansene som er opprettet for alle brukere som allerede har registrert seg i miljøet.</span><span class="sxs-lookup"><span data-stu-id="97c0c-165">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="97c0c-166">I dette tilfellet vil ingen legitimasjoner som er knyttet til det tilordnede B2C-programmet, være tilgjengelig for brukerne.</span><span class="sxs-lookup"><span data-stu-id="97c0c-166">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="97c0c-167">Derfor kan du bare endre en Azure AD B2C-konfigurasjon hvis du konfigurerer kanalen for første gang, og ingen brukere har muligheten til å registrere seg.</span><span class="sxs-lookup"><span data-stu-id="97c0c-167">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="97c0c-168">Hvis ikke kan det hende at brukerne må registrere seg på nytt for å opprette en post i den nye Azure AD B2C-leieren.</span><span class="sxs-lookup"><span data-stu-id="97c0c-168">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="97c0c-169">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="97c0c-169">Additional resources</span></span>

[<span data-ttu-id="97c0c-170">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="97c0c-170">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="97c0c-171">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="97c0c-171">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="97c0c-172">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="97c0c-172">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="97c0c-173">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="97c0c-173">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="97c0c-174">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="97c0c-174">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="97c0c-175">Laste opp masseomdirigeringer for URL-adresse</span><span class="sxs-lookup"><span data-stu-id="97c0c-175">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="97c0c-176">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="97c0c-176">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="97c0c-177">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="97c0c-177">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="97c0c-178">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="97c0c-178">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="97c0c-179">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="97c0c-179">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

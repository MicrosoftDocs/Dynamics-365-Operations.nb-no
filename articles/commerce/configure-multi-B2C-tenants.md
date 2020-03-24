---
title: Konfigurere flere B2C-leiere i et Commerce-miljø
description: Dette emnet beskriver når og hvordan du definerer flere per kanals Microsoft Azure Active Directory (Azure AD) B2C-leiere for brukergodkjenning i et dedikert Dynamics 365 Commerce-miljø.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6ca48badbe15b7e1bf543716a9b0e3da31477a20
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096520"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="2e7f8-103">Konfigurere flere B2C-leiere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="2e7f8-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2e7f8-104">Dette emnet beskriver når og hvordan du definerer flere per kanals Microsoft Azure Active Directory (Azure AD) B2C-leiere for brukergodkjenning i et dedikert Dynamics 365 Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="2e7f8-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="2e7f8-105">Overview</span></span>

<span data-ttu-id="2e7f8-106">Dynamics 365 Commerce bruker identitetstjenesten Azure AD B2C til å støtte brukerlegitimasjon og godkjenningsflyt.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-106">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="2e7f8-107">Brukere kan bruke godkjenningsflyt til å registrere seg, logge inn og tilbakestille passordet.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-107">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="2e7f8-108">Azure AD B2C lagrer sensitiv brukergodkjenningsinformasjon, for eksempel brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-108">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="2e7f8-109">Brukerposten er unik for hver B2C-leier og bruker enten brukernavn (e-postadresse) eller legitimasjon for sosial identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-109">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="2e7f8-110">I de fleste tilfeller brukes en enkelt Azure AD B2C-leier i et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-110">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="2e7f8-111">Commerce-kunder kan deretter opprette og publisere flere områder i samme Commerce-miljø, og samme kundelegitimasjon vil bli brukt på tvers av disse områdene.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-111">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="2e7f8-112">Hvis imidlertid områdene i miljøet skal behandles som ulike merker og vises for brukere som separate firmaer, kan en B2C-leier konfigureres for kanalen som brukes for området/merke-skillet.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-112">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="2e7f8-113">Betraktninger når flere B2C-leiere settes opp per kanal</span><span class="sxs-lookup"><span data-stu-id="2e7f8-113">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="2e7f8-114">Når hver kanal eller hvert område behandles som et separat firma, er det ofte best å bruke egne juridiske enheter med hensyn til brukergodkjenningsflyter i Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-114">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="2e7f8-115">Hvis du imidlertid vil beholde hver kanal/hvert område i samme miljø og juridisk enhet, men vil ha separate brukergodkjenninger for hvert område, er det viktig at du vurderer følgende punkter før du fortsetter:</span><span class="sxs-lookup"><span data-stu-id="2e7f8-115">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="2e7f8-116">Brukerne vil ha egne legitimasjonsbeskrivelser for hver kanal/hvert område.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-116">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="2e7f8-117">Samme person kan ha to separate kontoer per kanal/område, fordi hver konto vil være en unik oppføring i en separat B2C-leier.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-117">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="2e7f8-118">I Microsoft Dynamics-miljøet returneres separate kundeoppføringer for søk etter globale poster.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-118">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="2e7f8-119">Hvis en bruker bruker samme e-postadresse på tvers av kanaler/områder, returnerer det globale kundesøket resultater for hver kanal/hvert område.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-119">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="2e7f8-120">(Det vises en kanalindikator.)</span><span class="sxs-lookup"><span data-stu-id="2e7f8-120">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="2e7f8-121">Adresseboken kan brukes til å gruppere brukere, slik at de kan spores per kanal.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-121">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="2e7f8-122">Antallet kundeposter per kanal kan øke, og denne økningen kan påvirke ytelsen til globale kundesøk.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-122">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="2e7f8-123">B2C-leiere må nøye tilordnes til en kanal for å hindre situasjoner der kunder registrerer seg for å finne en feil leier.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-123">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="2e7f8-124">Ellers kan forvirring eller sporingsproblemer oppstå.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-124">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="2e7f8-125">Følgende illustrasjon viser flere B2C-leiere i et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-125">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Flere B2C-leiere i et Commerce-miljø](media/MultiB2C_In_Environment.png)

<span data-ttu-id="2e7f8-127">Hvis du finner ut at bedriften krever forskjellige B2C-leiere per kanal i samme Commerce-miljø, må du utføre fremgangsmåtene i de følgende delene for å be om denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-127">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="2e7f8-128">Be om at B2C per kanal aktiveres i miljøet ditt</span><span class="sxs-lookup"><span data-stu-id="2e7f8-128">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="2e7f8-129">Hvis du vil at forskjellige B2C-leiere per kanal skal være tilgjengelige i det samme Commerce-miljøet, må du sende en forespørsel til Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-129">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="2e7f8-130">Hvis du vil ha mer informasjon, se [Få kundestøtte for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), eller diskuter dette problemet med Commerce-løsningskontakten.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-130">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="2e7f8-131">Konfigurere B2C-leiere i ditt miljø</span><span class="sxs-lookup"><span data-stu-id="2e7f8-131">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="2e7f8-132">Hvis du vil konfigurere B2C-leiere i miljøet ditt, fullfører du de relevante fremgangsmåtene i denne delen.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-132">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="2e7f8-133">Legge til en Azure AD B2C-leier</span><span class="sxs-lookup"><span data-stu-id="2e7f8-133">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="2e7f8-134">Følg denne fremgangsmåten for å legge til en Azure AD B2C-leier i miljøet.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-134">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="2e7f8-135">Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-135">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="2e7f8-136">Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-136">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="2e7f8-137">Velg **B2C-innstillinger**, og velg deretter **Behandle**.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-137">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="2e7f8-138">Velg **Legg til B2C-program**, og angi deretter følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="2e7f8-138">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="2e7f8-139">**Programnavn**: Angi navnet som skal brukes for programmet i konteksten for administrasjon av det i Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-139">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="2e7f8-140">Vi anbefaler at du bruker programnavnet du valgte da du konfigurerte Azure AD B2C-programmet i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-140">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="2e7f8-141">På denne måten kan du bidra til å redusere forvirring når du administrerer B2C-leiere i Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-141">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="2e7f8-142">**Navn på leietaker**: Angi navnet på B2C-leieren slik det vises i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-142">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="2e7f8-143">**Policy-ID for glemt passord**: Angi policy-IDen (navnet på policyen i Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="2e7f8-143">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="2e7f8-144">**Policy-ID for registrering/pålogging**: Angi policy-IDen (navnet på policyen i Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="2e7f8-144">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="2e7f8-145">**Klient-GUID**: Angi Azure AD B2C-leier-IDen slik den vises i Azure-portalen (ikke program-IDen for B2C-leieren).</span><span class="sxs-lookup"><span data-stu-id="2e7f8-145">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="2e7f8-146">**Policy-ID for redigering av profil**: Angi policy-IDen (navnet på policyen i Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="2e7f8-146">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="2e7f8-147">Når du er ferdig med å angi denne informasjonen, velger du **OK** for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-147">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="2e7f8-148">Du bør la felt som **Omfang**, **Ikke-interaktiv policy-ID**, **Ikke-interaktiv klient-ID**, **Egendefinert domene for pålogging** og **Policy-ID for registrering** stå tomme, med mindre Dynamics 365 Commerce-teamet instruerer deg om å angi dem.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-148">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="2e7f8-149">Den nye Azure AD B2C-leieren skal nå vises i listen under **Behandle B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-149">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="2e7f8-150">Administrere eller slette en Azure AD B2C-leier</span><span class="sxs-lookup"><span data-stu-id="2e7f8-150">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="2e7f8-151">Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-151">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="2e7f8-152">Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-152">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="2e7f8-153">Velg **B2C-innstillinger**, og velg deretter **Behandle**.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-153">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="2e7f8-154">Hvis du vil redigere en B2C-leier, velger du blyantsymbolet ved siden av den.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-154">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="2e7f8-155">Hvis du vil slette en B2C-leier, velger du papirkurvsymbolet ved siden av.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-155">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="2e7f8-156">Velg **Lagre**, og velg deretter **Publiser** for å aktivere endringene.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-156">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="2e7f8-157">Når en B2C-leier er konfigurert for et aktivt/publisert område, kan brukere ha registrert seg ved å bruke kontoer som finnes på leieren.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-157">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="2e7f8-158">Hvis du sletter en konfigurert leier på menyen **Leierinnstillinger \> B2C-leier**, fjerner du tilknytningen av B2C-leieren fra områder som er knyttet til en hvilken som helst kanal i leieren.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-158">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="2e7f8-159">I dette tilfellet kan det hende at brukerne ikke lenger kan logge på kontoene sine.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-159">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="2e7f8-160">Vær derfor svært forsiktig når du sletter en konfigurert leier.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-160">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="2e7f8-161">Når en konfigurert leier slettes, vil B2C-leieren og -postene fortsatt bli opprettholdt, men Commerce-systemkonfigurasjonen for denne leieren vil bli endret eller fjernet.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-161">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="2e7f8-162">Brukere som prøver å registrere seg eller logge på området, vil opprette en ny forretningsforbindelsesoppføring i den standard eller nylig tilknyttede B2C-leieren som er konfigurert for kanalen på området.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-162">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="2e7f8-163">Konfigurere kanalen med en B2C-leier</span><span class="sxs-lookup"><span data-stu-id="2e7f8-163">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="2e7f8-164">Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-164">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="2e7f8-165">Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-165">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="2e7f8-166">Velg **Kanaler**, og velg deretter kanalen som skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-166">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="2e7f8-167">I egenskaper-ruten til høyre i feltet **Velg B2C-program** velger du den konfigurerte Azure AD B2C-leieren som skal brukes for denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-167">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="2e7f8-168">Velg **Lagre og publiser** på kommandolinjen for å utføre den nye eller oppdaterte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-168">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="2e7f8-169">Hvis du endrer B2C-programmet som er tilordnet til kanalen, fjerner du de gjeldende referansene som er opprettet for alle brukere som allerede har registrert seg i miljøet.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-169">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="2e7f8-170">I dette tilfellet vil ingen legitimasjoner som er knyttet til det tilordnede B2C-programmet, være tilgjengelig for brukerne.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-170">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="2e7f8-171">Derfor kan du bare endre en Azure AD B2C-konfigurasjon hvis du konfigurerer kanalen for første gang, og ingen brukere har muligheten til å registrere seg.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-171">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="2e7f8-172">Hvis ikke kan det hende at brukerne må registrere seg på nytt for å opprette en post i den nye Azure AD B2C-leieren.</span><span class="sxs-lookup"><span data-stu-id="2e7f8-172">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="2e7f8-173">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2e7f8-173">Additional resources</span></span>

[<span data-ttu-id="2e7f8-174">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="2e7f8-174">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="2e7f8-175">Distribuere et nytt e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="2e7f8-175">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="2e7f8-176">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="2e7f8-176">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="2e7f8-177">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="2e7f8-177">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="2e7f8-178">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="2e7f8-178">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="2e7f8-179">Laste opp URL-adresser for omadressering samtidig</span><span class="sxs-lookup"><span data-stu-id="2e7f8-179">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="2e7f8-180">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="2e7f8-180">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="2e7f8-181">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="2e7f8-181">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="2e7f8-182">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="2e7f8-182">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="2e7f8-183">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="2e7f8-183">Enable location-based store detection</span></span>](enable-store-detection.md)

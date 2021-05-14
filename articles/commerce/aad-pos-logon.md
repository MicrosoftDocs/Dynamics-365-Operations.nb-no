---
title: Konfigurere Azure Active Directory-godkjenning for salgsstedspålogging
description: Dette emnet beskriver hvordan du konfigurerer Azure Active Directory som godkjenningsmetoden på Microsoft Dynamics 365 Commerce-salgsstedet.
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937464"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="75bde-103">Konfigurere Azure Active Directory-godkjenning for salgsstedspålogging</span><span class="sxs-lookup"><span data-stu-id="75bde-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="75bde-104">Dette emnet beskriver hvordan du konfigurerer Azure Active Directory (Azure AD) som godkjenningsmetoden på Microsoft Dynamics 365 Commerce-salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="75bde-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="75bde-105">Forhandlere som bruker Dynamics 365 Commerce sammen med andre Microsoft-skytjenester, for eksempel Microsoft Azure, Microsoft 365 og Microsoft Teams, vil vanligvis bruke Azure AD til sentralisert behandling av brukerlegitimasjonen for å få en sikker og sømløs påloggingsopplevelse på tvers av programmer.</span><span class="sxs-lookup"><span data-stu-id="75bde-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="75bde-106">For å bruke Azure AD-godkjenning for Commerce POS, må du først konfigurere Azure AD som godkjenningsmetode i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="75bde-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="75bde-107">Konfigurere godkjenningsmetode for salgssted</span><span class="sxs-lookup"><span data-stu-id="75bde-107">Configure POS authentication method</span></span>

<span data-ttu-id="75bde-108">Følg denne fremgangsmåten for å konfigurere godkjenningsmetode på salgssted i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="75bde-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="75bde-109">Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonsprofiler**, og velg funksjonalitetsprofil for å endre.</span><span class="sxs-lookup"><span data-stu-id="75bde-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="75bde-110">Velg et alternativ for ønsket godkjenningsmetode fra rullegardinlisten **Metode for påloggingsgodkjenning** i hurtigkategorien **Funksjoner** i delen **Stabspålogging på salgssted**.</span><span class="sxs-lookup"><span data-stu-id="75bde-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="75bde-111">**Metode for påloggingsgodkjenning** har tre alternativer:</span><span class="sxs-lookup"><span data-stu-id="75bde-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="75bde-112">**Personal-ID og passord** - Dette standardalternativet krever at POS-brukere angir en personal-ID og passord for å logge seg på salgsstedet, og at lederen skal overstyre funksjonene.</span><span class="sxs-lookup"><span data-stu-id="75bde-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="75bde-113">**Azure AD uten enkel pålogging** – Dette alternativet krever at POS-brukere bruker Azure AD-legitimasjon for å logge seg på salgsstedet og få tilgang til funksjonaliteten for lederoverstyring.</span><span class="sxs-lookup"><span data-stu-id="75bde-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="75bde-114">Når salgsstedsklienten oppdateres eller åpnes på nytt, må salgsstedsbrukeren angi Azure AD-legitimasjonen for å kunne logge seg på igjen.</span><span class="sxs-lookup"><span data-stu-id="75bde-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="75bde-115">**Azure AD med enkel pålogging** – Når dette alternativet er valgt, kan POS-brukere logge seg på Cloud POS (CPOS) med aktiv Azure AD-legitimasjon som brukes av andre webprogrammer i den samme webleseren, eller logge seg på Modern POS (MPOS) med Azure AD-legitimasjon som er logget på Windows.</span><span class="sxs-lookup"><span data-stu-id="75bde-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="75bde-116">Begge metodene tillater pålogging uten at du trenger å angi Azure AD-legitimasjon på påloggingsskjermen for salgssted.</span><span class="sxs-lookup"><span data-stu-id="75bde-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="75bde-117">Tilgangen til overstyringsfunksjonaliteten i POS-behandling vil imidlertid fortsatt kreve at du logger deg på med Azure AD-legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="75bde-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="75bde-118">Gå til **Retail og Commerce > IT for Retail og Commerce > Distribusjonsplan**, og kjør jobben **1070 (Kanalkonfigurasjon)** for å synkronisere de nyeste innstillingene for funksjonalitetsprofilen til POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="75bde-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="75bde-119">Alternativet for godkjenningsmetode **Azure AD uten enkel pålogging** erstatter alternativet **Azure Active Directory** i Commerce-versjon 10.0.18 og tidligere.</span><span class="sxs-lookup"><span data-stu-id="75bde-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="75bde-120">Azure AD-godkjenning krever en aktiv Internett-tilkobling og vil ikke fungere når salgsstedet er frakoblet.</span><span class="sxs-lookup"><span data-stu-id="75bde-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="75bde-121">Knytte Azure AD-kontoer til salgsstedsbrukere</span><span class="sxs-lookup"><span data-stu-id="75bde-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="75bde-122">For å bruke Azure AD som godkjenningsmetode for salgssted, må du knytte Azure AD-kontoer til salgsstedsbrukere i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="75bde-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="75bde-123">Følg denne fremgangsmåten for å knytte kontoer for Azure AD til salgsstedsbrukere i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="75bde-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="75bde-124">Gå til **Retail og Commerce > Ansatte > Arbeidere**, og åpne en arbeiderpost.</span><span class="sxs-lookup"><span data-stu-id="75bde-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="75bde-125">I handlingsruten velger du kategorien **Commerce** og deretter under **Ekstern identitet** velger du **Tilknytt eksisterende ID**.</span><span class="sxs-lookup"><span data-stu-id="75bde-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="75bde-126">I dialogboksen **Bruk eksisterende eksterne ID** velger du **Søk ved hjelp av e-post**, angir en Azure AD-e-postadresse og velger **Søk**.</span><span class="sxs-lookup"><span data-stu-id="75bde-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="75bde-127">Velg den returnerte Azure AD-kontoen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="75bde-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="75bde-128">Etter konfigurasjonstrinnene over vil feltene **Alias**, **UPN** og **Ekstern underidentifikator** i kategorien **Commerce** på arbeiderens detaljside fylles ut.</span><span class="sxs-lookup"><span data-stu-id="75bde-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="75bde-129">Du må kjøre **1060 (Stab)** i **Retail og Commerce > Retail og Commerce IT > Distribusjonsplan** for å synkronisere den siste salgsstedsbrukeren og Azure AD-kontodataene til kanalen.</span><span class="sxs-lookup"><span data-stu-id="75bde-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="75bde-130">Det er en anbefalt fremgangsmåte, etter at arbeiderinformasjon som passord, POS-tillatelse, tilknyttet Azure AD-konto eller adressebok for ansatt er oppdatert i Commerce Headquarters, at du kjører **1060 (stab)** for å synkronisere den nyeste arbeiderinformasjonen til kanalen.</span><span class="sxs-lookup"><span data-stu-id="75bde-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="75bde-131">Salgsstedsklienten kan deretter hente de riktige dataene for brukergodkjenning og godkjenningskontroller.</span><span class="sxs-lookup"><span data-stu-id="75bde-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="75bde-132">Låsregistrering og -utlogging for salgssted med Azure AD-godkjenning</span><span class="sxs-lookup"><span data-stu-id="75bde-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="75bde-133">Følgende skjer når salgsstedet er konfigurert til å bruke Azure AD-godkjenningsmetoden:</span><span class="sxs-lookup"><span data-stu-id="75bde-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="75bde-134">Funksjonen for **Lås kasse** er ikke tilgjengelig i salgsstedsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="75bde-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="75bde-135">**Automatisk lås**-funksjonen vil fungere som **Automatisk avlogging**-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="75bde-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="75bde-136">Hvis salgsstedsbrukeren velger **Logg av**, blir brukeren bedt om å logge seg på med Azure AD-legitimasjon neste gang salgsstedet starter, uansett om en enkel pålogging er aktivert.</span><span class="sxs-lookup"><span data-stu-id="75bde-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="75bde-137">Funksjonalitet for Lederoverstyring med Azure AD-godkjenning</span><span class="sxs-lookup"><span data-stu-id="75bde-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="75bde-138">Når salgsstedet er konfigurert til å bruke Azure AD-godkjenning, vil funksjonalitete for lederoverstyring åpne en dialogboks som ber lederbrukeren om Azure AD-legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="75bde-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="75bde-139">Når lederpålogging er godkjent, blir lederens Azure AD-legitimasjon slettet, og den forrige brukerens Azure AD-legitimasjon blir brukt for påfølgende salgsstedsoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="75bde-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="75bde-140">I Commerce-versjoner 10.0.18 og tidligere støtter ikke funksjonen for lederoverstyring Azure AD.</span><span class="sxs-lookup"><span data-stu-id="75bde-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="75bde-141">En personell-ID og -passord kreves selv om salgsstedet er konfigurert til å bruke Azure AD-godkjenningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="75bde-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="75bde-142">Når du bruker CPOS med Safari-webeseren på en Apple iOS-enhet, må du først slå av **Blokker popup-vinduer** i Safari-innstillinger for at funksjonen for lederoverstyring skal fungerer med Azure AD-godkjenning.</span><span class="sxs-lookup"><span data-stu-id="75bde-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="75bde-143">Anbefalte fremgangsmåter for sikkerhet for Azure AD-basert salgsstedsgodkjenning på delte enheter</span><span class="sxs-lookup"><span data-stu-id="75bde-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="75bde-144">Mange forhandlere konfigurerer butikkmiljøet på en måte som gjør det nødvendig for flere brukere å få tilgang til salgsstedsprogrammet fra en delt fysisk enhet.</span><span class="sxs-lookup"><span data-stu-id="75bde-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="75bde-145">I den sammenhengen kan det, selv om enkel pålogging gir en nyttig og sømløs godkjenningsopplevelse, også føre til at det opprettes sikkerhetshull der den gjeldende salgsstedsbrukeren ikke innser at en annen brukers legitimasjon brukes til å utføre transaksjoner eller operasjoner på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="75bde-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="75bde-146">Før du konfigurerer salgsstedssystemet for å bruke Azure AD-godkjenningsmetoden anbefales det på det sterkeste at du går gjennom sikkerhetspolicyen og den delte enhetens påloggingsinnstillinger for å avgjøre hvilket alternativ som passer best.</span><span class="sxs-lookup"><span data-stu-id="75bde-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="75bde-147">Hvis detaljhandelsmiljøet bruker en delt konto (for eksempel en lokal konto) for fysisk enhetspålogging, anbefales det å bruke alternativet **Azure AD uten enkel pålogging**.</span><span class="sxs-lookup"><span data-stu-id="75bde-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="75bde-148">Dette sikrer at hver salgsstedsbruker eksplisitt angir legitimasjon for Azure AD for å logge seg på salgsstedsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="75bde-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="75bde-149">Hvis detaljhandelsmiljøet krever at ansatte bruker sine egne Azure AD-kontoer for å logge seg på salgsstedssystemet og er vert for den fysiske enheten, anbefales det å bruke alternativet **Azure AD med enkel pålogging**.</span><span class="sxs-lookup"><span data-stu-id="75bde-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75bde-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="75bde-150">Additional resources</span></span>

[<span data-ttu-id="75bde-151"> Konfigurere en arbeider</span><span class="sxs-lookup"><span data-stu-id="75bde-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="75bde-152">Opprette en funksjonalitetsprofil for Retail</span><span class="sxs-lookup"><span data-stu-id="75bde-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="75bde-153">Definere funksjonalitet for utvidet pålogging MPOS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="75bde-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="75bde-154">Anbefalte fremgangsmåter for Cloud POS i delte miljøer</span><span class="sxs-lookup"><span data-stu-id="75bde-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

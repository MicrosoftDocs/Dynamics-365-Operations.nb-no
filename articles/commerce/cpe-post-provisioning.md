---
title: Konfigurere et miljø for forhåndsvisning av Commerce
description: Dette emnet forklarer hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø etter klargjøring.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906145"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="657ea-103">Konfigurere et miljø for forhåndsvisning av Commerce</span><span class="sxs-lookup"><span data-stu-id="657ea-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="657ea-104">Dette emnet forklarer hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljø etter klargjøring.</span><span class="sxs-lookup"><span data-stu-id="657ea-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="657ea-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="657ea-105">Overview</span></span>

<span data-ttu-id="657ea-106">Fullfør prosedyrene i dette emnet bare etter at forhåndsvisningsmiljøet i Commerce er klargjort.</span><span class="sxs-lookup"><span data-stu-id="657ea-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="657ea-107">Hvis du vil ha informasjon om hvordan du klargjør Commerce-forhåndsvisningsmiljøet, kan du se [Klargjøre et Commerce-forhåndsvisningsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="657ea-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="657ea-108">Når forhåndsvisningsmiljøet i Commerce er klargjort ende til ende, må du fullføre flere trinn etter klargjøring før du kan begynne å evaluere miljøet.</span><span class="sxs-lookup"><span data-stu-id="657ea-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="657ea-109">Hvis du vil fullføre disse trinnene, må du bruke Microsoft Dynamics Lifecycle Services (LCS, Dynamics 365 Commerce) og Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="657ea-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="657ea-110">Før du starter</span><span class="sxs-lookup"><span data-stu-id="657ea-110">Before you start</span></span>

1. <span data-ttu-id="657ea-111">Logg på [LCS-portalen](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="657ea-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="657ea-112">Gå til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="657ea-112">Go to your project.</span></span>
1. <span data-ttu-id="657ea-113">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="657ea-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="657ea-114">Velg miljøet fra listen.</span><span class="sxs-lookup"><span data-stu-id="657ea-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="657ea-115">Klikk **Detaljerte opplysninger** i miljøinformasjonen til høyre.</span><span class="sxs-lookup"><span data-stu-id="657ea-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="657ea-116">Klikk **Pålogging** for å åpne en meny, og velg **Logg på miljøet**.</span><span class="sxs-lookup"><span data-stu-id="657ea-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="657ea-117">Kontroller at den juridiske enheten **USRT** er valgt i øvre høyre hjørne.</span><span class="sxs-lookup"><span data-stu-id="657ea-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="657ea-118">Konfigurere salgsstedet i LCS</span><span class="sxs-lookup"><span data-stu-id="657ea-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="657ea-119">Knytt en arbeider til din identitet</span><span class="sxs-lookup"><span data-stu-id="657ea-119">Associate a worker with your identity</span></span>

<span data-ttu-id="657ea-120">Hvis du vil knytte en arbeider med identiteten din i LCS, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="657ea-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="657ea-121">Bruk menyen til venstre, og gå til **Moduler \> Detaljhandel \> Ansatte \> Arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="657ea-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="657ea-122">Finn og velg følgnede post i listen **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="657ea-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="657ea-123">Velg **Detaljhandel** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="657ea-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="657ea-124">Velg **Tilknytt eksisterende ID**.</span><span class="sxs-lookup"><span data-stu-id="657ea-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="657ea-125">I feltet **E-post** (til høyre for **Søk ved hjelp av e-post**) skriver du inn e-postadressen din.</span><span class="sxs-lookup"><span data-stu-id="657ea-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="657ea-126">Velg **Søk**.</span><span class="sxs-lookup"><span data-stu-id="657ea-126">Select **Search**.</span></span>
1. <span data-ttu-id="657ea-127">Velg posten med navnet ditt.</span><span class="sxs-lookup"><span data-stu-id="657ea-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="657ea-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="657ea-128">Select **OK**.</span></span>
1. <span data-ttu-id="657ea-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="657ea-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="657ea-130">Aktivere Skysalgssted</span><span class="sxs-lookup"><span data-stu-id="657ea-130">Activate Cloud POS</span></span>

<span data-ttu-id="657ea-131">Hvis du vil aktivere Cloud POS i LCS, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="657ea-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="657ea-132">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="657ea-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="657ea-133">Velg miljøet fra listen.</span><span class="sxs-lookup"><span data-stu-id="657ea-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="657ea-134">Klikk **Detaljerte opplysninger** i miljøinformasjonen til høyre.</span><span class="sxs-lookup"><span data-stu-id="657ea-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="657ea-135">Velg **Logg inn** for å åpne en meny, og velg deretter **Logg på Cloud Point of Sale** for å åpne salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="657ea-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="657ea-136">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="657ea-136">Select **Next**.</span></span>
1. <span data-ttu-id="657ea-137">Logg på ved hjelp av Microsoft Azure Active Directory (Azure AD)-kontoen din.</span><span class="sxs-lookup"><span data-stu-id="657ea-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="657ea-138">Under **Butikknavn** velger du **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="657ea-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="657ea-139">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="657ea-139">Select **Next**.</span></span>
1. <span data-ttu-id="657ea-140">Under **Register og enhet** velger du **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="657ea-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="657ea-141">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="657ea-141">Select **Activate**.</span></span> <span data-ttu-id="657ea-142">Du er logget av og tatt til påloggingssiden for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="657ea-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="657ea-143">Du kan nå logge på Cloud POS-opplevelsen ved hjelp av operatør-ID-en **000713** og passordet **123**.</span><span class="sxs-lookup"><span data-stu-id="657ea-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="657ea-144">Konfigurere området i Commerce</span><span class="sxs-lookup"><span data-stu-id="657ea-144">Set up your site in Commerce</span></span>

<span data-ttu-id="657ea-145">Følg denne fremgangsmåten for å begynne å konfigurere forhåndsvisningsområdet i Commerce.</span><span class="sxs-lookup"><span data-stu-id="657ea-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="657ea-146">Logg på områdebehandlingsverktøyet ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="657ea-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="657ea-147">Klikk på **Fabrikam**-området for å åpne dialogboksen for områdeoppsett.</span><span class="sxs-lookup"><span data-stu-id="657ea-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="657ea-148">Velg domenet du angav da du startet e-handel.</span><span class="sxs-lookup"><span data-stu-id="657ea-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="657ea-149">Velg **Fabrikam-utvidet nettbutikk** for standardkanal.</span><span class="sxs-lookup"><span data-stu-id="657ea-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="657ea-150">(Pass på at du velger den **utvidede** nettbutikken.)</span><span class="sxs-lookup"><span data-stu-id="657ea-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="657ea-151">Velg **nb-no** for standardspråk.</span><span class="sxs-lookup"><span data-stu-id="657ea-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="657ea-152">Behold verdien i **Bane**-feltet slik det er.</span><span class="sxs-lookup"><span data-stu-id="657ea-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="657ea-153">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="657ea-153">Select **OK**.</span></span> <span data-ttu-id="657ea-154">Listen over sider på området vises.</span><span class="sxs-lookup"><span data-stu-id="657ea-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="657ea-155">Aktivere jobber i detaljhandel</span><span class="sxs-lookup"><span data-stu-id="657ea-155">Enable jobs in Retail</span></span>

<span data-ttu-id="657ea-156">Følg disse trinnene for å aktivere jobber i detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="657ea-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="657ea-157">Logg på miljøet (hovedkontor).</span><span class="sxs-lookup"><span data-stu-id="657ea-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="657ea-158">Gå til **Detaljhandel \> Forespørsler og rapporter \> Satsvise jobber** ved hjelp av menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="657ea-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="657ea-159">De resterende trinnene i denne prosedyren må fullføres for hver av følgende jobber:</span><span class="sxs-lookup"><span data-stu-id="657ea-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="657ea-160">Behandle e-postvarsling for detaljistordre</span><span class="sxs-lookup"><span data-stu-id="657ea-160">Process retail order email notification</span></span>
    * <span data-ttu-id="657ea-161">Produkttilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="657ea-161">Product availability</span></span>
    * <span data-ttu-id="657ea-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="657ea-162">P-0001</span></span>
    * <span data-ttu-id="657ea-163">Synkroniser ordrejobb</span><span class="sxs-lookup"><span data-stu-id="657ea-163">Synchronize orders job</span></span>

1. <span data-ttu-id="657ea-164">Bruk hurtigfilteret til å søke etter jobben ved hjelp av navnet.</span><span class="sxs-lookup"><span data-stu-id="657ea-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="657ea-165">Hvis statusen for jobben er **Trekk tilbake**, utfører du følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="657ea-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="657ea-166">Velg posten.</span><span class="sxs-lookup"><span data-stu-id="657ea-166">Select the record.</span></span>
    1. <span data-ttu-id="657ea-167">Velg **Endre status** i kategorien **Satsvis jobb** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="657ea-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="657ea-168">Velg **Venter**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="657ea-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="657ea-169">Kjøre fullstendig datasynkronisering i detaljhandel</span><span class="sxs-lookup"><span data-stu-id="657ea-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="657ea-170">Hvis du vil kjøre full datasynkronisering i detaljhandel, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="657ea-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="657ea-171">Bruk menyen til venstre og gå til **Moduler \> Detaljhandel \> Hovedkvarteroppsett \> Detaljhandel Planlegger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="657ea-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="657ea-172">**Standard**-kanalen velges fra listen til venstre.</span><span class="sxs-lookup"><span data-stu-id="657ea-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="657ea-173">Velg den andre tilgjengelige kanalen.</span><span class="sxs-lookup"><span data-stu-id="657ea-173">Select the other available channel.</span></span> <span data-ttu-id="657ea-174">Denne kanalen heter **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="657ea-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="657ea-175">I handlingsruten velger du **Fullstendig datasynkronisering**.</span><span class="sxs-lookup"><span data-stu-id="657ea-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="657ea-176">Angi **9999** som distribusjonsplan.</span><span class="sxs-lookup"><span data-stu-id="657ea-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="657ea-177">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="657ea-177">Select **OK**.</span></span>
1. <span data-ttu-id="657ea-178">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="657ea-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="657ea-179">Teste kredittkortinformasjon for å utføre testinnkjøp</span><span class="sxs-lookup"><span data-stu-id="657ea-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="657ea-180">Hvis du skal utføre testtransaksjoner på området, kan du bruke denne testkredittkortinformasjonen:</span><span class="sxs-lookup"><span data-stu-id="657ea-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="657ea-181">**Kortnummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="657ea-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="657ea-182">**Utløpsdato:** 10/20</span><span class="sxs-lookup"><span data-stu-id="657ea-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="657ea-183">**Verdi for kortbekreftelse (CVV-kode):** 737</span><span class="sxs-lookup"><span data-stu-id="657ea-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="657ea-184">Du bør ikke prøve å bruke faktisk kredittkortinformasjon på testområdet under noen omstendigheter!</span><span class="sxs-lookup"><span data-stu-id="657ea-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="657ea-185">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="657ea-185">Next steps</span></span>

<span data-ttu-id="657ea-186">Når klargjøringen og konfigurasjonstrinnene er fullført, er du klar til å evaluere forhåndsvisningsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="657ea-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="657ea-187">Bruk URL-adressen for verktøyet for administrasjon av handelsområde til å gå til redigeringsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="657ea-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="657ea-188">Bruk URL-adressen for verktøyet for e-handelsområdet til å gå til kundeområdet for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="657ea-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="657ea-189">Hvis du vil konfigurere valgfrie funksjoner for Commerce-forhåndsvisningsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="657ea-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="657ea-190">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="657ea-190">Additional resources</span></span>

[<span data-ttu-id="657ea-191">Oversikt over Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="657ea-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="657ea-192">Klargjøre et Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="657ea-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="657ea-193">Konfigurere valgfrie funksjoner for et Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="657ea-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="657ea-194">Vanlige spørsmål for Commerce-forhåndsvisningsmiljø</span><span class="sxs-lookup"><span data-stu-id="657ea-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="657ea-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="657ea-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="657ea-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="657ea-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="657ea-197">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="657ea-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="657ea-198">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="657ea-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="657ea-199">Hjelperessurser for Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="657ea-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)

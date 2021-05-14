---
title: Konfigurere et evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du konfigurerer et evalueringsmiljø i Microsoft Dynamics 365 Commerce etter klargjøring.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b291a6515c6a3ae7382ea2ad8024ca036489de19
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937044"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="ad142-103">Konfigurere et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ad142-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad142-104">Dette emnet forklarer hvordan du konfigurerer et evalueringsmiljø i Microsoft Dynamics 365 Commerce etter klargjøring.</span><span class="sxs-lookup"><span data-stu-id="ad142-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="ad142-105">Fullfør prosedyrene i dette emnet bare etter at evalueringsmiljøet i Commerce er klargjort.</span><span class="sxs-lookup"><span data-stu-id="ad142-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="ad142-106">Hvis du vil ha informasjon om hvordan du klargjør Commerce-evalueringsmiljøet, kan du se [Klargjøre et Commerce-evalueringsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="ad142-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="ad142-107">Når evalueringsmiljøet i Commerce er klargjort ende til ende, må du fullføre flere trinn etter klargjøring før du kan begynne å evaluere miljøet.</span><span class="sxs-lookup"><span data-stu-id="ad142-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="ad142-108">Hvis du vil fullføre disse trinnene, må du bruke Microsoft Dynamics Lifecycle Services (LCS, ) og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad142-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="ad142-109">Før du starter</span><span class="sxs-lookup"><span data-stu-id="ad142-109">Before you start</span></span>

1. <span data-ttu-id="ad142-110">Logg på [LCS-portalen](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="ad142-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="ad142-111">Gå til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="ad142-111">Go to your project.</span></span>
1. <span data-ttu-id="ad142-112">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="ad142-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="ad142-113">Velg miljøet fra listen.</span><span class="sxs-lookup"><span data-stu-id="ad142-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="ad142-114">Velg **Logg på miljøet** i miljøinformasjonen til høyre.</span><span class="sxs-lookup"><span data-stu-id="ad142-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="ad142-115">Du vil bli sendt til Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ad142-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="ad142-116">Kontroller at den juridiske enheten **USRT** er valgt i øvre høyre hjørne.</span><span class="sxs-lookup"><span data-stu-id="ad142-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="ad142-117">Under aktiviteter etter klargjøring i Commerce Headquarters må du kontrollere at den juridiske enheten **USRT** alltid er valgt.</span><span class="sxs-lookup"><span data-stu-id="ad142-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="ad142-118">Konfigurere salgsstedet</span><span class="sxs-lookup"><span data-stu-id="ad142-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="ad142-119">Knytt en arbeider til din identitet</span><span class="sxs-lookup"><span data-stu-id="ad142-119">Associate a worker with your identity</span></span>

<span data-ttu-id="ad142-120">Hvis du vil knytte en arbeider med identiteten din i Commerce Headquarters, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ad142-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="ad142-121">Bruk menyen til venstre, og gå til **Moduler \> Retail og Commerce \> Ansatte \> Arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="ad142-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="ad142-122">Finn og velg følgnede post i listen **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="ad142-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="ad142-123">Klikk **Commerce** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ad142-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="ad142-124">Velg **Tilknytt eksisterende ID**.</span><span class="sxs-lookup"><span data-stu-id="ad142-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="ad142-125">I feltet **E-post** (til høyre for **Søk ved hjelp av e-post**) skriver du inn e-postadressen din.</span><span class="sxs-lookup"><span data-stu-id="ad142-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="ad142-126">Velg **Søk**.</span><span class="sxs-lookup"><span data-stu-id="ad142-126">Select **Search**.</span></span>
1. <span data-ttu-id="ad142-127">Velg posten med navnet ditt.</span><span class="sxs-lookup"><span data-stu-id="ad142-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="ad142-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad142-128">Select **OK**.</span></span>
1. <span data-ttu-id="ad142-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ad142-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="ad142-130">Aktivere Skysalgssted</span><span class="sxs-lookup"><span data-stu-id="ad142-130">Activate Cloud POS</span></span>

<span data-ttu-id="ad142-131">Hvis du vil aktivere Cloud POS, følger du denne fremgangsmåten i LCS.</span><span class="sxs-lookup"><span data-stu-id="ad142-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="ad142-132">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="ad142-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="ad142-133">Velg miljøet fra listen.</span><span class="sxs-lookup"><span data-stu-id="ad142-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="ad142-134">Velg **Logg på Cloud Point of Sale** i miljøinformasjonen til høyre.</span><span class="sxs-lookup"><span data-stu-id="ad142-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="ad142-135">Velg **Neste** for å åpne dialogboksen **Før du starter**.</span><span class="sxs-lookup"><span data-stu-id="ad142-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="ad142-136">La **Server-URL**-feltet være slik det er.</span><span class="sxs-lookup"><span data-stu-id="ad142-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="ad142-137">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="ad142-137">Select **Next**.</span></span>
1. <span data-ttu-id="ad142-138">Logg på ved hjelp av Microsoft Azure Active Directory (Azure AD)-kontoen din.</span><span class="sxs-lookup"><span data-stu-id="ad142-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="ad142-139">Under **Butikknavn** velger du **San Francisco**, og deretter velger du **Neste**.</span><span class="sxs-lookup"><span data-stu-id="ad142-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="ad142-140">Under **Register og enhet** velger du **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="ad142-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="ad142-141">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="ad142-141">Select **Activate**.</span></span> <span data-ttu-id="ad142-142">Du er logget av og tatt til påloggingssiden for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="ad142-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="ad142-143">Du kan nå logge på Cloud POS-opplevelsen ved hjelp av operatør-ID-en **000713** og passordet **123**.</span><span class="sxs-lookup"><span data-stu-id="ad142-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="ad142-144">Konfigurere området i Commerce</span><span class="sxs-lookup"><span data-stu-id="ad142-144">Set up your site in Commerce</span></span>

<span data-ttu-id="ad142-145">Følg denne fremgangsmåten for å begynne å konfigurere evalueringsområdet i Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad142-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ad142-146">Logg på områdebyggeren ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="ad142-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="ad142-147">Klikk på **Fabrikam**-området for å åpne dialogboksen for områdeoppsett.</span><span class="sxs-lookup"><span data-stu-id="ad142-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="ad142-148">Velg domenet du angav da du startet e-handel.</span><span class="sxs-lookup"><span data-stu-id="ad142-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="ad142-149">Velg **Fabrikam-utvidet nettbutikk** for standardkanal.</span><span class="sxs-lookup"><span data-stu-id="ad142-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="ad142-150">(Pass på at du velger den **utvidede** nettbutikken.)</span><span class="sxs-lookup"><span data-stu-id="ad142-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="ad142-151">Velg **nb-no** for standardspråk.</span><span class="sxs-lookup"><span data-stu-id="ad142-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="ad142-152">Behold verdien i **Bane**-feltet slik det er.</span><span class="sxs-lookup"><span data-stu-id="ad142-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="ad142-153">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad142-153">Select **OK**.</span></span> <span data-ttu-id="ad142-154">Listen over sider på området vises.</span><span class="sxs-lookup"><span data-stu-id="ad142-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="ad142-155">Aktivere jobber</span><span class="sxs-lookup"><span data-stu-id="ad142-155">Enable jobs</span></span>

<span data-ttu-id="ad142-156">Følg disse trinnene for å aktivere jobber i Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad142-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ad142-157">Logg på miljøet (hovedkontor).</span><span class="sxs-lookup"><span data-stu-id="ad142-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="ad142-158">Gå til **Retail og Commerce \> Forespørsler og rapporter \> Satsvise jobber** ved hjelp av menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="ad142-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="ad142-159">De resterende trinnene i denne prosedyren må fullføres for hver av følgende jobber:</span><span class="sxs-lookup"><span data-stu-id="ad142-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="ad142-160">Behandle e-postvarsling for detaljistordre</span><span class="sxs-lookup"><span data-stu-id="ad142-160">Process retail order email notification</span></span>
    * <span data-ttu-id="ad142-161">Produkttilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="ad142-161">Product availability</span></span>
    * <span data-ttu-id="ad142-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="ad142-162">P-0001</span></span>
    * <span data-ttu-id="ad142-163">Synkroniser ordrejobb</span><span class="sxs-lookup"><span data-stu-id="ad142-163">Synchronize orders job</span></span>

1. <span data-ttu-id="ad142-164">Bruk hurtigfilteret til å søke etter jobben ved hjelp av navnet.</span><span class="sxs-lookup"><span data-stu-id="ad142-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="ad142-165">Hvis statusen for jobben er **Utfører**, utfører du følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="ad142-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="ad142-166">Velg posten.</span><span class="sxs-lookup"><span data-stu-id="ad142-166">Select the record.</span></span>
    1. <span data-ttu-id="ad142-167">Velg **Endre status** i kategorien **Satsvis jobb** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ad142-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="ad142-168">Velg **Avbryt**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad142-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="ad142-169">Du kan også angi et intervall for regelmessighet til ett (1) minutt for følgende jobber:</span><span class="sxs-lookup"><span data-stu-id="ad142-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="ad142-170">Behandle e-postvarslingsjobb for detaljistordre</span><span class="sxs-lookup"><span data-stu-id="ad142-170">Process retail order email notification job</span></span>
* <span data-ttu-id="ad142-171">P-0001-jobb</span><span class="sxs-lookup"><span data-stu-id="ad142-171">P-0001 job</span></span>
* <span data-ttu-id="ad142-172">Synkroniser ordrejobb</span><span class="sxs-lookup"><span data-stu-id="ad142-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="ad142-173">Kjøre fullstendig datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="ad142-173">Run full data synchronization</span></span>

<span data-ttu-id="ad142-174">Hvis du vil kjøre full datasynkronisering i Commerce, gjør du følgende i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ad142-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="ad142-175">Bruk menyen til venstre og gå til **Moduler \> Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="ad142-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="ad142-176">Velg kanalen med navnet **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="ad142-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="ad142-177">I handlingsruten velger du **Fullstendig datasynkronisering**.</span><span class="sxs-lookup"><span data-stu-id="ad142-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="ad142-178">Angi **9999** som distribusjonsplan.</span><span class="sxs-lookup"><span data-stu-id="ad142-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="ad142-179">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad142-179">Select **OK**.</span></span>
1. <span data-ttu-id="ad142-180">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad142-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="ad142-181">Teste kredittkortinformasjon for å utføre testinnkjøp</span><span class="sxs-lookup"><span data-stu-id="ad142-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="ad142-182">Hvis du skal utføre testtransaksjoner på området, kan du bruke denne testkredittkortinformasjonen:</span><span class="sxs-lookup"><span data-stu-id="ad142-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="ad142-183">**Kortnummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="ad142-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="ad142-184">**Utløpsdato:** 10/20</span><span class="sxs-lookup"><span data-stu-id="ad142-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="ad142-185">**Verdi for kortbekreftelse (CVV-kode):** 737</span><span class="sxs-lookup"><span data-stu-id="ad142-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad142-186">Du bør ikke prøve å bruke faktisk kredittkortinformasjon på testområdet under noen omstendigheter!</span><span class="sxs-lookup"><span data-stu-id="ad142-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ad142-187">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="ad142-187">Next steps</span></span>

<span data-ttu-id="ad142-188">Når klargjøringen og konfigurasjonstrinnene er fullført, er du klar til å bruke evalueringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="ad142-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="ad142-189">Bruk URL-adressen for Commerce-områdebygger for å gå til redigeringsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="ad142-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="ad142-190">Bruk URL-adressen for Commerce-området for å gå til kundeområdet for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="ad142-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="ad142-191">Hvis du vil konfigurere valgfrie funksjoner for Commerce-evalueringsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-evalueringsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="ad142-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad142-192">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ad142-192">Additional resources</span></span>

[<span data-ttu-id="ad142-193">Oversikt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="ad142-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ad142-194">Klargjøre et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ad142-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="ad142-195">Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ad142-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="ad142-196">Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ad142-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="ad142-197">Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="ad142-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ad142-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ad142-198">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ad142-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="ad142-199">Retail Cloud Scale Unit (RCSU)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ad142-200">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="ad142-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ad142-201">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="ad142-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
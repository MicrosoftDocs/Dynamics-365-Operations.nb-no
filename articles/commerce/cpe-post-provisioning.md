---
title: Konfigurere et evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø etter klargjøring.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599730"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="8a19a-103">Konfigurere et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8a19a-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a19a-104">Dette emnet forklarer hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø etter klargjøring.</span><span class="sxs-lookup"><span data-stu-id="8a19a-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="8a19a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="8a19a-105">Overview</span></span>

<span data-ttu-id="8a19a-106">Fullfør prosedyrene i dette emnet bare etter at evalueringsmiljøet i Commerce er klargjort.</span><span class="sxs-lookup"><span data-stu-id="8a19a-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="8a19a-107">Hvis du vil ha informasjon om hvordan du klargjør Commerce-evalueringsmiljøet, kan du se [Klargjøre et Commerce-evalueringsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="8a19a-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="8a19a-108">Når evalueringsmiljøet i Commerce er klargjort ende til ende, må du fullføre flere trinn etter klargjøring før du kan begynne å evaluere miljøet.</span><span class="sxs-lookup"><span data-stu-id="8a19a-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="8a19a-109">Hvis du vil fullføre disse trinnene, må du bruke Microsoft Dynamics Lifecycle Services (LCS, ) og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a19a-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="8a19a-110">Før du starter</span><span class="sxs-lookup"><span data-stu-id="8a19a-110">Before you start</span></span>

1. <span data-ttu-id="8a19a-111">Logg på [LCS-portalen](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="8a19a-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="8a19a-112">Gå til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="8a19a-112">Go to your project.</span></span>
1. <span data-ttu-id="8a19a-113">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="8a19a-114">Velg miljøet fra listen.</span><span class="sxs-lookup"><span data-stu-id="8a19a-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="8a19a-115">Velg \***Logg på miljøet** i miljøinformasjonen til høyre.</span><span class="sxs-lookup"><span data-stu-id="8a19a-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="8a19a-116">Du vil bli sendt til Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8a19a-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="8a19a-117">Kontroller at den juridiske enheten **USRT** er valgt i øvre høyre hjørne.</span><span class="sxs-lookup"><span data-stu-id="8a19a-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="8a19a-118">Under aktiviteter etter klargjøring i Commerce Headquarters må du kontrollere at den juridiske enheten **USRT** alltid er valgt.</span><span class="sxs-lookup"><span data-stu-id="8a19a-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="8a19a-119">Konfigurere salgsstedet</span><span class="sxs-lookup"><span data-stu-id="8a19a-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="8a19a-120">Knytt en arbeider til din identitet</span><span class="sxs-lookup"><span data-stu-id="8a19a-120">Associate a worker with your identity</span></span>

<span data-ttu-id="8a19a-121">Hvis du vil knytte en arbeider med identiteten din i Commerce Headquarters, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8a19a-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="8a19a-122">Bruk menyen til venstre, og gå til **Moduler \> Retail og Commerce \> Ansatte \> Arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="8a19a-123">Finn og velg følgnede post i listen **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="8a19a-124">Klikk **Commerce** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8a19a-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="8a19a-125">Velg **Tilknytt eksisterende ID**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="8a19a-126">I feltet **E-post** (til høyre for **Søk ved hjelp av e-post**) skriver du inn e-postadressen din.</span><span class="sxs-lookup"><span data-stu-id="8a19a-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="8a19a-127">Velg **Søk**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-127">Select **Search**.</span></span>
1. <span data-ttu-id="8a19a-128">Velg posten med navnet ditt.</span><span class="sxs-lookup"><span data-stu-id="8a19a-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="8a19a-129">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-129">Select **OK**.</span></span>
1. <span data-ttu-id="8a19a-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="8a19a-131">Aktivere Skysalgssted</span><span class="sxs-lookup"><span data-stu-id="8a19a-131">Activate Cloud POS</span></span>

<span data-ttu-id="8a19a-132">Hvis du vil aktivere Cloud POS, følger du denne fremgangsmåten i LCS.</span><span class="sxs-lookup"><span data-stu-id="8a19a-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="8a19a-133">Fra den øverste menyen velger du **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="8a19a-134">Velg miljøet fra listen.</span><span class="sxs-lookup"><span data-stu-id="8a19a-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="8a19a-135">Velg \***Logg på Cloud Point of Sale** i miljøinformasjonen til høyre.</span><span class="sxs-lookup"><span data-stu-id="8a19a-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="8a19a-136">Velg **Neste** for å åpne dialogboksen **Før du starter**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="8a19a-137">La **Server-URL**-feltet være slik det er.</span><span class="sxs-lookup"><span data-stu-id="8a19a-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="8a19a-138">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-138">Select **Next**.</span></span>
1. <span data-ttu-id="8a19a-139">Logg på ved hjelp av Microsoft Azure Active Directory (Azure AD)-kontoen din.</span><span class="sxs-lookup"><span data-stu-id="8a19a-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="8a19a-140">Under **Butikknavn** velger du **San Francisco**, og deretter velger du **Neste**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="8a19a-141">Under **Register og enhet** velger du **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="8a19a-142">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-142">Select **Activate**.</span></span> <span data-ttu-id="8a19a-143">Du er logget av og tatt til påloggingssiden for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="8a19a-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="8a19a-144">Du kan nå logge på Cloud POS-opplevelsen ved hjelp av operatør-ID-en **000713** og passordet **123**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="8a19a-145">Konfigurere området i Commerce</span><span class="sxs-lookup"><span data-stu-id="8a19a-145">Set up your site in Commerce</span></span>

<span data-ttu-id="8a19a-146">Følg denne fremgangsmåten for å begynne å konfigurere evalueringsområdet i Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a19a-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="8a19a-147">Logg på områdebyggeren ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="8a19a-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="8a19a-148">Klikk på **Fabrikam**-området for å åpne dialogboksen for områdeoppsett.</span><span class="sxs-lookup"><span data-stu-id="8a19a-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="8a19a-149">Velg domenet du angav da du startet e-handel.</span><span class="sxs-lookup"><span data-stu-id="8a19a-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="8a19a-150">Velg **Fabrikam-utvidet nettbutikk** for standardkanal.</span><span class="sxs-lookup"><span data-stu-id="8a19a-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="8a19a-151">(Pass på at du velger den **utvidede** nettbutikken.)</span><span class="sxs-lookup"><span data-stu-id="8a19a-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="8a19a-152">Velg **nb-no** for standardspråk.</span><span class="sxs-lookup"><span data-stu-id="8a19a-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="8a19a-153">Behold verdien i **Bane**-feltet slik det er.</span><span class="sxs-lookup"><span data-stu-id="8a19a-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="8a19a-154">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-154">Select **OK**.</span></span> <span data-ttu-id="8a19a-155">Listen over sider på området vises.</span><span class="sxs-lookup"><span data-stu-id="8a19a-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="8a19a-156">Aktivere jobber</span><span class="sxs-lookup"><span data-stu-id="8a19a-156">Enable jobs</span></span>

<span data-ttu-id="8a19a-157">Følg disse trinnene for å aktivere jobber i Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a19a-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="8a19a-158">Logg på miljøet (hovedkontor).</span><span class="sxs-lookup"><span data-stu-id="8a19a-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="8a19a-159">Gå til **Retail og Commerce \> Forespørsler og rapporter \> Satsvise jobber** ved hjelp av menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="8a19a-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="8a19a-160">De resterende trinnene i denne prosedyren må fullføres for hver av følgende jobber:</span><span class="sxs-lookup"><span data-stu-id="8a19a-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="8a19a-161">Behandle e-postvarsling for detaljistordre</span><span class="sxs-lookup"><span data-stu-id="8a19a-161">Process retail order email notification</span></span>
    * <span data-ttu-id="8a19a-162">Produkttilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="8a19a-162">Product availability</span></span>
    * <span data-ttu-id="8a19a-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="8a19a-163">P-0001</span></span>
    * <span data-ttu-id="8a19a-164">Synkroniser ordrejobb</span><span class="sxs-lookup"><span data-stu-id="8a19a-164">Synchronize orders job</span></span>

1. <span data-ttu-id="8a19a-165">Bruk hurtigfilteret til å søke etter jobben ved hjelp av navnet.</span><span class="sxs-lookup"><span data-stu-id="8a19a-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="8a19a-166">Hvis statusen for jobben er **Utfører**, utfører du følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="8a19a-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="8a19a-167">Velg posten.</span><span class="sxs-lookup"><span data-stu-id="8a19a-167">Select the record.</span></span>
    1. <span data-ttu-id="8a19a-168">Velg **Endre status** i kategorien **Satsvis jobb** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8a19a-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="8a19a-169">Velg **Avbryt**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="8a19a-170">Du kan også angi et intervall for regelmessighet til ett (1) minutt for følgende jobber:</span><span class="sxs-lookup"><span data-stu-id="8a19a-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="8a19a-171">Behandle e-postvarslingsjobb for detaljistordre</span><span class="sxs-lookup"><span data-stu-id="8a19a-171">Process retail order email notification job</span></span>
* <span data-ttu-id="8a19a-172">P-0001-jobb</span><span class="sxs-lookup"><span data-stu-id="8a19a-172">P-0001 job</span></span>
* <span data-ttu-id="8a19a-173">Synkroniser ordrejobb</span><span class="sxs-lookup"><span data-stu-id="8a19a-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="8a19a-174">Kjøre fullstendig datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="8a19a-174">Run full data synchronization</span></span>

<span data-ttu-id="8a19a-175">Hvis du vil kjøre full datasynkronisering i Commerce, gjør du følgende i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8a19a-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="8a19a-176">Bruk menyen til venstre og gå til **Moduler \> Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="8a19a-177">Velg kanalen med navnet **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="8a19a-178">I handlingsruten velger du **Fullstendig datasynkronisering**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="8a19a-179">Angi **9999** som distribusjonsplan.</span><span class="sxs-lookup"><span data-stu-id="8a19a-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="8a19a-180">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-180">Select **OK**.</span></span>
1. <span data-ttu-id="8a19a-181">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a19a-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="8a19a-182">Teste kredittkortinformasjon for å utføre testinnkjøp</span><span class="sxs-lookup"><span data-stu-id="8a19a-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="8a19a-183">Hvis du skal utføre testtransaksjoner på området, kan du bruke denne testkredittkortinformasjonen:</span><span class="sxs-lookup"><span data-stu-id="8a19a-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="8a19a-184">**Kortnummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="8a19a-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="8a19a-185">**Utløpsdato:** 10/20</span><span class="sxs-lookup"><span data-stu-id="8a19a-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="8a19a-186">**Verdi for kortbekreftelse (CVV-kode):** 737</span><span class="sxs-lookup"><span data-stu-id="8a19a-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a19a-187">Du bør ikke prøve å bruke faktisk kredittkortinformasjon på testområdet under noen omstendigheter!</span><span class="sxs-lookup"><span data-stu-id="8a19a-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8a19a-188">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="8a19a-188">Next steps</span></span>

<span data-ttu-id="8a19a-189">Når klargjøringen og konfigurasjonstrinnene er fullført, er du klar til å bruke evalueringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="8a19a-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="8a19a-190">Bruk URL-adressen for Commerce-områdebygger for å gå til redigeringsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="8a19a-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="8a19a-191">Bruk URL-adressen for Commerce-området for å gå til kundeområdet for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="8a19a-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="8a19a-192">Hvis du vil konfigurere valgfrie funksjoner for Commerce-evalueringsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-evalueringsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="8a19a-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a19a-193">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8a19a-193">Additional resources</span></span>

[<span data-ttu-id="8a19a-194">Oversikt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="8a19a-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="8a19a-195">Klargjøre et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8a19a-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="8a19a-196">Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8a19a-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="8a19a-197">Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8a19a-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="8a19a-198">Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="8a19a-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="8a19a-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8a19a-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="8a19a-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="8a19a-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="8a19a-201">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="8a19a-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="8a19a-202">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="8a19a-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

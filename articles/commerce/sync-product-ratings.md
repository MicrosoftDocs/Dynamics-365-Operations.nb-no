---
title: Synkronisere produktvurderinger i Dynamics 365 Commerce
description: Dette emnet beskriver hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dec87b548f3a218e1f833b752305f373e893b14c
ms.sourcegitcommit: 58d7133ae9909fa205730e3cf4c7fd5a1d5d0b75
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/10/2020
ms.locfileid: "3793593"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="6a92d-103">Synkronisere produktvurderinger i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6a92d-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a92d-104">Dette emnet beskriver hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a92d-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6a92d-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="6a92d-105">Overview</span></span>

<span data-ttu-id="6a92d-106">Hvis du vil bruke produktvurderinger i omnikanaler, for eksempel ved salgsstedet og i telefonsentre, må produktvurderingene fra vurderings- og omtaletjenesten importeres til handelskanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="6a92d-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="6a92d-107">Når produktvurderinger gjøres tilgjengelig i omnikanaler, kan de hjelpe kundene indirekte i løpet av samhandlingen med salgspartnere.</span><span class="sxs-lookup"><span data-stu-id="6a92d-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="6a92d-108">Dette emnet beskriver følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="6a92d-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="6a92d-109">Konfigurer **Synkroniseringsjobb for produktvurderinger** som en satsvis jobb for å synkronisere produktvurderinger fra **tjenesten for vurderinger og omtaler**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="6a92d-110">Kontroller at den satsvise jobben for synkronisering av produktvurdering er vellykket.</span><span class="sxs-lookup"><span data-stu-id="6a92d-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="6a92d-111">Gjør produktvurderinger tilgjengelige på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="6a92d-112">Konfigurere en satsvis jobb for å synkronisere produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="6a92d-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a92d-113">Før du starter må du kontrollere at versjon 10.0.6 eller senere av Dynamics 365 Commerce er installert.</span><span class="sxs-lookup"><span data-stu-id="6a92d-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="6a92d-114">Initialisere handelsplanleggeren</span><span class="sxs-lookup"><span data-stu-id="6a92d-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="6a92d-115">Bruk følgende fremgangsmåte for å initialisere handelsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="6a92d-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="6a92d-116">Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Initialiser handelsplanlegger**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="6a92d-117">Du kan også søke etter "Initialiser handelsplanlegger".</span><span class="sxs-lookup"><span data-stu-id="6a92d-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="6a92d-118">I dialogboksen **Initialiser handelsplanlegger** kontrollerer du at alternativet **Slett eksisterende konfigurasjon** er satt til **Nei**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="6a92d-119">Kontrollere RetailProductRating-deljobben</span><span class="sxs-lookup"><span data-stu-id="6a92d-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="6a92d-120">Følg denne fremgangsmåten for å kontrollere at **RetailProductRating**-deljobben finnes.</span><span class="sxs-lookup"><span data-stu-id="6a92d-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="6a92d-121">Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Deljobber i planlegger**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="6a92d-122">Du kan også søke etter "Deljobber i planlegger".</span><span class="sxs-lookup"><span data-stu-id="6a92d-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="6a92d-123">I listen over deljobber finner eller søker du etter deljobben **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="6a92d-124">Illustrasjonen nedenfor viser et eksempel på deljobbdetaljer i Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a92d-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![Detaljer i RetailProductRating-deljobben](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="6a92d-126">Hvis du ikke finner deljobben **RetailProductRating** kan det hende at du allerede har kjørt jobben **Synkroniser produktvurderinger** og jobben **1040 CDX** før du initialiserte handelsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="6a92d-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="6a92d-127">I dette tilfellet følger du denne fremgangsmåten for å kjøre jobben **Fullstendig datasynkronisering**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="6a92d-128">Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="6a92d-129">Du kan også søke etter "kanaldatabase".</span><span class="sxs-lookup"><span data-stu-id="6a92d-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="6a92d-130">Velg kanaldatabasen som skal synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="6a92d-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="6a92d-131">I handlingsruten velger du **Fullstendig datasynkronisering**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="6a92d-132">I rullegardinboksen **Velg en distribusjonsplan** velger du **1040 – produkter**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="6a92d-133">Gjenta trinnene for den forrige prosedyren for å kontrollere at deljobben **RetailProductRating** er opprettet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="6a92d-134">Importere produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="6a92d-134">Import product ratings</span></span>

<span data-ttu-id="6a92d-135">Følg denne fremgangsmåten for å importere produktvurderinger til Commerce fra vurderings- og omtaletjenesten:</span><span class="sxs-lookup"><span data-stu-id="6a92d-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="6a92d-136">Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Synkroniser produktvurderinger-jobb**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="6a92d-137">Du kan også søke etter "Synkroniser produktvurderinger-jobb".</span><span class="sxs-lookup"><span data-stu-id="6a92d-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="6a92d-138">I dialogboksen **Hent produktvurderinger** i hurtigfanen **Kjør i bakgrunnen** velger du **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="6a92d-139">Angi et gjentakende mønster i dialogboksen **Definer regelmessighet** .</span><span class="sxs-lookup"><span data-stu-id="6a92d-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="6a92d-140">(Den foreslåtte verdien er to timer.) Ikke planlegg en regelmessighet som er mindre enn én time.</span><span class="sxs-lookup"><span data-stu-id="6a92d-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="6a92d-141">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-141">Select **OK**.</span></span>
1. <span data-ttu-id="6a92d-142">Sett alternativet **Partiprosess** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="6a92d-143">Denne innstillingen hjelper deg med å kontrollere at du kan overvåke loggene og kontrollere at statusen til de satsvise jobbene kjøres.</span><span class="sxs-lookup"><span data-stu-id="6a92d-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="6a92d-144">Velg **OK** for å planlegge den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="6a92d-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="6a92d-145">Illustrasjonen nedenfor viser et eksempel på konfigurasjon av satsvis jobb i Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a92d-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Konfigurasjon av den satsvise jobben for synkroniserings produktvurderinger](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="6a92d-147">Kontrollere at den satsvise jobben for synkronisering av produktvurdering er vellykket</span><span class="sxs-lookup"><span data-stu-id="6a92d-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="6a92d-148">Følg denne fremgangsmåten for å kontrollere at den satsvise jobben for **Synkroniser produktvurderinger** er fullført.</span><span class="sxs-lookup"><span data-stu-id="6a92d-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="6a92d-149">Gå til **Retail og Commerce \> Systemansvarlig \> Forespørsler \> Satsvise jobber** eller, hvis du bruker en Commerce-spesifikk SKU, går du til **Retail og Commerce \> Forespørsler og rapporter \> Satsvise jobber** i stedet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="6a92d-150">Du kan også søke etter "Satsvise jobber".</span><span class="sxs-lookup"><span data-stu-id="6a92d-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="6a92d-151">Hvis du vil vise detaljene for den satsvise jobben, kan du gå til kolonnen **Jobbeskrivelse** i listen over satsvise jobber og søke etter en beskrivelse som inneholder "Hent produktvurderinger".</span><span class="sxs-lookup"><span data-stu-id="6a92d-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="6a92d-152">Velg jobb-ID for å vise detaljene for de satsvise jobbene, for eksempel planlagt startdato/-klokkeslett og teksten for regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="6a92d-153">Følgende illustrasjon viser et eksempel på detaljene for den satsvise jobben i Commerce når den satsvise jobben er planlagt å kjøres med totimersintervaller.</span><span class="sxs-lookup"><span data-stu-id="6a92d-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Detaljer for den satsvise jobben for synkronisering av produktvurderinger](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="6a92d-155">Gjør produktvurderinger tilgjengelige på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="6a92d-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="6a92d-156">Vurderings- og omtaleløsningen i Dynamics 365 Commerce er en omnikanalløsning.</span><span class="sxs-lookup"><span data-stu-id="6a92d-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="6a92d-157">Produktvurderinger vises imidlertid ikke som standard på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="6a92d-158">Hvis du vil hjelpe kunder i butikker med å se vurderinger og omtaler når de blir hjulpet av salgsmedarbeidere, må du slå på produktvurderinger på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="6a92d-159">Følg denne fremgangsmåten for å slå på produktvurderinger på salgsstedet:</span><span class="sxs-lookup"><span data-stu-id="6a92d-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="6a92d-160">Gå til **Retail og Commerce \> Handelsoppsett \> Parametere \> Handelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="6a92d-161">Du kan også søke etter "Handelsparametere".</span><span class="sxs-lookup"><span data-stu-id="6a92d-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="6a92d-162">Velg **Ny** i kategorien **Konfigurasjonsparametre**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="6a92d-163">Skriv inn et navn, for eksempel **VurderingerOgOmtaler.AktiverProduktvurderingerForDetaljhandelsbutikker**, og sett verdien til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="6a92d-164">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-164">Select **Save**.</span></span>
1. <span data-ttu-id="6a92d-165">Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="6a92d-166">Alternativt kan du søke etter "Distribusjonsplan".</span><span class="sxs-lookup"><span data-stu-id="6a92d-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="6a92d-167">Velg **1110** i jobblisten (**Global konfigurasjon**), og velg deretter **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="6a92d-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="6a92d-168">Når jobben er kjørt uten problemer, må du kontrollere at produktvurderingene nå vises på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="6a92d-169">Følgende illustrasjon viser et eksempel på konfigurasjon av handelsparametere for å slå på produktvurderinger på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![Konfigurasjon av handelsparametere for produktvurderinger på salgsstedet](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="6a92d-171">Illustrasjonen nedenfor viser et eksempel på produktvurderinger på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="6a92d-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Produktvurderinger på salgsstedet](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="6a92d-173">Illustrasjonen nedenfor viser et eksempel på produktvurderinger i telefonsenterkanaler.</span><span class="sxs-lookup"><span data-stu-id="6a92d-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Produktvurderinger i en telefonsenterkanal](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="6a92d-175">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6a92d-175">Additional resources</span></span>

[<span data-ttu-id="6a92d-176">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="6a92d-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="6a92d-177">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="6a92d-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="6a92d-178">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="6a92d-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="6a92d-179">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="6a92d-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

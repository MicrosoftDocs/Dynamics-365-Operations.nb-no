---
title: Synkronisere produktvurderinger i Dynamics 365 Retail
description: Dette emnet beskriver hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Retail.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698171"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a><span data-ttu-id="a9777-103">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="a9777-103">Sync product ratings in Dynamics 365 Retail</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a9777-104">Dette emnet beskriver hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="a9777-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="a9777-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="a9777-105">Overview</span></span>

<span data-ttu-id="a9777-106">Hvis du vil bruke produktvurderinger i omnikanaler, for eksempel ved salgsstedet og i telefonsentre, må produktvurderingene fra vurderings- og omtaletjenesten importeres til detaljhandelsdatabasen.</span><span class="sxs-lookup"><span data-stu-id="a9777-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Retail channel database.</span></span> <span data-ttu-id="a9777-107">Når produktvurderinger gjøres tilgjengelig i omnikanaler, kan de hjelpe kundene indirekte i løpet av samhandlingen med salgspartnere.</span><span class="sxs-lookup"><span data-stu-id="a9777-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="a9777-108">Dette emnet beskriver følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="a9777-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="a9777-109">Konfigurer en satsvis detaljhandelsjobb for å importere produktvurderinger.</span><span class="sxs-lookup"><span data-stu-id="a9777-109">Configure a Retail batch job to import product ratings.</span></span>
1. <span data-ttu-id="a9777-110">Kontroller at den satsvise jobben for synkronisering av produktvurdering er vellykket.</span><span class="sxs-lookup"><span data-stu-id="a9777-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="a9777-111">Gjør produktvurderinger tilgjengelige på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="a9777-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a><span data-ttu-id="a9777-112">Konfigurere en satsvis detaljhandelsjobb for å importere produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="a9777-112">Configure a Retail batch job to import product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9777-113">Før du starter må du kontrollere at versjon 10.0.6 eller senere av Retail er installert.</span><span class="sxs-lookup"><span data-stu-id="a9777-113">Before you start, make sure that version 10.0.6 or later of Retail is installed.</span></span>

### <a name="initialize-the-retail-scheduler"></a><span data-ttu-id="a9777-114">Initialisere detaljhandelsplanlegger</span><span class="sxs-lookup"><span data-stu-id="a9777-114">Initialize the retail scheduler</span></span>

<span data-ttu-id="a9777-115">Bruk følgende fremgangsmåte for å initialisere detaljhandelsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="a9777-115">To initialize the retail scheduler, follow these steps.</span></span>

1. <span data-ttu-id="a9777-116">Gå til **Retail \> Hovedkvarteroppsett \> Detaljhandel Planlegger \> Initialiser Retail-planlegger**.</span><span class="sxs-lookup"><span data-stu-id="a9777-116">Go to **Retail \> Headquarters setup \> Retail scheduler \> Initialize retail scheduler**.</span></span> <span data-ttu-id="a9777-117">Du kan også søke etter "Initialiser Retail-planlegger".</span><span class="sxs-lookup"><span data-stu-id="a9777-117">Alternatively, search for "Initialize retail scheduler."</span></span>
1. <span data-ttu-id="a9777-118">I dialogboksen **Initialiser Retail-planlegger** kontrollerer du at alternativet **Slett eksisterende konfigurasjon** er satt til **Nei**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9777-118">In the **Initialize retail scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="a9777-119">Kontrollere RetailProductRating-deljobben</span><span class="sxs-lookup"><span data-stu-id="a9777-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="a9777-120">Følg denne fremgangsmåten for å kontrollere at **RetailProductRating**-deljobben finnes.</span><span class="sxs-lookup"><span data-stu-id="a9777-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="a9777-121">Gå til **Retail \> Hovedkvarteroppsett \> Detaljhandel Planlegger \> Deljobber i planlegger**.</span><span class="sxs-lookup"><span data-stu-id="a9777-121">Go to **Retail \> Headquarters setup \> Retail scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="a9777-122">Du kan også søke etter "Deljobber i planlegger".</span><span class="sxs-lookup"><span data-stu-id="a9777-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="a9777-123">I listen over deljobber finner eller søker du etter deljobben **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="a9777-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="a9777-124">Illustrasjonen nedenfor viser et eksempel på deljobbdetaljer i Retail.</span><span class="sxs-lookup"><span data-stu-id="a9777-124">The following illustration shows an example of the subjob details in Retail.</span></span>

![Detaljer i RetailProductRating-deljobben](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="a9777-126">Hvis du ikke finner deljobben **RetailProductRating** kan det hende at du allerede har kjørt jobben **Synkroniser produktvurderinger** og jobben **1040 CDX** før du initialiserte detaljhandelplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="a9777-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the retail scheduler.</span></span> <span data-ttu-id="a9777-127">I dette tilfellet følger du denne fremgangsmåten for å kjøre jobben **Fullstendig datasynkronisering**.</span><span class="sxs-lookup"><span data-stu-id="a9777-127">In this case, follow these steps to run the **Full data sync** job.</span></span>
>
> 1. <span data-ttu-id="a9777-128">Gå til **Retail \> Hovedkvarteroppsett \> Detaljhandel Planlegger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="a9777-128">Go to **Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span> <span data-ttu-id="a9777-129">Du kan også søke etter "kanaldatabase".</span><span class="sxs-lookup"><span data-stu-id="a9777-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="a9777-130">Velg kanaldatabasen som skal synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="a9777-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="a9777-131">I handlingsruten velger du **Fullstendig datasynkronisering**.</span><span class="sxs-lookup"><span data-stu-id="a9777-131">On the Action Pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="a9777-132">I rullegardinboksen **Velg en distribusjonsplan** velger du **1040 – produkter**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9777-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="a9777-133">Gjenta trinnene for den forrige prosedyren for å kontrollere at deljobben **RetailProductRating** er opprettet.</span><span class="sxs-lookup"><span data-stu-id="a9777-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="a9777-134">Importere produktvurderinger</span><span class="sxs-lookup"><span data-stu-id="a9777-134">Import product ratings</span></span>

<span data-ttu-id="a9777-135">Følg denne fremgangsmåten for å importere produktvurderinger til Retail fra vurderings- og omtaletjenesten:</span><span class="sxs-lookup"><span data-stu-id="a9777-135">To import product ratings into Retail from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="a9777-136">Gå til **Retail \> Hovedkvarteroppsett \> Detaljhandel Planlegger \> Synkroniser produktvurderinger-jobb**.</span><span class="sxs-lookup"><span data-stu-id="a9777-136">Go to **Retail \> Headquarters setup \> Retail scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="a9777-137">Du kan også søke etter "Synkroniser produktvurderinger-jobb".</span><span class="sxs-lookup"><span data-stu-id="a9777-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="a9777-138">I dialogboksen **Hent produktvurderinger** i hurtigfanen **Kjør i bakgrunnen** velger du **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="a9777-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="a9777-139">Angi et gjentakende mønster i dialogboksen **Definer regelmessighet** .</span><span class="sxs-lookup"><span data-stu-id="a9777-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="a9777-140">(Den foreslåtte verdien er to timer.) Ikke planlegg en regelmessighet som er mindre enn én time.</span><span class="sxs-lookup"><span data-stu-id="a9777-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="a9777-141">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9777-141">Select **OK**.</span></span>
1. <span data-ttu-id="a9777-142">Sett alternativet **Partiprosess** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a9777-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="a9777-143">Denne innstillingen hjelper deg med å kontrollere at du kan overvåke loggene og kontrollere at statusen til de satsvise jobbene kjøres.</span><span class="sxs-lookup"><span data-stu-id="a9777-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="a9777-144">Velg **OK** for å planlegge den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="a9777-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="a9777-145">Illustrasjonen nedenfor viser et eksempel på konfigurasjon av satsvis jobb i Retail.</span><span class="sxs-lookup"><span data-stu-id="a9777-145">The following illustration shows an example of batch job configuration in Retail.</span></span>

![Konfigurasjon av den satsvise jobben for synkroniserings produktvurderinger](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="a9777-147">Kontrollere at den satsvise jobben for synkronisering av produktvurdering er vellykket</span><span class="sxs-lookup"><span data-stu-id="a9777-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="a9777-148">Følg denne fremgangsmåten for å kontrollere at den satsvise jobben for **Synkroniser produktvurderinger** er fullført.</span><span class="sxs-lookup"><span data-stu-id="a9777-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="a9777-149">Gå til **Retail \> Systemansvarlig \> Forespørsler \> Satsvise jobber** eller, hvis du bruker en Retail-spesifikk SKU, går du til **Retail \> Forespørsler og rapporter \> Satsvise jobber** i stedet.</span><span class="sxs-lookup"><span data-stu-id="a9777-149">Go to **Retail \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Retail-only stock keeping unit (SKU), **Retail \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="a9777-150">Du kan også søke etter "Satsvise jobber".</span><span class="sxs-lookup"><span data-stu-id="a9777-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="a9777-151">Hvis du vil vise detaljene for den satsvise jobben, kan du gå til kolonnen **Jobbeskrivelse** i listen over satsvise jobber og søke etter en beskrivelse som inneholder "Hent produktvurderinger".</span><span class="sxs-lookup"><span data-stu-id="a9777-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="a9777-152">Velg jobb-ID for å vise detaljene for de satsvise jobbene, for eksempel planlagt startdato/-klokkeslett og teksten for regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="a9777-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="a9777-153">Følgende illustrasjon viser et eksempel på detaljene for den satsvise jobben i Retail når den satsvise jobben er planlagt å kjøres med totimersintervaller.</span><span class="sxs-lookup"><span data-stu-id="a9777-153">The following illustration shows an example of the batch job details in Retail when the batch job is scheduled to run at two-hour intervals.</span></span>

![Detaljer for den satsvise jobben for synkronisering av produktvurderinger](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="a9777-155">Gjør produktvurderinger tilgjengelige på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="a9777-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="a9777-156">Vurderings- og omtaleløsningen i Dynamics 365 Commerce er en omnikanalløsning.</span><span class="sxs-lookup"><span data-stu-id="a9777-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="a9777-157">Produktvurderinger vises imidlertid ikke som standard på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="a9777-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="a9777-158">Hvis du vil hjelpe kunder i butikker med å se vurderinger og omtaler når de blir hjulpet av salgsmedarbeidere, må du slå på produktvurderinger på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="a9777-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="a9777-159">Følg denne fremgangsmåten for å slå på produktvurderinger på salgsstedet:</span><span class="sxs-lookup"><span data-stu-id="a9777-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="a9777-160">Gå til **Retail \> Handelsoppsett \> Parametere \> Detaljhandelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="a9777-160">Go to **Retail \> Retail setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="a9777-161">Du kan også søke etter "Detaljhandelsparametere".</span><span class="sxs-lookup"><span data-stu-id="a9777-161">Alternatively, search for "Retail parameters."</span></span>
1. <span data-ttu-id="a9777-162">Velg **Ny** i kategorien **Konfigurasjonsparametre**.</span><span class="sxs-lookup"><span data-stu-id="a9777-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="a9777-163">Skriv inn et navn, for eksempel **VurderingerOgOmtaler.AktiverProduktvurderingerForDetaljhandelsbutikker**, og sett verdien til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="a9777-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="a9777-164">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a9777-164">Select **Save**.</span></span>
1. <span data-ttu-id="a9777-165">Gå til **Detaljhandel \> IT for detaljhandel \> Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="a9777-165">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span> <span data-ttu-id="a9777-166">Alternativt kan du søke etter "Distribusjonsplan".</span><span class="sxs-lookup"><span data-stu-id="a9777-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="a9777-167">Velg **1110** i jobblisten (**Global konfigurasjon**), og velg deretter **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="a9777-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="a9777-168">Når jobben er kjørt uten problemer, må du kontrollere at produktvurderingene nå vises på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="a9777-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="a9777-169">Følgende illustrasjon viser et eksempel på konfigurasjon av detaljhandelsparametere for å slå på produktvurderinger på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="a9777-169">The following illustration shows an example of the configuration of the Retail parameters to turn on product ratings at the POS.</span></span>

![Konfigurasjon av detaljhandelsparametere for produktvurderinger på salgsstedet](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="a9777-171">Illustrasjonen nedenfor viser et eksempel på produktvurderinger på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="a9777-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Produktvurderinger på salgsstedet](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="a9777-173">Illustrasjonen nedenfor viser et eksempel på produktvurderinger i telefonsenterkanaler.</span><span class="sxs-lookup"><span data-stu-id="a9777-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Produktvurderinger i en telefonsenterkanal](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="a9777-175">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a9777-175">Additional resources</span></span>

[<span data-ttu-id="a9777-176">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a9777-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="a9777-177">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a9777-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="a9777-178">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a9777-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="a9777-179">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="a9777-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

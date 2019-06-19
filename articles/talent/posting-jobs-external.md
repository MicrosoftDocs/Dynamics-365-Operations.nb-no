---
title: Postere jobber på eksterne karriereområder fra Attract
description: Dette emnet forklarer hvordan du bruker Dynamics 365 for Talent - Attract til å postere jobber til eksterne områder for rekruttering
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590488"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="3bb5e-103">Postere jobber på eksterne karriereområder fra Attract</span><span class="sxs-lookup"><span data-stu-id="3bb5e-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3bb5e-104">Du vil gjerne vise ledige stillingene for så mange kvalifiserte kandidater som mulig.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="3bb5e-105">Rekrutteringsområder, for eksempel Broadbean, hjelper deg med å oppnå dette målet.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="3bb5e-106">Microsoft Dynamics 365 Talent: Med Attract kan du postere jobber til Broadbean, og Microsoft gir deg kontinuerlig nye tilbud på dette området.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="3bb5e-107">Legge inn jobber på Broadbean</span><span class="sxs-lookup"><span data-stu-id="3bb5e-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="3bb5e-108">Før du kan postere jobber til Broadbean må du konfigurere Broadbean-integreringen.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="3bb5e-109">Hvis du vil postere jobber til eksterne områder, må du ha [tillegget for omfattende ansettelse](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="3bb5e-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="3bb5e-110">Hvis du vil postere jobber til Broadbean via Attract, må du ha et Broadbean-abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="3bb5e-111">Denne funksjonen er for øyeblikket i forhåndsvisningen.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-111">This feature is currently in preview.</span></span> <span data-ttu-id="3bb5e-112">Hvis du vil prøve dette, må du [aktiverer funksjonen i innstillingene for administrasjon av Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="3bb5e-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="3bb5e-113">Konfigurere Broadbean-integrering</span><span class="sxs-lookup"><span data-stu-id="3bb5e-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="3bb5e-114">Logge på Attract som en administrator.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="3bb5e-115">Velg **Innstillinger**-knappen (tannhjulssymbolet) i øvre høyre hjørne på siden, og velg deretter **Administrasjonssenter**.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="3bb5e-116">I kategorien **Innstillinger for jobbtavle** i delen **Aktiver Broadbean-integrering** aktiverer du integreringen.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="3bb5e-117">Kontakt Broadbean, og skriv inn informasjonen din i **Brukernavn, Klient-ID, Krypteringstoken**.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="3bb5e-118">Broadbean-legitimasjonen din er sensitiv og konfidensiell.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="3bb5e-119">Derfor må du lagre og dele den på en ansvarlig måte.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="3bb5e-120">Alle som har en Administrator-rolle i Attract, kan vise denne legitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="3bb5e-121">Microsoft og Attract er ikke er involvert i å opprette og vedlikeholde disse verdiene.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="3bb5e-122">Det er ditt ansvar å holde dem oppdatert i Attract og arbeide sammen med Broadbean for å løse problemer som involverer legitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="3bb5e-123">Legge inn en jobb på Broadbean</span><span class="sxs-lookup"><span data-stu-id="3bb5e-123">Post a job to Broadbean</span></span>

<span data-ttu-id="3bb5e-124">Når Broadbean er aktivert, kan rekrutteringspersoner og administratorer postere en jobb til den.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="3bb5e-125">Du må ha en URL-adresse for jobben.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="3bb5e-126">I Attract åpner du jobben du vil postere til Broadbean.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="3bb5e-127">I **Posteringer**-delen velger du **Legg ut nå**-knappen som tilsvarer Broadbean.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="3bb5e-128">Følg instruksjonene i Broadbean-vinduet.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="3bb5e-129">Attract sender følgende informasjon til Broadbean:</span><span class="sxs-lookup"><span data-stu-id="3bb5e-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="3bb5e-130">Forespørsels-ID</span><span class="sxs-lookup"><span data-stu-id="3bb5e-130">Request ID</span></span>
- <span data-ttu-id="3bb5e-131">Jobbtittel</span><span class="sxs-lookup"><span data-stu-id="3bb5e-131">Job title</span></span>
- <span data-ttu-id="3bb5e-132">Beskrivelse av jobb</span><span class="sxs-lookup"><span data-stu-id="3bb5e-132">Job description</span></span>
- <span data-ttu-id="3bb5e-133">Jobbsted</span><span class="sxs-lookup"><span data-stu-id="3bb5e-133">Job location</span></span>
- <span data-ttu-id="3bb5e-134">Søk-URL</span><span class="sxs-lookup"><span data-stu-id="3bb5e-134">Apply URL</span></span>
- <span data-ttu-id="3bb5e-135">Informasjon om verver</span><span class="sxs-lookup"><span data-stu-id="3bb5e-135">Recruiter information</span></span>

<span data-ttu-id="3bb5e-136">Når Broadbean har fullført posteringen, viser **Posteringer**-delen av jobben i Attract statusen for Broadbean som **Postert**.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="3bb5e-137">Broadbean krever **Bransje**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="3bb5e-138">For øyeblikket er dette feltet satt til **IT** som standard.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="3bb5e-139">Du kan imidlertid endre verdien til riktig bransje i vinduet for Broadbean-stillingsposteringen.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="3bb5e-140">Det tar litt tid for Broadbean å fullføre postering av jobben til alle jobbtavlene du har valgt.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="3bb5e-141">Derfor kan være en liten forsinkelse før Attract gir en statusoppdatering for jobben.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="3bb5e-142">Vise en Broadbean-jobbpostering</span><span class="sxs-lookup"><span data-stu-id="3bb5e-142">View a Broadbean job posting</span></span>

<span data-ttu-id="3bb5e-143">Når du posterer en jobb til Broadbean, kan du vise den fra Attract.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="3bb5e-144">I Attract åpner du jobben du vil vise på Broadbean.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="3bb5e-145">I delen **Posteringer** velger du ellipseknappen (**...**) som tilsvarer Broadbean, og velg deretter **Vis**.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="3bb5e-146">Broadbean-jobbposteringen vises i et nytt vindu.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="3bb5e-147">Oppdatere en Broadbean-jobbpostering</span><span class="sxs-lookup"><span data-stu-id="3bb5e-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="3bb5e-148">Du kan oppdatere en Broadbean-jobbpostering på to forskjellige måter.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="3bb5e-149">I Attract åpner du jobben du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="3bb5e-150">I **Posteringer**-delen velger du **Oppdater oppføring**-knappen som tilsvarer Broadbean.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="3bb5e-151">Rediger posteringen i Broadbean-vinduet.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="3bb5e-152">– eller –</span><span class="sxs-lookup"><span data-stu-id="3bb5e-152">–or–</span></span>

1. <span data-ttu-id="3bb5e-153">I Attract åpner du jobben du vil vise på Broadbean.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="3bb5e-154">I delen **Posteringer** velger du ellipseknappen (**...**) som tilsvarer Broadbean, og velg deretter **Vis**.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="3bb5e-155">Rediger jobbdetaljene i Broadbean-vinduet, og poster deretter jobben på nytt.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="3bb5e-156">Jobbdetaljene i Attract endres ikke.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="3bb5e-157">Fjerne en Broadbean-jobbpostering</span><span class="sxs-lookup"><span data-stu-id="3bb5e-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="3bb5e-158">Du kan fjerne en jobbpostering fra Broadbean etter behov.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="3bb5e-159">I Attract åpner du jobben du vil fjerne.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="3bb5e-160">I delen **Posteringer** velger du ellipseknappen (**...**) som tilsvarer Broadbean, og velg deretter **Fjern utlysing**.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="3bb5e-161">Når Broadbean fjerner jobben, har Broadbean-elementet i Attract en **Legg ut nå**-knapp.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="3bb5e-162">Denne knappen angir at jobben er fjernet og kan posteres på nytt.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="3bb5e-163">Feilsøke Broadbean-integreringen</span><span class="sxs-lookup"><span data-stu-id="3bb5e-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="3bb5e-164">Hvis du har problemer med å postere en jobb til Broadbean, kan du prøve følgende fremgangsmåte:</span><span class="sxs-lookup"><span data-stu-id="3bb5e-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="3bb5e-165">Kontroller at Broadbean-legitimasjonen du har angitt, er gyldig og korrekt.</span><span class="sxs-lookup"><span data-stu-id="3bb5e-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="3bb5e-166">Hvis legitimasjonen er gyldig og korrekt, kan du kontakte [Broadbean-støtten](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="3bb5e-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="3bb5e-167">Hvis problemet vedvarer, kontakter du [Microsoft Kundestøtte](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="3bb5e-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

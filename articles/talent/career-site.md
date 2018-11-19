---
title: "Karriereområde-funksjonalitet i Attract"
description: "Denne artikkelen gir en oversikt over den kandidatrettede karrireområde-funksjonaliteten i Microsoft Dynamics 365 for Talent - Attract. Den forklarer også hvordan du konfigurerer denne funksjonen."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: nb-no
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="84dd4-104">Karriereområde-funksjonalitet i Attract</span><span class="sxs-lookup"><span data-stu-id="84dd4-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84dd4-105">Denne artikkelen gir en oversikt over den kandidatrettede karrireområde-funksjonaliteten i Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="84dd4-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="84dd4-106">Den forklarer også hvordan du konfigurerer denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="84dd4-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="84dd4-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="84dd4-107">Overview</span></span>

<span data-ttu-id="84dd4-108">Attract inneholder ett karriereområde for hvert miljø i en leier.</span><span class="sxs-lookup"><span data-stu-id="84dd4-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="84dd4-109">Hvis en organisasjon for eksempel har et utviklingsmiljø og et testmiljø, klargjøres ett karriereområde for utviklingsmiljøet og et annet karriereområde klargjøres for testmiljøet.</span><span class="sxs-lookup"><span data-stu-id="84dd4-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="84dd4-110">Hvert karriereområde er **fullstendig isolert** og har sin egen godkjenningsmekanisme.</span><span class="sxs-lookup"><span data-stu-id="84dd4-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="84dd4-111">Jobber og kandidatprofiler deles ikke mellom karriereområder.</span><span class="sxs-lookup"><span data-stu-id="84dd4-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="84dd4-112">Som standard er karriereområdet offentlig.</span><span class="sxs-lookup"><span data-stu-id="84dd4-112">By default, the career site is public.</span></span> <span data-ttu-id="84dd4-113">Derfor kan kandidater vise alle jobbene som er merket som eksterne, uten å måtte logge på.</span><span class="sxs-lookup"><span data-stu-id="84dd4-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="84dd4-114">Alle andre handlinger krever imidlertid at kandidater logger på.</span><span class="sxs-lookup"><span data-stu-id="84dd4-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="84dd4-115">Karrierestedsledelse</span><span class="sxs-lookup"><span data-stu-id="84dd4-115">Career site management</span></span>

<span data-ttu-id="84dd4-116">Følgende elementer på karriereområdet styres av innstillingene:</span><span class="sxs-lookup"><span data-stu-id="84dd4-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="84dd4-117">**Organisasjonsnavn:** Organisasjonsnavnet vises i navigasjonsfeltet øverst i karriereområdet.</span><span class="sxs-lookup"><span data-stu-id="84dd4-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="84dd4-118">Ved å velge navnet på organisasjonen går kandidater til en side som viser alle åpne jobber.</span><span class="sxs-lookup"><span data-stu-id="84dd4-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="84dd4-119">**Organisasjonslogo:** Et bilde av organisasjonens logo vises øverst til venstre for karriereområdet.</span><span class="sxs-lookup"><span data-stu-id="84dd4-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="84dd4-120">Ved å velge logobildet går kandidater til en side som viser alle åpne jobber.</span><span class="sxs-lookup"><span data-stu-id="84dd4-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="84dd4-121">Hvis du vil angi verdier for organisasjonsnavn og logo, logger du deg på Attract som administrator, velger **Administrasjonssenter** på **Innstillinger**-menyen (tannhjulsymbolet), og velger deretter den **Firmainformasjon**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="84dd4-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="84dd4-122">Logobildet som vises på karriereområdet, har en fast høyde på 20 piksler.</span><span class="sxs-lookup"><span data-stu-id="84dd4-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="84dd4-123">Bildet du legger til i administrasjonssenteret, skaleres slik at det passer.</span><span class="sxs-lookup"><span data-stu-id="84dd4-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="84dd4-124">Avhengig av bildet kan derfor bredden endres.</span><span class="sxs-lookup"><span data-stu-id="84dd4-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="84dd4-125">URL-adresse for karriereområde</span><span class="sxs-lookup"><span data-stu-id="84dd4-125">Career site URL</span></span>

<span data-ttu-id="84dd4-126">Når du [posterer en ekstern jobb](./Creating-jobs-Attract.md#postings) for første gang, kan du kopiere **Søk**-koblingen fra programmet Attract.</span><span class="sxs-lookup"><span data-stu-id="84dd4-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="84dd4-127">URL-adressen for denne koblingen vil være i følgende format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="84dd4-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="84dd4-128">URL-adressen til karriereområdet er en delstreng av **Søk**-URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="84dd4-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="84dd4-129">Den består av alt opp til og med firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="84dd4-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="84dd4-130">For den foregående **Søk**-URL-adressen er derfor URL-adressen for karriereområdet `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="84dd4-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="84dd4-131">Godkjenningsalternativer</span><span class="sxs-lookup"><span data-stu-id="84dd4-131">Authentication options</span></span>

<span data-ttu-id="84dd4-132">Kandidater har følgende alternativer for pålogging for et Attract-karriereområde:</span><span class="sxs-lookup"><span data-stu-id="84dd4-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="84dd4-133">Personlig konto:</span><span class="sxs-lookup"><span data-stu-id="84dd4-133">Personal account:</span></span>

    - <span data-ttu-id="84dd4-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="84dd4-134">LinkedIn</span></span>
    - <span data-ttu-id="84dd4-135">Microsoft </span><span class="sxs-lookup"><span data-stu-id="84dd4-135">Microsoft</span></span>
    - <span data-ttu-id="84dd4-136">Google</span><span class="sxs-lookup"><span data-stu-id="84dd4-136">Google</span></span>
    - <span data-ttu-id="84dd4-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="84dd4-137">Facebook</span></span>

- <span data-ttu-id="84dd4-138">Jobb- eller skolekonto:</span><span class="sxs-lookup"><span data-stu-id="84dd4-138">Work or school account:</span></span>

    - <span data-ttu-id="84dd4-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="84dd4-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="84dd4-140">Azure AD-påloggingen er bare beregnet for interne kandidater.</span><span class="sxs-lookup"><span data-stu-id="84dd4-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="84dd4-141">Derfor fungerer den bare for interne kandidater som bruker den Azure AD-legitimasjonen for firmaet.</span><span class="sxs-lookup"><span data-stu-id="84dd4-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="84dd4-142">Eksempel: En kandidat som for tiden er ansatt hos Contoso Ltd., vil søke på en jobb i et ikke-relatert firma, Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="84dd4-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="84dd4-143">I dette tilfellet vil ikke påloggingen lykkes hvis den ansatte prøver å bruke Azure AD-legitimasjonen fra Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="84dd4-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="84dd4-144">Opprette og vedlikeholde en profil</span><span class="sxs-lookup"><span data-stu-id="84dd4-144">Create and maintain a profile</span></span>

<span data-ttu-id="84dd4-145">Etter at kandidater har logget på karriereområdet, kan de velge **Min profil** i navigasjonsfeltet øverst på siden for å opprette og vedlikeholde profilen.</span><span class="sxs-lookup"><span data-stu-id="84dd4-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="84dd4-146">Profilen inneholder personlige opplysninger, informasjon om arbeidserfaring, opplysninger om utdannelse, dokumenter, koblinger og informasjon om kompetanse.</span><span class="sxs-lookup"><span data-stu-id="84dd4-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="84dd4-147">Når det opprettes en profil, kan den brukes til å søke på jobber som kandidaten er interessert i.</span><span class="sxs-lookup"><span data-stu-id="84dd4-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="84dd4-148">Profiler også hjelpe Attract med å anbefale de rette jobbene for kandidater.</span><span class="sxs-lookup"><span data-stu-id="84dd4-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="84dd4-149">Finne riktig jobb</span><span class="sxs-lookup"><span data-stu-id="84dd4-149">Find the right job</span></span>

<span data-ttu-id="84dd4-150">På jobblistesiden kan kandidater søke etter en bestemt jobb ved å skrive inn søkeord.</span><span class="sxs-lookup"><span data-stu-id="84dd4-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="84dd4-151">Søkefunksjonaliteten ser etter søketermene i stillingsbetegnelser og jobbeskrivelser, og viser relevante jobber som resultater.</span><span class="sxs-lookup"><span data-stu-id="84dd4-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="84dd4-152">Kandidater kan filtrere resultatene når som helst basert på jobbplasseringen eller jobbfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="84dd4-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="84dd4-153">Kandidater kan også vise et sett med anbefalte jobber på karriereområdet.</span><span class="sxs-lookup"><span data-stu-id="84dd4-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="84dd4-154">Jobbene som anbefales til en kandidat, er basert på kandidatens tidligere søknader, profil og CVer.</span><span class="sxs-lookup"><span data-stu-id="84dd4-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="84dd4-155">Jobbanbefalinger vises bare hvis minst 10 jobber er postert på karriereomrdådet, og kandidaten har fullført sin profil.</span><span class="sxs-lookup"><span data-stu-id="84dd4-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="84dd4-156">Søke på stillinger</span><span class="sxs-lookup"><span data-stu-id="84dd4-156">Apply for jobs</span></span>

<span data-ttu-id="84dd4-157">Når kandidater har funnet riktig jobb, kan de søke ved hjelp av **Søk**-knappen øverst på siden for jobbdetaljer.</span><span class="sxs-lookup"><span data-stu-id="84dd4-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="84dd4-158">Nå kan kandidater opprette en helt ny profil eller gå gjennom informasjonen i den eksisterende profilen.</span><span class="sxs-lookup"><span data-stu-id="84dd4-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="84dd4-159">Kandidater kan også laste opp en CV, etter behov, og deretter sende inn jobbsøknaden.</span><span class="sxs-lookup"><span data-stu-id="84dd4-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="84dd4-160">Kontrollere søknadsstatus</span><span class="sxs-lookup"><span data-stu-id="84dd4-160">Check application status</span></span>

<span data-ttu-id="84dd4-161">Når kandidater har søkt på én eller flere jobber, kan de velge **Søknader** i navigasjonsfeltet øverst på siden for å vise åpne og lukkede søknader.</span><span class="sxs-lookup"><span data-stu-id="84dd4-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="84dd4-162">Når kandidater åpner en av søknadene, ser de gjeldende stadium og ventende handlingselementer de må fullføre.</span><span class="sxs-lookup"><span data-stu-id="84dd4-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="84dd4-163">Hvis en kandidat må oppgi potensielle datoer for et personlig intervju, viser for eksempel siden hans eller hennes alternativer.</span><span class="sxs-lookup"><span data-stu-id="84dd4-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="84dd4-164">Interne stillinger</span><span class="sxs-lookup"><span data-stu-id="84dd4-164">Internal jobs</span></span>

<span data-ttu-id="84dd4-165">Jobber som er merket som interne og er postert til Attract-karriereområdet, vises for øyeblikket ikke på karriereområdet.</span><span class="sxs-lookup"><span data-stu-id="84dd4-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="84dd4-166">De er bare tilgjengelig via den direkte **Søk**-URL-adressen som kan kopieres fra programmet Attract.</span><span class="sxs-lookup"><span data-stu-id="84dd4-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>


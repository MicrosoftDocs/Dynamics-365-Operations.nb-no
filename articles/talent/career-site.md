---
title: Karriereområde-funksjonalitet i Attract
description: Dette emnet gir en oversikt over den kandidatrettede karriereområde-funksjonaliteten i Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/13/2019
ms.locfileid: "389978"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="16c63-103">Karriereområde-funksjonalitet i Attract</span><span class="sxs-lookup"><span data-stu-id="16c63-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="16c63-104">Dette emnet gir en oversikt over den kandidatrettede karriereområde-funksjonaliteten i Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="16c63-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="16c63-105">Den forklarer også hvordan du konfigurerer denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="16c63-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="16c63-106">Attract inneholder ett karriereområde for hvert miljø i en leier.</span><span class="sxs-lookup"><span data-stu-id="16c63-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="16c63-107">Hvis en organisasjon for eksempel har et utviklingsmiljø og et testmiljø, klargjøres ett karriereområde for utviklingsmiljøet og et annet karriereområde klargjøres for testmiljøet.</span><span class="sxs-lookup"><span data-stu-id="16c63-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="16c63-108">Hvert karriereområde er fullstendig isolert og har sin egen godkjenningsmekanisme.</span><span class="sxs-lookup"><span data-stu-id="16c63-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="16c63-109">Jobber og kandidatprofiler deles ikke mellom karriereområder.</span><span class="sxs-lookup"><span data-stu-id="16c63-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="16c63-110">Som standard er karriereområdet offentlig.</span><span class="sxs-lookup"><span data-stu-id="16c63-110">By default, the career site is public.</span></span> <span data-ttu-id="16c63-111">Derfor kan kandidater vise alle jobbene som er merket som eksterne, uten å måtte logge på.</span><span class="sxs-lookup"><span data-stu-id="16c63-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="16c63-112">Alle andre handlinger krever imidlertid at kandidater logger på.</span><span class="sxs-lookup"><span data-stu-id="16c63-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="16c63-113">Karrierestedsledelse</span><span class="sxs-lookup"><span data-stu-id="16c63-113">Career site management</span></span>

<span data-ttu-id="16c63-114">Hvis du vil angi verdier for følgende elementer, logger du deg på Attract som administrator, velger **Administrasjonssenter** på **Innstillinger**-menyen (tannhjulsymbolet), og velger deretter **Firmainformasjon**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="16c63-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="16c63-115">**Organisasjonsnavn** – Organisasjonsnavnet vises i navigasjonsfeltet øverst i karriereområdet.</span><span class="sxs-lookup"><span data-stu-id="16c63-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="16c63-116">Ved å velge navnet på organisasjonen går kandidater til en side som viser alle åpne jobber.</span><span class="sxs-lookup"><span data-stu-id="16c63-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="16c63-117">**Organisasjonslogo** – Et bilde av organisasjonens logo vises øverst til venstre for karriereområdet.</span><span class="sxs-lookup"><span data-stu-id="16c63-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="16c63-118">Ved å velge logobildet går kandidater til en side som viser alle åpne jobber.</span><span class="sxs-lookup"><span data-stu-id="16c63-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="16c63-119">Logobildet som vises på karriereområdet, har en fast høyde på 20 piksler.</span><span class="sxs-lookup"><span data-stu-id="16c63-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="16c63-120">Bildet du legger til i administrasjonssenteret, skaleres slik at det passer.</span><span class="sxs-lookup"><span data-stu-id="16c63-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="16c63-121">Avhengig av bildet kan derfor bredden endres.</span><span class="sxs-lookup"><span data-stu-id="16c63-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="16c63-122">Hvis du vil angi verdier for følgende elementer, logger du deg på Attract som administrator, velger **Administrasjonssenter** på **Innstillinger**-menyen og velger deretter **Karrierestedsledelse**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="16c63-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="16c63-123">**Optimalisering av søkemotor** – Når aktivert er alle offentlige jobber som er postert til Attract-karriereområdet, søkbare ved hjelp av søkemotorer som Bing og Google.</span><span class="sxs-lookup"><span data-stu-id="16c63-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="16c63-124">Det kan være en forsinkelse fra aktivering av denne innstillingen til at søkeresultatene vises, avhengig av søkemotoren du bruker.</span><span class="sxs-lookup"><span data-stu-id="16c63-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="16c63-125">URL-adresser for karriereområde</span><span class="sxs-lookup"><span data-stu-id="16c63-125">Career site URLs</span></span>

<span data-ttu-id="16c63-126">Følgende liste inneholder vanlige URL-adresser for karriereområde og hvordan du åpner dem.</span><span class="sxs-lookup"><span data-stu-id="16c63-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="16c63-127">**URL-adresse til hjemmeside for karriereområde** – Hvis du vil vise URL-adressen til hjemmesiden for karriereområdet, logger du på Attract som administrator, velger **Administrasjonssenter** på **Innstillinger**-menyen og velger deretter **Karrierestedsledelse**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="16c63-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="16c63-128">**Søk-URL for individuell jobbutlysning** – Når du [posterer en ekstern jobb](Creating-jobs-Attract.md#postings) for første gang, kan du kopiere **Søk**-koblingen fra programmet Attract.</span><span class="sxs-lookup"><span data-stu-id="16c63-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="16c63-129">URL-adressen for denne koblingen vil være i følgende format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="16c63-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="16c63-130">**URL-adresse til jobbutlysning** – URL-adressen til jobbutlysningen er en delstreng til Søk-URL-en.</span><span class="sxs-lookup"><span data-stu-id="16c63-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="16c63-131">Den består av alt opp til og med jobbnummeret.</span><span class="sxs-lookup"><span data-stu-id="16c63-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="16c63-132">For den foregående Søk-URL-adressen er derfor URL-adressen for jobbutlysningen [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="16c63-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="16c63-133">Godkjenningsalternativer</span><span class="sxs-lookup"><span data-stu-id="16c63-133">Authentication options</span></span>

<span data-ttu-id="16c63-134">Kandidater har følgende alternativer for pålogging for et Attract-karriereområde:</span><span class="sxs-lookup"><span data-stu-id="16c63-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="16c63-135">Personlig konto:</span><span class="sxs-lookup"><span data-stu-id="16c63-135">Personal account:</span></span>

    -   <span data-ttu-id="16c63-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="16c63-136">LinkedIn</span></span>

    -   <span data-ttu-id="16c63-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="16c63-137">Microsoft</span></span>

    -   <span data-ttu-id="16c63-138">Google</span><span class="sxs-lookup"><span data-stu-id="16c63-138">Google</span></span>

    -   <span data-ttu-id="16c63-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="16c63-139">Facebook</span></span>

-   <span data-ttu-id="16c63-140">Jobb- eller skolekonto:</span><span class="sxs-lookup"><span data-stu-id="16c63-140">Work or school account:</span></span>

    -   <span data-ttu-id="16c63-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="16c63-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="16c63-142">Azure AD-påloggingen er bare beregnet for interne kandidater.</span><span class="sxs-lookup"><span data-stu-id="16c63-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="16c63-143">Derfor fungerer den bare for interne kandidater som bruker Azure AD-legitimasjonen for firmaet.</span><span class="sxs-lookup"><span data-stu-id="16c63-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="16c63-144">Eksempel: En kandidat som for tiden er ansatt hos Contoso Ltd., vil søke på en jobb i et ikke-relatert firma, Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="16c63-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="16c63-145">I dette tilfellet vil ikke påloggingen lykkes hvis den ansatte prøver å bruke Azure AD-legitimasjonen fra Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="16c63-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="16c63-146">Opprette og vedlikeholde en profil</span><span class="sxs-lookup"><span data-stu-id="16c63-146">Create and maintain a profile</span></span>

<span data-ttu-id="16c63-147">Etter at kandidater har logget på karriereområdet, kan de velge **Min profil** i navigasjonsfeltet øverst på siden for å opprette og vedlikeholde profilen.</span><span class="sxs-lookup"><span data-stu-id="16c63-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="16c63-148">Profilen inneholder personlige opplysninger, informasjon om arbeidserfaring, opplysninger om utdannelse, dokumenter, koblinger og informasjon om kompetanse.</span><span class="sxs-lookup"><span data-stu-id="16c63-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="16c63-149">Når det opprettes en profil, kan den brukes til å søke på jobber som kandidaten er interessert i.</span><span class="sxs-lookup"><span data-stu-id="16c63-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="16c63-150">Profiler hjelper også Attract med å anbefale de rette jobbene for kandidater.</span><span class="sxs-lookup"><span data-stu-id="16c63-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="16c63-151">Hvis en kandidat bruker en e-post-ID til å logge på med en av godkjenningsleverandørene ovenfor, vil denne e-post-IDen som standard gå til kontaktens e-post-ID som er knyttet til profilen.</span><span class="sxs-lookup"><span data-stu-id="16c63-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="16c63-152">Den sistnevnte endres imidlertid endres når som helst og er fullstendig uavhengig av den tidligere.</span><span class="sxs-lookup"><span data-stu-id="16c63-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="16c63-153">Attract vil alltid bruke kontaktens e-post-ID til å knytte til profilen din for alle e-postmeldinger.</span><span class="sxs-lookup"><span data-stu-id="16c63-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="16c63-154">Finne riktig jobb</span><span class="sxs-lookup"><span data-stu-id="16c63-154">Find the right job</span></span>

<span data-ttu-id="16c63-155">På jobblistesiden kan kandidater søke etter en bestemt jobb ved å skrive inn søkeord.</span><span class="sxs-lookup"><span data-stu-id="16c63-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="16c63-156">Søkefunksjonaliteten ser etter søketermene i stillingsbetegnelser og jobbeskrivelser og viser relevante jobber som resultater.</span><span class="sxs-lookup"><span data-stu-id="16c63-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="16c63-157">Kandidater kan filtrere resultatene når som helst basert på jobbplasseringen eller jobbfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="16c63-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="16c63-158">Kandidater kan også vise et sett med anbefalte jobber på karriereområdet.</span><span class="sxs-lookup"><span data-stu-id="16c63-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="16c63-159">Jobbene som anbefales til en kandidat, er basert på kandidatens tidligere søknader, profil og CVer.</span><span class="sxs-lookup"><span data-stu-id="16c63-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="16c63-160">Jobbanbefalinger vises bare hvis minst 10 jobber er postert på karriereområdet og kandidaten har fullført en profil.</span><span class="sxs-lookup"><span data-stu-id="16c63-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="16c63-161">Søke på stillinger</span><span class="sxs-lookup"><span data-stu-id="16c63-161">Apply for jobs</span></span>

<span data-ttu-id="16c63-162">Når kandidater har funnet riktig jobb, kan de søke ved hjelp av **Søk**-knappen på siden for **Jobbdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="16c63-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="16c63-163">Nå kan kandidater opprette en ny profil eller gå gjennom informasjonen i den eksisterende profilen.</span><span class="sxs-lookup"><span data-stu-id="16c63-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="16c63-164">Kandidater kan også laste opp en CV, etter behov, og deretter sende inn jobbsøknaden.</span><span class="sxs-lookup"><span data-stu-id="16c63-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="16c63-165">Kontrollere søknadsstatus</span><span class="sxs-lookup"><span data-stu-id="16c63-165">Check application status</span></span>

<span data-ttu-id="16c63-166">Når kandidater har søkt på én eller flere jobber, kan de velge **Søknader** i navigasjonsfeltet øverst på siden for å vise åpne og lukkede søknader.</span><span class="sxs-lookup"><span data-stu-id="16c63-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="16c63-167">Når kandidater åpner en av søknadene, ser de gjeldende stadium og ventende handlingselementer de må fullføre.</span><span class="sxs-lookup"><span data-stu-id="16c63-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="16c63-168">Hvis en kandidat må oppgi potensielle datoer for et personlig intervju, viser for eksempel siden tilgjengelige alternativer.</span><span class="sxs-lookup"><span data-stu-id="16c63-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="16c63-169">Interne stillinger</span><span class="sxs-lookup"><span data-stu-id="16c63-169">Internal jobs</span></span>

<span data-ttu-id="16c63-170">Jobber som er merket som interne og er postert til Attract-karriereområdet, vises for øyeblikket ikke på karriereområdet.</span><span class="sxs-lookup"><span data-stu-id="16c63-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="16c63-171">De er bare tilgjengelige via den direkte **Søk**-URL-adressen som kan kopieres fra programmet Attract.</span><span class="sxs-lookup"><span data-stu-id="16c63-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>

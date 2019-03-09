---
title: Leverandører med LinkedIn-rekrutterer
description: Dette emnet gir informasjon om hvordan du bruker maskinlæring til å få jobb- og kandidatanbefalinger for jobb.
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 9bb323728923ff3b09ff0bfba3849f3c5d84eb34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305581"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="b1804-103">Leverandører med LinkedIn-rekrutterer</span><span class="sxs-lookup"><span data-stu-id="b1804-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="b1804-104">LinkedIn er verdens største talentdatabase og er ofte hovedsystemet som rekrutteringspersoner bruker til å finne, kommunisere med og velge kandidater for jobbene som rekrutteringspersoner vil fylle.</span><span class="sxs-lookup"><span data-stu-id="b1804-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="b1804-105">Integrering med LinkedIn-rekrutterer med Dynamics 365 for Talent: Attract gjør det enklere for brukere å ansette og holde dataene synkronisert mellom de to systemene.</span><span class="sxs-lookup"><span data-stu-id="b1804-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="b1804-106">Du trenger tillegget for omfattende ansettelse og LinkedIn-rekruttererplasser for å kunne bruke integrering med LinkedIn-rekrutterer med Attract.</span><span class="sxs-lookup"><span data-stu-id="b1804-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="b1804-107">Definere LinkedIn-rekrutterer med Attract</span><span class="sxs-lookup"><span data-stu-id="b1804-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="b1804-108">Før du kan bruke LinkedIn-rekruttererfunksjonene, må du konfigurere tilgang på kontraktnivå eller firmanivå med Attract-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="b1804-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="b1804-109">For å fullføre konfigurasjonen må du arbeide med brukeren som er en administrator på LinkedIn-rekrutteringskontrakten.</span><span class="sxs-lookup"><span data-stu-id="b1804-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="b1804-110">Fullfør fremgangsmåten nedenfor for å konfigurere LinkedIn-rekrutterer med Attract.</span><span class="sxs-lookup"><span data-stu-id="b1804-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="b1804-111">Logg på Attract som administrator, og gå til **Administrasjonsinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="b1804-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="b1804-112">I ruten til venstre klikker du på kategorien **LinkedIn-integrering**.</span><span class="sxs-lookup"><span data-stu-id="b1804-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="b1804-113">[![Attract-administratorvisning for å starte LinkedIn-rekruttererintegrering](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="b1804-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="b1804-114">Klikk på **Koble til** for å starte oppsettet og bli veiledet gjennom prosessen for LinkedIn-pålogging.</span><span class="sxs-lookup"><span data-stu-id="b1804-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="b1804-115">Hvis du har plasser i flere LinkedIn-kontrakter, velger du kontrakten du vil koble til Attract-systemet.</span><span class="sxs-lookup"><span data-stu-id="b1804-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="b1804-116">Hvis du har en plass i bare én LinkedIn-kontrakt, vil ikke dette trinnet være nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b1804-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="b1804-117">LinkedIn-kontrollprogrammet lastes nå i administrasjonsinnstillingene og viser listen over integreringer.</span><span class="sxs-lookup"><span data-stu-id="b1804-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="b1804-118">Under **Tilkobling til rekrutteringssystem** klikker du **Forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="b1804-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="b1804-119">[![Attract-administratorvisning for å be om integrering med LinkedIn-rekrutterer](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b1804-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="b1804-120">Etter at integreringen er forespurt fra Attract, vises det som **Partner klar** og er klar til å aktiveres fra **Administrasjonsinnstillinger for rekrutterer**.</span><span class="sxs-lookup"><span data-stu-id="b1804-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="b1804-121">Hvis du ser **Varsle partner** på denne siden, venter du litt, klikker på **Varsle partner** og oppdaterer deretter siden.</span><span class="sxs-lookup"><span data-stu-id="b1804-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="b1804-122">Den skal nå vises som **Partner klar**.</span><span class="sxs-lookup"><span data-stu-id="b1804-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="b1804-123">[![Attact-administratorvisning for å angi at Attract-siden av forespørsler er fullført](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b1804-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="b1804-124">For å fullføre neste trinn må du ha en administratorrettighet i LinkedIn-rekruttererkontrakten.</span><span class="sxs-lookup"><span data-stu-id="b1804-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="b1804-125">Logg på LinkedIn med administratorkontoen og gå til LinkedIn-rekrutterer øverst til høyre.</span><span class="sxs-lookup"><span data-stu-id="b1804-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="b1804-126">På **Flere**-menyen øverst på skjermen klikker du på **Administrasjonsinnstillinger**, og klikker deretter på **ATS**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="b1804-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="b1804-127">Attract-systemet vises med et par alternativer som kan aktiveres.</span><span class="sxs-lookup"><span data-stu-id="b1804-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="b1804-128">Hvis du bare vil aktivere 1-klikk-eksport for kontrollprogrammet **In-ATS indicator** og **In-ATS Profile**, velger du **Tilgang på firmanivå**.</span><span class="sxs-lookup"><span data-stu-id="b1804-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="b1804-129">Hvis du vil aktivere alle tilgangsfunksjoner på firmanivå pluss InMail-logg, Merknader-logg og InMail-stub-profiltilgang, velger du **Tilgang på kontraktnivå**.</span><span class="sxs-lookup"><span data-stu-id="b1804-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="b1804-130">Slå på ønsket tilgangsnivå fra LinkedIn-rekrutterer **Admin-ATS**-innstillingene.</span><span class="sxs-lookup"><span data-stu-id="b1804-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="b1804-131">[![Slå på Attract-integrering fra administratorvisningen for LinkedIn-rekrutterer](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b1804-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="b1804-132">Gå tilbake til Attract-administatorinnstillinger som en Attract-administrator og velg kategorien **LinkedIn-integrering**. Nå skal du se at LinkedIn-kontrollprogrammet lastes inn og viser **Aktivert** med det valgte tilgangsnivået aktivert.</span><span class="sxs-lookup"><span data-stu-id="b1804-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="b1804-133">[![LinkedIn-rekruttererintegrering er fullført](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="b1804-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="b1804-134">Bruke LinkedIn-rekruttererfunksjoner</span><span class="sxs-lookup"><span data-stu-id="b1804-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="b1804-135">Når LinkedIn-rekruttererfunksjonene er aktivert av Attract-administratoren, er de tilgjengelig for ansettelsesansvarlige og rekrutterere.</span><span class="sxs-lookup"><span data-stu-id="b1804-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="b1804-136">Hvis du vil bruke disse funksjonene, kan du koble til LinkedIn-kontoen under **Brukerinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="b1804-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="b1804-137">Flere funksjoner vil være tilgjengelige når både adminator- og brukerinnstillinger er tilkoblet.</span><span class="sxs-lookup"><span data-stu-id="b1804-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="b1804-138">In-ATS Profile-kontrollprogram</span><span class="sxs-lookup"><span data-stu-id="b1804-138">In-ATS profile widget</span></span>

<span data-ttu-id="b1804-139">Du kan vise den kandidatens LinkedIn-profil i Attract.</span><span class="sxs-lookup"><span data-stu-id="b1804-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="b1804-140">LinkedIn-kontrollprogrammet viser kandidatprofilen når ATS-informasjonen samsvarer med LinkedIn-informasjonen til brukerne.</span><span class="sxs-lookup"><span data-stu-id="b1804-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="b1804-141">Hvis du vil vise en profil, går du til kandidatprofilen fra et jobb- eller talentutvalg.</span><span class="sxs-lookup"><span data-stu-id="b1804-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="b1804-142">I kandidatprofilen velger du den **LinkedIn**-kategorien, og profil-kontrollprogrammet lastes inn.</span><span class="sxs-lookup"><span data-stu-id="b1804-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="b1804-143">Du kan også lagre kandidaten i LinkedIn-rekruttererprosjektene fra denne siden.</span><span class="sxs-lookup"><span data-stu-id="b1804-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="b1804-144">Hvis LinkedIn fant treff basert på e-post og LinkedIn-medlems-ID (nøyaktig samsvar), vises kandidatens profil.</span><span class="sxs-lookup"><span data-stu-id="b1804-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="b1804-145">Brukeren har fortsatt et valg for å koble til / koble fra profilen.</span><span class="sxs-lookup"><span data-stu-id="b1804-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="b1804-146">Hvis LinkedIn ikke finner kandidaten basert på e-posten eller medlems-ID-en, vises en liste over potensielle kandidattreff basert på kandidatens navn, og brukeren kan velge ett av dem og koble til profilen.</span><span class="sxs-lookup"><span data-stu-id="b1804-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="b1804-147">Hvis LinkedIn ikke finner en kandidat basert på navnet, returneres det at ingen treff ble funnet.</span><span class="sxs-lookup"><span data-stu-id="b1804-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="b1804-148">1-klikk-eksport</span><span class="sxs-lookup"><span data-stu-id="b1804-148">1-click export</span></span> 

<span data-ttu-id="b1804-149">Under utvelgelsen av kandidater i LinkedIn, kan du eksportere kandidaten til jobbene som du har åpne, med ett klikk.</span><span class="sxs-lookup"><span data-stu-id="b1804-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="b1804-150">Bruk følgende fremgangsmåte for å utføre eksport med ett klikk.</span><span class="sxs-lookup"><span data-stu-id="b1804-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="b1804-151">Før du fullfører denne fremgangsmåten, kontrollerer du at du er en tilordnet rollen som ansettelsesansvarlig eller rekrutterer for jobben, og at jobben har et **Kundeemne**-stadium.</span><span class="sxs-lookup"><span data-stu-id="b1804-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="b1804-152">Opprett jobben, tilordne de riktige rollene og aktiverer jobben.</span><span class="sxs-lookup"><span data-stu-id="b1804-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="b1804-153">Når jobben er aktivert, kan du gå til LinkedIn-rekrutterer.</span><span class="sxs-lookup"><span data-stu-id="b1804-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="b1804-154">Finn kandidaten du leter etter, og gå til den aktuelle profilen.</span><span class="sxs-lookup"><span data-stu-id="b1804-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="b1804-155">Bruk jobbsøk-boksen i kontaktkortet til å finne jobben ved hjelp av tittelen eller jobb-IDen som ble aktivert i Attract.</span><span class="sxs-lookup"><span data-stu-id="b1804-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="b1804-156">Hvis du ikke finner jobben, klikker du **Endre ATS** for å finne den riktige Attract-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="b1804-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="b1804-157">Når jobben er merket, klikker du **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="b1804-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="b1804-158">Kandidaten hentes nå av Attract.</span><span class="sxs-lookup"><span data-stu-id="b1804-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="b1804-159">Gå til Attract og åpne den aktuelle jobben.</span><span class="sxs-lookup"><span data-stu-id="b1804-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="b1804-160">Du finner kandidaten du nettopp eksporterte, i **Kundeemne**-stadiet for jobben.</span><span class="sxs-lookup"><span data-stu-id="b1804-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="b1804-161">In-ATS-indikator</span><span class="sxs-lookup"><span data-stu-id="b1804-161">In-ATS indicator</span></span> 

<span data-ttu-id="b1804-162">Ved hjelp av LinkedIn-rekrutterer kan du kontrollere om en kandidat har søkt på andre jobber i organisasjonen, se hvor de er i forskjellige faser av jobbsøknader, og vise tilbakemeldinger og kommentarer fra Attract i LinkedIn-rekrutterer.</span><span class="sxs-lookup"><span data-stu-id="b1804-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="b1804-163">Åpne LinkedIn-rekrutterer og finn kandidatprofilen du leter etter.</span><span class="sxs-lookup"><span data-stu-id="b1804-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="b1804-164">Bla ned for å se **In-ATS**-delen på kandidatens profil.</span><span class="sxs-lookup"><span data-stu-id="b1804-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="b1804-165">Du kan bruke dette kontrollprogrammet til å vise all informasjon om kandidaten som finnes i Attract fra LinkedIn-rekruttervisningen.</span><span class="sxs-lookup"><span data-stu-id="b1804-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="b1804-166">Velg **Jobber og statuser**-kategorien for å vise jobbene de er en del av, den siste statusen og hvordan de har flyttet mot hver jobb.</span><span class="sxs-lookup"><span data-stu-id="b1804-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="b1804-167">Velg **Intervjutilbakemelding**-kategorien for å se tilbakemeldinger som intervjuerne har sendt i Attract.</span><span class="sxs-lookup"><span data-stu-id="b1804-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="b1804-168">Velg **Merknader**-kategorien for å vise merknader som er registrert for denne søkeren i Attract.</span><span class="sxs-lookup"><span data-stu-id="b1804-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="b1804-169">Kandidat- og søknadsdata blir ikke synkronisert til LinkedIn Recruiter hvis kandidaten ikke er forbi jobbkandidatfasen.</span><span class="sxs-lookup"><span data-stu-id="b1804-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="b1804-170">InMail-historikk</span><span class="sxs-lookup"><span data-stu-id="b1804-170">InMail history</span></span>

<span data-ttu-id="b1804-171">LinkedIn InMail-loggen er tilgjengelig med tilgang på kontraktnivå med LinkedIn-rekrutterer.</span><span class="sxs-lookup"><span data-stu-id="b1804-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b1804-172">Når den er aktivert, kan du vise hele InMail-loggen for kandidaten.</span><span class="sxs-lookup"><span data-stu-id="b1804-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="b1804-173">Du kan også se hvem andre fra organisasjonen som har utvekslet InMail med kandidaten, men du ikke kan vise meldinger mellom dem.</span><span class="sxs-lookup"><span data-stu-id="b1804-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="b1804-174">Hvis du vil vise InMail-loggen, går du til en kandidats profil, går til **LinkedIn**-kategorien og blar til bunnen av siden for å vise loggen.</span><span class="sxs-lookup"><span data-stu-id="b1804-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b1804-175">Du kan vise InMail-historikken hvis du har hatt en diskusjon med kandidaten.</span><span class="sxs-lookup"><span data-stu-id="b1804-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="b1804-176">Meldinger fra InMail synkroniseres med Attract annenhver time.</span><span class="sxs-lookup"><span data-stu-id="b1804-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="b1804-177">Notatlogg</span><span class="sxs-lookup"><span data-stu-id="b1804-177">Notes history</span></span> 

<span data-ttu-id="b1804-178">LinkedIn-notatloggen er tilgjengelig med tilgang på kontraktnivå med LinkedIn-rekrutterer.</span><span class="sxs-lookup"><span data-stu-id="b1804-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b1804-179">Når den er aktivert, kan du vise merknadene som er registrert om kandidaten som av ulike rekrutterere fra organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="b1804-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="b1804-180">Hvis du vil vise notatloggen, går du til en kandidats profil, går til **LinkedIn**-kategorien og blar til bunnen av siden for å vise loggen.</span><span class="sxs-lookup"><span data-stu-id="b1804-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b1804-181">Du kan vise alle merknadene om kandidaten fra LinkedIn-rekruttereren.</span><span class="sxs-lookup"><span data-stu-id="b1804-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="b1804-182">InMail-stub-profil</span><span class="sxs-lookup"><span data-stu-id="b1804-182">InMail stub profile</span></span>

<span data-ttu-id="b1804-183">InMail-stub-profilen er tilgjengelig med tilgang på kontraktnivå med LinkedIn-rekrutterer.</span><span class="sxs-lookup"><span data-stu-id="b1804-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b1804-184">Hvis kandidater er enige om å dele sine LinkedIn-profiler med alle brukere i organisasjonen, kan du spore kandidater i Attract, så opprettes en ny kandidatpost for hver kandidat.</span><span class="sxs-lookup"><span data-stu-id="b1804-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="b1804-185">Du kan vise kandidatens e-postadresse hvis kandidaten allerede finnes i systemet med en e-postadresse, eller har valgt å dele e-postadressen med rekruttereren.</span><span class="sxs-lookup"><span data-stu-id="b1804-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="b1804-186">Hvis du vil vise listen over kandidater, kan du gå til **Talentutvalg** for å se et systemopprettet LinkedIn-talentutvalg.</span><span class="sxs-lookup"><span data-stu-id="b1804-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="b1804-187">Dette talentutvalget inneholder listen over kandidater og stub-profiler som mottatt fra LinkedIn, og viser kandidatens fornavn og etternavn.</span><span class="sxs-lookup"><span data-stu-id="b1804-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="b1804-188">Kandidatens e-post-ID vises hvis kandidaten har valgt å dele e-postadressen.</span><span class="sxs-lookup"><span data-stu-id="b1804-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

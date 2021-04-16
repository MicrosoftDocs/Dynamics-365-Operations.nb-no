---
title: Rekruttere jobbkandidater
description: Dette emnet beskriver hvordan du rekrutterer kandidater i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9259cfa78d65f36da653c807a66e291b3cb01c63
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802533"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="faa54-103">Rekruttere jobbkandidater</span><span class="sxs-lookup"><span data-stu-id="faa54-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="faa54-104">Dynamics 365 Human Resources hjelper deg med å administrere rekrutteringsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="faa54-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="faa54-105">Den hjelper deg også med overgangen fra jobbkandidater til ansatte på en sømløs måte.</span><span class="sxs-lookup"><span data-stu-id="faa54-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="faa54-106">Hvis organisasjonen bruker et separat rekrutteringsprogram, kan rekrutteringsprosessen omfatte følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="faa54-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="faa54-107">Angi rekrutteringsforespørselen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="faa54-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="faa54-108">Motta kandidatreferanser i Human Resources fra rekrutteringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="faa54-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="faa54-109">Fullfør kandidatgodkjenningsprosessen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="faa54-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="faa54-110">Hvis du ikke bruker et eget rekrutteringsprogram, kan du også administrere kandidater manuelt i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="faa54-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="faa54-111">Hvis du er administrator eller utvikler og vil integrere Human Resources med et tredjeparts rekrutteringsprogram, kan du se [Konfigurer Dataverse-integrering](hr-admin-integration-common-data-service.md) og [Konfigurer virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="faa54-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="faa54-112">Du kan også finne rekrutteringsintegreringsprogrammer på [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="faa54-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="faa54-113">Hvis du vil teste forhåndsversjonen for integrering med LinkedIn Talent Hub, kan du se [Integrer med LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="faa54-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="faa54-114">Aktiver rekrutteringsforespørsler</span><span class="sxs-lookup"><span data-stu-id="faa54-114">Enable recruiting requests</span></span>

<span data-ttu-id="faa54-115">Hvis du vil sende rekrutteringsforespørsler i Human Resources, må du først aktivere funksjonaliteten i **Delte parametere for Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="faa54-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="faa54-116">I arbeidsområdet **Personaladministrasjon** velger du **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="faa54-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="faa54-117">Under **Oppsett** velger du **delte parametere for Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="faa54-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="faa54-118">I fanen **Rekruttering**, under **REKRUTTERING** setter **Aktiver rekrutteringsforespørsler** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="faa54-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="faa54-119">Legg til en rekrutteringsforespørselssted</span><span class="sxs-lookup"><span data-stu-id="faa54-119">Add a recruiting request location</span></span>

<span data-ttu-id="faa54-120">Hvis organisasjonen har flere steder, kan du legge dem til slik at anmodere kan velge et sted der den nye rekrutten skal fungere.</span><span class="sxs-lookup"><span data-stu-id="faa54-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="faa54-121">Stedet vil bli inkludert i prosjektbokføringen.</span><span class="sxs-lookup"><span data-stu-id="faa54-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="faa54-122">Angi **rekrutteringsforespørselssted** i søkefeltet.</span><span class="sxs-lookup"><span data-stu-id="faa54-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="faa54-123">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="faa54-123">Select **New**.</span></span>

3. <span data-ttu-id="faa54-124">I feltet **Rekrutteringsforespørselssted** angir du stedsnavnet.</span><span class="sxs-lookup"><span data-stu-id="faa54-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Legg til en rekrutteringsforespørselssted](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="faa54-126">I **beskrivelsen** skriver du inn en beskrivelse for stedet.</span><span class="sxs-lookup"><span data-stu-id="faa54-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="faa54-127">Under **Sted** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="faa54-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="faa54-128">Hvis den meldingen **Ny adresse** vises, angir du adressen til stedet.</span><span class="sxs-lookup"><span data-stu-id="faa54-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Angi adresse](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="faa54-130">Angi informasjonen for stedets kontakt under **Kontaktinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="faa54-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="faa54-131">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="faa54-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="faa54-132">Legg til en rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="faa54-132">Add a recruiting request</span></span>

<span data-ttu-id="faa54-133">Ledere kan sende inn rekrutteringsforespørsler i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="faa54-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="faa54-134">Hvis du bruker et separat rekrutteringsprogram, vil denne fremgangsmåten sende en rekrutteringsforespørsel og starte rekrutteringsprosessen i dette programmet.</span><span class="sxs-lookup"><span data-stu-id="faa54-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="faa54-135">Hvis ikke kan du fullføre denne fremgangsmåten for å starte arbeidsflyten for din egen interne rekrutteringsprosess.</span><span class="sxs-lookup"><span data-stu-id="faa54-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="faa54-136">Velg **Selvbetjening for ansatte**.</span><span class="sxs-lookup"><span data-stu-id="faa54-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="faa54-137">Velg fanen **Mitt team**.</span><span class="sxs-lookup"><span data-stu-id="faa54-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="faa54-138">Velg **Forespørsel om å rekruttere**.</span><span class="sxs-lookup"><span data-stu-id="faa54-138">Select  **Request to recruit**.</span></span>

   ![Start en rekrutteringsforespørsel](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="faa54-140">Fyll ut feltene **Beskrivelse**, **Jobb** og **Beregnet startdato**.</span><span class="sxs-lookup"><span data-stu-id="faa54-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Fullfør rekrutteringsforespørselen](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="faa54-142">Velg **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="faa54-142">Select **Continue**.</span></span> <span data-ttu-id="faa54-143">Rekrutteringsforespørselen for stillingen din vises.</span><span class="sxs-lookup"><span data-stu-id="faa54-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="faa54-144">Under **Generelt** velger du en rekrutterer fra rullegardinlisten **Rekrutterer**, og deretter velger du et sted fra rullegardinlisten **Rekrutteringsforespørselssted**.</span><span class="sxs-lookup"><span data-stu-id="faa54-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="faa54-145">Endre eventuell informasjon etter behov under **Jobb**, og velg deretter **Opprett detaljer fra jobb**.</span><span class="sxs-lookup"><span data-stu-id="faa54-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Opprett detaljer fra jobb](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="faa54-147">Resten av rekrutteringsforespørselen vil bli fylt ut med standardinformasjonen for jobben du angav.</span><span class="sxs-lookup"><span data-stu-id="faa54-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="faa54-148">Under **Ekstern beskrivelse** angir du en ekstern jobbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="faa54-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="faa54-149">Under **Stillinger** velger du **Legg til**, og deretter velger du en stilling for denne rekrutteringsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="faa54-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Legg til en stilling](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="faa54-151">Under **Ferdigheter** velger du **Legg til** og velger deretter en ferdighet.</span><span class="sxs-lookup"><span data-stu-id="faa54-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="faa54-152">Under **Krav til utdannelse** velger du **Legg til**, og deretter velger du verdier fra rullegardinlistene **Utdanning** og **Utdanningsnivå**.</span><span class="sxs-lookup"><span data-stu-id="faa54-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Legg til krav til utdanning](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="faa54-154">Legg til kommentarer etter behov under **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="faa54-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="faa54-155">Under **Kompensasjon** velger du et nivå fra rullegardinlisten **Nivå**, og justerer deretter **Lav terskel**, **Kontrollpunkt** og **Høy terskel** etter behov.</span><span class="sxs-lookup"><span data-stu-id="faa54-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="faa54-156">Når rekrutteringsforespørselen er fullført og du er klar til å starte rekrutteringsprosessen, velger du **Aktiver** på menylinjen.</span><span class="sxs-lookup"><span data-stu-id="faa54-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Aktiver rekrutteringsforespørsel](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="faa54-158">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="faa54-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="faa54-159">Vis og rediger rekrutteringsforespørsler</span><span class="sxs-lookup"><span data-stu-id="faa54-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="faa54-160">Hvis du er en leder og ønsker å vise dine egne forespørsler:</span><span class="sxs-lookup"><span data-stu-id="faa54-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="faa54-161">Velg **Selvbetjening for ansatte**.</span><span class="sxs-lookup"><span data-stu-id="faa54-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="faa54-162">Velg fanen **Mitt team**.</span><span class="sxs-lookup"><span data-stu-id="faa54-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="faa54-163">Under **Informasjon om mitt team** velger du kategorien **Rekrutteringsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="faa54-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Velg fanen Rekrutteringsforespørsler](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="faa54-165">Hvis du vil vise eller redigere en rekrutteringsforespørsel, velger du den i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="faa54-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="faa54-166">Hvis du er en HR Pro og ønsker å vise alle rekrutteringsforespørslene:</span><span class="sxs-lookup"><span data-stu-id="faa54-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="faa54-167">Velg **Personaladministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="faa54-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="faa54-168">Velg fanen **Rekrutteringsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="faa54-168">Select **Recruiting requests**.</span></span>

   ![Vise rekrutteringsforespørsler i Personaladministrasjon](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="faa54-170">Hvis du vil vise eller redigere en rekrutteringsforespørsel, velger du den i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="faa54-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="faa54-171">Legg til eller rediger en kandidatprofil</span><span class="sxs-lookup"><span data-stu-id="faa54-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="faa54-172">Hvis organisasjonen har integrert med et annet program for å administrere rekrutteringsforespørsler, blir rekrutteringsforespørsler videresendt til dette programmet.</span><span class="sxs-lookup"><span data-stu-id="faa54-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="faa54-173">Rekrutteringsprogrammet sender deretter kandidatinformasjon tilbake til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="faa54-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="faa54-174">Hvis ikke kan du følge dine egne interne rekrutteringsprosesser og legge inn kandidatinformasjon manuelt.</span><span class="sxs-lookup"><span data-stu-id="faa54-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="faa54-175">Velg **Personaladministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="faa54-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="faa54-176">Velg **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="faa54-176">Select **Links**.</span></span>

3. <span data-ttu-id="faa54-177">Under **Rekruttering** velger du **Kandidater**.</span><span class="sxs-lookup"><span data-stu-id="faa54-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Vis kandidater](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="faa54-179">Velg **Ny** for å legge til en kandidat.</span><span class="sxs-lookup"><span data-stu-id="faa54-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="faa54-180">Hvis du vil redigere en eksisterende kandidat fra listen, merker du adressen og velger **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="faa54-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="faa54-181">Kandidatprofilen vises.</span><span class="sxs-lookup"><span data-stu-id="faa54-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="faa54-182">Under **Kandidatsammendrag** legger du inn eller redigerer kandidatinformasjonen etter behov.</span><span class="sxs-lookup"><span data-stu-id="faa54-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="faa54-183">Under **Rekrutteringsforespørsel** velger du en rekrutteringsforespørsel du vil koble kandidaten til.</span><span class="sxs-lookup"><span data-stu-id="faa54-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="faa54-184">Deretter fyller du ut feltene **Beregnet startdato**, **Ansettelsessjef**, **Stilling** og **Beskrivelse** etter behov.</span><span class="sxs-lookup"><span data-stu-id="faa54-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Koble til rekrutteringsforespørsel](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="faa54-186">Fyll ut all informasjonen i følgende områder som du vil ta med i kandidatens post:</span><span class="sxs-lookup"><span data-stu-id="faa54-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="faa54-187">**Kommentarer**</span><span class="sxs-lookup"><span data-stu-id="faa54-187">**Comments**</span></span>
   - <span data-ttu-id="faa54-188">**Yrkeserfaring**</span><span class="sxs-lookup"><span data-stu-id="faa54-188">**Professional experience**</span></span>
   - <span data-ttu-id="faa54-189">**Kontaktinformasjon**</span><span class="sxs-lookup"><span data-stu-id="faa54-189">**Contact information**</span></span>
   - <span data-ttu-id="faa54-190">**Utdanning**</span><span class="sxs-lookup"><span data-stu-id="faa54-190">**Education**</span></span>
   - <span data-ttu-id="faa54-191">**Kompetanse**</span><span class="sxs-lookup"><span data-stu-id="faa54-191">**Skills**</span></span>
   - <span data-ttu-id="faa54-192">**Attester**</span><span class="sxs-lookup"><span data-stu-id="faa54-192">**Certificates**</span></span>
   - <span data-ttu-id="faa54-193">**Screeninger**</span><span class="sxs-lookup"><span data-stu-id="faa54-193">**Screenings**</span></span>

8. <span data-ttu-id="faa54-194">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="faa54-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="faa54-195">Ansett en kandidat</span><span class="sxs-lookup"><span data-stu-id="faa54-195">Hire a candidate</span></span>

<span data-ttu-id="faa54-196">Når du er klar til å ansette en kandidat, følger du denne fremgangsmåten for overgang fra kandidat til ansatt.</span><span class="sxs-lookup"><span data-stu-id="faa54-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="faa54-197">Velg **Ansett** i kandidatskjemaet.</span><span class="sxs-lookup"><span data-stu-id="faa54-197">On the candidate form, select **Hire**.</span></span>

   ![Ansett en kandidat](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="faa54-199">Fyll ut alle feltene under **Detaljer** i skjemaet **Ansett ny arbeider**.</span><span class="sxs-lookup"><span data-stu-id="faa54-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Angi detaljer for ny ansettelse](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="faa54-201">Under **Stillingsdetaljer** kan du bekrefte og endre informasjon etter behov.</span><span class="sxs-lookup"><span data-stu-id="faa54-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="faa54-202">Under **Sjekklister for jobbintroduksjon** velger du de relevante sjekklistene for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="faa54-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="faa54-203">Velg **Fortsett** for å opprette ansattposten.</span><span class="sxs-lookup"><span data-stu-id="faa54-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="faa54-204">Kandidatposten kan gå gjennom flere godkjenningstrinn før den blir til en ansattpost, avhengig av arbeidsflytene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="faa54-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="faa54-205">Bestemme deg for ikke å ansette en kandidat</span><span class="sxs-lookup"><span data-stu-id="faa54-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="faa54-206">Hvis du bestemmer deg for ikke å ansette en kandidat, kan du følge denne fremgangsmåten for å fjerne dem fra gjennomgangsprosessen.</span><span class="sxs-lookup"><span data-stu-id="faa54-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="faa54-207">Velg **Ikke ansett** i kandidatskjemaet.</span><span class="sxs-lookup"><span data-stu-id="faa54-207">On the candidate form, select **Do not hire**.</span></span>

   ![Ikke ansett kandidat](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="faa54-209">Velg en **årsakskode**, og ta med eventuelle kommentarer.</span><span class="sxs-lookup"><span data-stu-id="faa54-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="faa54-210">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="faa54-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="faa54-211">Forkast en kandidat</span><span class="sxs-lookup"><span data-stu-id="faa54-211">Dismiss a candidate</span></span>

<span data-ttu-id="faa54-212">Om nødvendig kan du forkaste en kandidat etter å ha ansatt vedkommende.</span><span class="sxs-lookup"><span data-stu-id="faa54-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="faa54-213">En kandidat kan for eksempel avvise tilbudet eller ikke dukke opp den første dagen.</span><span class="sxs-lookup"><span data-stu-id="faa54-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="faa54-214">Velg **Forkast kandidat** i kandidatskjemaet.</span><span class="sxs-lookup"><span data-stu-id="faa54-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Forkast kandidat](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="faa54-216">Se også</span><span class="sxs-lookup"><span data-stu-id="faa54-216">See also</span></span>

[<span data-ttu-id="faa54-217">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="faa54-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="faa54-218">Organisere arbeidsstyrken</span><span class="sxs-lookup"><span data-stu-id="faa54-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="faa54-219">Definere komponentene for en jobb</span><span class="sxs-lookup"><span data-stu-id="faa54-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Rekruttere jobbkandidater
description: Dette emnet beskriver hvordan du rekrutterer kandidater i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669183"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="4d9e6-103">Rekruttere jobbkandidater</span><span class="sxs-lookup"><span data-stu-id="4d9e6-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="4d9e6-104">Dynamics 365 Human Resources hjelper deg med å administrere rekrutteringsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="4d9e6-105">Den hjelper deg også med overgangen fra jobbkandidater til ansatte på en sømløs måte.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="4d9e6-106">Hvis organisasjonen bruker et separat rekrutteringsprogram, kan rekrutteringsprosessen omfatte følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="4d9e6-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="4d9e6-107">Angi rekrutteringsforespørselen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="4d9e6-108">Motta kandidatreferanser i Human Resources fra rekrutteringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="4d9e6-109">Fullfør kandidatgodkjenningsprosessen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="4d9e6-110">Hvis du ikke bruker et eget rekrutteringsprogram, kan du også administrere kandidater manuelt i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="4d9e6-111">Hvis du er administrator eller utvikler og vil integrere Human Resources med et tredjeparts rekrutteringsprogram, kan du se [Konfigurer Common Data Service-integrering](hr-admin-integration-common-data-service.md) og [Konfigurer virtuelle Common Data Service-enheter](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="4d9e6-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="4d9e6-112">Du kan også finne rekrutteringsintegreringsprogrammer på [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="4d9e6-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="4d9e6-113">Hvis du vil teste forhåndsversjonen for integrering med LinkedIn Talent Hub, kan du se [Integrer med LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="4d9e6-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="4d9e6-114">Aktiver rekrutteringsforespørsler</span><span class="sxs-lookup"><span data-stu-id="4d9e6-114">Enable recruiting requests</span></span>

<span data-ttu-id="4d9e6-115">Hvis du vil sende rekrutteringsforespørsler i Human Resources, må du først aktivere funksjonaliteten i **Parametere for Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="4d9e6-116">I arbeidsområdet **Personaladministrasjon** velger du **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="4d9e6-117">Under **Oppsett** velger du **Personalparametere**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="4d9e6-118">I fanen **Generelt**, under **REKRUTTERING** setter **Aktiver rekrutteringsforespørsler** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Aktiver rekrutteringsforespørsler](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="4d9e6-120">Legg til en rekrutteringsforespørselssted</span><span class="sxs-lookup"><span data-stu-id="4d9e6-120">Add a recruiting request location</span></span>

<span data-ttu-id="4d9e6-121">Hvis organisasjonen har flere steder, kan du legge dem til slik at anmodere kan velge et sted der den nye rekrutten skal fungere.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="4d9e6-122">Stedet vil bli inkludert i prosjektbokføringen.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="4d9e6-123">Angi **rekrutteringsforespørselssted** i søkefeltet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="4d9e6-124">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-124">Select **New**.</span></span>

3. <span data-ttu-id="4d9e6-125">I feltet **Rekrutteringsforespørselssted** angir du stedsnavnet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Legg til en rekrutteringsforespørselssted](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="4d9e6-127">I **beskrivelsen** skriver du inn en beskrivelse for stedet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="4d9e6-128">Under **Sted** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="4d9e6-129">Hvis den meldingen **Ny adresse** vises, angir du adressen til stedet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Angi adresse](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="4d9e6-131">Angi informasjonen for stedets kontakt under **Kontaktinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="4d9e6-132">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="4d9e6-133">Legg til en rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="4d9e6-133">Add a recruiting request</span></span>

<span data-ttu-id="4d9e6-134">Ledere kan sende inn rekrutteringsforespørsler i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="4d9e6-135">Hvis du bruker et separat rekrutteringsprogram, vil denne fremgangsmåten sende en rekrutteringsforespørsel og starte rekrutteringsprosessen i dette programmet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="4d9e6-136">Hvis ikke kan du fullføre denne fremgangsmåten for å starte arbeidsflyten for din egen interne rekrutteringsprosess.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="4d9e6-137">Velg **Selvbetjening for ansatte**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="4d9e6-138">Velg fanen **Mitt team**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="4d9e6-139">Velg **Forespørsel om å rekruttere**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-139">Select  **Request to recruit**.</span></span>

   ![Start en rekrutteringsforespørsel](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="4d9e6-141">Fyll ut feltene **Beskrivelse**, **Jobb** og **Beregnet startdato**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Fullfør rekrutteringsforespørselen](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="4d9e6-143">Velg **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-143">Select **Continue**.</span></span> <span data-ttu-id="4d9e6-144">Rekrutteringsforespørselen for stillingen din vises.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="4d9e6-145">Under **Generelt** velger du en rekrutterer fra rullegardinlisten **Rekrutterer**, og deretter velger du et sted fra rullegardinlisten **Rekrutteringsforespørselssted**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="4d9e6-146">Endre eventuell informasjon etter behov under **Jobb**, og velg deretter **Opprett detaljer fra jobb**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Opprett detaljer fra jobb](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="4d9e6-148">Resten av rekrutteringsforespørselen vil bli fylt ut med standardinformasjonen for jobben du angav.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="4d9e6-149">Under **Ekstern beskrivelse** angir du en ekstern jobbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="4d9e6-150">Under **Stillinger** velger du **Legg til**, og deretter velger du en stilling for denne rekrutteringsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Legg til en stilling](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="4d9e6-152">Under **Ferdigheter** velger du **Legg til** og velger deretter en ferdighet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="4d9e6-153">Under **Krav til utdannelse** velger du **Legg til**, og deretter velger du verdier fra rullegardinlistene **Utdanning** og **Utdanningsnivå**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Legg til krav til utdanning](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="4d9e6-155">Legg til kommentarer etter behov under **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="4d9e6-156">Under **Kompensasjon** velger du et nivå fra rullegardinlisten **Nivå**, og justerer deretter **Lav terskel**, **Kontrollpunkt** og **Høy terskel** etter behov.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="4d9e6-157">Når rekrutteringsforespørselen er fullført og du er klar til å starte rekrutteringsprosessen, velger du **Aktiver** på menylinjen.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Aktiver rekrutteringsforespørsel](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="4d9e6-159">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="4d9e6-160">Vis og rediger rekrutteringsforespørsler</span><span class="sxs-lookup"><span data-stu-id="4d9e6-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="4d9e6-161">Hvis du er en leder og ønsker å vise dine egne forespørsler:</span><span class="sxs-lookup"><span data-stu-id="4d9e6-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="4d9e6-162">Velg **Selvbetjening for ansatte**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="4d9e6-163">Velg fanen **Mitt team**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="4d9e6-164">Under **Informasjon om mitt team** velger du kategorien **Rekrutteringsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Velg fanen Rekrutteringsforespørsler](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="4d9e6-166">Hvis du vil vise eller redigere en rekrutteringsforespørsel, velger du den i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="4d9e6-167">Hvis du er en HR Pro og ønsker å vise alle rekrutteringsforespørslene:</span><span class="sxs-lookup"><span data-stu-id="4d9e6-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="4d9e6-168">Velg **Personaladministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="4d9e6-169">Velg fanen **Rekrutteringsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-169">Select **Recruiting requests**.</span></span>

   ![Vise rekrutteringsforespørsler i Personaladministrasjon](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="4d9e6-171">Hvis du vil vise eller redigere en rekrutteringsforespørsel, velger du den i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="4d9e6-172">Legg til eller rediger en kandidatprofil</span><span class="sxs-lookup"><span data-stu-id="4d9e6-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="4d9e6-173">Hvis organisasjonen har integrert med et annet program for å administrere rekrutteringsforespørsler, blir rekrutteringsforespørsler videresendt til dette programmet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="4d9e6-174">Rekrutteringsprogrammet sender deretter kandidatinformasjon tilbake til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="4d9e6-175">Hvis ikke kan du følge dine egne interne rekrutteringsprosesser og legge inn kandidatinformasjon manuelt.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="4d9e6-176">Velg **Personaladministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="4d9e6-177">Velg **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-177">Select **Links**.</span></span>

3. <span data-ttu-id="4d9e6-178">Under **Rekruttering** velger du **Kandidater**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Vis kandidater](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="4d9e6-180">Velg **Ny** for å legge til en kandidat.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="4d9e6-181">Hvis du vil redigere en eksisterende kandidat fra listen, merker du adressen og velger **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="4d9e6-182">Kandidatprofilen vises.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="4d9e6-183">Under **Kandidatsammendrag** legger du inn eller redigerer kandidatinformasjonen etter behov.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="4d9e6-184">Under **Rekrutteringsforespørsel** velger du en rekrutteringsforespørsel du vil koble kandidaten til.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="4d9e6-185">Deretter fyller du ut feltene **Beregnet startdato**, **Ansettelsessjef**, **Stilling** og **Beskrivelse** etter behov.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Koble til rekrutteringsforespørsel](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="4d9e6-187">Fyll ut all informasjonen i følgende områder som du vil ta med i kandidatens post:</span><span class="sxs-lookup"><span data-stu-id="4d9e6-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="4d9e6-188">**Kommentarer**</span><span class="sxs-lookup"><span data-stu-id="4d9e6-188">**Comments**</span></span>
   - <span data-ttu-id="4d9e6-189">**Yrkeserfaring**</span><span class="sxs-lookup"><span data-stu-id="4d9e6-189">**Professional experience**</span></span>
   - <span data-ttu-id="4d9e6-190">**Kontaktinformasjon**</span><span class="sxs-lookup"><span data-stu-id="4d9e6-190">**Contact information**</span></span>
   - <span data-ttu-id="4d9e6-191">**Utdanning**</span><span class="sxs-lookup"><span data-stu-id="4d9e6-191">**Education**</span></span>
   - <span data-ttu-id="4d9e6-192">**Kompetanse**</span><span class="sxs-lookup"><span data-stu-id="4d9e6-192">**Skills**</span></span>
   - <span data-ttu-id="4d9e6-193">**Attester**</span><span class="sxs-lookup"><span data-stu-id="4d9e6-193">**Certificates**</span></span>
   - <span data-ttu-id="4d9e6-194">**Screeninger**</span><span class="sxs-lookup"><span data-stu-id="4d9e6-194">**Screenings**</span></span>

8. <span data-ttu-id="4d9e6-195">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="4d9e6-196">Ansett en kandidat</span><span class="sxs-lookup"><span data-stu-id="4d9e6-196">Hire a candidate</span></span>

<span data-ttu-id="4d9e6-197">Når du er klar til å ansette en kandidat, følger du denne fremgangsmåten for overgang fra kandidat til ansatt.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="4d9e6-198">Velg **Ansett** i kandidatskjemaet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-198">On the candidate form, select **Hire**.</span></span>

   ![Ansett en kandidat](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="4d9e6-200">Fyll ut alle feltene under **Detaljer** i skjemaet **Ansett ny arbeider**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Angi detaljer for ny ansettelse](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="4d9e6-202">Under **Stillingsdetaljer** kan du bekrefte og endre informasjon etter behov.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="4d9e6-203">Under **Sjekklister for jobbintroduksjon** velger du de relevante sjekklistene for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="4d9e6-204">Velg **Fortsett** for å opprette ansattposten.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="4d9e6-205">Kandidatposten kan gå gjennom flere godkjenningstrinn før den blir til en ansattpost, avhengig av arbeidsflytene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="4d9e6-206">Bestemme deg for ikke å ansette en kandidat</span><span class="sxs-lookup"><span data-stu-id="4d9e6-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="4d9e6-207">Hvis du bestemmer deg for ikke å ansette en kandidat, kan du følge denne fremgangsmåten for å fjerne dem fra gjennomgangsprosessen.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="4d9e6-208">Velg **Ikke ansett** i kandidatskjemaet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-208">On the candidate form, select **Do not hire**.</span></span>

   ![Ikke ansett kandidat](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="4d9e6-210">Velg en **årsakskode**, og ta med eventuelle kommentarer.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="4d9e6-211">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="4d9e6-212">Forkast en kandidat</span><span class="sxs-lookup"><span data-stu-id="4d9e6-212">Dismiss a candidate</span></span>

<span data-ttu-id="4d9e6-213">Om nødvendig kan du forkaste en kandidat etter å ha ansatt vedkommende.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="4d9e6-214">En kandidat kan for eksempel avvise tilbudet eller ikke dukke opp den første dagen.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="4d9e6-215">Velg **Forkast kandidat** i kandidatskjemaet.</span><span class="sxs-lookup"><span data-stu-id="4d9e6-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Forkast kandidat](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="4d9e6-217">Se også</span><span class="sxs-lookup"><span data-stu-id="4d9e6-217">See also</span></span>

[<span data-ttu-id="4d9e6-218">Konfigurere virtuelle enheter for Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4d9e6-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="4d9e6-219">Organisere arbeidsstyrken</span><span class="sxs-lookup"><span data-stu-id="4d9e6-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="4d9e6-220">Definere komponentene for en jobb</span><span class="sxs-lookup"><span data-stu-id="4d9e6-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)
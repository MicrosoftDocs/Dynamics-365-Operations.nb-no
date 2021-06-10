---
title: Distribuere og planlegge spørreskjemaer
description: Denne artikkelen forklarer hvordan du distribuerer spørreskjemaene du utformer, slik at de er tilgjengelige for personen eller personene som skal fylle dem ut.
author: andreabichsel
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67ea9b61b9e4ed47f6bb1dd051e532ed4dcbce48
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058712"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="7a965-103">Distribuere og planlegge spørreskjemaer</span><span class="sxs-lookup"><span data-stu-id="7a965-103">Distribute and schedule questionnaires</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7a965-104">Denne artikkelen forklarer hvordan du distribuerer spørreskjemaene du utformer, slik at de er tilgjengelige for personen eller personene som skal fylle dem ut.</span><span class="sxs-lookup"><span data-stu-id="7a965-104">This article explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="7a965-105">Et spørreskjema kan distribueres på flere ulike måter:</span><span class="sxs-lookup"><span data-stu-id="7a965-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="7a965-106">Merk spørreskjemaet som aktivt.</span><span class="sxs-lookup"><span data-stu-id="7a965-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="7a965-107">Spørreskjemaet blir dermed tilgjengelig for alle ansatte, med mindre en spørreskjemagruppe er konfigurert slik at tilgangen til den er begrenset.</span><span class="sxs-lookup"><span data-stu-id="7a965-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="7a965-108">Tilordne rettigheter til en spørreskjemagruppe.</span><span class="sxs-lookup"><span data-stu-id="7a965-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="7a965-109">Spørreskjemaet blir dermed tilgjengelig for alle medlemmer av den valgte gruppen.</span><span class="sxs-lookup"><span data-stu-id="7a965-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="7a965-110">Opprett planlagte svarøkter.</span><span class="sxs-lookup"><span data-stu-id="7a965-110">Create planned answer sessions.</span></span> <span data-ttu-id="7a965-111">Spørreskjemaet blir dermed tilgjengelig bare for en bestemt person.</span><span class="sxs-lookup"><span data-stu-id="7a965-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="7a965-112">Opprett en tidsplan.</span><span class="sxs-lookup"><span data-stu-id="7a965-112">Create a schedule.</span></span> <span data-ttu-id="7a965-113">Spørreskjemaet kan dermed bli tilgjengelig for flere personer.</span><span class="sxs-lookup"><span data-stu-id="7a965-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="7a965-114">Merke et spørreskjemaet som aktivt</span><span class="sxs-lookup"><span data-stu-id="7a965-114">Marking a questionnaire as active</span></span>

<span data-ttu-id="7a965-115">Når du setter **Aktiv**-feltet til **Ja** på **Spørreskjemaer**-siden, gjør du spørreskjemaet tilgjengelig slik at alle ansatte kan fylle det ut.</span><span class="sxs-lookup"><span data-stu-id="7a965-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="7a965-116">Respondenter kan fylle ut spørreskjemaet flere ganger.</span><span class="sxs-lookup"><span data-stu-id="7a965-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="7a965-117">Denne funksjonen er nyttig hvis du vil samle inn kontinuerlig tilbakemelding i løpet av året.</span><span class="sxs-lookup"><span data-stu-id="7a965-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="7a965-118">Du kan for eksempel lage et spørreskjema som ansatte bruker til å gi tilbakemelding om lunsjtjenesten i kaféen.</span><span class="sxs-lookup"><span data-stu-id="7a965-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="7a965-119">Spørreskjemagrupper</span><span class="sxs-lookup"><span data-stu-id="7a965-119">Questionnaire groups</span></span>

<span data-ttu-id="7a965-120">Du kan definere spørreskjemagrupper og deretter inkludere respondenter som et spørreskjema skal distribueres til.</span><span class="sxs-lookup"><span data-stu-id="7a965-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="7a965-121">Du kan opprette spørreskjemagrupper fra følgende sider:</span><span class="sxs-lookup"><span data-stu-id="7a965-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="7a965-122">**Spørreskjemagrupper**– Bare personer i en spørreskjemagruppe kan fylle ut et valgt spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="7a965-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="7a965-123">La oss si at den planlagte målgruppen for eksempel er leverandører, så du oppretter en spørreskjemagruppe som er spesifikk for disse respondentene.</span><span class="sxs-lookup"><span data-stu-id="7a965-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="7a965-124">**Medlemmer av spørreskjemagruppe** – Du kan legge til personer i spørreskjemagruppene.</span><span class="sxs-lookup"><span data-stu-id="7a965-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="7a965-125">Hvis du vil tilordne en spørreskjemagruppe til et spørreskjema, klikker du **Brukerrettigheter** på **Spørreskjemaer**-siden.</span><span class="sxs-lookup"><span data-stu-id="7a965-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="7a965-126">Når spørreskjemaet er lagret som aktivt, kan medlemmene av spørreskjemagruppen fylle det ut.</span><span class="sxs-lookup"><span data-stu-id="7a965-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="7a965-127">Denne funksjonaliteten er nyttig hvis du vil teste et spørreskjema på en utvalgt gruppe personer før du distribuerer den til en større gruppe, eller hvis du vil utforme et spørreskjema for en bestemt målgruppe.</span><span class="sxs-lookup"><span data-stu-id="7a965-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="7a965-128">Planlagte svarøkter i et spørreskjema</span><span class="sxs-lookup"><span data-stu-id="7a965-128">Planned answer sessions in a questionnaire</span></span>

<span data-ttu-id="7a965-129">Planlagte svarøkter er spørreskjemaer du har utformet og valgt respondentene for.</span><span class="sxs-lookup"><span data-stu-id="7a965-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a965-130">Før du kan definere planlagte svarøkter, må du utforme et spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="7a965-130">Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="7a965-131">Du kan opprette en planlagt svarøkt for én ansatt på siden **Planlagt svarøkt**.</span><span class="sxs-lookup"><span data-stu-id="7a965-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="7a965-132">Listen på siden viser alle planlagte spørreskjemaer.</span><span class="sxs-lookup"><span data-stu-id="7a965-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="7a965-133">Planlagte svarøkter brukes også på siden **Spørreskjemaplaner**, der du kan planlegge spørreskjemaer for flere personer:</span><span class="sxs-lookup"><span data-stu-id="7a965-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="7a965-134">Ansatte</span><span class="sxs-lookup"><span data-stu-id="7a965-134">Employees</span></span>
-   <span data-ttu-id="7a965-135">Kursdeltakere</span><span class="sxs-lookup"><span data-stu-id="7a965-135">Course participants</span></span>
-   <span data-ttu-id="7a965-136">Organisasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="7a965-136">Organizational units</span></span>

<span data-ttu-id="7a965-137">Hver person kan svare på spørreskjemaet bare én gang.</span><span class="sxs-lookup"><span data-stu-id="7a965-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="7a965-138">Planlegge et spørreskjema</span><span class="sxs-lookup"><span data-stu-id="7a965-138">Scheduling a questionnaire</span></span>

<span data-ttu-id="7a965-139">Du kan velge om du vil planlegge et spørreskjema for flere respondenter.</span><span class="sxs-lookup"><span data-stu-id="7a965-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="7a965-140">Planleggingstyper</span><span class="sxs-lookup"><span data-stu-id="7a965-140">Planning types</span></span>

<span data-ttu-id="7a965-141">Planleggingstyper er nødvendige hvis du vil planlegge planlagte svarøkter for flere respondenter.</span><span class="sxs-lookup"><span data-stu-id="7a965-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="7a965-142">Planleggingstyper brukes til å klassifisere spørreskjemaplaner.</span><span class="sxs-lookup"><span data-stu-id="7a965-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="7a965-143">Du kan for eksempel planlegge spørreskjemaer for følgende formål:</span><span class="sxs-lookup"><span data-stu-id="7a965-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="7a965-144">Evaluering</span><span class="sxs-lookup"><span data-stu-id="7a965-144">Evaluation</span></span>
-   <span data-ttu-id="7a965-145">Undersøkelse</span><span class="sxs-lookup"><span data-stu-id="7a965-145">Survey</span></span>
-   <span data-ttu-id="7a965-146">Testing</span><span class="sxs-lookup"><span data-stu-id="7a965-146">Testing</span></span>

<span data-ttu-id="7a965-147">Du kan angi planleggingstyper for en spørreskjemaplan på siden **Spørreskjemaplaner**.</span><span class="sxs-lookup"><span data-stu-id="7a965-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="7a965-148">Referansetyper for spørreskjema</span><span class="sxs-lookup"><span data-stu-id="7a965-148">Reference types for questionnaire</span></span>

<span data-ttu-id="7a965-149">Du kan bruke referansetyper til å angi kriterier for respondentene du kanskje velger når du planlegger et spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="7a965-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="7a965-150">Bruk **Referansetyper**-siden til å definere referansetyper for et spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="7a965-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="7a965-151">Hver referansetype svarer til en tabell i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7a965-151">Each reference type corresponds to a table in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="7a965-152">Når du oppretter spørreskjemaplaner, kan du angi enkeltposter i tabellen eller et utvalg av poster som spørreskjemaet skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="7a965-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="7a965-153">Hvis du for eksempel velger Kurs-tabellen, kan du bestemme det bestemte kurset spørreskjemaet skal være for.</span><span class="sxs-lookup"><span data-stu-id="7a965-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="7a965-154">Når du definerer en referanse til Kurs-tabellen, blir enkelte felt og knapper på **Kurs**-siden tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="7a965-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="7a965-155">Spørreskjemaplaner</span><span class="sxs-lookup"><span data-stu-id="7a965-155">Questionnaire schedules</span></span>

<span data-ttu-id="7a965-156">Du kan bruke spørreskjemaplaner til å generere flere planlagte svarøkter for en gruppe brukere, basert på en referansetype.</span><span class="sxs-lookup"><span data-stu-id="7a965-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="7a965-157">Opprett en plan på **Spørreskjemaplaner**-siden.</span><span class="sxs-lookup"><span data-stu-id="7a965-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="7a965-158">Velg planleggingstypen for å kategorisere tidsplanen, og velg også referansetypen som skal brukes til å spørre systemet om bestemte brukere.</span><span class="sxs-lookup"><span data-stu-id="7a965-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="7a965-159">Hvis du for eksempel setter referansetypen til Kurs-tabellen, kan du velge et bestemt kurs i **Referanse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a965-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="7a965-160">Klikk **Oppsettsdetaljer** for å velge spørreskjemaet og andre kriterier.</span><span class="sxs-lookup"><span data-stu-id="7a965-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="7a965-161">Du kan for eksempel angi instruktørens navn som et kriterium hvis spørreskjemaet er en evaluering av instruktøren.</span><span class="sxs-lookup"><span data-stu-id="7a965-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="7a965-162">Når du er ferdig med å skrive inn oppsettsdetaljer, genererer systemet planlagte svarøkter for brukerne som er inkludert i spørringen.</span><span class="sxs-lookup"><span data-stu-id="7a965-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="7a965-163">Klikk **Planlagte svarøkter** for å vise svarøkter for tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="7a965-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="7a965-164">Du kan deretter manuelt opprette flere planlagte svarøkter eller slette planlagte svarøkter som ikke er besvart.</span><span class="sxs-lookup"><span data-stu-id="7a965-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="7a965-165">Klikk **Funksjoner** &gt; **Start** for å gjøre spørreskjemaet tilgjengelig for brukerne i relaterte planlagte svarøkter.</span><span class="sxs-lookup"><span data-stu-id="7a965-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="7a965-166">Klikk **Svar** for å vise de fullførte svarene på spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="7a965-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="7a965-167">Du kan eventuelt kopiere innstillingene for spørreskjemaplan, planlagte svarøkter og svar på en ny spørreskjemaplan.</span><span class="sxs-lookup"><span data-stu-id="7a965-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="7a965-168">Varsle respondenter om spørreskjemaer som er tilgjengelige for dem</span><span class="sxs-lookup"><span data-stu-id="7a965-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="7a965-169">Når du distribuerer et spørreskjema, må du varsle respondentene om at spørreskjemaet er tilgjengelige for dem.</span><span class="sxs-lookup"><span data-stu-id="7a965-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="7a965-170">Varsle respondenter om en planlagt svarøkt</span><span class="sxs-lookup"><span data-stu-id="7a965-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="7a965-171">Hvis du bruker en planlagt svarøkt, må du varsle personen direkte, for eksempel via telefon eller e-post.</span><span class="sxs-lookup"><span data-stu-id="7a965-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="7a965-172">Varsle respondenter om en planlegging</span><span class="sxs-lookup"><span data-stu-id="7a965-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="7a965-173">Bruk siden **Spørreskjemaplaner** til å klargjøre og sende e-post til alle respondenter som er tilordnet spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="7a965-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="7a965-174">Skriv inn e-postteksten i kategorien **E-post for ansattselvbetjening**. Etter at tidsplanen er startet, klikk **Funksjoner** &gt; **Send e-post** for å generere og sende e-posten til respondentene.</span><span class="sxs-lookup"><span data-stu-id="7a965-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="7a965-175">Respondentene kan deretter logge seg på webområdet og fylle ut spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="7a965-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a965-176">Før du kan bruke e-postfunksjonaliteten, må IT-administratoren angi e-postinnstillingene på siden **E-postparametere**.</span><span class="sxs-lookup"><span data-stu-id="7a965-176">Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="7a965-177">Avslutte et planlagt spørreskjema</span><span class="sxs-lookup"><span data-stu-id="7a965-177">Ending a scheduled questionnaire</span></span>

<span data-ttu-id="7a965-178">Du kan avslutte et planlagt spørreskjema når alle respondentene har fullført sin svarøkt.</span><span class="sxs-lookup"><span data-stu-id="7a965-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="7a965-179">Når et planlagt spørreskjema er avsluttet, kan du ikke kopiere innstillingene til en ny plan.</span><span class="sxs-lookup"><span data-stu-id="7a965-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> [!NOTE]
>   <span data-ttu-id="7a965-180">Hvis én eller flere respondenter ikke har fylt ut spørreskjemaet, men du likevel vil avslutte planleggingen, må du først slette disse respondentene fra listen, på siden **Planlagt svarøkt**.</span><span class="sxs-lookup"><span data-stu-id="7a965-180">If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="7a965-181">Du kan deretter avslutte tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="7a965-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="7a965-182">Fylle ut spørreskjemaer</span><span class="sxs-lookup"><span data-stu-id="7a965-182">Completing questionnaires</span></span>

<span data-ttu-id="7a965-183">Når du har utformet og distribuert et spørreskjema, kan spørreskjemaet fylles ut av valgte respondenter.</span><span class="sxs-lookup"><span data-stu-id="7a965-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="7a965-184">Du kan fylle ut spørreskjemaene som er tilgjengelige for deg fra to steder:</span><span class="sxs-lookup"><span data-stu-id="7a965-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="7a965-185">I navigasjonsruten klikker du **Spørreskjemaer** &gt; **Distribuer** &gt; **Fullfør et spørreskjema**.</span><span class="sxs-lookup"><span data-stu-id="7a965-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="7a965-186">I Ansattselvbetjening klikker du **Spørreskjemaer som skal fullføres**.</span><span class="sxs-lookup"><span data-stu-id="7a965-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="7a965-187">Spørreskjemaer kan gjøres tilgjengelige for bestemte brukere eller brukergrupper eller alle brukere i et nettverk.</span><span class="sxs-lookup"><span data-stu-id="7a965-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Utvide Talent ved hjelp av PowerApps og Microsoft Flow – eksempelscenarier
description: Dette emnet beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 for Talent som bruker Microsoft PowerApps og Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518724"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="969ce-103">Utvide Talent ved hjelp av PowerApps og Microsoft Flow – eksempelscenarier</span><span class="sxs-lookup"><span data-stu-id="969ce-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="969ce-104">Dette emnet beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 for Talent som bruker Microsoft PowerApps og Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="969ce-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="969ce-105">Du kan importere løsningspakken som er tilknyttet hvert eksempel, i ditt miljø for PowerApps.</span><span class="sxs-lookup"><span data-stu-id="969ce-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="969ce-106">Du kan deretter bruke pakkene som retningslinjer eller som utgangspunkt til å implementere scenarioene som gjelder for organisasjonen din.</span><span class="sxs-lookup"><span data-stu-id="969ce-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="969ce-107">Hvis du vil bruke malene og appen som er beskrevet i dette emnet, "som de er", må du teste dem å være sikker på at de dekker alle scenarioene som er spesifikke for implementeringen.</span><span class="sxs-lookup"><span data-stu-id="969ce-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="969ce-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="969ce-108">Prerequisites</span></span>

- <span data-ttu-id="969ce-109">Hvis du vil importere pakker, må brukerne ha **Miljøskaper**-tillatelsen.</span><span class="sxs-lookup"><span data-stu-id="969ce-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="969ce-110">Hvis du vil eksportere eller importere apper, må brukerne ha en PowerApps Plan 2-lisens eller en PowerApps Plan 2-prøvelisens.</span><span class="sxs-lookup"><span data-stu-id="969ce-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="969ce-111">Flyt – skjematilkobling</span><span class="sxs-lookup"><span data-stu-id="969ce-111">Flow – Form Connect</span></span>

<span data-ttu-id="969ce-112">Malen for **Flyt – skjematilkobling** kan brukes til å lese data fra Microsoft Forms og lagre den i en Common Data Service-enhet.</span><span class="sxs-lookup"><span data-stu-id="969ce-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="969ce-113">Denne malen kan utvides slik at den kan brukes til andre scenarioer.</span><span class="sxs-lookup"><span data-stu-id="969ce-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="969ce-114">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="969ce-114">Here are some examples:</span></span>

- <span data-ttu-id="969ce-115">Registrer kandidatvurderinger.</span><span class="sxs-lookup"><span data-stu-id="969ce-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="969ce-116">Lagre resultater fra kursspørreskjema.</span><span class="sxs-lookup"><span data-stu-id="969ce-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="969ce-117">Kompiler et bibliotek med intervjuspørsmål for HR-administratorer.</span><span class="sxs-lookup"><span data-stu-id="969ce-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="969ce-118">Registrere en kandidats evaluering av intervjuprosessen</span><span class="sxs-lookup"><span data-stu-id="969ce-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="969ce-119">I Microsoft Dynamics 365: Attract kan skjemaer vises i kandidatportalen, og kandidater kan fylle ut detaljer.</span><span class="sxs-lookup"><span data-stu-id="969ce-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="969ce-120">Skjemaer kan også innebygges som aktiviteter i en jobbmal.</span><span class="sxs-lookup"><span data-stu-id="969ce-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="969ce-121">Når en kandidat sender et skjema, fanger Microsoft Flow opp skjemainnsendingen, leser dataene og lagrer den i Common Data Service-enheten.</span><span class="sxs-lookup"><span data-stu-id="969ce-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="969ce-122">For å laste ned malen for **Flyt – skjematilkobling** og den egendefinerte enhetsstrukturen, kan du gå til [Flyt – skjematilkobling](https://go.microsoft.com/fwlink/?linkid=2081988) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="969ce-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="969ce-123">Starte og hente parametere som er sendt til Powerapps</span><span class="sxs-lookup"><span data-stu-id="969ce-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="969ce-124">Malen for **Starte og hente parametere som er sendt til Powerapps** kan brukes som utgangspunkt for et hvilket som helst PowerApps-scenario som er spesifikt for Attract.</span><span class="sxs-lookup"><span data-stu-id="969ce-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="969ce-125">Den inneholder alle standardparameterne som sendes av Attract, for eksempel **Stillingssøknad**, **Kandidat-ID** og **Jobb-ID**.</span><span class="sxs-lookup"><span data-stu-id="969ce-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="969ce-126">Denne malen kan brukes til å hente et kandidatvurderingsskjema, slik at en ansettelsesansvarlig kan vise vurderingen som en kandidat fylte ut.</span><span class="sxs-lookup"><span data-stu-id="969ce-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="969ce-127">Apper som er opprettet ved hjelp av PowerApps, kan bygges inn jobbmalen i Attract.</span><span class="sxs-lookup"><span data-stu-id="969ce-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="969ce-128">For å laste ned malen for **Starte og hente parametere som er sendt til Powerapps** og den egendefinerte enhetsstruktur, kan du gå til [Starte og hente parametere som er sendt til Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="969ce-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="969ce-129">Integrering med Office 365</span><span class="sxs-lookup"><span data-stu-id="969ce-129">Integration with Office 365</span></span>

<span data-ttu-id="969ce-130">**Integrering med Office 365**-appen kan brukes til å hente teaminformasjon for påloggede brukere fra Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="969ce-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="969ce-131">Den refererer til arbeidere i Talent for å hente innstemplings- og utstemplingsdetaljer og unntaksregistreringer.</span><span class="sxs-lookup"><span data-stu-id="969ce-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="969ce-132">Innstemplings- og utstemplingsinformasjon lagres i egendefinerte Common Data Service-enheter.</span><span class="sxs-lookup"><span data-stu-id="969ce-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="969ce-133">Det antas at disse opplysningene fylles ut fra tredjepartssystemer via integrasjon.</span><span class="sxs-lookup"><span data-stu-id="969ce-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="969ce-134">Denne appen kan utvides, slik at den kan brukes til andre scenarioer.</span><span class="sxs-lookup"><span data-stu-id="969ce-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="969ce-135">Den kan for eksempel brukes til å vise ferieinformasjon for team, kalenderhendelser og teamspesifikke hendelser.</span><span class="sxs-lookup"><span data-stu-id="969ce-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="969ce-136">For å laste ned **Integrering med Office 365**-appen og egendefinert enhetsstruktur, kan du gå til [Integrering med Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="969ce-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="969ce-137">Flyt – e-postvarsling</span><span class="sxs-lookup"><span data-stu-id="969ce-137">Flow – Email Notification</span></span>

<span data-ttu-id="969ce-138">Malen **Flyt – e-postvarsling** kan brukes i e-postvarslingsscenarioer.</span><span class="sxs-lookup"><span data-stu-id="969ce-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="969ce-139">Den kan brukes til å utløse varsel-e-postmeldinger til kandidater som ansettelsesteamet avviser i løpet av et hvilket som helst trinn i rekrutteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="969ce-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="969ce-140">Denne malen kan utvides til å spore endringer i kandidatstadiet i rekrutteringsprosessen og til å sende meldinger til ansettelsesteamet og kandidaten.</span><span class="sxs-lookup"><span data-stu-id="969ce-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="969ce-141">Generelt for enhetene som er lagret i Common Data Service, kan flyter defineres til å sende varslinger for hendelser som forekommer i Core HR, Attract eller Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="969ce-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="969ce-142">For å laste ned **Flyt – e-postvarsling**-malen, gå til [Flyt – e-postvarsling](https://go.microsoft.com/fwlink/?linkid=2082103) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="969ce-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="969ce-143">Flyt – SQL-tilkobling og kjøring</span><span class="sxs-lookup"><span data-stu-id="969ce-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="969ce-144">**Flyt – SQL-tilkobling og kjøring**-malen kobler til Microsoft SQL Server og aktiverer SQL-spørringer som skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="969ce-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="969ce-145">Selv om denne malen er utformet for å lese og oppdatere SQL-tabeller, kan den utvides, slik at den kan brukes til andre scenarioer.</span><span class="sxs-lookup"><span data-stu-id="969ce-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="969ce-146">Den kan for eksempel brukes til å fylle ut en oppsamlingstabell i Common Data Service med poster fra SQL Server og synkronisere oppsamlingstabellen jevnlig ved hjelp av en trinnvis push fra SQL Server.</span><span class="sxs-lookup"><span data-stu-id="969ce-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="969ce-147">For å laste ned malen for **Flyt – SQL-tilkobling og kjøring**, kan du gå til [Flyt – SQL-tilkobling og kjøring](https://go.microsoft.com/fwlink/?linkid=2081789) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="969ce-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="969ce-148">Flyt – SharePoint-integrering</span><span class="sxs-lookup"><span data-stu-id="969ce-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="969ce-149">Malen **Flyt – SharePoint-ingetrering** kan brukes til å lese data fra en Microsoft SharePoint-liste, sammenligne listen med feltverdier for alle Common Data Service-enheter og sende resultatene av sammenligningen som en e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="969ce-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="969ce-150">En organisasjon kan ha et sett med ferdigheter som den har raskt behov for.</span><span class="sxs-lookup"><span data-stu-id="969ce-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="969ce-151">Disse ferdighetene kan lagres i SharePoint som en SharePoint-liste.</span><span class="sxs-lookup"><span data-stu-id="969ce-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="969ce-152">Når en kandidat søker på jobber som er oppført med et sett med nødvendige kvalifikasjoner, og hvis det er betydelig samsvar mellom kandidatens ferdigheter og ferdighetene som er lagret i SharePoint, sendes en e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="969ce-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="969ce-153">Dermed blir hastestillinger raskere fylt, fordi varslingene hjelper rekrutteringspersoner med å kontakte og ansette kandidater på tvers av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="969ce-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="969ce-154">Denne malen kan utvides, slik at den kan brukes på alle scenarioer som involverer SharePoint-integrering.</span><span class="sxs-lookup"><span data-stu-id="969ce-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="969ce-155">For å laste ned **Flyt – SharePoint-integrering**-malen, gå til [Flyt – SharePoint-integrering](https://go.microsoft.com/fwlink/?linkid=2082109) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="969ce-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="969ce-156">Administrasjonskonsoll for å administrere talentsamlinger</span><span class="sxs-lookup"><span data-stu-id="969ce-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="969ce-157">Når du aktiverer integrering med LinkedIn, oppretter Attract automatisk en LinkedIn-talentsamling.</span><span class="sxs-lookup"><span data-stu-id="969ce-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="969ce-158">Når en rekrutterer utveksler InMail med en rekrutt via LinkedIn, oppretter Attract en profil for rekrutten, og rekrutten blir medlem av LinkedIn-talentsamlingen.</span><span class="sxs-lookup"><span data-stu-id="969ce-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="969ce-159">Denne PowerApps-appen er nyttig for omorganisering av kandidater i talentsamlinger på basis av kompetanse.</span><span class="sxs-lookup"><span data-stu-id="969ce-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="969ce-160">Kjør denne PowerApps-appen som administrasjonskonsoll for å utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="969ce-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="969ce-161">Angi kandidater i en talentsamling</span><span class="sxs-lookup"><span data-stu-id="969ce-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="969ce-162">Legge til og fjerne kandidater fra en talentsamling</span><span class="sxs-lookup"><span data-stu-id="969ce-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="969ce-163">Flytte kandidater fra én talentsamling til en annen</span><span class="sxs-lookup"><span data-stu-id="969ce-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="969ce-164">Finne ut om kandidater allerede er del av en talentsamling før du flytter dem</span><span class="sxs-lookup"><span data-stu-id="969ce-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="969ce-165">Kontrollere kompetansen til kandidater før du flytter dem til andre talentsamlinger</span><span class="sxs-lookup"><span data-stu-id="969ce-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="969ce-166">Denne PowerApps-appen bruker mange-til-mange-relasjoner, slik at du kan bruke den som en mal for andre scenarier der du må trekke ut poster som har mange-til-mange-relasjoner.</span><span class="sxs-lookup"><span data-stu-id="969ce-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="969ce-167">Hvis du vil laste ned malen **Administrasjonskonsoll for å administrere talentsamlinger**, går du til [Administrasjonskonsoll for å administrere talentsamlinger](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="969ce-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="969ce-168">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="969ce-168">Additional resources</span></span>

[<span data-ttu-id="969ce-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="969ce-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="969ce-170">Overføre app mellom leiere og miljøer</span><span class="sxs-lookup"><span data-stu-id="969ce-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)

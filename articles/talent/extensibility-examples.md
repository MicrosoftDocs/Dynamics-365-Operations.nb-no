---
title: Utvide Talent med Power Apps og Power Automate
description: Dette emnet beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 Talent som bruker Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898323"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="4dd28-103">Utvide Talent med Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="4dd28-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="4dd28-104">Dette emnet beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 Talent som bruker Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="4dd28-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="4dd28-105">Du kan importere løsningspakken som er tilknyttet hvert eksempel, i ditt Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="4dd28-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="4dd28-106">Du kan deretter bruke pakkene som retningslinjer eller som utgangspunkt til å implementere scenarioene som gjelder for organisasjonen din.</span><span class="sxs-lookup"><span data-stu-id="4dd28-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4dd28-107">Hvis du vil bruke malene og appen som er beskrevet i dette emnet, "som de er", må du teste dem å være sikker på at de dekker alle scenarioene som er spesifikke for implementeringen.</span><span class="sxs-lookup"><span data-stu-id="4dd28-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="4dd28-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="4dd28-108">Prerequisites</span></span>

- <span data-ttu-id="4dd28-109">Hvis du vil importere pakker, må brukerne ha **Miljøskaper**-tillatelsen.</span><span class="sxs-lookup"><span data-stu-id="4dd28-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="4dd28-110">Hvis du vil eksportere eller importere apper, må brukerne ha en Power Apps Plan 2-lisens eller en Power Apps Plan 2-prøvelisens.</span><span class="sxs-lookup"><span data-stu-id="4dd28-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="4dd28-111">Power Automate – skjematilkobling</span><span class="sxs-lookup"><span data-stu-id="4dd28-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="4dd28-112">Malen for **Power Automate – skjematilkobling** kan brukes til å lese data fra Microsoft Forms og lagre den i en Common Data Service-enhet.</span><span class="sxs-lookup"><span data-stu-id="4dd28-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="4dd28-113">Denne malen kan utvides slik at den kan brukes til andre scenarioer.</span><span class="sxs-lookup"><span data-stu-id="4dd28-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="4dd28-114">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="4dd28-114">Here are some examples:</span></span>

- <span data-ttu-id="4dd28-115">Registrer kandidatvurderinger.</span><span class="sxs-lookup"><span data-stu-id="4dd28-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="4dd28-116">Lagre resultater fra kursspørreskjema.</span><span class="sxs-lookup"><span data-stu-id="4dd28-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="4dd28-117">Kompiler et bibliotek med intervjuspørsmål for HR-administratorer.</span><span class="sxs-lookup"><span data-stu-id="4dd28-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="4dd28-118">Registrere en kandidats evaluering av intervjuprosessen</span><span class="sxs-lookup"><span data-stu-id="4dd28-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="4dd28-119">I Microsoft Dynamics 365: Attract kan skjemaer vises i kandidatportalen, og kandidater kan fylle ut detaljer.</span><span class="sxs-lookup"><span data-stu-id="4dd28-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="4dd28-120">Skjemaer kan også innebygges som aktiviteter i en jobbmal.</span><span class="sxs-lookup"><span data-stu-id="4dd28-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="4dd28-121">Når en kandidat sender et skjema, fanger Microsoft Power Automate opp skjemainnsendingen, leser dataene og lagrer den i Common Data Service-enheten.</span><span class="sxs-lookup"><span data-stu-id="4dd28-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="4dd28-122">For å laste ned malen for **Power Automate – skjematilkobling** og den egendefinerte enhetsstrukturen, kan du gå til [Power Automate – skjematilkobling](https://go.microsoft.com/fwlink/?linkid=2081988) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="4dd28-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="4dd28-123">Starte og hente parametere som er sendt til Power Apps</span><span class="sxs-lookup"><span data-stu-id="4dd28-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="4dd28-124">Malen **Starte og hente parametere som er sendt til Power Apps** kan brukes som utgangspunkt for et hvilket som helst Power Apps-scenario som er spesifikt for Attract.</span><span class="sxs-lookup"><span data-stu-id="4dd28-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="4dd28-125">Den inneholder alle standardparameterne som sendes av Attract, for eksempel **Stillingssøknad**, **Kandidat-ID** og **Jobb-ID**.</span><span class="sxs-lookup"><span data-stu-id="4dd28-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="4dd28-126">Denne malen kan brukes til å hente et kandidatvurderingsskjema, slik at en ansettelsesansvarlig kan vise vurderingen som en kandidat fylte ut.</span><span class="sxs-lookup"><span data-stu-id="4dd28-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="4dd28-127">Apper som er opprettet ved hjelp av Power Apps, kan bygges inn jobbmalen i Attract.</span><span class="sxs-lookup"><span data-stu-id="4dd28-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="4dd28-128">For å laste ned malen for **Starte og hente parametere som er sendt til Power Apps** og den egendefinerte enhetsstruktur, kan du gå til [Starte og hente parametere som er sendt til Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="4dd28-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="4dd28-129">Integrering med Office 365</span><span class="sxs-lookup"><span data-stu-id="4dd28-129">Integration with Office 365</span></span>

<span data-ttu-id="4dd28-130">**Integrering med Office 365**-appen kan brukes til å hente teaminformasjon for påloggede brukere fra Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="4dd28-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="4dd28-131">Den refererer til arbeidere i Talent for å hente innstemplings- og utstemplingsdetaljer og unntaksregistreringer.</span><span class="sxs-lookup"><span data-stu-id="4dd28-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="4dd28-132">Innstemplings- og utstemplingsinformasjon lagres i egendefinerte Common Data Service-enheter.</span><span class="sxs-lookup"><span data-stu-id="4dd28-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="4dd28-133">Det antas at disse opplysningene fylles ut fra tredjepartssystemer via integrasjon.</span><span class="sxs-lookup"><span data-stu-id="4dd28-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="4dd28-134">Denne appen kan utvides, slik at den kan brukes til andre scenarioer.</span><span class="sxs-lookup"><span data-stu-id="4dd28-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="4dd28-135">Den kan for eksempel brukes til å vise ferieinformasjon for team, kalenderhendelser og teamspesifikke hendelser.</span><span class="sxs-lookup"><span data-stu-id="4dd28-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="4dd28-136">For å laste ned **Integrering med Office 365**-appen og egendefinert enhetsstruktur, kan du gå til [Integrering med Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="4dd28-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="4dd28-137">Power Automate – e-postvarsling</span><span class="sxs-lookup"><span data-stu-id="4dd28-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="4dd28-138">Malen **Power Automate – e-postvarsling** kan brukes i e-postvarslingsscenarioer.</span><span class="sxs-lookup"><span data-stu-id="4dd28-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="4dd28-139">Den kan brukes til å utløse varsel-e-postmeldinger til kandidater som ansettelsesteamet avviser i løpet av et hvilket som helst trinn i rekrutteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="4dd28-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="4dd28-140">Denne malen kan utvides til å spore endringer i kandidatstadiet i rekrutteringsprosessen og til å sende meldinger til ansettelsesteamet og kandidaten.</span><span class="sxs-lookup"><span data-stu-id="4dd28-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="4dd28-141">Generelt for enhetene som er lagret i Common Data Service, kan flyter defineres til å sende varslinger for hendelser som forekommer i Core HR, Attract eller Onboard.</span><span class="sxs-lookup"><span data-stu-id="4dd28-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="4dd28-142">For å laste ned malen **Power Automate – e-postvarsling** gå du til [Power Automate – e-postvarsling](https://go.microsoft.com/fwlink/?linkid=2082103) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="4dd28-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="4dd28-143">Power Automate – SQL-tilkobling og kjøring</span><span class="sxs-lookup"><span data-stu-id="4dd28-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="4dd28-144">Malen **Power Automate – SQL-tilkobling og kjøring** kobler til Microsoft SQL Server og aktiverer SQL-spørringer som skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="4dd28-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="4dd28-145">Selv om denne malen er utformet for å lese og oppdatere SQL-tabeller, kan den utvides, slik at den kan brukes til andre scenarioer.</span><span class="sxs-lookup"><span data-stu-id="4dd28-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="4dd28-146">Den kan for eksempel brukes til å fylle ut en oppsamlingstabell i Common Data Service med poster fra SQL Server og synkronisere oppsamlingstabellen jevnlig ved hjelp av en trinnvis push fra SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4dd28-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="4dd28-147">For å laste ned malen **Power Automate – SQL-tilkobling og kjøring** kan du gå til [Power Automate – SQL-tilkobling og kjøring](https://go.microsoft.com/fwlink/?linkid=2081789) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="4dd28-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="4dd28-148">Power Automate – SharePoint-integrering</span><span class="sxs-lookup"><span data-stu-id="4dd28-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="4dd28-149">Malen **Power Automate – SharePoint-integrering** kan brukes til å lese data fra en Microsoft SharePoint-liste, sammenligne listen med feltverdier for alle Common Data Service-enheter og sende resultatene av sammenligningen som en e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="4dd28-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="4dd28-150">En organisasjon kan ha et sett med ferdigheter som den har raskt behov for.</span><span class="sxs-lookup"><span data-stu-id="4dd28-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="4dd28-151">Disse ferdighetene kan lagres i SharePoint som en SharePoint-liste.</span><span class="sxs-lookup"><span data-stu-id="4dd28-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="4dd28-152">Når en kandidat søker på jobber som er oppført med et sett med nødvendige kvalifikasjoner, og hvis det er betydelig samsvar mellom kandidatens ferdigheter og ferdighetene som er lagret i SharePoint, sendes en e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="4dd28-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="4dd28-153">Dermed blir hastestillinger raskere fylt, fordi varslingene hjelper rekrutteringspersoner med å kontakte og ansette kandidater på tvers av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="4dd28-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="4dd28-154">Denne malen kan utvides, slik at den kan brukes på alle scenarioer som involverer SharePoint-integrering.</span><span class="sxs-lookup"><span data-stu-id="4dd28-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="4dd28-155">For å laste ned malen **Power Automate – SharePoint-integrering** går du til [Power Automate – SharePoint-integrering](https://go.microsoft.com/fwlink/?linkid=2082109) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="4dd28-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="4dd28-156">Henvisning-appen</span><span class="sxs-lookup"><span data-stu-id="4dd28-156">Referral App</span></span>
<span data-ttu-id="4dd28-157">Du kan bruke henvisningsappen for å legge til kandidater i en delt talentsamling.</span><span class="sxs-lookup"><span data-stu-id="4dd28-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="4dd28-158">Henviseren kan angi **fornavn**, **etternavn** **e-post** og **URL-adresse til LinkedIn** når en kandidat sendes inn.</span><span class="sxs-lookup"><span data-stu-id="4dd28-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="4dd28-159">Metadataene for kandidatkilden fylles deretter ut med henviserens informasjon.</span><span class="sxs-lookup"><span data-stu-id="4dd28-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="4dd28-160">Du kan bygge inn denne appen i Employee Self-Service (ESS) for innsending av henvisninger, eller du kan bruke den som en hyperkobling i firmaportalen og kjøre som en frittstående app.</span><span class="sxs-lookup"><span data-stu-id="4dd28-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="4dd28-161">Hvis du vil laste ned **henvisningsappen**, går du til [Dynamics 365 Talent-utvidelsesløsning: Henvisningsapp](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="4dd28-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="4dd28-162">Du kan importere denne appen og tilpasse den for å legge til flere funksjoner.</span><span class="sxs-lookup"><span data-stu-id="4dd28-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4dd28-163">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4dd28-163">Additional resources</span></span>

[<span data-ttu-id="4dd28-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="4dd28-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="4dd28-165">Overføre app mellom leiere og miljøer</span><span class="sxs-lookup"><span data-stu-id="4dd28-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)

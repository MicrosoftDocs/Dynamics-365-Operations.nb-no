---
title: Utvide Talent med Power Apps og Power Automate
description: Denne artikkelen beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 Talent – Attract som bruker Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529640"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="0840b-103">Utvide Talent med Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="0840b-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0840b-104">Denne artikkelen beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 Talent: Attract som bruker Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="0840b-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="0840b-105">Du kan importere løsningspakken som er tilknyttet hvert eksempel, i ditt Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="0840b-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="0840b-106">Du kan deretter bruke pakkene som retningslinjer eller som utgangspunkt til å implementere scenarioene som gjelder for organisasjonen din.</span><span class="sxs-lookup"><span data-stu-id="0840b-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0840b-107">Hvis du vil bruke malene og appen som er beskrevet i denne artikkelen, "som de er", må du teste dem å være sikker på at de dekker alle scenarioene som er spesifikke for implementeringen.</span><span class="sxs-lookup"><span data-stu-id="0840b-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="0840b-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="0840b-108">Prerequisites</span></span>

- <span data-ttu-id="0840b-109">Hvis du vil importere pakker, må brukerne ha **Miljøskaper**-tillatelsen.</span><span class="sxs-lookup"><span data-stu-id="0840b-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="0840b-110">Hvis du vil eksportere eller importere apper, må brukerne ha en Power Apps Plan 2-lisens eller en Power Apps Plan 2-prøvelisens.</span><span class="sxs-lookup"><span data-stu-id="0840b-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="0840b-111">Power Automate – skjematilkobling</span><span class="sxs-lookup"><span data-stu-id="0840b-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="0840b-112">Malen for **Power Automate – skjematilkobling** kan brukes til å lese data fra Microsoft Forms og lagre den i en Common Data Service-enhet.</span><span class="sxs-lookup"><span data-stu-id="0840b-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="0840b-113">Denne malen kan utvides slik at den kan brukes til andre scenarioer.</span><span class="sxs-lookup"><span data-stu-id="0840b-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="0840b-114">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="0840b-114">Here are some examples:</span></span>

- <span data-ttu-id="0840b-115">Registrer kandidatvurderinger.</span><span class="sxs-lookup"><span data-stu-id="0840b-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="0840b-116">Lagre resultater fra kursspørreskjema.</span><span class="sxs-lookup"><span data-stu-id="0840b-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="0840b-117">Kompiler et bibliotek med intervjuspørsmål for HR-administratorer.</span><span class="sxs-lookup"><span data-stu-id="0840b-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="0840b-118">Registrere en kandidats evaluering av intervjuprosessen</span><span class="sxs-lookup"><span data-stu-id="0840b-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="0840b-119">I Microsoft Dynamics 365: Attract kan du bruke skjemaer i kandidatportalen, der kandidater fyller ut detaljer.</span><span class="sxs-lookup"><span data-stu-id="0840b-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="0840b-120">Du kan også legge inn skjemaer som aktiviteter i en jobbmal.</span><span class="sxs-lookup"><span data-stu-id="0840b-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="0840b-121">Når en kandidat sender et skjema, fanger Microsoft Power Automate opp skjemainnsendingen, leser dataene og lagrer den i Common Data Service-enheten.</span><span class="sxs-lookup"><span data-stu-id="0840b-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="0840b-122">For å laste ned malen for **Power Automate – skjematilkobling** og den egendefinerte enhetsstrukturen, kan du gå til [Power Automate – skjematilkobling](https://go.microsoft.com/fwlink/?linkid=2081988) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="0840b-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="0840b-123">Power Automate – SharePoint-integrering</span><span class="sxs-lookup"><span data-stu-id="0840b-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="0840b-124">Malen **Power Automate – SharePoint-integrering** kan brukes til å lese data fra en Microsoft SharePoint-liste, sammenligne listen med feltverdier for alle Common Data Service-enheter og sende resultatene av sammenligningen som en e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="0840b-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="0840b-125">En organisasjon kan ha et sett med ferdigheter som den har raskt behov for.</span><span class="sxs-lookup"><span data-stu-id="0840b-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="0840b-126">Disse ferdighetene kan lagres i SharePoint som en SharePoint-liste.</span><span class="sxs-lookup"><span data-stu-id="0840b-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="0840b-127">Når en kandidat søker på jobber som er oppført med et sett med nødvendige kvalifikasjoner, og hvis det er betydelig samsvar mellom kandidatens ferdigheter og ferdighetene som er lagret i SharePoint, sendes en e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="0840b-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="0840b-128">Dette forenkler fylling av påkrevde hastestillinger raskere, fordi varslingene hjelper rekrutterere å ansette kandidater på tvers av hele organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="0840b-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="0840b-129">Denne malen kan utvides, slik at den kan brukes på alle scenarioer som involverer SharePoint-integrering.</span><span class="sxs-lookup"><span data-stu-id="0840b-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="0840b-130">For å laste ned malen **Power Automate – SharePoint-integrering** går du til [Power Automate – SharePoint-integrering](https://go.microsoft.com/fwlink/?linkid=2082109) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="0840b-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="0840b-131">Henvisning-appen</span><span class="sxs-lookup"><span data-stu-id="0840b-131">Referral App</span></span>

<span data-ttu-id="0840b-132">Du kan bruke henvisningsappen for å legge til kandidater i en delt talentsamling.</span><span class="sxs-lookup"><span data-stu-id="0840b-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="0840b-133">Henviseren kan angi **Fornavn**, **Etternavn** **E-post** og **URL-adresse for LinkedIn** når en kandidat sendes inn.</span><span class="sxs-lookup"><span data-stu-id="0840b-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="0840b-134">Metadataene for kandidatkilden fylles deretter ut med henviserens informasjon.</span><span class="sxs-lookup"><span data-stu-id="0840b-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="0840b-135">Du kan bygge inn denne appen i Employee Self-Service (ESS) for innsending av henvisninger, eller du kan bruke den som en hyperkobling i bedriftsportalen og kjøre den som en frittstående app.</span><span class="sxs-lookup"><span data-stu-id="0840b-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="0840b-136">Hvis du vil laste ned **henvisningsappen**, går du til [Dynamics 365 Talent-utvidelsesløsning: Henvisningsapp](https://www.microsoft.com/download/details.aspx?id=58497) på Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="0840b-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="0840b-137">Du kan importere denne appen og tilpasse den for å legge til flere funksjoner.</span><span class="sxs-lookup"><span data-stu-id="0840b-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0840b-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0840b-138">Additional resources</span></span>

[<span data-ttu-id="0840b-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="0840b-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="0840b-140">Overføre app mellom leiere og miljøer</span><span class="sxs-lookup"><span data-stu-id="0840b-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)

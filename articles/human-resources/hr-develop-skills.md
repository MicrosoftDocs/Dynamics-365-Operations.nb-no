---
title: Justere kompetansen til arbeidsstyrken etter bedriftens behov
description: Du kan følge opp ferdighetene som ansatte, søkere eller kontaktpersoner har eller bør ha for å oppfylle rollen effektivt. Du kan også angi kompetansen som kreves for en bestemt jobb.
author: andreabichsel
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: fc9996c31c3575ccf942907a66e59b00a344f3d1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793711"
---
# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="64fea-104">Justere kompetansen til arbeidsstyrken etter bedriftens behov</span><span class="sxs-lookup"><span data-stu-id="64fea-104">Align workforce skills with business needs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="64fea-105">Du kan følge opp ferdighetene som ansatte, søkere eller kontaktpersoner har eller bør ha for å oppfylle rollen effektivt.</span><span class="sxs-lookup"><span data-stu-id="64fea-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="64fea-106">Du kan også angi kompetansen som kreves for en bestemt jobb.</span><span class="sxs-lookup"><span data-stu-id="64fea-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="64fea-107">Eksempler på kompetanser du kan spore, omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="64fea-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="64fea-108">Tilsyn – Evne til å overvåke andres arbeid.</span><span class="sxs-lookup"><span data-stu-id="64fea-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="64fea-109">Ledelse – Evne til å lede ansatte og forretningsområder.</span><span class="sxs-lookup"><span data-stu-id="64fea-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="64fea-110">Planlegging – Evne til å tenke fremover, forme fremtidsplaner og gjennomføre dem.</span><span class="sxs-lookup"><span data-stu-id="64fea-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="64fea-111">HTML – Evne til å skrive HTML-kode.</span><span class="sxs-lookup"><span data-stu-id="64fea-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="64fea-112">Før du kan tilordne en kompetanse til en person eller en jobb, opprette et kompetansesøk eller opprette en kompetanseprofil, må du angi informasjon om kompetansen på **Kompetanse**-siden.</span><span class="sxs-lookup"><span data-stu-id="64fea-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="64fea-113">Du kan velge en ferdighetstype og en vurderingsmodell for hver kompetanse.</span><span class="sxs-lookup"><span data-stu-id="64fea-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="64fea-114">Vurderingsmodeller</span><span class="sxs-lookup"><span data-stu-id="64fea-114">Rating models</span></span>
<span data-ttu-id="64fea-115">Vurderingsmodeller bidrar til å vurdere en persons faktiske kompetansenivå, nivået de bør arbeide for å oppnå, eller kompetansenivået som kreves for en jobb.</span><span class="sxs-lookup"><span data-stu-id="64fea-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="64fea-116">Du kan angi opptil ti nivåer for en vurderingsmodell.</span><span class="sxs-lookup"><span data-stu-id="64fea-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="64fea-117">Hvert nivå i en vurderingsmodell tilordnes en faktor.</span><span class="sxs-lookup"><span data-stu-id="64fea-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="64fea-118">Omregningsverdien brukes til å normalisere resultatene for kompetanse som bruker forskjellige vurderingsmodeller.</span><span class="sxs-lookup"><span data-stu-id="64fea-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="64fea-119">Faktoren må være et tall mellom 0-9 og hvert nivå må ha en unik faktor</span><span class="sxs-lookup"><span data-stu-id="64fea-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="64fea-120">Nivåer med høyere faktorverdier vektlegges mer i en vurderingsmodell.</span><span class="sxs-lookup"><span data-stu-id="64fea-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="64fea-121">Angi jobbkompetanse</span><span class="sxs-lookup"><span data-stu-id="64fea-121">Specify job skills</span></span>
<span data-ttu-id="64fea-122">Når du angir informasjon om en jobb, kan du angi kompetansen som en person skal ha for å utføre arbeidet som kreves for jobben.</span><span class="sxs-lookup"><span data-stu-id="64fea-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="64fea-123">I tillegg kan du angi ønsket nivå for hver type kompetanse samt betydningsnivåer til kompetansen.</span><span class="sxs-lookup"><span data-stu-id="64fea-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="64fea-124">Forskjellige jobber kan kreve forskjellige betydningsnivåer for den sammen kompetansen.</span><span class="sxs-lookup"><span data-stu-id="64fea-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="64fea-125">Angi kompetanse for ansatte, søkere eller kontakter</span><span class="sxs-lookup"><span data-stu-id="64fea-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="64fea-126">Du kan angi målkompetanse eller faktisk kompetanse for arbeidere, søkere eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="64fea-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="64fea-127">En målkompetanse er en kompetanse en person ønsker å oppnå.</span><span class="sxs-lookup"><span data-stu-id="64fea-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="64fea-128">En faktisk kompetanse er en kompetanse en person har.</span><span class="sxs-lookup"><span data-stu-id="64fea-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="64fea-129">Kompetansetilordning og kompetansetilordningsprofiler</span><span class="sxs-lookup"><span data-stu-id="64fea-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="64fea-130">Du kan opprette et kompetanesøk for å finne en arbeider, søker eller kontaktperson som er kvalifisert til å utføre en bestemt type oppgave.</span><span class="sxs-lookup"><span data-stu-id="64fea-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="64fea-131">Kompetanesøk søker på tvers av ferdigheter, utdanning, sertifikater, tillitsverv og prosjekterfaring, og returnerer et resultat som samsvarer med kriteriene som er angitt.</span><span class="sxs-lookup"><span data-stu-id="64fea-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="64fea-132">Det kan for eksempel være nyttig å vite hvilke ansatte i organisasjonen som har opptjent deres CPA.</span><span class="sxs-lookup"><span data-stu-id="64fea-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="64fea-133">Med profiler for kompetansesøk kan du søke etter nåværende ansatte eller kandidater med kvalifikasjoner som direkte samsvarer med bedriftens behov.</span><span class="sxs-lookup"><span data-stu-id="64fea-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="64fea-134">Du kan for eksempel opprette en profil for kompetansesøk for en åpen stilling i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="64fea-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="64fea-135">Ved å opprette en profil for en bestemt jobb og kopiere kompetanse, utdanning og sertifikater fra denne jobben til profilen, kan du raskt søke arbeidere, søkere og kontaktpersoner som samsvarer med ett eller flere av kriteriene som er angitt på profilen, og vise en liste over kandidater som har kvalifikasjoner som nærmest oppfyller kompetansen som kreves for jobben.</span><span class="sxs-lookup"><span data-stu-id="64fea-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

> <span data-ttu-id="64fea-136">**Obs!** Bare arbeidere, søkere eller kontaktpersoner som er valgt for inkludering i kompetansesøk, kan vises i resultatlisten for kompetansesøk eller inkluderes i en kompetanseprofil.</span><span class="sxs-lookup"><span data-stu-id="64fea-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="64fea-137">Hvis du vil ta med en arbeider, søker eller kontaktperson i kompetansesøk, angir du valget **Inkluder i kompetansesøk** til Ja i de følgende sidene:</span><span class="sxs-lookup"><span data-stu-id="64fea-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>
> 
> + <span data-ttu-id="64fea-138">Arbeider</span><span class="sxs-lookup"><span data-stu-id="64fea-138">Worker</span></span>
> + <span data-ttu-id="64fea-139">Ansatt</span><span class="sxs-lookup"><span data-stu-id="64fea-139">Employee</span></span>
> + <span data-ttu-id="64fea-140">Søker</span><span class="sxs-lookup"><span data-stu-id="64fea-140">Applicant</span></span>
> + <span data-ttu-id="64fea-141">Kontakter</span><span class="sxs-lookup"><span data-stu-id="64fea-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="64fea-142">Kompetansegapanalyse og kompetanseprofilanalyse</span><span class="sxs-lookup"><span data-stu-id="64fea-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="64fea-143">Du kan opprette en analyse av kompetanseprofil for å vise en kompetanseliste for en arbeider, søker eller kontaktperson fra en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="64fea-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="64fea-144">Du kan opprette en kompetansegapanalyse hvis du vil sammenligne kompetansen til en person med kompetansen som kreves for en bestemt jobb.</span><span class="sxs-lookup"><span data-stu-id="64fea-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  




[!INCLUDE[footer-include](../includes/footer-banner.md)]
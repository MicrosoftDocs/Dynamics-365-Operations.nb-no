---
title: Konfigurere kompetanse
description: Du kan spore arbeiderens kompetanse i Dynamics 365 Human Resources. Du kan også angi kompetansen som kreves for en bestemt jobb.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076565"
---
# <a name="configure-skills"></a><span data-ttu-id="899c4-104">Konfigurere kompetanse</span><span class="sxs-lookup"><span data-stu-id="899c4-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="899c4-105">Du kan spore arbeiderens kompetanse i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="899c4-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="899c4-106">Du kan også angi kompetansen som kreves for en bestemt jobb.</span><span class="sxs-lookup"><span data-stu-id="899c4-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="899c4-107">Eksempler på kompetanser du kan spore:</span><span class="sxs-lookup"><span data-stu-id="899c4-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="899c4-108">Tilsyn – Evne til å overvåke andres arbeid.</span><span class="sxs-lookup"><span data-stu-id="899c4-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="899c4-109">Ledelse – Evne til å lede ansatte og forretningsområder.</span><span class="sxs-lookup"><span data-stu-id="899c4-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="899c4-110">Planlegging – Evne til å tenke fremover, forme fremtidsplaner og gjennomføre dem.</span><span class="sxs-lookup"><span data-stu-id="899c4-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="899c4-111">HTML – Evne til å skrive HTML-kode.</span><span class="sxs-lookup"><span data-stu-id="899c4-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="899c4-112">Hvis du ikke allerede har definert kompetansetyper og vurderingsmodeller, må du legge til noen før du kan opprette kompentanser.</span><span class="sxs-lookup"><span data-stu-id="899c4-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="899c4-113">Følgende personer kan angi kompetanser for en arbeider:</span><span class="sxs-lookup"><span data-stu-id="899c4-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="899c4-114">Arbeidere kan registrere kompetanser for seg selv i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="899c4-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="899c4-115">Disse kompetansene krever ledergodkjenning.</span><span class="sxs-lookup"><span data-stu-id="899c4-115">These skills require manager approval.</span></span>
- <span data-ttu-id="899c4-116">Ledere kan angi kompetanser for arbeiderne sine.</span><span class="sxs-lookup"><span data-stu-id="899c4-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="899c4-117">Du kan opprette en arbeidsflyt som godkjenner disse kompetansene automatisk.</span><span class="sxs-lookup"><span data-stu-id="899c4-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="899c4-118">Opprette en kompetansetype</span><span class="sxs-lookup"><span data-stu-id="899c4-118">Create a skill type</span></span>

<span data-ttu-id="899c4-119">Kompetansetyper er kategorier som individuelle kompetanser faller under, for eksempel Administrasjon eller Salg.</span><span class="sxs-lookup"><span data-stu-id="899c4-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="899c4-120">Velg **Koblinger** i arbeidsområdet for **Ansattutvikling**.</span><span class="sxs-lookup"><span data-stu-id="899c4-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="899c4-121">Velg **Kompetansetyper** under **Kompetanseoppsett**.</span><span class="sxs-lookup"><span data-stu-id="899c4-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="899c4-122">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="899c4-122">Select **New**.</span></span>

4. <span data-ttu-id="899c4-123">Fyll ut følgende felt:</span><span class="sxs-lookup"><span data-stu-id="899c4-123">Complete the following fields:</span></span>

   - <span data-ttu-id="899c4-124">**Kompetansetype**: Angi et navn på kompetansetypen.</span><span class="sxs-lookup"><span data-stu-id="899c4-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="899c4-125">**Beskrivelse**: Skriv inn en beskrivelse av kompetansetypen.</span><span class="sxs-lookup"><span data-stu-id="899c4-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="899c4-126">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="899c4-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="899c4-127">Opprette en vurderingsmodell</span><span class="sxs-lookup"><span data-stu-id="899c4-127">Create a rating model</span></span>

<span data-ttu-id="899c4-128">Vurderingsmodeller bidrar til å vurdere en persons faktiske kompetansenivå, nivået de bør arbeide for å oppnå, eller kompetansenivået som kreves for en jobb.</span><span class="sxs-lookup"><span data-stu-id="899c4-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="899c4-129">Hvert nivå i en vurderingsmodell tilordnes en faktor.</span><span class="sxs-lookup"><span data-stu-id="899c4-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="899c4-130">Velg **Koblinger** i arbeidsområdet for **Ansattutvikling**.</span><span class="sxs-lookup"><span data-stu-id="899c4-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="899c4-131">Velg **Vurderingsmodeller** under **Kompetanseoppsett**.</span><span class="sxs-lookup"><span data-stu-id="899c4-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="899c4-132">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="899c4-132">Select **New**.</span></span>

4. <span data-ttu-id="899c4-133">Fyll ut følgende felt:</span><span class="sxs-lookup"><span data-stu-id="899c4-133">Complete the following fields:</span></span>

   - <span data-ttu-id="899c4-134">**Vurdering**: Angi et navn på vurderingsmodellen, for eksempel **Kompetanser**.</span><span class="sxs-lookup"><span data-stu-id="899c4-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="899c4-135">**Beskrivelse** : Angi en beskrivelse av vurderingsmodellen, for eksempel **Kompetansevurderinger**.</span><span class="sxs-lookup"><span data-stu-id="899c4-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="899c4-136">Velg **Ny** i **Nivåer**-delen.</span><span class="sxs-lookup"><span data-stu-id="899c4-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="899c4-137">Fyll ut følgende felt for hvert nivå du vil legge til:</span><span class="sxs-lookup"><span data-stu-id="899c4-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="899c4-138">**Nivå**: Angi et navn på nivået.</span><span class="sxs-lookup"><span data-stu-id="899c4-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="899c4-139">**Beskrivelse**: Angi en beskrivelse av nivået.</span><span class="sxs-lookup"><span data-stu-id="899c4-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="899c4-140">**Faktor** : Angi en faktorverdi fra 0-9.</span><span class="sxs-lookup"><span data-stu-id="899c4-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="899c4-141">Faktorer bidrar til å normalisere resultatene av kompetanser som bruker ulike vurderingsmodeller.</span><span class="sxs-lookup"><span data-stu-id="899c4-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="899c4-142">Hvert nivå må ha en unik faktor.</span><span class="sxs-lookup"><span data-stu-id="899c4-142">Each level must have a unique factor.</span></span> <span data-ttu-id="899c4-143">Nivåer med høyere faktorverdier vektlegges mer i en vurderingsmodell.</span><span class="sxs-lookup"><span data-stu-id="899c4-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="899c4-144">Fortsett å legge til nivåer etter behov.</span><span class="sxs-lookup"><span data-stu-id="899c4-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="899c4-145">Du kan angi opptil 10 nivåer for hver vurderingsmodell.</span><span class="sxs-lookup"><span data-stu-id="899c4-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="899c4-146">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="899c4-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="899c4-147">Opprette en kompetanse</span><span class="sxs-lookup"><span data-stu-id="899c4-147">Create a skill</span></span>

<span data-ttu-id="899c4-148">Før du kan tilordne en kompetanse eller opprette et kompetansesøk eller en kompetanseprofil, må du angi informasjon om kompetansen på **Kompetanse**-siden.</span><span class="sxs-lookup"><span data-stu-id="899c4-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="899c4-149">Du kan velge en ferdighetstype og en vurderingsmodell for hver kompetanse.</span><span class="sxs-lookup"><span data-stu-id="899c4-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="899c4-150">Velg **Koblinger** i arbeidsområdet for **Ansattutvikling**.</span><span class="sxs-lookup"><span data-stu-id="899c4-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="899c4-151">Velg **Kompetanser** under **Kompetanseoppsett**.</span><span class="sxs-lookup"><span data-stu-id="899c4-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="899c4-152">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="899c4-152">Select **New**.</span></span>

4. <span data-ttu-id="899c4-153">Fyll ut følgende felt:</span><span class="sxs-lookup"><span data-stu-id="899c4-153">Complete the following fields:</span></span>

   - <span data-ttu-id="899c4-154">**Kompetanse**: Angi et navn på kompetansen.</span><span class="sxs-lookup"><span data-stu-id="899c4-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="899c4-155">**Beskrivelse**: Skriv inn en beskrivelse av kompetansen.</span><span class="sxs-lookup"><span data-stu-id="899c4-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="899c4-156">**Vurdering**: Velg vurderingsmodellen du vil bruke for denne kompetansen.</span><span class="sxs-lookup"><span data-stu-id="899c4-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="899c4-157">**Kompetansetype** – Velg fra listen over kompetansetyper.</span><span class="sxs-lookup"><span data-stu-id="899c4-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="899c4-158">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="899c4-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="899c4-159">Se også</span><span class="sxs-lookup"><span data-stu-id="899c4-159">See also</span></span>

[<span data-ttu-id="899c4-160">Angi ferdigheter</span><span class="sxs-lookup"><span data-stu-id="899c4-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="899c4-161">Kompetansesøk</span><span class="sxs-lookup"><span data-stu-id="899c4-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
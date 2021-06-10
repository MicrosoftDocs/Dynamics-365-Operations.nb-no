---
title: Kompetansesøk
description: Du kan opprette et kompetansesøk for å finne en kvalifisert person i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
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
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076607"
---
# <a name="map-skills"></a><span data-ttu-id="55c33-103">Kompetansesøk</span><span class="sxs-lookup"><span data-stu-id="55c33-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="55c33-104">Du kan opprette et kompetansesøk for å finne en kvalifisert person i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="55c33-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="55c33-105">Søk i kompetansesøk gir resultater for kriterier du angir ved å se gjennom følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="55c33-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="55c33-106">Kompetanse</span><span class="sxs-lookup"><span data-stu-id="55c33-106">Skills</span></span>
- <span data-ttu-id="55c33-107">Utdanning</span><span class="sxs-lookup"><span data-stu-id="55c33-107">Education</span></span>
- <span data-ttu-id="55c33-108">Attester</span><span class="sxs-lookup"><span data-stu-id="55c33-108">Certificates</span></span>
- <span data-ttu-id="55c33-109">Stillinger</span><span class="sxs-lookup"><span data-stu-id="55c33-109">Positions</span></span>
- <span data-ttu-id="55c33-110">Prosjekterfaring</span><span class="sxs-lookup"><span data-stu-id="55c33-110">Project experience</span></span>

<span data-ttu-id="55c33-111">Du kan for eksempel finne personer i organisasjonen som har opptjent CPA.</span><span class="sxs-lookup"><span data-stu-id="55c33-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="55c33-112">Med profiler for kompetansesøk kan du søke etter nåværende ansatte eller kandidater med kvalifikasjoner som direkte samsvarer med bedriftens behov.</span><span class="sxs-lookup"><span data-stu-id="55c33-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="55c33-113">Bare arbeidere, søkere eller kontaktpersoner som er valgt for inkludering i kompetansesøk, vises i resultatlisten for kompetansesøk eller inkluderes i en kompetanseprofil.</span><span class="sxs-lookup"><span data-stu-id="55c33-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="55c33-114">Hvis du vil ta med en person i kompetansesøk, angir du valget **Inkluder i kompetansesøk** til **Ja** i de følgende sidene:</span><span class="sxs-lookup"><span data-stu-id="55c33-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="55c33-115">Worker</span><span class="sxs-lookup"><span data-stu-id="55c33-115">Worker</span></span><br>
> - <span data-ttu-id="55c33-116">Ansatt</span><span class="sxs-lookup"><span data-stu-id="55c33-116">Employee</span></span><br>
> - <span data-ttu-id="55c33-117">Søker</span><span class="sxs-lookup"><span data-stu-id="55c33-117">Applicant</span></span><br>
> - <span data-ttu-id="55c33-118">Kontakter</span><span class="sxs-lookup"><span data-stu-id="55c33-118">Contacts</span></span><br>

<span data-ttu-id="55c33-119">Hvis du vil opprette et kompetansesøk, kan du gå **Ansattutvikling > Koblinger > Kompetansesøk**.</span><span class="sxs-lookup"><span data-stu-id="55c33-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="55c33-120">Hvis du vil opprette en kompetansesøkprofil, kan du gå **Ansattutvikling > Koblinger > Kompetansesøkprofiler**.</span><span class="sxs-lookup"><span data-stu-id="55c33-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="55c33-121">Kompetansegapanalyse og kompetanseprofilanalyse</span><span class="sxs-lookup"><span data-stu-id="55c33-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="55c33-122">Du kan opprette en kompetanseprofilanalyse for å vise en liste over en persons kompetanse.</span><span class="sxs-lookup"><span data-stu-id="55c33-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="55c33-123">Du kan opprette en kompetansegapanalyse hvis du vil sammenligne kompetansen til en person og ferdighetene som kreves for en jobb.</span><span class="sxs-lookup"><span data-stu-id="55c33-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="55c33-124">Hvis du vil opprette en gapanalyse, kan du gå til **Ansattutvikling > Koblinger > Analysejobb for kompetansegap – person**.</span><span class="sxs-lookup"><span data-stu-id="55c33-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="55c33-125">Hvis du vil opprette en kompetanseprofilanalyse, kan du gå **Ansattutvikling > Koblinger > Analyse av kompetanseprofil**.</span><span class="sxs-lookup"><span data-stu-id="55c33-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="55c33-126">Se også</span><span class="sxs-lookup"><span data-stu-id="55c33-126">See also</span></span>

[<span data-ttu-id="55c33-127">Konfigurere kompetanse</span><span class="sxs-lookup"><span data-stu-id="55c33-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="55c33-128">Angi ferdigheter</span><span class="sxs-lookup"><span data-stu-id="55c33-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
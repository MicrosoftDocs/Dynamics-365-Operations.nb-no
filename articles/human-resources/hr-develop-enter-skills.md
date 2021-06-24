---
title: Angi ferdigheter
description: Jobber og ledere kan angi ferdigheter i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193983"
---
# <a name="enter-skills"></a><span data-ttu-id="665cf-103">Angi ferdigheter</span><span class="sxs-lookup"><span data-stu-id="665cf-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="665cf-104">Du kan angi målkompetanse eller faktisk kompetanse for arbeidere, søkere eller kontakter i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="665cf-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="665cf-105">En målkompetanse er en kompetanse en person ønsker å oppnå.</span><span class="sxs-lookup"><span data-stu-id="665cf-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="665cf-106">En faktisk kompetanse er en kompetanse en person har.</span><span class="sxs-lookup"><span data-stu-id="665cf-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="665cf-107">Opprette en arbeidsflyt for å godkjenne kompetanse automatisk</span><span class="sxs-lookup"><span data-stu-id="665cf-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="665cf-108">Hvis du vil legge inn kompetanse uten å kreve godkjenning, må du opprette en arbeidsflyt for å godkjenne kompetanse automatisk.</span><span class="sxs-lookup"><span data-stu-id="665cf-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="665cf-109">Kompetanse som angis av ansatte, krever alltid ledergodkjenning.</span><span class="sxs-lookup"><span data-stu-id="665cf-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="665cf-110">Denne arbeidsflyten godkjenner bare automatisk kompetanse som angis av ledere på vegne av arbeiderne.</span><span class="sxs-lookup"><span data-stu-id="665cf-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="665cf-111">I arbeidsområdet **Personaladministrasjon** velger du **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="665cf-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="665cf-112">Under **Oppsett** velger du **Personalarbeidsflyter**.</span><span class="sxs-lookup"><span data-stu-id="665cf-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="665cf-113">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="665cf-113">Select **New**.</span></span>

4. <span data-ttu-id="665cf-114">Velg **Arbeiderkompetanse** i ruten **Opprett arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="665cf-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="665cf-115">[![Velge arbeidsflyt for arbeiderkompetanse](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="665cf-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="665cf-116">Velg **Åpne** i dialogboksen **Åpne denne filen?**.</span><span class="sxs-lookup"><span data-stu-id="665cf-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="665cf-117">Angi påloggingsinformasjon når du blir spurt.</span><span class="sxs-lookup"><span data-stu-id="665cf-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="665cf-118">Velg arbeidsflytelementet **Godkjenn ferdigheter** i redigeringsprogrammet, og dra det til lerretet.</span><span class="sxs-lookup"><span data-stu-id="665cf-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="665cf-119">[![Velge arbeidsflytelementet Godkjenn ferdigheter](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="665cf-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="665cf-120">Koble **Start**-elementet til elementet **Godkjenn ferdigheter 1**, og koble deretter elementet **Godkjenn ferdigheter 1** til **Slutt**-elementet.</span><span class="sxs-lookup"><span data-stu-id="665cf-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="665cf-121">Det kan hende at du må rulle ned for å se **Slutt**-elementet.</span><span class="sxs-lookup"><span data-stu-id="665cf-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="665cf-122">Du kan dra det nærmere de andre elementene.</span><span class="sxs-lookup"><span data-stu-id="665cf-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="665cf-123">[![Koble arbeidsflytelementer](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="665cf-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="665cf-124">Dobbeltklikk arbeidsflytelementet **Godkjenn ferdigheter 1**, og høyreklikk **Trinn 1**-elementet.</span><span class="sxs-lookup"><span data-stu-id="665cf-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="665cf-125">Høyreklikk trinn **Trinn 1**-elementet, og velg deretter **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="665cf-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="665cf-126">Velg **Betingelse**-vinduet på venstre navigasjonslinje i **Egenskap**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="665cf-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="665cf-127">Velg **Kjør bare dette trinnet når følgende betingelse er oppfylt**.</span><span class="sxs-lookup"><span data-stu-id="665cf-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="665cf-128">Velg **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="665cf-128">Select **Add condition**.</span></span> <span data-ttu-id="665cf-129">Velg **Ansattselvbetjeningsferdigheter** etter **Hvor**, og velg deretter **Ansattselvbetjeningsferdigheter.Person**.</span><span class="sxs-lookup"><span data-stu-id="665cf-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="665cf-130">Etter **er,** velg **felt**, og velg deretter **Bruker til person-forhold. Person**.</span><span class="sxs-lookup"><span data-stu-id="665cf-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="665cf-131">[![Angi betingelse](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="665cf-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="665cf-132">Velg **Tilordning** på venstre navigasjonslinje.</span><span class="sxs-lookup"><span data-stu-id="665cf-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="665cf-133">Velg **Hierarki** i kategorien **Tilordningstype**.</span><span class="sxs-lookup"><span data-stu-id="665cf-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="665cf-134">Velg **Lederhierarki** i feltet **Hierarkitype:** i kategorien **Hierarkivalg**.</span><span class="sxs-lookup"><span data-stu-id="665cf-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="665cf-135">[![Angi lederhierarki](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="665cf-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="665cf-136">Velg **Lukk**, velg **Arbeidsflyt** i opprettelsesarbeidsflyten, og velg deretter **Lagre og lukk**.</span><span class="sxs-lookup"><span data-stu-id="665cf-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="665cf-137">Hvis du vil ha mer informasjon om hvordan du oppretter arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="665cf-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="665cf-138">Angi kompetanse for en arbeider</span><span class="sxs-lookup"><span data-stu-id="665cf-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="665cf-139">Velg en arbeider.</span><span class="sxs-lookup"><span data-stu-id="665cf-139">Select a worker.</span></span>

2. <span data-ttu-id="665cf-140">Velg **Person** på handlingslinjen til **Person**, og velg deretter **Kompetanse**.</span><span class="sxs-lookup"><span data-stu-id="665cf-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="665cf-141">Fyll ut følgende felt for hver kompetanse på **Kompetanse**-siden:</span><span class="sxs-lookup"><span data-stu-id="665cf-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="665cf-142">**Kompetanse**: Velg en kompetanse.</span><span class="sxs-lookup"><span data-stu-id="665cf-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="665cf-143">**Nivåtype** : Velg **Faktisk** for en kompetanse arbeideren allerede har, eller velg **Mål** for en kompetanse som arbeideren arbeider mot.</span><span class="sxs-lookup"><span data-stu-id="665cf-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="665cf-144">**Nivå** : Velg et nivå for arbeiderens kompetanse.</span><span class="sxs-lookup"><span data-stu-id="665cf-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="665cf-145">**Nivådato**: Velg en dato i kalenderverktøyet.</span><span class="sxs-lookup"><span data-stu-id="665cf-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="665cf-146">**Eksaminator**: Velg om nødvendig en eksaminator fra listen.</span><span class="sxs-lookup"><span data-stu-id="665cf-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="665cf-147">Du kan filtrere søket.</span><span class="sxs-lookup"><span data-stu-id="665cf-147">You can filter your search.</span></span>
   - <span data-ttu-id="665cf-148">**År med erfaring**: Angi år med erfaring.</span><span class="sxs-lookup"><span data-stu-id="665cf-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="665cf-149">**Verifisert**: Hvis kompetansen er kontrollert, merker du av for dette.</span><span class="sxs-lookup"><span data-stu-id="665cf-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="665cf-150">**Kontrollert av** : Angi navnet på kontrolløren.</span><span class="sxs-lookup"><span data-stu-id="665cf-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="665cf-151">Når du er ferdig med å angi ferdigheter, velger du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="665cf-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="665cf-152">Se også</span><span class="sxs-lookup"><span data-stu-id="665cf-152">See also</span></span>

[<span data-ttu-id="665cf-153">Konfigurere kompetanse</span><span class="sxs-lookup"><span data-stu-id="665cf-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="665cf-154">Kompetansesøk</span><span class="sxs-lookup"><span data-stu-id="665cf-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
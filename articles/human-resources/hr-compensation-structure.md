---
title: Utvikle en kompensasjonsstruktur
description: Denne artikkelen leder deg gjennom prosessen med å opprette en fast kompensasjonsplan og registrere ansatte i planen gjennom rettighetsregler.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: de715b7fda2f1548f2f443b9e0f6d09f5b881d61
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2020
ms.locfileid: "3034269"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="9c40c-103">Utvikle en kompensasjonsstruktur</span><span class="sxs-lookup"><span data-stu-id="9c40c-103">Develop a compensation structure</span></span>

<span data-ttu-id="9c40c-104">Denne artikkelen leder deg gjennom prosessen med å opprette en fast kompensasjonsplan og registrere ansatte i planen gjennom rettighetsregler.</span><span class="sxs-lookup"><span data-stu-id="9c40c-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="9c40c-105">Denne artikkelen bruker USMF-demodataene og gjelder ansvarlige for kompensasjon og fordeler.</span><span class="sxs-lookup"><span data-stu-id="9c40c-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="9c40c-106">Opprette en fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="9c40c-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="9c40c-107">Velg **Kompensasjonsstyring**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="9c40c-108">Velg **Faste kompensasjonsplaner**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="9c40c-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-109">Select **New**.</span></span>

4. <span data-ttu-id="9c40c-110">Angi en verdi i **Plan**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c40c-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="9c40c-111">Angi en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="9c40c-112">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="9c40c-113">I **Type**-feltet velger du om den faste kompensasjonsplanen er en plan for **segment**, **klasse** eller **trinn**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="9c40c-114">Avmerkingsboksen **Anbefaling tillatt** fungerer som en standardverdi for alle handlinger som er lagt til i denne planen i en prosesshendelse.</span><span class="sxs-lookup"><span data-stu-id="9c40c-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="9c40c-115">Ved å tillate anbefalinger kan du overstyre det beregnede retningslinjebeløpet ved behandling av kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="9c40c-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="9c40c-116">Med feltet **Utenfor områdetoleranse** kan du angi hvordan du vil håndtere kompensasjonsbeløp som faller utenfor det angitte kompensasjonsstrukturområdet for det angitte nivået.</span><span class="sxs-lookup"><span data-stu-id="9c40c-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="9c40c-117">Hvis du angir feltet **Utenfor område-toleranse** til **Ingenl**, kan du bruke et hvilket som helst kompensasjonsbeløp.</span><span class="sxs-lookup"><span data-stu-id="9c40c-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="9c40c-118">**Myk toleranse** varsler brukeren hvis kompensasjonsbeløpet er mindre enn det minste eller større enn det maksimale referansepunktbeløpet for dette nivået.</span><span class="sxs-lookup"><span data-stu-id="9c40c-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="9c40c-119">Brukeren kan ignorere advarselen og fortsette.</span><span class="sxs-lookup"><span data-stu-id="9c40c-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="9c40c-120">**Hard toleranse** genererer en feil hvis en ansatts kompensasjon er utenfor de minste og største referansepunktene for nivået, og justerer automatisk den ansattes kompensasjon slik at den faller innenfor området.</span><span class="sxs-lookup"><span data-stu-id="9c40c-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="9c40c-121">Feltet **Ansettelsesregel** beregner kompensasjonen til en ansatt i løpet av en prosesshendelse.</span><span class="sxs-lookup"><span data-stu-id="9c40c-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="9c40c-122">En **ansettelsesregel** med **prosent** beregner en økning som er fordelt på hele tiden arbeideren har vært ansatt i syklusen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="9c40c-123">Skriv inn en verdi i **Valuta**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c40c-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="9c40c-124">Angi eller velg en verdi i feltet **Konverteringer av lønnssats**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="9c40c-125">Vis delen **Områdeutnyttelsesmatrise**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="9c40c-126">Du kan også legge til områdeutnyttelsesposter for å få ansatte til midtpunktet raskere og øke tiden det tar å nå det maksimale antallet av området.</span><span class="sxs-lookup"><span data-stu-id="9c40c-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="9c40c-127">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-127">Select **Save**.</span></span> <span data-ttu-id="9c40c-128">Dermed aktiveres knappen **Angi kompensasjon**, og du kan fortsette å definere kompensasjonsstrukturen for planen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="9c40c-129">Velg **Angi kompensasjon**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-129">Select **Set up compensation**.</span></span> <span data-ttu-id="9c40c-130">Du kan opprette en kompensasjonsstruktur på en av følgende tre måter:</span><span class="sxs-lookup"><span data-stu-id="9c40c-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="9c40c-131">Opprett en helt ny struktur ved å velge et sett med referansepunkt og legge til nivåene for å opprette din egen struktur.</span><span class="sxs-lookup"><span data-stu-id="9c40c-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="9c40c-132">Kopier en kompensasjonsstruktur fra en eksisterende plan som utgangspunkt, og endre den for den nye planen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="9c40c-133">Velg et eksisterende kompensasjonsrutenett.</span><span class="sxs-lookup"><span data-stu-id="9c40c-133">Select an existing compensation grid.</span></span> <span data-ttu-id="9c40c-134">Hvis en annen plan allerede bruker kompensasjonsrutenettet, gjenspeiler den andre planen også endringer du gjør i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="9c40c-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="9c40c-135">Velg **Opprett ny fra eksisterende kompensasjonsmatrise**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="9c40c-136">Angi eller velg en verdi i feltet **Kopier fra rutenett**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="9c40c-137">Du kan også endre navnet på det nye kompensasjonsrutenettet som du oppretter ved å kopiere det valgte rutenettet.</span><span class="sxs-lookup"><span data-stu-id="9c40c-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="9c40c-138">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-138">Select **OK**.</span></span>

19. <span data-ttu-id="9c40c-139">Velg **Masseendring**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-139">Select **Mass change**.</span></span> <span data-ttu-id="9c40c-140">Ved hjelp av **Masseendring** kan du beholde kompensasjonsmatrisebeløpene ved å bruke en økning i prosent eller et flatt beløp på én eller flere nivåer eller referansepunkt.</span><span class="sxs-lookup"><span data-stu-id="9c40c-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="9c40c-141">Angi et tall i **Justeringsbeløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c40c-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="9c40c-142">Merk eller fjern merking for alle rader i listen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="9c40c-143">Klikk **Bruk på rutenett**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="9c40c-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9c40c-144">Close the page.</span></span> <span data-ttu-id="9c40c-145">Når du har opprettet kompensasjonsstrukturen, kan du velge hvilke av referansepunktene som skal brukes som kontrollpunktet for den faste kompensasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="9c40c-146">Kontrollpunktet brukes til å beregne den ansattes Komp.grad.</span><span class="sxs-lookup"><span data-stu-id="9c40c-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="9c40c-147">Angi eller velg en verdi i feltet **Kontrollpunkt**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="9c40c-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9c40c-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="9c40c-149">Opprette en rettighetsregel for den faste kompensasjonsplanen</span><span class="sxs-lookup"><span data-stu-id="9c40c-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="9c40c-150">Du kan ikke tilordne en fast kompensasjonsplan til en ansatt før du definerer rettighetsregler for planen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="9c40c-151">Velg **Rettighetsregler**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="9c40c-152">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-152">Select **New**.</span></span>

3. <span data-ttu-id="9c40c-153">Angi eller velg en verdi i feltet **Rettighet**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="9c40c-154">Angi en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="9c40c-155">Angi en dato i feltet **Gyldighetsdato**.</span><span class="sxs-lookup"><span data-stu-id="9c40c-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="9c40c-156">Både faste og variable kompensasjonsplaner bruker rettighetsregler.</span><span class="sxs-lookup"><span data-stu-id="9c40c-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="9c40c-157">Velg plantypen i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c40c-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="9c40c-158">Angi eller velg en verdi i **Plan**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c40c-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="9c40c-159">Velg kriteriene en ansatt må oppfylle for å være kvalifisert for kompensasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="9c40c-160">Vilkårene kan omfatte:</span><span class="sxs-lookup"><span data-stu-id="9c40c-160">Criteria can include:</span></span>

    - <span data-ttu-id="9c40c-161">**Avdeling**</span><span class="sxs-lookup"><span data-stu-id="9c40c-161">**Department**</span></span>
    - <span data-ttu-id="9c40c-162">**Fagforening**</span><span class="sxs-lookup"><span data-stu-id="9c40c-162">**Labor union**</span></span>
    - <span data-ttu-id="9c40c-163">**Sted** (**Kompensasjonsområde**)</span><span class="sxs-lookup"><span data-stu-id="9c40c-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="9c40c-164">**Jobb**</span><span class="sxs-lookup"><span data-stu-id="9c40c-164">**Job**</span></span>
    - <span data-ttu-id="9c40c-165">**Funksjon**</span><span class="sxs-lookup"><span data-stu-id="9c40c-165">**Function**</span></span>
    - <span data-ttu-id="9c40c-166">**Jobbtype**</span><span class="sxs-lookup"><span data-stu-id="9c40c-166">**Job type**</span></span>
    - <span data-ttu-id="9c40c-167">**Kompensasjonsnivå**</span><span class="sxs-lookup"><span data-stu-id="9c40c-167">**Compensation level**</span></span>
    
    <span data-ttu-id="9c40c-168">Den ansatte må oppfylle alle angitte kriterier for å være kvalifisert for kompensasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="9c40c-169">Hvis du ikke angir kriterier, er alle ansatte kvalifisert for kompensasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="9c40c-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="9c40c-170">Hvis en ansatt ikke oppfyller kriteriene angitt i rettighetsregelen, eller en rettighetsregel ikke er angitt for en kompensasjonsplan, vises ikke kompensasjonsplanen i oppslaget når du oppretter en post for fast kompensasjon for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="9c40c-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="9c40c-171">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9c40c-171">Close the page.</span></span>

8. <span data-ttu-id="9c40c-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9c40c-172">Close the page.</span></span>


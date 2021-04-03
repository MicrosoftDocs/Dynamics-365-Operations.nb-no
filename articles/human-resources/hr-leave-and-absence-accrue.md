---
title: Avsett permisjons- og fraværsplaner
description: Du kan avsette permisjon og fravær i Dynamics 365 Human Resources for flere ansatte eller for en enkeltperson.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 348c8e5336854eb2a1c04a1f98a97a2c9dba7176
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464916"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="cc86a-103">Avsett permisjons- og fraværsplaner</span><span class="sxs-lookup"><span data-stu-id="cc86a-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cc86a-104">Du kan avsette permisjon og fravær i Dynamics 365 Human Resources for flere ansatte eller for en enkeltperson.</span><span class="sxs-lookup"><span data-stu-id="cc86a-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="cc86a-105">Avsette permisjon og fravær for flere ansatte</span><span class="sxs-lookup"><span data-stu-id="cc86a-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="cc86a-106">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="cc86a-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="cc86a-107">Under **Administrer permisjon** velger du **Avsett permisjons- og fraværsplaner**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="cc86a-108">Dialogboksen **Avsett permisjons- og fraværsplaner** vises.</span><span class="sxs-lookup"><span data-stu-id="cc86a-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="cc86a-109">I **Avsett per** velger du **Dagens dato**, eller du velger **Egendefinert dato** og angir en egendefinert dato.</span><span class="sxs-lookup"><span data-stu-id="cc86a-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="cc86a-110">Hvis du vil kjøre avsetninger for alle firmaer, velger du **Alle selskaper**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="cc86a-111">Hvis du vil behandle avsetninger for en enkelt permisjonsplan, velger du **Nei** for **Alle planer**, og deretter velger du en **Permisjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="cc86a-112">Hvis du velger alle firmaer, kan du ikke velge en individuell permisjonsplan.</span><span class="sxs-lookup"><span data-stu-id="cc86a-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="cc86a-113">Hvis du vil kjøre avsetningsprosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="cc86a-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="cc86a-114">Angi informasjon for avsetningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="cc86a-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="cc86a-115">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="cc86a-116">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="cc86a-117">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-117">Select **OK**.</span></span> <span data-ttu-id="cc86a-118">Avsetningsprosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="cc86a-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="cc86a-119">Avsette permisjon og fravær for en ansatt</span><span class="sxs-lookup"><span data-stu-id="cc86a-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="cc86a-120">Velg **Permisjon** i posten for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="cc86a-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="cc86a-121">Velg **Avsett permisjon og fravær**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="cc86a-122">Dialogboksen **Avsett permisjons- og fraværsplaner** vises.</span><span class="sxs-lookup"><span data-stu-id="cc86a-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="cc86a-123">I **Avsett per** velger du **Dagens dato**, eller du velger **Egendefinert dato** og angir en egendefinert dato.</span><span class="sxs-lookup"><span data-stu-id="cc86a-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="cc86a-124">Hvis du vil kjøre avsetninger for alle firmaer, velger du **Alle selskaper**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="cc86a-125">Hvis du vil behandle avsetninger for en enkelt permisjonsplan, velger du **Nei** for **Alle planer**, og deretter velger du en **Permisjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="cc86a-126">Hvis du velger alle firmaer, kan du ikke velge en individuell permisjonsplan.</span><span class="sxs-lookup"><span data-stu-id="cc86a-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="cc86a-127">Hvis du vil kjøre avsetningsprosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="cc86a-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="cc86a-128">Angi informasjon for avsetningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="cc86a-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="cc86a-129">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="cc86a-130">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="cc86a-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-131">Select **OK**.</span></span> <span data-ttu-id="cc86a-132">Avsetningsprosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="cc86a-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="cc86a-133">Slette permisjons- og fraværsavsetninger for flere ansatte</span><span class="sxs-lookup"><span data-stu-id="cc86a-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="cc86a-134">Slett avsetningsposter for en spesifikk plan og et bestemt datoområde.</span><span class="sxs-lookup"><span data-stu-id="cc86a-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="cc86a-135">Avsetningsdatoer må være datert i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="cc86a-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="cc86a-136">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="cc86a-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="cc86a-137">Under **Administrer permisjon** velger du **Slett permisjons- og fraværsplanavsetninger**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="cc86a-138">I dialogboksen **Slett permisjons- og fraværsavsetninger** velger du **Permisjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="cc86a-139">Hvis det er aktuelt , velger du **Slett saldojusteringer**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="cc86a-140">Angi eller velg en **Permisjonsavsetningsdato**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="cc86a-141">Denne datoen må være enten i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="cc86a-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="cc86a-142">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-142">Select **OK**.</span></span> <span data-ttu-id="cc86a-143">Avsetningsprosessen sletter avsetninger med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="cc86a-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="cc86a-144">Slette permisjons- og fraværsavsetninger for én ansatt</span><span class="sxs-lookup"><span data-stu-id="cc86a-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="cc86a-145">Velg **Permisjon** i posten for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="cc86a-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="cc86a-146">Velg **Slett permisjons- og fraværsplanavsetninger**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="cc86a-147">I dialogboksen **Slett permisjons- og fraværsavsetninger** velger du **Permisjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="cc86a-148">Hvis det er aktuelt , velger du **Slett saldojusteringer**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="cc86a-149">Angi eller velg en **Permisjonsavsetningsdato**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="cc86a-150">Denne datoen må være enten i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="cc86a-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="cc86a-151">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-151">Select **OK**.</span></span> <span data-ttu-id="cc86a-152">Avsetningsprosessen sletter avsetninger med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="cc86a-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="cc86a-153">Gå gjennom prosesser for permisjonsavsetning og -sletting</span><span class="sxs-lookup"><span data-stu-id="cc86a-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="cc86a-154">**Permisjonsavsetningsrevisjon** vises hver gang du kjører eller sletter en avsetning for én ansatt eller alle ansatte.</span><span class="sxs-lookup"><span data-stu-id="cc86a-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="cc86a-155">Datoen og personen som utførte handlingen, vises også.</span><span class="sxs-lookup"><span data-stu-id="cc86a-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="cc86a-156">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="cc86a-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="cc86a-157">Under **Administrer permisjon** velger du **Slett permisjonsavsetningsrevisjon**.</span><span class="sxs-lookup"><span data-stu-id="cc86a-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc86a-158">Se også</span><span class="sxs-lookup"><span data-stu-id="cc86a-158">See also</span></span>

[<span data-ttu-id="cc86a-159">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="cc86a-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="cc86a-160">Opprette en permisjons- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="cc86a-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
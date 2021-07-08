---
title: Avsett permisjons- og fraværsplaner
description: Du kan avsette permisjon og fravær i Dynamics 365 Human Resources for flere ansatte eller for en enkeltperson.
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ddd4c55f6ebfbe91fb949a92cb379f51d826c465
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303470"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="09e5d-103">Avsett permisjons- og fraværsplaner</span><span class="sxs-lookup"><span data-stu-id="09e5d-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="09e5d-104">Du kan avsette permisjon og fravær i Dynamics 365 Human Resources for flere ansatte eller for en enkeltperson.</span><span class="sxs-lookup"><span data-stu-id="09e5d-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="09e5d-105">Avsette permisjon og fravær for flere ansatte</span><span class="sxs-lookup"><span data-stu-id="09e5d-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="09e5d-106">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="09e5d-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="09e5d-107">Under **Administrer permisjon** velger du **Avsett permisjons- og fraværsplaner**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="09e5d-108">Dialogboksen **Avsett permisjons- og fraværsplaner** vises.</span><span class="sxs-lookup"><span data-stu-id="09e5d-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="09e5d-109">I **Avsett per** velger du **Dagens dato**, eller du velger **Egendefinert dato** og angir en egendefinert dato.</span><span class="sxs-lookup"><span data-stu-id="09e5d-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="09e5d-110">Hvis du vil kjøre avsetninger for alle firmaer, velger du **Alle selskaper**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="09e5d-111">Hvis du vil behandle avsetninger for en enkelt permisjonsplan, velger du **Nei** for **Alle planer**, og deretter velger du en **Permisjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="09e5d-112">Hvis du velger alle firmaer, kan du ikke velge en individuell permisjonsplan.</span><span class="sxs-lookup"><span data-stu-id="09e5d-112">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="09e5d-113">Hvis du vil kjøre avsetningsprosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="09e5d-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

    1. <span data-ttu-id="09e5d-114">Angi informasjon for avsetningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="09e5d-114">Enter information for the accrual process.</span></span>
    2. <span data-ttu-id="09e5d-115">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and then select **OK**.</span></span>
    3. <span data-ttu-id="09e5d-116">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>
    4. <span data-ttu-id="09e5d-117">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-117">Select **OK**.</span></span> <span data-ttu-id="09e5d-118">Avsetningsprosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="09e5d-118">The accrual process will run with the parameters you set.</span></span> 

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="09e5d-119">Avsette permisjon og fravær for en ansatt</span><span class="sxs-lookup"><span data-stu-id="09e5d-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="09e5d-120">Velg **Permisjon** i posten for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="09e5d-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="09e5d-121">Velg **Avsett permisjon og fravær**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="09e5d-122">Dialogboksen **Avsett permisjons- og fraværsplaner** vises.</span><span class="sxs-lookup"><span data-stu-id="09e5d-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="09e5d-123">I **Avsett per** velger du **Dagens dato**, eller du velger **Egendefinert dato** og angir en egendefinert dato.</span><span class="sxs-lookup"><span data-stu-id="09e5d-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="09e5d-124">Hvis du vil kjøre avsetninger for alle firmaer, velger du **Alle selskaper**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="09e5d-125">Hvis du vil behandle avsetninger for en enkelt permisjonsplan, velger du **Nei** for **Alle planer**, og deretter velger du en **Permisjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="09e5d-126">Hvis du velger alle firmaer, kan du ikke velge en individuell permisjonsplan.</span><span class="sxs-lookup"><span data-stu-id="09e5d-126">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="09e5d-127">Hvis du vil kjøre avsetningsprosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="09e5d-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="09e5d-128">Angi informasjon for avsetningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="09e5d-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="09e5d-129">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="09e5d-130">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="09e5d-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-131">Select **OK**.</span></span> <span data-ttu-id="09e5d-132">Avsetningsprosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="09e5d-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="09e5d-133">Slette permisjons- og fraværsavsetninger for flere ansatte</span><span class="sxs-lookup"><span data-stu-id="09e5d-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="09e5d-134">Slett avsetningsposter for en spesifikk plan og et bestemt datoområde.</span><span class="sxs-lookup"><span data-stu-id="09e5d-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="09e5d-135">Avsetningsdatoer må være datert i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="09e5d-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="09e5d-136">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="09e5d-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="09e5d-137">Under **Administrer permisjon** velger du **Slett permisjons- og fraværsplanavsetninger**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="09e5d-138">I dialogboksen **Slett permisjons- og fraværsavsetninger** velger du **Permisjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span>

4. <span data-ttu-id="09e5d-139">Hvis det er aktuelt , velger du **Slett saldojusteringer**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="09e5d-140">Angi eller velg en **Permisjonsavsetningsdato**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="09e5d-141">Denne datoen må være enten i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="09e5d-141">This date has to be either today or in the future.</span></span>

6. <span data-ttu-id="09e5d-142">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-142">Select **OK**.</span></span> <span data-ttu-id="09e5d-143">Avsetningsprosessen sletter avsetninger med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="09e5d-143">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="09e5d-144">Slette permisjons- og fraværsavsetninger for én ansatt</span><span class="sxs-lookup"><span data-stu-id="09e5d-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="09e5d-145">Velg **Permisjon** i posten for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="09e5d-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="09e5d-146">Velg **Slett permisjons- og fraværsplanavsetninger**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="09e5d-147">I dialogboksen **Slett permisjons- og fraværsavsetninger** velger du **Permisjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span>

4. <span data-ttu-id="09e5d-148">Hvis det er aktuelt , velger du **Slett saldojusteringer**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="09e5d-149">Angi eller velg en **Permisjonsavsetningsdato**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="09e5d-150">Denne datoen må være enten i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="09e5d-150">This date must be either today or in the future.</span></span>

6. <span data-ttu-id="09e5d-151">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-151">Select **OK**.</span></span> <span data-ttu-id="09e5d-152">Avsetningsprosessen sletter avsetninger med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="09e5d-152">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="09e5d-153">Gå gjennom prosesser for permisjonsavsetning og -sletting</span><span class="sxs-lookup"><span data-stu-id="09e5d-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="09e5d-154">**Permisjonsavsetningsrevisjon** vises hver gang du kjører eller sletter en avsetning for én ansatt eller alle ansatte.</span><span class="sxs-lookup"><span data-stu-id="09e5d-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="09e5d-155">Datoen og personen som utførte handlingen, vises også.</span><span class="sxs-lookup"><span data-stu-id="09e5d-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="09e5d-156">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="09e5d-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="09e5d-157">Under **Administrer permisjon** velger du **Slett permisjonsavsetningsrevisjon**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="leave-accrual-transaction-auditing"></a><span data-ttu-id="09e5d-158">Overvåking av permisjonsavsetningstransaksjon</span><span class="sxs-lookup"><span data-stu-id="09e5d-158">Leave accrual transaction auditing</span></span>

<span data-ttu-id="09e5d-159">Ved hjelp av denne funksjonen kan permisjons- og fraværsledere forstå avsetningstransaksjonene for permisjon og fravær som er knyttet til en ansatts fraværssaldoer for en bestemt permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="09e5d-159">This feature helps leave and absence managers understand the leave and absence accrual transactions related to an employee’s time off balances for a specific leave type.</span></span>

<span data-ttu-id="09e5d-160">Slik viser du transaksjonsdetaljer:</span><span class="sxs-lookup"><span data-stu-id="09e5d-160">To view transaction details:</span></span>

1. <span data-ttu-id="09e5d-161">Velg **Permisjon** i posten for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="09e5d-161">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="09e5d-162">Velg **Vis fravær**, og velg deretter kategorien **Saldoer**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-162">Select **View time off**, and then select the **Balances** tab.</span></span>

<span data-ttu-id="09e5d-163">Hvis du vil vise avsetningstransaksjonene som er knyttet til en bestemt permisjonstype, velger du den numeriske verdien i kolonnen **Gjeldende saldo**.</span><span class="sxs-lookup"><span data-stu-id="09e5d-163">To view the accrual transactions related to a specific leave type, select the numerical value in the **Current balance** column.</span></span>

<span data-ttu-id="09e5d-164">Hvis du vil vise transaksjonsdetaljene for et bestemt avsetningsbeløp, velger du en avsetningsrad, åpner **Beslektet informasjon**-panelet til høyre og åpner deretter **Transaksjonsdetaljer**-delen.</span><span class="sxs-lookup"><span data-stu-id="09e5d-164">To view the transaction details for a specific accrual amount, select an accrual row, open the **Related information** panel on the right, and then open the **Transaction details** section.</span></span> <span data-ttu-id="09e5d-165">Delen Transaksjonsdetaljer viser:</span><span class="sxs-lookup"><span data-stu-id="09e5d-165">The Transaction details section displays:</span></span>

- <span data-ttu-id="09e5d-166">Endringer i saldoen for permisjonstype for en ansatt</span><span class="sxs-lookup"><span data-stu-id="09e5d-166">Changes to the employee’s leave type balance</span></span>
- <span data-ttu-id="09e5d-167">Ansattdetaljer for den angitte avsetningsperioden</span><span class="sxs-lookup"><span data-stu-id="09e5d-167">Employment details for that specified accrual period</span></span>
- <span data-ttu-id="09e5d-168">Detaljer om avsetningsperioden og -satsene</span><span class="sxs-lookup"><span data-stu-id="09e5d-168">Details about the accrual period and rates</span></span>
- <span data-ttu-id="09e5d-169">Eventuelle endringer som er gjort for permisjonsplankonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="09e5d-169">Any changes made to leave plan configurations</span></span>

![Vise overvåking av permisjonsavsetningstransaksjon](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a><span data-ttu-id="09e5d-171">Se også</span><span class="sxs-lookup"><span data-stu-id="09e5d-171">See also</span></span>

[<span data-ttu-id="09e5d-172">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="09e5d-172">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="09e5d-173">Opprette en permisjons- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="09e5d-173">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

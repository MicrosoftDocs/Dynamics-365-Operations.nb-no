---
title: Administrere tid og fremmøte i Retail
description: Dette emnet beskriver scenarier som støttes for administrasjon av tid og fremmøte i Microsoft Dynamics 365 for Retail.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4c54909a02376a62a72a986e634649fa0ae54284
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567959"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="bfd89-103">Administrere tid og fremmøte i Retail</span><span class="sxs-lookup"><span data-stu-id="bfd89-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bfd89-104">Dette emnet beskriver scenarier som støttes for administrasjon av tid og fremmøte i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="bfd89-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="bfd89-105">Behandle konfigurasjon og planlegging for arbeider</span><span class="sxs-lookup"><span data-stu-id="bfd89-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="bfd89-106"> Opprinnelig konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="bfd89-106">Initial configuration</span></span>

- <span data-ttu-id="bfd89-107">Kjør konfigurasjonsveiviseren.</span><span class="sxs-lookup"><span data-stu-id="bfd89-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="bfd89-108">Registrer arbeidere som timeregistreringsarbeidere.</span><span class="sxs-lookup"><span data-stu-id="bfd89-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="bfd89-109">Planlegge tidsplaner for arbeidere</span><span class="sxs-lookup"><span data-stu-id="bfd89-109">Plan worker schedules</span></span>

- <span data-ttu-id="bfd89-110">Bruk profiler ved hjelp av jobbplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="bfd89-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="bfd89-111">Hvis du vil ha mer informasjon, kan du se [Bruke profiler ved hjelp av jobbplanlegger](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="bfd89-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="bfd89-112">Hvis du vil ha informasjon om konfigurasjonstrinnene, kan du se [Definere timeregistrering](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="bfd89-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="bfd89-113">Detaljhandelsspesifikk konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="bfd89-113">Retail-specific configuration</span></span>

- <span data-ttu-id="bfd89-114">Aktiver en funksjonalitetsprofil for tidsklokke, for arbeidere som du vil aktivere tidsregistreringer for.</span><span class="sxs-lookup"><span data-stu-id="bfd89-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="bfd89-115">Klikk på **Funksjonalitetsprofiler for salgssted** &gt; **Funksjoner** &gt; **Tidsregistreringer for salgssted** &gt; **Aktiver tidsregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="bfd89-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="bfd89-116">Konfigurer grupper for tillatelser for salgssted for å aktivere tillatelsen Vis tidsklokkeoppføringer.</span><span class="sxs-lookup"><span data-stu-id="bfd89-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="bfd89-117">Med denne tillatelsen kan en bruker vise tidsklokkeregistreringene for andre arbeidere i butikken (og fra alle andre butikker som brukeren er tilknyttet, via adresseboken).</span><span class="sxs-lookup"><span data-stu-id="bfd89-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="bfd89-118">Du vil kanskje aktivere denne tillatelsen for en lederrolle, men ikke en kassererrolle.</span><span class="sxs-lookup"><span data-stu-id="bfd89-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="bfd89-119">Klikk på **Salgsstedstillatelsesgrupper** &gt; **Vis tidsklokkeoppføringer**.</span><span class="sxs-lookup"><span data-stu-id="bfd89-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="bfd89-120">Kassetid</span><span class="sxs-lookup"><span data-stu-id="bfd89-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="bfd89-121">Tidsregistreringer for kasserer og ikke-kasserer</span><span class="sxs-lookup"><span data-stu-id="bfd89-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="bfd89-122">På salgssted:</span><span class="sxs-lookup"><span data-stu-id="bfd89-122">On POS:</span></span>

    - <span data-ttu-id="bfd89-123">Stemple inn operasjoner:</span><span class="sxs-lookup"><span data-stu-id="bfd89-123">Clock-in operations:</span></span>

        - <span data-ttu-id="bfd89-124">Logg på med en ikke-skuff-operasjon eller et nytt skift.</span><span class="sxs-lookup"><span data-stu-id="bfd89-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="bfd89-125">Velg en tidsklokkeoperasjon.</span><span class="sxs-lookup"><span data-stu-id="bfd89-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="bfd89-126">Velg en ønsket operasjon:</span><span class="sxs-lookup"><span data-stu-id="bfd89-126">Select a desired operation:</span></span>

            - <span data-ttu-id="bfd89-127">Innstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-127">Clock-in</span></span>
            - <span data-ttu-id="bfd89-128">Arbeidspause</span><span class="sxs-lookup"><span data-stu-id="bfd89-128">Break for Work</span></span>
            - <span data-ttu-id="bfd89-129">Lunsjpause</span><span class="sxs-lookup"><span data-stu-id="bfd89-129">Break for Lunch</span></span>
            - <span data-ttu-id="bfd89-130">Utstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="bfd89-131">Gjeldende tilstand</span><span class="sxs-lookup"><span data-stu-id="bfd89-131">Current state</span></span></th>
        <th><span data-ttu-id="bfd89-132">Tilgjengelige operasjoner</span><span class="sxs-lookup"><span data-stu-id="bfd89-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="bfd89-133">Innstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="bfd89-134">Arbeidspause</span><span class="sxs-lookup"><span data-stu-id="bfd89-134">Break for Work</span></span></li>
        <li><span data-ttu-id="bfd89-135">Lunsjpause</span><span class="sxs-lookup"><span data-stu-id="bfd89-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="bfd89-136">Utstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="bfd89-137">Arbeidspause</span><span class="sxs-lookup"><span data-stu-id="bfd89-137">Break for Work</span></span></td>
        <td><span data-ttu-id="bfd89-138">Innstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="bfd89-139">Lunsjpause</span><span class="sxs-lookup"><span data-stu-id="bfd89-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="bfd89-140">Innstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="bfd89-141">Utstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-141">Clock-out</span></span></td>
        <td><span data-ttu-id="bfd89-142">Innstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="bfd89-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="bfd89-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="bfd89-144">Vis bekreftelsesmeldingen, og valider at den gjeldende aktivitetstiden er riktig.</span><span class="sxs-lookup"><span data-stu-id="bfd89-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="bfd89-145">Loggbok:</span><span class="sxs-lookup"><span data-stu-id="bfd89-145">Logbook:</span></span>

    - <span data-ttu-id="bfd89-146">Klikk **Loggbok** for å vise tidsklokkeaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="bfd89-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="bfd89-147">Bruk tidsfiltre for å velge forskjellige tidsvinduer.</span><span class="sxs-lookup"><span data-stu-id="bfd89-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="bfd89-148">Hvis du arbeider på flere butikklokasjoner, kan du se tidsregistreringene fra alle butikkene der du har registrert tid.</span><span class="sxs-lookup"><span data-stu-id="bfd89-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="bfd89-149">Du kan bruke butikkfilteret for å vise tidsregistreringer fra en valgt butikk.</span><span class="sxs-lookup"><span data-stu-id="bfd89-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="bfd89-150">Ulike tidssoner:</span><span class="sxs-lookup"><span data-stu-id="bfd89-150">Different time zones:</span></span>

    - <span data-ttu-id="bfd89-151">Hvis du viser tiden fra en annen lokasjon (for kassererens loggbok eller ved hjelp av **Vis tidsklokkeoppføringer** for et lederscenario), og den er i en annen tidssone, blir tidspostene som du ser, konvertert til den lokale tidssonen.</span><span class="sxs-lookup"><span data-stu-id="bfd89-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="bfd89-152">Du er for eksempel en leder for to butikker, én i Arizona og den andre i Nevada.</span><span class="sxs-lookup"><span data-stu-id="bfd89-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="bfd89-153">En kasserer registrerer en innstempling klokken 9:00</span><span class="sxs-lookup"><span data-stu-id="bfd89-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="bfd89-154">i Arizona.</span><span class="sxs-lookup"><span data-stu-id="bfd89-154">in Arizona.</span></span> <span data-ttu-id="bfd89-155">På dette tidspunktet er klokken 8:00 i Nevada.</span><span class="sxs-lookup"><span data-stu-id="bfd89-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="bfd89-156">Derfor, hvis du er i butikken i Nevada og ser på timeregistreringsposter, er timeregistreringen merket som 8:00.</span><span class="sxs-lookup"><span data-stu-id="bfd89-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="bfd89-157">Vise tidsregistrering for arbeidere</span><span class="sxs-lookup"><span data-stu-id="bfd89-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="bfd89-158">Vis tidsregistreringer for arbeider, og filtrer etter butikk eller aktivitetstype</span><span class="sxs-lookup"><span data-stu-id="bfd89-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="bfd89-159">På salgssted:</span><span class="sxs-lookup"><span data-stu-id="bfd89-159">On POS:</span></span>

- <span data-ttu-id="bfd89-160">Velg **Vis tidsklokkeoppføringer**.</span><span class="sxs-lookup"><span data-stu-id="bfd89-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="bfd89-161">Du kan se aktiviteter for tidsklokkeregistrering fra alle arbeidere som er tilordnet til de samme butikkene som du er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="bfd89-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="bfd89-162">Du kan bruke aktivitetstypen og butikkfiltre for å filtrere etter tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="bfd89-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="bfd89-163">Behandle og administrere tidsregistreringer</span><span class="sxs-lookup"><span data-stu-id="bfd89-163">Process and manage time registrations</span></span>

<span data-ttu-id="bfd89-164">En Dynamics 365 for Retail-bruker følger arbeidsflyten for å beregne, godkjenne og overføre tidsregistreringer til lønn.</span><span class="sxs-lookup"><span data-stu-id="bfd89-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="bfd89-165">Primære operasjoner</span><span class="sxs-lookup"><span data-stu-id="bfd89-165">Primary operations</span></span>

- <span data-ttu-id="bfd89-166">Beregn</span><span class="sxs-lookup"><span data-stu-id="bfd89-166">Calculate</span></span>
- <span data-ttu-id="bfd89-167">Godkjenn</span><span class="sxs-lookup"><span data-stu-id="bfd89-167">Approve</span></span>
- <span data-ttu-id="bfd89-168">Send til lønn</span><span class="sxs-lookup"><span data-stu-id="bfd89-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="bfd89-169">Andre vanlige operasjoner</span><span class="sxs-lookup"><span data-stu-id="bfd89-169">Other common operations</span></span>

- <span data-ttu-id="bfd89-170">Masseutstempling</span><span class="sxs-lookup"><span data-stu-id="bfd89-170">Bulk Clock-out</span></span>
- <span data-ttu-id="bfd89-171">Registrer fravær</span><span class="sxs-lookup"><span data-stu-id="bfd89-171">Register Absence</span></span>

<span data-ttu-id="bfd89-172">Hvis du vil ha mer informasjon om hvordan du behandler registreringer av timeregistrering, kan du se [Behandle registreringer av timeregistrering](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="bfd89-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>

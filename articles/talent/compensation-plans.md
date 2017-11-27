---
title: Kompensasjonsplaner
description: "Kompensasjons- og fordelsansvarlige kan bruke kompensasjonsstyring til å vedlikeholde og behandle faste og variable kompensasjonsplaner for ansatte i organisasjonen."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 405a298ab26e343f50cb8dd80622a414695950a7
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="compensation-plans"></a><span data-ttu-id="b6d36-103">Kompensasjonsplaner</span><span class="sxs-lookup"><span data-stu-id="b6d36-103">Compensation plans</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b6d36-104">Kompensasjons- og fordelsansvarlige kan bruke kompensasjonsstyring til å vedlikeholde og behandle faste og variable kompensasjonsplaner for ansatte i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="b6d36-105">Innledning</span><span class="sxs-lookup"><span data-stu-id="b6d36-105">Introduction</span></span>

<span data-ttu-id="b6d36-106">Kompensasjonsstyring brukes til å kontrollere levering av grunnlønn og bonuser.</span><span class="sxs-lookup"><span data-stu-id="b6d36-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="b6d36-107">En ansatts faste grunnlønn og personlige tilleggsøkninger styres via faste kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="b6d36-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="b6d36-108">Betaling av insitamentutbetalinger, for eksempel bonuser, ytelsestillegg, aksjeopsjoner og tilskudd, og også engangsbonuser, kontrolleres via variable kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="b6d36-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="b6d36-109">Ansatte kan knyttes til én eller flere planer av begge typer.</span><span class="sxs-lookup"><span data-stu-id="b6d36-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="b6d36-110">En ansatt må oppfylle følgende krav for å være kvalifisert for registrering i en kompensasjonsplan:</span><span class="sxs-lookup"><span data-stu-id="b6d36-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="b6d36-111">Den ansatte må ha en aktiv stillingstilordningen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="b6d36-112">Den ansatte må overholde kriteriene som er definert av rettighetsreglene for en kompensasjonsplan.</span><span class="sxs-lookup"><span data-stu-id="b6d36-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="b6d36-113"> Kompensasjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="b6d36-113">Compensation setup</span></span>
<span data-ttu-id="b6d36-114">Tabellen nedenfor viser komponenter i kompensasjonsprosessen som kan være integrert i oppsettet av selskapets kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="b6d36-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b6d36-115">Komponent</span><span class="sxs-lookup"><span data-stu-id="b6d36-115">Component</span></span></th>
<th><span data-ttu-id="b6d36-116">Mer informasjon ...</span><span class="sxs-lookup"><span data-stu-id="b6d36-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6d36-117">Handlinger for fast kompensasjon</span><span class="sxs-lookup"><span data-stu-id="b6d36-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="b6d36-118">Faste kompensasjonshandlinger har to formål:</span><span class="sxs-lookup"><span data-stu-id="b6d36-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="b6d36-119">Handlinger kan angi hvilken type informasjon som må registreres når kompensasjonen til en ansatt endres.</span><span class="sxs-lookup"><span data-stu-id="b6d36-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="b6d36-120">Du kan for eksempel kreve at årsaken til at en endring, for eksempel en forfremmelse eller degradering, registreres.</span><span class="sxs-lookup"><span data-stu-id="b6d36-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="b6d36-121">Handlinger kan sikre at en beregning brukes når planer for fast kompensasjon er behandlet.</span><span class="sxs-lookup"><span data-stu-id="b6d36-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="b6d36-122">Eksempelvis vil handlinger av typen Egenkapital sammenligne ansattbetalingen med minste referansepunkt for nivået for den ansatte og sikre at den ansatte betales minst minimum.</span><span class="sxs-lookup"><span data-stu-id="b6d36-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee's and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d36-123">Nivåer</span><span class="sxs-lookup"><span data-stu-id="b6d36-123">Levels</span></span></td>
<td><span data-ttu-id="b6d36-124">Nivåer er tilknyttet jobber og stillinger som er relatert til en jobbreferanse.</span><span class="sxs-lookup"><span data-stu-id="b6d36-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="b6d36-125">Du kan opprette atskilte nivåer for tre typer kompensasjonsplaner: Segment, Klasse og Trinn.</span><span class="sxs-lookup"><span data-stu-id="b6d36-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d36-126">Områdeutnyttelsesmatrise</span><span class="sxs-lookup"><span data-stu-id="b6d36-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="b6d36-127">En områdeutnyttelsesmatrise hjelper deg med å overføre ansatte til kontrollpunktet for jobben.</span><span class="sxs-lookup"><span data-stu-id="b6d36-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="b6d36-128">Du kan også bruke områdeutnyttelse til å kontrollere lønnssatsens egenkapital i firmaet uten å ta hensyn til enkeltansattes ytelse eller firmaets totale ytelse.</span><span class="sxs-lookup"><span data-stu-id="b6d36-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee's performance or the overall performance of the company.</span></span> <span data-ttu-id="b6d36-129">Eksempelvis får ansatte som mottar lavere betaling i sitt område, høyere prosentøkninger enn ansatte som blir betalt høyere i området.</span><span class="sxs-lookup"><span data-stu-id="b6d36-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="b6d36-130">På denne måten kan du systematisk forskyve egenkapitalforskjeller.</span><span class="sxs-lookup"><span data-stu-id="b6d36-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="b6d36-131">Områdeutnyttelsen beregnes på følgende måte: (fast lønnssats - minimumsområde) ÷ (maksimumsområde - minimumsområde).</span><span class="sxs-lookup"><span data-stu-id="b6d36-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d36-132">Referansepunktoppsett</span><span class="sxs-lookup"><span data-stu-id="b6d36-132">Reference point setups</span></span></td>
<td><span data-ttu-id="b6d36-133">Et referansepunktoppsett inneholder et sett med referansepunkt som utgjør områder i en matrise.</span><span class="sxs-lookup"><span data-stu-id="b6d36-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="b6d36-134">Hvert område kan knyttes til en lønnssats.</span><span class="sxs-lookup"><span data-stu-id="b6d36-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="b6d36-135">Eksempelvis har segmentplaner often referansepunktene Minimum, Midtpunkt og Maksimum.</span><span class="sxs-lookup"><span data-stu-id="b6d36-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d36-136">Kompensasjonsmatrise</span><span class="sxs-lookup"><span data-stu-id="b6d36-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="b6d36-137">En kompensasjonsmatrise er et sett med referansepunkt og nivåer du bruker til å opprette en kompensasjonsstruktur.</span><span class="sxs-lookup"><span data-stu-id="b6d36-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d36-138">Kompensasjonsstruktur</span><span class="sxs-lookup"><span data-stu-id="b6d36-138">Compensation structure</span></span></td>
<td><span data-ttu-id="b6d36-139">En kompensasjonsstruktur er en kompensasjonsmatrise med lønnssatser som er knyttet til referansepunkt for hvert nivå.</span><span class="sxs-lookup"><span data-stu-id="b6d36-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d36-140">Rettighetsregler</span><span class="sxs-lookup"><span data-stu-id="b6d36-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="b6d36-141">Rettighetsregler brukes til å identifisere ansatte i bestemte jobber, jobbfunksjoner, jobbtyper, avdelinger, fagforeninger eller kompensasjonsområder som dekkes av spesifikke kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="b6d36-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="b6d36-142">Du må opprette rettighetsregler for både variable og faste kompensasjonsplaner for å registrere ansatte i planen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="b6d36-143">Når du har angitt rettighetsregler for en kompensasjonsplan, kan du definere nivåene som skal gjelde for jobbene som dekkes av planen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d36-144">Lønnsfrekvenser</span><span class="sxs-lookup"><span data-stu-id="b6d36-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="b6d36-145">Lønnsfrekvenser brukes til å definere tidsperioden som er angitt for kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="b6d36-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="b6d36-146">Eksempelvis hjelper lønnsfrekvensen deg med å forstå om kompensasjonsbeløpet er angitt som en årslønn kontra en timelønn.</span><span class="sxs-lookup"><span data-stu-id="b6d36-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="b6d36-147">Lønnsfrekvenser er også brukt til å definere omregningsfaktorer for å konvertere kompensasjonsbeløp fra frekvensen månedlig, ukentlig, lønn annenhver uke og timelønn til en årlig lønnsfrekvens.</span><span class="sxs-lookup"><span data-stu-id="b6d36-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d36-148">Kompensasjonsregioner</span><span class="sxs-lookup"><span data-stu-id="b6d36-148">Compensation regions</span></span></td>
<td><span data-ttu-id="b6d36-149">Kompensasjonsregioner brukes til å angi ansattkompensasjon på grunnlag av arbeidsstedets lokasjon.</span><span class="sxs-lookup"><span data-stu-id="b6d36-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d36-150">Kontrollpunkt</span><span class="sxs-lookup"><span data-stu-id="b6d36-150">Control point</span></span></td>
<td><span data-ttu-id="b6d36-151">Kontrollpunktet angir hva du anser som ideell lønnssats for alle ansatte på et gitt kompensasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="b6d36-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="b6d36-152">Kontrollpunkt er normalt områdenes midtpunkt for kategoriplanstrukturer.</span><span class="sxs-lookup"><span data-stu-id="b6d36-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="b6d36-153">Segmentstrukturer bruker sjelden kontrollpunkt.</span><span class="sxs-lookup"><span data-stu-id="b6d36-153">Band structures rarely use control points.</span></span> <span data-ttu-id="b6d36-154">Du kan angi kontrollpunktet for en fast kompensasjonsplan i skjemaet Faste kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="b6d36-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d36-155">Jobbfunksjoner</span><span class="sxs-lookup"><span data-stu-id="b6d36-155">Job functions</span></span></td>
<td><span data-ttu-id="b6d36-156">Jobbfunksjoner brukes til å klassifisere og filtrere kompensasjonsplaner til bestemte jobber.</span><span class="sxs-lookup"><span data-stu-id="b6d36-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d36-157">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="b6d36-157">Job types</span></span></td>
<td><span data-ttu-id="b6d36-158">Jobbtyper brukes til å klassifisere og filtrere kompensasjonsplaner til bestemte jobber.</span><span class="sxs-lookup"><span data-stu-id="b6d36-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d36-159">Typer av variabel kompensasjon</span><span class="sxs-lookup"><span data-stu-id="b6d36-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="b6d36-160">Typer av variabel kompensasjon, for eksempel aksjebelønninger eller kontantbonusbelønninger, blir brukt i variable kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="b6d36-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d36-161">Kompensasjonsrutenett</span><span class="sxs-lookup"><span data-stu-id="b6d36-161">Compensation grids</span></span></td>
<td><span data-ttu-id="b6d36-162">Kompensasjonsrutenett inneholder kompensasjonsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="b6d36-163">Kompensasjonsrutenett kan brukes av én eller flere kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="b6d36-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6d36-164">Ytelsesplaner</span><span class="sxs-lookup"><span data-stu-id="b6d36-164">Performance plans</span></span></td>
<td><span data-ttu-id="b6d36-165">Ytelsesplaner brukes til å knytte ytelse til en fordelingsmatrise slik at du kan bruke planen i en betal-for-ytelse-strategi.</span><span class="sxs-lookup"><span data-stu-id="b6d36-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6d36-166">Ytelsesvurdering</span><span class="sxs-lookup"><span data-stu-id="b6d36-166">Performance ratings</span></span></td>
<td><span data-ttu-id="b6d36-167">Ytelsesvurderinger brukes i ytelsesplaner for å fastsette belønningsbeløp i form av personlige tillegg eller ytelsestillegg.</span><span class="sxs-lookup"><span data-stu-id="b6d36-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="b6d36-168">Prosesshendelser</span><span class="sxs-lookup"><span data-stu-id="b6d36-168">Process events</span></span>
<span data-ttu-id="b6d36-169">En prosesshendelse beregner kompensasjonsinformasjon for en bestemt periode for alle ansatte som er registrert i én eller flere faste eller variable kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="b6d36-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="b6d36-170">Du kan kjøre en prosesshendelse gjentatte ganger for å teste eller oppdatere beregnede kompensasjonsresultater.</span><span class="sxs-lookup"><span data-stu-id="b6d36-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="b6d36-171">Kompensasjonshendelser</span><span class="sxs-lookup"><span data-stu-id="b6d36-171">Compensation events</span></span>
-------------------

<span data-ttu-id="b6d36-172">Hver gang en prosesshendelse kjøres, opprettes en kompensasjonshendelse.</span><span class="sxs-lookup"><span data-stu-id="b6d36-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="b6d36-173">Kompensasjonshendelser inneholder resultatene av kompensasjonsprosessen for hver ansatt som er inkludert i prosesshendelsen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="b6d36-174">Når beregningene er riktige, kan du laste inn kompensasjonshendelsen for å oppdatere kompensasjonsposter for ansatte som er berørt av prosesshendelsen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="b6d36-175"> Anbefalinger</span><span class="sxs-lookup"><span data-stu-id="b6d36-175">Recommendations</span></span>
<span data-ttu-id="b6d36-176">Når du kjører en prosesshendelse, kan du anbefale justeringer for en ansatts personlige tilleggsøkning eller bonusbeløp basert på de beregnede retningslinjeøkningene for prosesshendelsen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="b6d36-177">Hvis du gjøre anbefalinger for ansatte, må du aktivere anbefalinger når du definerer kompensasjonsplaner, eller når du definerer prosesshendelsen.</span><span class="sxs-lookup"><span data-stu-id="b6d36-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>





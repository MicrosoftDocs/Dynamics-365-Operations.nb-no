---
title: Konfigurere lønnsintegreringen mellom Talent og Dayforce
description: Dette emnet forklarer hvordan du konfigurerer integrasjonen mellom Microsoft Dynamics 365 for Talent og Ceridian Dayforce slik at du kan behandle en lønnskjøring.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518702"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="935ca-103">Konfigurere lønnsintegrering mellom Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="935ca-104">Integrasjonen mellom Microsoft Dynamics 365 for Talent og Ceridian Dayforce bruker flere konfigurasjonstrinn som er beskrevet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="935ca-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="935ca-105">Du må konfigurere integreringen i både Talent og Dayforce før du kan behandle en lønnskjøring.</span><span class="sxs-lookup"><span data-stu-id="935ca-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="935ca-106">Når du bruker en tjeneste som Dayforce til å fullføre lønnskjøringer, må du aktivere integrering i Talent.</span><span class="sxs-lookup"><span data-stu-id="935ca-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="935ca-107">Integreringen krever bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="935ca-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="935ca-108">Derfor må du kontrollere at data som tilordnes til Dayforce, er konfigurert i Talent på en måte som støtter integreringen.</span><span class="sxs-lookup"><span data-stu-id="935ca-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="935ca-109">Integrasjonen bruker følgende brede datakategorier:</span><span class="sxs-lookup"><span data-stu-id="935ca-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="935ca-110">Personaldata</span><span class="sxs-lookup"><span data-stu-id="935ca-110">Human resources data</span></span>
- <span data-ttu-id="935ca-111">Kompensasjonsdata</span><span class="sxs-lookup"><span data-stu-id="935ca-111">Compensation data</span></span>
- <span data-ttu-id="935ca-112">Lønnsdata, for eksempel lønnssykluser, lønnsperioder og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="935ca-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="935ca-113">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="935ca-113">Worker data</span></span>

<span data-ttu-id="935ca-114">Dette emnet beskriver trinnene du må følge for å aktivere integreringen.</span><span class="sxs-lookup"><span data-stu-id="935ca-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="935ca-115">Den beskriver også hvilke typer data og konfigurasjonsdetaljer som integreringen krever.</span><span class="sxs-lookup"><span data-stu-id="935ca-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="935ca-116">Aktivere integrasjonen</span><span class="sxs-lookup"><span data-stu-id="935ca-116">Enable the integration</span></span>

<span data-ttu-id="935ca-117">I Talent må du aktivere integreringen og angi konfigurasjonsinformasjonen for å koble til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="935ca-118">Hvis du vil at økonomimodultransaksjonen som produseres, skal importeres til Microsoft Dynamics 365 for Finance and Operations, må du også definere en Microsoft Azure-lagringskonto og angi Azure Storage-tilkoblingsstrengen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="935ca-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="935ca-119">Følg denne fremgangsmåten for å aktivere integrasjonen i Talent.</span><span class="sxs-lookup"><span data-stu-id="935ca-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="935ca-120">Velg **Konfigurasjon av integrering** på siden **Systemadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="935ca-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="935ca-121">Angi sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="935ca-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="935ca-122">Angi brukernavnet og passordet til brukeren som skal ha tilgang til sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="935ca-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="935ca-123">Test tilkoblingen etter behov, og sett alternativet **Aktiver lønnsintegrering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="935ca-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="935ca-124">Når integreringen er slått på, opprettes dataeksportpakken og -filene, og frekvensen angis.</span><span class="sxs-lookup"><span data-stu-id="935ca-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="935ca-125">Du kan endre denne frekvensen etter behov.</span><span class="sxs-lookup"><span data-stu-id="935ca-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="935ca-126">Hvis du vil ha mer informasjon om Azure Storage-kontoer og Azure Storage-tilkoblingsstrenger, kan du se følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="935ca-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="935ca-127">Om Azure Storage-kontoer</span><span class="sxs-lookup"><span data-stu-id="935ca-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="935ca-128">Konfigurere Azure Storage-tilkoblingsstrenger</span><span class="sxs-lookup"><span data-stu-id="935ca-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="935ca-129">Konfigurere dataene dine</span><span class="sxs-lookup"><span data-stu-id="935ca-129">Configure your data</span></span> 

<span data-ttu-id="935ca-130">For å behandle lønn må du konfigurere Personaldata i Talent.</span><span class="sxs-lookup"><span data-stu-id="935ca-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="935ca-131">Du må definere organisasjonsdata, for eksempel jobber og stillinger, samt informasjon om fordeler og kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="935ca-132">Denne informasjonen gir informasjon om ansettelse, lønn og trekk som kreves for å kunne generere lønn for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="935ca-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="935ca-133">Personaldata</span><span class="sxs-lookup"><span data-stu-id="935ca-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="935ca-134">Fordeler</span><span class="sxs-lookup"><span data-stu-id="935ca-134">Benefits</span></span> 

<span data-ttu-id="935ca-135">Personale inneholder verktøy for oppsett og vedlikehold av fordeler, fradrag og arbeiderkompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere.</span><span class="sxs-lookup"><span data-stu-id="935ca-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="935ca-136">Når du oppretter fordeler, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="935ca-137">Fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="935ca-137">Benefit plans</span></span>

- <span data-ttu-id="935ca-138">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-138">Plan (required)</span></span>
- <span data-ttu-id="935ca-139">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-139">Type (required)</span></span>
- <span data-ttu-id="935ca-140">Lønnsinnvirkning (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-140">Payroll impact (required)</span></span>
- <span data-ttu-id="935ca-141">Gjenopprett etterskudd</span><span class="sxs-lookup"><span data-stu-id="935ca-141">Recover arrears</span></span>
- <span data-ttu-id="935ca-142">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="935ca-142">Deduction method</span></span>
- <span data-ttu-id="935ca-143">Fradragsprioritet</span><span class="sxs-lookup"><span data-stu-id="935ca-143">Deduction priority</span></span>
- <span data-ttu-id="935ca-144">Begrens periode</span><span class="sxs-lookup"><span data-stu-id="935ca-144">Limit period</span></span>
- <span data-ttu-id="935ca-145">Grensebeløp</span><span class="sxs-lookup"><span data-stu-id="935ca-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="935ca-146">Fordeler</span><span class="sxs-lookup"><span data-stu-id="935ca-146">Benefits</span></span>

- <span data-ttu-id="935ca-147">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-147">Plan (required)</span></span>
- <span data-ttu-id="935ca-148">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-148">Type (required)</span></span>
- <span data-ttu-id="935ca-149">Alternativ (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-149">Option (required)</span></span>
- <span data-ttu-id="935ca-150">Fordel-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-150">Benefit ID (required)</span></span>
- <span data-ttu-id="935ca-151">Frekvens</span><span class="sxs-lookup"><span data-stu-id="935ca-151">Frequency</span></span>
- <span data-ttu-id="935ca-152">Grunnlag</span><span class="sxs-lookup"><span data-stu-id="935ca-152">Basis</span></span>
- <span data-ttu-id="935ca-153">Beløp eller sats</span><span class="sxs-lookup"><span data-stu-id="935ca-153">Amount or rate</span></span>
- <span data-ttu-id="935ca-154">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="935ca-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="935ca-155">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="935ca-155">Supported frequencies</span></span> 

- <span data-ttu-id="935ca-156">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="935ca-156">Weekly</span></span>
- <span data-ttu-id="935ca-157">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="935ca-157">Bi-weekly</span></span>
- <span data-ttu-id="935ca-158">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="935ca-158">Semi-monthly</span></span>
- <span data-ttu-id="935ca-159">Månedlig</span><span class="sxs-lookup"><span data-stu-id="935ca-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="935ca-160">Støttede grunnlag</span><span class="sxs-lookup"><span data-stu-id="935ca-160">Supported bases</span></span> 

- <span data-ttu-id="935ca-161">Fast beløp</span><span class="sxs-lookup"><span data-stu-id="935ca-161">Fixed amount</span></span>
- <span data-ttu-id="935ca-162">Prosentandel av inntekter</span><span class="sxs-lookup"><span data-stu-id="935ca-162">Percent of earnings</span></span>
- <span data-ttu-id="935ca-163">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="935ca-163">Productive hours</span></span>

<span data-ttu-id="935ca-164">Dayforce oppretter følgende fradrag, basert på lønnsinnvirkning som er definert på fordelsplanen.</span><span class="sxs-lookup"><span data-stu-id="935ca-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="935ca-165">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-165">Selection in Talent</span></span>        | <span data-ttu-id="935ca-166">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="935ca-167">None</span><span class="sxs-lookup"><span data-stu-id="935ca-167">None</span></span>                       | <span data-ttu-id="935ca-168">Ingen fradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="935ca-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="935ca-169">Bare fradrag</span><span class="sxs-lookup"><span data-stu-id="935ca-169">Deduction only</span></span>             | <span data-ttu-id="935ca-170">Et ansattfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="935ca-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="935ca-171">Bare bidrag</span><span class="sxs-lookup"><span data-stu-id="935ca-171">Contribution only</span></span>          | <span data-ttu-id="935ca-172">Et arbeidsgiverfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="935ca-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="935ca-173">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="935ca-173">Deduction and contribution</span></span> | <span data-ttu-id="935ca-174">Fradrag for ansatte og arbeidsgivere opprettes.</span><span class="sxs-lookup"><span data-stu-id="935ca-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="935ca-175">Hvis du vil ha mer informasjon om hvordan du definerer og administrerer et program for fordeler, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="935ca-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="935ca-176">Levere et program for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="935ca-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="935ca-177">Opprette en ny fordel</span><span class="sxs-lookup"><span data-stu-id="935ca-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="935ca-178">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="935ca-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="935ca-179">Registrere og fjerne fordeler fra arbeidere</span><span class="sxs-lookup"><span data-stu-id="935ca-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="935ca-180">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-180">Compensation</span></span> 

<span data-ttu-id="935ca-181">Kompensasjonsstyring brukes til å kontrollere levering av grunnlønn og bonuser.</span><span class="sxs-lookup"><span data-stu-id="935ca-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="935ca-182">En ansatts faste grunnlønn og personlige tilleggsøkninger styres via faste kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="935ca-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="935ca-183">Betaling av insitamentutbetalinger, for eksempel bonuser, ytelsestillegg, aksjeopsjoner og tilskudd, og også engangsbonuser, kontrolleres via variable kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="935ca-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="935ca-184">Dayforce bruker kompensasjonsinformasjon til å beregne timesats eller årlig sats for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="935ca-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="935ca-185">Planer for faste kompensasjoner og konverteringer av lønnssats er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="935ca-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="935ca-186">Ansatte må tilknyttes en plan for fast kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="935ca-187">Hvis du vil ha mer informasjon om kompensasjonsplaner, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="935ca-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="935ca-188">Opprette planer for fast kompensasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="935ca-189">Opprette variable kompensasjonsplaner</span><span class="sxs-lookup"><span data-stu-id="935ca-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="935ca-190">Utvikle struktur og planer for lønn/kompensasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="935ca-191">Behandle kompensasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="935ca-192">Definere kompensasjonsprosess og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="935ca-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="935ca-193">Registrere en ansatt i en fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="935ca-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="935ca-194">Registrere en ansatt i en variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="935ca-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="935ca-195">Jobber</span><span class="sxs-lookup"><span data-stu-id="935ca-195">Jobs</span></span> 

<span data-ttu-id="935ca-196">En jobb er en samling oppgaver og ansvarsområder som kreves av en person som utfører en jobb.</span><span class="sxs-lookup"><span data-stu-id="935ca-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="935ca-197">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="935ca-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="935ca-198">Definere komponentene for en jobb</span><span class="sxs-lookup"><span data-stu-id="935ca-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="935ca-199">Definere nye jobber</span><span class="sxs-lookup"><span data-stu-id="935ca-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="935ca-200">Stillinger</span><span class="sxs-lookup"><span data-stu-id="935ca-200">Positions</span></span>

<span data-ttu-id="935ca-201">En stilling er én enkeltforekomst av en jobb.</span><span class="sxs-lookup"><span data-stu-id="935ca-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="935ca-202">"Salgssjef (øst)"-stillingen er for eksempel én av stillingene som er knyttet til jobben "Salgssjef".</span><span class="sxs-lookup"><span data-stu-id="935ca-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="935ca-203">Det finnes en stilling i en avdeling.</span><span class="sxs-lookup"><span data-stu-id="935ca-203">A position exists in a department.</span></span> <span data-ttu-id="935ca-204">Bare én arbeider kan være tilknyttet hvert område.</span><span class="sxs-lookup"><span data-stu-id="935ca-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="935ca-205">Ha følgende data og konfigurasjon i bakhodet når du definerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="935ca-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="935ca-206">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-206">Position (required)</span></span>
- <span data-ttu-id="935ca-207">Beskrivelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-207">Description (required)</span></span>
- <span data-ttu-id="935ca-208">Jobb (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-208">Job (required)</span></span>
- <span data-ttu-id="935ca-209">Avdeling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-209">Department (required)</span></span>
- <span data-ttu-id="935ca-210">Stillingstype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-210">Position type (required)</span></span>
- <span data-ttu-id="935ca-211">Fulltidsekvivalent</span><span class="sxs-lookup"><span data-stu-id="935ca-211">Full-time equivalent</span></span>
- <span data-ttu-id="935ca-212">Årlige vanlige timer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="935ca-213">Betalt av juridisk enhet (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="935ca-214">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-214">Pay cycle (required)</span></span>
- <span data-ttu-id="935ca-215">Standard finansdimensjon – kostsenter (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="935ca-216">Arbeidertilordning – arbeider, start for tilordning, slutt for tilordning, årsakskode</span><span class="sxs-lookup"><span data-stu-id="935ca-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="935ca-217">Hvis flere stillinger i samme avdeling er knyttet til den samme jobben, konsolideres de til én stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="935ca-218">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="935ca-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="935ca-219">Organisere arbeidsstyrken ved bruk av avdelinger, jobber og stillinger</span><span class="sxs-lookup"><span data-stu-id="935ca-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="935ca-220">Definere stillinger</span><span class="sxs-lookup"><span data-stu-id="935ca-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="935ca-221">Avdelinger</span><span class="sxs-lookup"><span data-stu-id="935ca-221">Departments</span></span>

<span data-ttu-id="935ca-222">En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="935ca-223">En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale.</span><span class="sxs-lookup"><span data-stu-id="935ca-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="935ca-224">Du kan bruke avdelinger til å rapportere om funksjonsområder.</span><span class="sxs-lookup"><span data-stu-id="935ca-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="935ca-225">Avdelinger kan ha ansvar for fortjeneste og tap.</span><span class="sxs-lookup"><span data-stu-id="935ca-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="935ca-226">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="935ca-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="935ca-227">Opprette en avdeling og knytte den til avdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="935ca-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="935ca-228">Definere nye avdelinger</span><span class="sxs-lookup"><span data-stu-id="935ca-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="935ca-229">Lønnssykluser og lønnsperioder</span><span class="sxs-lookup"><span data-stu-id="935ca-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="935ca-230">En betalingssyklus avgjør hvor ofte lønnskjøring utføres, og de spesifikke dagene arbeidere lønnes.</span><span class="sxs-lookup"><span data-stu-id="935ca-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="935ca-231">For eksempel kan en lønnssyklus være månedlig, og ansatte kan betales på den siste dagen i måneden.</span><span class="sxs-lookup"><span data-stu-id="935ca-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="935ca-232">En lønnssyklus kan også være ukentlig, og ansatte kan betales tirsdagen etter slutten av lønnsperioden.</span><span class="sxs-lookup"><span data-stu-id="935ca-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="935ca-233">Lønnssykluser tilordnes til stillinger for å styre når arbeidere i disse stillingene lønnes.</span><span class="sxs-lookup"><span data-stu-id="935ca-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="935ca-234">Når du oppretter lønnssykler, kan du generere lønnsperioder for hver enkelt syklus.</span><span class="sxs-lookup"><span data-stu-id="935ca-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="935ca-235">Hver lønnsperiode inkluderer en standard betalingsdato som er basert på informasjonen du angir.</span><span class="sxs-lookup"><span data-stu-id="935ca-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="935ca-236">Du kan imidlertid endre standard betalingsdato i en lønnsperiode for å tillate unntak, for eksempel når betalingsdatoen faller på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="935ca-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="935ca-237">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="935ca-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="935ca-238">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-238">Pay cycle (required)</span></span>
- <span data-ttu-id="935ca-239">Lønnssyklusfrekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="935ca-240">Periodens startdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="935ca-241">Standard betalingsdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="935ca-242">Denne informasjonen er integrert med Dayforce som lønnsgrupper og er inndelt etter land eller område for hver lønnssyklus.</span><span class="sxs-lookup"><span data-stu-id="935ca-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="935ca-243">Minst én lønnsperiode må genereres før integrasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="935ca-244">Dayforce genererer lønnsgruppekalendere og betalingsdatoer basert på startdatoen for den første lønnsperioden og standard betalingsdato som er definert i Talent.</span><span class="sxs-lookup"><span data-stu-id="935ca-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="935ca-245">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="935ca-245">Earning codes</span></span>

<span data-ttu-id="935ca-246">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="935ca-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="935ca-247">Kodene har forskjellige parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="935ca-248">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="935ca-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="935ca-249">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-249">Earning Code (required)</span></span>
- <span data-ttu-id="935ca-250">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="935ca-250">Description</span></span>
- <span data-ttu-id="935ca-251">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="935ca-251">Unit of measure</span></span>
- <span data-ttu-id="935ca-252">Produktiv</span><span class="sxs-lookup"><span data-stu-id="935ca-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="935ca-253">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="935ca-253">Worker data</span></span>

<span data-ttu-id="935ca-254">Poster for ulike typer arbeidere som du har, er viktig for personal. og lønnsystemene dine.</span><span class="sxs-lookup"><span data-stu-id="935ca-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="935ca-255">Informasjonen du legger inn, kan brukes til å spore arbeidere og personlig informasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="935ca-256">Du kan vedlikeholde følgende informasjon om arbeidere:</span><span class="sxs-lookup"><span data-stu-id="935ca-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="935ca-257">**Grunnleggende** – Vedlikehold grunnleggende informasjon om en arbeider, for eksempel kontaktinformasjon, demografisk informasjon, identifikasjonsinformasjon, familieinformasjon, militærtjenestestatus, informasjon om personer som bor i utlandet, og personlige kontakter og kontakter i nødfall.</span><span class="sxs-lookup"><span data-stu-id="935ca-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="935ca-258">**Ansettelse** – Vedlikehold informasjon om en arbeiders ansettelse, for eksempel informasjon om firma- eller organisasjonstilknytning, stillingstilordning, start- og sluttdatoer, arbeidstillatelse, vilkår for ansettelse, pensjon, ferie og flytting.</span><span class="sxs-lookup"><span data-stu-id="935ca-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="935ca-259">**Lønn og fravær** – Vedlikehold opplysninger om en arbeiders fravær, for eksempel arbeidskalendere, fraværstransaksjoner og fraværsoppsett.</span><span class="sxs-lookup"><span data-stu-id="935ca-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="935ca-260">**Kompensasjon og lønn** – Vedlikehold informasjon om en arbeiders kompensasjonsplaner og lønn, for eksempel planregistrering, priser, ytelse, provisjon, avgiftsinformasjon, pensjonering og lønnstrekk.</span><span class="sxs-lookup"><span data-stu-id="935ca-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="935ca-261">Når du legger inn arbeiderinformasjon, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="935ca-262">Generell informasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-262">General information</span></span>

- <span data-ttu-id="935ca-263">Personalnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-263">Personnel number (required)</span></span>
- <span data-ttu-id="935ca-264">Fornavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-264">First name (required)</span></span>
- <span data-ttu-id="935ca-265">Etternavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-265">Last name (required)</span></span>
- <span data-ttu-id="935ca-266">Mellomnavn</span><span class="sxs-lookup"><span data-stu-id="935ca-266">Middle name</span></span>
- <span data-ttu-id="935ca-267">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="935ca-267">Seniority date</span></span>
- <span data-ttu-id="935ca-268">Kalt</span><span class="sxs-lookup"><span data-stu-id="935ca-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="935ca-269">Personlige opplysninger</span><span class="sxs-lookup"><span data-stu-id="935ca-269">Personal information</span></span>

- <span data-ttu-id="935ca-270">Sivilstand (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-270">Marital status (required)</span></span>
- <span data-ttu-id="935ca-271">Fødselsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-271">Birth date (required)</span></span>
- <span data-ttu-id="935ca-272">Kjønn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-272">Gender (required)</span></span>
- <span data-ttu-id="935ca-273">Person med funksjonshemminger</span><span class="sxs-lookup"><span data-stu-id="935ca-273">Person with disabilities</span></span>
- <span data-ttu-id="935ca-274">Nasjonalitet land/område (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="935ca-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="935ca-275">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="935ca-275">Address information</span></span>

- <span data-ttu-id="935ca-276">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-276">Primary (required)</span></span>
- <span data-ttu-id="935ca-277">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-277">Country/region (required)</span></span>
- <span data-ttu-id="935ca-278">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-278">Postal code (required)</span></span>
- <span data-ttu-id="935ca-279">Gatenummer (obligatorisk) (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="935ca-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="935ca-280">Bygningsnavn (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="935ca-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="935ca-281">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-281">City (required)</span></span>
- <span data-ttu-id="935ca-282">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-282">State (required)</span></span>
- <span data-ttu-id="935ca-283">Land (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="935ca-284">Kontaktinformasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-284">Contact information</span></span> 

- <span data-ttu-id="935ca-285">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-285">Primary (required)</span></span>
- <span data-ttu-id="935ca-286">Kontaktnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-286">Contact number (required)</span></span>
- <span data-ttu-id="935ca-287">Utvidelse</span><span class="sxs-lookup"><span data-stu-id="935ca-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="935ca-288">Lønnsinformasjon og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="935ca-288">Payroll information and earning codes</span></span>

<span data-ttu-id="935ca-289">Ansatte kan tilordnes spesifikke inntekter med en gitt betalingfrekvens og med en foretrukket betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="935ca-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="935ca-290">Følgende felt brukes i Dayforce for å sørge for at disse valgene og innstillingene brukes.</span><span class="sxs-lookup"><span data-stu-id="935ca-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="935ca-291">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="935ca-291">Earning codes</span></span>

- <span data-ttu-id="935ca-292">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-292">Position (required)</span></span>
- <span data-ttu-id="935ca-293">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-293">Earning Code (required)</span></span>
- <span data-ttu-id="935ca-294">Frekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-294">Frequency (required)</span></span>
- <span data-ttu-id="935ca-295">Beløp (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="935ca-296">Lønnsinformasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-296">Payroll information</span></span>

- <span data-ttu-id="935ca-297">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="935ca-297">Payment Method</span></span>
- <span data-ttu-id="935ca-298">Økonomisk område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-298">Economic Region (required)</span></span>
- <span data-ttu-id="935ca-299">ID for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="935ca-299">Employee Benefits ID</span></span>
- <span data-ttu-id="935ca-300">Nasjonalt ID-nummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-300">National ID Number (required)</span></span>
- <span data-ttu-id="935ca-301">Militærtjenestenummer</span><span class="sxs-lookup"><span data-stu-id="935ca-301">Military Service Number</span></span>
- <span data-ttu-id="935ca-302">Skift-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-302">Shift ID (required)</span></span>
- <span data-ttu-id="935ca-303">Avgiftsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-303">Tax Number (required)</span></span>
- <span data-ttu-id="935ca-304">Fagforenings-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-304">Union ID (required)</span></span>
- <span data-ttu-id="935ca-305">Arbeidsdag-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-305">Work Day ID (required)</span></span>
- <span data-ttu-id="935ca-306">Arbeidstillatelsesnummer</span><span class="sxs-lookup"><span data-stu-id="935ca-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="935ca-307">Når det gjelder betalingsmåte støtter Mexico **Kontanter**, **Sjekk** (firmaets fysisk sjekk) og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="935ca-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="935ca-308">Hvis betalingsmåte ikke er angitt, brukes **Sjekk** som standard.</span><span class="sxs-lookup"><span data-stu-id="935ca-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="935ca-309">Ansettelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="935ca-309">Employment details</span></span>

<span data-ttu-id="935ca-310">Ansettelsesdetaljhistorikk brukes som nøkkelinformasjon til å avlede en ansatts ansettelse-, oppsigelses- og nyansettelsesstatuser i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="935ca-311">Dayforce støtter bare én aktiv ansettelsespost om gangen.</span><span class="sxs-lookup"><span data-stu-id="935ca-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="935ca-312">Startdato for ansettelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-312">Employment start date (required)</span></span>
- <span data-ttu-id="935ca-313">Sluttdato for ansettelse</span><span class="sxs-lookup"><span data-stu-id="935ca-313">Employment end date</span></span>
- <span data-ttu-id="935ca-314">Startdato</span><span class="sxs-lookup"><span data-stu-id="935ca-314">Start date</span></span>
- <span data-ttu-id="935ca-315">Justert startdato</span><span class="sxs-lookup"><span data-stu-id="935ca-315">Adjusted start date</span></span>
- <span data-ttu-id="935ca-316">Avslutningsdato (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="935ca-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="935ca-317">Avslutningsårsak (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="935ca-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="935ca-318">En ansatts nøkkeldatoer avledes ved å bruke følgende informasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="935ca-319">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-319">Talent</span></span>                | <span data-ttu-id="935ca-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935ca-321">Den siste ansettelsesdatoen</span><span class="sxs-lookup"><span data-stu-id="935ca-321">Most recent hire date</span></span> | <span data-ttu-id="935ca-322">Ansettelsesstart for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="935ca-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="935ca-323">Avslutningsdato</span><span class="sxs-lookup"><span data-stu-id="935ca-323">Termination date</span></span>      | <span data-ttu-id="935ca-324">Avslutningsdato for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="935ca-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="935ca-325">Startdato</span><span class="sxs-lookup"><span data-stu-id="935ca-325">Start date</span></span>            | <span data-ttu-id="935ca-326">Justert startdato, startdato eller ansettelsesstart for gjeldende ikke-aktive ansettelseloggpost</span><span class="sxs-lookup"><span data-stu-id="935ca-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="935ca-327">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="935ca-327">Original hire date</span></span>    | <span data-ttu-id="935ca-328">Ansettelsesstart for tidligste ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="935ca-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="935ca-329">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-329">Compensation</span></span>

<span data-ttu-id="935ca-330">En fast kompensasjonsplan må være knyttet til hver ansatts primære stilling i en ansattperiode.</span><span class="sxs-lookup"><span data-stu-id="935ca-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="935ca-331">Denne perioden begynner på datoen da den ansatte ble ansatt (eller startdatoen for ansettelsen), og fortsetter til avslutning.</span><span class="sxs-lookup"><span data-stu-id="935ca-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="935ca-332">Gyldighetsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-332">Effective Date (required)</span></span>
- <span data-ttu-id="935ca-333">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="935ca-333">Expiration date</span></span>
- <span data-ttu-id="935ca-334">Lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-334">Pay Rate (required)</span></span>
- <span data-ttu-id="935ca-335">Konverteringer av lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="935ca-336">Tilsvarende årlig (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="935ca-337">Tilsvarende per time (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="935ca-338">Hvis en timebaserte ansatt har flere stillinger, importeres fast kompensasjon for den primære stillingen til Dayforce som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="935ca-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="935ca-339">For ikke-primære stillinger lagres timeprisen til den tilsvarende stillingen i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="935ca-340">Hvis en lønnsansatt har flere stillinger, avledes kumulativ timepris og årslønn på tvers av alle aktive stillinger og brukes som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="935ca-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="935ca-341">Identifikasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="935ca-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="935ca-342">Personnummeridentifikator</span><span class="sxs-lookup"><span data-stu-id="935ca-342">Social Security identifier</span></span> 

<span data-ttu-id="935ca-343">Alle ansatte må ha én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="935ca-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="935ca-344">Identifikatoren må være av identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="935ca-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="935ca-345">I Dayforce hentes den automatisk som den ansattes personnummeridentifikator som kreves for ansettelse.</span><span class="sxs-lookup"><span data-stu-id="935ca-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="935ca-346">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-346">Primary (required)</span></span>
- <span data-ttu-id="935ca-347">Identifikasjonstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="935ca-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="935ca-348">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="935ca-348">Issued Date</span></span>
- <span data-ttu-id="935ca-349">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="935ca-349">Expiration Date</span></span>

<span data-ttu-id="935ca-350">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="935ca-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="935ca-351">Det er imidlertid bare posten som er merket som **Primær**, som er integrert i Dayforce, uansett om nummeret er aktivt eller utløpt.</span><span class="sxs-lookup"><span data-stu-id="935ca-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="935ca-352">Bankkontoer og -utlegg</span><span class="sxs-lookup"><span data-stu-id="935ca-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="935ca-353">Gyldig bankkontoinformasjon må angis for alle ansatte som velger å betales via bankkontooverføringer.</span><span class="sxs-lookup"><span data-stu-id="935ca-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="935ca-354">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-354">Talent</span></span>                         | <span data-ttu-id="935ca-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935ca-356">Bankkontonummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="935ca-357">SWIFT-kode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-357">SWIFT code (required)</span></span>          | <span data-ttu-id="935ca-358">**Bank-ID**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="935ca-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="935ca-359">Avdelingsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="935ca-360">Bankkontotype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-360">Bank account type (required)</span></span>   | <span data-ttu-id="935ca-361">**Kontotoype**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="935ca-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="935ca-362">Støttede verdier inkluderer **Kontroll** og **Lønn**.</span><span class="sxs-lookup"><span data-stu-id="935ca-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="935ca-363">Ansatte som velger å betales via bankkontooverføringer, må oppgi en kobling til en restkonto som er under en juridisk enhet som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en meksikansk bank.</span><span class="sxs-lookup"><span data-stu-id="935ca-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="935ca-364">Alle andre ikke-restkontoer ignoreres.</span><span class="sxs-lookup"><span data-stu-id="935ca-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="935ca-365">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="935ca-365">Address information</span></span>

<span data-ttu-id="935ca-366">Alle ansatte må ha ett primært sted.</span><span class="sxs-lookup"><span data-stu-id="935ca-366">Every employee must have one primary location.</span></span> <span data-ttu-id="935ca-367">I Dayforce brukes dette stedet til å fastslå den ansattes primære bosted for skatte- og avgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="935ca-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="935ca-368">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-368">Primary (required)</span></span>
- <span data-ttu-id="935ca-369">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-369">Country/region (required)</span></span>
- <span data-ttu-id="935ca-370">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="935ca-371">Gate (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-371">Street (required)</span></span>
- <span data-ttu-id="935ca-372">Gatenummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-372">Street Number (required)</span></span>
- <span data-ttu-id="935ca-373">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="935ca-373">Building Complement</span></span>
- <span data-ttu-id="935ca-374">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-374">City (required)</span></span>
- <span data-ttu-id="935ca-375">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-375">State (required)</span></span>
- <span data-ttu-id="935ca-376">Land (oblitagorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="935ca-377">Konfigurer dataene for å generere lønn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="935ca-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="935ca-378">Hvis du skal generere lønn for ansatte i USA og Canada, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="935ca-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="935ca-379">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="935ca-379">Departments are required on positions.</span></span>
- <span data-ttu-id="935ca-380">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="935ca-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="935ca-381">Du kan konfigurere Talent slik at det kreves at stillinger spesifiserer en avdeling.</span><span class="sxs-lookup"><span data-stu-id="935ca-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="935ca-382">For å gjøre dette går du til **HR delte stillinger > Stillinger > Avdelinger må oppgis for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="935ca-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="935ca-383">Vi anbefaler at denne innstillingen iverksettes for integreringen.</span><span class="sxs-lookup"><span data-stu-id="935ca-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="935ca-384">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="935ca-384">Job types</span></span>

<span data-ttu-id="935ca-385">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="935ca-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="935ca-386">Jobbtyper kreves for å kunne behandle lønn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="935ca-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="935ca-387">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="935ca-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="935ca-388">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="935ca-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="935ca-389">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="935ca-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="935ca-390">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="935ca-390">Job type</span></span>   | <span data-ttu-id="935ca-391">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="935ca-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="935ca-392">Per time</span><span class="sxs-lookup"><span data-stu-id="935ca-392">Hourly</span></span>     | <span data-ttu-id="935ca-393">Per time</span><span class="sxs-lookup"><span data-stu-id="935ca-393">Hourly</span></span>      |
| <span data-ttu-id="935ca-394">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="935ca-394">Salaried</span></span>   | <span data-ttu-id="935ca-395">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="935ca-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="935ca-396">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="935ca-396">Position types</span></span> 

<span data-ttu-id="935ca-397">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="935ca-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="935ca-398">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="935ca-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="935ca-399">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="935ca-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="935ca-400">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="935ca-400">Position type</span></span>   | <span data-ttu-id="935ca-401">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="935ca-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="935ca-402">Heltid</span><span class="sxs-lookup"><span data-stu-id="935ca-402">Full-time</span></span>       | <span data-ttu-id="935ca-403">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="935ca-403">Full time employee</span></span> |
| <span data-ttu-id="935ca-404">Deltid</span><span class="sxs-lookup"><span data-stu-id="935ca-404">Part-time</span></span>       | <span data-ttu-id="935ca-405">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="935ca-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="935ca-406">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="935ca-406">Reason codes</span></span>

<span data-ttu-id="935ca-407">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="935ca-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="935ca-408">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="935ca-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="935ca-409">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="935ca-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="935ca-410">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="935ca-410">Reason code</span></span>    | <span data-ttu-id="935ca-411">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="935ca-411">Description</span></span>      | <span data-ttu-id="935ca-412">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="935ca-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="935ca-413">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="935ca-413">RESIGNATION</span></span>    | <span data-ttu-id="935ca-414">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="935ca-414">Resignation</span></span>      | <span data-ttu-id="935ca-415">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-415">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-416">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="935ca-416">TERMINATION</span></span>    | <span data-ttu-id="935ca-417">Avslutning</span><span class="sxs-lookup"><span data-stu-id="935ca-417">Termination</span></span>      | <span data-ttu-id="935ca-418">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-418">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-419">AVGANG VED PENSJON</span><span class="sxs-lookup"><span data-stu-id="935ca-419">RETIREMENT</span></span>     | <span data-ttu-id="935ca-420">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="935ca-420">Retirement</span></span>       | <span data-ttu-id="935ca-421">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-421">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-422">ANNET</span><span class="sxs-lookup"><span data-stu-id="935ca-422">OTHER</span></span>          | <span data-ttu-id="935ca-423">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="935ca-423">Other Reasons</span></span>    | <span data-ttu-id="935ca-424">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-424">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-425">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="935ca-425">DEATH</span></span>          | <span data-ttu-id="935ca-426">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="935ca-426">Death</span></span>            | <span data-ttu-id="935ca-427">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-427">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-428">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="935ca-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="935ca-429">Permisjon</span><span class="sxs-lookup"><span data-stu-id="935ca-429">Leave of Absence</span></span> | <span data-ttu-id="935ca-430">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-430">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-431">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="935ca-431">CONTRACTEND</span></span>    | <span data-ttu-id="935ca-432">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="935ca-432">End of Contract</span></span>  | <span data-ttu-id="935ca-433">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-433">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-434">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="935ca-434">SALARYCHANGE</span></span>   | <span data-ttu-id="935ca-435">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="935ca-435">Change of Salary</span></span> | <span data-ttu-id="935ca-436">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="935ca-437">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="935ca-437">Marital status</span></span>

<span data-ttu-id="935ca-438">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="935ca-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="935ca-439">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="935ca-440">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-440">Talent</span></span>                 | <span data-ttu-id="935ca-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="935ca-442">Gift</span><span class="sxs-lookup"><span data-stu-id="935ca-442">Married</span></span>                | <span data-ttu-id="935ca-443">Gift</span><span class="sxs-lookup"><span data-stu-id="935ca-443">Married</span></span>              |
| <span data-ttu-id="935ca-444">Én</span><span class="sxs-lookup"><span data-stu-id="935ca-444">Single</span></span>                 | <span data-ttu-id="935ca-445">Én</span><span class="sxs-lookup"><span data-stu-id="935ca-445">Single</span></span>               |
| <span data-ttu-id="935ca-446">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="935ca-446">Widowed</span></span>                | <span data-ttu-id="935ca-447">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="935ca-447">Widowed</span></span>              |
| <span data-ttu-id="935ca-448">Skilt</span><span class="sxs-lookup"><span data-stu-id="935ca-448">Divorced</span></span>               | <span data-ttu-id="935ca-449">Skilt</span><span class="sxs-lookup"><span data-stu-id="935ca-449">Divorced</span></span>             |
| <span data-ttu-id="935ca-450">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="935ca-450">Registered Partnership</span></span> | <span data-ttu-id="935ca-451">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="935ca-451">Domestic Partnership</span></span> |
| <span data-ttu-id="935ca-452">None</span><span class="sxs-lookup"><span data-stu-id="935ca-452">None</span></span>                   | <span data-ttu-id="935ca-453">None</span><span class="sxs-lookup"><span data-stu-id="935ca-453">None</span></span>                 |
| <span data-ttu-id="935ca-454">Samboer</span><span class="sxs-lookup"><span data-stu-id="935ca-454">Cohabiting</span></span>             | <span data-ttu-id="935ca-455">Samboer</span><span class="sxs-lookup"><span data-stu-id="935ca-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="935ca-456">Kjønn</span><span class="sxs-lookup"><span data-stu-id="935ca-456">Gender</span></span>

<span data-ttu-id="935ca-457">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="935ca-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="935ca-458">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="935ca-459">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-459">Talent</span></span>       | <span data-ttu-id="935ca-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="935ca-461">Mann</span><span class="sxs-lookup"><span data-stu-id="935ca-461">Male</span></span>         | <span data-ttu-id="935ca-462">Mann</span><span class="sxs-lookup"><span data-stu-id="935ca-462">Male</span></span>            |
| <span data-ttu-id="935ca-463">Kvinne</span><span class="sxs-lookup"><span data-stu-id="935ca-463">Female</span></span>       | <span data-ttu-id="935ca-464">Kvinne</span><span class="sxs-lookup"><span data-stu-id="935ca-464">Female</span></span>          |
| <span data-ttu-id="935ca-465">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="935ca-465">Non-specific</span></span> | <span data-ttu-id="935ca-466">*Støttes ikke*</span><span class="sxs-lookup"><span data-stu-id="935ca-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="935ca-467">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="935ca-467">Earning codes</span></span>

<span data-ttu-id="935ca-468">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="935ca-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="935ca-469">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="935ca-470">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="935ca-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="935ca-471">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="935ca-471">Supported frequencies</span></span>

- <span data-ttu-id="935ca-472">Alle</span><span class="sxs-lookup"><span data-stu-id="935ca-472">All</span></span>
- <span data-ttu-id="935ca-473">HVERBET</span><span class="sxs-lookup"><span data-stu-id="935ca-473">EVERYPAY</span></span>
- <span data-ttu-id="935ca-474">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="935ca-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="935ca-475">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="935ca-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="935ca-476">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="935ca-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="935ca-477">1IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-477">1OFMTH</span></span>
- <span data-ttu-id="935ca-478">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="935ca-478">LASTOFMTH</span></span>
- <span data-ttu-id="935ca-479">2IMDN</span><span class="sxs-lookup"><span data-stu-id="935ca-479">2OFMTH</span></span>
- <span data-ttu-id="935ca-480">3IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-480">3OFMTH</span></span>
- <span data-ttu-id="935ca-481">4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-481">4OFMTH</span></span>
- <span data-ttu-id="935ca-482">5IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-482">5OFMTH</span></span>
- <span data-ttu-id="935ca-483">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-483">1N2OFMTH</span></span>
- <span data-ttu-id="935ca-484">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-484">3N4OFMTH</span></span>
- <span data-ttu-id="935ca-485">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-485">1N3OFMTH</span></span>
- <span data-ttu-id="935ca-486">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-486">1N4OFMTH</span></span>
- <span data-ttu-id="935ca-487">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-487">2N3OFMTH</span></span>
- <span data-ttu-id="935ca-488">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-488">2N4OFMTH</span></span>
- <span data-ttu-id="935ca-489">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="935ca-490">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="935ca-491">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="935ca-492">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="935ca-493">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="935ca-494">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="935ca-495">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="935ca-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="935ca-496">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="935ca-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="935ca-497">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="935ca-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="935ca-498">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="935ca-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="935ca-499">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="935ca-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="935ca-500">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="935ca-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="935ca-501">Adresser</span><span class="sxs-lookup"><span data-stu-id="935ca-501">Addresses</span></span>

<span data-ttu-id="935ca-502">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="935ca-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="935ca-503">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="935ca-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="935ca-504">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-504">Talent</span></span>          | <span data-ttu-id="935ca-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="935ca-506">Land/område</span><span class="sxs-lookup"><span data-stu-id="935ca-506">Country/Region</span></span>  | <span data-ttu-id="935ca-507">Landskode</span><span class="sxs-lookup"><span data-stu-id="935ca-507">Country Code</span></span>          |
| <span data-ttu-id="935ca-508">Postnummer</span><span class="sxs-lookup"><span data-stu-id="935ca-508">Zip/Postal Code</span></span> | <span data-ttu-id="935ca-509">Postnummer</span><span class="sxs-lookup"><span data-stu-id="935ca-509">Postal Code</span></span>           |
| <span data-ttu-id="935ca-510">Delstat</span><span class="sxs-lookup"><span data-stu-id="935ca-510">State</span></span>           | <span data-ttu-id="935ca-511">Statskode</span><span class="sxs-lookup"><span data-stu-id="935ca-511">State Code</span></span>            |
| <span data-ttu-id="935ca-512">By</span><span class="sxs-lookup"><span data-stu-id="935ca-512">City</span></span>            | <span data-ttu-id="935ca-513">By</span><span class="sxs-lookup"><span data-stu-id="935ca-513">City</span></span>                  |
| <span data-ttu-id="935ca-514">Kommune</span><span class="sxs-lookup"><span data-stu-id="935ca-514">County</span></span>          | <span data-ttu-id="935ca-515">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="935ca-515">County (Municipality)</span></span> |
| <span data-ttu-id="935ca-516">Gate</span><span class="sxs-lookup"><span data-stu-id="935ca-516">Street</span></span>          | <span data-ttu-id="935ca-517">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="935ca-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="935ca-518">Avgiftsområder</span><span class="sxs-lookup"><span data-stu-id="935ca-518">Tax regions</span></span>

<span data-ttu-id="935ca-519">Avgiftsområder brukes til å bestemme den gjeldende avgiften som skal brukes ved generering av lønn.</span><span class="sxs-lookup"><span data-stu-id="935ca-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="935ca-520">Avgiftsområder er tilordnet Dayforce som stedsadresser.</span><span class="sxs-lookup"><span data-stu-id="935ca-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="935ca-521">Standard avgiftområde må være knyttet til arbeiderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="935ca-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="935ca-522">Avgiftsområde (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-522">Tax region (required)</span></span>
- <span data-ttu-id="935ca-523">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-523">Country/Region (required)</span></span>
- <span data-ttu-id="935ca-524">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-524">State (required)</span></span>
- <span data-ttu-id="935ca-525">Kommune</span><span class="sxs-lookup"><span data-stu-id="935ca-525">County</span></span> 
- <span data-ttu-id="935ca-526">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="935ca-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="935ca-527">Konfigurere data for å generere lønn i Mexico</span><span class="sxs-lookup"><span data-stu-id="935ca-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="935ca-528">Hvis du skal generere lønn for ansatte i Mexico, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="935ca-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="935ca-529">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="935ca-529">Departments are required on positions.</span></span>
- <span data-ttu-id="935ca-530">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="935ca-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="935ca-531">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="935ca-531">Job types</span></span>

<span data-ttu-id="935ca-532">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="935ca-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="935ca-533">Jobbtype kreves for å kunne behandle lønn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="935ca-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="935ca-534">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="935ca-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="935ca-535">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="935ca-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="935ca-536">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="935ca-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="935ca-537">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="935ca-537">Job type</span></span>   | <span data-ttu-id="935ca-538">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="935ca-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="935ca-539">Per time</span><span class="sxs-lookup"><span data-stu-id="935ca-539">Hourly</span></span>     | <span data-ttu-id="935ca-540">MX per time</span><span class="sxs-lookup"><span data-stu-id="935ca-540">MX Hourly</span></span>   |
| <span data-ttu-id="935ca-541">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="935ca-541">Salaried</span></span>   | <span data-ttu-id="935ca-542">MX lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="935ca-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="935ca-543">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="935ca-543">Position types</span></span> 

<span data-ttu-id="935ca-544">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="935ca-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="935ca-545">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="935ca-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="935ca-546">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="935ca-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="935ca-547">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="935ca-547">Position type</span></span>   | <span data-ttu-id="935ca-548">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="935ca-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="935ca-549">Heltid</span><span class="sxs-lookup"><span data-stu-id="935ca-549">Full-time</span></span>       | <span data-ttu-id="935ca-550">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="935ca-550">Full time employee</span></span> |
| <span data-ttu-id="935ca-551">Deltid</span><span class="sxs-lookup"><span data-stu-id="935ca-551">Part-time</span></span>       | <span data-ttu-id="935ca-552">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="935ca-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="935ca-553">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="935ca-553">Reason codes</span></span>

<span data-ttu-id="935ca-554">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="935ca-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="935ca-555">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="935ca-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="935ca-556">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="935ca-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="935ca-557">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="935ca-557">Reason code</span></span>            | <span data-ttu-id="935ca-558">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="935ca-558">Description</span></span>                    | <span data-ttu-id="935ca-559">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="935ca-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="935ca-560">AVGANGFØRBETALING</span><span class="sxs-lookup"><span data-stu-id="935ca-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="935ca-561">Avgang før første lønn</span><span class="sxs-lookup"><span data-stu-id="935ca-561">Departure before first payroll</span></span> | <span data-ttu-id="935ca-562">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-562">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-563">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="935ca-563">RESIGNATION</span></span>            | <span data-ttu-id="935ca-564">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="935ca-564">Resignation</span></span>                    | <span data-ttu-id="935ca-565">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-565">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-566">PENSJON</span><span class="sxs-lookup"><span data-stu-id="935ca-566">PENSION</span></span>                | <span data-ttu-id="935ca-567">Pensjon</span><span class="sxs-lookup"><span data-stu-id="935ca-567">Pension</span></span>                        | <span data-ttu-id="935ca-568">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-568">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-569">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="935ca-569">TERMINATION</span></span>            | <span data-ttu-id="935ca-570">Avslutning</span><span class="sxs-lookup"><span data-stu-id="935ca-570">Termination</span></span>                    | <span data-ttu-id="935ca-571">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-571">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-572">AVGANGVEDPENSJON</span><span class="sxs-lookup"><span data-stu-id="935ca-572">RETIREMENT</span></span>             | <span data-ttu-id="935ca-573">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="935ca-573">Retirement</span></span>                     | <span data-ttu-id="935ca-574">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-574">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-575">FRAVÆRENDEPERSON</span><span class="sxs-lookup"><span data-stu-id="935ca-575">ABSENTEE</span></span>               | <span data-ttu-id="935ca-576">Fraværende person</span><span class="sxs-lookup"><span data-stu-id="935ca-576">Absentee</span></span>                       | <span data-ttu-id="935ca-577">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-577">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-578">ANNET</span><span class="sxs-lookup"><span data-stu-id="935ca-578">OTHER</span></span>                  | <span data-ttu-id="935ca-579">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="935ca-579">Other Reasons</span></span>                  | <span data-ttu-id="935ca-580">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-580">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-581">STENGNING</span><span class="sxs-lookup"><span data-stu-id="935ca-581">CLOSURE</span></span>                | <span data-ttu-id="935ca-582">Forretning stenger</span><span class="sxs-lookup"><span data-stu-id="935ca-582">Business Closure</span></span>               | <span data-ttu-id="935ca-583">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-583">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-584">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="935ca-584">DEATH</span></span>                  | <span data-ttu-id="935ca-585">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="935ca-585">Death</span></span>                          | <span data-ttu-id="935ca-586">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-586">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-587">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="935ca-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="935ca-588">Permisjon</span><span class="sxs-lookup"><span data-stu-id="935ca-588">Leave of Absence</span></span>               | <span data-ttu-id="935ca-589">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-589">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-590">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="935ca-590">CONTRACTEND</span></span>            | <span data-ttu-id="935ca-591">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="935ca-591">End of Contract</span></span>                | <span data-ttu-id="935ca-592">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="935ca-592">Terminate worker</span></span>     |
| <span data-ttu-id="935ca-593">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="935ca-593">SALARYCHANGE</span></span>           | <span data-ttu-id="935ca-594">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="935ca-594">Change of Salary</span></span>               | <span data-ttu-id="935ca-595">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="935ca-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="935ca-596">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="935ca-596">Terms of employment</span></span>

<span data-ttu-id="935ca-597">Ansettelsesbetingelser brukes til å opprette kategorier for ansettelsesbetingelser.</span><span class="sxs-lookup"><span data-stu-id="935ca-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="935ca-598">Vilkårene tilordnes til Dayforce som ansettelseindikatorverdier.</span><span class="sxs-lookup"><span data-stu-id="935ca-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="935ca-599">Følgende betingelsene for ansettelse og beskrivelser kreves.</span><span class="sxs-lookup"><span data-stu-id="935ca-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="935ca-600">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="935ca-600">Terms of employment</span></span>   | <span data-ttu-id="935ca-601">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="935ca-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="935ca-602">Vanlig</span><span class="sxs-lookup"><span data-stu-id="935ca-602">Regular</span></span>               | <span data-ttu-id="935ca-603">Vanlig</span><span class="sxs-lookup"><span data-stu-id="935ca-603">Regular</span></span>     |
| <span data-ttu-id="935ca-604">Direkte</span><span class="sxs-lookup"><span data-stu-id="935ca-604">Direct</span></span>                | <span data-ttu-id="935ca-605">Direkte</span><span class="sxs-lookup"><span data-stu-id="935ca-605">Direct</span></span>      |
| <span data-ttu-id="935ca-606">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="935ca-606">Internship</span></span>            | <span data-ttu-id="935ca-607">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="935ca-607">Internship</span></span>  |
| <span data-ttu-id="935ca-608">Permanent</span><span class="sxs-lookup"><span data-stu-id="935ca-608">Permanent</span></span>             | <span data-ttu-id="935ca-609">Permanent</span><span class="sxs-lookup"><span data-stu-id="935ca-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="935ca-610">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="935ca-610">Marital status</span></span>

<span data-ttu-id="935ca-611">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="935ca-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="935ca-612">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="935ca-613">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-613">Talent</span></span>                 | <span data-ttu-id="935ca-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="935ca-615">Gift</span><span class="sxs-lookup"><span data-stu-id="935ca-615">Married</span></span>                | <span data-ttu-id="935ca-616">Gift</span><span class="sxs-lookup"><span data-stu-id="935ca-616">Married</span></span>                   |
| <span data-ttu-id="935ca-617">Én</span><span class="sxs-lookup"><span data-stu-id="935ca-617">Single</span></span>                 | <span data-ttu-id="935ca-618">Én</span><span class="sxs-lookup"><span data-stu-id="935ca-618">Single</span></span>                    |
| <span data-ttu-id="935ca-619">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="935ca-619">Widowed</span></span>                | <span data-ttu-id="935ca-620">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="935ca-620">Widowed</span></span>                   |
| <span data-ttu-id="935ca-621">Skilt</span><span class="sxs-lookup"><span data-stu-id="935ca-621">Divorced</span></span>               | <span data-ttu-id="935ca-622">Skilt</span><span class="sxs-lookup"><span data-stu-id="935ca-622">Divorced</span></span>                  |
| <span data-ttu-id="935ca-623">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="935ca-623">Registered Partnership</span></span> | <span data-ttu-id="935ca-624">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="935ca-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="935ca-625">None</span><span class="sxs-lookup"><span data-stu-id="935ca-625">None</span></span>                   | <span data-ttu-id="935ca-626">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="935ca-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="935ca-627">Samboer</span><span class="sxs-lookup"><span data-stu-id="935ca-627">Cohabiting</span></span>             | <span data-ttu-id="935ca-628">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="935ca-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="935ca-629">Kjønn</span><span class="sxs-lookup"><span data-stu-id="935ca-629">Gender</span></span>

<span data-ttu-id="935ca-630">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="935ca-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="935ca-631">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="935ca-632">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-632">Talent</span></span>       | <span data-ttu-id="935ca-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="935ca-634">Mann</span><span class="sxs-lookup"><span data-stu-id="935ca-634">Male</span></span>         | <span data-ttu-id="935ca-635">Mann</span><span class="sxs-lookup"><span data-stu-id="935ca-635">Male</span></span>                      |
| <span data-ttu-id="935ca-636">Kvinne</span><span class="sxs-lookup"><span data-stu-id="935ca-636">Female</span></span>       | <span data-ttu-id="935ca-637">Kvinne</span><span class="sxs-lookup"><span data-stu-id="935ca-637">Female</span></span>                    |
| <span data-ttu-id="935ca-638">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="935ca-638">Non-specific</span></span> | <span data-ttu-id="935ca-639">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="935ca-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="935ca-640">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="935ca-640">Payment method</span></span>

<span data-ttu-id="935ca-641">Betalingsmåter gir den ansatte og firmaet en måte å beskrive hvordan ansatte skal betales.</span><span class="sxs-lookup"><span data-stu-id="935ca-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="935ca-642">Betalingsmåter tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="935ca-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="935ca-643">Tabellen nedenfor viser hvordan betalingsmåter tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="935ca-644">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-644">Talent</span></span>             | <span data-ttu-id="935ca-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="935ca-646">Kontanter</span><span class="sxs-lookup"><span data-stu-id="935ca-646">Cash</span></span>               | <span data-ttu-id="935ca-647">Kontanter</span><span class="sxs-lookup"><span data-stu-id="935ca-647">Cash</span></span>                      |
| <span data-ttu-id="935ca-648">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="935ca-648">Electronic Payment</span></span> | <span data-ttu-id="935ca-649">Overfør</span><span class="sxs-lookup"><span data-stu-id="935ca-649">Transfer</span></span>                  |
| <span data-ttu-id="935ca-650">Kontroll</span><span class="sxs-lookup"><span data-stu-id="935ca-650">Check</span></span>              | <span data-ttu-id="935ca-651">Sjekk</span><span class="sxs-lookup"><span data-stu-id="935ca-651">Cheque</span></span>                    |
| <span data-ttu-id="935ca-652">Bankoverføring</span><span class="sxs-lookup"><span data-stu-id="935ca-652">Bank Draft</span></span>         | <span data-ttu-id="935ca-653">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="935ca-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="935ca-654">Annet</span><span class="sxs-lookup"><span data-stu-id="935ca-654">Other</span></span>              | <span data-ttu-id="935ca-655">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="935ca-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="935ca-656">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="935ca-656">Bank account type</span></span>

<span data-ttu-id="935ca-657">Bankkontotypene brukes for elektroniske betalinger til ansatte.</span><span class="sxs-lookup"><span data-stu-id="935ca-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="935ca-658">Bankkontotypene tilordnes til Dayforce som overføringskontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="935ca-659">Bankkontotypene oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="935ca-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="935ca-660">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-660">Talent</span></span>            | <span data-ttu-id="935ca-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="935ca-662">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="935ca-662">Checking Account</span></span>  | <span data-ttu-id="935ca-663">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="935ca-663">CheckingAccount</span></span>           |
| <span data-ttu-id="935ca-664">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="935ca-664">Payroll Account</span></span>   | <span data-ttu-id="935ca-665">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="935ca-665">PayrollAccount</span></span>            |
| <span data-ttu-id="935ca-666">Sparekonto</span><span class="sxs-lookup"><span data-stu-id="935ca-666">Savings Account</span></span>   | <span data-ttu-id="935ca-667">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="935ca-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="935ca-668">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="935ca-668">BankGirot account</span></span> | <span data-ttu-id="935ca-669">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="935ca-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="935ca-670">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="935ca-670">PlusGirot account</span></span> | <span data-ttu-id="935ca-671">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="935ca-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="935ca-672">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="935ca-672">Earning codes</span></span>

<span data-ttu-id="935ca-673">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="935ca-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="935ca-674">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="935ca-675">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="935ca-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="935ca-676">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="935ca-676">Supported frequencies</span></span>

- <span data-ttu-id="935ca-677">Alle</span><span class="sxs-lookup"><span data-stu-id="935ca-677">All</span></span>
- <span data-ttu-id="935ca-678">HVERBET</span><span class="sxs-lookup"><span data-stu-id="935ca-678">EVERYPAY</span></span>
- <span data-ttu-id="935ca-679">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="935ca-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="935ca-680">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="935ca-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="935ca-681">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="935ca-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="935ca-682">1IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-682">1OFMTH</span></span>
- <span data-ttu-id="935ca-683">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="935ca-683">LASTOFMTH</span></span>
- <span data-ttu-id="935ca-684">2IMDN</span><span class="sxs-lookup"><span data-stu-id="935ca-684">2OFMTH</span></span>
- <span data-ttu-id="935ca-685">3IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-685">3OFMTH</span></span>
- <span data-ttu-id="935ca-686">4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-686">4OFMTH</span></span>
- <span data-ttu-id="935ca-687">5IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-687">5OFMTH</span></span>
- <span data-ttu-id="935ca-688">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-688">1N2OFMTH</span></span>
- <span data-ttu-id="935ca-689">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-689">3N4OFMTH</span></span>
- <span data-ttu-id="935ca-690">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-690">1N3OFMTH</span></span>
- <span data-ttu-id="935ca-691">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-691">1N4OFMTH</span></span>
- <span data-ttu-id="935ca-692">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-692">2N3OFMTH</span></span>
- <span data-ttu-id="935ca-693">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-693">2N4OFMTH</span></span>
- <span data-ttu-id="935ca-694">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="935ca-695">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="935ca-696">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="935ca-697">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="935ca-698">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="935ca-699">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="935ca-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="935ca-700">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="935ca-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="935ca-701">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="935ca-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="935ca-702">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="935ca-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="935ca-703">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="935ca-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="935ca-704">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="935ca-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="935ca-705">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="935ca-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="935ca-706">Adresser</span><span class="sxs-lookup"><span data-stu-id="935ca-706">Addresses</span></span>

<span data-ttu-id="935ca-707">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="935ca-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="935ca-708">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="935ca-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="935ca-709">Talent</span><span class="sxs-lookup"><span data-stu-id="935ca-709">Talent</span></span>              | <span data-ttu-id="935ca-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="935ca-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="935ca-711">Land/område</span><span class="sxs-lookup"><span data-stu-id="935ca-711">Country/Region</span></span>      | <span data-ttu-id="935ca-712">Landskode</span><span class="sxs-lookup"><span data-stu-id="935ca-712">Country Code</span></span>          |
| <span data-ttu-id="935ca-713">Postnummer</span><span class="sxs-lookup"><span data-stu-id="935ca-713">Zip/Postal Code</span></span>     | <span data-ttu-id="935ca-714">Postnummer</span><span class="sxs-lookup"><span data-stu-id="935ca-714">Postal Code</span></span>           |
| <span data-ttu-id="935ca-715">Delstat</span><span class="sxs-lookup"><span data-stu-id="935ca-715">State</span></span>               | <span data-ttu-id="935ca-716">Statskode</span><span class="sxs-lookup"><span data-stu-id="935ca-716">State Code</span></span>            |
| <span data-ttu-id="935ca-717">By</span><span class="sxs-lookup"><span data-stu-id="935ca-717">City</span></span>                | <span data-ttu-id="935ca-718">By</span><span class="sxs-lookup"><span data-stu-id="935ca-718">City</span></span>                  |
| <span data-ttu-id="935ca-719">Kommune</span><span class="sxs-lookup"><span data-stu-id="935ca-719">County</span></span>              | <span data-ttu-id="935ca-720">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="935ca-720">County (Municipality)</span></span> |
| <span data-ttu-id="935ca-721">Gate</span><span class="sxs-lookup"><span data-stu-id="935ca-721">Street</span></span>              | <span data-ttu-id="935ca-722">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="935ca-722">Address Line 1</span></span>        |
| <span data-ttu-id="935ca-723">Gatenummer</span><span class="sxs-lookup"><span data-stu-id="935ca-723">Street Number</span></span>       | <span data-ttu-id="935ca-724">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="935ca-724">Address Line 2</span></span>        |
| <span data-ttu-id="935ca-725">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="935ca-725">Building Complement</span></span> | <span data-ttu-id="935ca-726">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="935ca-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="935ca-727">Passnummer</span><span class="sxs-lookup"><span data-stu-id="935ca-727">Passport number</span></span>

<span data-ttu-id="935ca-728">Ansatte kan deklarere passinformasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-728">Employees can declare passport information.</span></span> <span data-ttu-id="935ca-729">Denne informasjonen er av **Pass**-identifikasjonstypen og er integrert i Dayforce som en del av en ansatts Mexico-spesifikke informasjon.</span><span class="sxs-lookup"><span data-stu-id="935ca-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="935ca-730">Identifikasjonstype = "Pass"</span><span class="sxs-lookup"><span data-stu-id="935ca-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="935ca-731">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="935ca-731">Issued Date</span></span>
- <span data-ttu-id="935ca-732">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="935ca-732">Expiration Date</span></span>

<span data-ttu-id="935ca-733">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **Pass**.</span><span class="sxs-lookup"><span data-stu-id="935ca-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="935ca-734">Men bare den gjeldende aktive passoppføringen er integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="935ca-735">Hvis alle passoppføringer er utløpt, er passet som sist ble utstedt, integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="935ca-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

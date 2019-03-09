---
title: Konfigurere lønnsintegreringen mellom Talent og Dayforce
description: Dette emnet forklarer hvordan du konfigurerer integrasjonen mellom Microsoft Dynamics 365 for Talent og Ceridian Dayforce slik at du kan behandle en lønnskjøring.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305605"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="5e992-103">Konfigurere lønnsintegrering mellom Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e992-104">Integrasjonen mellom Microsoft Dynamics 365 for Talent og Ceridian Dayforce bruker flere konfigurasjonstrinn som er beskrevet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="5e992-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="5e992-105">Du må konfigurere integreringen i både Talent og Dayforce før du kan behandle en lønnskjøring.</span><span class="sxs-lookup"><span data-stu-id="5e992-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="5e992-106">Når du bruker en tjeneste som Dayforce til å fullføre lønnskjøringer, må du aktivere integrering i Talent.</span><span class="sxs-lookup"><span data-stu-id="5e992-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="5e992-107">Integreringen krever bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="5e992-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="5e992-108">Derfor må du kontrollere at data som tilordnes til Dayforce, er konfigurert i Talent på en måte som støtter integreringen.</span><span class="sxs-lookup"><span data-stu-id="5e992-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="5e992-109">Integrasjonen bruker følgende brede datakategorier:</span><span class="sxs-lookup"><span data-stu-id="5e992-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="5e992-110">Personaldata</span><span class="sxs-lookup"><span data-stu-id="5e992-110">Human resources data</span></span>
- <span data-ttu-id="5e992-111">Kompensasjonsdata</span><span class="sxs-lookup"><span data-stu-id="5e992-111">Compensation data</span></span>
- <span data-ttu-id="5e992-112">Lønnsdata, for eksempel lønnssykluser, lønnsperioder og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="5e992-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="5e992-113">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="5e992-113">Worker data</span></span>

<span data-ttu-id="5e992-114">Dette emnet beskriver trinnene du må følge for å aktivere integreringen.</span><span class="sxs-lookup"><span data-stu-id="5e992-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="5e992-115">Den beskriver også hvilke typer data og konfigurasjonsdetaljer som integreringen krever.</span><span class="sxs-lookup"><span data-stu-id="5e992-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="5e992-116">Aktivere integrasjonen</span><span class="sxs-lookup"><span data-stu-id="5e992-116">Enable the integration</span></span>

<span data-ttu-id="5e992-117">I Talent må du aktivere integreringen og angi konfigurasjonsinformasjonen for å koble til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="5e992-118">Hvis du vil at økonomimodultransaksjonen som produseres, skal importeres til Microsoft Dynamics 365 for Finance and Operations, må du også definere en Microsoft Azure-lagringskonto og angi Azure Storage-tilkoblingsstrengen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e992-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="5e992-119">Følg denne fremgangsmåten for å aktivere integrasjonen i Talent.</span><span class="sxs-lookup"><span data-stu-id="5e992-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="5e992-120">Velg **Konfigurasjon av integrering** på siden **Systemadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="5e992-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="5e992-121">Angi sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="5e992-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="5e992-122">Angi brukernavnet og passordet til brukeren som skal ha tilgang til sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="5e992-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="5e992-123">Test tilkoblingen etter behov, og sett alternativet **Aktiver lønnsintegrering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5e992-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="5e992-124">Når integreringen er slått på, opprettes dataeksportpakken og -filene, og frekvensen angis.</span><span class="sxs-lookup"><span data-stu-id="5e992-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="5e992-125">Du kan endre denne frekvensen etter behov.</span><span class="sxs-lookup"><span data-stu-id="5e992-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="5e992-126">Hvis du vil ha mer informasjon om Azure Storage-kontoer og Azure Storage-tilkoblingsstrenger, kan du se følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="5e992-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="5e992-127">Om Azure Storage-kontoer</span><span class="sxs-lookup"><span data-stu-id="5e992-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="5e992-128">Konfigurere Azure Storage-tilkoblingsstrenger</span><span class="sxs-lookup"><span data-stu-id="5e992-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="5e992-129">Konfigurere dataene dine</span><span class="sxs-lookup"><span data-stu-id="5e992-129">Configure your data</span></span> 

<span data-ttu-id="5e992-130">For å behandle lønn må du konfigurere Personaldata i Talent.</span><span class="sxs-lookup"><span data-stu-id="5e992-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="5e992-131">Du må definere organisasjonsdata, for eksempel jobber og stillinger, samt informasjon om fordeler og kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="5e992-132">Denne informasjonen gir informasjon om ansettelse, lønn og trekk som kreves for å kunne generere lønn for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="5e992-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="5e992-133">Personaldata</span><span class="sxs-lookup"><span data-stu-id="5e992-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="5e992-134">Fordeler</span><span class="sxs-lookup"><span data-stu-id="5e992-134">Benefits</span></span> 

<span data-ttu-id="5e992-135">Personale inneholder verktøy for oppsett og vedlikehold av fordeler, fradrag og arbeiderkompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere.</span><span class="sxs-lookup"><span data-stu-id="5e992-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="5e992-136">Når du oppretter fordeler, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="5e992-137">Fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="5e992-137">Benefit plans</span></span>

- <span data-ttu-id="5e992-138">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-138">Plan (required)</span></span>
- <span data-ttu-id="5e992-139">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-139">Type (required)</span></span>
- <span data-ttu-id="5e992-140">Lønnsinnvirkning (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-140">Payroll impact (required)</span></span>
- <span data-ttu-id="5e992-141">Gjenopprett etterskudd</span><span class="sxs-lookup"><span data-stu-id="5e992-141">Recover arrears</span></span>
- <span data-ttu-id="5e992-142">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="5e992-142">Deduction method</span></span>
- <span data-ttu-id="5e992-143">Fradragsprioritet</span><span class="sxs-lookup"><span data-stu-id="5e992-143">Deduction priority</span></span>
- <span data-ttu-id="5e992-144">Begrens periode</span><span class="sxs-lookup"><span data-stu-id="5e992-144">Limit period</span></span>
- <span data-ttu-id="5e992-145">Grensebeløp</span><span class="sxs-lookup"><span data-stu-id="5e992-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="5e992-146">Fordeler</span><span class="sxs-lookup"><span data-stu-id="5e992-146">Benefits</span></span>

- <span data-ttu-id="5e992-147">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-147">Plan (required)</span></span>
- <span data-ttu-id="5e992-148">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-148">Type (required)</span></span>
- <span data-ttu-id="5e992-149">Alternativ (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-149">Option (required)</span></span>
- <span data-ttu-id="5e992-150">Fordel-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-150">Benefit ID (required)</span></span>
- <span data-ttu-id="5e992-151">Frekvens</span><span class="sxs-lookup"><span data-stu-id="5e992-151">Frequency</span></span>
- <span data-ttu-id="5e992-152">Grunnlag</span><span class="sxs-lookup"><span data-stu-id="5e992-152">Basis</span></span>
- <span data-ttu-id="5e992-153">Beløp eller sats</span><span class="sxs-lookup"><span data-stu-id="5e992-153">Amount or rate</span></span>
- <span data-ttu-id="5e992-154">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="5e992-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="5e992-155">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="5e992-155">Supported frequencies</span></span> 

- <span data-ttu-id="5e992-156">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="5e992-156">Weekly</span></span>
- <span data-ttu-id="5e992-157">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="5e992-157">Bi-weekly</span></span>
- <span data-ttu-id="5e992-158">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="5e992-158">Semi-monthly</span></span>
- <span data-ttu-id="5e992-159">Månedlig</span><span class="sxs-lookup"><span data-stu-id="5e992-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="5e992-160">Støttede grunnlag</span><span class="sxs-lookup"><span data-stu-id="5e992-160">Supported bases</span></span> 

- <span data-ttu-id="5e992-161">Fast beløp</span><span class="sxs-lookup"><span data-stu-id="5e992-161">Fixed amount</span></span>
- <span data-ttu-id="5e992-162">Prosentandel av inntekter</span><span class="sxs-lookup"><span data-stu-id="5e992-162">Percent of earnings</span></span>
- <span data-ttu-id="5e992-163">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="5e992-163">Productive hours</span></span>

<span data-ttu-id="5e992-164">Dayforce oppretter følgende fradrag, basert på lønnsinnvirkning som er definert på fordelsplanen.</span><span class="sxs-lookup"><span data-stu-id="5e992-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="5e992-165">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-165">Selection in Talent</span></span>        | <span data-ttu-id="5e992-166">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="5e992-167">None</span><span class="sxs-lookup"><span data-stu-id="5e992-167">None</span></span>                       | <span data-ttu-id="5e992-168">Ingen fradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="5e992-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="5e992-169">Bare fradrag</span><span class="sxs-lookup"><span data-stu-id="5e992-169">Deduction only</span></span>             | <span data-ttu-id="5e992-170">Et ansattfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="5e992-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="5e992-171">Bare bidrag</span><span class="sxs-lookup"><span data-stu-id="5e992-171">Contribution only</span></span>          | <span data-ttu-id="5e992-172">Et arbeidsgiverfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="5e992-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="5e992-173">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="5e992-173">Deduction and contribution</span></span> | <span data-ttu-id="5e992-174">Fradrag for ansatte og arbeidsgivere opprettes.</span><span class="sxs-lookup"><span data-stu-id="5e992-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="5e992-175">Hvis du vil ha mer informasjon om hvordan du definerer og administrerer et program for fordeler, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="5e992-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="5e992-176">Levere et program for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="5e992-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="5e992-177">Opprette en ny fordel</span><span class="sxs-lookup"><span data-stu-id="5e992-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="5e992-178">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="5e992-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="5e992-179">Registrere og fjerne fordeler fra arbeidere</span><span class="sxs-lookup"><span data-stu-id="5e992-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="5e992-180">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-180">Compensation</span></span> 

<span data-ttu-id="5e992-181">Kompensasjonsstyring brukes til å kontrollere levering av grunnlønn og bonuser.</span><span class="sxs-lookup"><span data-stu-id="5e992-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="5e992-182">En ansatts faste grunnlønn og personlige tilleggsøkninger styres via faste kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="5e992-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="5e992-183">Betaling av insitamentutbetalinger, for eksempel bonuser, ytelsestillegg, aksjeopsjoner og tilskudd, og også engangsbonuser, kontrolleres via variable kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="5e992-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="5e992-184">Dayforce bruker kompensasjonsinformasjon til å beregne timesats eller årlig sats for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="5e992-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="5e992-185">Planer for faste kompensasjoner og konverteringer av lønnssats er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="5e992-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="5e992-186">Ansatte må tilknyttes en plan for fast kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="5e992-187">Hvis du vil ha mer informasjon om kompensasjonsplaner, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="5e992-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="5e992-188">Opprette planer for fast kompensasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="5e992-189">Opprette variable kompensasjonsplaner</span><span class="sxs-lookup"><span data-stu-id="5e992-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="5e992-190">Utvikle struktur og planer for lønn/kompensasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="5e992-191">Behandle kompensasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="5e992-192">Definere kompensasjonsprosess og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="5e992-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="5e992-193">Registrere en ansatt i en fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="5e992-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="5e992-194">Registrere en ansatt i en variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="5e992-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="5e992-195">Jobber</span><span class="sxs-lookup"><span data-stu-id="5e992-195">Jobs</span></span> 

<span data-ttu-id="5e992-196">En jobb er en samling oppgaver og ansvarsområder som kreves av en person som utfører en jobb.</span><span class="sxs-lookup"><span data-stu-id="5e992-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="5e992-197">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="5e992-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="5e992-198">Definere komponentene for en jobb</span><span class="sxs-lookup"><span data-stu-id="5e992-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="5e992-199">Definere nye jobber</span><span class="sxs-lookup"><span data-stu-id="5e992-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="5e992-200">Stillinger</span><span class="sxs-lookup"><span data-stu-id="5e992-200">Positions</span></span>

<span data-ttu-id="5e992-201">En stilling er én enkeltforekomst av en jobb.</span><span class="sxs-lookup"><span data-stu-id="5e992-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="5e992-202">"Salgssjef (øst)"-stillingen er for eksempel én av stillingene som er knyttet til jobben "Salgssjef".</span><span class="sxs-lookup"><span data-stu-id="5e992-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="5e992-203">Det finnes en stilling i en avdeling.</span><span class="sxs-lookup"><span data-stu-id="5e992-203">A position exists in a department.</span></span> <span data-ttu-id="5e992-204">Bare én arbeider kan være tilknyttet hvert område.</span><span class="sxs-lookup"><span data-stu-id="5e992-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="5e992-205">Ha følgende data og konfigurasjon i bakhodet når du definerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="5e992-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="5e992-206">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-206">Position (required)</span></span>
- <span data-ttu-id="5e992-207">Beskrivelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-207">Description (required)</span></span>
- <span data-ttu-id="5e992-208">Jobb (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-208">Job (required)</span></span>
- <span data-ttu-id="5e992-209">Avdeling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-209">Department (required)</span></span>
- <span data-ttu-id="5e992-210">Stillingstype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-210">Position type (required)</span></span>
- <span data-ttu-id="5e992-211">Fulltidsekvivalent</span><span class="sxs-lookup"><span data-stu-id="5e992-211">Full-time equivalent</span></span>
- <span data-ttu-id="5e992-212">Årlige vanlige timer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="5e992-213">Betalt av juridisk enhet (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="5e992-214">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-214">Pay cycle (required)</span></span>
- <span data-ttu-id="5e992-215">Standard finansdimensjon – kostsenter (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="5e992-216">Arbeidertilordning – arbeider, start for tilordning, slutt for tilordning, årsakskode</span><span class="sxs-lookup"><span data-stu-id="5e992-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="5e992-217">Hvis flere stillinger i samme avdeling er knyttet til den samme jobben, konsolideres de til én stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="5e992-218">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="5e992-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="5e992-219">Organisere arbeidsstyrken ved bruk av avdelinger, jobber og stillinger</span><span class="sxs-lookup"><span data-stu-id="5e992-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="5e992-220">Definere stillinger</span><span class="sxs-lookup"><span data-stu-id="5e992-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="5e992-221">Avdelinger</span><span class="sxs-lookup"><span data-stu-id="5e992-221">Departments</span></span>

<span data-ttu-id="5e992-222">En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="5e992-223">En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale.</span><span class="sxs-lookup"><span data-stu-id="5e992-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="5e992-224">Du kan bruke avdelinger til å rapportere om funksjonsområder.</span><span class="sxs-lookup"><span data-stu-id="5e992-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="5e992-225">Avdelinger kan ha ansvar for fortjeneste og tap.</span><span class="sxs-lookup"><span data-stu-id="5e992-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="5e992-226">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="5e992-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="5e992-227">Opprette en avdeling og knytte den til avdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="5e992-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="5e992-228">Definere nye avdelinger</span><span class="sxs-lookup"><span data-stu-id="5e992-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="5e992-229">Lønnssykluser og lønnsperioder</span><span class="sxs-lookup"><span data-stu-id="5e992-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="5e992-230">En betalingssyklus avgjør hvor ofte lønnskjøring utføres, og de spesifikke dagene arbeidere lønnes.</span><span class="sxs-lookup"><span data-stu-id="5e992-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="5e992-231">For eksempel kan en lønnssyklus være månedlig, og ansatte kan betales på den siste dagen i måneden.</span><span class="sxs-lookup"><span data-stu-id="5e992-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="5e992-232">En lønnssyklus kan også være ukentlig, og ansatte kan betales tirsdagen etter slutten av lønnsperioden.</span><span class="sxs-lookup"><span data-stu-id="5e992-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="5e992-233">Lønnssykluser tilordnes til stillinger for å styre når arbeidere i disse stillingene lønnes.</span><span class="sxs-lookup"><span data-stu-id="5e992-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="5e992-234">Når du oppretter lønnssykler, kan du generere lønnsperioder for hver enkelt syklus.</span><span class="sxs-lookup"><span data-stu-id="5e992-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="5e992-235">Hver lønnsperiode inkluderer en standard betalingsdato som er basert på informasjonen du angir.</span><span class="sxs-lookup"><span data-stu-id="5e992-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="5e992-236">Du kan imidlertid endre standard betalingsdato i en lønnsperiode for å tillate unntak, for eksempel når betalingsdatoen faller på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="5e992-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="5e992-237">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="5e992-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="5e992-238">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-238">Pay cycle (required)</span></span>
- <span data-ttu-id="5e992-239">Lønnssyklusfrekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="5e992-240">Periodens startdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="5e992-241">Standard betalingsdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="5e992-242">Denne informasjonen er integrert med Dayforce som lønnsgrupper og er inndelt etter land eller område for hver lønnssyklus.</span><span class="sxs-lookup"><span data-stu-id="5e992-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="5e992-243">Minst én lønnsperiode må genereres før integrasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="5e992-244">Dayforce genererer lønnsgruppekalendere og betalingsdatoer basert på startdatoen for den første lønnsperioden og standard betalingsdato som er definert i Talent.</span><span class="sxs-lookup"><span data-stu-id="5e992-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="5e992-245">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="5e992-245">Earning codes</span></span>

<span data-ttu-id="5e992-246">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="5e992-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5e992-247">Kodene har forskjellige parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="5e992-248">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="5e992-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="5e992-249">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-249">Earning Code (required)</span></span>
- <span data-ttu-id="5e992-250">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5e992-250">Description</span></span>
- <span data-ttu-id="5e992-251">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="5e992-251">Unit of measure</span></span>
- <span data-ttu-id="5e992-252">Produktiv</span><span class="sxs-lookup"><span data-stu-id="5e992-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="5e992-253">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="5e992-253">Worker data</span></span>

<span data-ttu-id="5e992-254">Poster for ulike typer arbeidere som du har, er viktig for personal. og lønnsystemene dine.</span><span class="sxs-lookup"><span data-stu-id="5e992-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="5e992-255">Informasjonen du legger inn, kan brukes til å spore arbeidere og personlig informasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="5e992-256">Du kan vedlikeholde følgende informasjon om arbeidere:</span><span class="sxs-lookup"><span data-stu-id="5e992-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="5e992-257">**Grunnleggende** – Vedlikehold grunnleggende informasjon om en arbeider, for eksempel kontaktinformasjon, demografisk informasjon, identifikasjonsinformasjon, familieinformasjon, militærtjenestestatus, informasjon om personer som bor i utlandet, og personlige kontakter og kontakter i nødfall.</span><span class="sxs-lookup"><span data-stu-id="5e992-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="5e992-258">**Ansettelse** – Vedlikehold informasjon om en arbeiders ansettelse, for eksempel informasjon om firma- eller organisasjonstilknytning, stillingstilordning, start- og sluttdatoer, arbeidstillatelse, vilkår for ansettelse, pensjon, ferie og flytting.</span><span class="sxs-lookup"><span data-stu-id="5e992-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="5e992-259">**Lønn og fravær** – Vedlikehold opplysninger om en arbeiders fravær, for eksempel arbeidskalendere, fraværstransaksjoner og fraværsoppsett.</span><span class="sxs-lookup"><span data-stu-id="5e992-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="5e992-260">**Kompensasjon og lønn** – Vedlikehold informasjon om en arbeiders kompensasjonsplaner og lønn, for eksempel planregistrering, priser, ytelse, provisjon, avgiftsinformasjon, pensjonering og lønnstrekk.</span><span class="sxs-lookup"><span data-stu-id="5e992-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="5e992-261">Når du legger inn arbeiderinformasjon, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="5e992-262">Generell informasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-262">General information</span></span>

- <span data-ttu-id="5e992-263">Personalnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-263">Personnel number (required)</span></span>
- <span data-ttu-id="5e992-264">Fornavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-264">First name (required)</span></span>
- <span data-ttu-id="5e992-265">Etternavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-265">Last name (required)</span></span>
- <span data-ttu-id="5e992-266">Mellomnavn</span><span class="sxs-lookup"><span data-stu-id="5e992-266">Middle name</span></span>
- <span data-ttu-id="5e992-267">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="5e992-267">Seniority date</span></span>
- <span data-ttu-id="5e992-268">Kalt</span><span class="sxs-lookup"><span data-stu-id="5e992-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="5e992-269">Personlige opplysninger</span><span class="sxs-lookup"><span data-stu-id="5e992-269">Personal information</span></span>

- <span data-ttu-id="5e992-270">Sivilstand (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-270">Marital status (required)</span></span>
- <span data-ttu-id="5e992-271">Fødselsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-271">Birth date (required)</span></span>
- <span data-ttu-id="5e992-272">Kjønn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-272">Gender (required)</span></span>
- <span data-ttu-id="5e992-273">Person med funksjonshemminger</span><span class="sxs-lookup"><span data-stu-id="5e992-273">Person with disabilities</span></span>
- <span data-ttu-id="5e992-274">Nasjonalitet land/område (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="5e992-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="5e992-275">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="5e992-275">Address information</span></span>

- <span data-ttu-id="5e992-276">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-276">Primary (required)</span></span>
- <span data-ttu-id="5e992-277">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-277">Country/region (required)</span></span>
- <span data-ttu-id="5e992-278">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-278">Postal code (required)</span></span>
- <span data-ttu-id="5e992-279">Gatenummer (obligatorisk) (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="5e992-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="5e992-280">Bygningsnavn (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="5e992-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="5e992-281">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-281">City (required)</span></span>
- <span data-ttu-id="5e992-282">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-282">State (required)</span></span>
- <span data-ttu-id="5e992-283">Land (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="5e992-284">Kontaktinformasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-284">Contact information</span></span> 

- <span data-ttu-id="5e992-285">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-285">Primary (required)</span></span>
- <span data-ttu-id="5e992-286">Kontaktnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-286">Contact number (required)</span></span>
- <span data-ttu-id="5e992-287">Utvidelse</span><span class="sxs-lookup"><span data-stu-id="5e992-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="5e992-288">Lønnsinformasjon og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="5e992-288">Payroll information and earning codes</span></span>

<span data-ttu-id="5e992-289">Ansatte kan tilordnes spesifikke inntekter med en gitt betalingfrekvens og med en foretrukket betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="5e992-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="5e992-290">Følgende felt brukes i Dayforce for å sørge for at disse valgene og innstillingene brukes.</span><span class="sxs-lookup"><span data-stu-id="5e992-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="5e992-291">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="5e992-291">Earning codes</span></span>

- <span data-ttu-id="5e992-292">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-292">Position (required)</span></span>
- <span data-ttu-id="5e992-293">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-293">Earning Code (required)</span></span>
- <span data-ttu-id="5e992-294">Frekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-294">Frequency (required)</span></span>
- <span data-ttu-id="5e992-295">Beløp (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="5e992-296">Lønnsinformasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-296">Payroll information</span></span>

- <span data-ttu-id="5e992-297">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="5e992-297">Payment Method</span></span>
- <span data-ttu-id="5e992-298">Økonomisk område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-298">Economic Region (required)</span></span>
- <span data-ttu-id="5e992-299">ID for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="5e992-299">Employee Benefits ID</span></span>
- <span data-ttu-id="5e992-300">Nasjonalt ID-nummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-300">National ID Number (required)</span></span>
- <span data-ttu-id="5e992-301">Militærtjenestenummer</span><span class="sxs-lookup"><span data-stu-id="5e992-301">Military Service Number</span></span>
- <span data-ttu-id="5e992-302">Skift-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-302">Shift ID (required)</span></span>
- <span data-ttu-id="5e992-303">Avgiftsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-303">Tax Number (required)</span></span>
- <span data-ttu-id="5e992-304">Fagforenings-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-304">Union ID (required)</span></span>
- <span data-ttu-id="5e992-305">Arbeidsdag-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-305">Work Day ID (required)</span></span>
- <span data-ttu-id="5e992-306">Arbeidstillatelsesnummer</span><span class="sxs-lookup"><span data-stu-id="5e992-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="5e992-307">Når det gjelder betalingsmåte støtter Mexico **Kontanter**, **Sjekk** (firmaets fysisk sjekk) og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="5e992-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="5e992-308">Hvis betalingsmåte ikke er angitt, brukes **Sjekk** som standard.</span><span class="sxs-lookup"><span data-stu-id="5e992-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="5e992-309">Ansettelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="5e992-309">Employment details</span></span>

<span data-ttu-id="5e992-310">Ansettelsesdetaljhistorikk brukes som nøkkelinformasjon til å avlede en ansatts ansettelse-, oppsigelses- og nyansettelsesstatuser i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="5e992-311">Dayforce støtter bare én aktiv ansettelsespost om gangen.</span><span class="sxs-lookup"><span data-stu-id="5e992-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="5e992-312">Startdato for ansettelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-312">Employment start date (required)</span></span>
- <span data-ttu-id="5e992-313">Sluttdato for ansettelse</span><span class="sxs-lookup"><span data-stu-id="5e992-313">Employment end date</span></span>
- <span data-ttu-id="5e992-314">Startdato</span><span class="sxs-lookup"><span data-stu-id="5e992-314">Start date</span></span>
- <span data-ttu-id="5e992-315">Justert startdato</span><span class="sxs-lookup"><span data-stu-id="5e992-315">Adjusted start date</span></span>
- <span data-ttu-id="5e992-316">Avslutningsdato (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="5e992-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="5e992-317">Avslutningsårsak (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="5e992-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="5e992-318">En ansatts nøkkeldatoer avledes ved å bruke følgende informasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="5e992-319">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-319">Talent</span></span>                | <span data-ttu-id="5e992-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e992-321">Den siste ansettelsesdatoen</span><span class="sxs-lookup"><span data-stu-id="5e992-321">Most recent hire date</span></span> | <span data-ttu-id="5e992-322">Ansettelsesstart for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="5e992-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="5e992-323">Avslutningsdato</span><span class="sxs-lookup"><span data-stu-id="5e992-323">Termination date</span></span>      | <span data-ttu-id="5e992-324">Avslutningsdato for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="5e992-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="5e992-325">Startdato</span><span class="sxs-lookup"><span data-stu-id="5e992-325">Start date</span></span>            | <span data-ttu-id="5e992-326">Justert startdato, startdato eller ansettelsesstart for gjeldende ikke-aktive ansettelseloggpost</span><span class="sxs-lookup"><span data-stu-id="5e992-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="5e992-327">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="5e992-327">Original hire date</span></span>    | <span data-ttu-id="5e992-328">Ansettelsesstart for tidligste ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="5e992-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="5e992-329">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-329">Compensation</span></span>

<span data-ttu-id="5e992-330">En fast kompensasjonsplan må være knyttet til hver ansatts primære stilling i en ansattperiode.</span><span class="sxs-lookup"><span data-stu-id="5e992-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="5e992-331">Denne perioden begynner på datoen da den ansatte ble ansatt (eller startdatoen for ansettelsen), og fortsetter til avslutning.</span><span class="sxs-lookup"><span data-stu-id="5e992-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="5e992-332">Gyldighetsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-332">Effective Date (required)</span></span>
- <span data-ttu-id="5e992-333">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="5e992-333">Expiration date</span></span>
- <span data-ttu-id="5e992-334">Lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-334">Pay Rate (required)</span></span>
- <span data-ttu-id="5e992-335">Konverteringer av lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="5e992-336">Tilsvarende årlig (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="5e992-337">Tilsvarende per time (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="5e992-338">Hvis en timebaserte ansatt har flere stillinger, importeres fast kompensasjon for den primære stillingen til Dayforce som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="5e992-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="5e992-339">For ikke-primære stillinger lagres timeprisen til den tilsvarende stillingen i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="5e992-340">Hvis en lønnsansatt har flere stillinger, avledes kumulativ timepris og årslønn på tvers av alle aktive stillinger og brukes som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="5e992-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="5e992-341">Identifikasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="5e992-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="5e992-342">Personnummeridentifikator</span><span class="sxs-lookup"><span data-stu-id="5e992-342">Social Security identifier</span></span> 

<span data-ttu-id="5e992-343">Alle ansatte må ha én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="5e992-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="5e992-344">Identifikatoren må være av identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="5e992-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="5e992-345">I Dayforce hentes den automatisk som den ansattes personnummeridentifikator som kreves for ansettelse.</span><span class="sxs-lookup"><span data-stu-id="5e992-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="5e992-346">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-346">Primary (required)</span></span>
- <span data-ttu-id="5e992-347">Identifikasjonstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="5e992-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="5e992-348">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="5e992-348">Issued Date</span></span>
- <span data-ttu-id="5e992-349">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="5e992-349">Expiration Date</span></span>

<span data-ttu-id="5e992-350">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="5e992-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="5e992-351">Det er imidlertid bare posten som er merket som **Primær**, som er integrert i Dayforce, uansett om nummeret er aktivt eller utløpt.</span><span class="sxs-lookup"><span data-stu-id="5e992-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="5e992-352">Bankkontoer og -utlegg</span><span class="sxs-lookup"><span data-stu-id="5e992-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="5e992-353">Gyldig bankkontoinformasjon må angis for alle ansatte som velger å betales via bankkontooverføringer.</span><span class="sxs-lookup"><span data-stu-id="5e992-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="5e992-354">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-354">Talent</span></span>                         | <span data-ttu-id="5e992-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e992-356">Bankkontonummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="5e992-357">SWIFT-kode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-357">SWIFT code (required)</span></span>          | <span data-ttu-id="5e992-358">**Bank-ID**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="5e992-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="5e992-359">Avdelingsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="5e992-360">Bankkontotype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-360">Bank account type (required)</span></span>   | <span data-ttu-id="5e992-361">**Kontotoype**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="5e992-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="5e992-362">Støttede verdier inkluderer **Kontroll** og **Lønn**.</span><span class="sxs-lookup"><span data-stu-id="5e992-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="5e992-363">Ansatte som velger å betales via bankkontooverføringer, må oppgi en kobling til en restkonto som er under en juridisk enhet som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en meksikansk bank.</span><span class="sxs-lookup"><span data-stu-id="5e992-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="5e992-364">Alle andre ikke-restkontoer ignoreres.</span><span class="sxs-lookup"><span data-stu-id="5e992-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="5e992-365">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="5e992-365">Address information</span></span>

<span data-ttu-id="5e992-366">Alle ansatte må ha ett primært sted.</span><span class="sxs-lookup"><span data-stu-id="5e992-366">Every employee must have one primary location.</span></span> <span data-ttu-id="5e992-367">I Dayforce brukes dette stedet til å fastslå den ansattes primære bosted for skatte- og avgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="5e992-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="5e992-368">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-368">Primary (required)</span></span>
- <span data-ttu-id="5e992-369">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-369">Country/region (required)</span></span>
- <span data-ttu-id="5e992-370">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="5e992-371">Gate (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-371">Street (required)</span></span>
- <span data-ttu-id="5e992-372">Gatenummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-372">Street Number (required)</span></span>
- <span data-ttu-id="5e992-373">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="5e992-373">Building Complement</span></span>
- <span data-ttu-id="5e992-374">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-374">City (required)</span></span>
- <span data-ttu-id="5e992-375">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-375">State (required)</span></span>
- <span data-ttu-id="5e992-376">Land (oblitagorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="5e992-377">Konfigurer dataene for å generere lønn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="5e992-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="5e992-378">Hvis du skal generere lønn for ansatte i USA og Canada, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="5e992-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="5e992-379">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="5e992-379">Departments are required on positions.</span></span>
- <span data-ttu-id="5e992-380">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="5e992-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="5e992-381">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="5e992-381">Job types</span></span>

<span data-ttu-id="5e992-382">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="5e992-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="5e992-383">Jobbtyper kreves for å kunne behandle lønn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="5e992-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="5e992-384">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="5e992-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="5e992-385">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="5e992-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="5e992-386">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="5e992-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="5e992-387">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="5e992-387">Job type</span></span>   | <span data-ttu-id="5e992-388">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5e992-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="5e992-389">Per time</span><span class="sxs-lookup"><span data-stu-id="5e992-389">Hourly</span></span>     | <span data-ttu-id="5e992-390">Per time</span><span class="sxs-lookup"><span data-stu-id="5e992-390">Hourly</span></span>      |
| <span data-ttu-id="5e992-391">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="5e992-391">Salaried</span></span>   | <span data-ttu-id="5e992-392">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="5e992-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="5e992-393">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="5e992-393">Position types</span></span> 

<span data-ttu-id="5e992-394">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="5e992-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="5e992-395">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="5e992-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="5e992-396">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="5e992-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="5e992-397">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="5e992-397">Position type</span></span>   | <span data-ttu-id="5e992-398">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5e992-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="5e992-399">Heltid</span><span class="sxs-lookup"><span data-stu-id="5e992-399">Full-time</span></span>       | <span data-ttu-id="5e992-400">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="5e992-400">Full time employee</span></span> |
| <span data-ttu-id="5e992-401">Deltid</span><span class="sxs-lookup"><span data-stu-id="5e992-401">Part-time</span></span>       | <span data-ttu-id="5e992-402">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="5e992-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="5e992-403">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="5e992-403">Reason codes</span></span>

<span data-ttu-id="5e992-404">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="5e992-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="5e992-405">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="5e992-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="5e992-406">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="5e992-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="5e992-407">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="5e992-407">Reason code</span></span>    | <span data-ttu-id="5e992-408">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5e992-408">Description</span></span>      | <span data-ttu-id="5e992-409">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="5e992-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="5e992-410">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="5e992-410">RESIGNATION</span></span>    | <span data-ttu-id="5e992-411">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="5e992-411">Resignation</span></span>      | <span data-ttu-id="5e992-412">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-412">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-413">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="5e992-413">TERMINATION</span></span>    | <span data-ttu-id="5e992-414">Avslutning</span><span class="sxs-lookup"><span data-stu-id="5e992-414">Termination</span></span>      | <span data-ttu-id="5e992-415">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-415">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-416">AVGANG VED PENSJON</span><span class="sxs-lookup"><span data-stu-id="5e992-416">RETIREMENT</span></span>     | <span data-ttu-id="5e992-417">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="5e992-417">Retirement</span></span>       | <span data-ttu-id="5e992-418">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-418">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-419">ANNET</span><span class="sxs-lookup"><span data-stu-id="5e992-419">OTHER</span></span>          | <span data-ttu-id="5e992-420">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="5e992-420">Other Reasons</span></span>    | <span data-ttu-id="5e992-421">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-421">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-422">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="5e992-422">DEATH</span></span>          | <span data-ttu-id="5e992-423">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="5e992-423">Death</span></span>            | <span data-ttu-id="5e992-424">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-424">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-425">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="5e992-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="5e992-426">Permisjon</span><span class="sxs-lookup"><span data-stu-id="5e992-426">Leave of Absence</span></span> | <span data-ttu-id="5e992-427">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-427">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-428">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="5e992-428">CONTRACTEND</span></span>    | <span data-ttu-id="5e992-429">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="5e992-429">End of Contract</span></span>  | <span data-ttu-id="5e992-430">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-430">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-431">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="5e992-431">SALARYCHANGE</span></span>   | <span data-ttu-id="5e992-432">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="5e992-432">Change of Salary</span></span> | <span data-ttu-id="5e992-433">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="5e992-434">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="5e992-434">Marital status</span></span>

<span data-ttu-id="5e992-435">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="5e992-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5e992-436">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="5e992-437">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-437">Talent</span></span>                 | <span data-ttu-id="5e992-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="5e992-439">Gift</span><span class="sxs-lookup"><span data-stu-id="5e992-439">Married</span></span>                | <span data-ttu-id="5e992-440">Gift</span><span class="sxs-lookup"><span data-stu-id="5e992-440">Married</span></span>              |
| <span data-ttu-id="5e992-441">Én</span><span class="sxs-lookup"><span data-stu-id="5e992-441">Single</span></span>                 | <span data-ttu-id="5e992-442">Én</span><span class="sxs-lookup"><span data-stu-id="5e992-442">Single</span></span>               |
| <span data-ttu-id="5e992-443">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="5e992-443">Widowed</span></span>                | <span data-ttu-id="5e992-444">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="5e992-444">Widowed</span></span>              |
| <span data-ttu-id="5e992-445">Skilt</span><span class="sxs-lookup"><span data-stu-id="5e992-445">Divorced</span></span>               | <span data-ttu-id="5e992-446">Skilt</span><span class="sxs-lookup"><span data-stu-id="5e992-446">Divorced</span></span>             |
| <span data-ttu-id="5e992-447">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="5e992-447">Registered Partnership</span></span> | <span data-ttu-id="5e992-448">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="5e992-448">Domestic Partnership</span></span> |
| <span data-ttu-id="5e992-449">None</span><span class="sxs-lookup"><span data-stu-id="5e992-449">None</span></span>                   | <span data-ttu-id="5e992-450">None</span><span class="sxs-lookup"><span data-stu-id="5e992-450">None</span></span>                 |
| <span data-ttu-id="5e992-451">Samboer</span><span class="sxs-lookup"><span data-stu-id="5e992-451">Cohabiting</span></span>             | <span data-ttu-id="5e992-452">Samboer</span><span class="sxs-lookup"><span data-stu-id="5e992-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="5e992-453">Kjønn</span><span class="sxs-lookup"><span data-stu-id="5e992-453">Gender</span></span>

<span data-ttu-id="5e992-454">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="5e992-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5e992-455">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="5e992-456">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-456">Talent</span></span>       | <span data-ttu-id="5e992-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="5e992-458">Mann</span><span class="sxs-lookup"><span data-stu-id="5e992-458">Male</span></span>         | <span data-ttu-id="5e992-459">Mann</span><span class="sxs-lookup"><span data-stu-id="5e992-459">Male</span></span>            |
| <span data-ttu-id="5e992-460">Kvinne</span><span class="sxs-lookup"><span data-stu-id="5e992-460">Female</span></span>       | <span data-ttu-id="5e992-461">Kvinne</span><span class="sxs-lookup"><span data-stu-id="5e992-461">Female</span></span>          |
| <span data-ttu-id="5e992-462">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="5e992-462">Non-specific</span></span> | <span data-ttu-id="5e992-463">*Støttes ikke*</span><span class="sxs-lookup"><span data-stu-id="5e992-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="5e992-464">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="5e992-464">Earning codes</span></span>

<span data-ttu-id="5e992-465">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="5e992-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5e992-466">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="5e992-467">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="5e992-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="5e992-468">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="5e992-468">Supported frequencies</span></span>

- <span data-ttu-id="5e992-469">Alle</span><span class="sxs-lookup"><span data-stu-id="5e992-469">All</span></span>
- <span data-ttu-id="5e992-470">HVERBET</span><span class="sxs-lookup"><span data-stu-id="5e992-470">EVERYPAY</span></span>
- <span data-ttu-id="5e992-471">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="5e992-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="5e992-472">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="5e992-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="5e992-473">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="5e992-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="5e992-474">1IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-474">1OFMTH</span></span>
- <span data-ttu-id="5e992-475">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="5e992-475">LASTOFMTH</span></span>
- <span data-ttu-id="5e992-476">2IMDN</span><span class="sxs-lookup"><span data-stu-id="5e992-476">2OFMTH</span></span>
- <span data-ttu-id="5e992-477">3IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-477">3OFMTH</span></span>
- <span data-ttu-id="5e992-478">4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-478">4OFMTH</span></span>
- <span data-ttu-id="5e992-479">5IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-479">5OFMTH</span></span>
- <span data-ttu-id="5e992-480">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-480">1N2OFMTH</span></span>
- <span data-ttu-id="5e992-481">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-481">3N4OFMTH</span></span>
- <span data-ttu-id="5e992-482">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-482">1N3OFMTH</span></span>
- <span data-ttu-id="5e992-483">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-483">1N4OFMTH</span></span>
- <span data-ttu-id="5e992-484">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-484">2N3OFMTH</span></span>
- <span data-ttu-id="5e992-485">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-485">2N4OFMTH</span></span>
- <span data-ttu-id="5e992-486">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="5e992-487">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="5e992-488">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="5e992-489">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="5e992-490">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="5e992-491">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="5e992-492">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="5e992-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="5e992-493">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="5e992-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="5e992-494">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="5e992-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="5e992-495">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="5e992-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="5e992-496">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="5e992-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="5e992-497">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="5e992-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="5e992-498">Adresser</span><span class="sxs-lookup"><span data-stu-id="5e992-498">Addresses</span></span>

<span data-ttu-id="5e992-499">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="5e992-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="5e992-500">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="5e992-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="5e992-501">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-501">Talent</span></span>          | <span data-ttu-id="5e992-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="5e992-503">Land/område</span><span class="sxs-lookup"><span data-stu-id="5e992-503">Country/Region</span></span>  | <span data-ttu-id="5e992-504">Landskode</span><span class="sxs-lookup"><span data-stu-id="5e992-504">Country Code</span></span>          |
| <span data-ttu-id="5e992-505">Postnummer</span><span class="sxs-lookup"><span data-stu-id="5e992-505">Zip/Postal Code</span></span> | <span data-ttu-id="5e992-506">Postnummer</span><span class="sxs-lookup"><span data-stu-id="5e992-506">Postal Code</span></span>           |
| <span data-ttu-id="5e992-507">Delstat</span><span class="sxs-lookup"><span data-stu-id="5e992-507">State</span></span>           | <span data-ttu-id="5e992-508">Statskode</span><span class="sxs-lookup"><span data-stu-id="5e992-508">State Code</span></span>            |
| <span data-ttu-id="5e992-509">By</span><span class="sxs-lookup"><span data-stu-id="5e992-509">City</span></span>            | <span data-ttu-id="5e992-510">By</span><span class="sxs-lookup"><span data-stu-id="5e992-510">City</span></span>                  |
| <span data-ttu-id="5e992-511">Kommune</span><span class="sxs-lookup"><span data-stu-id="5e992-511">County</span></span>          | <span data-ttu-id="5e992-512">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="5e992-512">County (Municipality)</span></span> |
| <span data-ttu-id="5e992-513">Gate</span><span class="sxs-lookup"><span data-stu-id="5e992-513">Street</span></span>          | <span data-ttu-id="5e992-514">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="5e992-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="5e992-515">Avgiftsområder</span><span class="sxs-lookup"><span data-stu-id="5e992-515">Tax regions</span></span>

<span data-ttu-id="5e992-516">Avgiftsområder brukes til å bestemme den gjeldende avgiften som skal brukes ved generering av lønn.</span><span class="sxs-lookup"><span data-stu-id="5e992-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="5e992-517">Avgiftsområder er tilordnet Dayforce som stedsadresser.</span><span class="sxs-lookup"><span data-stu-id="5e992-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="5e992-518">Standard avgiftområde må være knyttet til arbeiderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="5e992-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="5e992-519">Avgiftsområde (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-519">Tax region (required)</span></span>
- <span data-ttu-id="5e992-520">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-520">Country/Region (required)</span></span>
- <span data-ttu-id="5e992-521">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-521">State (required)</span></span>
- <span data-ttu-id="5e992-522">Kommune</span><span class="sxs-lookup"><span data-stu-id="5e992-522">County</span></span> 
- <span data-ttu-id="5e992-523">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="5e992-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="5e992-524">Konfigurere data for å generere lønn i Mexico</span><span class="sxs-lookup"><span data-stu-id="5e992-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="5e992-525">Hvis du skal generere lønn for ansatte i Mexico, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="5e992-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="5e992-526">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="5e992-526">Departments are required on positions.</span></span>
- <span data-ttu-id="5e992-527">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="5e992-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="5e992-528">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="5e992-528">Job types</span></span>

<span data-ttu-id="5e992-529">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="5e992-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="5e992-530">Jobbtype kreves for å kunne behandle lønn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="5e992-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="5e992-531">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="5e992-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="5e992-532">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="5e992-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="5e992-533">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="5e992-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="5e992-534">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="5e992-534">Job type</span></span>   | <span data-ttu-id="5e992-535">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5e992-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="5e992-536">Per time</span><span class="sxs-lookup"><span data-stu-id="5e992-536">Hourly</span></span>     | <span data-ttu-id="5e992-537">MX per time</span><span class="sxs-lookup"><span data-stu-id="5e992-537">MX Hourly</span></span>   |
| <span data-ttu-id="5e992-538">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="5e992-538">Salaried</span></span>   | <span data-ttu-id="5e992-539">MX lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="5e992-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="5e992-540">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="5e992-540">Position types</span></span> 

<span data-ttu-id="5e992-541">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="5e992-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="5e992-542">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="5e992-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="5e992-543">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="5e992-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="5e992-544">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="5e992-544">Position type</span></span>   | <span data-ttu-id="5e992-545">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5e992-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="5e992-546">Heltid</span><span class="sxs-lookup"><span data-stu-id="5e992-546">Full-time</span></span>       | <span data-ttu-id="5e992-547">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="5e992-547">Full time employee</span></span> |
| <span data-ttu-id="5e992-548">Deltid</span><span class="sxs-lookup"><span data-stu-id="5e992-548">Part-time</span></span>       | <span data-ttu-id="5e992-549">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="5e992-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="5e992-550">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="5e992-550">Reason codes</span></span>

<span data-ttu-id="5e992-551">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="5e992-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="5e992-552">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="5e992-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="5e992-553">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="5e992-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="5e992-554">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="5e992-554">Reason code</span></span>            | <span data-ttu-id="5e992-555">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5e992-555">Description</span></span>                    | <span data-ttu-id="5e992-556">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="5e992-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="5e992-557">AVGANGFØRBETALING</span><span class="sxs-lookup"><span data-stu-id="5e992-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="5e992-558">Avgang før første lønn</span><span class="sxs-lookup"><span data-stu-id="5e992-558">Departure before first payroll</span></span> | <span data-ttu-id="5e992-559">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-559">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-560">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="5e992-560">RESIGNATION</span></span>            | <span data-ttu-id="5e992-561">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="5e992-561">Resignation</span></span>                    | <span data-ttu-id="5e992-562">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-562">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-563">PENSJON</span><span class="sxs-lookup"><span data-stu-id="5e992-563">PENSION</span></span>                | <span data-ttu-id="5e992-564">Pensjon</span><span class="sxs-lookup"><span data-stu-id="5e992-564">Pension</span></span>                        | <span data-ttu-id="5e992-565">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-565">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-566">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="5e992-566">TERMINATION</span></span>            | <span data-ttu-id="5e992-567">Avslutning</span><span class="sxs-lookup"><span data-stu-id="5e992-567">Termination</span></span>                    | <span data-ttu-id="5e992-568">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-568">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-569">AVGANGVEDPENSJON</span><span class="sxs-lookup"><span data-stu-id="5e992-569">RETIREMENT</span></span>             | <span data-ttu-id="5e992-570">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="5e992-570">Retirement</span></span>                     | <span data-ttu-id="5e992-571">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-571">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-572">FRAVÆRENDEPERSON</span><span class="sxs-lookup"><span data-stu-id="5e992-572">ABSENTEE</span></span>               | <span data-ttu-id="5e992-573">Fraværende person</span><span class="sxs-lookup"><span data-stu-id="5e992-573">Absentee</span></span>                       | <span data-ttu-id="5e992-574">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-574">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-575">ANNET</span><span class="sxs-lookup"><span data-stu-id="5e992-575">OTHER</span></span>                  | <span data-ttu-id="5e992-576">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="5e992-576">Other Reasons</span></span>                  | <span data-ttu-id="5e992-577">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-577">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-578">STENGNING</span><span class="sxs-lookup"><span data-stu-id="5e992-578">CLOSURE</span></span>                | <span data-ttu-id="5e992-579">Forretning stenger</span><span class="sxs-lookup"><span data-stu-id="5e992-579">Business Closure</span></span>               | <span data-ttu-id="5e992-580">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-580">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-581">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="5e992-581">DEATH</span></span>                  | <span data-ttu-id="5e992-582">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="5e992-582">Death</span></span>                          | <span data-ttu-id="5e992-583">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-583">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-584">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="5e992-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="5e992-585">Permisjon</span><span class="sxs-lookup"><span data-stu-id="5e992-585">Leave of Absence</span></span>               | <span data-ttu-id="5e992-586">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-586">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-587">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="5e992-587">CONTRACTEND</span></span>            | <span data-ttu-id="5e992-588">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="5e992-588">End of Contract</span></span>                | <span data-ttu-id="5e992-589">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="5e992-589">Terminate worker</span></span>     |
| <span data-ttu-id="5e992-590">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="5e992-590">SALARYCHANGE</span></span>           | <span data-ttu-id="5e992-591">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="5e992-591">Change of Salary</span></span>               | <span data-ttu-id="5e992-592">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="5e992-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="5e992-593">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="5e992-593">Terms of employment</span></span>

<span data-ttu-id="5e992-594">Ansettelsesbetingelser brukes til å opprette kategorier for ansettelsesbetingelser.</span><span class="sxs-lookup"><span data-stu-id="5e992-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="5e992-595">Vilkårene tilordnes til Dayforce som ansettelseindikatorverdier.</span><span class="sxs-lookup"><span data-stu-id="5e992-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="5e992-596">Følgende betingelsene for ansettelse og beskrivelser kreves.</span><span class="sxs-lookup"><span data-stu-id="5e992-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="5e992-597">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="5e992-597">Terms of employment</span></span>   | <span data-ttu-id="5e992-598">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5e992-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="5e992-599">Vanlig</span><span class="sxs-lookup"><span data-stu-id="5e992-599">Regular</span></span>               | <span data-ttu-id="5e992-600">Vanlig</span><span class="sxs-lookup"><span data-stu-id="5e992-600">Regular</span></span>     |
| <span data-ttu-id="5e992-601">Direkte</span><span class="sxs-lookup"><span data-stu-id="5e992-601">Direct</span></span>                | <span data-ttu-id="5e992-602">Direkte</span><span class="sxs-lookup"><span data-stu-id="5e992-602">Direct</span></span>      |
| <span data-ttu-id="5e992-603">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="5e992-603">Internship</span></span>            | <span data-ttu-id="5e992-604">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="5e992-604">Internship</span></span>  |
| <span data-ttu-id="5e992-605">Permanent</span><span class="sxs-lookup"><span data-stu-id="5e992-605">Permanent</span></span>             | <span data-ttu-id="5e992-606">Permanent</span><span class="sxs-lookup"><span data-stu-id="5e992-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="5e992-607">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="5e992-607">Marital status</span></span>

<span data-ttu-id="5e992-608">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="5e992-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5e992-609">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="5e992-610">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-610">Talent</span></span>                 | <span data-ttu-id="5e992-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="5e992-612">Gift</span><span class="sxs-lookup"><span data-stu-id="5e992-612">Married</span></span>                | <span data-ttu-id="5e992-613">Gift</span><span class="sxs-lookup"><span data-stu-id="5e992-613">Married</span></span>                   |
| <span data-ttu-id="5e992-614">Én</span><span class="sxs-lookup"><span data-stu-id="5e992-614">Single</span></span>                 | <span data-ttu-id="5e992-615">Én</span><span class="sxs-lookup"><span data-stu-id="5e992-615">Single</span></span>                    |
| <span data-ttu-id="5e992-616">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="5e992-616">Widowed</span></span>                | <span data-ttu-id="5e992-617">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="5e992-617">Widowed</span></span>                   |
| <span data-ttu-id="5e992-618">Skilt</span><span class="sxs-lookup"><span data-stu-id="5e992-618">Divorced</span></span>               | <span data-ttu-id="5e992-619">Skilt</span><span class="sxs-lookup"><span data-stu-id="5e992-619">Divorced</span></span>                  |
| <span data-ttu-id="5e992-620">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="5e992-620">Registered Partnership</span></span> | <span data-ttu-id="5e992-621">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="5e992-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="5e992-622">None</span><span class="sxs-lookup"><span data-stu-id="5e992-622">None</span></span>                   | <span data-ttu-id="5e992-623">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="5e992-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5e992-624">Samboer</span><span class="sxs-lookup"><span data-stu-id="5e992-624">Cohabiting</span></span>             | <span data-ttu-id="5e992-625">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="5e992-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="5e992-626">Kjønn</span><span class="sxs-lookup"><span data-stu-id="5e992-626">Gender</span></span>

<span data-ttu-id="5e992-627">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="5e992-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5e992-628">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="5e992-629">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-629">Talent</span></span>       | <span data-ttu-id="5e992-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="5e992-631">Mann</span><span class="sxs-lookup"><span data-stu-id="5e992-631">Male</span></span>         | <span data-ttu-id="5e992-632">Mann</span><span class="sxs-lookup"><span data-stu-id="5e992-632">Male</span></span>                      |
| <span data-ttu-id="5e992-633">Kvinne</span><span class="sxs-lookup"><span data-stu-id="5e992-633">Female</span></span>       | <span data-ttu-id="5e992-634">Kvinne</span><span class="sxs-lookup"><span data-stu-id="5e992-634">Female</span></span>                    |
| <span data-ttu-id="5e992-635">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="5e992-635">Non-specific</span></span> | <span data-ttu-id="5e992-636">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="5e992-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="5e992-637">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="5e992-637">Payment method</span></span>

<span data-ttu-id="5e992-638">Betalingsmåter gir den ansatte og firmaet en måte å beskrive hvordan ansatte skal betales.</span><span class="sxs-lookup"><span data-stu-id="5e992-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="5e992-639">Betalingsmåter tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="5e992-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5e992-640">Tabellen nedenfor viser hvordan betalingsmåter tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="5e992-641">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-641">Talent</span></span>             | <span data-ttu-id="5e992-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="5e992-643">Kontanter</span><span class="sxs-lookup"><span data-stu-id="5e992-643">Cash</span></span>               | <span data-ttu-id="5e992-644">Kontanter</span><span class="sxs-lookup"><span data-stu-id="5e992-644">Cash</span></span>                      |
| <span data-ttu-id="5e992-645">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="5e992-645">Electronic Payment</span></span> | <span data-ttu-id="5e992-646">Overfør</span><span class="sxs-lookup"><span data-stu-id="5e992-646">Transfer</span></span>                  |
| <span data-ttu-id="5e992-647">Kontroll</span><span class="sxs-lookup"><span data-stu-id="5e992-647">Check</span></span>              | <span data-ttu-id="5e992-648">Sjekk</span><span class="sxs-lookup"><span data-stu-id="5e992-648">Cheque</span></span>                    |
| <span data-ttu-id="5e992-649">Bankoverføring</span><span class="sxs-lookup"><span data-stu-id="5e992-649">Bank Draft</span></span>         | <span data-ttu-id="5e992-650">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="5e992-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5e992-651">Annet</span><span class="sxs-lookup"><span data-stu-id="5e992-651">Other</span></span>              | <span data-ttu-id="5e992-652">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="5e992-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="5e992-653">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="5e992-653">Bank account type</span></span>

<span data-ttu-id="5e992-654">Bankkontotypene brukes for elektroniske betalinger til ansatte.</span><span class="sxs-lookup"><span data-stu-id="5e992-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="5e992-655">Bankkontotypene tilordnes til Dayforce som overføringskontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="5e992-656">Bankkontotypene oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="5e992-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="5e992-657">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-657">Talent</span></span>            | <span data-ttu-id="5e992-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="5e992-659">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="5e992-659">Checking Account</span></span>  | <span data-ttu-id="5e992-660">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="5e992-660">CheckingAccount</span></span>           |
| <span data-ttu-id="5e992-661">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="5e992-661">Payroll Account</span></span>   | <span data-ttu-id="5e992-662">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="5e992-662">PayrollAccount</span></span>            |
| <span data-ttu-id="5e992-663">Sparekonto</span><span class="sxs-lookup"><span data-stu-id="5e992-663">Savings Account</span></span>   | <span data-ttu-id="5e992-664">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="5e992-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5e992-665">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="5e992-665">BankGirot account</span></span> | <span data-ttu-id="5e992-666">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="5e992-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5e992-667">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="5e992-667">PlusGirot account</span></span> | <span data-ttu-id="5e992-668">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="5e992-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="5e992-669">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="5e992-669">Earning codes</span></span>

<span data-ttu-id="5e992-670">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="5e992-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5e992-671">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="5e992-672">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="5e992-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="5e992-673">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="5e992-673">Supported frequencies</span></span>

- <span data-ttu-id="5e992-674">Alle</span><span class="sxs-lookup"><span data-stu-id="5e992-674">All</span></span>
- <span data-ttu-id="5e992-675">HVERBET</span><span class="sxs-lookup"><span data-stu-id="5e992-675">EVERYPAY</span></span>
- <span data-ttu-id="5e992-676">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="5e992-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="5e992-677">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="5e992-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="5e992-678">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="5e992-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="5e992-679">1IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-679">1OFMTH</span></span>
- <span data-ttu-id="5e992-680">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="5e992-680">LASTOFMTH</span></span>
- <span data-ttu-id="5e992-681">2IMDN</span><span class="sxs-lookup"><span data-stu-id="5e992-681">2OFMTH</span></span>
- <span data-ttu-id="5e992-682">3IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-682">3OFMTH</span></span>
- <span data-ttu-id="5e992-683">4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-683">4OFMTH</span></span>
- <span data-ttu-id="5e992-684">5IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-684">5OFMTH</span></span>
- <span data-ttu-id="5e992-685">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-685">1N2OFMTH</span></span>
- <span data-ttu-id="5e992-686">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-686">3N4OFMTH</span></span>
- <span data-ttu-id="5e992-687">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-687">1N3OFMTH</span></span>
- <span data-ttu-id="5e992-688">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-688">1N4OFMTH</span></span>
- <span data-ttu-id="5e992-689">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-689">2N3OFMTH</span></span>
- <span data-ttu-id="5e992-690">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-690">2N4OFMTH</span></span>
- <span data-ttu-id="5e992-691">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="5e992-692">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="5e992-693">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="5e992-694">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="5e992-695">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="5e992-696">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="5e992-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="5e992-697">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="5e992-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="5e992-698">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="5e992-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="5e992-699">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="5e992-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="5e992-700">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="5e992-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="5e992-701">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="5e992-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="5e992-702">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="5e992-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="5e992-703">Adresser</span><span class="sxs-lookup"><span data-stu-id="5e992-703">Addresses</span></span>

<span data-ttu-id="5e992-704">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="5e992-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="5e992-705">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="5e992-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="5e992-706">Talent</span><span class="sxs-lookup"><span data-stu-id="5e992-706">Talent</span></span>              | <span data-ttu-id="5e992-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5e992-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="5e992-708">Land/område</span><span class="sxs-lookup"><span data-stu-id="5e992-708">Country/Region</span></span>      | <span data-ttu-id="5e992-709">Landskode</span><span class="sxs-lookup"><span data-stu-id="5e992-709">Country Code</span></span>          |
| <span data-ttu-id="5e992-710">Postnummer</span><span class="sxs-lookup"><span data-stu-id="5e992-710">Zip/Postal Code</span></span>     | <span data-ttu-id="5e992-711">Postnummer</span><span class="sxs-lookup"><span data-stu-id="5e992-711">Postal Code</span></span>           |
| <span data-ttu-id="5e992-712">Delstat</span><span class="sxs-lookup"><span data-stu-id="5e992-712">State</span></span>               | <span data-ttu-id="5e992-713">Statskode</span><span class="sxs-lookup"><span data-stu-id="5e992-713">State Code</span></span>            |
| <span data-ttu-id="5e992-714">By</span><span class="sxs-lookup"><span data-stu-id="5e992-714">City</span></span>                | <span data-ttu-id="5e992-715">By</span><span class="sxs-lookup"><span data-stu-id="5e992-715">City</span></span>                  |
| <span data-ttu-id="5e992-716">Kommune</span><span class="sxs-lookup"><span data-stu-id="5e992-716">County</span></span>              | <span data-ttu-id="5e992-717">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="5e992-717">County (Municipality)</span></span> |
| <span data-ttu-id="5e992-718">Gate</span><span class="sxs-lookup"><span data-stu-id="5e992-718">Street</span></span>              | <span data-ttu-id="5e992-719">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="5e992-719">Address Line 1</span></span>        |
| <span data-ttu-id="5e992-720">Gatenummer</span><span class="sxs-lookup"><span data-stu-id="5e992-720">Street Number</span></span>       | <span data-ttu-id="5e992-721">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="5e992-721">Address Line 2</span></span>        |
| <span data-ttu-id="5e992-722">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="5e992-722">Building Complement</span></span> | <span data-ttu-id="5e992-723">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="5e992-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="5e992-724">Passnummer</span><span class="sxs-lookup"><span data-stu-id="5e992-724">Passport number</span></span>

<span data-ttu-id="5e992-725">Ansatte kan deklarere passinformasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-725">Employees can declare passport information.</span></span> <span data-ttu-id="5e992-726">Denne informasjonen er av **Pass**-identifikasjonstypen og er integrert i Dayforce som en del av en ansatts Mexico-spesifikke informasjon.</span><span class="sxs-lookup"><span data-stu-id="5e992-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="5e992-727">Identifikasjonstype = "Pass"</span><span class="sxs-lookup"><span data-stu-id="5e992-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="5e992-728">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="5e992-728">Issued Date</span></span>
- <span data-ttu-id="5e992-729">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="5e992-729">Expiration Date</span></span>

<span data-ttu-id="5e992-730">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **Pass**.</span><span class="sxs-lookup"><span data-stu-id="5e992-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="5e992-731">Men bare den gjeldende aktive passoppføringen er integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="5e992-732">Hvis alle passoppføringer er utløpt, er passet som sist ble utstedt, integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5e992-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

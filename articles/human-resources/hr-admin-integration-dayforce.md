---
title: Konfigurere integrasjon med Dayforce
description: Integrasjonen mellom Microsoft Dynamics 365 Human Resources og Ceridian Dayforce bruker flere konfigurasjonstrinn som er beskrevet i denne artikkelen. Du må konfigurere integreringen i både Human Resources og Dayforce før du kan behandle en lønnskjøring.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85e7274b0e9c130e5c3426fd1fff98410f93e49a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010026"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="f34d1-104">Konfigurere integrasjon med Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="f34d1-105">Integrasjonen mellom Microsoft Dynamics 365 Human Resources og Ceridian Dayforce bruker flere konfigurasjonstrinn som er beskrevet i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="f34d1-106">Du må konfigurere integreringen i både Human Resources og Dayforce før du kan behandle en lønnskjøring.</span><span class="sxs-lookup"><span data-stu-id="f34d1-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="f34d1-107">Når du bruker en tjeneste som Dayforce til å fullføre lønnskjøringer, må du aktivere integrering i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f34d1-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="f34d1-108">Integreringen krever bestemte data fra Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f34d1-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="f34d1-109">Derfor må du kontrollere at data som tilordnes til Dayforce, er konfigurert i Human Resources på en måte som støtter integreringen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="f34d1-110">Integrasjonen bruker følgende brede datakategorier:</span><span class="sxs-lookup"><span data-stu-id="f34d1-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="f34d1-111">Personaldata</span><span class="sxs-lookup"><span data-stu-id="f34d1-111">Human resources data</span></span>
- <span data-ttu-id="f34d1-112">Kompensasjonsdata</span><span class="sxs-lookup"><span data-stu-id="f34d1-112">Compensation data</span></span>
- <span data-ttu-id="f34d1-113">Lønnsdata, for eksempel lønnssykluser, lønnsperioder og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="f34d1-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="f34d1-114">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="f34d1-114">Worker data</span></span>

<span data-ttu-id="f34d1-115">Denne artikkelen beskriver trinnene du må følge for å aktivere integreringen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="f34d1-116">Den beskriver også hvilke typer data og konfigurasjonsdetaljer som integreringen krever.</span><span class="sxs-lookup"><span data-stu-id="f34d1-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="f34d1-117">Aktivere integrasjonen</span><span class="sxs-lookup"><span data-stu-id="f34d1-117">Enable the integration</span></span>

<span data-ttu-id="f34d1-118">I Human Resources må du aktivere integreringen og angi konfigurasjonsinformasjonen for å koble til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="f34d1-119">Hvis du vil at økonomimodultransaksjonen som produseres, skal importeres til Microsoft Dynamics 365 Finance, må du også definere en Microsoft Azure-lagringskonto og angi Azure Storage-tilkoblingsstrengen i Finance.</span><span class="sxs-lookup"><span data-stu-id="f34d1-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="f34d1-120">Følg denne fremgangsmåten for å aktivere integrasjonen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f34d1-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="f34d1-121">Velg **Konfigurasjon av integrering** på siden **Systemadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="f34d1-122">Angi sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="f34d1-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="f34d1-123">Angi brukernavnet og passordet til brukeren som skal ha tilgang til sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="f34d1-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="f34d1-124">Test tilkoblingen etter behov, og sett alternativet **Aktiver lønnsintegrering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="f34d1-125">Når integreringen er slått på, opprettes dataeksportpakken og -filene, og frekvensen angis.</span><span class="sxs-lookup"><span data-stu-id="f34d1-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="f34d1-126">Du kan endre denne frekvensen etter behov.</span><span class="sxs-lookup"><span data-stu-id="f34d1-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="f34d1-127">Hvis du vil ha mer informasjon om Azure Storage-kontoer og Azure Storage-tilkoblingsstrenger, kan du se følgende Azure-artikler:</span><span class="sxs-lookup"><span data-stu-id="f34d1-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="f34d1-128">Om Azure Storage-kontoer</span><span class="sxs-lookup"><span data-stu-id="f34d1-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="f34d1-129">Konfigurere Azure Storage-tilkoblingsstrenger</span><span class="sxs-lookup"><span data-stu-id="f34d1-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="f34d1-130">Tekniske detaljer når lønnsintegrasjon er aktivert</span><span class="sxs-lookup"><span data-stu-id="f34d1-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="f34d1-131">Aktivering av lønnsintegrasjonen har to hovedvirkninger:</span><span class="sxs-lookup"><span data-stu-id="f34d1-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="f34d1-132">Det opprettes et dataeksportprosjekt kalt «Eksport av lønnsintegrasjon».</span><span class="sxs-lookup"><span data-stu-id="f34d1-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="f34d1-133">Dette prosjektet inneholder enhetene og feltene som kreves for lønnsintegrasjonen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="f34d1-134">Du kan undersøke prosjektet ved å gå til **Systemadministrasjon**, velge **Databehandling**-flisen og deretter åpne dataprosjektet fra listen over prosjekter.</span><span class="sxs-lookup"><span data-stu-id="f34d1-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="f34d1-135">Denne satsvise jobben utfører dataeksportprosjektet, krypterer den resulterende datapakken og overfører datapakkefilen til SFTP-endepunktet som er konfigurert på skjermen **Konfigurasjon av integrering**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="f34d1-136">Datapakken som overføres til SFTP-endepunktet, krypteres ved hjelp av en nøkkel som er unik for pakken.</span><span class="sxs-lookup"><span data-stu-id="f34d1-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="f34d1-137">Nøkkelen er i et Azure Key Vault som bare Ceridian har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="f34d1-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="f34d1-138">Det går ikke an å dekryptere og undersøke innholdet i datapakken.</span><span class="sxs-lookup"><span data-stu-id="f34d1-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="f34d1-139">Hvis du må undersøke innholdet i datapakken, må du eksportere dataprosjektet «Eksport av lønnsintegrasjon» manuelt, laste det ned, og deretter åpne det.</span><span class="sxs-lookup"><span data-stu-id="f34d1-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="f34d1-140">Pakken verken krypteres eller overføres når du foretar manuell eksport.</span><span class="sxs-lookup"><span data-stu-id="f34d1-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="f34d1-141">Konfigurere dataene dine</span><span class="sxs-lookup"><span data-stu-id="f34d1-141">Configure your data</span></span> 

<span data-ttu-id="f34d1-142">For å behandle lønn må du konfigurere Personaldata i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f34d1-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="f34d1-143">Du må definere organisasjonsdata, for eksempel jobber og stillinger, samt informasjon om fordeler og kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="f34d1-144">Denne informasjonen gir informasjon om ansettelse, lønn og trekk som kreves for å kunne generere lønn for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="f34d1-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="f34d1-145">Personaldata</span><span class="sxs-lookup"><span data-stu-id="f34d1-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="f34d1-146">Fordeler</span><span class="sxs-lookup"><span data-stu-id="f34d1-146">Benefits</span></span> 

<span data-ttu-id="f34d1-147">Personale inneholder verktøy for oppsett og vedlikehold av fordeler, fradrag og arbeiderkompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere.</span><span class="sxs-lookup"><span data-stu-id="f34d1-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="f34d1-148">Når du oppretter fordeler, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="f34d1-149">Fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="f34d1-149">Benefit plans</span></span>

- <span data-ttu-id="f34d1-150">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-150">Plan (required)</span></span>
- <span data-ttu-id="f34d1-151">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-151">Type (required)</span></span>
- <span data-ttu-id="f34d1-152">Lønnsinnvirkning (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-152">Payroll impact (required)</span></span>
- <span data-ttu-id="f34d1-153">Gjenopprett etterskudd</span><span class="sxs-lookup"><span data-stu-id="f34d1-153">Recover arrears</span></span>
- <span data-ttu-id="f34d1-154">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="f34d1-154">Deduction method</span></span>
- <span data-ttu-id="f34d1-155">Fradragsprioritet</span><span class="sxs-lookup"><span data-stu-id="f34d1-155">Deduction priority</span></span>
- <span data-ttu-id="f34d1-156">Begrens periode</span><span class="sxs-lookup"><span data-stu-id="f34d1-156">Limit period</span></span>
- <span data-ttu-id="f34d1-157">Grensebeløp</span><span class="sxs-lookup"><span data-stu-id="f34d1-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="f34d1-158">Fordeler</span><span class="sxs-lookup"><span data-stu-id="f34d1-158">Benefits</span></span>

- <span data-ttu-id="f34d1-159">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-159">Plan (required)</span></span>
- <span data-ttu-id="f34d1-160">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-160">Type (required)</span></span>
- <span data-ttu-id="f34d1-161">Alternativ (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-161">Option (required)</span></span>
- <span data-ttu-id="f34d1-162">Fordel-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-162">Benefit ID (required)</span></span>
- <span data-ttu-id="f34d1-163">Frekvens</span><span class="sxs-lookup"><span data-stu-id="f34d1-163">Frequency</span></span>
- <span data-ttu-id="f34d1-164">Grunnlag</span><span class="sxs-lookup"><span data-stu-id="f34d1-164">Basis</span></span>
- <span data-ttu-id="f34d1-165">Beløp eller sats</span><span class="sxs-lookup"><span data-stu-id="f34d1-165">Amount or rate</span></span>
- <span data-ttu-id="f34d1-166">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="f34d1-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="f34d1-167">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="f34d1-167">Supported frequencies</span></span> 

- <span data-ttu-id="f34d1-168">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="f34d1-168">Weekly</span></span>
- <span data-ttu-id="f34d1-169">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="f34d1-169">Bi-weekly</span></span>
- <span data-ttu-id="f34d1-170">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="f34d1-170">Semi-monthly</span></span>
- <span data-ttu-id="f34d1-171">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f34d1-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="f34d1-172">Støttede grunnlag</span><span class="sxs-lookup"><span data-stu-id="f34d1-172">Supported bases</span></span> 

- <span data-ttu-id="f34d1-173">Fast beløp</span><span class="sxs-lookup"><span data-stu-id="f34d1-173">Fixed amount</span></span>
- <span data-ttu-id="f34d1-174">Prosentandel av inntekter</span><span class="sxs-lookup"><span data-stu-id="f34d1-174">Percent of earnings</span></span>
- <span data-ttu-id="f34d1-175">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="f34d1-175">Productive hours</span></span>

<span data-ttu-id="f34d1-176">Dayforce oppretter følgende fradrag, basert på lønnsinnvirkning som er definert på fordelsplanen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="f34d1-177">Valg i Human Resources</span><span class="sxs-lookup"><span data-stu-id="f34d1-177">Selection in Human Resources</span></span>        | <span data-ttu-id="f34d1-178">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f34d1-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="f34d1-179">None</span></span>                       | <span data-ttu-id="f34d1-180">Ingen fradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="f34d1-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="f34d1-181">Bare fradrag</span><span class="sxs-lookup"><span data-stu-id="f34d1-181">Deduction only</span></span>             | <span data-ttu-id="f34d1-182">Et ansattfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="f34d1-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="f34d1-183">Bare bidrag</span><span class="sxs-lookup"><span data-stu-id="f34d1-183">Contribution only</span></span>          | <span data-ttu-id="f34d1-184">Et arbeidsgiverfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="f34d1-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="f34d1-185">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="f34d1-185">Deduction and contribution</span></span> | <span data-ttu-id="f34d1-186">Fradrag for ansatte og arbeidsgivere opprettes.</span><span class="sxs-lookup"><span data-stu-id="f34d1-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="f34d1-187">Hvis du vil ha mer informasjon om hvordan du definerer og administrerer et program for fordeler, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="f34d1-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="f34d1-188">Levere et program for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="f34d1-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="f34d1-189">Opprett en ny fordel</span><span class="sxs-lookup"><span data-stu-id="f34d1-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="f34d1-190">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="f34d1-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="f34d1-191">Registrere og fjerne fordeler fra arbeidere</span><span class="sxs-lookup"><span data-stu-id="f34d1-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="f34d1-192">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-192">Compensation</span></span> 

<span data-ttu-id="f34d1-193">Kompensasjonsstyring brukes til å kontrollere levering av grunnlønn og bonuser.</span><span class="sxs-lookup"><span data-stu-id="f34d1-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="f34d1-194">En ansatts faste grunnlønn og personlige tilleggsøkninger styres via faste kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="f34d1-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="f34d1-195">Betaling av insitamentutbetalinger, for eksempel bonuser, ytelsestillegg, aksjeopsjoner og tilskudd, og også engangsbonuser, kontrolleres via variable kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="f34d1-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="f34d1-196">Dayforce bruker kompensasjonsinformasjon til å beregne timesats eller årlig sats for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="f34d1-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="f34d1-197">Planer for faste kompensasjoner og konverteringer av lønnssats er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="f34d1-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="f34d1-198">Ansatte må tilknyttes en plan for fast kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="f34d1-199">Hvis du vil ha mer informasjon om kompensasjonsplaner, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="f34d1-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="f34d1-200">Opprette planer for fast kompensasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="f34d1-201">Opprette variable kompensasjonsplaner</span><span class="sxs-lookup"><span data-stu-id="f34d1-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="f34d1-202">Utvikle struktur og planer for lønn/kompensasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="f34d1-203">Behandle kompensasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="f34d1-204">Definere kompensasjonsprosess og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="f34d1-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="f34d1-205">Registrere en ansatt i en fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="f34d1-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="f34d1-206">Registrere en ansatt i en variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="f34d1-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="f34d1-207">Jobber</span><span class="sxs-lookup"><span data-stu-id="f34d1-207">Jobs</span></span> 

<span data-ttu-id="f34d1-208">En jobb er en samling oppgaver og ansvarsområder som kreves av en person som utfører en jobb.</span><span class="sxs-lookup"><span data-stu-id="f34d1-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="f34d1-209">Hvis du vil ha mer informasjon, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="f34d1-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="f34d1-210">Definere komponentene for en jobb</span><span class="sxs-lookup"><span data-stu-id="f34d1-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="f34d1-211">Definere nye jobber</span><span class="sxs-lookup"><span data-stu-id="f34d1-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="f34d1-212">Stillinger</span><span class="sxs-lookup"><span data-stu-id="f34d1-212">Positions</span></span>

<span data-ttu-id="f34d1-213">En stilling er én enkeltforekomst av en jobb.</span><span class="sxs-lookup"><span data-stu-id="f34d1-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="f34d1-214">"Salgssjef (øst)"-stillingen er for eksempel én av stillingene som er knyttet til jobben "Salgssjef".</span><span class="sxs-lookup"><span data-stu-id="f34d1-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="f34d1-215">Det finnes en stilling i en avdeling.</span><span class="sxs-lookup"><span data-stu-id="f34d1-215">A position exists in a department.</span></span> <span data-ttu-id="f34d1-216">Bare én arbeider kan være tilknyttet hvert område.</span><span class="sxs-lookup"><span data-stu-id="f34d1-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="f34d1-217">Ha følgende data og konfigurasjon i bakhodet når du definerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="f34d1-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="f34d1-218">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-218">Position (required)</span></span>
- <span data-ttu-id="f34d1-219">Beskrivelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-219">Description (required)</span></span>
- <span data-ttu-id="f34d1-220">Jobb (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-220">Job (required)</span></span>
- <span data-ttu-id="f34d1-221">Avdeling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-221">Department (required)</span></span>
- <span data-ttu-id="f34d1-222">Stillingstype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-222">Position type (required)</span></span>
- <span data-ttu-id="f34d1-223">Fulltidsekvivalent</span><span class="sxs-lookup"><span data-stu-id="f34d1-223">Full-time equivalent</span></span>
- <span data-ttu-id="f34d1-224">Årlige vanlige timer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="f34d1-225">Betalt av juridisk enhet (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="f34d1-226">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-226">Pay cycle (required)</span></span>
- <span data-ttu-id="f34d1-227">Standard finansdimensjon – kostsenter (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="f34d1-228">Arbeidertilordning – arbeider, start for tilordning, slutt for tilordning, årsakskode</span><span class="sxs-lookup"><span data-stu-id="f34d1-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="f34d1-229">Hvis flere stillinger i samme avdeling er knyttet til den samme jobben, konsolideres de til én stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="f34d1-230">Hvis du vil ha mer informasjon, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="f34d1-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="f34d1-231">Organisere arbeidsstyrken ved bruk av avdelinger, jobber og stillinger</span><span class="sxs-lookup"><span data-stu-id="f34d1-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="f34d1-232">Definere stillinger</span><span class="sxs-lookup"><span data-stu-id="f34d1-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="f34d1-233">Avdelinger</span><span class="sxs-lookup"><span data-stu-id="f34d1-233">Departments</span></span>

<span data-ttu-id="f34d1-234">En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="f34d1-235">En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale.</span><span class="sxs-lookup"><span data-stu-id="f34d1-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="f34d1-236">Du kan bruke avdelinger til å rapportere om funksjonsområder.</span><span class="sxs-lookup"><span data-stu-id="f34d1-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="f34d1-237">Avdelinger kan ha ansvar for fortjeneste og tap.</span><span class="sxs-lookup"><span data-stu-id="f34d1-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="f34d1-238">Hvis du vil ha mer informasjon, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="f34d1-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="f34d1-239">Opprette en avdeling og knytte den til avdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="f34d1-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="f34d1-240">Definere nye avdelinger</span><span class="sxs-lookup"><span data-stu-id="f34d1-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="f34d1-241">Lønnssykluser og lønnsperioder</span><span class="sxs-lookup"><span data-stu-id="f34d1-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="f34d1-242">En betalingssyklus avgjør hvor ofte lønnskjøring utføres, og de spesifikke dagene arbeidere lønnes.</span><span class="sxs-lookup"><span data-stu-id="f34d1-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="f34d1-243">For eksempel kan en lønnssyklus være månedlig, og ansatte kan betales på den siste dagen i måneden.</span><span class="sxs-lookup"><span data-stu-id="f34d1-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="f34d1-244">En lønnssyklus kan også være ukentlig, og ansatte kan betales tirsdagen etter slutten av lønnsperioden.</span><span class="sxs-lookup"><span data-stu-id="f34d1-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="f34d1-245">Lønnssykluser tilordnes til stillinger for å styre når arbeidere i disse stillingene lønnes.</span><span class="sxs-lookup"><span data-stu-id="f34d1-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="f34d1-246">Når du oppretter lønnssykler, kan du generere lønnsperioder for hver enkelt syklus.</span><span class="sxs-lookup"><span data-stu-id="f34d1-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="f34d1-247">Hver lønnsperiode inkluderer en standard betalingsdato som er basert på informasjonen du angir.</span><span class="sxs-lookup"><span data-stu-id="f34d1-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="f34d1-248">Du kan imidlertid endre standard betalingsdato i en lønnsperiode for å tillate unntak, for eksempel når betalingsdatoen faller på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="f34d1-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="f34d1-249">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f34d1-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f34d1-250">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-250">Pay cycle (required)</span></span>
- <span data-ttu-id="f34d1-251">Lønnssyklusfrekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="f34d1-252">Periodens startdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="f34d1-253">Standard betalingsdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="f34d1-254">Denne informasjonen er integrert med Dayforce som lønnsgrupper og er inndelt etter land eller område for hver lønnssyklus.</span><span class="sxs-lookup"><span data-stu-id="f34d1-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="f34d1-255">Minst én lønnsperiode må genereres før integrasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="f34d1-256">Dayforce genererer lønnsgruppekalendere og betalingsdatoer basert på startdatoen for den første lønnsperioden og standard betalingsdato som er definert i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f34d1-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="f34d1-257">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="f34d1-257">Earning codes</span></span>

<span data-ttu-id="f34d1-258">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="f34d1-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f34d1-259">Kodene har forskjellige parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="f34d1-260">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="f34d1-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f34d1-261">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-261">Earning Code (required)</span></span>
- <span data-ttu-id="f34d1-262">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-262">Description</span></span>
- <span data-ttu-id="f34d1-263">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="f34d1-263">Unit of measure</span></span>
- <span data-ttu-id="f34d1-264">Produktiv</span><span class="sxs-lookup"><span data-stu-id="f34d1-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="f34d1-265">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="f34d1-265">Worker data</span></span>

<span data-ttu-id="f34d1-266">Poster for ulike typer arbeidere som du har, er viktig for personal. og lønnsystemene dine.</span><span class="sxs-lookup"><span data-stu-id="f34d1-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="f34d1-267">Informasjonen du legger inn, kan brukes til å spore arbeidere og personlig informasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="f34d1-268">Du kan vedlikeholde følgende informasjon om arbeidere:</span><span class="sxs-lookup"><span data-stu-id="f34d1-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="f34d1-269">**Grunnleggende** – Vedlikehold grunnleggende informasjon om en arbeider, for eksempel kontaktinformasjon, demografisk informasjon, identifikasjonsinformasjon, familieinformasjon, militærtjenestestatus, informasjon om personer som bor i utlandet, og personlige kontakter og kontakter i nødfall.</span><span class="sxs-lookup"><span data-stu-id="f34d1-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="f34d1-270">**Ansettelse** – Vedlikehold informasjon om en arbeiders ansettelse, for eksempel informasjon om firma- eller organisasjonstilknytning, stillingstilordning, start- og sluttdatoer, arbeidstillatelse, vilkår for ansettelse, pensjon, ferie og flytting.</span><span class="sxs-lookup"><span data-stu-id="f34d1-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="f34d1-271">**Lønn og fravær** – Vedlikehold opplysninger om en arbeiders fravær, for eksempel arbeidskalendere, fraværstransaksjoner og fraværsoppsett.</span><span class="sxs-lookup"><span data-stu-id="f34d1-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="f34d1-272">**Kompensasjon og lønn** – Vedlikehold informasjon om en arbeiders kompensasjonsplaner og lønn, for eksempel planregistrering, priser, ytelse, provisjon, avgiftsinformasjon, pensjonering og lønnstrekk.</span><span class="sxs-lookup"><span data-stu-id="f34d1-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="f34d1-273">Når du legger inn arbeiderinformasjon, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="f34d1-274">Generell informasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-274">General information</span></span>

- <span data-ttu-id="f34d1-275">Personalnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-275">Personnel number (required)</span></span>
- <span data-ttu-id="f34d1-276">Fornavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-276">First name (required)</span></span>
- <span data-ttu-id="f34d1-277">Etternavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-277">Last name (required)</span></span>
- <span data-ttu-id="f34d1-278">Mellomnavn</span><span class="sxs-lookup"><span data-stu-id="f34d1-278">Middle name</span></span>
- <span data-ttu-id="f34d1-279">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-279">Seniority date</span></span>
- <span data-ttu-id="f34d1-280">Kalt</span><span class="sxs-lookup"><span data-stu-id="f34d1-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="f34d1-281">Personlige opplysninger</span><span class="sxs-lookup"><span data-stu-id="f34d1-281">Personal information</span></span>

- <span data-ttu-id="f34d1-282">Sivilstand (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-282">Marital status (required)</span></span>
- <span data-ttu-id="f34d1-283">Fødselsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-283">Birth date (required)</span></span>
- <span data-ttu-id="f34d1-284">Kjønn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-284">Gender (required)</span></span>
- <span data-ttu-id="f34d1-285">Person med funksjonshemminger</span><span class="sxs-lookup"><span data-stu-id="f34d1-285">Person with disabilities</span></span>
- <span data-ttu-id="f34d1-286">Nasjonalitet land/område (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="f34d1-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="f34d1-287">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="f34d1-287">Address information</span></span>

- <span data-ttu-id="f34d1-288">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-288">Primary (required)</span></span>
- <span data-ttu-id="f34d1-289">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-289">Country/region (required)</span></span>
- <span data-ttu-id="f34d1-290">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-290">Postal code (required)</span></span>
- <span data-ttu-id="f34d1-291">Gatenummer (obligatorisk) (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="f34d1-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="f34d1-292">Bygningsnavn (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="f34d1-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="f34d1-293">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-293">City (required)</span></span>
- <span data-ttu-id="f34d1-294">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-294">State (required)</span></span>
- <span data-ttu-id="f34d1-295">Land (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="f34d1-296">Kontaktinformasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-296">Contact information</span></span> 

- <span data-ttu-id="f34d1-297">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-297">Primary (required)</span></span>
- <span data-ttu-id="f34d1-298">Kontaktnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-298">Contact number (required)</span></span>
- <span data-ttu-id="f34d1-299">Utvidelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="f34d1-300">Lønnsinformasjon og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="f34d1-300">Payroll information and earning codes</span></span>

<span data-ttu-id="f34d1-301">Ansatte kan tilordnes spesifikke inntekter med en gitt betalingfrekvens og med en foretrukket betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="f34d1-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="f34d1-302">Følgende felt brukes i Dayforce for å sørge for at disse valgene og innstillingene brukes.</span><span class="sxs-lookup"><span data-stu-id="f34d1-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="f34d1-303">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="f34d1-303">Earning codes</span></span>

- <span data-ttu-id="f34d1-304">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-304">Position (required)</span></span>
- <span data-ttu-id="f34d1-305">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-305">Earning Code (required)</span></span>
- <span data-ttu-id="f34d1-306">Frekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-306">Frequency (required)</span></span>
- <span data-ttu-id="f34d1-307">Beløp (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="f34d1-308">Lønnsinformasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-308">Payroll information</span></span>

- <span data-ttu-id="f34d1-309">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="f34d1-309">Payment Method</span></span>
- <span data-ttu-id="f34d1-310">Økonomisk område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-310">Economic Region (required)</span></span>
- <span data-ttu-id="f34d1-311">ID for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="f34d1-311">Employee Benefits ID</span></span>
- <span data-ttu-id="f34d1-312">Nasjonalt ID-nummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-312">National ID Number (required)</span></span>
- <span data-ttu-id="f34d1-313">Militærtjenestenummer</span><span class="sxs-lookup"><span data-stu-id="f34d1-313">Military Service Number</span></span>
- <span data-ttu-id="f34d1-314">Skift-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-314">Shift ID (required)</span></span>
- <span data-ttu-id="f34d1-315">Avgiftsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-315">Tax Number (required)</span></span>
- <span data-ttu-id="f34d1-316">Fagforenings-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-316">Union ID (required)</span></span>
- <span data-ttu-id="f34d1-317">Arbeidsdag-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-317">Work Day ID (required)</span></span>
- <span data-ttu-id="f34d1-318">Arbeidstillatelsesnummer</span><span class="sxs-lookup"><span data-stu-id="f34d1-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="f34d1-319">Når det gjelder betalingsmåte støtter Mexico **Kontanter**, **Sjekk** (firmaets fysisk sjekk) og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="f34d1-320">Hvis betalingsmåte ikke er angitt, brukes **Sjekk** som standard.</span><span class="sxs-lookup"><span data-stu-id="f34d1-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="f34d1-321">Ansettelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="f34d1-321">Employment details</span></span>

<span data-ttu-id="f34d1-322">Ansettelsesdetaljhistorikk brukes som nøkkelinformasjon til å avlede en ansatts ansettelse-, oppsigelses- og nyansettelsesstatuser i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="f34d1-323">Dayforce støtter bare én aktiv ansettelsespost om gangen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="f34d1-324">Startdato for ansettelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-324">Employment start date (required)</span></span>
- <span data-ttu-id="f34d1-325">Sluttdato for ansettelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-325">Employment end date</span></span>
- <span data-ttu-id="f34d1-326">Startdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-326">Start date</span></span>
- <span data-ttu-id="f34d1-327">Justert startdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-327">Adjusted start date</span></span>
- <span data-ttu-id="f34d1-328">Avslutningsdato (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="f34d1-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="f34d1-329">Avslutningsårsak (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="f34d1-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="f34d1-330">En ansatts nøkkeldatoer avledes ved å bruke følgende informasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="f34d1-331">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-331">Human Resources</span></span>                | <span data-ttu-id="f34d1-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f34d1-333">Den siste ansettelsesdatoen</span><span class="sxs-lookup"><span data-stu-id="f34d1-333">Most recent hire date</span></span> | <span data-ttu-id="f34d1-334">Ansettelsesstart for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="f34d1-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f34d1-335">Avslutningsdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-335">Termination date</span></span>      | <span data-ttu-id="f34d1-336">Avslutningsdato for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="f34d1-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f34d1-337">Startdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-337">Start date</span></span>            | <span data-ttu-id="f34d1-338">Justert startdato, startdato eller ansettelsesstart for gjeldende ikke-aktive ansettelseloggpost</span><span class="sxs-lookup"><span data-stu-id="f34d1-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="f34d1-339">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-339">Original hire date</span></span>    | <span data-ttu-id="f34d1-340">Ansettelsesstart for tidligste ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="f34d1-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="f34d1-341">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-341">Compensation</span></span>

<span data-ttu-id="f34d1-342">En fast kompensasjonsplan må være knyttet til hver ansatts primære stilling i en ansattperiode.</span><span class="sxs-lookup"><span data-stu-id="f34d1-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="f34d1-343">Denne perioden begynner på datoen da den ansatte ble ansatt (eller startdatoen for ansettelsen), og fortsetter til avslutning.</span><span class="sxs-lookup"><span data-stu-id="f34d1-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="f34d1-344">Gyldighetsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-344">Effective Date (required)</span></span>
- <span data-ttu-id="f34d1-345">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-345">Expiration date</span></span>
- <span data-ttu-id="f34d1-346">Lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-346">Pay Rate (required)</span></span>
- <span data-ttu-id="f34d1-347">Konverteringer av lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="f34d1-348">Tilsvarende årlig (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="f34d1-349">Tilsvarende per time (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="f34d1-350">Hvis en timebaserte ansatt har flere stillinger, importeres fast kompensasjon for den primære stillingen til Dayforce som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="f34d1-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="f34d1-351">For ikke-primære stillinger lagres timeprisen til den tilsvarende stillingen i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="f34d1-352">Hvis en lønnsansatt har flere stillinger, avledes kumulativ timepris og årslønn på tvers av alle aktive stillinger og brukes som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="f34d1-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="f34d1-353">Identifikasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="f34d1-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="f34d1-354">Personnummeridentifikator</span><span class="sxs-lookup"><span data-stu-id="f34d1-354">Social Security identifier</span></span> 

<span data-ttu-id="f34d1-355">Alle ansatte må ha én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="f34d1-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="f34d1-356">Identifikatoren må være av identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="f34d1-357">I Dayforce hentes den automatisk som den ansattes personnummeridentifikator som kreves for ansettelse.</span><span class="sxs-lookup"><span data-stu-id="f34d1-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="f34d1-358">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-358">Primary (required)</span></span>
- <span data-ttu-id="f34d1-359">Identifikasjonstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="f34d1-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="f34d1-360">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-360">Issued Date</span></span>
- <span data-ttu-id="f34d1-361">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-361">Expiration Date</span></span>

<span data-ttu-id="f34d1-362">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="f34d1-363">Det er imidlertid bare posten som er merket som **Primær**, som er integrert i Dayforce, uansett om nummeret er aktivt eller utløpt.</span><span class="sxs-lookup"><span data-stu-id="f34d1-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="f34d1-364">Bankkontoer og -utlegg</span><span class="sxs-lookup"><span data-stu-id="f34d1-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="f34d1-365">Gyldig bankkontoinformasjon må angis for alle ansatte som velger å betales via bankkontooverføringer.</span><span class="sxs-lookup"><span data-stu-id="f34d1-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="f34d1-366">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-366">Human Resources</span></span>                         | <span data-ttu-id="f34d1-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f34d1-368">Bankkontonummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="f34d1-369">SWIFT-kode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-369">SWIFT code (required)</span></span>          | <span data-ttu-id="f34d1-370">**Bank-ID**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="f34d1-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="f34d1-371">Avdelingsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="f34d1-372">Bankkontotype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-372">Bank account type (required)</span></span>   | <span data-ttu-id="f34d1-373">**Kontotoype**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="f34d1-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="f34d1-374">Støttede verdier inkluderer **Kontroll** og **Lønn**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="f34d1-375">Ansatte som velger å betales via bankkontooverføringer, må oppgi en kobling til en restkonto som er under en juridisk enhet som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en meksikansk bank.</span><span class="sxs-lookup"><span data-stu-id="f34d1-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="f34d1-376">Alle andre ikke-restkontoer ignoreres.</span><span class="sxs-lookup"><span data-stu-id="f34d1-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="f34d1-377">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="f34d1-377">Address information</span></span>

<span data-ttu-id="f34d1-378">Alle ansatte må ha ett primært sted.</span><span class="sxs-lookup"><span data-stu-id="f34d1-378">Every employee must have one primary location.</span></span> <span data-ttu-id="f34d1-379">I Dayforce brukes dette stedet til å fastslå den ansattes primære bosted for skatte- og avgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="f34d1-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="f34d1-380">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-380">Primary (required)</span></span>
- <span data-ttu-id="f34d1-381">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-381">Country/region (required)</span></span>
- <span data-ttu-id="f34d1-382">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="f34d1-383">Gate (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-383">Street (required)</span></span>
- <span data-ttu-id="f34d1-384">Gatenummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-384">Street Number (required)</span></span>
- <span data-ttu-id="f34d1-385">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="f34d1-385">Building Complement</span></span>
- <span data-ttu-id="f34d1-386">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-386">City (required)</span></span>
- <span data-ttu-id="f34d1-387">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-387">State (required)</span></span>
- <span data-ttu-id="f34d1-388">Land (oblitagorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="f34d1-389">Konfigurer dataene for å generere lønn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="f34d1-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="f34d1-390">Hvis du skal generere lønn for ansatte i USA og Canada, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="f34d1-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="f34d1-391">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="f34d1-391">Departments are required on positions.</span></span>
- <span data-ttu-id="f34d1-392">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="f34d1-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="f34d1-393">Du kan konfigurere Human Resources slik at det kreves at stillinger spesifiserer en avdeling.</span><span class="sxs-lookup"><span data-stu-id="f34d1-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="f34d1-394">For å gjøre dette går du til **HR delte stillinger > Stillinger > Avdelinger må oppgis for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="f34d1-395">Vi anbefaler at denne innstillingen iverksettes for integreringen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="f34d1-396">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="f34d1-396">Job types</span></span>

<span data-ttu-id="f34d1-397">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="f34d1-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f34d1-398">Jobbtyper kreves for å kunne behandle lønn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="f34d1-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="f34d1-399">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="f34d1-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f34d1-400">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="f34d1-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f34d1-401">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="f34d1-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f34d1-402">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="f34d1-402">Job type</span></span>   | <span data-ttu-id="f34d1-403">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f34d1-404">Per time</span><span class="sxs-lookup"><span data-stu-id="f34d1-404">Hourly</span></span>     | <span data-ttu-id="f34d1-405">Per time</span><span class="sxs-lookup"><span data-stu-id="f34d1-405">Hourly</span></span>      |
| <span data-ttu-id="f34d1-406">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="f34d1-406">Salaried</span></span>   | <span data-ttu-id="f34d1-407">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="f34d1-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="f34d1-408">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="f34d1-408">Position types</span></span> 

<span data-ttu-id="f34d1-409">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="f34d1-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f34d1-410">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="f34d1-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f34d1-411">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="f34d1-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f34d1-412">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="f34d1-412">Position type</span></span>   | <span data-ttu-id="f34d1-413">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f34d1-414">Heltid</span><span class="sxs-lookup"><span data-stu-id="f34d1-414">Full-time</span></span>       | <span data-ttu-id="f34d1-415">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="f34d1-415">Full time employee</span></span> |
| <span data-ttu-id="f34d1-416">Deltid</span><span class="sxs-lookup"><span data-stu-id="f34d1-416">Part-time</span></span>       | <span data-ttu-id="f34d1-417">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="f34d1-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f34d1-418">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="f34d1-418">Reason codes</span></span>

<span data-ttu-id="f34d1-419">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="f34d1-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f34d1-420">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="f34d1-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f34d1-421">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="f34d1-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f34d1-422">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="f34d1-422">Reason code</span></span>    | <span data-ttu-id="f34d1-423">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-423">Description</span></span>      | <span data-ttu-id="f34d1-424">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="f34d1-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="f34d1-425">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="f34d1-425">RESIGNATION</span></span>    | <span data-ttu-id="f34d1-426">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-426">Resignation</span></span>      | <span data-ttu-id="f34d1-427">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-427">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-428">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="f34d1-428">TERMINATION</span></span>    | <span data-ttu-id="f34d1-429">Avslutning</span><span class="sxs-lookup"><span data-stu-id="f34d1-429">Termination</span></span>      | <span data-ttu-id="f34d1-430">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-430">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-431">AVGANG VED PENSJON</span><span class="sxs-lookup"><span data-stu-id="f34d1-431">RETIREMENT</span></span>     | <span data-ttu-id="f34d1-432">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-432">Retirement</span></span>       | <span data-ttu-id="f34d1-433">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-433">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-434">ANNET</span><span class="sxs-lookup"><span data-stu-id="f34d1-434">OTHER</span></span>          | <span data-ttu-id="f34d1-435">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="f34d1-435">Other Reasons</span></span>    | <span data-ttu-id="f34d1-436">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-436">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-437">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="f34d1-437">DEATH</span></span>          | <span data-ttu-id="f34d1-438">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="f34d1-438">Death</span></span>            | <span data-ttu-id="f34d1-439">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-439">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-440">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="f34d1-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="f34d1-441">Permisjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-441">Leave of Absence</span></span> | <span data-ttu-id="f34d1-442">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-442">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-443">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="f34d1-443">CONTRACTEND</span></span>    | <span data-ttu-id="f34d1-444">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="f34d1-444">End of Contract</span></span>  | <span data-ttu-id="f34d1-445">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-445">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-446">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="f34d1-446">SALARYCHANGE</span></span>   | <span data-ttu-id="f34d1-447">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="f34d1-447">Change of Salary</span></span> | <span data-ttu-id="f34d1-448">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="f34d1-449">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="f34d1-449">Marital status</span></span>

<span data-ttu-id="f34d1-450">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="f34d1-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f34d1-451">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f34d1-452">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-452">Human Resources</span></span>                 | <span data-ttu-id="f34d1-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="f34d1-454">Gift</span><span class="sxs-lookup"><span data-stu-id="f34d1-454">Married</span></span>                | <span data-ttu-id="f34d1-455">Gift</span><span class="sxs-lookup"><span data-stu-id="f34d1-455">Married</span></span>              |
| <span data-ttu-id="f34d1-456">Ugift</span><span class="sxs-lookup"><span data-stu-id="f34d1-456">Single</span></span>                 | <span data-ttu-id="f34d1-457">Ugift</span><span class="sxs-lookup"><span data-stu-id="f34d1-457">Single</span></span>               |
| <span data-ttu-id="f34d1-458">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="f34d1-458">Widowed</span></span>                | <span data-ttu-id="f34d1-459">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="f34d1-459">Widowed</span></span>              |
| <span data-ttu-id="f34d1-460">Skilt</span><span class="sxs-lookup"><span data-stu-id="f34d1-460">Divorced</span></span>               | <span data-ttu-id="f34d1-461">Skilt</span><span class="sxs-lookup"><span data-stu-id="f34d1-461">Divorced</span></span>             |
| <span data-ttu-id="f34d1-462">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="f34d1-462">Registered Partnership</span></span> | <span data-ttu-id="f34d1-463">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="f34d1-463">Domestic Partnership</span></span> |
| <span data-ttu-id="f34d1-464">None</span><span class="sxs-lookup"><span data-stu-id="f34d1-464">None</span></span>                   | <span data-ttu-id="f34d1-465">None</span><span class="sxs-lookup"><span data-stu-id="f34d1-465">None</span></span>                 |
| <span data-ttu-id="f34d1-466">Samboer</span><span class="sxs-lookup"><span data-stu-id="f34d1-466">Cohabiting</span></span>             | <span data-ttu-id="f34d1-467">Samboer</span><span class="sxs-lookup"><span data-stu-id="f34d1-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="f34d1-468">Kjønn</span><span class="sxs-lookup"><span data-stu-id="f34d1-468">Gender</span></span>

<span data-ttu-id="f34d1-469">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="f34d1-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f34d1-470">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f34d1-471">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-471">Human Resources</span></span>       | <span data-ttu-id="f34d1-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="f34d1-473">Mann</span><span class="sxs-lookup"><span data-stu-id="f34d1-473">Male</span></span>         | <span data-ttu-id="f34d1-474">Mann</span><span class="sxs-lookup"><span data-stu-id="f34d1-474">Male</span></span>            |
| <span data-ttu-id="f34d1-475">Kvinne</span><span class="sxs-lookup"><span data-stu-id="f34d1-475">Female</span></span>       | <span data-ttu-id="f34d1-476">Kvinne</span><span class="sxs-lookup"><span data-stu-id="f34d1-476">Female</span></span>          |
| <span data-ttu-id="f34d1-477">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="f34d1-477">Non-specific</span></span> | <span data-ttu-id="f34d1-478">*Støttes ikke*</span><span class="sxs-lookup"><span data-stu-id="f34d1-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f34d1-479">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="f34d1-479">Earning codes</span></span>

<span data-ttu-id="f34d1-480">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="f34d1-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f34d1-481">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f34d1-482">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f34d1-483">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="f34d1-483">Supported frequencies</span></span>

- <span data-ttu-id="f34d1-484">Alle</span><span class="sxs-lookup"><span data-stu-id="f34d1-484">All</span></span>
- <span data-ttu-id="f34d1-485">HVERBET</span><span class="sxs-lookup"><span data-stu-id="f34d1-485">EVERYPAY</span></span>
- <span data-ttu-id="f34d1-486">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="f34d1-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f34d1-487">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="f34d1-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f34d1-488">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="f34d1-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f34d1-489">1IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-489">1OFMTH</span></span>
- <span data-ttu-id="f34d1-490">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-490">LASTOFMTH</span></span>
- <span data-ttu-id="f34d1-491">2IMDN</span><span class="sxs-lookup"><span data-stu-id="f34d1-491">2OFMTH</span></span>
- <span data-ttu-id="f34d1-492">3IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-492">3OFMTH</span></span>
- <span data-ttu-id="f34d1-493">4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-493">4OFMTH</span></span>
- <span data-ttu-id="f34d1-494">5IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-494">5OFMTH</span></span>
- <span data-ttu-id="f34d1-495">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-495">1N2OFMTH</span></span>
- <span data-ttu-id="f34d1-496">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-496">3N4OFMTH</span></span>
- <span data-ttu-id="f34d1-497">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-497">1N3OFMTH</span></span>
- <span data-ttu-id="f34d1-498">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-498">1N4OFMTH</span></span>
- <span data-ttu-id="f34d1-499">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-499">2N3OFMTH</span></span>
- <span data-ttu-id="f34d1-500">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-500">2N4OFMTH</span></span>
- <span data-ttu-id="f34d1-501">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="f34d1-502">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="f34d1-503">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="f34d1-504">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="f34d1-505">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f34d1-506">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f34d1-507">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="f34d1-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f34d1-508">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="f34d1-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f34d1-509">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="f34d1-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f34d1-510">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="f34d1-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f34d1-511">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="f34d1-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f34d1-512">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="f34d1-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f34d1-513">Adresser</span><span class="sxs-lookup"><span data-stu-id="f34d1-513">Addresses</span></span>

<span data-ttu-id="f34d1-514">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="f34d1-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f34d1-515">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="f34d1-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f34d1-516">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-516">Human Resources</span></span>          | <span data-ttu-id="f34d1-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="f34d1-518">Land/område</span><span class="sxs-lookup"><span data-stu-id="f34d1-518">Country/Region</span></span>  | <span data-ttu-id="f34d1-519">Landskode</span><span class="sxs-lookup"><span data-stu-id="f34d1-519">Country Code</span></span>          |
| <span data-ttu-id="f34d1-520">Postnummer</span><span class="sxs-lookup"><span data-stu-id="f34d1-520">Zip/Postal Code</span></span> | <span data-ttu-id="f34d1-521">Postnummer</span><span class="sxs-lookup"><span data-stu-id="f34d1-521">Postal Code</span></span>           |
| <span data-ttu-id="f34d1-522">Delstat</span><span class="sxs-lookup"><span data-stu-id="f34d1-522">State</span></span>           | <span data-ttu-id="f34d1-523">Statskode</span><span class="sxs-lookup"><span data-stu-id="f34d1-523">State Code</span></span>            |
| <span data-ttu-id="f34d1-524">By</span><span class="sxs-lookup"><span data-stu-id="f34d1-524">City</span></span>            | <span data-ttu-id="f34d1-525">By</span><span class="sxs-lookup"><span data-stu-id="f34d1-525">City</span></span>                  |
| <span data-ttu-id="f34d1-526">Kommune</span><span class="sxs-lookup"><span data-stu-id="f34d1-526">County</span></span>          | <span data-ttu-id="f34d1-527">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="f34d1-527">County (Municipality)</span></span> |
| <span data-ttu-id="f34d1-528">Gate</span><span class="sxs-lookup"><span data-stu-id="f34d1-528">Street</span></span>          | <span data-ttu-id="f34d1-529">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="f34d1-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="f34d1-530">Avgiftsområder</span><span class="sxs-lookup"><span data-stu-id="f34d1-530">Tax regions</span></span>

<span data-ttu-id="f34d1-531">Avgiftsområder brukes til å bestemme den gjeldende avgiften som skal brukes ved generering av lønn.</span><span class="sxs-lookup"><span data-stu-id="f34d1-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="f34d1-532">Avgiftsområder er tilordnet Dayforce som stedsadresser.</span><span class="sxs-lookup"><span data-stu-id="f34d1-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="f34d1-533">Standard avgiftområde må være knyttet til arbeiderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="f34d1-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="f34d1-534">Avgiftsområde (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-534">Tax region (required)</span></span>
- <span data-ttu-id="f34d1-535">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-535">Country/Region (required)</span></span>
- <span data-ttu-id="f34d1-536">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-536">State (required)</span></span>
- <span data-ttu-id="f34d1-537">Kommune</span><span class="sxs-lookup"><span data-stu-id="f34d1-537">County</span></span> 
- <span data-ttu-id="f34d1-538">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="f34d1-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="f34d1-539">Konfigurere data for å generere lønn i Mexico</span><span class="sxs-lookup"><span data-stu-id="f34d1-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="f34d1-540">Hvis du skal generere lønn for ansatte i Mexico, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="f34d1-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="f34d1-541">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="f34d1-541">Departments are required on positions.</span></span>
- <span data-ttu-id="f34d1-542">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="f34d1-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="f34d1-543">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="f34d1-543">Job types</span></span>

<span data-ttu-id="f34d1-544">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="f34d1-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f34d1-545">Jobbtype kreves for å kunne behandle lønn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="f34d1-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="f34d1-546">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="f34d1-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f34d1-547">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="f34d1-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f34d1-548">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="f34d1-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f34d1-549">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="f34d1-549">Job type</span></span>   | <span data-ttu-id="f34d1-550">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f34d1-551">Per time</span><span class="sxs-lookup"><span data-stu-id="f34d1-551">Hourly</span></span>     | <span data-ttu-id="f34d1-552">MX per time</span><span class="sxs-lookup"><span data-stu-id="f34d1-552">MX Hourly</span></span>   |
| <span data-ttu-id="f34d1-553">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="f34d1-553">Salaried</span></span>   | <span data-ttu-id="f34d1-554">MX lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="f34d1-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="f34d1-555">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="f34d1-555">Position types</span></span> 

<span data-ttu-id="f34d1-556">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="f34d1-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f34d1-557">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="f34d1-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f34d1-558">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="f34d1-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f34d1-559">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="f34d1-559">Position type</span></span>   | <span data-ttu-id="f34d1-560">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f34d1-561">Heltid</span><span class="sxs-lookup"><span data-stu-id="f34d1-561">Full-time</span></span>       | <span data-ttu-id="f34d1-562">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="f34d1-562">Full time employee</span></span> |
| <span data-ttu-id="f34d1-563">Deltid</span><span class="sxs-lookup"><span data-stu-id="f34d1-563">Part-time</span></span>       | <span data-ttu-id="f34d1-564">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="f34d1-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f34d1-565">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="f34d1-565">Reason codes</span></span>

<span data-ttu-id="f34d1-566">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="f34d1-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f34d1-567">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="f34d1-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f34d1-568">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="f34d1-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f34d1-569">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="f34d1-569">Reason code</span></span>            | <span data-ttu-id="f34d1-570">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-570">Description</span></span>                    | <span data-ttu-id="f34d1-571">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="f34d1-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="f34d1-572">AVGANGFØRBETALING</span><span class="sxs-lookup"><span data-stu-id="f34d1-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="f34d1-573">Avgang før første lønn</span><span class="sxs-lookup"><span data-stu-id="f34d1-573">Departure before first payroll</span></span> | <span data-ttu-id="f34d1-574">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-574">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-575">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="f34d1-575">RESIGNATION</span></span>            | <span data-ttu-id="f34d1-576">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-576">Resignation</span></span>                    | <span data-ttu-id="f34d1-577">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-577">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-578">PENSJON</span><span class="sxs-lookup"><span data-stu-id="f34d1-578">PENSION</span></span>                | <span data-ttu-id="f34d1-579">Pensjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-579">Pension</span></span>                        | <span data-ttu-id="f34d1-580">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-580">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-581">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="f34d1-581">TERMINATION</span></span>            | <span data-ttu-id="f34d1-582">Avslutning</span><span class="sxs-lookup"><span data-stu-id="f34d1-582">Termination</span></span>                    | <span data-ttu-id="f34d1-583">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-583">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-584">AVGANGVEDPENSJON</span><span class="sxs-lookup"><span data-stu-id="f34d1-584">RETIREMENT</span></span>             | <span data-ttu-id="f34d1-585">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-585">Retirement</span></span>                     | <span data-ttu-id="f34d1-586">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-586">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-587">FRAVÆRENDEPERSON</span><span class="sxs-lookup"><span data-stu-id="f34d1-587">ABSENTEE</span></span>               | <span data-ttu-id="f34d1-588">Fraværende person</span><span class="sxs-lookup"><span data-stu-id="f34d1-588">Absentee</span></span>                       | <span data-ttu-id="f34d1-589">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-589">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-590">ANNET</span><span class="sxs-lookup"><span data-stu-id="f34d1-590">OTHER</span></span>                  | <span data-ttu-id="f34d1-591">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="f34d1-591">Other Reasons</span></span>                  | <span data-ttu-id="f34d1-592">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-592">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-593">STENGNING</span><span class="sxs-lookup"><span data-stu-id="f34d1-593">CLOSURE</span></span>                | <span data-ttu-id="f34d1-594">Forretning stenger</span><span class="sxs-lookup"><span data-stu-id="f34d1-594">Business Closure</span></span>               | <span data-ttu-id="f34d1-595">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-595">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-596">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="f34d1-596">DEATH</span></span>                  | <span data-ttu-id="f34d1-597">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="f34d1-597">Death</span></span>                          | <span data-ttu-id="f34d1-598">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-598">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-599">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="f34d1-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="f34d1-600">Permisjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-600">Leave of Absence</span></span>               | <span data-ttu-id="f34d1-601">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-601">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-602">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="f34d1-602">CONTRACTEND</span></span>            | <span data-ttu-id="f34d1-603">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="f34d1-603">End of Contract</span></span>                | <span data-ttu-id="f34d1-604">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="f34d1-604">Terminate worker</span></span>     |
| <span data-ttu-id="f34d1-605">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="f34d1-605">SALARYCHANGE</span></span>           | <span data-ttu-id="f34d1-606">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="f34d1-606">Change of Salary</span></span>               | <span data-ttu-id="f34d1-607">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="f34d1-608">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="f34d1-608">Terms of employment</span></span>

<span data-ttu-id="f34d1-609">Ansettelsesbetingelser brukes til å opprette kategorier for ansettelsesbetingelser.</span><span class="sxs-lookup"><span data-stu-id="f34d1-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="f34d1-610">Vilkårene tilordnes til Dayforce som ansettelseindikatorverdier.</span><span class="sxs-lookup"><span data-stu-id="f34d1-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="f34d1-611">Følgende betingelsene for ansettelse og beskrivelser kreves.</span><span class="sxs-lookup"><span data-stu-id="f34d1-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="f34d1-612">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="f34d1-612">Terms of employment</span></span>   | <span data-ttu-id="f34d1-613">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f34d1-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f34d1-614">Vanlig</span><span class="sxs-lookup"><span data-stu-id="f34d1-614">Regular</span></span>               | <span data-ttu-id="f34d1-615">Vanlig</span><span class="sxs-lookup"><span data-stu-id="f34d1-615">Regular</span></span>     |
| <span data-ttu-id="f34d1-616">Direkte</span><span class="sxs-lookup"><span data-stu-id="f34d1-616">Direct</span></span>                | <span data-ttu-id="f34d1-617">Direkte</span><span class="sxs-lookup"><span data-stu-id="f34d1-617">Direct</span></span>      |
| <span data-ttu-id="f34d1-618">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="f34d1-618">Internship</span></span>            | <span data-ttu-id="f34d1-619">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="f34d1-619">Internship</span></span>  |
| <span data-ttu-id="f34d1-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="f34d1-620">Permanent</span></span>             | <span data-ttu-id="f34d1-621">Permanent</span><span class="sxs-lookup"><span data-stu-id="f34d1-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="f34d1-622">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="f34d1-622">Marital status</span></span>

<span data-ttu-id="f34d1-623">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="f34d1-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f34d1-624">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f34d1-625">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-625">Human Resources</span></span>                 | <span data-ttu-id="f34d1-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="f34d1-627">Gift</span><span class="sxs-lookup"><span data-stu-id="f34d1-627">Married</span></span>                | <span data-ttu-id="f34d1-628">Gift</span><span class="sxs-lookup"><span data-stu-id="f34d1-628">Married</span></span>                   |
| <span data-ttu-id="f34d1-629">Ugift</span><span class="sxs-lookup"><span data-stu-id="f34d1-629">Single</span></span>                 | <span data-ttu-id="f34d1-630">Ugift</span><span class="sxs-lookup"><span data-stu-id="f34d1-630">Single</span></span>                    |
| <span data-ttu-id="f34d1-631">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="f34d1-631">Widowed</span></span>                | <span data-ttu-id="f34d1-632">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="f34d1-632">Widowed</span></span>                   |
| <span data-ttu-id="f34d1-633">Skilt</span><span class="sxs-lookup"><span data-stu-id="f34d1-633">Divorced</span></span>               | <span data-ttu-id="f34d1-634">Skilt</span><span class="sxs-lookup"><span data-stu-id="f34d1-634">Divorced</span></span>                  |
| <span data-ttu-id="f34d1-635">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="f34d1-635">Registered Partnership</span></span> | <span data-ttu-id="f34d1-636">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="f34d1-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="f34d1-637">None</span><span class="sxs-lookup"><span data-stu-id="f34d1-637">None</span></span>                   | <span data-ttu-id="f34d1-638">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="f34d1-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f34d1-639">Samboer</span><span class="sxs-lookup"><span data-stu-id="f34d1-639">Cohabiting</span></span>             | <span data-ttu-id="f34d1-640">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="f34d1-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="f34d1-641">Kjønn</span><span class="sxs-lookup"><span data-stu-id="f34d1-641">Gender</span></span>

<span data-ttu-id="f34d1-642">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="f34d1-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f34d1-643">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f34d1-644">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-644">Human Resources</span></span>       | <span data-ttu-id="f34d1-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="f34d1-646">Mann</span><span class="sxs-lookup"><span data-stu-id="f34d1-646">Male</span></span>         | <span data-ttu-id="f34d1-647">Mann</span><span class="sxs-lookup"><span data-stu-id="f34d1-647">Male</span></span>                      |
| <span data-ttu-id="f34d1-648">Kvinne</span><span class="sxs-lookup"><span data-stu-id="f34d1-648">Female</span></span>       | <span data-ttu-id="f34d1-649">Kvinne</span><span class="sxs-lookup"><span data-stu-id="f34d1-649">Female</span></span>                    |
| <span data-ttu-id="f34d1-650">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="f34d1-650">Non-specific</span></span> | <span data-ttu-id="f34d1-651">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="f34d1-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="f34d1-652">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="f34d1-652">Payment method</span></span>

<span data-ttu-id="f34d1-653">Betalingsmåter gir den ansatte og firmaet en måte å beskrive hvordan ansatte skal betales.</span><span class="sxs-lookup"><span data-stu-id="f34d1-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="f34d1-654">Betalingsmåter tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="f34d1-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f34d1-655">Tabellen nedenfor viser hvordan betalingsmåter tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="f34d1-656">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-656">Human Resources</span></span>             | <span data-ttu-id="f34d1-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="f34d1-658">Kontant</span><span class="sxs-lookup"><span data-stu-id="f34d1-658">Cash</span></span>               | <span data-ttu-id="f34d1-659">Kontant</span><span class="sxs-lookup"><span data-stu-id="f34d1-659">Cash</span></span>                      |
| <span data-ttu-id="f34d1-660">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="f34d1-660">Electronic Payment</span></span> | <span data-ttu-id="f34d1-661">Overfør</span><span class="sxs-lookup"><span data-stu-id="f34d1-661">Transfer</span></span>                  |
| <span data-ttu-id="f34d1-662">Kontroll</span><span class="sxs-lookup"><span data-stu-id="f34d1-662">Check</span></span>              | <span data-ttu-id="f34d1-663">Sjekk</span><span class="sxs-lookup"><span data-stu-id="f34d1-663">Cheque</span></span>                    |
| <span data-ttu-id="f34d1-664">Bankoverføring</span><span class="sxs-lookup"><span data-stu-id="f34d1-664">Bank Draft</span></span>         | <span data-ttu-id="f34d1-665">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="f34d1-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f34d1-666">Annet</span><span class="sxs-lookup"><span data-stu-id="f34d1-666">Other</span></span>              | <span data-ttu-id="f34d1-667">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="f34d1-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="f34d1-668">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="f34d1-668">Bank account type</span></span>

<span data-ttu-id="f34d1-669">Bankkontotypene brukes for elektroniske betalinger til ansatte.</span><span class="sxs-lookup"><span data-stu-id="f34d1-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="f34d1-670">Bankkontotypene tilordnes til Dayforce som overføringskontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="f34d1-671">Bankkontotypene oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="f34d1-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="f34d1-672">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-672">Human Resources</span></span>            | <span data-ttu-id="f34d1-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="f34d1-674">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="f34d1-674">Checking Account</span></span>  | <span data-ttu-id="f34d1-675">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="f34d1-675">CheckingAccount</span></span>           |
| <span data-ttu-id="f34d1-676">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="f34d1-676">Payroll Account</span></span>   | <span data-ttu-id="f34d1-677">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="f34d1-677">PayrollAccount</span></span>            |
| <span data-ttu-id="f34d1-678">Sparekonto</span><span class="sxs-lookup"><span data-stu-id="f34d1-678">Savings Account</span></span>   | <span data-ttu-id="f34d1-679">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="f34d1-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f34d1-680">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="f34d1-680">BankGirot account</span></span> | <span data-ttu-id="f34d1-681">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="f34d1-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f34d1-682">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="f34d1-682">PlusGirot account</span></span> | <span data-ttu-id="f34d1-683">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="f34d1-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f34d1-684">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="f34d1-684">Earning codes</span></span>

<span data-ttu-id="f34d1-685">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="f34d1-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f34d1-686">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f34d1-687">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="f34d1-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f34d1-688">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="f34d1-688">Supported frequencies</span></span>

- <span data-ttu-id="f34d1-689">Alle</span><span class="sxs-lookup"><span data-stu-id="f34d1-689">All</span></span>
- <span data-ttu-id="f34d1-690">HVERBET</span><span class="sxs-lookup"><span data-stu-id="f34d1-690">EVERYPAY</span></span>
- <span data-ttu-id="f34d1-691">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="f34d1-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f34d1-692">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="f34d1-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f34d1-693">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="f34d1-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f34d1-694">1IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-694">1OFMTH</span></span>
- <span data-ttu-id="f34d1-695">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-695">LASTOFMTH</span></span>
- <span data-ttu-id="f34d1-696">2IMDN</span><span class="sxs-lookup"><span data-stu-id="f34d1-696">2OFMTH</span></span>
- <span data-ttu-id="f34d1-697">3IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-697">3OFMTH</span></span>
- <span data-ttu-id="f34d1-698">4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-698">4OFMTH</span></span>
- <span data-ttu-id="f34d1-699">5IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-699">5OFMTH</span></span>
- <span data-ttu-id="f34d1-700">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-700">1N2OFMTH</span></span>
- <span data-ttu-id="f34d1-701">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-701">3N4OFMTH</span></span>
- <span data-ttu-id="f34d1-702">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-702">1N3OFMTH</span></span>
- <span data-ttu-id="f34d1-703">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-703">1N4OFMTH</span></span>
- <span data-ttu-id="f34d1-704">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-704">2N3OFMTH</span></span>
- <span data-ttu-id="f34d1-705">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-705">2N4OFMTH</span></span>
- <span data-ttu-id="f34d1-706">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="f34d1-707">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="f34d1-708">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="f34d1-709">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="f34d1-710">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f34d1-711">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="f34d1-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f34d1-712">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="f34d1-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f34d1-713">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="f34d1-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f34d1-714">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="f34d1-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f34d1-715">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="f34d1-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f34d1-716">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="f34d1-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f34d1-717">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="f34d1-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f34d1-718">Adresser</span><span class="sxs-lookup"><span data-stu-id="f34d1-718">Addresses</span></span>

<span data-ttu-id="f34d1-719">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="f34d1-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f34d1-720">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="f34d1-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f34d1-721">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="f34d1-721">Human Resources</span></span>              | <span data-ttu-id="f34d1-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f34d1-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="f34d1-723">Land/område</span><span class="sxs-lookup"><span data-stu-id="f34d1-723">Country/Region</span></span>      | <span data-ttu-id="f34d1-724">Landskode</span><span class="sxs-lookup"><span data-stu-id="f34d1-724">Country Code</span></span>          |
| <span data-ttu-id="f34d1-725">Postnummer</span><span class="sxs-lookup"><span data-stu-id="f34d1-725">Zip/Postal Code</span></span>     | <span data-ttu-id="f34d1-726">Postnummer</span><span class="sxs-lookup"><span data-stu-id="f34d1-726">Postal Code</span></span>           |
| <span data-ttu-id="f34d1-727">Delstat</span><span class="sxs-lookup"><span data-stu-id="f34d1-727">State</span></span>               | <span data-ttu-id="f34d1-728">Statskode</span><span class="sxs-lookup"><span data-stu-id="f34d1-728">State Code</span></span>            |
| <span data-ttu-id="f34d1-729">By</span><span class="sxs-lookup"><span data-stu-id="f34d1-729">City</span></span>                | <span data-ttu-id="f34d1-730">By</span><span class="sxs-lookup"><span data-stu-id="f34d1-730">City</span></span>                  |
| <span data-ttu-id="f34d1-731">Kommune</span><span class="sxs-lookup"><span data-stu-id="f34d1-731">County</span></span>              | <span data-ttu-id="f34d1-732">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="f34d1-732">County (Municipality)</span></span> |
| <span data-ttu-id="f34d1-733">Gate</span><span class="sxs-lookup"><span data-stu-id="f34d1-733">Street</span></span>              | <span data-ttu-id="f34d1-734">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="f34d1-734">Address Line 1</span></span>        |
| <span data-ttu-id="f34d1-735">Gatenummer</span><span class="sxs-lookup"><span data-stu-id="f34d1-735">Street Number</span></span>       | <span data-ttu-id="f34d1-736">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="f34d1-736">Address Line 2</span></span>        |
| <span data-ttu-id="f34d1-737">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="f34d1-737">Building Complement</span></span> | <span data-ttu-id="f34d1-738">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="f34d1-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="f34d1-739">Passnummer</span><span class="sxs-lookup"><span data-stu-id="f34d1-739">Passport number</span></span>

<span data-ttu-id="f34d1-740">Ansatte kan deklarere passinformasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-740">Employees can declare passport information.</span></span> <span data-ttu-id="f34d1-741">Denne informasjonen er av **Pass**-identifikasjonstypen og er integrert i Dayforce som en del av en ansatts Mexico-spesifikke informasjon.</span><span class="sxs-lookup"><span data-stu-id="f34d1-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="f34d1-742">Identifikasjonstype = "Pass"</span><span class="sxs-lookup"><span data-stu-id="f34d1-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="f34d1-743">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-743">Issued Date</span></span>
- <span data-ttu-id="f34d1-744">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="f34d1-744">Expiration Date</span></span>

<span data-ttu-id="f34d1-745">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **Pass**.</span><span class="sxs-lookup"><span data-stu-id="f34d1-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="f34d1-746">Men bare den gjeldende aktive passoppføringen er integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="f34d1-747">Hvis alle passoppføringer er utløpt, er passet som sist ble utstedt, integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="f34d1-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

---
title: Konfigurere integrasjon med Dayforce
description: Integrasjonen mellom Microsoft Dynamics 365 Human Resources og Ceridian Dayforce bruker flere konfigurasjonstrinn som er beskrevet i denne artikkelen. Du må konfigurere integreringen i både Human Resources og Dayforce før du kan behandle en lønnskjøring.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890010"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="af9b3-104">Konfigurere integrasjon med Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="af9b3-105">Integrasjonen mellom Microsoft Dynamics 365 Human Resources og Ceridian Dayforce bruker flere konfigurasjonstrinn som er beskrevet i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="af9b3-106">Du må konfigurere integreringen i både Human Resources og Dayforce før du kan behandle en lønnskjøring.</span><span class="sxs-lookup"><span data-stu-id="af9b3-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="af9b3-107">Når du bruker en tjeneste som Dayforce til å fullføre lønnskjøringer, må du aktivere integrering i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="af9b3-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="af9b3-108">Integreringen krever bestemte data fra Human Resources.</span><span class="sxs-lookup"><span data-stu-id="af9b3-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="af9b3-109">Derfor må du kontrollere at data som tilordnes til Dayforce, er konfigurert i Human Resources på en måte som støtter integreringen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="af9b3-110">Integrasjonen bruker følgende brede datakategorier:</span><span class="sxs-lookup"><span data-stu-id="af9b3-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="af9b3-111">Personaldata</span><span class="sxs-lookup"><span data-stu-id="af9b3-111">Human resources data</span></span>
- <span data-ttu-id="af9b3-112">Kompensasjonsdata</span><span class="sxs-lookup"><span data-stu-id="af9b3-112">Compensation data</span></span>
- <span data-ttu-id="af9b3-113">Lønnsdata, for eksempel lønnssykluser, lønnsperioder og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="af9b3-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="af9b3-114">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="af9b3-114">Worker data</span></span>

<span data-ttu-id="af9b3-115">Denne artikkelen beskriver trinnene du må følge for å aktivere integreringen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="af9b3-116">Den beskriver også hvilke typer data og konfigurasjonsdetaljer som integreringen krever.</span><span class="sxs-lookup"><span data-stu-id="af9b3-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="af9b3-117">Aktivere integrasjonen</span><span class="sxs-lookup"><span data-stu-id="af9b3-117">Enable the integration</span></span>

<span data-ttu-id="af9b3-118">I Human Resources må du aktivere integreringen og angi konfigurasjonsinformasjonen for å koble til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="af9b3-119">Hvis du vil at økonomimodultransaksjonen som produseres, skal importeres til Microsoft Dynamics 365 Finance, må du også definere en Microsoft Azure-lagringskonto og angi Azure Storage-tilkoblingsstrengen i Finance.</span><span class="sxs-lookup"><span data-stu-id="af9b3-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="af9b3-120">Følg denne fremgangsmåten for å aktivere integrasjonen i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="af9b3-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="af9b3-121">Velg **Konfigurasjon av integrering** på siden **Systemadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="af9b3-122">Angi sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="af9b3-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="af9b3-123">Angi brukernavnet og passordet til brukeren som skal ha tilgang til sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="af9b3-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="af9b3-124">Test tilkoblingen etter behov, og sett alternativet **Aktiver lønnsintegrering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="af9b3-125">Når integreringen er slått på, opprettes dataeksportpakken og -filene, og frekvensen angis.</span><span class="sxs-lookup"><span data-stu-id="af9b3-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="af9b3-126">Du kan endre denne frekvensen etter behov.</span><span class="sxs-lookup"><span data-stu-id="af9b3-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="af9b3-127">Hvis du vil ha mer informasjon om Azure Storage-kontoer og Azure Storage-tilkoblingsstrenger, kan du se følgende Azure-artikler:</span><span class="sxs-lookup"><span data-stu-id="af9b3-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="af9b3-128">Om Azure Storage-kontoer</span><span class="sxs-lookup"><span data-stu-id="af9b3-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="af9b3-129">Konfigurere Azure Storage-tilkoblingsstrenger</span><span class="sxs-lookup"><span data-stu-id="af9b3-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="af9b3-130">Tekniske detaljer når lønnsintegrasjon er aktivert</span><span class="sxs-lookup"><span data-stu-id="af9b3-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="af9b3-131">Aktivering av lønnsintegrasjonen har to hovedvirkninger:</span><span class="sxs-lookup"><span data-stu-id="af9b3-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="af9b3-132">Det opprettes et dataeksportprosjekt kalt «Eksport av lønnsintegrasjon».</span><span class="sxs-lookup"><span data-stu-id="af9b3-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="af9b3-133">Dette prosjektet inneholder enhetene og feltene som kreves for lønnsintegrasjonen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="af9b3-134">Du kan undersøke prosjektet ved å gå til **Systemadministrasjon**, velge **Databehandling**-flisen og deretter åpne dataprosjektet fra listen over prosjekter.</span><span class="sxs-lookup"><span data-stu-id="af9b3-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="af9b3-135">Denne satsvise jobben utfører dataeksportprosjektet, krypterer den resulterende datapakken og overfører datapakkefilen til SFTP-endepunktet som er konfigurert på skjermen **Konfigurasjon av integrering**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="af9b3-136">Datapakken som overføres til SFTP-endepunktet, krypteres ved hjelp av en nøkkel som er unik for pakken.</span><span class="sxs-lookup"><span data-stu-id="af9b3-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="af9b3-137">Nøkkelen er i et Azure Key Vault som bare Ceridian har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="af9b3-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="af9b3-138">Det går ikke an å dekryptere og undersøke innholdet i datapakken.</span><span class="sxs-lookup"><span data-stu-id="af9b3-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="af9b3-139">Hvis du må undersøke innholdet i datapakken, må du eksportere dataprosjektet «Eksport av lønnsintegrasjon» manuelt, laste det ned, og deretter åpne det.</span><span class="sxs-lookup"><span data-stu-id="af9b3-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="af9b3-140">Pakken verken krypteres eller overføres når du foretar manuell eksport.</span><span class="sxs-lookup"><span data-stu-id="af9b3-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="af9b3-141">For forekomster der integreringsfilene sendes fra et Dynamics 365 Human Resources UAT-miljø eller et sandkassemiljø til et Ceridian Dayforce-testmiljø, kan du bruke følgende Key Vault-URL: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="af9b3-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="af9b3-142">Konfigurere dataene dine</span><span class="sxs-lookup"><span data-stu-id="af9b3-142">Configure your data</span></span> 

<span data-ttu-id="af9b3-143">For å behandle lønn må du konfigurere Personaldata i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="af9b3-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="af9b3-144">Du må definere organisasjonsdata, for eksempel jobber og stillinger, samt informasjon om fordeler og kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="af9b3-145">Denne informasjonen gir informasjon om ansettelse, lønn og trekk som kreves for å kunne generere lønn for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="af9b3-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="af9b3-146">Personaldata</span><span class="sxs-lookup"><span data-stu-id="af9b3-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="af9b3-147">Fordeler</span><span class="sxs-lookup"><span data-stu-id="af9b3-147">Benefits</span></span> 

<span data-ttu-id="af9b3-148">Personale inneholder verktøy for oppsett og vedlikehold av fordeler, fradrag og arbeiderkompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere.</span><span class="sxs-lookup"><span data-stu-id="af9b3-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="af9b3-149">Når du oppretter fordeler, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="af9b3-150">Fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="af9b3-150">Benefit plans</span></span>

- <span data-ttu-id="af9b3-151">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-151">Plan (required)</span></span>
- <span data-ttu-id="af9b3-152">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-152">Type (required)</span></span>
- <span data-ttu-id="af9b3-153">Lønnsinnvirkning (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-153">Payroll impact (required)</span></span>
- <span data-ttu-id="af9b3-154">Gjenopprett etterskudd</span><span class="sxs-lookup"><span data-stu-id="af9b3-154">Recover arrears</span></span>
- <span data-ttu-id="af9b3-155">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="af9b3-155">Deduction method</span></span>
- <span data-ttu-id="af9b3-156">Fradragsprioritet</span><span class="sxs-lookup"><span data-stu-id="af9b3-156">Deduction priority</span></span>
- <span data-ttu-id="af9b3-157">Begrens periode</span><span class="sxs-lookup"><span data-stu-id="af9b3-157">Limit period</span></span>
- <span data-ttu-id="af9b3-158">Grensebeløp</span><span class="sxs-lookup"><span data-stu-id="af9b3-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="af9b3-159">Fordeler</span><span class="sxs-lookup"><span data-stu-id="af9b3-159">Benefits</span></span>

- <span data-ttu-id="af9b3-160">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-160">Plan (required)</span></span>
- <span data-ttu-id="af9b3-161">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-161">Type (required)</span></span>
- <span data-ttu-id="af9b3-162">Alternativ (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-162">Option (required)</span></span>
- <span data-ttu-id="af9b3-163">Fordel-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-163">Benefit ID (required)</span></span>
- <span data-ttu-id="af9b3-164">Frekvens</span><span class="sxs-lookup"><span data-stu-id="af9b3-164">Frequency</span></span>
- <span data-ttu-id="af9b3-165">Grunnlag</span><span class="sxs-lookup"><span data-stu-id="af9b3-165">Basis</span></span>
- <span data-ttu-id="af9b3-166">Beløp eller sats</span><span class="sxs-lookup"><span data-stu-id="af9b3-166">Amount or rate</span></span>
- <span data-ttu-id="af9b3-167">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="af9b3-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="af9b3-168">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="af9b3-168">Supported frequencies</span></span> 

- <span data-ttu-id="af9b3-169">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="af9b3-169">Weekly</span></span>
- <span data-ttu-id="af9b3-170">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="af9b3-170">Bi-weekly</span></span>
- <span data-ttu-id="af9b3-171">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="af9b3-171">Semi-monthly</span></span>
- <span data-ttu-id="af9b3-172">Månedlig</span><span class="sxs-lookup"><span data-stu-id="af9b3-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="af9b3-173">Støttede grunnlag</span><span class="sxs-lookup"><span data-stu-id="af9b3-173">Supported bases</span></span> 

- <span data-ttu-id="af9b3-174">Fast beløp</span><span class="sxs-lookup"><span data-stu-id="af9b3-174">Fixed amount</span></span>
- <span data-ttu-id="af9b3-175">Prosentandel av inntekter</span><span class="sxs-lookup"><span data-stu-id="af9b3-175">Percent of earnings</span></span>
- <span data-ttu-id="af9b3-176">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="af9b3-176">Productive hours</span></span>

<span data-ttu-id="af9b3-177">Dayforce oppretter følgende fradrag, basert på lønnsinnvirkning som er definert på fordelsplanen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="af9b3-178">Valg i Human Resources</span><span class="sxs-lookup"><span data-stu-id="af9b3-178">Selection in Human Resources</span></span>        | <span data-ttu-id="af9b3-179">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="af9b3-180">Ingen</span><span class="sxs-lookup"><span data-stu-id="af9b3-180">None</span></span>                       | <span data-ttu-id="af9b3-181">Ingen fradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="af9b3-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="af9b3-182">Bare fradrag</span><span class="sxs-lookup"><span data-stu-id="af9b3-182">Deduction only</span></span>             | <span data-ttu-id="af9b3-183">Et ansattfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="af9b3-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="af9b3-184">Bare bidrag</span><span class="sxs-lookup"><span data-stu-id="af9b3-184">Contribution only</span></span>          | <span data-ttu-id="af9b3-185">Et arbeidsgiverfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="af9b3-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="af9b3-186">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="af9b3-186">Deduction and contribution</span></span> | <span data-ttu-id="af9b3-187">Fradrag for ansatte og arbeidsgivere opprettes.</span><span class="sxs-lookup"><span data-stu-id="af9b3-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="af9b3-188">Hvis du vil ha mer informasjon om hvordan du definerer og administrerer et program for fordeler, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="af9b3-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="af9b3-189">Levere et program for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="af9b3-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="af9b3-190">Opprett en ny fordel</span><span class="sxs-lookup"><span data-stu-id="af9b3-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="af9b3-191">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="af9b3-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="af9b3-192">Registrere og fjerne fordeler fra arbeidere</span><span class="sxs-lookup"><span data-stu-id="af9b3-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="af9b3-193">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-193">Compensation</span></span> 

<span data-ttu-id="af9b3-194">Kompensasjonsstyring brukes til å kontrollere levering av grunnlønn og bonuser.</span><span class="sxs-lookup"><span data-stu-id="af9b3-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="af9b3-195">En ansatts faste grunnlønn og personlige tilleggsøkninger styres via faste kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="af9b3-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="af9b3-196">Betaling av insitamentutbetalinger, for eksempel bonuser, ytelsestillegg, aksjeopsjoner og tilskudd, og også engangsbonuser, kontrolleres via variable kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="af9b3-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="af9b3-197">Dayforce bruker kompensasjonsinformasjon til å beregne timesats eller årlig sats for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="af9b3-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="af9b3-198">Planer for faste kompensasjoner og konverteringer av lønnssats er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="af9b3-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="af9b3-199">Ansatte må tilknyttes en plan for fast kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="af9b3-200">Hvis du vil ha mer informasjon om kompensasjonsplaner, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="af9b3-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="af9b3-201">Opprette planer for fast kompensasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="af9b3-202">Opprette variable kompensasjonsplaner</span><span class="sxs-lookup"><span data-stu-id="af9b3-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="af9b3-203">Utvikle struktur og planer for lønn/kompensasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="af9b3-204">Behandle kompensasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="af9b3-205">Definere kompensasjonsprosess og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="af9b3-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="af9b3-206">Registrere en ansatt i en fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="af9b3-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="af9b3-207">Registrere en ansatt i en variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="af9b3-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="af9b3-208">Jobber</span><span class="sxs-lookup"><span data-stu-id="af9b3-208">Jobs</span></span> 

<span data-ttu-id="af9b3-209">En jobb er en samling oppgaver og ansvarsområder som kreves av en person som utfører en jobb.</span><span class="sxs-lookup"><span data-stu-id="af9b3-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="af9b3-210">Hvis du vil ha mer informasjon, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="af9b3-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="af9b3-211">Definere komponentene for en jobb</span><span class="sxs-lookup"><span data-stu-id="af9b3-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="af9b3-212">Definere nye jobber</span><span class="sxs-lookup"><span data-stu-id="af9b3-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="af9b3-213">Stillinger</span><span class="sxs-lookup"><span data-stu-id="af9b3-213">Positions</span></span>

<span data-ttu-id="af9b3-214">En stilling er én enkeltforekomst av en jobb.</span><span class="sxs-lookup"><span data-stu-id="af9b3-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="af9b3-215">"Salgssjef (øst)"-stillingen er for eksempel én av stillingene som er knyttet til jobben "Salgssjef".</span><span class="sxs-lookup"><span data-stu-id="af9b3-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="af9b3-216">Det finnes en stilling i en avdeling.</span><span class="sxs-lookup"><span data-stu-id="af9b3-216">A position exists in a department.</span></span> <span data-ttu-id="af9b3-217">Bare én arbeider kan være tilknyttet hvert område.</span><span class="sxs-lookup"><span data-stu-id="af9b3-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="af9b3-218">Ha følgende data og konfigurasjon i bakhodet når du definerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="af9b3-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="af9b3-219">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-219">Position (required)</span></span>
- <span data-ttu-id="af9b3-220">Beskrivelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-220">Description (required)</span></span>
- <span data-ttu-id="af9b3-221">Jobb (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-221">Job (required)</span></span>
- <span data-ttu-id="af9b3-222">Avdeling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-222">Department (required)</span></span>
- <span data-ttu-id="af9b3-223">Stillingstype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-223">Position type (required)</span></span>
- <span data-ttu-id="af9b3-224">Fulltidsekvivalent</span><span class="sxs-lookup"><span data-stu-id="af9b3-224">Full-time equivalent</span></span>
- <span data-ttu-id="af9b3-225">Årlige vanlige timer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="af9b3-226">Betalt av juridisk enhet (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="af9b3-227">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-227">Pay cycle (required)</span></span>
- <span data-ttu-id="af9b3-228">Standard finansdimensjon – kostsenter (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="af9b3-229">Arbeidertilordning – arbeider, start for tilordning, slutt for tilordning, årsakskode</span><span class="sxs-lookup"><span data-stu-id="af9b3-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="af9b3-230">Hvis flere stillinger i samme avdeling er knyttet til den samme jobben, konsolideres de til én stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="af9b3-231">Hvis du vil ha mer informasjon, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="af9b3-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="af9b3-232">Organisere arbeidsstyrken ved bruk av avdelinger, jobber og stillinger</span><span class="sxs-lookup"><span data-stu-id="af9b3-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="af9b3-233">Definere stillinger</span><span class="sxs-lookup"><span data-stu-id="af9b3-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="af9b3-234">Avdelinger</span><span class="sxs-lookup"><span data-stu-id="af9b3-234">Departments</span></span>

<span data-ttu-id="af9b3-235">En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="af9b3-236">En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale.</span><span class="sxs-lookup"><span data-stu-id="af9b3-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="af9b3-237">Du kan bruke avdelinger til å rapportere om funksjonsområder.</span><span class="sxs-lookup"><span data-stu-id="af9b3-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="af9b3-238">Avdelinger kan ha ansvar for fortjeneste og tap.</span><span class="sxs-lookup"><span data-stu-id="af9b3-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="af9b3-239">Hvis du vil ha mer informasjon, kan du se følgende artikler:</span><span class="sxs-lookup"><span data-stu-id="af9b3-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="af9b3-240">Opprette en avdeling og knytte den til avdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="af9b3-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="af9b3-241">Definere nye avdelinger</span><span class="sxs-lookup"><span data-stu-id="af9b3-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="af9b3-242">Lønnssykluser og lønnsperioder</span><span class="sxs-lookup"><span data-stu-id="af9b3-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="af9b3-243">En betalingssyklus avgjør hvor ofte lønnskjøring utføres, og de spesifikke dagene arbeidere lønnes.</span><span class="sxs-lookup"><span data-stu-id="af9b3-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="af9b3-244">For eksempel kan en lønnssyklus være månedlig, og ansatte kan betales på den siste dagen i måneden.</span><span class="sxs-lookup"><span data-stu-id="af9b3-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="af9b3-245">En lønnssyklus kan også være ukentlig, og ansatte kan betales tirsdagen etter slutten av lønnsperioden.</span><span class="sxs-lookup"><span data-stu-id="af9b3-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="af9b3-246">Lønnssykluser tilordnes til stillinger for å styre når arbeidere i disse stillingene lønnes.</span><span class="sxs-lookup"><span data-stu-id="af9b3-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="af9b3-247">Når du oppretter lønnssykler, kan du generere lønnsperioder for hver enkelt syklus.</span><span class="sxs-lookup"><span data-stu-id="af9b3-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="af9b3-248">Hver lønnsperiode inkluderer en standard betalingsdato som er basert på informasjonen du angir.</span><span class="sxs-lookup"><span data-stu-id="af9b3-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="af9b3-249">Du kan imidlertid endre standard betalingsdato i en lønnsperiode for å tillate unntak, for eksempel når betalingsdatoen faller på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="af9b3-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="af9b3-250">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="af9b3-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="af9b3-251">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-251">Pay cycle (required)</span></span>
- <span data-ttu-id="af9b3-252">Lønnssyklusfrekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="af9b3-253">Periodens startdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="af9b3-254">Standard betalingsdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="af9b3-255">Denne informasjonen er integrert med Dayforce som lønnsgrupper og er inndelt etter land eller område for hver lønnssyklus.</span><span class="sxs-lookup"><span data-stu-id="af9b3-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="af9b3-256">Minst én lønnsperiode må genereres før integrasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="af9b3-257">Dayforce genererer lønnsgruppekalendere og betalingsdatoer basert på startdatoen for den første lønnsperioden og standard betalingsdato som er definert i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="af9b3-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="af9b3-258">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="af9b3-258">Earning codes</span></span>

<span data-ttu-id="af9b3-259">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="af9b3-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="af9b3-260">Kodene har forskjellige parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="af9b3-261">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="af9b3-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="af9b3-262">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-262">Earning Code (required)</span></span>
- <span data-ttu-id="af9b3-263">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-263">Description</span></span>
- <span data-ttu-id="af9b3-264">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="af9b3-264">Unit of measure</span></span>
- <span data-ttu-id="af9b3-265">Produktiv</span><span class="sxs-lookup"><span data-stu-id="af9b3-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="af9b3-266">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="af9b3-266">Worker data</span></span>

<span data-ttu-id="af9b3-267">Poster for ulike typer arbeidere som du har, er viktig for personal. og lønnsystemene dine.</span><span class="sxs-lookup"><span data-stu-id="af9b3-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="af9b3-268">Informasjonen du legger inn, kan brukes til å spore arbeidere og personlig informasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="af9b3-269">Du kan vedlikeholde følgende informasjon om arbeidere:</span><span class="sxs-lookup"><span data-stu-id="af9b3-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="af9b3-270">**Grunnleggende** – Vedlikehold grunnleggende informasjon om en arbeider, for eksempel kontaktinformasjon, demografisk informasjon, identifikasjonsinformasjon, familieinformasjon, militærtjenestestatus, informasjon om personer som bor i utlandet, og personlige kontakter og kontakter i nødfall.</span><span class="sxs-lookup"><span data-stu-id="af9b3-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="af9b3-271">**Ansettelse** – Vedlikehold informasjon om en arbeiders ansettelse, for eksempel informasjon om firma- eller organisasjonstilknytning, stillingstilordning, start- og sluttdatoer, arbeidstillatelse, vilkår for ansettelse, pensjon, ferie og flytting.</span><span class="sxs-lookup"><span data-stu-id="af9b3-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="af9b3-272">**Lønn og fravær** – Vedlikehold opplysninger om en arbeiders fravær, for eksempel arbeidskalendere, fraværstransaksjoner og fraværsoppsett.</span><span class="sxs-lookup"><span data-stu-id="af9b3-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="af9b3-273">**Kompensasjon og lønn** – Vedlikehold informasjon om en arbeiders kompensasjonsplaner og lønn, for eksempel planregistrering, priser, ytelse, provisjon, avgiftsinformasjon, pensjonering og lønnstrekk.</span><span class="sxs-lookup"><span data-stu-id="af9b3-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="af9b3-274">Når du legger inn arbeiderinformasjon, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="af9b3-275">Generell informasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-275">General information</span></span>

- <span data-ttu-id="af9b3-276">Personalnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-276">Personnel number (required)</span></span>
- <span data-ttu-id="af9b3-277">Fornavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-277">First name (required)</span></span>
- <span data-ttu-id="af9b3-278">Etternavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-278">Last name (required)</span></span>
- <span data-ttu-id="af9b3-279">Mellomnavn</span><span class="sxs-lookup"><span data-stu-id="af9b3-279">Middle name</span></span>
- <span data-ttu-id="af9b3-280">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-280">Seniority date</span></span>
- <span data-ttu-id="af9b3-281">Kalt</span><span class="sxs-lookup"><span data-stu-id="af9b3-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="af9b3-282">Personlige opplysninger</span><span class="sxs-lookup"><span data-stu-id="af9b3-282">Personal information</span></span>

- <span data-ttu-id="af9b3-283">Sivilstand (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-283">Marital status (required)</span></span>
- <span data-ttu-id="af9b3-284">Fødselsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-284">Birth date (required)</span></span>
- <span data-ttu-id="af9b3-285">Kjønn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-285">Gender (required)</span></span>
- <span data-ttu-id="af9b3-286">Person med funksjonshemminger</span><span class="sxs-lookup"><span data-stu-id="af9b3-286">Person with disabilities</span></span>
- <span data-ttu-id="af9b3-287">Nasjonalitet land/område (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="af9b3-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="af9b3-288">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="af9b3-288">Address information</span></span>

- <span data-ttu-id="af9b3-289">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-289">Primary (required)</span></span>
- <span data-ttu-id="af9b3-290">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-290">Country/region (required)</span></span>
- <span data-ttu-id="af9b3-291">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-291">Postal code (required)</span></span>
- <span data-ttu-id="af9b3-292">Gatenummer (obligatorisk) (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="af9b3-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="af9b3-293">Bygningsnavn (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="af9b3-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="af9b3-294">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-294">City (required)</span></span>
- <span data-ttu-id="af9b3-295">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-295">State (required)</span></span>
- <span data-ttu-id="af9b3-296">Land (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="af9b3-297">Kontaktinformasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-297">Contact information</span></span> 

- <span data-ttu-id="af9b3-298">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-298">Primary (required)</span></span>
- <span data-ttu-id="af9b3-299">Kontaktnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-299">Contact number (required)</span></span>
- <span data-ttu-id="af9b3-300">Utvidelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="af9b3-301">Lønnsinformasjon og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="af9b3-301">Payroll information and earning codes</span></span>

<span data-ttu-id="af9b3-302">Ansatte kan tilordnes spesifikke inntekter med en gitt betalingfrekvens og med en foretrukket betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="af9b3-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="af9b3-303">Følgende felt brukes i Dayforce for å sørge for at disse valgene og innstillingene brukes.</span><span class="sxs-lookup"><span data-stu-id="af9b3-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="af9b3-304">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="af9b3-304">Earning codes</span></span>

- <span data-ttu-id="af9b3-305">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-305">Position (required)</span></span>
- <span data-ttu-id="af9b3-306">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-306">Earning Code (required)</span></span>
- <span data-ttu-id="af9b3-307">Frekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-307">Frequency (required)</span></span>
- <span data-ttu-id="af9b3-308">Beløp (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="af9b3-309">Lønnsinformasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-309">Payroll information</span></span>

- <span data-ttu-id="af9b3-310">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="af9b3-310">Payment Method</span></span>
- <span data-ttu-id="af9b3-311">Økonomisk område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-311">Economic Region (required)</span></span>
- <span data-ttu-id="af9b3-312">ID for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="af9b3-312">Employee Benefits ID</span></span>
- <span data-ttu-id="af9b3-313">Nasjonalt ID-nummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-313">National ID Number (required)</span></span>
- <span data-ttu-id="af9b3-314">Militærtjenestenummer</span><span class="sxs-lookup"><span data-stu-id="af9b3-314">Military Service Number</span></span>
- <span data-ttu-id="af9b3-315">Skift-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-315">Shift ID (required)</span></span>
- <span data-ttu-id="af9b3-316">Avgiftsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-316">Tax Number (required)</span></span>
- <span data-ttu-id="af9b3-317">Fagforenings-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-317">Union ID (required)</span></span>
- <span data-ttu-id="af9b3-318">Arbeidsdag-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-318">Work Day ID (required)</span></span>
- <span data-ttu-id="af9b3-319">Arbeidstillatelsesnummer</span><span class="sxs-lookup"><span data-stu-id="af9b3-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="af9b3-320">Når det gjelder betalingsmåte støtter Mexico **Kontanter**, **Sjekk** (firmaets fysisk sjekk) og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="af9b3-321">Hvis betalingsmåte ikke er angitt, brukes **Sjekk** som standard.</span><span class="sxs-lookup"><span data-stu-id="af9b3-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="af9b3-322">Ansettelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="af9b3-322">Employment details</span></span>

<span data-ttu-id="af9b3-323">Ansettelsesdetaljhistorikk brukes som nøkkelinformasjon til å avlede en ansatts ansettelse-, oppsigelses- og nyansettelsesstatuser i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="af9b3-324">Dayforce støtter bare én aktiv ansettelsespost om gangen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="af9b3-325">Startdato for ansettelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-325">Employment start date (required)</span></span>
- <span data-ttu-id="af9b3-326">Sluttdato for ansettelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-326">Employment end date</span></span>
- <span data-ttu-id="af9b3-327">Startdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-327">Start date</span></span>
- <span data-ttu-id="af9b3-328">Justert startdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-328">Adjusted start date</span></span>
- <span data-ttu-id="af9b3-329">Avslutningsdato (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="af9b3-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="af9b3-330">Avslutningsårsak (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="af9b3-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="af9b3-331">En ansatts nøkkeldatoer avledes ved å bruke følgende informasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="af9b3-332">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-332">Human Resources</span></span>                | <span data-ttu-id="af9b3-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af9b3-334">Den siste ansettelsesdatoen</span><span class="sxs-lookup"><span data-stu-id="af9b3-334">Most recent hire date</span></span> | <span data-ttu-id="af9b3-335">Ansettelsesstart for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="af9b3-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="af9b3-336">Avslutningsdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-336">Termination date</span></span>      | <span data-ttu-id="af9b3-337">Avslutningsdato for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="af9b3-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="af9b3-338">Startdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-338">Start date</span></span>            | <span data-ttu-id="af9b3-339">Justert startdato, startdato eller ansettelsesstart for gjeldende ikke-aktive ansettelseloggpost</span><span class="sxs-lookup"><span data-stu-id="af9b3-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="af9b3-340">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-340">Original hire date</span></span>    | <span data-ttu-id="af9b3-341">Ansettelsesstart for tidligste ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="af9b3-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="af9b3-342">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-342">Compensation</span></span>

<span data-ttu-id="af9b3-343">En fast kompensasjonsplan må være knyttet til hver ansatts primære stilling i en ansattperiode.</span><span class="sxs-lookup"><span data-stu-id="af9b3-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="af9b3-344">Denne perioden begynner på datoen da den ansatte ble ansatt (eller startdatoen for ansettelsen), og fortsetter til avslutning.</span><span class="sxs-lookup"><span data-stu-id="af9b3-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="af9b3-345">Gyldighetsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-345">Effective Date (required)</span></span>
- <span data-ttu-id="af9b3-346">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-346">Expiration date</span></span>
- <span data-ttu-id="af9b3-347">Lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-347">Pay Rate (required)</span></span>
- <span data-ttu-id="af9b3-348">Konverteringer av lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="af9b3-349">Tilsvarende årlig (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="af9b3-350">Tilsvarende per time (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="af9b3-351">Hvis en timebaserte ansatt har flere stillinger, importeres fast kompensasjon for den primære stillingen til Dayforce som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="af9b3-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="af9b3-352">For ikke-primære stillinger lagres timeprisen til den tilsvarende stillingen i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="af9b3-353">Hvis en lønnsansatt har flere stillinger, avledes kumulativ timepris og årslønn på tvers av alle aktive stillinger og brukes som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="af9b3-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="af9b3-354">Identifikasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="af9b3-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="af9b3-355">Personnummeridentifikator</span><span class="sxs-lookup"><span data-stu-id="af9b3-355">Social Security identifier</span></span> 

<span data-ttu-id="af9b3-356">Alle ansatte må ha én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="af9b3-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="af9b3-357">Identifikatoren må være av identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="af9b3-358">I Dayforce hentes den automatisk som den ansattes personnummeridentifikator som kreves for ansettelse.</span><span class="sxs-lookup"><span data-stu-id="af9b3-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="af9b3-359">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-359">Primary (required)</span></span>
- <span data-ttu-id="af9b3-360">Identifikasjonstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="af9b3-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="af9b3-361">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-361">Issued Date</span></span>
- <span data-ttu-id="af9b3-362">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-362">Expiration Date</span></span>

<span data-ttu-id="af9b3-363">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="af9b3-364">Det er imidlertid bare posten som er merket som **Primær**, som er integrert i Dayforce, uansett om nummeret er aktivt eller utløpt.</span><span class="sxs-lookup"><span data-stu-id="af9b3-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="af9b3-365">Bankkontoer og -utlegg</span><span class="sxs-lookup"><span data-stu-id="af9b3-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="af9b3-366">Gyldig bankkontoinformasjon må angis for alle ansatte som velger å betales via bankkontooverføringer.</span><span class="sxs-lookup"><span data-stu-id="af9b3-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="af9b3-367">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-367">Human Resources</span></span>                         | <span data-ttu-id="af9b3-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af9b3-369">Bankkontonummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="af9b3-370">SWIFT-kode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-370">SWIFT code (required)</span></span>          | <span data-ttu-id="af9b3-371">**Bank-ID**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="af9b3-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="af9b3-372">Avdelingsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="af9b3-373">Bankkontotype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-373">Bank account type (required)</span></span>   | <span data-ttu-id="af9b3-374">**Kontotoype**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="af9b3-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="af9b3-375">Støttede verdier inkluderer **Kontroll** og **Lønn**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="af9b3-376">Ansatte som velger å betales via bankkontooverføringer, må oppgi en kobling til en restkonto som er under en juridisk enhet som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en meksikansk bank.</span><span class="sxs-lookup"><span data-stu-id="af9b3-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="af9b3-377">Alle andre ikke-restkontoer ignoreres.</span><span class="sxs-lookup"><span data-stu-id="af9b3-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="af9b3-378">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="af9b3-378">Address information</span></span>

<span data-ttu-id="af9b3-379">Alle ansatte må ha ett primært sted.</span><span class="sxs-lookup"><span data-stu-id="af9b3-379">Every employee must have one primary location.</span></span> <span data-ttu-id="af9b3-380">I Dayforce brukes dette stedet til å fastslå den ansattes primære bosted for skatte- og avgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="af9b3-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="af9b3-381">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-381">Primary (required)</span></span>
- <span data-ttu-id="af9b3-382">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-382">Country/region (required)</span></span>
- <span data-ttu-id="af9b3-383">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="af9b3-384">Gate (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-384">Street (required)</span></span>
- <span data-ttu-id="af9b3-385">Gatenummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-385">Street Number (required)</span></span>
- <span data-ttu-id="af9b3-386">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="af9b3-386">Building Complement</span></span>
- <span data-ttu-id="af9b3-387">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-387">City (required)</span></span>
- <span data-ttu-id="af9b3-388">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-388">State (required)</span></span>
- <span data-ttu-id="af9b3-389">Land (oblitagorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="af9b3-390">Konfigurer dataene for å generere lønn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="af9b3-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="af9b3-391">Hvis du skal generere lønn for ansatte i USA og Canada, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="af9b3-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="af9b3-392">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="af9b3-392">Departments are required on positions.</span></span>
- <span data-ttu-id="af9b3-393">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="af9b3-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="af9b3-394">Du kan konfigurere Human Resources slik at det kreves at stillinger spesifiserer en avdeling.</span><span class="sxs-lookup"><span data-stu-id="af9b3-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="af9b3-395">For å gjøre dette går du til **HR delte stillinger > Stillinger > Avdelinger må oppgis for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="af9b3-396">Det anbefales at denne innstillingen iverksettes for integreringen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="af9b3-397">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="af9b3-397">Job types</span></span>

<span data-ttu-id="af9b3-398">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="af9b3-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="af9b3-399">Jobbtyper kreves for å kunne behandle lønn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="af9b3-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="af9b3-400">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="af9b3-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="af9b3-401">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="af9b3-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="af9b3-402">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="af9b3-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="af9b3-403">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="af9b3-403">Job type</span></span>   | <span data-ttu-id="af9b3-404">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="af9b3-405">Per time</span><span class="sxs-lookup"><span data-stu-id="af9b3-405">Hourly</span></span>     | <span data-ttu-id="af9b3-406">Per time</span><span class="sxs-lookup"><span data-stu-id="af9b3-406">Hourly</span></span>      |
| <span data-ttu-id="af9b3-407">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="af9b3-407">Salaried</span></span>   | <span data-ttu-id="af9b3-408">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="af9b3-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="af9b3-409">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="af9b3-409">Position types</span></span> 

<span data-ttu-id="af9b3-410">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="af9b3-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="af9b3-411">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="af9b3-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="af9b3-412">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="af9b3-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="af9b3-413">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="af9b3-413">Position type</span></span>   | <span data-ttu-id="af9b3-414">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="af9b3-415">Heltid</span><span class="sxs-lookup"><span data-stu-id="af9b3-415">Full-time</span></span>       | <span data-ttu-id="af9b3-416">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="af9b3-416">Full time employee</span></span> |
| <span data-ttu-id="af9b3-417">Deltid</span><span class="sxs-lookup"><span data-stu-id="af9b3-417">Part-time</span></span>       | <span data-ttu-id="af9b3-418">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="af9b3-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="af9b3-419">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="af9b3-419">Reason codes</span></span>

<span data-ttu-id="af9b3-420">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="af9b3-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="af9b3-421">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="af9b3-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="af9b3-422">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="af9b3-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="af9b3-423">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="af9b3-423">Reason code</span></span>    | <span data-ttu-id="af9b3-424">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-424">Description</span></span>      | <span data-ttu-id="af9b3-425">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="af9b3-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="af9b3-426">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="af9b3-426">RESIGNATION</span></span>    | <span data-ttu-id="af9b3-427">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-427">Resignation</span></span>      | <span data-ttu-id="af9b3-428">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-428">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-429">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="af9b3-429">TERMINATION</span></span>    | <span data-ttu-id="af9b3-430">Avslutning</span><span class="sxs-lookup"><span data-stu-id="af9b3-430">Termination</span></span>      | <span data-ttu-id="af9b3-431">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-431">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-432">AVGANG VED PENSJON</span><span class="sxs-lookup"><span data-stu-id="af9b3-432">RETIREMENT</span></span>     | <span data-ttu-id="af9b3-433">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-433">Retirement</span></span>       | <span data-ttu-id="af9b3-434">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-434">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-435">ANNET</span><span class="sxs-lookup"><span data-stu-id="af9b3-435">OTHER</span></span>          | <span data-ttu-id="af9b3-436">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="af9b3-436">Other Reasons</span></span>    | <span data-ttu-id="af9b3-437">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-437">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-438">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="af9b3-438">DEATH</span></span>          | <span data-ttu-id="af9b3-439">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="af9b3-439">Death</span></span>            | <span data-ttu-id="af9b3-440">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-440">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-441">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="af9b3-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="af9b3-442">Permisjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-442">Leave of Absence</span></span> | <span data-ttu-id="af9b3-443">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-443">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-444">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="af9b3-444">CONTRACTEND</span></span>    | <span data-ttu-id="af9b3-445">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="af9b3-445">End of Contract</span></span>  | <span data-ttu-id="af9b3-446">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-446">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-447">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="af9b3-447">SALARYCHANGE</span></span>   | <span data-ttu-id="af9b3-448">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="af9b3-448">Change of Salary</span></span> | <span data-ttu-id="af9b3-449">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="af9b3-450">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="af9b3-450">Marital status</span></span>

<span data-ttu-id="af9b3-451">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="af9b3-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="af9b3-452">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="af9b3-453">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-453">Human Resources</span></span>                 | <span data-ttu-id="af9b3-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="af9b3-455">Gift</span><span class="sxs-lookup"><span data-stu-id="af9b3-455">Married</span></span>                | <span data-ttu-id="af9b3-456">Gift</span><span class="sxs-lookup"><span data-stu-id="af9b3-456">Married</span></span>              |
| <span data-ttu-id="af9b3-457">Ugift</span><span class="sxs-lookup"><span data-stu-id="af9b3-457">Single</span></span>                 | <span data-ttu-id="af9b3-458">Ugift</span><span class="sxs-lookup"><span data-stu-id="af9b3-458">Single</span></span>               |
| <span data-ttu-id="af9b3-459">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="af9b3-459">Widowed</span></span>                | <span data-ttu-id="af9b3-460">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="af9b3-460">Widowed</span></span>              |
| <span data-ttu-id="af9b3-461">Skilt</span><span class="sxs-lookup"><span data-stu-id="af9b3-461">Divorced</span></span>               | <span data-ttu-id="af9b3-462">Skilt</span><span class="sxs-lookup"><span data-stu-id="af9b3-462">Divorced</span></span>             |
| <span data-ttu-id="af9b3-463">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="af9b3-463">Registered Partnership</span></span> | <span data-ttu-id="af9b3-464">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="af9b3-464">Domestic Partnership</span></span> |
| <span data-ttu-id="af9b3-465">None</span><span class="sxs-lookup"><span data-stu-id="af9b3-465">None</span></span>                   | <span data-ttu-id="af9b3-466">None</span><span class="sxs-lookup"><span data-stu-id="af9b3-466">None</span></span>                 |
| <span data-ttu-id="af9b3-467">Samboer</span><span class="sxs-lookup"><span data-stu-id="af9b3-467">Cohabiting</span></span>             | <span data-ttu-id="af9b3-468">Samboer</span><span class="sxs-lookup"><span data-stu-id="af9b3-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="af9b3-469">Kjønn</span><span class="sxs-lookup"><span data-stu-id="af9b3-469">Gender</span></span>

<span data-ttu-id="af9b3-470">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="af9b3-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="af9b3-471">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="af9b3-472">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-472">Human Resources</span></span>       | <span data-ttu-id="af9b3-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="af9b3-474">Mann</span><span class="sxs-lookup"><span data-stu-id="af9b3-474">Male</span></span>         | <span data-ttu-id="af9b3-475">Mann</span><span class="sxs-lookup"><span data-stu-id="af9b3-475">Male</span></span>            |
| <span data-ttu-id="af9b3-476">Kvinne</span><span class="sxs-lookup"><span data-stu-id="af9b3-476">Female</span></span>       | <span data-ttu-id="af9b3-477">Kvinne</span><span class="sxs-lookup"><span data-stu-id="af9b3-477">Female</span></span>          |
| <span data-ttu-id="af9b3-478">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="af9b3-478">Non-specific</span></span> | <span data-ttu-id="af9b3-479">*Støttes ikke*</span><span class="sxs-lookup"><span data-stu-id="af9b3-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="af9b3-480">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="af9b3-480">Earning codes</span></span>

<span data-ttu-id="af9b3-481">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="af9b3-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="af9b3-482">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="af9b3-483">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="af9b3-484">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="af9b3-484">Supported frequencies</span></span>

- <span data-ttu-id="af9b3-485">Alle</span><span class="sxs-lookup"><span data-stu-id="af9b3-485">All</span></span>
- <span data-ttu-id="af9b3-486">HVERBET</span><span class="sxs-lookup"><span data-stu-id="af9b3-486">EVERYPAY</span></span>
- <span data-ttu-id="af9b3-487">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="af9b3-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="af9b3-488">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="af9b3-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="af9b3-489">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="af9b3-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="af9b3-490">1IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-490">1OFMTH</span></span>
- <span data-ttu-id="af9b3-491">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-491">LASTOFMTH</span></span>
- <span data-ttu-id="af9b3-492">2IMDN</span><span class="sxs-lookup"><span data-stu-id="af9b3-492">2OFMTH</span></span>
- <span data-ttu-id="af9b3-493">3IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-493">3OFMTH</span></span>
- <span data-ttu-id="af9b3-494">4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-494">4OFMTH</span></span>
- <span data-ttu-id="af9b3-495">5IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-495">5OFMTH</span></span>
- <span data-ttu-id="af9b3-496">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-496">1N2OFMTH</span></span>
- <span data-ttu-id="af9b3-497">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-497">3N4OFMTH</span></span>
- <span data-ttu-id="af9b3-498">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-498">1N3OFMTH</span></span>
- <span data-ttu-id="af9b3-499">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-499">1N4OFMTH</span></span>
- <span data-ttu-id="af9b3-500">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-500">2N3OFMTH</span></span>
- <span data-ttu-id="af9b3-501">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-501">2N4OFMTH</span></span>
- <span data-ttu-id="af9b3-502">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="af9b3-503">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="af9b3-504">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="af9b3-505">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="af9b3-506">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="af9b3-507">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="af9b3-508">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="af9b3-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="af9b3-509">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="af9b3-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="af9b3-510">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="af9b3-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="af9b3-511">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="af9b3-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="af9b3-512">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="af9b3-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="af9b3-513">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="af9b3-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="af9b3-514">Adresser</span><span class="sxs-lookup"><span data-stu-id="af9b3-514">Addresses</span></span>

<span data-ttu-id="af9b3-515">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="af9b3-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="af9b3-516">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="af9b3-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="af9b3-517">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-517">Human Resources</span></span>          | <span data-ttu-id="af9b3-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="af9b3-519">Land/område</span><span class="sxs-lookup"><span data-stu-id="af9b3-519">Country/Region</span></span>  | <span data-ttu-id="af9b3-520">Landskode</span><span class="sxs-lookup"><span data-stu-id="af9b3-520">Country Code</span></span>          |
| <span data-ttu-id="af9b3-521">Postnummer</span><span class="sxs-lookup"><span data-stu-id="af9b3-521">Zip/Postal Code</span></span> | <span data-ttu-id="af9b3-522">Postnummer</span><span class="sxs-lookup"><span data-stu-id="af9b3-522">Postal Code</span></span>           |
| <span data-ttu-id="af9b3-523">Delstat</span><span class="sxs-lookup"><span data-stu-id="af9b3-523">State</span></span>           | <span data-ttu-id="af9b3-524">Statskode</span><span class="sxs-lookup"><span data-stu-id="af9b3-524">State Code</span></span>            |
| <span data-ttu-id="af9b3-525">By</span><span class="sxs-lookup"><span data-stu-id="af9b3-525">City</span></span>            | <span data-ttu-id="af9b3-526">By</span><span class="sxs-lookup"><span data-stu-id="af9b3-526">City</span></span>                  |
| <span data-ttu-id="af9b3-527">Kommune</span><span class="sxs-lookup"><span data-stu-id="af9b3-527">County</span></span>          | <span data-ttu-id="af9b3-528">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="af9b3-528">County (Municipality)</span></span> |
| <span data-ttu-id="af9b3-529">Gate</span><span class="sxs-lookup"><span data-stu-id="af9b3-529">Street</span></span>          | <span data-ttu-id="af9b3-530">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="af9b3-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="af9b3-531">Avgiftsområder</span><span class="sxs-lookup"><span data-stu-id="af9b3-531">Tax regions</span></span>

<span data-ttu-id="af9b3-532">Avgiftsområder brukes til å bestemme den gjeldende avgiften som skal brukes ved generering av lønn.</span><span class="sxs-lookup"><span data-stu-id="af9b3-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="af9b3-533">Avgiftsområder er tilordnet Dayforce som stedsadresser.</span><span class="sxs-lookup"><span data-stu-id="af9b3-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="af9b3-534">Standard avgiftområde må være knyttet til arbeiderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="af9b3-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="af9b3-535">Avgiftsområde (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-535">Tax region (required)</span></span>
- <span data-ttu-id="af9b3-536">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-536">Country/Region (required)</span></span>
- <span data-ttu-id="af9b3-537">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-537">State (required)</span></span>
- <span data-ttu-id="af9b3-538">Kommune</span><span class="sxs-lookup"><span data-stu-id="af9b3-538">County</span></span> 
- <span data-ttu-id="af9b3-539">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="af9b3-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="af9b3-540">Konfigurere data for å generere lønn i Mexico</span><span class="sxs-lookup"><span data-stu-id="af9b3-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="af9b3-541">Hvis du skal generere lønn for ansatte i Mexico, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="af9b3-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="af9b3-542">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="af9b3-542">Departments are required on positions.</span></span>
- <span data-ttu-id="af9b3-543">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="af9b3-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="af9b3-544">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="af9b3-544">Job types</span></span>

<span data-ttu-id="af9b3-545">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="af9b3-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="af9b3-546">Jobbtype kreves for å kunne behandle lønn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="af9b3-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="af9b3-547">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="af9b3-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="af9b3-548">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="af9b3-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="af9b3-549">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="af9b3-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="af9b3-550">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="af9b3-550">Job type</span></span>   | <span data-ttu-id="af9b3-551">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="af9b3-552">Per time</span><span class="sxs-lookup"><span data-stu-id="af9b3-552">Hourly</span></span>     | <span data-ttu-id="af9b3-553">MX per time</span><span class="sxs-lookup"><span data-stu-id="af9b3-553">MX Hourly</span></span>   |
| <span data-ttu-id="af9b3-554">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="af9b3-554">Salaried</span></span>   | <span data-ttu-id="af9b3-555">MX lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="af9b3-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="af9b3-556">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="af9b3-556">Position types</span></span> 

<span data-ttu-id="af9b3-557">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="af9b3-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="af9b3-558">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="af9b3-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="af9b3-559">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="af9b3-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="af9b3-560">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="af9b3-560">Position type</span></span>   | <span data-ttu-id="af9b3-561">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="af9b3-562">Heltid</span><span class="sxs-lookup"><span data-stu-id="af9b3-562">Full-time</span></span>       | <span data-ttu-id="af9b3-563">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="af9b3-563">Full time employee</span></span> |
| <span data-ttu-id="af9b3-564">Deltid</span><span class="sxs-lookup"><span data-stu-id="af9b3-564">Part-time</span></span>       | <span data-ttu-id="af9b3-565">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="af9b3-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="af9b3-566">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="af9b3-566">Reason codes</span></span>

<span data-ttu-id="af9b3-567">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="af9b3-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="af9b3-568">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="af9b3-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="af9b3-569">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="af9b3-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="af9b3-570">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="af9b3-570">Reason code</span></span>            | <span data-ttu-id="af9b3-571">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-571">Description</span></span>                    | <span data-ttu-id="af9b3-572">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="af9b3-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="af9b3-573">AVGANGFØRBETALING</span><span class="sxs-lookup"><span data-stu-id="af9b3-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="af9b3-574">Avgang før første lønn</span><span class="sxs-lookup"><span data-stu-id="af9b3-574">Departure before first payroll</span></span> | <span data-ttu-id="af9b3-575">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-575">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-576">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="af9b3-576">RESIGNATION</span></span>            | <span data-ttu-id="af9b3-577">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-577">Resignation</span></span>                    | <span data-ttu-id="af9b3-578">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-578">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-579">PENSJON</span><span class="sxs-lookup"><span data-stu-id="af9b3-579">PENSION</span></span>                | <span data-ttu-id="af9b3-580">Pensjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-580">Pension</span></span>                        | <span data-ttu-id="af9b3-581">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-581">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-582">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="af9b3-582">TERMINATION</span></span>            | <span data-ttu-id="af9b3-583">Avslutning</span><span class="sxs-lookup"><span data-stu-id="af9b3-583">Termination</span></span>                    | <span data-ttu-id="af9b3-584">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-584">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-585">AVGANGVEDPENSJON</span><span class="sxs-lookup"><span data-stu-id="af9b3-585">RETIREMENT</span></span>             | <span data-ttu-id="af9b3-586">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-586">Retirement</span></span>                     | <span data-ttu-id="af9b3-587">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-587">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-588">FRAVÆRENDEPERSON</span><span class="sxs-lookup"><span data-stu-id="af9b3-588">ABSENTEE</span></span>               | <span data-ttu-id="af9b3-589">Fraværende person</span><span class="sxs-lookup"><span data-stu-id="af9b3-589">Absentee</span></span>                       | <span data-ttu-id="af9b3-590">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-590">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-591">ANNET</span><span class="sxs-lookup"><span data-stu-id="af9b3-591">OTHER</span></span>                  | <span data-ttu-id="af9b3-592">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="af9b3-592">Other Reasons</span></span>                  | <span data-ttu-id="af9b3-593">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-593">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-594">STENGNING</span><span class="sxs-lookup"><span data-stu-id="af9b3-594">CLOSURE</span></span>                | <span data-ttu-id="af9b3-595">Forretning stenger</span><span class="sxs-lookup"><span data-stu-id="af9b3-595">Business Closure</span></span>               | <span data-ttu-id="af9b3-596">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-596">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-597">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="af9b3-597">DEATH</span></span>                  | <span data-ttu-id="af9b3-598">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="af9b3-598">Death</span></span>                          | <span data-ttu-id="af9b3-599">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-599">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-600">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="af9b3-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="af9b3-601">Permisjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-601">Leave of Absence</span></span>               | <span data-ttu-id="af9b3-602">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-602">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-603">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="af9b3-603">CONTRACTEND</span></span>            | <span data-ttu-id="af9b3-604">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="af9b3-604">End of Contract</span></span>                | <span data-ttu-id="af9b3-605">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="af9b3-605">Terminate worker</span></span>     |
| <span data-ttu-id="af9b3-606">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="af9b3-606">SALARYCHANGE</span></span>           | <span data-ttu-id="af9b3-607">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="af9b3-607">Change of Salary</span></span>               | <span data-ttu-id="af9b3-608">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="af9b3-609">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="af9b3-609">Terms of employment</span></span>

<span data-ttu-id="af9b3-610">Ansettelsesbetingelser brukes til å opprette kategorier for ansettelsesbetingelser.</span><span class="sxs-lookup"><span data-stu-id="af9b3-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="af9b3-611">Vilkårene tilordnes til Dayforce som ansettelseindikatorverdier.</span><span class="sxs-lookup"><span data-stu-id="af9b3-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="af9b3-612">Følgende betingelsene for ansettelse og beskrivelser kreves.</span><span class="sxs-lookup"><span data-stu-id="af9b3-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="af9b3-613">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="af9b3-613">Terms of employment</span></span>   | <span data-ttu-id="af9b3-614">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="af9b3-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="af9b3-615">Vanlig</span><span class="sxs-lookup"><span data-stu-id="af9b3-615">Regular</span></span>               | <span data-ttu-id="af9b3-616">Vanlig</span><span class="sxs-lookup"><span data-stu-id="af9b3-616">Regular</span></span>     |
| <span data-ttu-id="af9b3-617">Direkte</span><span class="sxs-lookup"><span data-stu-id="af9b3-617">Direct</span></span>                | <span data-ttu-id="af9b3-618">Direkte</span><span class="sxs-lookup"><span data-stu-id="af9b3-618">Direct</span></span>      |
| <span data-ttu-id="af9b3-619">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="af9b3-619">Internship</span></span>            | <span data-ttu-id="af9b3-620">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="af9b3-620">Internship</span></span>  |
| <span data-ttu-id="af9b3-621">Permanent</span><span class="sxs-lookup"><span data-stu-id="af9b3-621">Permanent</span></span>             | <span data-ttu-id="af9b3-622">Permanent</span><span class="sxs-lookup"><span data-stu-id="af9b3-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="af9b3-623">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="af9b3-623">Marital status</span></span>

<span data-ttu-id="af9b3-624">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="af9b3-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="af9b3-625">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="af9b3-626">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-626">Human Resources</span></span>                 | <span data-ttu-id="af9b3-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="af9b3-628">Gift</span><span class="sxs-lookup"><span data-stu-id="af9b3-628">Married</span></span>                | <span data-ttu-id="af9b3-629">Gift</span><span class="sxs-lookup"><span data-stu-id="af9b3-629">Married</span></span>                   |
| <span data-ttu-id="af9b3-630">Ugift</span><span class="sxs-lookup"><span data-stu-id="af9b3-630">Single</span></span>                 | <span data-ttu-id="af9b3-631">Ugift</span><span class="sxs-lookup"><span data-stu-id="af9b3-631">Single</span></span>                    |
| <span data-ttu-id="af9b3-632">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="af9b3-632">Widowed</span></span>                | <span data-ttu-id="af9b3-633">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="af9b3-633">Widowed</span></span>                   |
| <span data-ttu-id="af9b3-634">Skilt</span><span class="sxs-lookup"><span data-stu-id="af9b3-634">Divorced</span></span>               | <span data-ttu-id="af9b3-635">Skilt</span><span class="sxs-lookup"><span data-stu-id="af9b3-635">Divorced</span></span>                  |
| <span data-ttu-id="af9b3-636">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="af9b3-636">Registered Partnership</span></span> | <span data-ttu-id="af9b3-637">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="af9b3-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="af9b3-638">None</span><span class="sxs-lookup"><span data-stu-id="af9b3-638">None</span></span>                   | <span data-ttu-id="af9b3-639">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="af9b3-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="af9b3-640">Samboer</span><span class="sxs-lookup"><span data-stu-id="af9b3-640">Cohabiting</span></span>             | <span data-ttu-id="af9b3-641">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="af9b3-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="af9b3-642">Kjønn</span><span class="sxs-lookup"><span data-stu-id="af9b3-642">Gender</span></span>

<span data-ttu-id="af9b3-643">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="af9b3-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="af9b3-644">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="af9b3-645">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-645">Human Resources</span></span>       | <span data-ttu-id="af9b3-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="af9b3-647">Mann</span><span class="sxs-lookup"><span data-stu-id="af9b3-647">Male</span></span>         | <span data-ttu-id="af9b3-648">Mann</span><span class="sxs-lookup"><span data-stu-id="af9b3-648">Male</span></span>                      |
| <span data-ttu-id="af9b3-649">Kvinne</span><span class="sxs-lookup"><span data-stu-id="af9b3-649">Female</span></span>       | <span data-ttu-id="af9b3-650">Kvinne</span><span class="sxs-lookup"><span data-stu-id="af9b3-650">Female</span></span>                    |
| <span data-ttu-id="af9b3-651">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="af9b3-651">Non-specific</span></span> | <span data-ttu-id="af9b3-652">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="af9b3-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="af9b3-653">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="af9b3-653">Payment method</span></span>

<span data-ttu-id="af9b3-654">Betalingsmåter gir den ansatte og firmaet en måte å beskrive hvordan ansatte skal betales.</span><span class="sxs-lookup"><span data-stu-id="af9b3-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="af9b3-655">Betalingsmåter tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="af9b3-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="af9b3-656">Tabellen nedenfor viser hvordan betalingsmåter tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="af9b3-657">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-657">Human Resources</span></span>             | <span data-ttu-id="af9b3-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="af9b3-659">Kontant</span><span class="sxs-lookup"><span data-stu-id="af9b3-659">Cash</span></span>               | <span data-ttu-id="af9b3-660">Kontant</span><span class="sxs-lookup"><span data-stu-id="af9b3-660">Cash</span></span>                      |
| <span data-ttu-id="af9b3-661">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="af9b3-661">Electronic Payment</span></span> | <span data-ttu-id="af9b3-662">Overfør</span><span class="sxs-lookup"><span data-stu-id="af9b3-662">Transfer</span></span>                  |
| <span data-ttu-id="af9b3-663">Kontroll</span><span class="sxs-lookup"><span data-stu-id="af9b3-663">Check</span></span>              | <span data-ttu-id="af9b3-664">Sjekk</span><span class="sxs-lookup"><span data-stu-id="af9b3-664">Cheque</span></span>                    |
| <span data-ttu-id="af9b3-665">Bankoverføring</span><span class="sxs-lookup"><span data-stu-id="af9b3-665">Bank Draft</span></span>         | <span data-ttu-id="af9b3-666">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="af9b3-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="af9b3-667">Annet</span><span class="sxs-lookup"><span data-stu-id="af9b3-667">Other</span></span>              | <span data-ttu-id="af9b3-668">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="af9b3-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="af9b3-669">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="af9b3-669">Bank account type</span></span>

<span data-ttu-id="af9b3-670">Bankkontotypene brukes for elektroniske betalinger til ansatte.</span><span class="sxs-lookup"><span data-stu-id="af9b3-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="af9b3-671">Bankkontotypene tilordnes til Dayforce som overføringskontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="af9b3-672">Bankkontotypene oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="af9b3-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="af9b3-673">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-673">Human Resources</span></span>            | <span data-ttu-id="af9b3-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="af9b3-675">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="af9b3-675">Checking Account</span></span>  | <span data-ttu-id="af9b3-676">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="af9b3-676">CheckingAccount</span></span>           |
| <span data-ttu-id="af9b3-677">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="af9b3-677">Payroll Account</span></span>   | <span data-ttu-id="af9b3-678">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="af9b3-678">PayrollAccount</span></span>            |
| <span data-ttu-id="af9b3-679">Sparekonto</span><span class="sxs-lookup"><span data-stu-id="af9b3-679">Savings Account</span></span>   | <span data-ttu-id="af9b3-680">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="af9b3-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="af9b3-681">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="af9b3-681">BankGirot account</span></span> | <span data-ttu-id="af9b3-682">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="af9b3-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="af9b3-683">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="af9b3-683">PlusGirot account</span></span> | <span data-ttu-id="af9b3-684">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="af9b3-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="af9b3-685">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="af9b3-685">Earning codes</span></span>

<span data-ttu-id="af9b3-686">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="af9b3-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="af9b3-687">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="af9b3-688">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="af9b3-689">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="af9b3-689">Supported frequencies</span></span>

- <span data-ttu-id="af9b3-690">Alle</span><span class="sxs-lookup"><span data-stu-id="af9b3-690">All</span></span>
- <span data-ttu-id="af9b3-691">HVERBET</span><span class="sxs-lookup"><span data-stu-id="af9b3-691">EVERYPAY</span></span>
- <span data-ttu-id="af9b3-692">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="af9b3-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="af9b3-693">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="af9b3-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="af9b3-694">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="af9b3-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="af9b3-695">1IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-695">1OFMTH</span></span>
- <span data-ttu-id="af9b3-696">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-696">LASTOFMTH</span></span>
- <span data-ttu-id="af9b3-697">2IMDN</span><span class="sxs-lookup"><span data-stu-id="af9b3-697">2OFMTH</span></span>
- <span data-ttu-id="af9b3-698">3IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-698">3OFMTH</span></span>
- <span data-ttu-id="af9b3-699">4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-699">4OFMTH</span></span>
- <span data-ttu-id="af9b3-700">5IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-700">5OFMTH</span></span>
- <span data-ttu-id="af9b3-701">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-701">1N2OFMTH</span></span>
- <span data-ttu-id="af9b3-702">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-702">3N4OFMTH</span></span>
- <span data-ttu-id="af9b3-703">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-703">1N3OFMTH</span></span>
- <span data-ttu-id="af9b3-704">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-704">1N4OFMTH</span></span>
- <span data-ttu-id="af9b3-705">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-705">2N3OFMTH</span></span>
- <span data-ttu-id="af9b3-706">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-706">2N4OFMTH</span></span>
- <span data-ttu-id="af9b3-707">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="af9b3-708">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="af9b3-709">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="af9b3-710">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="af9b3-711">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="af9b3-712">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="af9b3-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="af9b3-713">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="af9b3-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="af9b3-714">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="af9b3-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="af9b3-715">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="af9b3-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="af9b3-716">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="af9b3-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="af9b3-717">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="af9b3-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="af9b3-718">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="af9b3-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="af9b3-719">Adresser</span><span class="sxs-lookup"><span data-stu-id="af9b3-719">Addresses</span></span>

<span data-ttu-id="af9b3-720">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="af9b3-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="af9b3-721">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="af9b3-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="af9b3-722">Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="af9b3-722">Human Resources</span></span>              | <span data-ttu-id="af9b3-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="af9b3-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="af9b3-724">Land/område</span><span class="sxs-lookup"><span data-stu-id="af9b3-724">Country/Region</span></span>      | <span data-ttu-id="af9b3-725">Landskode</span><span class="sxs-lookup"><span data-stu-id="af9b3-725">Country Code</span></span>          |
| <span data-ttu-id="af9b3-726">Postnummer</span><span class="sxs-lookup"><span data-stu-id="af9b3-726">Zip/Postal Code</span></span>     | <span data-ttu-id="af9b3-727">Postnummer</span><span class="sxs-lookup"><span data-stu-id="af9b3-727">Postal Code</span></span>           |
| <span data-ttu-id="af9b3-728">Delstat</span><span class="sxs-lookup"><span data-stu-id="af9b3-728">State</span></span>               | <span data-ttu-id="af9b3-729">Statskode</span><span class="sxs-lookup"><span data-stu-id="af9b3-729">State Code</span></span>            |
| <span data-ttu-id="af9b3-730">By</span><span class="sxs-lookup"><span data-stu-id="af9b3-730">City</span></span>                | <span data-ttu-id="af9b3-731">By</span><span class="sxs-lookup"><span data-stu-id="af9b3-731">City</span></span>                  |
| <span data-ttu-id="af9b3-732">Kommune</span><span class="sxs-lookup"><span data-stu-id="af9b3-732">County</span></span>              | <span data-ttu-id="af9b3-733">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="af9b3-733">County (Municipality)</span></span> |
| <span data-ttu-id="af9b3-734">Gate</span><span class="sxs-lookup"><span data-stu-id="af9b3-734">Street</span></span>              | <span data-ttu-id="af9b3-735">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="af9b3-735">Address Line 1</span></span>        |
| <span data-ttu-id="af9b3-736">Gatenummer</span><span class="sxs-lookup"><span data-stu-id="af9b3-736">Street Number</span></span>       | <span data-ttu-id="af9b3-737">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="af9b3-737">Address Line 2</span></span>        |
| <span data-ttu-id="af9b3-738">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="af9b3-738">Building Complement</span></span> | <span data-ttu-id="af9b3-739">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="af9b3-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="af9b3-740">Passnummer</span><span class="sxs-lookup"><span data-stu-id="af9b3-740">Passport number</span></span>

<span data-ttu-id="af9b3-741">Ansatte kan deklarere passinformasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-741">Employees can declare passport information.</span></span> <span data-ttu-id="af9b3-742">Denne informasjonen er av **Pass**-identifikasjonstypen og er integrert i Dayforce som en del av en ansatts Mexico-spesifikke informasjon.</span><span class="sxs-lookup"><span data-stu-id="af9b3-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="af9b3-743">Identifikasjonstype = "Pass"</span><span class="sxs-lookup"><span data-stu-id="af9b3-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="af9b3-744">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-744">Issued Date</span></span>
- <span data-ttu-id="af9b3-745">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="af9b3-745">Expiration Date</span></span>

<span data-ttu-id="af9b3-746">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **Pass**.</span><span class="sxs-lookup"><span data-stu-id="af9b3-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="af9b3-747">Men bare den gjeldende aktive passoppføringen er integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="af9b3-748">Hvis alle passoppføringer er utløpt, er passet som sist ble utstedt, integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="af9b3-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
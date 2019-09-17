---
title: Konfigurere lønnsintegreringen mellom Talent og Dayforce
description: Dette emnet forklarer hvordan du konfigurerer integrasjonen mellom Microsoft Dynamics 365 for Talent og Ceridian Dayforce slik at du kan behandle en lønnskjøring.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: c26dfed9909b0dbd05fc18c206e5adc947feaef5
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742923"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="15edd-103">Konfigurere lønnsintegrering mellom Talent og Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="15edd-104">Integrasjonen mellom Microsoft Dynamics 365 for Talent og Ceridian Dayforce bruker flere konfigurasjonstrinn som er beskrevet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="15edd-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="15edd-105">Du må konfigurere integreringen i både Talent og Dayforce før du kan behandle en lønnskjøring.</span><span class="sxs-lookup"><span data-stu-id="15edd-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="15edd-106">Når du bruker en tjeneste som Dayforce til å fullføre lønnskjøringer, må du aktivere integrering i Talent.</span><span class="sxs-lookup"><span data-stu-id="15edd-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="15edd-107">Integreringen krever bestemte data fra Talent.</span><span class="sxs-lookup"><span data-stu-id="15edd-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="15edd-108">Derfor må du kontrollere at data som tilordnes til Dayforce, er konfigurert i Talent på en måte som støtter integreringen.</span><span class="sxs-lookup"><span data-stu-id="15edd-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="15edd-109">Integrasjonen bruker følgende brede datakategorier:</span><span class="sxs-lookup"><span data-stu-id="15edd-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="15edd-110">Personaldata</span><span class="sxs-lookup"><span data-stu-id="15edd-110">Human resources data</span></span>
- <span data-ttu-id="15edd-111">Kompensasjonsdata</span><span class="sxs-lookup"><span data-stu-id="15edd-111">Compensation data</span></span>
- <span data-ttu-id="15edd-112">Lønnsdata, for eksempel lønnssykluser, lønnsperioder og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="15edd-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="15edd-113">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="15edd-113">Worker data</span></span>

<span data-ttu-id="15edd-114">Dette emnet beskriver trinnene du må følge for å aktivere integreringen.</span><span class="sxs-lookup"><span data-stu-id="15edd-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="15edd-115">Den beskriver også hvilke typer data og konfigurasjonsdetaljer som integreringen krever.</span><span class="sxs-lookup"><span data-stu-id="15edd-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="15edd-116">Aktivere integrasjonen</span><span class="sxs-lookup"><span data-stu-id="15edd-116">Enable the integration</span></span>

<span data-ttu-id="15edd-117">I Talent må du aktivere integreringen og angi konfigurasjonsinformasjonen for å koble til Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="15edd-118">Hvis du vil at økonomimodultransaksjonen som produseres, skal importeres til Microsoft Dynamics 365 for Finance and Operations, må du også definere en Microsoft Azure-lagringskonto og angi Azure Storage-tilkoblingsstrengen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15edd-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="15edd-119">Følg denne fremgangsmåten for å aktivere integrasjonen i Talent.</span><span class="sxs-lookup"><span data-stu-id="15edd-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="15edd-120">Velg **Konfigurasjon av integrering** på siden **Systemadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="15edd-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="15edd-121">Angi sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="15edd-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="15edd-122">Angi brukernavnet og passordet til brukeren som skal ha tilgang til sikkert FTP-sluttpunkt og sikker FTP-mappebane.</span><span class="sxs-lookup"><span data-stu-id="15edd-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="15edd-123">Test tilkoblingen etter behov, og sett alternativet **Aktiver lønnsintegrering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="15edd-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="15edd-124">Når integreringen er slått på, opprettes dataeksportpakken og -filene, og frekvensen angis.</span><span class="sxs-lookup"><span data-stu-id="15edd-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="15edd-125">Du kan endre denne frekvensen etter behov.</span><span class="sxs-lookup"><span data-stu-id="15edd-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="15edd-126">Hvis du vil ha mer informasjon om Azure Storage-kontoer og Azure Storage-tilkoblingsstrenger, kan du se følgende Azure-emner:</span><span class="sxs-lookup"><span data-stu-id="15edd-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="15edd-127">Om Azure Storage-kontoer</span><span class="sxs-lookup"><span data-stu-id="15edd-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="15edd-128">Konfigurere Azure Storage-tilkoblingsstrenger</span><span class="sxs-lookup"><span data-stu-id="15edd-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="15edd-129">Tekniske detaljer når lønnsintegrasjon er aktivert</span><span class="sxs-lookup"><span data-stu-id="15edd-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="15edd-130">Aktivering av lønnsintegrasjonen har to hovedvirkninger:</span><span class="sxs-lookup"><span data-stu-id="15edd-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="15edd-131">Det opprettes et dataeksportprosjekt kalt «Eksport av lønnsintegrasjon».</span><span class="sxs-lookup"><span data-stu-id="15edd-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="15edd-132">Dette prosjektet inneholder enhetene og feltene som kreves for lønnsintegrasjonen.</span><span class="sxs-lookup"><span data-stu-id="15edd-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="15edd-133">Du kan undersøke prosjektet ved å gå til **Systemadministrasjon**, velge **Databehandling**-flisen og deretter åpne dataprosjektet fra listen over prosjekter.</span><span class="sxs-lookup"><span data-stu-id="15edd-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="15edd-134">Denne satsvise jobben utfører dataeksportprosjektet, krypterer den resulterende datapakken og overfører datapakkefilen til SFTP-endepunktet som er konfigurert på skjermen **Konfigurasjon av integrering**.</span><span class="sxs-lookup"><span data-stu-id="15edd-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="15edd-135">Datapakken som overføres til SFTP-endepunktet, krypteres ved hjelp av en nøkkel som er unik for pakken.</span><span class="sxs-lookup"><span data-stu-id="15edd-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="15edd-136">Nøkkelen er i et Azure Key Vault som bare Ceridian har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="15edd-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="15edd-137">Det går ikke an å dekryptere og undersøke innholdet i datapakken.</span><span class="sxs-lookup"><span data-stu-id="15edd-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="15edd-138">Hvis du må undersøke innholdet i datapakken, må du eksportere dataprosjektet «Eksport av lønnsintegrasjon» manuelt, laste det ned, og deretter åpne det.</span><span class="sxs-lookup"><span data-stu-id="15edd-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="15edd-139">Pakken verken krypteres eller overføres når du foretar manuell eksport.</span><span class="sxs-lookup"><span data-stu-id="15edd-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="15edd-140">Konfigurere dataene dine</span><span class="sxs-lookup"><span data-stu-id="15edd-140">Configure your data</span></span> 

<span data-ttu-id="15edd-141">For å behandle lønn må du konfigurere Personaldata i Talent.</span><span class="sxs-lookup"><span data-stu-id="15edd-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="15edd-142">Du må definere organisasjonsdata, for eksempel jobber og stillinger, samt informasjon om fordeler og kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="15edd-143">Denne informasjonen gir informasjon om ansettelse, lønn og trekk som kreves for å kunne generere lønn for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="15edd-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="15edd-144">Personaldata</span><span class="sxs-lookup"><span data-stu-id="15edd-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="15edd-145">Fordeler</span><span class="sxs-lookup"><span data-stu-id="15edd-145">Benefits</span></span> 

<span data-ttu-id="15edd-146">Personale inneholder verktøy for oppsett og vedlikehold av fordeler, fradrag og arbeiderkompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere.</span><span class="sxs-lookup"><span data-stu-id="15edd-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="15edd-147">Når du oppretter fordeler, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="15edd-148">Fordelsplaner</span><span class="sxs-lookup"><span data-stu-id="15edd-148">Benefit plans</span></span>

- <span data-ttu-id="15edd-149">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-149">Plan (required)</span></span>
- <span data-ttu-id="15edd-150">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-150">Type (required)</span></span>
- <span data-ttu-id="15edd-151">Lønnsinnvirkning (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-151">Payroll impact (required)</span></span>
- <span data-ttu-id="15edd-152">Gjenopprett etterskudd</span><span class="sxs-lookup"><span data-stu-id="15edd-152">Recover arrears</span></span>
- <span data-ttu-id="15edd-153">Fradragsmetode</span><span class="sxs-lookup"><span data-stu-id="15edd-153">Deduction method</span></span>
- <span data-ttu-id="15edd-154">Fradragsprioritet</span><span class="sxs-lookup"><span data-stu-id="15edd-154">Deduction priority</span></span>
- <span data-ttu-id="15edd-155">Begrens periode</span><span class="sxs-lookup"><span data-stu-id="15edd-155">Limit period</span></span>
- <span data-ttu-id="15edd-156">Grensebeløp</span><span class="sxs-lookup"><span data-stu-id="15edd-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="15edd-157">Fordeler</span><span class="sxs-lookup"><span data-stu-id="15edd-157">Benefits</span></span>

- <span data-ttu-id="15edd-158">Plan (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-158">Plan (required)</span></span>
- <span data-ttu-id="15edd-159">Type (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-159">Type (required)</span></span>
- <span data-ttu-id="15edd-160">Alternativ (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-160">Option (required)</span></span>
- <span data-ttu-id="15edd-161">Fordel-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-161">Benefit ID (required)</span></span>
- <span data-ttu-id="15edd-162">Frekvens</span><span class="sxs-lookup"><span data-stu-id="15edd-162">Frequency</span></span>
- <span data-ttu-id="15edd-163">Grunnlag</span><span class="sxs-lookup"><span data-stu-id="15edd-163">Basis</span></span>
- <span data-ttu-id="15edd-164">Beløp eller sats</span><span class="sxs-lookup"><span data-stu-id="15edd-164">Amount or rate</span></span>
- <span data-ttu-id="15edd-165">Inntektskode</span><span class="sxs-lookup"><span data-stu-id="15edd-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="15edd-166">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="15edd-166">Supported frequencies</span></span> 

- <span data-ttu-id="15edd-167">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="15edd-167">Weekly</span></span>
- <span data-ttu-id="15edd-168">Annenhver uke</span><span class="sxs-lookup"><span data-stu-id="15edd-168">Bi-weekly</span></span>
- <span data-ttu-id="15edd-169">Halvmånedlig</span><span class="sxs-lookup"><span data-stu-id="15edd-169">Semi-monthly</span></span>
- <span data-ttu-id="15edd-170">Månedlig</span><span class="sxs-lookup"><span data-stu-id="15edd-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="15edd-171">Støttede grunnlag</span><span class="sxs-lookup"><span data-stu-id="15edd-171">Supported bases</span></span> 

- <span data-ttu-id="15edd-172">Fast beløp</span><span class="sxs-lookup"><span data-stu-id="15edd-172">Fixed amount</span></span>
- <span data-ttu-id="15edd-173">Prosentandel av inntekter</span><span class="sxs-lookup"><span data-stu-id="15edd-173">Percent of earnings</span></span>
- <span data-ttu-id="15edd-174">Produktive timer</span><span class="sxs-lookup"><span data-stu-id="15edd-174">Productive hours</span></span>

<span data-ttu-id="15edd-175">Dayforce oppretter følgende fradrag, basert på lønnsinnvirkning som er definert på fordelsplanen.</span><span class="sxs-lookup"><span data-stu-id="15edd-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="15edd-176">Valg i Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-176">Selection in Talent</span></span>        | <span data-ttu-id="15edd-177">Resultat i Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="15edd-178">None</span><span class="sxs-lookup"><span data-stu-id="15edd-178">None</span></span>                       | <span data-ttu-id="15edd-179">Ingen fradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="15edd-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="15edd-180">Bare fradrag</span><span class="sxs-lookup"><span data-stu-id="15edd-180">Deduction only</span></span>             | <span data-ttu-id="15edd-181">Et ansattfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="15edd-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="15edd-182">Bare bidrag</span><span class="sxs-lookup"><span data-stu-id="15edd-182">Contribution only</span></span>          | <span data-ttu-id="15edd-183">Et arbeidsgiverfradrag opprettes.</span><span class="sxs-lookup"><span data-stu-id="15edd-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="15edd-184">Fradrag og bidrag</span><span class="sxs-lookup"><span data-stu-id="15edd-184">Deduction and contribution</span></span> | <span data-ttu-id="15edd-185">Fradrag for ansatte og arbeidsgivere opprettes.</span><span class="sxs-lookup"><span data-stu-id="15edd-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="15edd-186">Hvis du vil ha mer informasjon om hvordan du definerer og administrerer et program for fordeler, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="15edd-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="15edd-187">Levere et program for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="15edd-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="15edd-188">Opprette en ny fordel</span><span class="sxs-lookup"><span data-stu-id="15edd-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="15edd-189">Definere rettighetsregler og policyer for fordel</span><span class="sxs-lookup"><span data-stu-id="15edd-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="15edd-190">Registrere og fjerne fordeler fra arbeidere</span><span class="sxs-lookup"><span data-stu-id="15edd-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="15edd-191">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-191">Compensation</span></span> 

<span data-ttu-id="15edd-192">Kompensasjonsstyring brukes til å kontrollere levering av grunnlønn og bonuser.</span><span class="sxs-lookup"><span data-stu-id="15edd-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="15edd-193">En ansatts faste grunnlønn og personlige tilleggsøkninger styres via faste kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="15edd-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="15edd-194">Betaling av insitamentutbetalinger, for eksempel bonuser, ytelsestillegg, aksjeopsjoner og tilskudd, og også engangsbonuser, kontrolleres via variable kompensasjonsplaner.</span><span class="sxs-lookup"><span data-stu-id="15edd-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="15edd-195">Dayforce bruker kompensasjonsinformasjon til å beregne timesats eller årlig sats for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="15edd-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="15edd-196">Planer for faste kompensasjoner og konverteringer av lønnssats er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="15edd-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="15edd-197">Ansatte må tilknyttes en plan for fast kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="15edd-198">Hvis du vil ha mer informasjon om kompensasjonsplaner, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="15edd-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="15edd-199">Opprette planer for fast kompensasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="15edd-200">Opprette variable kompensasjonsplaner</span><span class="sxs-lookup"><span data-stu-id="15edd-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="15edd-201">Utvikle struktur og planer for lønn/kompensasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="15edd-202">Behandle kompensasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="15edd-203">Definere kompensasjonsprosess og beregne resultater</span><span class="sxs-lookup"><span data-stu-id="15edd-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="15edd-204">Registrere en ansatt i en fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="15edd-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="15edd-205">Registrere en ansatt i en variabel kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="15edd-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="15edd-206">Jobber</span><span class="sxs-lookup"><span data-stu-id="15edd-206">Jobs</span></span> 

<span data-ttu-id="15edd-207">En jobb er en samling oppgaver og ansvarsområder som kreves av en person som utfører en jobb.</span><span class="sxs-lookup"><span data-stu-id="15edd-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="15edd-208">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="15edd-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="15edd-209">Definere komponentene for en jobb</span><span class="sxs-lookup"><span data-stu-id="15edd-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="15edd-210">Definere nye jobber</span><span class="sxs-lookup"><span data-stu-id="15edd-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="15edd-211">Stillinger</span><span class="sxs-lookup"><span data-stu-id="15edd-211">Positions</span></span>

<span data-ttu-id="15edd-212">En stilling er én enkeltforekomst av en jobb.</span><span class="sxs-lookup"><span data-stu-id="15edd-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="15edd-213">"Salgssjef (øst)"-stillingen er for eksempel én av stillingene som er knyttet til jobben "Salgssjef".</span><span class="sxs-lookup"><span data-stu-id="15edd-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="15edd-214">Det finnes en stilling i en avdeling.</span><span class="sxs-lookup"><span data-stu-id="15edd-214">A position exists in a department.</span></span> <span data-ttu-id="15edd-215">Bare én arbeider kan være tilknyttet hvert område.</span><span class="sxs-lookup"><span data-stu-id="15edd-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="15edd-216">Ha følgende data og konfigurasjon i bakhodet når du definerer stillinger:</span><span class="sxs-lookup"><span data-stu-id="15edd-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="15edd-217">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-217">Position (required)</span></span>
- <span data-ttu-id="15edd-218">Beskrivelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-218">Description (required)</span></span>
- <span data-ttu-id="15edd-219">Jobb (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-219">Job (required)</span></span>
- <span data-ttu-id="15edd-220">Avdeling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-220">Department (required)</span></span>
- <span data-ttu-id="15edd-221">Stillingstype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-221">Position type (required)</span></span>
- <span data-ttu-id="15edd-222">Fulltidsekvivalent</span><span class="sxs-lookup"><span data-stu-id="15edd-222">Full-time equivalent</span></span>
- <span data-ttu-id="15edd-223">Årlige vanlige timer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="15edd-224">Betalt av juridisk enhet (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="15edd-225">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-225">Pay cycle (required)</span></span>
- <span data-ttu-id="15edd-226">Standard finansdimensjon – kostsenter (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="15edd-227">Arbeidertilordning – arbeider, start for tilordning, slutt for tilordning, årsakskode</span><span class="sxs-lookup"><span data-stu-id="15edd-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="15edd-228">Hvis flere stillinger i samme avdeling er knyttet til den samme jobben, konsolideres de til én stilling i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="15edd-229">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="15edd-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="15edd-230">Organisere arbeidsstyrken ved bruk av avdelinger, jobber og stillinger</span><span class="sxs-lookup"><span data-stu-id="15edd-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="15edd-231">Definere stillinger</span><span class="sxs-lookup"><span data-stu-id="15edd-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="15edd-232">Avdelinger</span><span class="sxs-lookup"><span data-stu-id="15edd-232">Departments</span></span>

<span data-ttu-id="15edd-233">En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="15edd-234">En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale.</span><span class="sxs-lookup"><span data-stu-id="15edd-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="15edd-235">Du kan bruke avdelinger til å rapportere om funksjonsområder.</span><span class="sxs-lookup"><span data-stu-id="15edd-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="15edd-236">Avdelinger kan ha ansvar for fortjeneste og tap.</span><span class="sxs-lookup"><span data-stu-id="15edd-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="15edd-237">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="15edd-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="15edd-238">Opprette en avdeling og knytte den til avdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="15edd-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="15edd-239">Definere nye avdelinger</span><span class="sxs-lookup"><span data-stu-id="15edd-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="15edd-240">Lønnssykluser og lønnsperioder</span><span class="sxs-lookup"><span data-stu-id="15edd-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="15edd-241">En betalingssyklus avgjør hvor ofte lønnskjøring utføres, og de spesifikke dagene arbeidere lønnes.</span><span class="sxs-lookup"><span data-stu-id="15edd-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="15edd-242">For eksempel kan en lønnssyklus være månedlig, og ansatte kan betales på den siste dagen i måneden.</span><span class="sxs-lookup"><span data-stu-id="15edd-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="15edd-243">En lønnssyklus kan også være ukentlig, og ansatte kan betales tirsdagen etter slutten av lønnsperioden.</span><span class="sxs-lookup"><span data-stu-id="15edd-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="15edd-244">Lønnssykluser tilordnes til stillinger for å styre når arbeidere i disse stillingene lønnes.</span><span class="sxs-lookup"><span data-stu-id="15edd-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="15edd-245">Når du oppretter lønnssykler, kan du generere lønnsperioder for hver enkelt syklus.</span><span class="sxs-lookup"><span data-stu-id="15edd-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="15edd-246">Hver lønnsperiode inkluderer en standard betalingsdato som er basert på informasjonen du angir.</span><span class="sxs-lookup"><span data-stu-id="15edd-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="15edd-247">Du kan imidlertid endre standard betalingsdato i en lønnsperiode for å tillate unntak, for eksempel når betalingsdatoen faller på en helligdag.</span><span class="sxs-lookup"><span data-stu-id="15edd-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="15edd-248">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="15edd-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="15edd-249">Betalingssyklus (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-249">Pay cycle (required)</span></span>
- <span data-ttu-id="15edd-250">Lønnssyklusfrekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="15edd-251">Periodens startdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="15edd-252">Standard betalingsdato (første lønnsperiode er obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="15edd-253">Denne informasjonen er integrert med Dayforce som lønnsgrupper og er inndelt etter land eller område for hver lønnssyklus.</span><span class="sxs-lookup"><span data-stu-id="15edd-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="15edd-254">Minst én lønnsperiode må genereres før integrasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="15edd-255">Dayforce genererer lønnsgruppekalendere og betalingsdatoer basert på startdatoen for den første lønnsperioden og standard betalingsdato som er definert i Talent.</span><span class="sxs-lookup"><span data-stu-id="15edd-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="15edd-256">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="15edd-256">Earning codes</span></span>

<span data-ttu-id="15edd-257">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="15edd-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="15edd-258">Kodene har forskjellige parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="15edd-259">Informasjonen nedenfor brukes i Dayforce:</span><span class="sxs-lookup"><span data-stu-id="15edd-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="15edd-260">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-260">Earning Code (required)</span></span>
- <span data-ttu-id="15edd-261">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="15edd-261">Description</span></span>
- <span data-ttu-id="15edd-262">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="15edd-262">Unit of measure</span></span>
- <span data-ttu-id="15edd-263">Produktiv</span><span class="sxs-lookup"><span data-stu-id="15edd-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="15edd-264">Arbeiderdata</span><span class="sxs-lookup"><span data-stu-id="15edd-264">Worker data</span></span>

<span data-ttu-id="15edd-265">Poster for ulike typer arbeidere som du har, er viktig for personal. og lønnsystemene dine.</span><span class="sxs-lookup"><span data-stu-id="15edd-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="15edd-266">Informasjonen du legger inn, kan brukes til å spore arbeidere og personlig informasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="15edd-267">Du kan vedlikeholde følgende informasjon om arbeidere:</span><span class="sxs-lookup"><span data-stu-id="15edd-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="15edd-268">**Grunnleggende** – Vedlikehold grunnleggende informasjon om en arbeider, for eksempel kontaktinformasjon, demografisk informasjon, identifikasjonsinformasjon, familieinformasjon, militærtjenestestatus, informasjon om personer som bor i utlandet, og personlige kontakter og kontakter i nødfall.</span><span class="sxs-lookup"><span data-stu-id="15edd-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="15edd-269">**Ansettelse** – Vedlikehold informasjon om en arbeiders ansettelse, for eksempel informasjon om firma- eller organisasjonstilknytning, stillingstilordning, start- og sluttdatoer, arbeidstillatelse, vilkår for ansettelse, pensjon, ferie og flytting.</span><span class="sxs-lookup"><span data-stu-id="15edd-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="15edd-270">**Lønn og fravær** – Vedlikehold opplysninger om en arbeiders fravær, for eksempel arbeidskalendere, fraværstransaksjoner og fraværsoppsett.</span><span class="sxs-lookup"><span data-stu-id="15edd-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="15edd-271">**Kompensasjon og lønn** – Vedlikehold informasjon om en arbeiders kompensasjonsplaner og lønn, for eksempel planregistrering, priser, ytelse, provisjon, avgiftsinformasjon, pensjonering og lønnstrekk.</span><span class="sxs-lookup"><span data-stu-id="15edd-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="15edd-272">Når du legger inn arbeiderinformasjon, husk følgende data og konfigurasjoner som brukes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="15edd-273">Generell informasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-273">General information</span></span>

- <span data-ttu-id="15edd-274">Personalnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-274">Personnel number (required)</span></span>
- <span data-ttu-id="15edd-275">Fornavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-275">First name (required)</span></span>
- <span data-ttu-id="15edd-276">Etternavn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-276">Last name (required)</span></span>
- <span data-ttu-id="15edd-277">Mellomnavn</span><span class="sxs-lookup"><span data-stu-id="15edd-277">Middle name</span></span>
- <span data-ttu-id="15edd-278">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="15edd-278">Seniority date</span></span>
- <span data-ttu-id="15edd-279">Kalt</span><span class="sxs-lookup"><span data-stu-id="15edd-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="15edd-280">Personlige opplysninger</span><span class="sxs-lookup"><span data-stu-id="15edd-280">Personal information</span></span>

- <span data-ttu-id="15edd-281">Sivilstand (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-281">Marital status (required)</span></span>
- <span data-ttu-id="15edd-282">Fødselsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-282">Birth date (required)</span></span>
- <span data-ttu-id="15edd-283">Kjønn (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-283">Gender (required)</span></span>
- <span data-ttu-id="15edd-284">Person med funksjonshemminger</span><span class="sxs-lookup"><span data-stu-id="15edd-284">Person with disabilities</span></span>
- <span data-ttu-id="15edd-285">Nasjonalitet land/område (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="15edd-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="15edd-286">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="15edd-286">Address information</span></span>

- <span data-ttu-id="15edd-287">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-287">Primary (required)</span></span>
- <span data-ttu-id="15edd-288">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-288">Country/region (required)</span></span>
- <span data-ttu-id="15edd-289">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-289">Postal code (required)</span></span>
- <span data-ttu-id="15edd-290">Gatenummer (obligatorisk) (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="15edd-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="15edd-291">Bygningsnavn (bare for Mexico)</span><span class="sxs-lookup"><span data-stu-id="15edd-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="15edd-292">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-292">City (required)</span></span>
- <span data-ttu-id="15edd-293">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-293">State (required)</span></span>
- <span data-ttu-id="15edd-294">Land (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="15edd-295">Kontaktinformasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-295">Contact information</span></span> 

- <span data-ttu-id="15edd-296">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-296">Primary (required)</span></span>
- <span data-ttu-id="15edd-297">Kontaktnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-297">Contact number (required)</span></span>
- <span data-ttu-id="15edd-298">Utvidelse</span><span class="sxs-lookup"><span data-stu-id="15edd-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="15edd-299">Lønnsinformasjon og inntektskoder</span><span class="sxs-lookup"><span data-stu-id="15edd-299">Payroll information and earning codes</span></span>

<span data-ttu-id="15edd-300">Ansatte kan tilordnes spesifikke inntekter med en gitt betalingfrekvens og med en foretrukket betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="15edd-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="15edd-301">Følgende felt brukes i Dayforce for å sørge for at disse valgene og innstillingene brukes.</span><span class="sxs-lookup"><span data-stu-id="15edd-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="15edd-302">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="15edd-302">Earning codes</span></span>

- <span data-ttu-id="15edd-303">Stilling (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-303">Position (required)</span></span>
- <span data-ttu-id="15edd-304">Inntektskode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-304">Earning Code (required)</span></span>
- <span data-ttu-id="15edd-305">Frekvens (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-305">Frequency (required)</span></span>
- <span data-ttu-id="15edd-306">Beløp (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="15edd-307">Lønnsinformasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-307">Payroll information</span></span>

- <span data-ttu-id="15edd-308">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="15edd-308">Payment Method</span></span>
- <span data-ttu-id="15edd-309">Økonomisk område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-309">Economic Region (required)</span></span>
- <span data-ttu-id="15edd-310">ID for ansattfordeler</span><span class="sxs-lookup"><span data-stu-id="15edd-310">Employee Benefits ID</span></span>
- <span data-ttu-id="15edd-311">Nasjonalt ID-nummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-311">National ID Number (required)</span></span>
- <span data-ttu-id="15edd-312">Militærtjenestenummer</span><span class="sxs-lookup"><span data-stu-id="15edd-312">Military Service Number</span></span>
- <span data-ttu-id="15edd-313">Skift-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-313">Shift ID (required)</span></span>
- <span data-ttu-id="15edd-314">Avgiftsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-314">Tax Number (required)</span></span>
- <span data-ttu-id="15edd-315">Fagforenings-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-315">Union ID (required)</span></span>
- <span data-ttu-id="15edd-316">Arbeidsdag-ID (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-316">Work Day ID (required)</span></span>
- <span data-ttu-id="15edd-317">Arbeidstillatelsesnummer</span><span class="sxs-lookup"><span data-stu-id="15edd-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="15edd-318">Når det gjelder betalingsmåte støtter Mexico **Kontanter**, **Sjekk** (firmaets fysisk sjekk) og **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="15edd-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="15edd-319">Hvis betalingsmåte ikke er angitt, brukes **Sjekk** som standard.</span><span class="sxs-lookup"><span data-stu-id="15edd-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="15edd-320">Ansettelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="15edd-320">Employment details</span></span>

<span data-ttu-id="15edd-321">Ansettelsesdetaljhistorikk brukes som nøkkelinformasjon til å avlede en ansatts ansettelse-, oppsigelses- og nyansettelsesstatuser i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="15edd-322">Dayforce støtter bare én aktiv ansettelsespost om gangen.</span><span class="sxs-lookup"><span data-stu-id="15edd-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="15edd-323">Startdato for ansettelse (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-323">Employment start date (required)</span></span>
- <span data-ttu-id="15edd-324">Sluttdato for ansettelse</span><span class="sxs-lookup"><span data-stu-id="15edd-324">Employment end date</span></span>
- <span data-ttu-id="15edd-325">Startdato</span><span class="sxs-lookup"><span data-stu-id="15edd-325">Start date</span></span>
- <span data-ttu-id="15edd-326">Justert startdato</span><span class="sxs-lookup"><span data-stu-id="15edd-326">Adjusted start date</span></span>
- <span data-ttu-id="15edd-327">Avslutningsdato (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="15edd-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="15edd-328">Avslutningsårsak (kreves ved avslutning)</span><span class="sxs-lookup"><span data-stu-id="15edd-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="15edd-329">En ansatts nøkkeldatoer avledes ved å bruke følgende informasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="15edd-330">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-330">Talent</span></span>                | <span data-ttu-id="15edd-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15edd-332">Den siste ansettelsesdatoen</span><span class="sxs-lookup"><span data-stu-id="15edd-332">Most recent hire date</span></span> | <span data-ttu-id="15edd-333">Ansettelsesstart for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="15edd-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="15edd-334">Avslutningsdato</span><span class="sxs-lookup"><span data-stu-id="15edd-334">Termination date</span></span>      | <span data-ttu-id="15edd-335">Avslutningsdato for gjeldende ikke-avsluttede ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="15edd-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="15edd-336">Startdato</span><span class="sxs-lookup"><span data-stu-id="15edd-336">Start date</span></span>            | <span data-ttu-id="15edd-337">Justert startdato, startdato eller ansettelsesstart for gjeldende ikke-aktive ansettelseloggpost</span><span class="sxs-lookup"><span data-stu-id="15edd-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="15edd-338">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="15edd-338">Original hire date</span></span>    | <span data-ttu-id="15edd-339">Ansettelsesstart for tidligste ansettelsesloggpost</span><span class="sxs-lookup"><span data-stu-id="15edd-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="15edd-340">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-340">Compensation</span></span>

<span data-ttu-id="15edd-341">En fast kompensasjonsplan må være knyttet til hver ansatts primære stilling i en ansattperiode.</span><span class="sxs-lookup"><span data-stu-id="15edd-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="15edd-342">Denne perioden begynner på datoen da den ansatte ble ansatt (eller startdatoen for ansettelsen), og fortsetter til avslutning.</span><span class="sxs-lookup"><span data-stu-id="15edd-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="15edd-343">Gyldighetsdato (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-343">Effective Date (required)</span></span>
- <span data-ttu-id="15edd-344">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="15edd-344">Expiration date</span></span>
- <span data-ttu-id="15edd-345">Lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-345">Pay Rate (required)</span></span>
- <span data-ttu-id="15edd-346">Konverteringer av lønnssats (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="15edd-347">Tilsvarende årlig (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="15edd-348">Tilsvarende per time (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="15edd-349">Hvis en timebaserte ansatt har flere stillinger, importeres fast kompensasjon for den primære stillingen til Dayforce som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="15edd-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="15edd-350">For ikke-primære stillinger lagres timeprisen til den tilsvarende stillingen i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="15edd-351">Hvis en lønnsansatt har flere stillinger, avledes kumulativ timepris og årslønn på tvers av alle aktive stillinger og brukes som basissats/lønn for ansattnivå.</span><span class="sxs-lookup"><span data-stu-id="15edd-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="15edd-352">Identifikasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="15edd-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="15edd-353">Personnummeridentifikator</span><span class="sxs-lookup"><span data-stu-id="15edd-353">Social Security identifier</span></span> 

<span data-ttu-id="15edd-354">Alle ansatte må ha én primær identifikator.</span><span class="sxs-lookup"><span data-stu-id="15edd-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="15edd-355">Identifikatoren må være av identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="15edd-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="15edd-356">I Dayforce hentes den automatisk som den ansattes personnummeridentifikator som kreves for ansettelse.</span><span class="sxs-lookup"><span data-stu-id="15edd-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="15edd-357">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-357">Primary (required)</span></span>
- <span data-ttu-id="15edd-358">Identifikasjonstype = "SSN"</span><span class="sxs-lookup"><span data-stu-id="15edd-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="15edd-359">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="15edd-359">Issued Date</span></span>
- <span data-ttu-id="15edd-360">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="15edd-360">Expiration Date</span></span>

<span data-ttu-id="15edd-361">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **SSN**.</span><span class="sxs-lookup"><span data-stu-id="15edd-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="15edd-362">Det er imidlertid bare posten som er merket som **Primær**, som er integrert i Dayforce, uansett om nummeret er aktivt eller utløpt.</span><span class="sxs-lookup"><span data-stu-id="15edd-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="15edd-363">Bankkontoer og -utlegg</span><span class="sxs-lookup"><span data-stu-id="15edd-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="15edd-364">Gyldig bankkontoinformasjon må angis for alle ansatte som velger å betales via bankkontooverføringer.</span><span class="sxs-lookup"><span data-stu-id="15edd-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="15edd-365">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-365">Talent</span></span>                         | <span data-ttu-id="15edd-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15edd-367">Bankkontonummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="15edd-368">SWIFT-kode (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-368">SWIFT code (required)</span></span>          | <span data-ttu-id="15edd-369">**Bank-ID**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="15edd-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="15edd-370">Avdelingsnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="15edd-371">Bankkontotype (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-371">Bank account type (required)</span></span>   | <span data-ttu-id="15edd-372">**Kontotoype**-felt som brukes ved behandling av lønninger i Mexico.</span><span class="sxs-lookup"><span data-stu-id="15edd-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="15edd-373">Støttede verdier inkluderer **Kontroll** og **Lønn**.</span><span class="sxs-lookup"><span data-stu-id="15edd-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="15edd-374">Ansatte som velger å betales via bankkontooverføringer, må oppgi en kobling til en restkonto som er under en juridisk enhet som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en meksikansk bank.</span><span class="sxs-lookup"><span data-stu-id="15edd-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="15edd-375">Alle andre ikke-restkontoer ignoreres.</span><span class="sxs-lookup"><span data-stu-id="15edd-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="15edd-376">Adresseopplysninger</span><span class="sxs-lookup"><span data-stu-id="15edd-376">Address information</span></span>

<span data-ttu-id="15edd-377">Alle ansatte må ha ett primært sted.</span><span class="sxs-lookup"><span data-stu-id="15edd-377">Every employee must have one primary location.</span></span> <span data-ttu-id="15edd-378">I Dayforce brukes dette stedet til å fastslå den ansattes primære bosted for skatte- og avgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="15edd-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="15edd-379">Primær (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-379">Primary (required)</span></span>
- <span data-ttu-id="15edd-380">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-380">Country/region (required)</span></span>
- <span data-ttu-id="15edd-381">Postnummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="15edd-382">Gate (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-382">Street (required)</span></span>
- <span data-ttu-id="15edd-383">Gatenummer (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-383">Street Number (required)</span></span>
- <span data-ttu-id="15edd-384">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="15edd-384">Building Complement</span></span>
- <span data-ttu-id="15edd-385">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-385">City (required)</span></span>
- <span data-ttu-id="15edd-386">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-386">State (required)</span></span>
- <span data-ttu-id="15edd-387">Land (oblitagorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="15edd-388">Konfigurer dataene for å generere lønn i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="15edd-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="15edd-389">Hvis du skal generere lønn for ansatte i USA og Canada, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="15edd-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="15edd-390">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="15edd-390">Departments are required on positions.</span></span>
- <span data-ttu-id="15edd-391">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="15edd-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="15edd-392">Du kan konfigurere Talent slik at det kreves at stillinger spesifiserer en avdeling.</span><span class="sxs-lookup"><span data-stu-id="15edd-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="15edd-393">For å gjøre dette går du til **HR delte stillinger > Stillinger > Avdelinger må oppgis for stillinger**.</span><span class="sxs-lookup"><span data-stu-id="15edd-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="15edd-394">Vi anbefaler at denne innstillingen iverksettes for integreringen.</span><span class="sxs-lookup"><span data-stu-id="15edd-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="15edd-395">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="15edd-395">Job types</span></span>

<span data-ttu-id="15edd-396">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="15edd-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="15edd-397">Jobbtyper kreves for å kunne behandle lønn i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="15edd-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="15edd-398">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="15edd-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="15edd-399">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="15edd-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="15edd-400">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="15edd-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="15edd-401">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="15edd-401">Job type</span></span>   | <span data-ttu-id="15edd-402">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="15edd-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="15edd-403">Per time</span><span class="sxs-lookup"><span data-stu-id="15edd-403">Hourly</span></span>     | <span data-ttu-id="15edd-404">Per time</span><span class="sxs-lookup"><span data-stu-id="15edd-404">Hourly</span></span>      |
| <span data-ttu-id="15edd-405">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="15edd-405">Salaried</span></span>   | <span data-ttu-id="15edd-406">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="15edd-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="15edd-407">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="15edd-407">Position types</span></span> 

<span data-ttu-id="15edd-408">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="15edd-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="15edd-409">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="15edd-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="15edd-410">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="15edd-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="15edd-411">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="15edd-411">Position type</span></span>   | <span data-ttu-id="15edd-412">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="15edd-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="15edd-413">Heltid</span><span class="sxs-lookup"><span data-stu-id="15edd-413">Full-time</span></span>       | <span data-ttu-id="15edd-414">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="15edd-414">Full time employee</span></span> |
| <span data-ttu-id="15edd-415">Deltid</span><span class="sxs-lookup"><span data-stu-id="15edd-415">Part-time</span></span>       | <span data-ttu-id="15edd-416">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="15edd-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="15edd-417">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="15edd-417">Reason codes</span></span>

<span data-ttu-id="15edd-418">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="15edd-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="15edd-419">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="15edd-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="15edd-420">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="15edd-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="15edd-421">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="15edd-421">Reason code</span></span>    | <span data-ttu-id="15edd-422">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="15edd-422">Description</span></span>      | <span data-ttu-id="15edd-423">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="15edd-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="15edd-424">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="15edd-424">RESIGNATION</span></span>    | <span data-ttu-id="15edd-425">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="15edd-425">Resignation</span></span>      | <span data-ttu-id="15edd-426">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-426">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-427">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="15edd-427">TERMINATION</span></span>    | <span data-ttu-id="15edd-428">Avslutning</span><span class="sxs-lookup"><span data-stu-id="15edd-428">Termination</span></span>      | <span data-ttu-id="15edd-429">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-429">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-430">AVGANG VED PENSJON</span><span class="sxs-lookup"><span data-stu-id="15edd-430">RETIREMENT</span></span>     | <span data-ttu-id="15edd-431">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="15edd-431">Retirement</span></span>       | <span data-ttu-id="15edd-432">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-432">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-433">ANNET</span><span class="sxs-lookup"><span data-stu-id="15edd-433">OTHER</span></span>          | <span data-ttu-id="15edd-434">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="15edd-434">Other Reasons</span></span>    | <span data-ttu-id="15edd-435">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-435">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-436">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="15edd-436">DEATH</span></span>          | <span data-ttu-id="15edd-437">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="15edd-437">Death</span></span>            | <span data-ttu-id="15edd-438">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-438">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-439">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="15edd-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="15edd-440">Permisjon</span><span class="sxs-lookup"><span data-stu-id="15edd-440">Leave of Absence</span></span> | <span data-ttu-id="15edd-441">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-441">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-442">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="15edd-442">CONTRACTEND</span></span>    | <span data-ttu-id="15edd-443">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="15edd-443">End of Contract</span></span>  | <span data-ttu-id="15edd-444">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-444">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-445">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="15edd-445">SALARYCHANGE</span></span>   | <span data-ttu-id="15edd-446">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="15edd-446">Change of Salary</span></span> | <span data-ttu-id="15edd-447">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="15edd-448">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="15edd-448">Marital status</span></span>

<span data-ttu-id="15edd-449">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="15edd-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="15edd-450">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="15edd-451">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-451">Talent</span></span>                 | <span data-ttu-id="15edd-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="15edd-453">Gift</span><span class="sxs-lookup"><span data-stu-id="15edd-453">Married</span></span>                | <span data-ttu-id="15edd-454">Gift</span><span class="sxs-lookup"><span data-stu-id="15edd-454">Married</span></span>              |
| <span data-ttu-id="15edd-455">Én</span><span class="sxs-lookup"><span data-stu-id="15edd-455">Single</span></span>                 | <span data-ttu-id="15edd-456">Én</span><span class="sxs-lookup"><span data-stu-id="15edd-456">Single</span></span>               |
| <span data-ttu-id="15edd-457">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="15edd-457">Widowed</span></span>                | <span data-ttu-id="15edd-458">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="15edd-458">Widowed</span></span>              |
| <span data-ttu-id="15edd-459">Skilt</span><span class="sxs-lookup"><span data-stu-id="15edd-459">Divorced</span></span>               | <span data-ttu-id="15edd-460">Skilt</span><span class="sxs-lookup"><span data-stu-id="15edd-460">Divorced</span></span>             |
| <span data-ttu-id="15edd-461">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="15edd-461">Registered Partnership</span></span> | <span data-ttu-id="15edd-462">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="15edd-462">Domestic Partnership</span></span> |
| <span data-ttu-id="15edd-463">None</span><span class="sxs-lookup"><span data-stu-id="15edd-463">None</span></span>                   | <span data-ttu-id="15edd-464">None</span><span class="sxs-lookup"><span data-stu-id="15edd-464">None</span></span>                 |
| <span data-ttu-id="15edd-465">Samboer</span><span class="sxs-lookup"><span data-stu-id="15edd-465">Cohabiting</span></span>             | <span data-ttu-id="15edd-466">Samboer</span><span class="sxs-lookup"><span data-stu-id="15edd-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="15edd-467">Kjønn</span><span class="sxs-lookup"><span data-stu-id="15edd-467">Gender</span></span>

<span data-ttu-id="15edd-468">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="15edd-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="15edd-469">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="15edd-470">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-470">Talent</span></span>       | <span data-ttu-id="15edd-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="15edd-472">Mann</span><span class="sxs-lookup"><span data-stu-id="15edd-472">Male</span></span>         | <span data-ttu-id="15edd-473">Mann</span><span class="sxs-lookup"><span data-stu-id="15edd-473">Male</span></span>            |
| <span data-ttu-id="15edd-474">Kvinne</span><span class="sxs-lookup"><span data-stu-id="15edd-474">Female</span></span>       | <span data-ttu-id="15edd-475">Kvinne</span><span class="sxs-lookup"><span data-stu-id="15edd-475">Female</span></span>          |
| <span data-ttu-id="15edd-476">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="15edd-476">Non-specific</span></span> | <span data-ttu-id="15edd-477">*Støttes ikke*</span><span class="sxs-lookup"><span data-stu-id="15edd-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="15edd-478">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="15edd-478">Earning codes</span></span>

<span data-ttu-id="15edd-479">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="15edd-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="15edd-480">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="15edd-481">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="15edd-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="15edd-482">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="15edd-482">Supported frequencies</span></span>

- <span data-ttu-id="15edd-483">Alle</span><span class="sxs-lookup"><span data-stu-id="15edd-483">All</span></span>
- <span data-ttu-id="15edd-484">HVERBET</span><span class="sxs-lookup"><span data-stu-id="15edd-484">EVERYPAY</span></span>
- <span data-ttu-id="15edd-485">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="15edd-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="15edd-486">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="15edd-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="15edd-487">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="15edd-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="15edd-488">1IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-488">1OFMTH</span></span>
- <span data-ttu-id="15edd-489">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="15edd-489">LASTOFMTH</span></span>
- <span data-ttu-id="15edd-490">2IMDN</span><span class="sxs-lookup"><span data-stu-id="15edd-490">2OFMTH</span></span>
- <span data-ttu-id="15edd-491">3IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-491">3OFMTH</span></span>
- <span data-ttu-id="15edd-492">4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-492">4OFMTH</span></span>
- <span data-ttu-id="15edd-493">5IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-493">5OFMTH</span></span>
- <span data-ttu-id="15edd-494">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-494">1N2OFMTH</span></span>
- <span data-ttu-id="15edd-495">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-495">3N4OFMTH</span></span>
- <span data-ttu-id="15edd-496">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-496">1N3OFMTH</span></span>
- <span data-ttu-id="15edd-497">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-497">1N4OFMTH</span></span>
- <span data-ttu-id="15edd-498">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-498">2N3OFMTH</span></span>
- <span data-ttu-id="15edd-499">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-499">2N4OFMTH</span></span>
- <span data-ttu-id="15edd-500">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="15edd-501">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="15edd-502">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="15edd-503">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="15edd-504">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="15edd-505">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="15edd-506">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="15edd-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="15edd-507">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="15edd-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="15edd-508">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="15edd-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="15edd-509">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="15edd-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="15edd-510">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="15edd-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="15edd-511">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="15edd-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="15edd-512">Adresser</span><span class="sxs-lookup"><span data-stu-id="15edd-512">Addresses</span></span>

<span data-ttu-id="15edd-513">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="15edd-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="15edd-514">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="15edd-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="15edd-515">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-515">Talent</span></span>          | <span data-ttu-id="15edd-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="15edd-517">Land/område</span><span class="sxs-lookup"><span data-stu-id="15edd-517">Country/Region</span></span>  | <span data-ttu-id="15edd-518">Landskode</span><span class="sxs-lookup"><span data-stu-id="15edd-518">Country Code</span></span>          |
| <span data-ttu-id="15edd-519">Postnummer</span><span class="sxs-lookup"><span data-stu-id="15edd-519">Zip/Postal Code</span></span> | <span data-ttu-id="15edd-520">Postnummer</span><span class="sxs-lookup"><span data-stu-id="15edd-520">Postal Code</span></span>           |
| <span data-ttu-id="15edd-521">Delstat</span><span class="sxs-lookup"><span data-stu-id="15edd-521">State</span></span>           | <span data-ttu-id="15edd-522">Statskode</span><span class="sxs-lookup"><span data-stu-id="15edd-522">State Code</span></span>            |
| <span data-ttu-id="15edd-523">By</span><span class="sxs-lookup"><span data-stu-id="15edd-523">City</span></span>            | <span data-ttu-id="15edd-524">By</span><span class="sxs-lookup"><span data-stu-id="15edd-524">City</span></span>                  |
| <span data-ttu-id="15edd-525">Kommune</span><span class="sxs-lookup"><span data-stu-id="15edd-525">County</span></span>          | <span data-ttu-id="15edd-526">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="15edd-526">County (Municipality)</span></span> |
| <span data-ttu-id="15edd-527">Gate</span><span class="sxs-lookup"><span data-stu-id="15edd-527">Street</span></span>          | <span data-ttu-id="15edd-528">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="15edd-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="15edd-529">Avgiftsområder</span><span class="sxs-lookup"><span data-stu-id="15edd-529">Tax regions</span></span>

<span data-ttu-id="15edd-530">Avgiftsområder brukes til å bestemme den gjeldende avgiften som skal brukes ved generering av lønn.</span><span class="sxs-lookup"><span data-stu-id="15edd-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="15edd-531">Avgiftsområder er tilordnet Dayforce som stedsadresser.</span><span class="sxs-lookup"><span data-stu-id="15edd-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="15edd-532">Standard avgiftområde må være knyttet til arbeiderens aktive stilling.</span><span class="sxs-lookup"><span data-stu-id="15edd-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="15edd-533">Avgiftsområde (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-533">Tax region (required)</span></span>
- <span data-ttu-id="15edd-534">Land/område (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-534">Country/Region (required)</span></span>
- <span data-ttu-id="15edd-535">Stat (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-535">State (required)</span></span>
- <span data-ttu-id="15edd-536">Kommune</span><span class="sxs-lookup"><span data-stu-id="15edd-536">County</span></span> 
- <span data-ttu-id="15edd-537">By (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="15edd-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="15edd-538">Konfigurere data for å generere lønn i Mexico</span><span class="sxs-lookup"><span data-stu-id="15edd-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="15edd-539">Hvis du skal generere lønn for ansatte i Mexico, konfigureres følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="15edd-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="15edd-540">Avdelinger må oppgis for stillinger.</span><span class="sxs-lookup"><span data-stu-id="15edd-540">Departments are required on positions.</span></span>
- <span data-ttu-id="15edd-541">Kostnadssentre må være angitt som finansdimensjoner og må være det første elementet i standard finansdimensjonsstreng.</span><span class="sxs-lookup"><span data-stu-id="15edd-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="15edd-542">Jobbtyper</span><span class="sxs-lookup"><span data-stu-id="15edd-542">Job types</span></span>

<span data-ttu-id="15edd-543">Jobbtyper brukes til å gruppere lignende jobber i kategorier.</span><span class="sxs-lookup"><span data-stu-id="15edd-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="15edd-544">Jobbtype kreves for å kunne behandle lønn i Mexico.</span><span class="sxs-lookup"><span data-stu-id="15edd-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="15edd-545">Eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn.</span><span class="sxs-lookup"><span data-stu-id="15edd-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="15edd-546">Jobbtyper er tilordnet til Dayforce som lønnstyper som angir om en ansatt er hver time eller lønn.</span><span class="sxs-lookup"><span data-stu-id="15edd-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="15edd-547">Følgende jobbtyper og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="15edd-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="15edd-548">Jobbtype</span><span class="sxs-lookup"><span data-stu-id="15edd-548">Job type</span></span>   | <span data-ttu-id="15edd-549">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="15edd-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="15edd-550">Per time</span><span class="sxs-lookup"><span data-stu-id="15edd-550">Hourly</span></span>     | <span data-ttu-id="15edd-551">MX per time</span><span class="sxs-lookup"><span data-stu-id="15edd-551">MX Hourly</span></span>   |
| <span data-ttu-id="15edd-552">Lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="15edd-552">Salaried</span></span>   | <span data-ttu-id="15edd-553">MX lønnsbasert</span><span class="sxs-lookup"><span data-stu-id="15edd-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="15edd-554">Stillingstyper</span><span class="sxs-lookup"><span data-stu-id="15edd-554">Position types</span></span> 

<span data-ttu-id="15edd-555">Du kan bruke stillingstyper til å beskrive om stillingen er heltid, deltid eller et annet navn.</span><span class="sxs-lookup"><span data-stu-id="15edd-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="15edd-556">Posisjonstyper er tilordnet til Dayforce som lønnsklasser som angir om en ansatt er fulltid eller deltid.</span><span class="sxs-lookup"><span data-stu-id="15edd-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="15edd-557">Følgende jobbposisjonstyper og -beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="15edd-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="15edd-558">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="15edd-558">Position type</span></span>   | <span data-ttu-id="15edd-559">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="15edd-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="15edd-560">Heltid</span><span class="sxs-lookup"><span data-stu-id="15edd-560">Full-time</span></span>       | <span data-ttu-id="15edd-561">Heltidsansatt</span><span class="sxs-lookup"><span data-stu-id="15edd-561">Full time employee</span></span> |
| <span data-ttu-id="15edd-562">Deltid</span><span class="sxs-lookup"><span data-stu-id="15edd-562">Part-time</span></span>       | <span data-ttu-id="15edd-563">Deltidsansatt</span><span class="sxs-lookup"><span data-stu-id="15edd-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="15edd-564">Årsakskoder</span><span class="sxs-lookup"><span data-stu-id="15edd-564">Reason codes</span></span>

<span data-ttu-id="15edd-565">Årsakskoder inneholder informasjon om statusen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="15edd-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="15edd-566">Årsakskoder er tilordnet til Dayforce som statusårsaker som angir årsaken til endringer i en ansatts stilling eller status.</span><span class="sxs-lookup"><span data-stu-id="15edd-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="15edd-567">Følgende årsakskoder og beskrivelser er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="15edd-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="15edd-568">Årsakskode</span><span class="sxs-lookup"><span data-stu-id="15edd-568">Reason code</span></span>            | <span data-ttu-id="15edd-569">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="15edd-569">Description</span></span>                    | <span data-ttu-id="15edd-570">Gjeldende scenarier</span><span class="sxs-lookup"><span data-stu-id="15edd-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="15edd-571">AVGANGFØRBETALING</span><span class="sxs-lookup"><span data-stu-id="15edd-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="15edd-572">Avgang før første lønn</span><span class="sxs-lookup"><span data-stu-id="15edd-572">Departure before first payroll</span></span> | <span data-ttu-id="15edd-573">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-573">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-574">OPPSIGELSE</span><span class="sxs-lookup"><span data-stu-id="15edd-574">RESIGNATION</span></span>            | <span data-ttu-id="15edd-575">Oppsigelse</span><span class="sxs-lookup"><span data-stu-id="15edd-575">Resignation</span></span>                    | <span data-ttu-id="15edd-576">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-576">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-577">PENSJON</span><span class="sxs-lookup"><span data-stu-id="15edd-577">PENSION</span></span>                | <span data-ttu-id="15edd-578">Pensjon</span><span class="sxs-lookup"><span data-stu-id="15edd-578">Pension</span></span>                        | <span data-ttu-id="15edd-579">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-579">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-580">AVSLUTNING</span><span class="sxs-lookup"><span data-stu-id="15edd-580">TERMINATION</span></span>            | <span data-ttu-id="15edd-581">Avslutning</span><span class="sxs-lookup"><span data-stu-id="15edd-581">Termination</span></span>                    | <span data-ttu-id="15edd-582">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-582">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-583">AVGANGVEDPENSJON</span><span class="sxs-lookup"><span data-stu-id="15edd-583">RETIREMENT</span></span>             | <span data-ttu-id="15edd-584">Avgang ved pensjon</span><span class="sxs-lookup"><span data-stu-id="15edd-584">Retirement</span></span>                     | <span data-ttu-id="15edd-585">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-585">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-586">FRAVÆRENDEPERSON</span><span class="sxs-lookup"><span data-stu-id="15edd-586">ABSENTEE</span></span>               | <span data-ttu-id="15edd-587">Fraværende person</span><span class="sxs-lookup"><span data-stu-id="15edd-587">Absentee</span></span>                       | <span data-ttu-id="15edd-588">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-588">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-589">ANNET</span><span class="sxs-lookup"><span data-stu-id="15edd-589">OTHER</span></span>                  | <span data-ttu-id="15edd-590">Andre årsaker</span><span class="sxs-lookup"><span data-stu-id="15edd-590">Other Reasons</span></span>                  | <span data-ttu-id="15edd-591">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-591">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-592">STENGNING</span><span class="sxs-lookup"><span data-stu-id="15edd-592">CLOSURE</span></span>                | <span data-ttu-id="15edd-593">Forretning stenger</span><span class="sxs-lookup"><span data-stu-id="15edd-593">Business Closure</span></span>               | <span data-ttu-id="15edd-594">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-594">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-595">DØDSFALL</span><span class="sxs-lookup"><span data-stu-id="15edd-595">DEATH</span></span>                  | <span data-ttu-id="15edd-596">Dødsfall</span><span class="sxs-lookup"><span data-stu-id="15edd-596">Death</span></span>                          | <span data-ttu-id="15edd-597">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-597">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-598">PERMISJON</span><span class="sxs-lookup"><span data-stu-id="15edd-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="15edd-599">Permisjon</span><span class="sxs-lookup"><span data-stu-id="15edd-599">Leave of Absence</span></span>               | <span data-ttu-id="15edd-600">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-600">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-601">KONTRAKTSLUTT</span><span class="sxs-lookup"><span data-stu-id="15edd-601">CONTRACTEND</span></span>            | <span data-ttu-id="15edd-602">Slutt på kontrakt</span><span class="sxs-lookup"><span data-stu-id="15edd-602">End of Contract</span></span>                | <span data-ttu-id="15edd-603">Avslutt arbeider</span><span class="sxs-lookup"><span data-stu-id="15edd-603">Terminate worker</span></span>     |
| <span data-ttu-id="15edd-604">LØNNSENDRING</span><span class="sxs-lookup"><span data-stu-id="15edd-604">SALARYCHANGE</span></span>           | <span data-ttu-id="15edd-605">Lønnsendring</span><span class="sxs-lookup"><span data-stu-id="15edd-605">Change of Salary</span></span>               | <span data-ttu-id="15edd-606">Kompensasjon</span><span class="sxs-lookup"><span data-stu-id="15edd-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="15edd-607">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="15edd-607">Terms of employment</span></span>

<span data-ttu-id="15edd-608">Ansettelsesbetingelser brukes til å opprette kategorier for ansettelsesbetingelser.</span><span class="sxs-lookup"><span data-stu-id="15edd-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="15edd-609">Vilkårene tilordnes til Dayforce som ansettelseindikatorverdier.</span><span class="sxs-lookup"><span data-stu-id="15edd-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="15edd-610">Følgende betingelsene for ansettelse og beskrivelser kreves.</span><span class="sxs-lookup"><span data-stu-id="15edd-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="15edd-611">Ansettelsesbetingelser</span><span class="sxs-lookup"><span data-stu-id="15edd-611">Terms of employment</span></span>   | <span data-ttu-id="15edd-612">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="15edd-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="15edd-613">Vanlig</span><span class="sxs-lookup"><span data-stu-id="15edd-613">Regular</span></span>               | <span data-ttu-id="15edd-614">Vanlig</span><span class="sxs-lookup"><span data-stu-id="15edd-614">Regular</span></span>     |
| <span data-ttu-id="15edd-615">Direkte</span><span class="sxs-lookup"><span data-stu-id="15edd-615">Direct</span></span>                | <span data-ttu-id="15edd-616">Direkte</span><span class="sxs-lookup"><span data-stu-id="15edd-616">Direct</span></span>      |
| <span data-ttu-id="15edd-617">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="15edd-617">Internship</span></span>            | <span data-ttu-id="15edd-618">Praktikantstilling</span><span class="sxs-lookup"><span data-stu-id="15edd-618">Internship</span></span>  |
| <span data-ttu-id="15edd-619">Permanent</span><span class="sxs-lookup"><span data-stu-id="15edd-619">Permanent</span></span>             | <span data-ttu-id="15edd-620">Permanent</span><span class="sxs-lookup"><span data-stu-id="15edd-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="15edd-621">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="15edd-621">Marital status</span></span>

<span data-ttu-id="15edd-622">Sivilstandverdier tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="15edd-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="15edd-623">Tabellen nedenfor viser hvordan sivilstandverdiene tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="15edd-624">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-624">Talent</span></span>                 | <span data-ttu-id="15edd-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="15edd-626">Gift</span><span class="sxs-lookup"><span data-stu-id="15edd-626">Married</span></span>                | <span data-ttu-id="15edd-627">Gift</span><span class="sxs-lookup"><span data-stu-id="15edd-627">Married</span></span>                   |
| <span data-ttu-id="15edd-628">Én</span><span class="sxs-lookup"><span data-stu-id="15edd-628">Single</span></span>                 | <span data-ttu-id="15edd-629">Én</span><span class="sxs-lookup"><span data-stu-id="15edd-629">Single</span></span>                    |
| <span data-ttu-id="15edd-630">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="15edd-630">Widowed</span></span>                | <span data-ttu-id="15edd-631">Enke/enkemann</span><span class="sxs-lookup"><span data-stu-id="15edd-631">Widowed</span></span>                   |
| <span data-ttu-id="15edd-632">Skilt</span><span class="sxs-lookup"><span data-stu-id="15edd-632">Divorced</span></span>               | <span data-ttu-id="15edd-633">Skilt</span><span class="sxs-lookup"><span data-stu-id="15edd-633">Divorced</span></span>                  |
| <span data-ttu-id="15edd-634">Registrert ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="15edd-634">Registered Partnership</span></span> | <span data-ttu-id="15edd-635">Ekteskapelig partnerskap</span><span class="sxs-lookup"><span data-stu-id="15edd-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="15edd-636">None</span><span class="sxs-lookup"><span data-stu-id="15edd-636">None</span></span>                   | <span data-ttu-id="15edd-637">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="15edd-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="15edd-638">Samboer</span><span class="sxs-lookup"><span data-stu-id="15edd-638">Cohabiting</span></span>             | <span data-ttu-id="15edd-639">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="15edd-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="15edd-640">Kjønn</span><span class="sxs-lookup"><span data-stu-id="15edd-640">Gender</span></span>

<span data-ttu-id="15edd-641">Kjønnsangivelser tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="15edd-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="15edd-642">Tabellen nedenfor viser hvordan kjønnsangivelser tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="15edd-643">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-643">Talent</span></span>       | <span data-ttu-id="15edd-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="15edd-645">Mann</span><span class="sxs-lookup"><span data-stu-id="15edd-645">Male</span></span>         | <span data-ttu-id="15edd-646">Mann</span><span class="sxs-lookup"><span data-stu-id="15edd-646">Male</span></span>                      |
| <span data-ttu-id="15edd-647">Kvinne</span><span class="sxs-lookup"><span data-stu-id="15edd-647">Female</span></span>       | <span data-ttu-id="15edd-648">Kvinne</span><span class="sxs-lookup"><span data-stu-id="15edd-648">Female</span></span>                    |
| <span data-ttu-id="15edd-649">Ikke spesifikt</span><span class="sxs-lookup"><span data-stu-id="15edd-649">Non-specific</span></span> | <span data-ttu-id="15edd-650">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="15edd-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="15edd-651">Betalingsmetode</span><span class="sxs-lookup"><span data-stu-id="15edd-651">Payment method</span></span>

<span data-ttu-id="15edd-652">Betalingsmåter gir den ansatte og firmaet en måte å beskrive hvordan ansatte skal betales.</span><span class="sxs-lookup"><span data-stu-id="15edd-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="15edd-653">Betalingsmåter tilordnes til Dayforce og oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="15edd-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="15edd-654">Tabellen nedenfor viser hvordan betalingsmåter tilordnes i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="15edd-655">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-655">Talent</span></span>             | <span data-ttu-id="15edd-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="15edd-657">Kontanter</span><span class="sxs-lookup"><span data-stu-id="15edd-657">Cash</span></span>               | <span data-ttu-id="15edd-658">Kontanter</span><span class="sxs-lookup"><span data-stu-id="15edd-658">Cash</span></span>                      |
| <span data-ttu-id="15edd-659">Elektronisk betaling</span><span class="sxs-lookup"><span data-stu-id="15edd-659">Electronic Payment</span></span> | <span data-ttu-id="15edd-660">Overfør</span><span class="sxs-lookup"><span data-stu-id="15edd-660">Transfer</span></span>                  |
| <span data-ttu-id="15edd-661">Kontroll</span><span class="sxs-lookup"><span data-stu-id="15edd-661">Check</span></span>              | <span data-ttu-id="15edd-662">Sjekk</span><span class="sxs-lookup"><span data-stu-id="15edd-662">Cheque</span></span>                    |
| <span data-ttu-id="15edd-663">Bankoverføring</span><span class="sxs-lookup"><span data-stu-id="15edd-663">Bank Draft</span></span>         | <span data-ttu-id="15edd-664">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="15edd-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="15edd-665">Annet</span><span class="sxs-lookup"><span data-stu-id="15edd-665">Other</span></span>              | <span data-ttu-id="15edd-666">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="15edd-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="15edd-667">Bankkontotype</span><span class="sxs-lookup"><span data-stu-id="15edd-667">Bank account type</span></span>

<span data-ttu-id="15edd-668">Bankkontotypene brukes for elektroniske betalinger til ansatte.</span><span class="sxs-lookup"><span data-stu-id="15edd-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="15edd-669">Bankkontotypene tilordnes til Dayforce som overføringskontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="15edd-670">Bankkontotypene oversettes, etter behov, til de godkjente verdiene ved integrering.</span><span class="sxs-lookup"><span data-stu-id="15edd-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="15edd-671">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-671">Talent</span></span>            | <span data-ttu-id="15edd-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="15edd-673">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="15edd-673">Checking Account</span></span>  | <span data-ttu-id="15edd-674">Sjekkonto</span><span class="sxs-lookup"><span data-stu-id="15edd-674">CheckingAccount</span></span>           |
| <span data-ttu-id="15edd-675">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="15edd-675">Payroll Account</span></span>   | <span data-ttu-id="15edd-676">Lønnskonto</span><span class="sxs-lookup"><span data-stu-id="15edd-676">PayrollAccount</span></span>            |
| <span data-ttu-id="15edd-677">Sparekonto</span><span class="sxs-lookup"><span data-stu-id="15edd-677">Savings Account</span></span>   | <span data-ttu-id="15edd-678">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="15edd-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="15edd-679">BankGirot-konto</span><span class="sxs-lookup"><span data-stu-id="15edd-679">BankGirot account</span></span> | <span data-ttu-id="15edd-680">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="15edd-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="15edd-681">PlusGirot-konto</span><span class="sxs-lookup"><span data-stu-id="15edd-681">PlusGirot account</span></span> | <span data-ttu-id="15edd-682">*Støttes ikke i Mexico*</span><span class="sxs-lookup"><span data-stu-id="15edd-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="15edd-683">Inntektskoder</span><span class="sxs-lookup"><span data-stu-id="15edd-683">Earning codes</span></span>

<span data-ttu-id="15edd-684">Inntektskoder sørger for unik identifisering av alle typer inntekter som ansatte mottar.</span><span class="sxs-lookup"><span data-stu-id="15edd-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="15edd-685">Kodene dekker flere parametere som er knyttet til inntekter, for eksempel regnskapsregler, skattelover, rapporteringkrav og bruttofunksjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="15edd-686">Hvis det brukes en frekvens som ikke støttes, brukes frekvensen **Hver betaling** som standard for beregningen.</span><span class="sxs-lookup"><span data-stu-id="15edd-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="15edd-687">Støttede frekvenser</span><span class="sxs-lookup"><span data-stu-id="15edd-687">Supported frequencies</span></span>

- <span data-ttu-id="15edd-688">Alle</span><span class="sxs-lookup"><span data-stu-id="15edd-688">All</span></span>
- <span data-ttu-id="15edd-689">HVERBET</span><span class="sxs-lookup"><span data-stu-id="15edd-689">EVERYPAY</span></span>
- <span data-ttu-id="15edd-690">HVERBETPERIODE</span><span class="sxs-lookup"><span data-stu-id="15edd-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="15edd-691">ANNENHVBETODD</span><span class="sxs-lookup"><span data-stu-id="15edd-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="15edd-692">ANNENHVBETPAR</span><span class="sxs-lookup"><span data-stu-id="15edd-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="15edd-693">1IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-693">1OFMTH</span></span>
- <span data-ttu-id="15edd-694">SISTEIMND</span><span class="sxs-lookup"><span data-stu-id="15edd-694">LASTOFMTH</span></span>
- <span data-ttu-id="15edd-695">2IMDN</span><span class="sxs-lookup"><span data-stu-id="15edd-695">2OFMTH</span></span>
- <span data-ttu-id="15edd-696">3IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-696">3OFMTH</span></span>
- <span data-ttu-id="15edd-697">4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-697">4OFMTH</span></span>
- <span data-ttu-id="15edd-698">5IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-698">5OFMTH</span></span>
- <span data-ttu-id="15edd-699">1OG2IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-699">1N2OFMTH</span></span>
- <span data-ttu-id="15edd-700">3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-700">3N4OFMTH</span></span>
- <span data-ttu-id="15edd-701">1OG3IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-701">1N3OFMTH</span></span>
- <span data-ttu-id="15edd-702">1OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-702">1N4OFMTH</span></span>
- <span data-ttu-id="15edd-703">2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-703">2N3OFMTH</span></span>
- <span data-ttu-id="15edd-704">2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-704">2N4OFMTH</span></span>
- <span data-ttu-id="15edd-705">1OG2OG3IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="15edd-706">1OG2OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="15edd-707">1OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="15edd-708">2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="15edd-709">1OG2OG3OG4IMND - 1OG2OG3OG4IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="15edd-710">2OG3OG4OG5IMND - 2OG3OG4OG5IMND</span><span class="sxs-lookup"><span data-stu-id="15edd-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="15edd-711">1IKVRT - 1IKVRT</span><span class="sxs-lookup"><span data-stu-id="15edd-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="15edd-712">SISTIKVART – SISTIKVART</span><span class="sxs-lookup"><span data-stu-id="15edd-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="15edd-713">SISTEMNDIKVRT – SISTEMNDIKVRT</span><span class="sxs-lookup"><span data-stu-id="15edd-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="15edd-714">1IÅR - 1IÅR</span><span class="sxs-lookup"><span data-stu-id="15edd-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="15edd-715">SISTEIÅR – SISTEIÅR</span><span class="sxs-lookup"><span data-stu-id="15edd-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="15edd-716">NOVOGDESIÅR - NOVOGDESIÅR</span><span class="sxs-lookup"><span data-stu-id="15edd-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="15edd-717">Adresser</span><span class="sxs-lookup"><span data-stu-id="15edd-717">Addresses</span></span>

<span data-ttu-id="15edd-718">Identifikasjon av bestemte koder for land eller område, delstat og fylke (kommune) krever spesifikke formater som Dayforce og leverandører i landet/området kan gjenkjenne.</span><span class="sxs-lookup"><span data-stu-id="15edd-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="15edd-719">Selv om formatet for byer er fleksibelt, må hver by være knyttet en stat.</span><span class="sxs-lookup"><span data-stu-id="15edd-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="15edd-720">Talent</span><span class="sxs-lookup"><span data-stu-id="15edd-720">Talent</span></span>              | <span data-ttu-id="15edd-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="15edd-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="15edd-722">Land/område</span><span class="sxs-lookup"><span data-stu-id="15edd-722">Country/Region</span></span>      | <span data-ttu-id="15edd-723">Landskode</span><span class="sxs-lookup"><span data-stu-id="15edd-723">Country Code</span></span>          |
| <span data-ttu-id="15edd-724">Postnummer</span><span class="sxs-lookup"><span data-stu-id="15edd-724">Zip/Postal Code</span></span>     | <span data-ttu-id="15edd-725">Postnummer</span><span class="sxs-lookup"><span data-stu-id="15edd-725">Postal Code</span></span>           |
| <span data-ttu-id="15edd-726">Delstat</span><span class="sxs-lookup"><span data-stu-id="15edd-726">State</span></span>               | <span data-ttu-id="15edd-727">Statskode</span><span class="sxs-lookup"><span data-stu-id="15edd-727">State Code</span></span>            |
| <span data-ttu-id="15edd-728">By</span><span class="sxs-lookup"><span data-stu-id="15edd-728">City</span></span>                | <span data-ttu-id="15edd-729">By</span><span class="sxs-lookup"><span data-stu-id="15edd-729">City</span></span>                  |
| <span data-ttu-id="15edd-730">Kommune</span><span class="sxs-lookup"><span data-stu-id="15edd-730">County</span></span>              | <span data-ttu-id="15edd-731">Fylke (kommune)</span><span class="sxs-lookup"><span data-stu-id="15edd-731">County (Municipality)</span></span> |
| <span data-ttu-id="15edd-732">Gate</span><span class="sxs-lookup"><span data-stu-id="15edd-732">Street</span></span>              | <span data-ttu-id="15edd-733">Adresselinje 1</span><span class="sxs-lookup"><span data-stu-id="15edd-733">Address Line 1</span></span>        |
| <span data-ttu-id="15edd-734">Gatenummer</span><span class="sxs-lookup"><span data-stu-id="15edd-734">Street Number</span></span>       | <span data-ttu-id="15edd-735">Adresselinje 2</span><span class="sxs-lookup"><span data-stu-id="15edd-735">Address Line 2</span></span>        |
| <span data-ttu-id="15edd-736">Bygningsnavn</span><span class="sxs-lookup"><span data-stu-id="15edd-736">Building Complement</span></span> | <span data-ttu-id="15edd-737">Adresselinje 5</span><span class="sxs-lookup"><span data-stu-id="15edd-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="15edd-738">Passnummer</span><span class="sxs-lookup"><span data-stu-id="15edd-738">Passport number</span></span>

<span data-ttu-id="15edd-739">Ansatte kan deklarere passinformasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-739">Employees can declare passport information.</span></span> <span data-ttu-id="15edd-740">Denne informasjonen er av **Pass**-identifikasjonstypen og er integrert i Dayforce som en del av en ansatts Mexico-spesifikke informasjon.</span><span class="sxs-lookup"><span data-stu-id="15edd-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="15edd-741">Identifikasjonstype = "Pass"</span><span class="sxs-lookup"><span data-stu-id="15edd-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="15edd-742">Utstedelsesdato</span><span class="sxs-lookup"><span data-stu-id="15edd-742">Issued Date</span></span>
- <span data-ttu-id="15edd-743">Utløpsdato</span><span class="sxs-lookup"><span data-stu-id="15edd-743">Expiration Date</span></span>

<span data-ttu-id="15edd-744">Ansatte kan angi flere identifikasjonsnumre for identifikasjonstypen **Pass**.</span><span class="sxs-lookup"><span data-stu-id="15edd-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="15edd-745">Men bare den gjeldende aktive passoppføringen er integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="15edd-746">Hvis alle passoppføringer er utløpt, er passet som sist ble utstedt, integrert i Dayforce.</span><span class="sxs-lookup"><span data-stu-id="15edd-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

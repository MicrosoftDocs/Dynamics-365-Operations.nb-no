---
title: Automatisering av leverandørfaktura
description: Dette emnet forklarer hvilke funksjoner som er tilgjengelige for ende-til-ende-automatisering av leverandørfakturaer, også fakturaer som inneholder vedlegg.
author: abruer
manager: AnnBe
ms.date: 05/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4560d7b61fa8f014f9a1185da087df8b1c8e61ba
ms.sourcegitcommit: b7af921189048d9f2eb4d3fd57c704c742bc96e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/23/2020
ms.locfileid: "3396015"
---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="75c04-103">Automatisering av leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="75c04-103">Vendor invoice automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75c04-104">Dette emnet forklarer hvilke funksjoner som er tilgjengelige for ende-til-ende-automatisering av leverandørfakturaer, også fakturaer som inneholder vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="75c04-105">Organisasjoner som ønsker å strømlinjeforme leverandørprosessene for (AP), identifiserer ofte fakturabehandling som ett av de øverste prosessområdene som bør være mer effektivt.</span><span class="sxs-lookup"><span data-stu-id="75c04-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="75c04-106">I mange tilfeller setter disse organisasjonene behandling av papirfakturaer ut til en tredjepartsleverandør av tjenester for optisk tegngjenkjenning (OCR).</span><span class="sxs-lookup"><span data-stu-id="75c04-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="75c04-107">Deretter mottar de maskinlesbare fakturametadata sammen med et skannet bilde av hver faktura.</span><span class="sxs-lookup"><span data-stu-id="75c04-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="75c04-108">For å få hjelp med automatisering bygges deretter en løsning for den siste delen for å aktivere forbruk av disse artefakterene i faktureringssystemet.</span><span class="sxs-lookup"><span data-stu-id="75c04-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="75c04-109">Nå er denne automatiseringen for den siste delen aktivert som standard, gjennom en løsning for automatisering av fakturaer.</span><span class="sxs-lookup"><span data-stu-id="75c04-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="75c04-110">Løsningskontekst</span><span class="sxs-lookup"><span data-stu-id="75c04-110">Solution context</span></span>

<span data-ttu-id="75c04-111">Fakturaautomatiseringsløsningen gjør det mulig å bruke et standardgrensesnitt som kan godta fakturametadata for fakturahodet og fakturalinjene, og også vedlegg som gjelder for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="75c04-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="75c04-112">Eksterne systemer som kan generere artefakter som samsvarer med dette grensesnittet, kan sende feeden for automatisk behandling av fakturaer og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="75c04-113">Illustrasjonen nedenfor viser et eksempelscenario for integrasjon der Contoso samarbeider med en OCR-tjenesteleverandør for leverandørfakturabehandling.</span><span class="sxs-lookup"><span data-stu-id="75c04-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="75c04-114">Contosos leverandører sender fakturaer til tjenesteleverandøren via e-post.</span><span class="sxs-lookup"><span data-stu-id="75c04-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="75c04-115">Ved hjelp av OCR-behandling genererer tjenesteleverandøren fakturametadata (hode og/eller linjer) og et skannet bilde på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="75c04-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="75c04-116">Et lag med integrasjon omformer deretter disse artefaktene slik at de kan brukes.</span><span class="sxs-lookup"><span data-stu-id="75c04-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![Eksempelscenario for integrasjon](media/vendor_invoice_automation_01.png)

<span data-ttu-id="75c04-118">Flere varianter av det forrige scenarioet er mulig hvis fakturaintegrasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="75c04-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="75c04-119">Migrering av data er et annet brukstilfelle der dette grensesnittet kan brukes til å opprette fakturaer og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="75c04-120">Løsningskomponenter</span><span class="sxs-lookup"><span data-stu-id="75c04-120">Solution components</span></span>

<span data-ttu-id="75c04-121">Løsningsavtrykket består av følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="75c04-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="75c04-122">Dataenheter for fakturahodet, fakturalinjene og fakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="75c04-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="75c04-123">Unntaksbehandling for fakturaer</span><span class="sxs-lookup"><span data-stu-id="75c04-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="75c04-124">Et visningsprogram for vedlegg side ved side i fakturaer</span><span class="sxs-lookup"><span data-stu-id="75c04-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="75c04-125">Resten av dette emnet inneholder detaljerte beskrivelser av disse løsningskomponentene.</span><span class="sxs-lookup"><span data-stu-id="75c04-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="75c04-126">Dataenheter</span><span class="sxs-lookup"><span data-stu-id="75c04-126">Data entities</span></span>

<span data-ttu-id="75c04-127">En datapakke er arbeidsenheten som må sendes, slik at fakturahoder, fakturalinjer og fakturavedlegg kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="75c04-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="75c04-128">Følgende dataenheter brukes for artefaktene som utgjør datapakken:</span><span class="sxs-lookup"><span data-stu-id="75c04-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="75c04-129">Leverandørfakturahode</span><span class="sxs-lookup"><span data-stu-id="75c04-129">Vendor invoice header</span></span>
+ <span data-ttu-id="75c04-130">Leverandørfakturalinje</span><span class="sxs-lookup"><span data-stu-id="75c04-130">Vendor invoice line</span></span>
+ <span data-ttu-id="75c04-131">Dokumentvedlegg for leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="75c04-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="75c04-132">Dokumentvedlegg for leverandørfaktura er en ny dataenhet som lanseres som en del av denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="75c04-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="75c04-133">Enheten for leverandørfakturahode er blitt endret slik at den støtter vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="75c04-134">Enheten for leverandørfakturalinje er ikke endret for denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="75c04-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="75c04-135">Hvis du vil ha mer informasjon om datapakker, kan du se [Oversikt over databehandling](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="75c04-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="75c04-136">Hvis du vil ha informasjon om hvordan du oppretter datapakker ved hjelp av arbeidsområdet for databehandling, kan du se [Behandle og bruke datapakker i løsningen for Dynamics 365 Finance and Operations-apper](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="75c04-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="75c04-137">Bruk følgende fremgangsmåte for å raskt generere testdata som inkluderer fakturaer og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="75c04-138">Logg på forekomsten.</span><span class="sxs-lookup"><span data-stu-id="75c04-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="75c04-139">Gå til **Leverandører** > **Fakturaer** > **Ventende leverandørfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="75c04-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="75c04-140">Opprett fakturaer som har linjer og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="75c04-141">Vedleggene må være hodevedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-141">The attachments must be header attachments.</span></span> <span data-ttu-id="75c04-142">Enheten for dokumentvedlegg for leverandørfaktura støtter for øyeblikket ikke linjevedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="75c04-143">Åpne arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="75c04-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="75c04-144">Opprett en eksportjobb som inkluderer enhetene for leverandørfakturahode, leverandørfakturalinje og dokumentvedlegg for leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="75c04-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="75c04-145">Eksporter dataene.</span><span class="sxs-lookup"><span data-stu-id="75c04-145">Export the data.</span></span>
1. <span data-ttu-id="75c04-146">Last ned de eksporterte dataene som en pakke.</span><span class="sxs-lookup"><span data-stu-id="75c04-146">Download the exported data as a package.</span></span> <span data-ttu-id="75c04-147">Du kan nå bruke pakken til å importere data til målforekomster for testformål.</span><span class="sxs-lookup"><span data-stu-id="75c04-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="75c04-148">Bestemme den juridiske enheten for en faktura</span><span class="sxs-lookup"><span data-stu-id="75c04-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="75c04-149">Fakturaer som importeres via datapakker, kan knyttes til den juridiske enheten som de hører til, på to måter:</span><span class="sxs-lookup"><span data-stu-id="75c04-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="75c04-150">Importjobben som behandler fakturaen, importerer den til det samme firmaet der jobben er planlagt i arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="75c04-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="75c04-151">Med andre ord bestemmer firmaet for jobben hvilket firma som fakturaen tilhører.</span><span class="sxs-lookup"><span data-stu-id="75c04-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="75c04-152">Når datapakken som inneholder fakturaer, sendes til Finance, kan oppkalleren (det vil si integrasjonsprogrammet som kjøres utenfor Finance) eksplisitt nevne firma-ID-en i HTTP-forespørselen.</span><span class="sxs-lookup"><span data-stu-id="75c04-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="75c04-153">I så fall overstyres firmakonteksten der behandlingsjobben kjører i Finance, og fakturaene importeres til firmaet som ble sendt via HTTP-forespørselen.</span><span class="sxs-lookup"><span data-stu-id="75c04-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="75c04-154">Dette er standard virkemåte for databehandling.</span><span class="sxs-lookup"><span data-stu-id="75c04-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="75c04-155">Det er beskrevet her, i forbindelse med fakturaer, bare å gi komplett informasjon.</span><span class="sxs-lookup"><span data-stu-id="75c04-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="75c04-156">Behandling av unntak</span><span class="sxs-lookup"><span data-stu-id="75c04-156">Exception processing</span></span>

<span data-ttu-id="75c04-157">I situasjoner der leverandørfakturaer kommer til Finance and Operations via integrasjon, må det være enkelt for et teammedlem i leverandører å behandle unntak eller mislykkede fakturaer og opprette ventende fakturaer fra mislykkede fakturaer.</span><span class="sxs-lookup"><span data-stu-id="75c04-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="75c04-158">Denne unntaksbehandlingen for leverandørfakturaer er nå en del av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75c04-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="75c04-159">Side med liste over unntak</span><span class="sxs-lookup"><span data-stu-id="75c04-159">Exceptions list page</span></span>

<span data-ttu-id="75c04-160">Den nye listesiden for fakturaunntak er tilgjengelig på **Leverandører** > **Fakturaer** > **Importfeil** > **Leverandørfakturaer som ikke ble importert**.</span><span class="sxs-lookup"><span data-stu-id="75c04-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="75c04-161">Denne siden viser alle hodepostene for leverandørfakturaer fra oppsamlingstabellen for dataenheten for leverandørfakturahode.</span><span class="sxs-lookup"><span data-stu-id="75c04-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="75c04-162">Vær oppmerksom på at du kan vise de samme postene fra arbeidsområdet **Databehandling**, der du også kan utføre de samme handlingene som er angitt i funksjonen for unntaksbehandling.</span><span class="sxs-lookup"><span data-stu-id="75c04-162">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="75c04-163">Imidlertid er brukergrensesnittet i funksjonen for unntaksbehandling optimalisert for en funksjonell bruker.</span><span class="sxs-lookup"><span data-stu-id="75c04-163">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Side med liste over unntak](media/vendor_invoice_automation_02.png)

<span data-ttu-id="75c04-165">Denne listesiden inneholder følgende felt som kommer inn via feeden:</span><span class="sxs-lookup"><span data-stu-id="75c04-165">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="75c04-166">**Firma** – firmaet som fakturaen tilhører</span><span class="sxs-lookup"><span data-stu-id="75c04-166">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="75c04-167">**Feilmelding** – feilmeldingen som rammeverket for databehandling utsteder for å forklare hvorfor fakturaen ikke kan opprettes</span><span class="sxs-lookup"><span data-stu-id="75c04-167">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="75c04-168">**Nummer** – fakturanummeret</span><span class="sxs-lookup"><span data-stu-id="75c04-168">**Number** – The invoice number</span></span>
+ <span data-ttu-id="75c04-169">**Fakturakonto**</span><span class="sxs-lookup"><span data-stu-id="75c04-169">**Invoice account**</span></span>
+ <span data-ttu-id="75c04-170">**Navn** – leverandørens navn</span><span class="sxs-lookup"><span data-stu-id="75c04-170">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="75c04-171">**Leverandørkonto**</span><span class="sxs-lookup"><span data-stu-id="75c04-171">**Vendor account**</span></span>
+ <span data-ttu-id="75c04-172">**Bestilling** – bestillingsnummeret for fakturaen</span><span class="sxs-lookup"><span data-stu-id="75c04-172">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="75c04-173">**Posteringsdato**</span><span class="sxs-lookup"><span data-stu-id="75c04-173">**Posting date**</span></span>
+ <span data-ttu-id="75c04-174">**Fakturadato**</span><span class="sxs-lookup"><span data-stu-id="75c04-174">**Invoice date**</span></span>
+ <span data-ttu-id="75c04-175">**Fakturabeskrivelse**</span><span class="sxs-lookup"><span data-stu-id="75c04-175">**Invoice description**</span></span>
+ <span data-ttu-id="75c04-176">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="75c04-176">**Currency**</span></span>
+ <span data-ttu-id="75c04-177">**Logg**</span><span class="sxs-lookup"><span data-stu-id="75c04-177">**Log**</span></span>
+ <span data-ttu-id="75c04-178">**Linjereferanse** – identifikatoren som kommer fra det eksterne systemet</span><span class="sxs-lookup"><span data-stu-id="75c04-178">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="75c04-179">Linjereferansen ikke er IDen for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="75c04-179">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="75c04-180">Denne listesiden har også en forhåndsvisningsrute som kan brukes på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="75c04-180">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="75c04-181">Vis hele feilmeldingen, slik at du ikke trenger å utvide **Feilmelding**-kolonnen i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="75c04-181">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="75c04-182">Vis hele listen over vedlegg for fakturaen, hvis vedlegg fulgte med fakturaen.</span><span class="sxs-lookup"><span data-stu-id="75c04-182">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="75c04-183">Listesiden støtter følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="75c04-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="75c04-184">**Rediger** – åpne unntaksposten i redigeringsmodus, slik at du kan løse problemene.</span><span class="sxs-lookup"><span data-stu-id="75c04-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="75c04-185">**Alternativer** – få tilgang til standardalternativene som er tilgjengelige på listesider.</span><span class="sxs-lookup"><span data-stu-id="75c04-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="75c04-186">Du kan bruke alternativet **Legg til i arbeidsområde** for å feste unntakslistesiden til arbeidsområdet som en liste eller flis.</span><span class="sxs-lookup"><span data-stu-id="75c04-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="75c04-187">Side for unntaksdetaljer</span><span class="sxs-lookup"><span data-stu-id="75c04-187">Exception details page</span></span>

<span data-ttu-id="75c04-188">Når du starter redigeringsmodus, vises siden for unntaksdetaljer for fakturaen som har problemer.</span><span class="sxs-lookup"><span data-stu-id="75c04-188">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="75c04-189">Hvis det ikke finnes vedlegg, vises fakturaen og standardvedlegget side ved side på siden for unntaksdetaljer.</span><span class="sxs-lookup"><span data-stu-id="75c04-189">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Side for unntaksdetaljer](media/vendor_invoice_automation_03.png)

<span data-ttu-id="75c04-191">I den forrige illustrasjonen var det ikke noen linjer for leverandørfakturahodet som kom inn.</span><span class="sxs-lookup"><span data-stu-id="75c04-191">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="75c04-192">Linjedelen er derfor tom.</span><span class="sxs-lookup"><span data-stu-id="75c04-192">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="75c04-193">Siden for unntaksdetaljer støtter følgende operasjon:</span><span class="sxs-lookup"><span data-stu-id="75c04-193">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="75c04-194">**Opprett ventende faktura** – Når du har løst problemene på fakturaen som en del av behandling av unntak, kan du klikke denne knappen for å opprette den ventende fakturaen.</span><span class="sxs-lookup"><span data-stu-id="75c04-194">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="75c04-195">Opprettelse av ventende fakturaer skjer i bakgrunnen (som en asynkron operasjon).</span><span class="sxs-lookup"><span data-stu-id="75c04-195">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="75c04-196">Unntaksbehandling for delte tjenester i forhold til organisasjonsbasert unntaksbehandling</span><span class="sxs-lookup"><span data-stu-id="75c04-196">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="75c04-197">Unntakslistesiden støtter standard sikkerhetsbegreper som arbeidsområdet **Databehandling** støtter for behandling av oppsamlingsposter.</span><span class="sxs-lookup"><span data-stu-id="75c04-197">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="75c04-198">Fakturaimportjobben kan sikres på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="75c04-198">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="75c04-199">Etter brukerrolle</span><span class="sxs-lookup"><span data-stu-id="75c04-199">By user role</span></span>
+ <span data-ttu-id="75c04-200">Etter bruker</span><span class="sxs-lookup"><span data-stu-id="75c04-200">By user</span></span>
+ <span data-ttu-id="75c04-201">Etter juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="75c04-201">By legal entity</span></span>

![Importjobb som er sikret etter brukerrolle og juridisk enhet](media/vendor_invoice_automation_04.png)

<span data-ttu-id="75c04-203">Hvis sikkerheten er konfigurert for fakturaimportjobben, bruker unntakslistesiden disse innstillingene.</span><span class="sxs-lookup"><span data-stu-id="75c04-203">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="75c04-204">Brukere vil kunne se bare fakturaunntakspostene som dette oppsettet tillater dem å se.</span><span class="sxs-lookup"><span data-stu-id="75c04-204">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="75c04-205">For eksempel har Contoso besluttet å behandle fakturaunntak etter juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="75c04-205">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="75c04-206">Derfor konfigureres sikkerhet på fakturaimportjobben på en slik måte at en bruker i juridisk enhet A bare kan se fakturaunntak i juridisk enhet A, mens en bruker i juridisk enhet B bare kan se fakturaunntak i juridisk enhet B. Dette oppsettet gjør mulig arbeidsdeling for behandlingen av fakturaunntak.</span><span class="sxs-lookup"><span data-stu-id="75c04-206">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="75c04-207">Contoso kan også bestemme å ikke overholder noen sikkerhet, slik at de samme brukerne kan behandle fakturaunntak for alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="75c04-207">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="75c04-208">Dette oppsettet gjør et scenario med delte tjenester mulig for behandling av fakturaunntak.</span><span class="sxs-lookup"><span data-stu-id="75c04-208">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="75c04-209">Et visningsprogram for vedlegg side ved side i fakturaer</span><span class="sxs-lookup"><span data-stu-id="75c04-209">Side-by-side attachment viewer</span></span>

<span data-ttu-id="75c04-210">For å hjelpe deg med å vise vedlegg for leverandørfakturaer, gir følgende sider som skal brukes i faktureringsprosessen, nå et visningsprogram for vedlegg:</span><span class="sxs-lookup"><span data-stu-id="75c04-210">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="75c04-211">**Unntaksbehandling**</span><span class="sxs-lookup"><span data-stu-id="75c04-211">**Exception handling**</span></span>
+ <span data-ttu-id="75c04-212">**Ventende leverandørfakturaer**-siden (også tilgjengelig i fakturavurderingsprosessen)</span><span class="sxs-lookup"><span data-stu-id="75c04-212">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="75c04-213">**Fakturajournal**-forespørselssiden (for posterte fakturaer)</span><span class="sxs-lookup"><span data-stu-id="75c04-213">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="75c04-214">Her er den viktigste funksjonaliteten som visningsprogrammet for vedlegg inneholder:</span><span class="sxs-lookup"><span data-stu-id="75c04-214">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="75c04-215">Vis alle vedleggstyper som dokumentbehandling støtter (filer, bilder, URL-adresser og merknader).</span><span class="sxs-lookup"><span data-stu-id="75c04-215">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="75c04-216">Vis TIFF-filer med flere sider.</span><span class="sxs-lookup"><span data-stu-id="75c04-216">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="75c04-217">Utfør følgende handlnger med bildefiler:</span><span class="sxs-lookup"><span data-stu-id="75c04-217">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="75c04-218">Uthev deler av bildet.</span><span class="sxs-lookup"><span data-stu-id="75c04-218">Highlight parts of the image.</span></span>
  + <span data-ttu-id="75c04-219">Blokker deler av bildet.</span><span class="sxs-lookup"><span data-stu-id="75c04-219">Block parts of the image.</span></span>
  + <span data-ttu-id="75c04-220">Legg til merknader i bildet.</span><span class="sxs-lookup"><span data-stu-id="75c04-220">Add annotations to the image.</span></span>
  + <span data-ttu-id="75c04-221">Zoom inn og ut på bildet.</span><span class="sxs-lookup"><span data-stu-id="75c04-221">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="75c04-222">Panorer bildet.</span><span class="sxs-lookup"><span data-stu-id="75c04-222">Pan the image.</span></span>
  + <span data-ttu-id="75c04-223">Angre og gjør om handlinger.</span><span class="sxs-lookup"><span data-stu-id="75c04-223">Undo and redo actions.</span></span>
  + <span data-ttu-id="75c04-224">Tilpass bildet til størrelse.</span><span class="sxs-lookup"><span data-stu-id="75c04-224">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="75c04-225">Disse handlingene er tilgjengelig bare for bildefiler (JPEG, TIFF, PNG og så videre).</span><span class="sxs-lookup"><span data-stu-id="75c04-225">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="75c04-226">Eventuelle endringer du gjør et bilde ved hjelp av disse handlingene lagres i bildefilen.</span><span class="sxs-lookup"><span data-stu-id="75c04-226">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="75c04-227">For øyeblikket inkluderer ikke visningsprogrammet for vedlegg funksjoner for versjonskontroll eller overvåking.</span><span class="sxs-lookup"><span data-stu-id="75c04-227">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="75c04-228">Standardvedlegg</span><span class="sxs-lookup"><span data-stu-id="75c04-228">Default attachment</span></span>

<span data-ttu-id="75c04-229">Hvis en leverandørfaktura har mer enn ett vedlegg, kan du angi ett av dokumentene som standardvedlegget på **Vedlegg**-siden.</span><span class="sxs-lookup"><span data-stu-id="75c04-229">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="75c04-230">Alternativet **Er standardvedlegg** er et nytt alternativ som ble lagt til som en del av denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="75c04-230">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="75c04-231">Dette alternativet vises også i dataenheten for dokumentvedlegg for leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="75c04-231">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="75c04-232">Standardvedlegget kan derfor angis via integreringer.</span><span class="sxs-lookup"><span data-stu-id="75c04-232">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="75c04-233">Bare ett dokument kan angis som standardvedlegget.</span><span class="sxs-lookup"><span data-stu-id="75c04-233">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="75c04-234">Når du har opprettet et dokument som standardvedlegget, vises det automatisk i visningsprogrammet for vedlegg når fakturaen åpnes.</span><span class="sxs-lookup"><span data-stu-id="75c04-234">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="75c04-235">Hvis du ikke angir noe dokument som standardvedlegget, viser ikke visningsprogrammet automatisk noen vedlegg når fakturaen åpnes.</span><span class="sxs-lookup"><span data-stu-id="75c04-235">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="75c04-236">Vis/skjul fakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="75c04-236">Show/hide invoice attachments</span></span>

<span data-ttu-id="75c04-237">En ny knapp som er tilgjengelig på forespørselssidene **Behandling av unntak**, **Faktura som venter** og **Fakturajournal**, lar deg vise eller skjule visningsprogrammet for vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-237">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="75c04-238">Sikkerhet</span><span class="sxs-lookup"><span data-stu-id="75c04-238">Security</span></span>

<span data-ttu-id="75c04-239">Følgende handlinger i visningsprogrammet for vedlegg styres via rollebasert sikkerhet:</span><span class="sxs-lookup"><span data-stu-id="75c04-239">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="75c04-240">Utheving</span><span class="sxs-lookup"><span data-stu-id="75c04-240">Highlighting</span></span>
+ <span data-ttu-id="75c04-241">Blokker</span><span class="sxs-lookup"><span data-stu-id="75c04-241">Block</span></span>
+ <span data-ttu-id="75c04-242">Merknad</span><span class="sxs-lookup"><span data-stu-id="75c04-242">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="75c04-243">Siden Ventende leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="75c04-243">Pending vendor invoices page</span></span>

<span data-ttu-id="75c04-244">Følgende rettigheter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknad:</span><span class="sxs-lookup"><span data-stu-id="75c04-244">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="75c04-245">**Vedlikehold leverandørfakturabilde** – denne rettigheten gir lese-/skrivetilgang.</span><span class="sxs-lookup"><span data-stu-id="75c04-245">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="75c04-246">**Vis leverandørfakturabilde** – denne rettigheten gir skrivebeskyttet tilgang.</span><span class="sxs-lookup"><span data-stu-id="75c04-246">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="75c04-247">Følgende plikter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for disse handlingene:</span><span class="sxs-lookup"><span data-stu-id="75c04-247">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="75c04-248">**Vedlikehold leverandørfakturaer** – Rettigheten Vedlikehold leverandørfakturabilde er tilordnet til denne plikten.</span><span class="sxs-lookup"><span data-stu-id="75c04-248">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="75c04-249">**Forespørsel om leverandørfakturastatus** – Rettigheten Vis leverandørfakturabilde er tilordnet til denne plikten.</span><span class="sxs-lookup"><span data-stu-id="75c04-249">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="75c04-250">Følgende roller gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for disse handlingene:</span><span class="sxs-lookup"><span data-stu-id="75c04-250">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="75c04-251">**Regnskapsassistent** og **Regnskapssjef leverandørreskontro** – Plikten Vedlikehold leverandørfakturaer er tilordnet disse rollene.</span><span class="sxs-lookup"><span data-stu-id="75c04-251">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="75c04-252">**Regnskapsassistent**, **Regnskapssjef leverandørreskontro**, **Assistent for sentraliserte leverandørbetalinger** og **Leverandørbetalingsassistent** – Plikten Forespørsel om leverandørfakturastatus er tilordnet til disse rollene.</span><span class="sxs-lookup"><span data-stu-id="75c04-252">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="75c04-253">Side for fakturaunntaksdetaljer</span><span class="sxs-lookup"><span data-stu-id="75c04-253">Invoice exception details page</span></span>

<span data-ttu-id="75c04-254">Følgende rettigheter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknad.</span><span class="sxs-lookup"><span data-stu-id="75c04-254">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="75c04-255">Rett fra esken gir rollene som er nevnt i denne delen, skrivebeskyttet tilgang til fakturabildene i visningsprogrammet for vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-255">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="75c04-256">Hvis en rolle også må ha skrivetilgang til bildene, kan du gi skrivetilgang til denne rollen ved hjelp av rettigheten og plikten som er beskrevet her.</span><span class="sxs-lookup"><span data-stu-id="75c04-256">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="75c04-257">**Vedlikehold bilde for enhet for leverandørfakturahode** – Denne rettigheten gir lese-/skrivetilgang til fakturabildene i visningsprogrammet for vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-257">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="75c04-258">**Vis bilde for enhet for leverandørfakturahode** – Denne rettigheten gir skrivebeskyttet visning av fakturabildet i visningsprogrammet for vedlegg.</span><span class="sxs-lookup"><span data-stu-id="75c04-258">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="75c04-259">Følgende plikter gir skrivebeskyttet tilgang eller til visningsprogrammet for vedlegg for disse handlingene:</span><span class="sxs-lookup"><span data-stu-id="75c04-259">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="75c04-260">**Vedlikehold leverandørfakturaer** – Rettigheten Vedlikehold bilde for enhet for leverandørfakturahode er tilordnet til denne plikten.</span><span class="sxs-lookup"><span data-stu-id="75c04-260">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="75c04-261">Følgende roller gir skrivebeskyttet tilgang eller til visningsprogrammet for vedlegg for disse handlingene:</span><span class="sxs-lookup"><span data-stu-id="75c04-261">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="75c04-262">**Regnskapsassistent** og **Regnskapssjef leverandørreskontro** – Plikten Vedlikehold leverandørfakturaer er tilordnet disse rollene.</span><span class="sxs-lookup"><span data-stu-id="75c04-262">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="75c04-263">Hvis brukerrollen har redigeringsrettigheter på en side, har brukeren som standard også redigeringsrettigheter på visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknader.</span><span class="sxs-lookup"><span data-stu-id="75c04-263">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="75c04-264">Hvis det finnes situasjoner der en bestemt rolle skal ha redigeringsrettigheter på siden, men ikke på visningsprogrammet for vedlegg, kan imidlertid de nødvendige rettighetene i listen ovenfor brukes til å dekke brukstilfellet.</span><span class="sxs-lookup"><span data-stu-id="75c04-264">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>

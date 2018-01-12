---
title: "Automatisering av leverandørfaktura"
description: "Dette emnet forklarer hvilke funksjoner som er tilgjengelige for ende-til-ende-automatisering av leverandørfakturaer, også fakturaer som inneholder vedlegg."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 04809337167741c30677844adad8addeaba303bc
ms.openlocfilehash: e55c4f6fb2168ec1a308c49545f372872610aff0
ms.contentlocale: nb-no
ms.lasthandoff: 01/12/2018

---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="a3432-103">Automatisering av leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="a3432-103">Vendor invoice automation</span></span>

<span data-ttu-id="a3432-104">Dette emnet forklarer hvilke funksjoner som er tilgjengelige for ende-til-ende-automatisering av leverandørfakturaer, også fakturaer som inneholder vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="a3432-105">Organisasjoner som ønsker å strømlinjeforme leverandørprosessene for (AP), identifiserer ofte fakturabehandling som ett av de øverste prosessområdene som bør være mer effektivt.</span><span class="sxs-lookup"><span data-stu-id="a3432-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="a3432-106">I mange tilfeller setter disse organisasjonene behandling av papirfakturaer ut til en tredjepartsleverandør av tjenester for optisk tegngjenkjenning (OCR).</span><span class="sxs-lookup"><span data-stu-id="a3432-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="a3432-107">Deretter mottar de maskinlesbare fakturametadata sammen med et skannet bilde av hver faktura.</span><span class="sxs-lookup"><span data-stu-id="a3432-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="a3432-108">For å få hjelp med automatisering bygges deretter en løsning for den siste delen for å aktivere forbruk av disse artefakterene i faktureringssystemet.</span><span class="sxs-lookup"><span data-stu-id="a3432-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="a3432-109">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition tilbyr nå denne automatiseringen for den siste delen rett fra esken, gjennom en løsning for automatisering av fakturaer.</span><span class="sxs-lookup"><span data-stu-id="a3432-109">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="a3432-110">Løsningskontekst</span><span class="sxs-lookup"><span data-stu-id="a3432-110">Solution context</span></span>

<span data-ttu-id="a3432-111">Fakturaautomatiseringsløsningen gjør det mulig å bruke et standardgrensesnitt som kan godta fakturametadata for fakturahodet og fakturalinjene, og også vedlegg som gjelder for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a3432-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="a3432-112">Eksterne systemer som kan generere artefakter som samsvarer med dette grensesnittet, kan sende feeden til Finance and Operations for automatisk behandling av fakturaer og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="a3432-113">Illustrasjonen nedenfor viser et eksempelscenario for integrasjon der Contoso samarbeider med en OCR-tjenesteleverandør for leverandørfakturabehandling.</span><span class="sxs-lookup"><span data-stu-id="a3432-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="a3432-114">Contosos leverandører sender fakturaer til tjenesteleverandøren via e-post.</span><span class="sxs-lookup"><span data-stu-id="a3432-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="a3432-115">Ved hjelp av OCR-behandling genererer tjenesteleverandøren fakturametadata (hode og/eller linjer) og et skannet bilde på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a3432-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="a3432-116">Et lag med integrasjon omformer deretter disse artefaktene slik at Finance and Operations kan bruke dem.</span><span class="sxs-lookup"><span data-stu-id="a3432-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![Eksempelscenario for integrasjon](media/vendor_invoice_automation_01.png)

<span data-ttu-id="a3432-118">Flere varianter av det forrige scenariet er mulig hvis fakturaintegrasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="a3432-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="a3432-119">Migrering av data er et annet brukstilfelle der dette grensesnittet kan brukes til å opprette fakturaer og vedlegg i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3432-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="a3432-120">Løsningskomponenter</span><span class="sxs-lookup"><span data-stu-id="a3432-120">Solution components</span></span>

<span data-ttu-id="a3432-121">Løsningsavtrykket består av følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="a3432-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="a3432-122">Dataenheter for fakturahodet, fakturalinjene og fakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="a3432-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="a3432-123">Unntaksbehandling for fakturaer</span><span class="sxs-lookup"><span data-stu-id="a3432-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="a3432-124">Et visningsprogram for vedlegg side ved side i fakturaer</span><span class="sxs-lookup"><span data-stu-id="a3432-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="a3432-125">Resten av dette emnet inneholder detaljerte beskrivelser av disse løsningskomponentene.</span><span class="sxs-lookup"><span data-stu-id="a3432-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="a3432-126">Dataenheter</span><span class="sxs-lookup"><span data-stu-id="a3432-126">Data entities</span></span>

<span data-ttu-id="a3432-127">En datapakke er arbeidsenheten som må sendes til Finance and Operations, slik at fakturahoder, fakturalinjer og fakturavedlegg kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="a3432-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="a3432-128">Følgende dataenheter brukes for artefaktene som utgjør datapakken:</span><span class="sxs-lookup"><span data-stu-id="a3432-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="a3432-129">Leverandørfakturahode</span><span class="sxs-lookup"><span data-stu-id="a3432-129">Vendor invoice header</span></span>
+ <span data-ttu-id="a3432-130">Leverandørfakturalinje</span><span class="sxs-lookup"><span data-stu-id="a3432-130">Vendor invoice line</span></span>
+ <span data-ttu-id="a3432-131">Dokumentvedlegg for leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="a3432-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="a3432-132">Dokumentvedlegg for leverandørfaktura er en ny dataenhet som lanseres som en del av denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="a3432-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="a3432-133">Enheten for leverandørfakturahode er blitt endret slik at den støtter vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="a3432-134">Enheten for leverandørfakturalinje er ikke endret for denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="a3432-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="a3432-135">Dette emnet gir ikke en detaljert definisjon av en datapakke.</span><span class="sxs-lookup"><span data-stu-id="a3432-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="a3432-136">Det forklarer heller ikke hvordan du oppretter datapakker.</span><span class="sxs-lookup"><span data-stu-id="a3432-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="a3432-137">Hvis du vil ha denne informasjonen, kan du se [Rammeverk for dataenheter og pakker](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="a3432-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="a3432-138">Bruk følgende fremgangsmåte for å raskt generere testdata som inkluderer fakturaer og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="a3432-139">Logg på forekomsten av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3432-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="a3432-140">Gå til **Leverandører** > **Fakturaer** > **Ventende leverandørfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="a3432-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="a3432-141">Opprett fakturaer som har linjer og vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3432-142">Vedleggene må være hodevedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-142">The attachments must be header attachments.</span></span> <span data-ttu-id="a3432-143">Enheten for dokumentvedlegg for leverandørfaktura støtter for øyeblikket ikke linjevedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="a3432-144">Åpne arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="a3432-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="a3432-145">Opprett en eksportjobb som inkluderer enhetene for leverandørfakturahode, leverandørfakturalinje og dokumentvedlegg for leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="a3432-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="a3432-146">Eksporter dataene.</span><span class="sxs-lookup"><span data-stu-id="a3432-146">Export the data.</span></span>
1. <span data-ttu-id="a3432-147">Last ned de eksporterte dataene som en pakke.</span><span class="sxs-lookup"><span data-stu-id="a3432-147">Download the exported data as a package.</span></span> <span data-ttu-id="a3432-148">Du kan nå bruke pakken til å importere data til målforekomster for testformål.</span><span class="sxs-lookup"><span data-stu-id="a3432-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="a3432-149">Bestemme den juridiske enheten for en faktura</span><span class="sxs-lookup"><span data-stu-id="a3432-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="a3432-150">Fakturaer som importeres via datapakker, kan knyttes til den juridiske enheten som de hører til, på to måter:</span><span class="sxs-lookup"><span data-stu-id="a3432-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="a3432-151">Importjobben som behandler fakturaen, importerer den til det samme firmaet der jobben er planlagt i arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="a3432-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="a3432-152">Med andre ord bestemmer firmaet for jobben hvilket firma som fakturaen tilhører.</span><span class="sxs-lookup"><span data-stu-id="a3432-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="a3432-153">Når datapakken som inneholder fakturaer, sendes til Finance and Operations, kan oppkalleren (det vil si integrasjonprogrammet som kjøres utenfor Finance and Operations) eksplisitt nevne firma-ID-en i HTTP-forespørselen.</span><span class="sxs-lookup"><span data-stu-id="a3432-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="a3432-154">I så fall overstyres firmakonteksten der behandlingsjobben kjører i Finance and Operations, og fakturaene importeres til firmaet som ble sendt via HTTP-forespørselen.</span><span class="sxs-lookup"><span data-stu-id="a3432-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="a3432-155">Dette er standard virkemåte for databehandling.</span><span class="sxs-lookup"><span data-stu-id="a3432-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="a3432-156">Det er beskrevet her, i forbindelse med fakturaer, bare å gi komplett informasjon.</span><span class="sxs-lookup"><span data-stu-id="a3432-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="a3432-157">Behandling av unntak</span><span class="sxs-lookup"><span data-stu-id="a3432-157">Exception processing</span></span>

<span data-ttu-id="a3432-158">I situasjoner der leverandørfakturaer kommer til Finance and Operations via integrasjon, må det være enkelt for et teammedlem i leverandører å behandle unntak eller mislykkede fakturaer og opprette ventende fakturaer fra mislykkede fakturaer.</span><span class="sxs-lookup"><span data-stu-id="a3432-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="a3432-159">Denne unntaksbehandlingen for leverandørfakturaer er nå en del av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3432-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="a3432-160">Side med liste over unntak</span><span class="sxs-lookup"><span data-stu-id="a3432-160">Exceptions list page</span></span>

<span data-ttu-id="a3432-161">Den nye listesiden for fakturaunntak er tilgjengelig på **Leverandører** > **Fakturaer** > **Importfeil** > **Leverandørfakturaer som ikke ble importert**.</span><span class="sxs-lookup"><span data-stu-id="a3432-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="a3432-162">Denne siden viser alle hodepostene for leverandørfakturaer fra oppsamlingstabellen for dataenheten for leverandørfakturahode.</span><span class="sxs-lookup"><span data-stu-id="a3432-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="a3432-163">Vær oppmerksom på at du kan vise de samme postene fra arbeidsområdet **Databehandling**, der du også kan utføre de samme handlingene som er angitt i funksjonen for unntaksbehandling.</span><span class="sxs-lookup"><span data-stu-id="a3432-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="a3432-164">Imidlertid er brukergrensesnittet i funksjonen for unntaksbehandling optimalisert for en funksjonell bruker.</span><span class="sxs-lookup"><span data-stu-id="a3432-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Side med liste over unntak](media/vendor_invoice_automation_02.png)

<span data-ttu-id="a3432-166">Denne listesiden inneholder følgende felt som kommer inn via feeden:</span><span class="sxs-lookup"><span data-stu-id="a3432-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="a3432-167">**Firma** – firmaet som fakturaen tilhører</span><span class="sxs-lookup"><span data-stu-id="a3432-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="a3432-168">**Feilmelding** – feilmeldingen som rammeverket for databehandling utsteder for å forklare hvorfor fakturaen ikke kan opprettes</span><span class="sxs-lookup"><span data-stu-id="a3432-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="a3432-169">**Nummer** – fakturanummeret</span><span class="sxs-lookup"><span data-stu-id="a3432-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="a3432-170">**Fakturakonto**</span><span class="sxs-lookup"><span data-stu-id="a3432-170">**Invoice account**</span></span>
+ <span data-ttu-id="a3432-171">**Navn** – leverandørens navn</span><span class="sxs-lookup"><span data-stu-id="a3432-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="a3432-172">**Leverandørkonto**</span><span class="sxs-lookup"><span data-stu-id="a3432-172">**Vendor account**</span></span>
+ <span data-ttu-id="a3432-173">**Bestilling** – bestillingsnummeret for fakturaen</span><span class="sxs-lookup"><span data-stu-id="a3432-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="a3432-174">**Posteringsdato**</span><span class="sxs-lookup"><span data-stu-id="a3432-174">**Posting date**</span></span>
+ <span data-ttu-id="a3432-175">**Fakturadato**</span><span class="sxs-lookup"><span data-stu-id="a3432-175">**Invoice date**</span></span>
+ <span data-ttu-id="a3432-176">**Fakturabeskrivelse**</span><span class="sxs-lookup"><span data-stu-id="a3432-176">**Invoice description**</span></span>
+ <span data-ttu-id="a3432-177">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="a3432-177">**Currency**</span></span>
+ <span data-ttu-id="a3432-178">**Logg**</span><span class="sxs-lookup"><span data-stu-id="a3432-178">**Log**</span></span>
+ <span data-ttu-id="a3432-179">**Linjereferanse** – identifikatoren som kommer fra det eksterne systemet</span><span class="sxs-lookup"><span data-stu-id="a3432-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3432-180">Linjereferansen ikke er IDen for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a3432-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="a3432-181">Denne listesiden har også en forhåndsvisningsrute som kan brukes på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="a3432-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="a3432-182">Vis hele feilmeldingen, slik at du ikke trenger å utvide **Feilmelding**-kolonnen i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a3432-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="a3432-183">Vis hele listen over vedlegg for fakturaen, hvis vedlegg fulgte med fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a3432-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="a3432-184">Listesiden støtter følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="a3432-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="a3432-185">**Rediger** – åpne unntaksposten i redigeringsmodus, slik at du kan løse problemene.</span><span class="sxs-lookup"><span data-stu-id="a3432-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="a3432-186">**Alternativer** – få tilgang til standardalternativene som er tilgjengelige på listesider.</span><span class="sxs-lookup"><span data-stu-id="a3432-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="a3432-187">Du kan bruke alternativet **Legg til i arbeidsområde** for å feste unntakslistesiden til arbeidsområdet som en liste eller flis.</span><span class="sxs-lookup"><span data-stu-id="a3432-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="a3432-188">Side for unntaksdetaljer</span><span class="sxs-lookup"><span data-stu-id="a3432-188">Exception details page</span></span>

<span data-ttu-id="a3432-189">Når du starter redigeringsmodus, vises siden for unntaksdetaljer for fakturaen som har problemer.</span><span class="sxs-lookup"><span data-stu-id="a3432-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="a3432-190">Hvis det ikke finnes vedlegg, vises fakturaen og standardvedlegget side ved side på siden for unntaksdetaljer.</span><span class="sxs-lookup"><span data-stu-id="a3432-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Side for unntaksdetaljer](media/vendor_invoice_automation_03.png)

<span data-ttu-id="a3432-192">I den forrige illustrasjonen var det ikke noen linjer for leverandørfakturahodet som kom inn.</span><span class="sxs-lookup"><span data-stu-id="a3432-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="a3432-193">Linjedelen er derfor tom.</span><span class="sxs-lookup"><span data-stu-id="a3432-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="a3432-194">Siden for unntaksdetaljer støtter følgende operasjon:</span><span class="sxs-lookup"><span data-stu-id="a3432-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="a3432-195">**Opprett ventende faktura** – Når du har løst problemene på fakturaen som en del av behandling av unntak, kan du klikke denne knappen for å opprette den ventende fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a3432-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="a3432-196">Opprettelse av ventende fakturaer skjer i bakgrunnen (som en asynkron operasjon).</span><span class="sxs-lookup"><span data-stu-id="a3432-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="a3432-197">Unntaksbehandling for delte tjenester i forhold til organisasjonsbasert unntaksbehandling</span><span class="sxs-lookup"><span data-stu-id="a3432-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="a3432-198">Unntakslistesiden støtter standard sikkerhetsbegreper som arbeidsområdet **Databehandling** støtter for behandling av oppsamlingsposter.</span><span class="sxs-lookup"><span data-stu-id="a3432-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="a3432-199">Fakturaimportjobben kan sikres på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="a3432-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="a3432-200">Etter brukerrolle</span><span class="sxs-lookup"><span data-stu-id="a3432-200">By user role</span></span>
+ <span data-ttu-id="a3432-201">Etter bruker</span><span class="sxs-lookup"><span data-stu-id="a3432-201">By user</span></span>
+ <span data-ttu-id="a3432-202">Etter juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="a3432-202">By legal entity</span></span>

![Importjobb som er sikret etter brukerrolle og juridisk enhet](media/vendor_invoice_automation_04.png)

<span data-ttu-id="a3432-204">Hvis sikkerheten er konfigurert for fakturaimportjobben, bruker unntakslistesiden disse innstillingene.</span><span class="sxs-lookup"><span data-stu-id="a3432-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="a3432-205">Brukere vil kunne se bare fakturaunntakspostene som dette oppsettet tillater dem å se.</span><span class="sxs-lookup"><span data-stu-id="a3432-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="a3432-206">For eksempel har Contoso besluttet å behandle fakturaunntak etter juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="a3432-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="a3432-207">Derfor konfigureres sikkerhet på fakturaimportjobben på en slik måte at en bruker i juridisk enhet A bare kan se fakturaunntak i juridisk enhet A, mens en bruker i juridisk enhet B bare kan se fakturaunntak i juridisk enhet B. Dette oppsettet gjør mulig arbeidsdeling for behandlingen av fakturaunntak.</span><span class="sxs-lookup"><span data-stu-id="a3432-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="a3432-208">Contoso kan også bestemme å ikke overholder noen sikkerhet, slik at de samme brukerne kan behandle fakturaunntak for alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="a3432-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="a3432-209">Dette oppsettet gjør et scenario med delte tjenester mulig for behandling av fakturaunntak.</span><span class="sxs-lookup"><span data-stu-id="a3432-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="a3432-210">Et visningsprogram for vedlegg side ved side i fakturaer</span><span class="sxs-lookup"><span data-stu-id="a3432-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="a3432-211">For å hjelpe deg med å vise vedlegg for leverandørfakturaer, gir følgende sider som skal brukes i faktureringsprosessen, nå et visningsprogram for vedlegg:</span><span class="sxs-lookup"><span data-stu-id="a3432-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="a3432-212">**Unntaksbehandling**</span><span class="sxs-lookup"><span data-stu-id="a3432-212">**Exception handling**</span></span>
+ <span data-ttu-id="a3432-213">**Ventende leverandørfakturaer**-siden (også tilgjengelig i fakturavurderingsprosessen)</span><span class="sxs-lookup"><span data-stu-id="a3432-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="a3432-214">**Fakturajournal**-forespørselssiden (for posterte fakturaer)</span><span class="sxs-lookup"><span data-stu-id="a3432-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="a3432-215">Her er den viktigste funksjonaliteten som visningsprogrammet for vedlegg inneholder:</span><span class="sxs-lookup"><span data-stu-id="a3432-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="a3432-216">Vis alle vedleggstyper som dokumentbehandling støtter (filer, bilder, URL-adresser og merknader).</span><span class="sxs-lookup"><span data-stu-id="a3432-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="a3432-217">Vis TIFF-filer med flere sider.</span><span class="sxs-lookup"><span data-stu-id="a3432-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="a3432-218">Utfør følgende handlnger med bildefiler:</span><span class="sxs-lookup"><span data-stu-id="a3432-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="a3432-219">Uthev deler av bildet.</span><span class="sxs-lookup"><span data-stu-id="a3432-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="a3432-220">Blokker deler av bildet.</span><span class="sxs-lookup"><span data-stu-id="a3432-220">Block parts of the image.</span></span>
  + <span data-ttu-id="a3432-221">Legg til merknader i bildet.</span><span class="sxs-lookup"><span data-stu-id="a3432-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="a3432-222">Zoom inn og ut på bildet.</span><span class="sxs-lookup"><span data-stu-id="a3432-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="a3432-223">Panorer bildet.</span><span class="sxs-lookup"><span data-stu-id="a3432-223">Pan the image.</span></span>
  + <span data-ttu-id="a3432-224">Angre og gjør om handlinger.</span><span class="sxs-lookup"><span data-stu-id="a3432-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="a3432-225">Tilpass bildet til størrelse.</span><span class="sxs-lookup"><span data-stu-id="a3432-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="a3432-226">Disse handlingene er tilgjengelig bare for bildefiler (JPEG, TIFF, PNG og så videre).</span><span class="sxs-lookup"><span data-stu-id="a3432-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="a3432-227">Eventuelle endringer du gjør et bilde ved hjelp av disse handlingene lagres i bildefilen.</span><span class="sxs-lookup"><span data-stu-id="a3432-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="a3432-228">For øyeblikket inkluderer ikke visningsprogrammet for vedlegg funksjoner for versjonskontroll eller overvåking.</span><span class="sxs-lookup"><span data-stu-id="a3432-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="a3432-229">Standardvedlegg</span><span class="sxs-lookup"><span data-stu-id="a3432-229">Default attachment</span></span>

<span data-ttu-id="a3432-230">Hvis en leverandørfaktura har mer enn ett vedlegg, kan du angi ett av dokumentene som standardvedlegget på **Vedlegg**-siden.</span><span class="sxs-lookup"><span data-stu-id="a3432-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="a3432-231">Alternativet **Er standardvedlegg** er et nytt alternativ som ble lagt til som en del av denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="a3432-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="a3432-232">Dette alternativet vises også i dataenheten for dokumentvedlegg for leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="a3432-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="a3432-233">Standardvedlegget kan derfor angis via integreringer.</span><span class="sxs-lookup"><span data-stu-id="a3432-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="a3432-234">Bare ett dokument kan angis som standardvedlegget.</span><span class="sxs-lookup"><span data-stu-id="a3432-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="a3432-235">Når du har opprettet et dokument som standardvedlegget, vises det automatisk i visningsprogrammet for vedlegg når fakturaen åpnes.</span><span class="sxs-lookup"><span data-stu-id="a3432-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="a3432-236">Hvis du ikke angir noe dokument som standardvedlegget, viser ikke visningsprogrammet automatisk noen vedlegg når fakturaen åpnes.</span><span class="sxs-lookup"><span data-stu-id="a3432-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="a3432-237">Vis/skjul fakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="a3432-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="a3432-238">En ny knapp som er tilgjengelig på forespørselssidene **Behandling av unntak**, **Faktura som venter** og **Fakturajournal**, lar deg vise eller skjule visningsprogrammet for vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="a3432-239">Sikkerhet</span><span class="sxs-lookup"><span data-stu-id="a3432-239">Security</span></span>

<span data-ttu-id="a3432-240">Følgende handlinger i visningsprogrammet for vedlegg styres via rollebasert sikkerhet:</span><span class="sxs-lookup"><span data-stu-id="a3432-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="a3432-241">Utheving</span><span class="sxs-lookup"><span data-stu-id="a3432-241">Highlighting</span></span>
+ <span data-ttu-id="a3432-242">Blokker</span><span class="sxs-lookup"><span data-stu-id="a3432-242">Block</span></span>
+ <span data-ttu-id="a3432-243">Merknad</span><span class="sxs-lookup"><span data-stu-id="a3432-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="a3432-244">Siden Ventende leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="a3432-244">Pending vendor invoices page</span></span>

<span data-ttu-id="a3432-245">Følgende rettigheter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknad:</span><span class="sxs-lookup"><span data-stu-id="a3432-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="a3432-246">**Vedlikehold leverandørfakturabilde** – denne rettigheten gir lese-/skrivetilgang.</span><span class="sxs-lookup"><span data-stu-id="a3432-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="a3432-247">**Vis leverandørfakturabilde** – denne rettigheten gir skrivebeskyttet tilgang.</span><span class="sxs-lookup"><span data-stu-id="a3432-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="a3432-248">Følgende plikter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for disse handlingene:</span><span class="sxs-lookup"><span data-stu-id="a3432-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a3432-249">**Vedlikehold leverandørfakturaer** – Rettigheten Vedlikehold leverandørfakturabilde er tilordnet til denne plikten.</span><span class="sxs-lookup"><span data-stu-id="a3432-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="a3432-250">**Forespørsel om leverandørfakturastatus** – Rettigheten Vis leverandørfakturabilde er tilordnet til denne plikten.</span><span class="sxs-lookup"><span data-stu-id="a3432-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="a3432-251">Følgende roller gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for disse handlingene:</span><span class="sxs-lookup"><span data-stu-id="a3432-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a3432-252">**Regnskapsassistent** og **Regnskapssjef leverandørreskontro** – Plikten Vedlikehold leverandørfakturaer er tilordnet disse rollene.</span><span class="sxs-lookup"><span data-stu-id="a3432-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="a3432-253">**Regnskapsassistent**, **Regnskapssjef leverandørreskontro**, **Assistent for sentraliserte leverandørbetalinger** og **Leverandørbetalingsassistent** – Plikten Forespørsel om leverandørfakturastatus er tilordnet til disse rollene.</span><span class="sxs-lookup"><span data-stu-id="a3432-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="a3432-254">Side for fakturaunntaksdetaljer</span><span class="sxs-lookup"><span data-stu-id="a3432-254">Invoice exception details page</span></span>

<span data-ttu-id="a3432-255">Følgende rettigheter gir skrivebeskyttet tilgang eller lese-/skrivetilgang til visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknad.</span><span class="sxs-lookup"><span data-stu-id="a3432-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="a3432-256">Rett fra esken gir rollene som er nevnt i denne delen, skrivebeskyttet tilgang til fakturabildene i visningsprogrammet for vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="a3432-257">Hvis en rolle også må ha skrivetilgang til bildene, kan du gi skrivetilgang til denne rollen ved hjelp av rettigheten og plikten som er beskrevet her.</span><span class="sxs-lookup"><span data-stu-id="a3432-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="a3432-258">**Vedlikehold bilde for enhet for leverandørfakturahode** – Denne rettigheten gir lese-/skrivetilgang til fakturabildene i visningsprogrammet for vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="a3432-259">**Vis bilde for enhet for leverandørfakturahode** – Denne rettigheten gir skrivebeskyttet visning av fakturabildet i visningsprogrammet for vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a3432-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="a3432-260">Følgende plikter gir skrivebeskyttet tilgang eller til visningsprogrammet for vedlegg for disse handlingene:</span><span class="sxs-lookup"><span data-stu-id="a3432-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a3432-261">**Vedlikehold leverandørfakturaer** – Rettigheten Vedlikehold bilde for enhet for leverandørfakturahode er tilordnet til denne plikten.</span><span class="sxs-lookup"><span data-stu-id="a3432-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="a3432-262">Følgende roller gir skrivebeskyttet tilgang eller til visningsprogrammet for vedlegg for disse handlingene:</span><span class="sxs-lookup"><span data-stu-id="a3432-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a3432-263">**Regnskapsassistent** og **Regnskapssjef leverandørreskontro** – Plikten Vedlikehold leverandørfakturaer er tilordnet disse rollene.</span><span class="sxs-lookup"><span data-stu-id="a3432-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="a3432-264">Hvis brukerrollen har redigeringsrettigheter på en side, har brukeren som standard også redigeringsrettigheter på visningsprogrammet for vedlegg for handlingene for utheving, blokkering og merknader.</span><span class="sxs-lookup"><span data-stu-id="a3432-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="a3432-265">Hvis det finnes situasjoner der en bestemt rolle skal ha redigeringsrettigheter på siden, men ikke på visningsprogrammet for vedlegg, kan imidlertid de nødvendige rettighetene i listen ovenfor brukes til å dekke brukstilfellet.</span><span class="sxs-lookup"><span data-stu-id="a3432-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>


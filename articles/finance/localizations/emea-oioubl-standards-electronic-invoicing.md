---
title: Standarder som støttes for elektronisk fakturering i Europa
description: Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering for Europa.
author: mrolecki
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3ed98c268af841b1625f547c79f271f3e3a81b74
ms.sourcegitcommit: 3d16522c00ba2d30aa43befbf1b7b3eaad377325
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/20/2020
ms.locfileid: "4592468"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="d33bf-103">Standarder som støttes for elektronisk fakturering i Europa</span><span class="sxs-lookup"><span data-stu-id="d33bf-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d33bf-104">Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering for Europa.</span><span class="sxs-lookup"><span data-stu-id="d33bf-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="d33bf-105">Implementering og bruk av elektronisk fakturering i hele EU er regulert [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), noe som påvirker alle EU-medlemsland.</span><span class="sxs-lookup"><span data-stu-id="d33bf-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="d33bf-106">Bedrifter som ønsker å dra nytte av elektronisk fakturering må sende salgsordrefakturaer, fritekstfakturaer, prosjektfakturaer, salgsordre, kreditnotaer og prosjekt faktura kreditnotaer som XML-filer til den offentlig myndighet eller andre handelspartneren parter som kreve bruk av elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="d33bf-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="d33bf-107">Disse XML-filer må oppfylle visse standarder.</span><span class="sxs-lookup"><span data-stu-id="d33bf-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="d33bf-108">Landspesifikke behovene og implementeringen kan variere på tvers av EU-medlemsland, men de bruker ofte UNC Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskjellige versjoner med tilpasninger i tillegg til [PEPPOL](https://www.peppol.eu) spesifikasjoner og tilgangspunkt for validering og transport.</span><span class="sxs-lookup"><span data-stu-id="d33bf-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="d33bf-109">Primære fordelen med UBL er at forretningsdokumenter kan standardisert for ulike formål.</span><span class="sxs-lookup"><span data-stu-id="d33bf-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="d33bf-110">Siden UBL er en fleksibel, internasjonal standard som støtter mange forretningskrav, kan disse forretningsdokumenter utveksles på tvers av landegrenser.</span><span class="sxs-lookup"><span data-stu-id="d33bf-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="electronic-invoice-formats-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="d33bf-111">Elektroniske fakturaformater er for øyeblikket tilgjengelige i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d33bf-111">Electronic invoice formats currently available in Dynamics 365 Finance</span></span>

<span data-ttu-id="d33bf-112">Følgende landspesifikke formater av elektroniske fakturaer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="d33bf-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="d33bf-113">OIOUBL v.2.02 for Danmark</span><span class="sxs-lookup"><span data-stu-id="d33bf-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="d33bf-114">EHF v. 3.0 for Norge</span><span class="sxs-lookup"><span data-stu-id="d33bf-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="d33bf-115">PEPPOL BIS v.2 for Østerrike, Frankrike og Belgia</span><span class="sxs-lookup"><span data-stu-id="d33bf-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="d33bf-116">UBL-OHNL 1.9 for Nederland</span><span class="sxs-lookup"><span data-stu-id="d33bf-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="d33bf-117">FacturaE v.3.2.1 for Spania</span><span class="sxs-lookup"><span data-stu-id="d33bf-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="d33bf-118">FatturaPA v.1.2 for Italia</span><span class="sxs-lookup"><span data-stu-id="d33bf-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="d33bf-119">xRechnung v. 1.2 for Tyskland</span><span class="sxs-lookup"><span data-stu-id="d33bf-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="d33bf-120">Åpne PEPPOL BIS Billing v. 3.0 for den europeiske union</span><span class="sxs-lookup"><span data-stu-id="d33bf-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>
-   <span data-ttu-id="d33bf-121">Estisk spesifikt format, versjon 1.2</span><span class="sxs-lookup"><span data-stu-id="d33bf-121">Estonian specific format version 1.2</span></span>
-   <span data-ttu-id="d33bf-122">Finvoice 3.0 for Finland</span><span class="sxs-lookup"><span data-stu-id="d33bf-122">Finvoice 3.0 for Finland</span></span>

<span data-ttu-id="d33bf-123">Elektronisk fakturering er basert på [elektronisk rapportering](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="d33bf-123">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="d33bf-124">En datamodell for **Fakturamodell**, fakturamodelltilordning og flere lands-/områdespesifikke ER-formatkonfigurasjoner er opprettet for følgende land/områder:</span><span class="sxs-lookup"><span data-stu-id="d33bf-124">An **Invoice model** data model, invoice model mapping, and several country/region-specific ER format configurations have been created for the following countries/regions:</span></span> 

- <span data-ttu-id="d33bf-125">Østerrike (AT)</span><span class="sxs-lookup"><span data-stu-id="d33bf-125">Austria (AT)</span></span>
- <span data-ttu-id="d33bf-126">Danmark (DK)</span><span class="sxs-lookup"><span data-stu-id="d33bf-126">Denmark (DK)</span></span>
- <span data-ttu-id="d33bf-127">Italia (IT)</span><span class="sxs-lookup"><span data-stu-id="d33bf-127">Italy (IT)</span></span>
- <span data-ttu-id="d33bf-128">Norge (NO)</span><span class="sxs-lookup"><span data-stu-id="d33bf-128">Norway (NO)</span></span>
- <span data-ttu-id="d33bf-129">Spania (ES)</span><span class="sxs-lookup"><span data-stu-id="d33bf-129">Spain (ES)</span></span>
- <span data-ttu-id="d33bf-130">Frankrike (FR)</span><span class="sxs-lookup"><span data-stu-id="d33bf-130">France (FR)</span></span>
- <span data-ttu-id="d33bf-131">Belgia (BE)</span><span class="sxs-lookup"><span data-stu-id="d33bf-131">Belgium (BE)</span></span>
- <span data-ttu-id="d33bf-132">Nederland (BE)</span><span class="sxs-lookup"><span data-stu-id="d33bf-132">The Netherlands (NL)</span></span>
- <span data-ttu-id="d33bf-133">Tyskland (DE)</span><span class="sxs-lookup"><span data-stu-id="d33bf-133">Germany (DE)</span></span>
- <span data-ttu-id="d33bf-134">Estland (EE)</span><span class="sxs-lookup"><span data-stu-id="d33bf-134">Estonia (EE)</span></span>
- <span data-ttu-id="d33bf-135">Finland (FI)</span><span class="sxs-lookup"><span data-stu-id="d33bf-135">Finland (FI)</span></span>
- <span data-ttu-id="d33bf-136">Den europeiske union (EU)</span><span class="sxs-lookup"><span data-stu-id="d33bf-136">The European Union (EU)</span></span>

<span data-ttu-id="d33bf-137">Datamodellen for **Fakturamodell**, fakturamodelltilordningen og de lands-/områdespesifikke ER-formatkonfigurasjonene omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="d33bf-137">The **Invoice model** data model, invoice model mapping, and country/region-specific ER format configurations include:</span></span>

-   <span data-ttu-id="d33bf-138">OIOUBL salgsfaktura - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="d33bf-138">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="d33bf-139">OIOUBL salgskreditnota - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="d33bf-139">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="d33bf-140">OIOUBL prosjektfaktura - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="d33bf-140">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="d33bf-141">OIOUBL prosjektkreditnota - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="d33bf-141">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="d33bf-142">UBL salgsfaktura FR</span><span class="sxs-lookup"><span data-stu-id="d33bf-142">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="d33bf-143">UBL salgskreditnota FR</span><span class="sxs-lookup"><span data-stu-id="d33bf-143">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="d33bf-144">UBL prosjektfaktura FR</span><span class="sxs-lookup"><span data-stu-id="d33bf-144">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="d33bf-145">UBL prosjektkreditnota FR</span><span class="sxs-lookup"><span data-stu-id="d33bf-145">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="d33bf-146">UBL salgsfaktura BE</span><span class="sxs-lookup"><span data-stu-id="d33bf-146">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="d33bf-147">UBL salgskreditnota BE</span><span class="sxs-lookup"><span data-stu-id="d33bf-147">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="d33bf-148">UBL prosjektfaktura BE</span><span class="sxs-lookup"><span data-stu-id="d33bf-148">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="d33bf-149">UBL prosjektkreditnota BE</span><span class="sxs-lookup"><span data-stu-id="d33bf-149">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="d33bf-150">UBL salgsfaktura NL</span><span class="sxs-lookup"><span data-stu-id="d33bf-150">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="d33bf-151">UBL salgskreditnota NL</span><span class="sxs-lookup"><span data-stu-id="d33bf-151">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="d33bf-152">UBL prosjektfaktura NL</span><span class="sxs-lookup"><span data-stu-id="d33bf-152">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="d33bf-153">UBL prosjektkreditnota NL</span><span class="sxs-lookup"><span data-stu-id="d33bf-153">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="d33bf-154">Salgsfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="d33bf-154">Sales invoice (ES)</span></span>
-   <span data-ttu-id="d33bf-155">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="d33bf-155">Sales invoice (IT)</span></span>
-   <span data-ttu-id="d33bf-156">Prosjektfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="d33bf-156">Project invoice (ES)</span></span>
-   <span data-ttu-id="d33bf-157">Prosjektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="d33bf-157">Project invoice (IT)</span></span>
-   <span data-ttu-id="d33bf-158">Salgsfaktura DE</span><span class="sxs-lookup"><span data-stu-id="d33bf-158">Sales Invoice DE</span></span>
-   <span data-ttu-id="d33bf-159">Prosjektfaktura DE</span><span class="sxs-lookup"><span data-stu-id="d33bf-159">Project Invoice DE</span></span>
-   <span data-ttu-id="d33bf-160">Peppol-salgsfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="d33bf-160">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="d33bf-161">Peppol-salgskreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="d33bf-161">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="d33bf-162">Peppol-prosjektfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="d33bf-162">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="d33bf-163">Peppol-prosjektkreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="d33bf-163">Peppol Project Credit Note - for EU</span></span>
-   <span data-ttu-id="d33bf-164">Salgsfaktura (EE)</span><span class="sxs-lookup"><span data-stu-id="d33bf-164">Sales invoice (EE)</span></span>
-   <span data-ttu-id="d33bf-165">Prosjektfaktura (EE)</span><span class="sxs-lookup"><span data-stu-id="d33bf-165">Project invoice (EE)</span></span>
-   <span data-ttu-id="d33bf-166">Salgsfaktura (FI)</span><span class="sxs-lookup"><span data-stu-id="d33bf-166">Sales invoice (FI)</span></span>
-   <span data-ttu-id="d33bf-167">Prosjektfaktura (FI)</span><span class="sxs-lookup"><span data-stu-id="d33bf-167">Project invoice (FI)</span></span>

<span data-ttu-id="d33bf-168">De elektroniske fakturaene og kreditnotaene du genrerer, inneholder obligatorisk informasjon, for eksempel EAN-nummeret, ordrenummer, kontakt, dimensjonskontokode og adresseopplysninger for kunden.</span><span class="sxs-lookup"><span data-stu-id="d33bf-168">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="d33bf-169">Valideringsregler brukes når fakturaer genereres, slik at du kan verifisere at riktig informasjon er angitt.</span><span class="sxs-lookup"><span data-stu-id="d33bf-169">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="d33bf-170">Settet med nødvendig informasjon kan variere fra land til land.</span><span class="sxs-lookup"><span data-stu-id="d33bf-170">The set of required information may differ from country to country.</span></span> <span data-ttu-id="d33bf-171">Siden både kravene og de støttede landene og formatene kan endres, bør du alltid gå til det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) og vise den mest oppdaterte listen over tilgjengelige filer som har aktivatypen **GER-konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="d33bf-171">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle Services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="electronic-invoice-configuration"></a><span data-ttu-id="d33bf-172">Konfigurasjon av elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="d33bf-172">Electronic invoice configuration</span></span>
<span data-ttu-id="d33bf-173">Konfigurasjonen av og detaljene i elektroniske fakturaer avhenger av landet/området den er implementert for.</span><span class="sxs-lookup"><span data-stu-id="d33bf-173">The setup and specifics of electronic invoices depend on the country/region that it's implemented for.</span></span> <span data-ttu-id="d33bf-174">Hvis du vil ha mer informasjon om hvordan du konfigurerer og bruker elektroniske fakturaer for kunder, kan du se de relaterte landsspesifikke emnene:</span><span class="sxs-lookup"><span data-stu-id="d33bf-174">For more information about how to set up and use customer electronic invoices, see the related country-specific topics:</span></span>

- [<span data-ttu-id="d33bf-175">Italia</span><span class="sxs-lookup"><span data-stu-id="d33bf-175">Italy</span></span>](emea-ita-e-invoices.md)
- [<span data-ttu-id="d33bf-176">Norge</span><span class="sxs-lookup"><span data-stu-id="d33bf-176">Norway</span></span>](emea-nor-e-invoices.md)
- [<span data-ttu-id="d33bf-177">Tyskland</span><span class="sxs-lookup"><span data-stu-id="d33bf-177">Germany</span></span>](emea-deu-e-invoices.md)
- [<span data-ttu-id="d33bf-178">Finland</span><span class="sxs-lookup"><span data-stu-id="d33bf-178">Finland</span></span>](https://support.microsoft.com/help/4559937)
- [<span data-ttu-id="d33bf-179">Estland</span><span class="sxs-lookup"><span data-stu-id="d33bf-179">Estonia</span></span>](https://support.microsoft.com/help/4552679)
- [<span data-ttu-id="d33bf-180">PEPPOL</span><span class="sxs-lookup"><span data-stu-id="d33bf-180">PEPPOL</span></span>](https://support.microsoft.com/help/4490320)

## <a name="additional-resources"></a><span data-ttu-id="d33bf-181">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d33bf-181">Additional resources</span></span>
<span data-ttu-id="d33bf-182">Hvis du vil ha mer informasjon om hvordan du konfigurerer elektroniske fakturaer, kan du spille av følgende [Oppgaveveiledninger](../../fin-and-ops/get-started/help-overview.md#task-guides) i Hjelp-ruten:</span><span class="sxs-lookup"><span data-stu-id="d33bf-182">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="d33bf-183">Definere elektronisk fakturering for OIOUBL</span><span class="sxs-lookup"><span data-stu-id="d33bf-183">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="d33bf-184">Importere konfigurasjoner for elektroniske OIOUBL-faktureringer</span><span class="sxs-lookup"><span data-stu-id="d33bf-184">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="d33bf-185">Definere kundekontoer for elektronisk fakturering med OIOUBL</span><span class="sxs-lookup"><span data-stu-id="d33bf-185">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="d33bf-186">Selv om disse oppgaveveiledningene ble opprettet for det danske e-fakturaformatet *OIOUBL*, gjelder de for andre støttede land/områder med mindre avvik.</span><span class="sxs-lookup"><span data-stu-id="d33bf-186">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries/regions with minor deviations.</span></span>

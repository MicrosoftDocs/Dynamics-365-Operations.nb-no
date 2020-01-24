---
title: Standarder som støttes for elektronisk fakturering i Europa
description: Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering for Europa.
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
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
ms.openlocfilehash: 2fb188498705dcbad841645ced43e6a1715cbbd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915165"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="9f089-103">Standarder som støttes for elektronisk fakturering i Europa</span><span class="sxs-lookup"><span data-stu-id="9f089-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f089-104">Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering for Europa.</span><span class="sxs-lookup"><span data-stu-id="9f089-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="9f089-105">Implementering og bruk av elektronisk fakturering i hele EU er regulert [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), noe som påvirker alle EU-medlemsland.</span><span class="sxs-lookup"><span data-stu-id="9f089-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="9f089-106">Bedrifter som ønsker å dra nytte av elektronisk fakturering må sende salgsordrefakturaer, fritekstfakturaer, prosjektfakturaer, salgsordre, kreditnotaer og prosjekt faktura kreditnotaer som XML-filer til den offentlig myndighet eller andre handelspartneren parter som kreve bruk av elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="9f089-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="9f089-107">Disse XML-filer må oppfylle visse standarder.</span><span class="sxs-lookup"><span data-stu-id="9f089-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="9f089-108">Landspesifikke behovene og implementeringen kan variere på tvers av EU-medlemsland, men de bruker ofte UNC Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskjellige versjoner med tilpasninger i tillegg til [PEPPOL](https://www.peppol.eu) spesifikasjoner og tilgangspunkt for validering og transport.</span><span class="sxs-lookup"><span data-stu-id="9f089-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="9f089-109">Primære fordelen med UBL er at forretningsdokumenter kan standardisert for ulike formål.</span><span class="sxs-lookup"><span data-stu-id="9f089-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="9f089-110">Siden UBL er en fleksibel, internasjonal standard som støtter mange forretningskrav, kan disse forretningsdokumenter utveksles på tvers av landegrenser.</span><span class="sxs-lookup"><span data-stu-id="9f089-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="9f089-111">Hvilke formater for elektroniske fakturaer er tilgjengelige i Dynamics 365 Finance?</span><span class="sxs-lookup"><span data-stu-id="9f089-111">What electronic invoice formats are currently available in Dynamics 365 Finance?</span></span>

<span data-ttu-id="9f089-112">Følgende landspesifikke formater av elektroniske fakturaer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="9f089-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="9f089-113">OIOUBL v.2.02 for Danmark</span><span class="sxs-lookup"><span data-stu-id="9f089-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="9f089-114">EHF v. 3.0 for Norge</span><span class="sxs-lookup"><span data-stu-id="9f089-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="9f089-115">PEPPOL BIS v.2 for Østerrike, Frankrike og Belgia</span><span class="sxs-lookup"><span data-stu-id="9f089-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="9f089-116">UBL-OHNL 1.9 for Nederland</span><span class="sxs-lookup"><span data-stu-id="9f089-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="9f089-117">FacturaE v.3.2.1 for Spania</span><span class="sxs-lookup"><span data-stu-id="9f089-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="9f089-118">FatturaPA v.1.2 for Italia</span><span class="sxs-lookup"><span data-stu-id="9f089-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="9f089-119">xRechnung v. 1.2 for Tyskland</span><span class="sxs-lookup"><span data-stu-id="9f089-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="9f089-120">Åpne PEPPOL BIS Billing v. 3.0 for den europeiske union</span><span class="sxs-lookup"><span data-stu-id="9f089-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>

<span data-ttu-id="9f089-121">Elektronisk fakturering er basert på [elektronisk rapportering](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9f089-121">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="9f089-122">En **Kundefakturamodell**-datamodell og flere lands/områdespesifikke ER-formatkonfigurasjoner er opprettet for Østerrike (AT), Danmark (DK), Italia (IT), Norge (NO), Spania (ES), Frankrike (FR), Belgia (BE), Nederland (NL), Tyskland (DE) og den europeiske uniun (EU).</span><span class="sxs-lookup"><span data-stu-id="9f089-122">A **Customer invoice model** data model and several country/region-specific ER format configurations have been created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), the Netherlands (NL), Germany (DE), and the European Union (EU).</span></span>

-   <span data-ttu-id="9f089-123">OIOUBL salgsfaktura - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="9f089-123">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="9f089-124">OIOUBL salgskreditnota - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="9f089-124">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="9f089-125">OIOUBL prosjektfaktura - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="9f089-125">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="9f089-126">OIOUBL prosjektkreditnota - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="9f089-126">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="9f089-127">UBL salgsfaktura FR</span><span class="sxs-lookup"><span data-stu-id="9f089-127">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="9f089-128">UBL salgskreditnota FR</span><span class="sxs-lookup"><span data-stu-id="9f089-128">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="9f089-129">UBL prosjektfaktura FR</span><span class="sxs-lookup"><span data-stu-id="9f089-129">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="9f089-130">UBL prosjektkreditnota FR</span><span class="sxs-lookup"><span data-stu-id="9f089-130">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="9f089-131">UBL salgsfaktura BE</span><span class="sxs-lookup"><span data-stu-id="9f089-131">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="9f089-132">UBL salgskreditnota BE</span><span class="sxs-lookup"><span data-stu-id="9f089-132">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="9f089-133">UBL prosjektfaktura BE</span><span class="sxs-lookup"><span data-stu-id="9f089-133">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="9f089-134">UBL prosjektkreditnota BE</span><span class="sxs-lookup"><span data-stu-id="9f089-134">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="9f089-135">UBL salgsfaktura NL</span><span class="sxs-lookup"><span data-stu-id="9f089-135">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="9f089-136">UBL salgskreditnota NL</span><span class="sxs-lookup"><span data-stu-id="9f089-136">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="9f089-137">UBL prosjektfaktura NL</span><span class="sxs-lookup"><span data-stu-id="9f089-137">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="9f089-138">UBL prosjektkreditnota NL</span><span class="sxs-lookup"><span data-stu-id="9f089-138">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="9f089-139">Salgsfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="9f089-139">Sales invoice (ES)</span></span>
-   <span data-ttu-id="9f089-140">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="9f089-140">Sales invoice (IT)</span></span>
-   <span data-ttu-id="9f089-141">Prosjektfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="9f089-141">Project invoice (ES)</span></span>
-   <span data-ttu-id="9f089-142">Prosjektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="9f089-142">Project invoice (IT)</span></span>
-   <span data-ttu-id="9f089-143">Salgsfaktura DE</span><span class="sxs-lookup"><span data-stu-id="9f089-143">Sales Invoice DE</span></span>
-   <span data-ttu-id="9f089-144">Prosjektfaktura DE</span><span class="sxs-lookup"><span data-stu-id="9f089-144">Project Invoice DE</span></span>
-   <span data-ttu-id="9f089-145">Peppol-salgsfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="9f089-145">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="9f089-146">Peppol-salgskreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="9f089-146">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="9f089-147">Peppol-prosjektfaktura - for EU</span><span class="sxs-lookup"><span data-stu-id="9f089-147">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="9f089-148">Peppol-prosjektkreditnota - for EU</span><span class="sxs-lookup"><span data-stu-id="9f089-148">Peppol Project Credit Note - for EU</span></span>

<span data-ttu-id="9f089-149">De elektroniske fakturaene og kreditnotaene du genrerer, inneholder obligatorisk informasjon, for eksempel EAN-nummeret, ordrenummer, kontakt, dimensjonskontokode og adresseopplysninger for kunden.</span><span class="sxs-lookup"><span data-stu-id="9f089-149">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="9f089-150">Valideringsregler brukes når fakturaer genereres, slik at du kan verifisere at riktig informasjon er angitt.</span><span class="sxs-lookup"><span data-stu-id="9f089-150">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="9f089-151">Settet med nødvendig informasjon kan variere fra land til land.</span><span class="sxs-lookup"><span data-stu-id="9f089-151">The set of required information may differ from country to country.</span></span> <span data-ttu-id="9f089-152">Siden både kravene og de støttede landene og formatene kan endres, bør du alltid gå til det delte ativabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) og viser den mest oppdaterte listen over tilgjengelige filer som har aktivatypen **TYSK konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="9f089-152">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="9f089-153">Tilleggsinformasjon</span><span class="sxs-lookup"><span data-stu-id="9f089-153">Additional information</span></span>
<span data-ttu-id="9f089-154">Hvis du vil ha mer informasjon om hvordan du konfigurerer elektroniske fakturaer, kan du spille av følgende [Oppgaveveiledninger](../../fin-and-ops/get-started/help-overview.md#task-guides) i Hjelp-ruten:</span><span class="sxs-lookup"><span data-stu-id="9f089-154">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="9f089-155">Definere elektronisk fakturering for OIOUBL</span><span class="sxs-lookup"><span data-stu-id="9f089-155">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="9f089-156">Importere konfigurasjoner for elektroniske OIOUBL-faktureringer</span><span class="sxs-lookup"><span data-stu-id="9f089-156">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="9f089-157">Definere kundekontoer for elektronisk fakturering med OIOUBL</span><span class="sxs-lookup"><span data-stu-id="9f089-157">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="9f089-158">Selv om disse oppgaveveiledningene ble opprettet for dansk spesifikt format for e-faktura *OIOUBL*, de som kan brukes av andre støttede land med mindre avvik.</span><span class="sxs-lookup"><span data-stu-id="9f089-158">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>

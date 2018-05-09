---
title: "Standarder som støttes for elektronisk fakturering i Europa"
description: "Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering i Microsoft Dynamics 365 for Finance and Operations i den europeiske regionen."
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: 
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 366e67415b82c6bbc6b066b4ce44e4654bd93103
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="247c1-103">Standarder som støttes for elektronisk fakturering i Europa</span><span class="sxs-lookup"><span data-stu-id="247c1-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="247c1-104">Dette emnet forklarer dekningsnivået som finnes for elektronisk fakturering for Europa.</span><span class="sxs-lookup"><span data-stu-id="247c1-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="247c1-105">Implementering og bruk av elektronisk fakturering i hele EU er regulert [Council Directive 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), noe som påvirker alle EU-medlemsland.</span><span class="sxs-lookup"><span data-stu-id="247c1-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="247c1-106">Bedrifter som ønsker å dra nytte av elektronisk fakturering må sende salgsordrefakturaer, fritekstfakturaer, prosjektfakturaer, salgsordre, kreditnotaer og prosjekt faktura kreditnotaer som XML-filer til den offentlig myndighet eller andre handelspartneren parter som kreve bruk av elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="247c1-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="247c1-107">Disse XML-filer må oppfylle visse standarder.</span><span class="sxs-lookup"><span data-stu-id="247c1-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="247c1-108">Landspesifikke behovene og implementeringen kan variere på tvers av EU-medlemsland, men de bruker ofte UNC Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskjellige versjoner med tilpasninger i tillegg til [PEPPOL](http://www.peppol.eu) spesifikasjoner og tilgangspunkt for validering og transport.</span><span class="sxs-lookup"><span data-stu-id="247c1-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](http://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="247c1-109">Primære fordelen med UBL er at forretningsdokumenter kan standardisert for ulike formål.</span><span class="sxs-lookup"><span data-stu-id="247c1-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="247c1-110">Siden UBL er en fleksibel, internasjonal standard som støtter mange forretningskrav, kan disse forretningsdokumenter utveksles på tvers av landegrenser.</span><span class="sxs-lookup"><span data-stu-id="247c1-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-finance-and-operations"></a><span data-ttu-id="247c1-111">Hvilke formater for elektroniske fakturaer er tilgjengelige i Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="247c1-111">What electronic invoice formats are currently available in Finance and Operations?</span></span>

<span data-ttu-id="247c1-112">Følgende landspesifikke formater av elektroniske fakturaer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="247c1-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="247c1-113">OIOUBL v.2.02 for Danmark</span><span class="sxs-lookup"><span data-stu-id="247c1-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="247c1-114">EHF v.2.0.8 for Norge</span><span class="sxs-lookup"><span data-stu-id="247c1-114">EHF v.2.0.8 for Norway</span></span>
-   <span data-ttu-id="247c1-115">PEPPOL BIS v.2 for Østerrike, Frankrike og Belgia</span><span class="sxs-lookup"><span data-stu-id="247c1-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="247c1-116">UBL-OHNL 1.9 for Nederland</span><span class="sxs-lookup"><span data-stu-id="247c1-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="247c1-117">FacturaE v.3.2.1 for Spania</span><span class="sxs-lookup"><span data-stu-id="247c1-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="247c1-118">FatturaPA v.1.2 for Italia</span><span class="sxs-lookup"><span data-stu-id="247c1-118">FatturaPA v.1.2 for Italy</span></span>

<span data-ttu-id="247c1-119">Elektronisk fakturering er basert på [elektronisk rapportering](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="247c1-119">Electronic invoicing is based on [electronic reporting](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="247c1-120">Det finnes en **Kundefakturamodell**-datamodell og et tallformat for landsspesifikke konfigurasjoner for elektronisk rapporteringsformat som er opprettet for Østerrike (AT), Danmark (DK), Italia (IT), Norge (NO), Spania (ES), Frankrike (FR), Belgia (BE) og Nederland (NL).</span><span class="sxs-lookup"><span data-stu-id="247c1-120">There is a **Customer invoice model** data model and a number of country-specific electronic reporting format configurations created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), and the Netherlands (NL).</span></span>

-   <span data-ttu-id="247c1-121">OIOUBL salgsfaktura - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="247c1-121">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="247c1-122">OIOUBL salgskreditnota - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="247c1-122">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="247c1-123">OIOUBL prosjektfaktura - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="247c1-123">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="247c1-124">OIOUBL prosjektkreditnota - for AT, DK, og NO</span><span class="sxs-lookup"><span data-stu-id="247c1-124">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="247c1-125">UBL salgsfaktura FR</span><span class="sxs-lookup"><span data-stu-id="247c1-125">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="247c1-126">UBL salgskreditnota FR</span><span class="sxs-lookup"><span data-stu-id="247c1-126">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="247c1-127">UBL prosjektfaktura FR</span><span class="sxs-lookup"><span data-stu-id="247c1-127">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="247c1-128">UBL prosjektkreditnota FR</span><span class="sxs-lookup"><span data-stu-id="247c1-128">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="247c1-129">UBL salgsfaktura BE</span><span class="sxs-lookup"><span data-stu-id="247c1-129">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="247c1-130">UBL salgskreditnota BE</span><span class="sxs-lookup"><span data-stu-id="247c1-130">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="247c1-131">UBL prosjektfaktura BE</span><span class="sxs-lookup"><span data-stu-id="247c1-131">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="247c1-132">UBL prosjektkreditnota BE</span><span class="sxs-lookup"><span data-stu-id="247c1-132">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="247c1-133">UBL salgsfaktura NL</span><span class="sxs-lookup"><span data-stu-id="247c1-133">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="247c1-134">UBL salgskreditnota NL</span><span class="sxs-lookup"><span data-stu-id="247c1-134">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="247c1-135">UBL prosjektfaktura NL</span><span class="sxs-lookup"><span data-stu-id="247c1-135">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="247c1-136">UBL prosjektkreditnota NL</span><span class="sxs-lookup"><span data-stu-id="247c1-136">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="247c1-137">Salgsfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="247c1-137">Sales invoice (ES)</span></span>
-   <span data-ttu-id="247c1-138">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="247c1-138">Sales invoice (IT)</span></span>
-   <span data-ttu-id="247c1-139">Prosjektfaktura (ES)</span><span class="sxs-lookup"><span data-stu-id="247c1-139">Project invoice (ES)</span></span>
-   <span data-ttu-id="247c1-140">Prosjektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="247c1-140">Project invoice (IT)</span></span>

<span data-ttu-id="247c1-141">De elektroniske fakturaene og kreditnotaene du genrerer, inneholder obligatorisk informasjon, for eksempel EAN-nummeret, ordrenummer, kontakt, dimensjonskontokode og adresseopplysninger for kunden.</span><span class="sxs-lookup"><span data-stu-id="247c1-141">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="247c1-142">Valideringsregler brukes når fakturaer genereres, slik at du kan verifisere at riktig informasjon er angitt.</span><span class="sxs-lookup"><span data-stu-id="247c1-142">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="247c1-143">Settet med nødvendig informasjon kan variere fra land til land.</span><span class="sxs-lookup"><span data-stu-id="247c1-143">The set of required information may differ from country to country.</span></span> <span data-ttu-id="247c1-144">Siden både kravene og de støttede landene og formatene kan endres, bør du alltid gå til det delte ativabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) og viser den mest oppdaterte listen over tilgjengelige filer som har aktivatypen **TYSK konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="247c1-144">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="247c1-145">Tilleggsinformasjon</span><span class="sxs-lookup"><span data-stu-id="247c1-145">Additional information</span></span>
<span data-ttu-id="247c1-146">Hvis du vil ha mer informasjon om hvordan du konfigurerer elektroniske fakturaer, kan du spille av følgende [Oppgaveveiledninger](../../fin-and-ops/get-started/help-overview.md#task-guides) i Hjelp-ruten:</span><span class="sxs-lookup"><span data-stu-id="247c1-146">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="247c1-147">Definere elektronisk fakturering for OIOUBL</span><span class="sxs-lookup"><span data-stu-id="247c1-147">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="247c1-148">Importere konfigurasjoner for elektroniske OIOUBL-faktureringer</span><span class="sxs-lookup"><span data-stu-id="247c1-148">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="247c1-149">Definere kundekontoer for elektronisk fakturering med OIOUBL</span><span class="sxs-lookup"><span data-stu-id="247c1-149">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="247c1-150">Selv om disse oppgaveveiledningene ble opprettet for dansk spesifikt format for e-faktura *OIOUBL*, de som kan brukes av andre støttede land med mindre avvik.</span><span class="sxs-lookup"><span data-stu-id="247c1-150">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>


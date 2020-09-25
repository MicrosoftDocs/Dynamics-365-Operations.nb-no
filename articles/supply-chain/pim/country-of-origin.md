---
title: Opprinnelsesland
description: Mange organisasjoner utsteder sertifikater til sine leverandører for å sikre at produkter oppfyller bestemte sertifiseringsstandarder. Disse sertifikatene avhenger ofte av opprinnelseslandet. Dette emnet gir informasjon om funksjonen for opprinnelsesland, der du kan koble et produkt til opprinnelsesland og holde oversikt over produktsertifiseringer.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: d0d93a02817bab8e188818862c1bb7f84b498fc1
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802803"
---
# <a name="country-of-origin"></a><span data-ttu-id="80317-105">Opprinnelsesland</span><span class="sxs-lookup"><span data-stu-id="80317-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="80317-106">Mange organisasjoner utsteder sertifikater til sine leverandører for å sikre at produkter oppfyller bestemte sertifiseringsstandarder.</span><span class="sxs-lookup"><span data-stu-id="80317-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="80317-107">Disse sertifikatene avhenger ofte av opprinnelseslandet.</span><span class="sxs-lookup"><span data-stu-id="80317-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="80317-108">I opprinnelseslandet kan du koble et produkt til opprinnelsesland og holde oversikt over produktsertifiseringer.</span><span class="sxs-lookup"><span data-stu-id="80317-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="80317-109">Aktivere funksjonen for opprinnelsesland</span><span class="sxs-lookup"><span data-stu-id="80317-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="80317-110">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="80317-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="80317-111">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="80317-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="80317-112">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="80317-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="80317-113">**Modul:** *Behandling av produktinformasjon*</span><span class="sxs-lookup"><span data-stu-id="80317-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="80317-114">**Funksjonsnavn:** *Funksjon for administrasjon av opprinnelsesland*</span><span class="sxs-lookup"><span data-stu-id="80317-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="80317-115">Konfigurere kilde- og målland</span><span class="sxs-lookup"><span data-stu-id="80317-115">Configure source and destination countries</span></span>

<span data-ttu-id="80317-116">Før du utsteder et sertifikat for et produkt må du koble produktet til mållandet og opprinnelseslandet.</span><span class="sxs-lookup"><span data-stu-id="80317-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="80317-117">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Opprinnelsesland \> Regler for opprinnelsesland**.</span><span class="sxs-lookup"><span data-stu-id="80317-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="80317-118">Velg et eksisterende landsoppsett for å redigere, eller velg **Ny** i handlingsruten for å opprette et nytt landsoppsett.</span><span class="sxs-lookup"><span data-stu-id="80317-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="80317-119">Angi følgende verdier for det valgte eller nye landet.</span><span class="sxs-lookup"><span data-stu-id="80317-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="80317-120">Felt</span><span class="sxs-lookup"><span data-stu-id="80317-120">Field</span></span> | <span data-ttu-id="80317-121">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="80317-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="80317-122">Varenummer</span><span class="sxs-lookup"><span data-stu-id="80317-122">Item number</span></span> | <span data-ttu-id="80317-123">Velg varenummeret for produktet.</span><span class="sxs-lookup"><span data-stu-id="80317-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="80317-124">Målland</span><span class="sxs-lookup"><span data-stu-id="80317-124">Destination country</span></span> | <span data-ttu-id="80317-125">Velg landet du sender produktet til.</span><span class="sxs-lookup"><span data-stu-id="80317-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="80317-126">Opprinnelsesland</span><span class="sxs-lookup"><span data-stu-id="80317-126">Origin country</span></span> | <span data-ttu-id="80317-127">Velg landet du sender produktet fra.</span><span class="sxs-lookup"><span data-stu-id="80317-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="80317-128">Formålet med dette oppsettet er å hjelpe deg med å generere en stykklisterapport der du kan ta med opprinnelseslandet for hver del som kilde- og mållandene er angitt for.</span><span class="sxs-lookup"><span data-stu-id="80317-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="80317-129">Denne rapporten vil hjelpe deg med å få et helhetlig bilde av stedet der delene kommer fra, og hvor de skal.</span><span class="sxs-lookup"><span data-stu-id="80317-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="80317-130">Holde oversikt over leverandørsertifikater</span><span class="sxs-lookup"><span data-stu-id="80317-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="80317-131">Du kan bruke siden for **Leverandørsertifikater for opprinnelsesland** til å holde oversikt over sertifikater som du utsteder til leverandører.</span><span class="sxs-lookup"><span data-stu-id="80317-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="80317-132">Du må bestemme hvilke sertifikatdokumenter du skal utstede, og hvordan de skal rapportere dem til kunder.</span><span class="sxs-lookup"><span data-stu-id="80317-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="80317-133">Denne funksjonen hjelper deg med å holde orden på sertifikatene.</span><span class="sxs-lookup"><span data-stu-id="80317-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="80317-134">Du kan også velge om de aktuelle sertifikatnumrene skal vises på fakturaer, følgesedler og/eller ordrebekreftelser.</span><span class="sxs-lookup"><span data-stu-id="80317-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="80317-135">Gjør følgende for å konfigurere sertifikatinformasjon.</span><span class="sxs-lookup"><span data-stu-id="80317-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="80317-136">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Opprinnelsesland \> Leverandørsertifikater for opprinnelsesland**.</span><span class="sxs-lookup"><span data-stu-id="80317-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="80317-137">Velg et eksisterende sertifikatoppsett for å redigere, eller velg **Ny** i handlingsruten for å opprette et nytt sertifikatoppsett.</span><span class="sxs-lookup"><span data-stu-id="80317-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="80317-138">Angi følgende innstillinger for det valgte eller nye sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="80317-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="80317-139">Felt</span><span class="sxs-lookup"><span data-stu-id="80317-139">Field</span></span> | <span data-ttu-id="80317-140">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="80317-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="80317-141">Leverandørnummer</span><span class="sxs-lookup"><span data-stu-id="80317-141">Vendor account</span></span> | <span data-ttu-id="80317-142">Velg leverandøren som du utstedte sertifikatet til.</span><span class="sxs-lookup"><span data-stu-id="80317-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="80317-143">Varenummer</span><span class="sxs-lookup"><span data-stu-id="80317-143">Item number</span></span> | <span data-ttu-id="80317-144">Velg varen som du utstedte sertifikatet for.</span><span class="sxs-lookup"><span data-stu-id="80317-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="80317-145">Land/område</span><span class="sxs-lookup"><span data-stu-id="80317-145">Country/region</span></span> | <span data-ttu-id="80317-146">Mållandet eller -området der du må bruke dette sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="80317-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="80317-147">Sertifikatnummer</span><span class="sxs-lookup"><span data-stu-id="80317-147">Certificate number</span></span> | <span data-ttu-id="80317-148">Angi identifikasjonsnummeret for sertifikatet du har utstedt.</span><span class="sxs-lookup"><span data-stu-id="80317-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="80317-149">Gyldighet</span><span class="sxs-lookup"><span data-stu-id="80317-149">Effective</span></span> | <span data-ttu-id="80317-150">Velg den første datoen når det gjeldende sertifikatet er gyldig.</span><span class="sxs-lookup"><span data-stu-id="80317-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="80317-151">Utløp</span><span class="sxs-lookup"><span data-stu-id="80317-151">Expiration</span></span> | <span data-ttu-id="80317-152">Velg den siste datoen når det gjeldende sertifikatet er gyldig.</span><span class="sxs-lookup"><span data-stu-id="80317-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="80317-153">Skriv ut på faktura</span><span class="sxs-lookup"><span data-stu-id="80317-153">Print on invoice</span></span> | <span data-ttu-id="80317-154">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på fakturaer som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="80317-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="80317-155">Skrive ut på følgeseddel</span><span class="sxs-lookup"><span data-stu-id="80317-155">Print on packing slip</span></span> | <span data-ttu-id="80317-156">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på følgesedler som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="80317-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="80317-157">Skriv ut på salgsordre</span><span class="sxs-lookup"><span data-stu-id="80317-157">Print on sales order</span></span> | <span data-ttu-id="80317-158">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på salgsordrer som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="80317-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="80317-159">Ta med opprinnelsesland på stykklisterapporter</span><span class="sxs-lookup"><span data-stu-id="80317-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="80317-160">Når du genererer en stykklisterapport, kan du ta med opprinnelseslandet for hver del du angav kilde- og målland for, på siden **Regler for opprinnelsesland**.</span><span class="sxs-lookup"><span data-stu-id="80317-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="80317-161">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="80317-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="80317-162">Velg eller opprett et produkt for å åpne siden **Detaljer om frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="80317-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="80317-163">I handlingsruten, i kategorien **Utvikling** i **Stykkliste**-gruppen, velger du **Designer**.</span><span class="sxs-lookup"><span data-stu-id="80317-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="80317-164">I handlingsruten velger du **Stykkliste \> Skriv ut** på siden som vises.</span><span class="sxs-lookup"><span data-stu-id="80317-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="80317-165">I dialogboksen **Stykklistelinjer** angir du feltet **Målland** til mållandet du vil vise i rapporten.</span><span class="sxs-lookup"><span data-stu-id="80317-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="80317-166">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80317-166">Select **OK**.</span></span>

<span data-ttu-id="80317-167">En rapport som viser informasjon om opprinnelsesland for hver del, genereres og vises.</span><span class="sxs-lookup"><span data-stu-id="80317-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="80317-168">Her er et eksempel på rapporten.</span><span class="sxs-lookup"><span data-stu-id="80317-168">Here is an example of the report.</span></span>

<span data-ttu-id="80317-169">![Rapport for opprinnelsesland](media/country-of-origin-report.png "Rapport for opprinnelsesland")</span><span class="sxs-lookup"><span data-stu-id="80317-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>

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
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596262"
---
# <a name="country-of-origin"></a><span data-ttu-id="2e7db-105">Opprinnelsesland</span><span class="sxs-lookup"><span data-stu-id="2e7db-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e7db-106">Mange organisasjoner utsteder sertifikater til sine leverandører for å sikre at produkter oppfyller bestemte sertifiseringsstandarder.</span><span class="sxs-lookup"><span data-stu-id="2e7db-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="2e7db-107">Disse sertifikatene avhenger ofte av opprinnelseslandet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="2e7db-108">I opprinnelseslandet kan du koble et produkt til opprinnelsesland og holde oversikt over produktsertifiseringer.</span><span class="sxs-lookup"><span data-stu-id="2e7db-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="2e7db-109">Konfigurere kilde- og målland</span><span class="sxs-lookup"><span data-stu-id="2e7db-109">Configure source and destination countries</span></span>

<span data-ttu-id="2e7db-110">Før du utsteder et sertifikat for et produkt må du koble produktet til mållandet og opprinnelseslandet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="2e7db-111">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Opprinnelsesland \> Regler for opprinnelsesland**.</span><span class="sxs-lookup"><span data-stu-id="2e7db-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="2e7db-112">Velg et eksisterende landsoppsett for å redigere, eller velg **Ny** i handlingsruten for å opprette et nytt landsoppsett.</span><span class="sxs-lookup"><span data-stu-id="2e7db-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="2e7db-113">Angi følgende verdier for det valgte eller nye landet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="2e7db-114">Felt</span><span class="sxs-lookup"><span data-stu-id="2e7db-114">Field</span></span> | <span data-ttu-id="2e7db-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2e7db-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="2e7db-116">Varenummer</span><span class="sxs-lookup"><span data-stu-id="2e7db-116">Item number</span></span> | <span data-ttu-id="2e7db-117">Velg varenummeret for produktet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="2e7db-118">Målland</span><span class="sxs-lookup"><span data-stu-id="2e7db-118">Destination country</span></span> | <span data-ttu-id="2e7db-119">Velg landet du sender produktet til.</span><span class="sxs-lookup"><span data-stu-id="2e7db-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="2e7db-120">Opprinnelsesland</span><span class="sxs-lookup"><span data-stu-id="2e7db-120">Origin country</span></span> | <span data-ttu-id="2e7db-121">Velg landet du sender produktet fra.</span><span class="sxs-lookup"><span data-stu-id="2e7db-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="2e7db-122">Formålet med dette oppsettet er å hjelpe deg med å generere en stykklisterapport der du kan ta med opprinnelseslandet for hver del som kilde- og mållandene er angitt for.</span><span class="sxs-lookup"><span data-stu-id="2e7db-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="2e7db-123">Denne rapporten vil hjelpe deg med å få et helhetlig bilde av stedet der delene kommer fra, og hvor de skal.</span><span class="sxs-lookup"><span data-stu-id="2e7db-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="2e7db-124">Holde oversikt over leverandørsertifikater</span><span class="sxs-lookup"><span data-stu-id="2e7db-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="2e7db-125">Du kan bruke siden for **Leverandørsertifikater for opprinnelsesland** til å holde oversikt over sertifikater som du utsteder til leverandører.</span><span class="sxs-lookup"><span data-stu-id="2e7db-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="2e7db-126">Du må bestemme hvilke sertifikatdokumenter du skal utstede, og hvordan de skal rapportere dem til kunder.</span><span class="sxs-lookup"><span data-stu-id="2e7db-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="2e7db-127">Denne funksjonen hjelper deg med å holde orden på sertifikatene.</span><span class="sxs-lookup"><span data-stu-id="2e7db-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="2e7db-128">Du kan også velge om de aktuelle sertifikatnumrene skal vises på fakturaer, følgesedler og/eller ordrebekreftelser.</span><span class="sxs-lookup"><span data-stu-id="2e7db-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="2e7db-129">Gjør følgende for å konfigurere sertifikatinformasjon.</span><span class="sxs-lookup"><span data-stu-id="2e7db-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="2e7db-130">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Opprinnelsesland \> Leverandørsertifikater for opprinnelsesland**.</span><span class="sxs-lookup"><span data-stu-id="2e7db-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="2e7db-131">Velg et eksisterende sertifikatoppsett for å redigere, eller velg **Ny** i handlingsruten for å opprette et nytt sertifikatoppsett.</span><span class="sxs-lookup"><span data-stu-id="2e7db-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="2e7db-132">Angi følgende innstillinger for det valgte eller nye sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="2e7db-133">Felt</span><span class="sxs-lookup"><span data-stu-id="2e7db-133">Field</span></span> | <span data-ttu-id="2e7db-134">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2e7db-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="2e7db-135">Leverandørnummer</span><span class="sxs-lookup"><span data-stu-id="2e7db-135">Vendor account</span></span> | <span data-ttu-id="2e7db-136">Velg leverandøren som du utstedte sertifikatet til.</span><span class="sxs-lookup"><span data-stu-id="2e7db-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="2e7db-137">Varenummer</span><span class="sxs-lookup"><span data-stu-id="2e7db-137">Item number</span></span> | <span data-ttu-id="2e7db-138">Velg varen som du utstedte sertifikatet for.</span><span class="sxs-lookup"><span data-stu-id="2e7db-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="2e7db-139">Land/område</span><span class="sxs-lookup"><span data-stu-id="2e7db-139">Country/region</span></span> | <span data-ttu-id="2e7db-140">Mållandet eller -området der du må bruke dette sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="2e7db-141">Sertifikatnummer</span><span class="sxs-lookup"><span data-stu-id="2e7db-141">Certificate number</span></span> | <span data-ttu-id="2e7db-142">Angi identifikasjonsnummeret for sertifikatet du har utstedt.</span><span class="sxs-lookup"><span data-stu-id="2e7db-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="2e7db-143">Gyldighet</span><span class="sxs-lookup"><span data-stu-id="2e7db-143">Effective</span></span> | <span data-ttu-id="2e7db-144">Velg den første datoen når det gjeldende sertifikatet er gyldig.</span><span class="sxs-lookup"><span data-stu-id="2e7db-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="2e7db-145">Utløp</span><span class="sxs-lookup"><span data-stu-id="2e7db-145">Expiration</span></span> | <span data-ttu-id="2e7db-146">Velg den siste datoen når det gjeldende sertifikatet er gyldig.</span><span class="sxs-lookup"><span data-stu-id="2e7db-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="2e7db-147">Skriv ut på faktura</span><span class="sxs-lookup"><span data-stu-id="2e7db-147">Print on invoice</span></span> | <span data-ttu-id="2e7db-148">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på fakturaer som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="2e7db-149">Skrive ut på følgeseddel</span><span class="sxs-lookup"><span data-stu-id="2e7db-149">Print on packing slip</span></span> | <span data-ttu-id="2e7db-150">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på følgesedler som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="2e7db-151">Skriv ut på salgsordre</span><span class="sxs-lookup"><span data-stu-id="2e7db-151">Print on sales order</span></span> | <span data-ttu-id="2e7db-152">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på salgsordrer som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="2e7db-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="2e7db-153">Ta med opprinnelsesland på stykklisterapporter</span><span class="sxs-lookup"><span data-stu-id="2e7db-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="2e7db-154">Når du genererer en stykklisterapport, kan du ta med opprinnelseslandet for hver del du angav kilde- og målland for, på siden **Regler for opprinnelsesland**.</span><span class="sxs-lookup"><span data-stu-id="2e7db-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="2e7db-155">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="2e7db-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="2e7db-156">Velg eller opprett et produkt for å åpne siden **Detaljer om frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="2e7db-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="2e7db-157">I handlingsruten, i kategorien **Utvikling** i **Stykkliste**-gruppen, velger du **Designer**.</span><span class="sxs-lookup"><span data-stu-id="2e7db-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="2e7db-158">I handlingsruten velger du **Stykkliste \> Skriv ut** på siden som vises.</span><span class="sxs-lookup"><span data-stu-id="2e7db-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="2e7db-159">I dialogboksen **Stykklistelinjer** angir du feltet **Målland** til mållandet du vil vise i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2e7db-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="2e7db-160">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e7db-160">Select **OK**.</span></span>

<span data-ttu-id="2e7db-161">En rapport som viser informasjon om opprinnelsesland for hver del, genereres og vises.</span><span class="sxs-lookup"><span data-stu-id="2e7db-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="2e7db-162">Her er et eksempel på rapporten.</span><span class="sxs-lookup"><span data-stu-id="2e7db-162">Here is an example of the report.</span></span>

<span data-ttu-id="2e7db-163">![Rapport for opprinnelsesland](media/country-of-origin-report.png "Rapport for opprinnelsesland")</span><span class="sxs-lookup"><span data-stu-id="2e7db-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>

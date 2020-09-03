---
title: Varer med to bruksområder
description: Dette emnet forklarer hvordan du holder rede på produkter som er identifisert som varer med to bruksområder, lagrer sertifikatnumre for hvert relevante produkt og målland og skriver ut gyldige sertifikatnumre på relevante fakturaer, følgesedler og/eller salgsordrer.
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
ms.openlocfilehash: 0847dc1ce01a6e6f4f8b72db115445f75de4aac2
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596261"
---
# <a name="dual-use-goods"></a><span data-ttu-id="2a368-103">Varer med to bruksområder</span><span class="sxs-lookup"><span data-stu-id="2a368-103">Dual-use goods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a368-104">Bruk av varer med to bruksområder er vanligvis varer som har både sivile og militær bruksområder.</span><span class="sxs-lookup"><span data-stu-id="2a368-104">Dual-use goods are typically items that have both civilian and military applications.</span></span> <span data-ttu-id="2a368-105">Et kjemikalie kan for eksempel brukes som gjødsel eller et eksplosiv.</span><span class="sxs-lookup"><span data-stu-id="2a368-105">For example, a chemical might be used as either a fertilizer or an explosive.</span></span> <span data-ttu-id="2a368-106">Mange land har spesielle bestemmelser som gjelder for eksport, import og transport av varer med to bruksområder.</span><span class="sxs-lookup"><span data-stu-id="2a368-106">Many countries have special regulations that apply to the export, import, and transportation of dual-use goods.</span></span> <span data-ttu-id="2a368-107">Derfor er det viktig at firmaer som er involvert i den internasjonale handelen av varer med to bruksområder, holder oversikt over de ulike policyene og sertifikatene.</span><span class="sxs-lookup"><span data-stu-id="2a368-107">Therefore, it's important that companies that are involved in the international trade of dual-use goods keep track of the various policies and certificates.</span></span>

<span data-ttu-id="2a368-108">Funksjonen for to bruksområder hjelper firmaer med å holde rede på produkter som er identifisert som varer med to bruksområder, lagrer sertifikatnumre for hvert relevante produkt og målland og skriver ut gyldige sertifikatnumre på relevante fakturaer, følgesedler og/eller salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="2a368-108">The dual-use feature helps companies keep track of products that are identified as dual-use goods, stores certificate numbers for each relevant product and destination country, and print valid certificate numbers on relevant invoices, packing slips, and/or sales orders.</span></span> <span data-ttu-id="2a368-109">Den bidrar til å sikre at når produktene sendes, inkluderer de alltid oppdaterte sertifiseringer.</span><span class="sxs-lookup"><span data-stu-id="2a368-109">It helps ensure that, when your products are shipped, they always include up-to-date certifications.</span></span>

<span data-ttu-id="2a368-110">Tenk deg følgende scenario:</span><span class="sxs-lookup"><span data-stu-id="2a368-110">Consider the following scenario:</span></span>

1. <span data-ttu-id="2a368-111">Siden for **landoppsett for flerbruk** i systemet angir at forsendelser til Frankrike krever en sertifisering.</span><span class="sxs-lookup"><span data-stu-id="2a368-111">The **Dual use country setup** page in your system indicates that shipments to France require a certification.</span></span>
2. <span data-ttu-id="2a368-112">Siden **Detaljer om frigitt produkt** for produkt X-100 angir at varen har to bruksområder.</span><span class="sxs-lookup"><span data-stu-id="2a368-112">The **Released product details** page for product X-100 indicates that it's a dual-use good.</span></span> <span data-ttu-id="2a368-113">Samlet angir kode, kategori, gruppe og regime eksportkontrollklassifiseringen som produktet tilhører.</span><span class="sxs-lookup"><span data-stu-id="2a368-113">Together, the code, category, group, and regime indicate the export control classification that the product belongs to.</span></span>
3. <span data-ttu-id="2a368-114">Siden for **sertifikater for to bruksområder** inneholder et sertifikat for produkt X-100 når det sendes til Frankrike.</span><span class="sxs-lookup"><span data-stu-id="2a368-114">The **Dual use certificates** page includes a certificate for product X-100 when it's shipped to France.</span></span> <span data-ttu-id="2a368-115">Dette sertifikatet utløper 1. januar 2020.</span><span class="sxs-lookup"><span data-stu-id="2a368-115">This certificate expires January 1, 2020.</span></span>
4. <span data-ttu-id="2a368-116">17. juni 2020 oppretter du en salgsordre for et kundefirma som er basert i Frankrike, og ordren inkluderer produkt X-100.</span><span class="sxs-lookup"><span data-stu-id="2a368-116">On June 17, 2020, you create a sales order for a customer company that is based in France, and the order includes product X-100.</span></span>
5. <span data-ttu-id="2a368-117">Når du lagrer salgsordren, finner systemet følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="2a368-117">When you save the sales order, the system determines the following information:</span></span>

    1. <span data-ttu-id="2a368-118">Tar ordren med varer som har to bruksområder?</span><span class="sxs-lookup"><span data-stu-id="2a368-118">Does the order include any products that are dual-use goods?</span></span>
    2. <span data-ttu-id="2a368-119">Hvis ordren inneholder varer med to bruksområder, må mållandet kreve sertifikater for to bruksområder?</span><span class="sxs-lookup"><span data-stu-id="2a368-119">If the order includes dual-use goods, does the destination country require dual-use certificates?</span></span>
    3. <span data-ttu-id="2a368-120">Hvis landet krever sertifikater for to bruksområder, finnes det et gyldig sertifikat for hver vare for to bruksområder for mållandet?</span><span class="sxs-lookup"><span data-stu-id="2a368-120">If the country requires dual-use certificates, does a valid certificate exist for each dual-use good for the destination country?</span></span>

6. <span data-ttu-id="2a368-121">Ordren inkluderer produkt X-100, produktet sendes til Frankrike, og det finnes et fransk sertifikat for produktet.</span><span class="sxs-lookup"><span data-stu-id="2a368-121">The order includes product X-100, the product is being shipped to France, and a French certificate exists for the product.</span></span> <span data-ttu-id="2a368-122">Sertifikatet er imidlertid utløpt.</span><span class="sxs-lookup"><span data-stu-id="2a368-122">However, the certificate has expired.</span></span> <span data-ttu-id="2a368-123">Du får derfor følgende advarsel: "Sertifikater for to bruksområder for ett eller flere flerbruksvarer i denne salgsordren er ikke gyldig.</span><span class="sxs-lookup"><span data-stu-id="2a368-123">Therefore, you receive the following warning message: "Dual use certificates for one or more dual-use items in this sales order aren't valid.</span></span> <span data-ttu-id="2a368-124">Vil du fortsette med bekreftelsen?"</span><span class="sxs-lookup"><span data-stu-id="2a368-124">Do you want to proceed with the confirmation?"</span></span>

<span data-ttu-id="2a368-125">Dette emnet forklarer hvordan du konfigurerer alle innstillingene som kreves for å konfigurere flerbruksvarer og støtte dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="2a368-125">This topic explains how to configure all the settings that are required to set up dual-use goods and support this scenario.</span></span>

## <a name="define-dual-use-requirements-for-each-relevant-country"></a><span data-ttu-id="2a368-126">Definere flerbrukskrav for hvert aktuelle land</span><span class="sxs-lookup"><span data-stu-id="2a368-126">Define dual-use requirements for each relevant country</span></span>

<span data-ttu-id="2a368-127">Forskjellige land har ulike krav til flerbruksvarer.</span><span class="sxs-lookup"><span data-stu-id="2a368-127">Different countries have different requirements for dual-use goods.</span></span> <span data-ttu-id="2a368-128">Du bruker siden for **landoppsett for flerbruk** for å holde oversikt over landene som krever og ikke krever et sertifikat.</span><span class="sxs-lookup"><span data-stu-id="2a368-128">You use the **Dual use country setup** page to keep track of the countries that do and don't require a certificate.</span></span> <span data-ttu-id="2a368-129">Informasjonen du angir her, kontrolleres når du oppretter salgsordrer, og du vil bli minnet på å gi de nødvendige sertifiseringene.</span><span class="sxs-lookup"><span data-stu-id="2a368-129">The information that you specify here is checked when you create sales orders, and you will be reminded to provide the required certifications.</span></span>

<span data-ttu-id="2a368-130">Følg denne fremgangsmåten for å angi flerbruksinformasjon for ulike land.</span><span class="sxs-lookup"><span data-stu-id="2a368-130">To set up the information about dual-use requirements for different countries, follow these steps.</span></span>

1. <span data-ttu-id="2a368-131">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Flerbruksprodukter \> Landsoppsett for flerbruk**.</span><span class="sxs-lookup"><span data-stu-id="2a368-131">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use country setup**.</span></span>
2. <span data-ttu-id="2a368-132">Velg et eksisterende landsoppsett for å redigere det, eller velg **Ny** i handlingsruten for å opprette et nytt landsoppsett.</span><span class="sxs-lookup"><span data-stu-id="2a368-132">Select an existing country setup to edit it, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="2a368-133">Angi følgende verdier for det valgte eller det nye landsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="2a368-133">Set the following values for the selected or new country setup.</span></span>

    | <span data-ttu-id="2a368-134">Felt</span><span class="sxs-lookup"><span data-stu-id="2a368-134">Field</span></span> | <span data-ttu-id="2a368-135">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2a368-135">Description</span></span> |
    |---|---|
    | <span data-ttu-id="2a368-136">Land/område</span><span class="sxs-lookup"><span data-stu-id="2a368-136">Country/region</span></span> | <span data-ttu-id="2a368-137">Velg landet du vil spore krav for.</span><span class="sxs-lookup"><span data-stu-id="2a368-137">Select the country that you're tracking requirements for.</span></span> |
    | <span data-ttu-id="2a368-138">Sertifikat obligatorisk</span><span class="sxs-lookup"><span data-stu-id="2a368-138">Certificate Required</span></span> | <span data-ttu-id="2a368-139">Merk av i denne avmerkingsboksen for land som krever en sertifisering for flerbruksvarer.</span><span class="sxs-lookup"><span data-stu-id="2a368-139">Select this check box for countries that require a certification for dual-use goods.</span></span> <span data-ttu-id="2a368-140">Fjern merket for land som ikke krever denne sertifiseringen.</span><span class="sxs-lookup"><span data-stu-id="2a368-140">Clear it for countries that don't require this certification.</span></span> |

## <a name="create-dual-use-categories"></a><span data-ttu-id="2a368-141">Opprette kategorier for flerbruk</span><span class="sxs-lookup"><span data-stu-id="2a368-141">Create dual-use categories</span></span>

<span data-ttu-id="2a368-142">Flerbruksvarer må ofte kategoriseres i henhold til ECCN-nummer (eksportkontrollklassifiseringsnummer).</span><span class="sxs-lookup"><span data-stu-id="2a368-142">Dual-use goods must often be categorized according to their export control classification number (ECCN).</span></span> <span data-ttu-id="2a368-143">ECCN er en alfanumerisk kode som kategoriserer varer basert på faktorer som for eksempel artikkel og teknologi.</span><span class="sxs-lookup"><span data-stu-id="2a368-143">The ECCN is an alphanumeric code that categorizes items based on factors such as the commodity and technology.</span></span> <span data-ttu-id="2a368-144">Siden for **kategorier for flerbruk** hjelper deg med å opprette en liste over kategoriene du bruker, for rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="2a368-144">The **Dual use categories** page helps you make a list of the categories that you use, for reporting purposes.</span></span>

<span data-ttu-id="2a368-145">Gjør følgende for å konfigurere kategorier for flerbruk.</span><span class="sxs-lookup"><span data-stu-id="2a368-145">To set up dual-use categories, follow these steps.</span></span>

1. <span data-ttu-id="2a368-146">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Flerbruksprodukter \> Kategorier for flerbruk**.</span><span class="sxs-lookup"><span data-stu-id="2a368-146">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use categories**.</span></span>
2. <span data-ttu-id="2a368-147">Velg en eksisterende kategori for å redigere den, eller velg **Ny** i handlingsruten for å opprette en ny kategori.</span><span class="sxs-lookup"><span data-stu-id="2a368-147">Select an existing category to edit it, or select **New** on the Action Pane to create a new category.</span></span>
3. <span data-ttu-id="2a368-148">Angi følgende verdier for den valgte eller nye kategorien.</span><span class="sxs-lookup"><span data-stu-id="2a368-148">Set the following values for the selected or new category.</span></span>

    | <span data-ttu-id="2a368-149">Felt</span><span class="sxs-lookup"><span data-stu-id="2a368-149">Fields</span></span> | <span data-ttu-id="2a368-150">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2a368-150">Description</span></span> |
    |---|---|
    | <span data-ttu-id="2a368-151">Kode for flerbruk</span><span class="sxs-lookup"><span data-stu-id="2a368-151">Dual use code</span></span> | <span data-ttu-id="2a368-152">Angi den fullstendige ECCN-koden (for eksempel *3A001*).</span><span class="sxs-lookup"><span data-stu-id="2a368-152">Enter the full ECCN code (for example, *3A001*).</span></span>|
    | <span data-ttu-id="2a368-153">Kategori for flerbruk</span><span class="sxs-lookup"><span data-stu-id="2a368-153">Dual use category</span></span> | <span data-ttu-id="2a368-154">Angi CCL-kategoridelen (commerce control list) av ECCN-koden.</span><span class="sxs-lookup"><span data-stu-id="2a368-154">Enter the commerce control list (CCL) category part of the ECCN code.</span></span> <span data-ttu-id="2a368-155">For ECCN-koden *3A001* er denne verdien *3*.</span><span class="sxs-lookup"><span data-stu-id="2a368-155">For example, for the ECCN code *3A001*, this value is *3*.</span></span> |
    | <span data-ttu-id="2a368-156">Gruppe for flerbruk</span><span class="sxs-lookup"><span data-stu-id="2a368-156">Dual use group</span></span> | <span data-ttu-id="2a368-157">Angi produktgruppedelen av ECCN-koden.</span><span class="sxs-lookup"><span data-stu-id="2a368-157">Enter the product group part of the ECCN code.</span></span> <span data-ttu-id="2a368-158">For ECCN-koden *3A001* er denne verdien *A*.</span><span class="sxs-lookup"><span data-stu-id="2a368-158">For example, for the ECCN code *3A001*, this value is *A*.</span></span> |
    | <span data-ttu-id="2a368-159">Ordning for flerbruk</span><span class="sxs-lookup"><span data-stu-id="2a368-159">Dual use regime</span></span> | <span data-ttu-id="2a368-160">Angi koden for ordningen for varen.</span><span class="sxs-lookup"><span data-stu-id="2a368-160">Enter the regime code for the item.</span></span> <span data-ttu-id="2a368-161">Denne koden identifiserer årsaken til at varen er klassifisert som flerbruksvare.</span><span class="sxs-lookup"><span data-stu-id="2a368-161">This code identifies the reason why the item is classified as a dual-use good.</span></span> <span data-ttu-id="2a368-162">For ECCN-koden *3A001* er denne verdien *001*.</span><span class="sxs-lookup"><span data-stu-id="2a368-162">For example, for the ECCN code *3A001*, this value is *001*.</span></span> |

## <a name="apply-dual-use-categories-to-products"></a><span data-ttu-id="2a368-163">Bruke flerbrukskategorier for produkter</span><span class="sxs-lookup"><span data-stu-id="2a368-163">Apply dual-use categories to products</span></span>

<span data-ttu-id="2a368-164">Følg denne fremgangsmåten for å identifisere et produkt som en flerbruksvare og bruke en flerbrukskategori på den.</span><span class="sxs-lookup"><span data-stu-id="2a368-164">To identify a product as a dual-use good and apply a dual-use category to it, follow these steps.</span></span>

1. <span data-ttu-id="2a368-165">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="2a368-165">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="2a368-166">Velg eller opprett et produkt for å åpne siden **Detaljer om frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="2a368-166">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="2a368-167">På hurtigfanen **Utenrikshandel** angir du alternativet for **Flerbruksprodukter** til **Ja** for å identifisere det gjeldende produktet som en flerbruksvare.</span><span class="sxs-lookup"><span data-stu-id="2a368-167">On the **Foreign trade** FastTab, set the **Dual use products** option to **Yes** to identify the current product as a dual-use good.</span></span>
1. <span data-ttu-id="2a368-168">Sett feltet **Kode for flerbruk** til koden som gjelder for det gjeldende produktet.</span><span class="sxs-lookup"><span data-stu-id="2a368-168">Set the **Dual use code** field to the code that applies to the current product.</span></span> <span data-ttu-id="2a368-169">(Du definerte denne koden på siden for **Kategorier for flerbruk**.)</span><span class="sxs-lookup"><span data-stu-id="2a368-169">(You defined this code on the **Dual use categories** page.)</span></span>

<span data-ttu-id="2a368-170">Dette oppsettet kontrolleres når du oppretter en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="2a368-170">This setup is checked when you create a sales order.</span></span>

## <a name="set-up-dual-use-certificates"></a><span data-ttu-id="2a368-171">Angi sertifikater for flerbruk</span><span class="sxs-lookup"><span data-stu-id="2a368-171">Set up dual-use certificates</span></span>

<span data-ttu-id="2a368-172">Du bruker siden for **Sertifikater for flerbruk** til å definere og behandle de nødvendige sertifikatene for flerbruk for hvert produkt og hvert land.</span><span class="sxs-lookup"><span data-stu-id="2a368-172">You use the **Dual use certificates** page to set up and manage the required dual-use certificates for each product and country.</span></span> <span data-ttu-id="2a368-173">Du kan spore detaljene for hvert sertifikat, for eksempel landet og datoene for gyldighet.</span><span class="sxs-lookup"><span data-stu-id="2a368-173">You can track each certificate's details, such as the country and the dates of validity.</span></span> <span data-ttu-id="2a368-174">Du kan også angi alternativer for å angi hvor denne informasjonen skal skrives ut.</span><span class="sxs-lookup"><span data-stu-id="2a368-174">You can also set options to specify where this information should be printed.</span></span> <span data-ttu-id="2a368-175">Informasjonen kan for eksempel skrives ut på fakturaen, følgeseddelen og/eller salgsordren.</span><span class="sxs-lookup"><span data-stu-id="2a368-175">For example, the information can be printed on the invoice, packing slip, and/or sales order.</span></span> <span data-ttu-id="2a368-176">Dette oppsettet kontrolleres når du oppretter en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="2a368-176">This setup is checked when you create a sales order.</span></span>

1. <span data-ttu-id="2a368-177">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Flerbruksprodukter \> Sertifikater for flerbruk**.</span><span class="sxs-lookup"><span data-stu-id="2a368-177">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use certificates**.</span></span>
2. <span data-ttu-id="2a368-178">Velg et eksisterende sertifikat for å redigere det, eller velg **Ny** i handlingsruten for å opprette et nytt sertifikat.</span><span class="sxs-lookup"><span data-stu-id="2a368-178">Select an existing certificate to edit it, or select **New** on the Action Pane to create a new certificate.</span></span>
3. <span data-ttu-id="2a368-179">Angi følgende verdier for det valgte eller nye sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="2a368-179">Set the following values for the selected or new certificate.</span></span>

    | <span data-ttu-id="2a368-180">Felt</span><span class="sxs-lookup"><span data-stu-id="2a368-180">Field</span></span> | <span data-ttu-id="2a368-181">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2a368-181">Description</span></span> |
    |---|---|
    | <span data-ttu-id="2a368-182">Varenummer</span><span class="sxs-lookup"><span data-stu-id="2a368-182">Item number</span></span> | <span data-ttu-id="2a368-183">Velg varenummeret til flerbruksvaren som dette sertifikatet skal brukes på.</span><span class="sxs-lookup"><span data-stu-id="2a368-183">Select the item number of the dual-use good that this certificate applies to.</span></span> |
    | <span data-ttu-id="2a368-184">Land/område</span><span class="sxs-lookup"><span data-stu-id="2a368-184">Country/region</span></span> | <span data-ttu-id="2a368-185">Mållandet eller -området der du må bruke dette sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="2a368-185">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="2a368-186">Sertifikatnummer</span><span class="sxs-lookup"><span data-stu-id="2a368-186">Certificate number</span></span> | <span data-ttu-id="2a368-187">Nummeret som vises på sertifikatet som er utstedt til leverandøren eller kunden.</span><span class="sxs-lookup"><span data-stu-id="2a368-187">The number that appears on the certificate that is issued to the vendor or customer.</span></span> |
    | <span data-ttu-id="2a368-188">Gyldighet</span><span class="sxs-lookup"><span data-stu-id="2a368-188">Effective</span></span> | <span data-ttu-id="2a368-189">Velg den første datoen når det gjeldende sertifikatet er gyldig.</span><span class="sxs-lookup"><span data-stu-id="2a368-189">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="2a368-190">Utløp</span><span class="sxs-lookup"><span data-stu-id="2a368-190">Expiration</span></span> | <span data-ttu-id="2a368-191">Velg den siste datoen når det gjeldende sertifikatet er gyldig.</span><span class="sxs-lookup"><span data-stu-id="2a368-191">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="2a368-192">Skriv ut på faktura</span><span class="sxs-lookup"><span data-stu-id="2a368-192">Print on invoice</span></span> | <span data-ttu-id="2a368-193">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på fakturaer som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="2a368-193">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="2a368-194">Skrive ut på følgeseddel</span><span class="sxs-lookup"><span data-stu-id="2a368-194">Print on packing slip</span></span> | <span data-ttu-id="2a368-195">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på følgesedler som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="2a368-195">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="2a368-196">Skriv ut på salgsordre</span><span class="sxs-lookup"><span data-stu-id="2a368-196">Print on sales order</span></span> | <span data-ttu-id="2a368-197">Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på salgsordrer som er adressert til det angitte landet i det angitte datoområdet.</span><span class="sxs-lookup"><span data-stu-id="2a368-197">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |
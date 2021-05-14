---
title: Opprette forhåndsdefinerte produktvarianter
description: Denne fremgangsmåten veileder deg gjennom oppretting av produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner.
author: t-benebo
manager: tfehr
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acd2e3f1464dfed09ee24764270b06970b747d7c
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938208"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="c70cd-103">Forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="c70cd-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="c70cd-104">Eksempelscenario: Opprette forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="c70cd-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="c70cd-105">Dette eksempelscenarioet viser hvordan du oppretter produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="c70cd-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="c70cd-106">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="c70cd-106">Make demo data available</span></span>

<span data-ttu-id="c70cd-107">For å følge dette scenarioet ved å bruke verdiene som er foreslått her, må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten *USMF*.</span><span class="sxs-lookup"><span data-stu-id="c70cd-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="c70cd-108">Trinn 1: Opprette en produktstandard</span><span class="sxs-lookup"><span data-stu-id="c70cd-108">Step 1: Create a product master</span></span>

<span data-ttu-id="c70cd-109">Slik opprettes en produktstandard:</span><span class="sxs-lookup"><span data-stu-id="c70cd-109">To create a product master:</span></span>

1. <span data-ttu-id="c70cd-110">Gå til **Behandling av produktinformasjon > Produkter > Produktstandarder**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="c70cd-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-111">Select **New**.</span></span>
1. <span data-ttu-id="c70cd-112">Hvis **Produktnummer**-feltet ikke allerede viser et tall, angir du en verdi.</span><span class="sxs-lookup"><span data-stu-id="c70cd-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="c70cd-113">Dette er bare nødvendig hvis ingen nummerserie er definert for dette feltet.</span><span class="sxs-lookup"><span data-stu-id="c70cd-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="c70cd-114">Angi et navn i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="c70cd-115">I feltet **Produktdimensjonsgruppe** velger du produktdimensjonsgruppen *SizeCol* (Størrelse og farge).</span><span class="sxs-lookup"><span data-stu-id="c70cd-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="c70cd-116">Velg **OK** for å opprette og åpne den nye produktstandard.</span><span class="sxs-lookup"><span data-stu-id="c70cd-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="c70cd-117">Trinn 2: Legge til produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="c70cd-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="c70cd-118">Dette eksemplet viser hvordan du manuelt angir produktdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="c70cd-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="c70cd-119">Du kan også velge en størrelse, farge eller stilgruppe som inkluderer produktdimensjonsverdiene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="c70cd-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="c70cd-120">Slik legger du til produktdimensjoner:</span><span class="sxs-lookup"><span data-stu-id="c70cd-120">To add product dimensions:</span></span>

1. <span data-ttu-id="c70cd-121">Når den nye produktstandarden fremdeles er åpen, velger du **Produktdimensjoner** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c70cd-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="c70cd-122">Åpne kategorien **Størrelse**, og velg **Ny** på verktøylinjen for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="c70cd-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="c70cd-123">Gjør følgende innstillinger for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="c70cd-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="c70cd-124">**Størrelse:** Velg en størrelsesverdi.</span><span class="sxs-lookup"><span data-stu-id="c70cd-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="c70cd-125">**Navn:** Angi et navn for størrelsen.</span><span class="sxs-lookup"><span data-stu-id="c70cd-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="c70cd-126">Velg **Ny** på verktøylinjen, og legg til en ny størrelse i rutenettet med ny **Størrelse** og nytt **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="c70cd-127">Åpne kategorien **Farger**, og velg **Ny** på verktøylinjen for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="c70cd-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="c70cd-128">Gjør følgende innstillinger for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="c70cd-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="c70cd-129">**Farge:** Velg en fargeverdi.</span><span class="sxs-lookup"><span data-stu-id="c70cd-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="c70cd-130">**Navn:** Angi et navn for fargen.</span><span class="sxs-lookup"><span data-stu-id="c70cd-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="c70cd-131">Velg **Ny** på verktøylinjen, og legg til en ny farge i rutenettet med ny **Farge** og nytt **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="c70cd-132">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-132">Select **Save**.</span></span>
1. <span data-ttu-id="c70cd-133">Lukk siden for å gå tilbake til den nye produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="c70cd-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="c70cd-134">Trinn 3: Generere produktvarianter</span><span class="sxs-lookup"><span data-stu-id="c70cd-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="c70cd-135">Denne delen beskriver hvordan du genererer produktvarianter når funksjonen *Forbedringer for variantforslagssiden* ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="c70cd-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="c70cd-136">I neste del finner du informasjon om hvordan du genererer produktvarianter når denne funksjonen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="c70cd-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="c70cd-137">Slik genererer du produktvarianter:</span><span class="sxs-lookup"><span data-stu-id="c70cd-137">To generate product variants:</span></span>

1. <span data-ttu-id="c70cd-138">Når den nye produktstandarden fremdeles er åpen, velger du **Produktvarianter** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c70cd-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="c70cd-139">Velg **Variantforslag** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c70cd-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="c70cd-140">Systemet genererer en liste med alle mulige kombinasjoner av størrelsene og fargene du definerte for produktet.</span><span class="sxs-lookup"><span data-stu-id="c70cd-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="c70cd-141">Velg **Velg alle** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="c70cd-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="c70cd-142">I dette eksemplet velger du alle mulige varianter.</span><span class="sxs-lookup"><span data-stu-id="c70cd-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="c70cd-143">Hvis du bare vil bruke et delsett av de mulige produktdimensjonskombinasjonene, merker du bare av i de obligatoriske avmerkingsboksene etter behov.</span><span class="sxs-lookup"><span data-stu-id="c70cd-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="c70cd-144">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-144">Select **Create**.</span></span>
1. <span data-ttu-id="c70cd-145">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="c70cd-146">Forbedrede variantforslag</span><span class="sxs-lookup"><span data-stu-id="c70cd-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="c70cd-147">Funksjonen *Forbedringer for variantforslagssiden* forbedrer **Variantforslag** for å adressere ytelses- og brukervennlighetsproblemer for firmaer som har et høyt antall produktdimensjonskombinasjoner.</span><span class="sxs-lookup"><span data-stu-id="c70cd-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="c70cd-148">Den utvidede prosessen for valg av produktdimensjonsverdier som du kan generere variantforslag for, gjør det raskere og enklere å identifisere og frigi det relevante settet med produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="c70cd-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="c70cd-149">Følgende forbedringer er lagt til av denne funksjonen:</span><span class="sxs-lookup"><span data-stu-id="c70cd-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="c70cd-150">**Utsatt generering av variantforslag:** **Variantforslag**-siden viser ikke lenger forslag når du åpner den første gang.</span><span class="sxs-lookup"><span data-stu-id="c70cd-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="c70cd-151">I stedet må du uttrykkelig velge hvilke verdier du trenger, og deretter velge **Foreslå**-knappen for å generere kombinasjonene.</span><span class="sxs-lookup"><span data-stu-id="c70cd-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="c70cd-152">Dette gjør prosessen mer synlig og interaktiv.</span><span class="sxs-lookup"><span data-stu-id="c70cd-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="c70cd-153">**Valg av dimensjonsverdier:** Når du har mange dimensjonsverdier, er du vanligvis interessert i å generere variantforslag som bare omfatter noen få av dem (for eksempel når du introduserer et nytt sett med farger eller stiler).</span><span class="sxs-lookup"><span data-stu-id="c70cd-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="c70cd-154">Med den forbedrede utformingen kan du velge dimensjonsverdiene du vil generere produktvariantforslag for.</span><span class="sxs-lookup"><span data-stu-id="c70cd-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="c70cd-155">Dette øker relevansen av de foreslåtte variantene betydelig og forbedrer både systemets ytelse og brukerproduktivitet.</span><span class="sxs-lookup"><span data-stu-id="c70cd-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="c70cd-156">Aktivere funksjonen Forbedringer for variantforslagssiden</span><span class="sxs-lookup"><span data-stu-id="c70cd-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="c70cd-157">Før du kan bruke funksjonen *Forbedringer for variantforslagssiden* må den aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="c70cd-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="c70cd-158">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="c70cd-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c70cd-159">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="c70cd-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c70cd-160">**Modul:** *Behandling av produktinformasjon*</span><span class="sxs-lookup"><span data-stu-id="c70cd-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="c70cd-161">**Funksjonsnavn:** *Forbedringer for variantforslagssiden*</span><span class="sxs-lookup"><span data-stu-id="c70cd-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="c70cd-162">Arbeide med de forbedrede variantforslagene</span><span class="sxs-lookup"><span data-stu-id="c70cd-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="c70cd-163">For å generere produktvariantforslag når funksjonen *Forbedringer for variantforslagssiden* er aktivert:</span><span class="sxs-lookup"><span data-stu-id="c70cd-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="c70cd-164">Åpne eller opprett en produktstandard, og legg til de nødvendige produktdimensjonene, som beskrevet i forrige del.</span><span class="sxs-lookup"><span data-stu-id="c70cd-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="c70cd-165">Når den produktstandarden er åpen, velger du **Produktvarianter** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c70cd-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="c70cd-166">Velg **Variantforslag** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c70cd-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="c70cd-167">Velg verdiene du vil bruke for hver av dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="c70cd-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="c70cd-168">På verktøylinjen velger du **Foreslå**.</span><span class="sxs-lookup"><span data-stu-id="c70cd-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="c70cd-169">Systemet genererer en liste med alle mulige kombinasjoner av størrelsene og fargene du valgte.</span><span class="sxs-lookup"><span data-stu-id="c70cd-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="c70cd-170">I hurtigkategorien **Foreslåtte varianter** merker du av for hver produktdimensjonskombinasjon du vil bruke, eller velger **Velg alle** på verktøylinjen for å velge alle.</span><span class="sxs-lookup"><span data-stu-id="c70cd-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="c70cd-171">Velg **Opprett** for å legge til variantene i gjeldende produktstandard.</span><span class="sxs-lookup"><span data-stu-id="c70cd-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

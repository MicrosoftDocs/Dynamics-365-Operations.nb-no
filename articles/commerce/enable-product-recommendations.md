---
title: Aktiver produktanbefalinger
description: Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcb3b542d290e01a3cddc73ae163ed2ef420771b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238803"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="181d3-103">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="181d3-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="181d3-104">Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="181d3-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="181d3-105">Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="181d3-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="181d3-106">Anbefalinger, forhåndssjekk</span><span class="sxs-lookup"><span data-stu-id="181d3-106">Recommendations pre-check</span></span>

<span data-ttu-id="181d3-107">Før du aktiverer, må du være oppmerksom på at produktanbefalinger bare støttes for Commerce-kunder som har migrert lagringen til å bruke Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="181d3-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="181d3-108">Følgende konfigurasjoner må aktiveres i Back Office før aktivering av anbefalinger:</span><span class="sxs-lookup"><span data-stu-id="181d3-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="181d3-109">Kontroller at Azure Data Lake Storage er kjøpt og korrekt verifisert i miljøet.</span><span class="sxs-lookup"><span data-stu-id="181d3-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="181d3-110">For mer informasjon, se [Kontroller at Azure Data Lake Storage er kjøpt og korrekt verifisert i miljøet](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="181d3-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="181d3-111">Kontroller at oppdateringen av enhetslageret er automatisert.</span><span class="sxs-lookup"><span data-stu-id="181d3-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="181d3-112">For mer informasjon, se [Kontroller at oppdateringen av enhetslageret er automatisert](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="181d3-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="181d3-113">Kontroller at Azure AD-identitetskonfigurasjonen inneholder en oppføring for anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="181d3-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="181d3-114">Du finner mer informasjon om hvordan du utfører denne handlingen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="181d3-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="181d3-115">Kontroller også at RetailSale-mål er aktivert.</span><span class="sxs-lookup"><span data-stu-id="181d3-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="181d3-116">Hvis du vil lære mer om denne konfigureringsprosessen, kan du se [Arbeide med mål](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="181d3-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="181d3-117">Azure AD-identitetskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="181d3-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="181d3-118">Dette trinnet er nødvendig for alle kunder som kjører en IaaS-konfigurasjon (infrastruktur som tjeneste).</span><span class="sxs-lookup"><span data-stu-id="181d3-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="181d3-119">For kunder som kjører på Service Fabric (SF), bør dette trinnet være automatisk, og vi anbefaler at du kontrollerer at innstillingen er konfigurert som forventet.</span><span class="sxs-lookup"><span data-stu-id="181d3-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="181d3-120">Installasjon</span><span class="sxs-lookup"><span data-stu-id="181d3-120">Setup</span></span>

1. <span data-ttu-id="181d3-121">Fra Back Office, søk etter siden **Azure Active Directory-apper**.</span><span class="sxs-lookup"><span data-stu-id="181d3-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="181d3-122">Kontroller om det finnes en oppføring for "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="181d3-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="181d3-123">Hvis oppføringen ikke finnes, legger du til en ny oppføring med følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="181d3-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="181d3-124">**Klient-ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="181d3-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="181d3-125">**Navn** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="181d3-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="181d3-126">**Bruker-ID** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="181d3-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="181d3-127">Lagre og lukk siden.</span><span class="sxs-lookup"><span data-stu-id="181d3-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="181d3-128">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="181d3-128">Turn on recommendations</span></span>

<span data-ttu-id="181d3-129">Gjør følgende for å aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="181d3-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="181d3-130">I Commerce Headquarters søker du etter **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="181d3-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="181d3-131">Velg **Alle** for å vise en liste over tilgjengelige funksjoner.</span><span class="sxs-lookup"><span data-stu-id="181d3-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="181d3-132">Skriv inn **Anbefalinger** i søkeboksen.</span><span class="sxs-lookup"><span data-stu-id="181d3-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="181d3-133">Velg funksjonen **Produktanbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="181d3-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="181d3-134">I egenskapsruten **Produktanbefalinger** velger du **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="181d3-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Aktivere anbefalinger](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="181d3-136">Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="181d3-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="181d3-137">Det kan ta flere timer kan være nødvendig før listene er tilgjengelige og kan vises ved salgsstedet (POS) eller i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="181d3-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="181d3-138">Konfigurere parametere for anbefalingsliste</span><span class="sxs-lookup"><span data-stu-id="181d3-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="181d3-139">Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier.</span><span class="sxs-lookup"><span data-stu-id="181d3-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="181d3-140">Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten.</span><span class="sxs-lookup"><span data-stu-id="181d3-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="181d3-141">Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="181d3-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="181d3-142">Vis anbefalinger på salgsstedsenheter</span><span class="sxs-lookup"><span data-stu-id="181d3-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="181d3-143">Når du har aktivert anbefalinger i Handel-administrasjonskontoret, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen ved hjelp av oppsettverktøyet.</span><span class="sxs-lookup"><span data-stu-id="181d3-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="181d3-144">Hvis du vil lære om denne prosessen, kan du se [Legge til en anbefalingskontroll på transaksjonsskjermbildet på salgsstedsenheter](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="181d3-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="181d3-145">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="181d3-145">Enable personalized recommendations</span></span>

<span data-ttu-id="181d3-146">I Dynamics 365 Commerce kan forhandlere få tilpassede produktanbefalinger (også kjent som personalisering).</span><span class="sxs-lookup"><span data-stu-id="181d3-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="181d3-147">På denne måten kan tilpassede anbefalinger bygges inn i kundeopplevelsen på nettet og ved salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="181d3-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="181d3-148">Når funksjonaliteten for personalisering er aktivert, kan systemet tilknytte en brukers innkjøps- og produktinformasjon, slik at de genererer indivduelle produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="181d3-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="181d3-149">Hvis du vil finne ut mer om tilpassede anbefalinger, kan du se [Aktivere tilpassede anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="181d3-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="181d3-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="181d3-150">Additional resources</span></span>

[<span data-ttu-id="181d3-151">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="181d3-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="181d3-152">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="181d3-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="181d3-153">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="181d3-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="181d3-154">Aktivere Kjøp lignende utseender-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="181d3-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="181d3-155">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="181d3-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="181d3-156">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="181d3-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="181d3-157">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="181d3-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="181d3-158">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="181d3-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="181d3-159">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="181d3-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="181d3-160">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="181d3-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="181d3-161">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="181d3-161">Product recommendations FAQ</span></span>](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
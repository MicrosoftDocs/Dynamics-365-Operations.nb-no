---
title: Aktiver produktanbefalinger
description: Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 694e5a451b8e25f3729364dfaed0adc7d242f2fe
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404215"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="24579-103">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="24579-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24579-104">Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="24579-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="24579-105">Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="24579-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="24579-106">Anbefalinger, forhåndssjekk</span><span class="sxs-lookup"><span data-stu-id="24579-106">Recommendations pre-check</span></span>

<span data-ttu-id="24579-107">Før du aktiverer, må du være oppmerksom på at produktanbefalinger bare støttes for Commerce-kunder som har migrert lagringen til å bruke Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="24579-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="24579-108">Følgende konfigurasjoner må aktiveres i Back Office før aktivering av anbefalinger:</span><span class="sxs-lookup"><span data-stu-id="24579-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="24579-109">Kontroller at Azure Data Lake Storage er kjøpt og korrekt verifisert i miljøet.</span><span class="sxs-lookup"><span data-stu-id="24579-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="24579-110">For mer informasjon, se [Kontroller at Azure Data Lake Storage er kjøpt og korrekt verifisert i miljøet](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="24579-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="24579-111">Kontroller at oppdateringen av enhetslageret er automatisert.</span><span class="sxs-lookup"><span data-stu-id="24579-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="24579-112">For mer informasjon, se [Kontroller at oppdateringen av enhetslageret er automatisert](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="24579-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="24579-113">Kontroller at Azure AD-identitetskonfigurasjonen inneholder en oppføring for anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="24579-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="24579-114">Du finner mer informasjon om hvordan du utfører denne handlingen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="24579-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="24579-115">Kontroller også at RetailSale-mål er aktivert.</span><span class="sxs-lookup"><span data-stu-id="24579-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="24579-116">Hvis du vil lære mer om denne konfigureringsprosessen, kan du se [Arbeide med mål](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="24579-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="24579-117">Azure AD-identitetskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="24579-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="24579-118">Dette trinnet er nødvendig for alle kunder som kjører en IaaS-konfigurasjon (infrastruktur som tjeneste).</span><span class="sxs-lookup"><span data-stu-id="24579-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="24579-119">For kunder som kjører på Service Fabric (SF), bør dette trinnet være automatisk, og vi anbefaler at du kontrollerer at innstillingen er konfigurert som forventet.</span><span class="sxs-lookup"><span data-stu-id="24579-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="24579-120">Installasjon</span><span class="sxs-lookup"><span data-stu-id="24579-120">Setup</span></span>

1. <span data-ttu-id="24579-121">Fra Back Office, søk etter siden **Azure Active Directory-apper**.</span><span class="sxs-lookup"><span data-stu-id="24579-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="24579-122">Kontroller om det finnes en oppføring for "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="24579-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="24579-123">Hvis oppføringen ikke finnes, legger du til en ny oppføring med følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="24579-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="24579-124">**Klient-ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="24579-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="24579-125">**Navn** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="24579-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="24579-126">**Bruker-ID** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="24579-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="24579-127">Lagre og lukk siden.</span><span class="sxs-lookup"><span data-stu-id="24579-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="24579-128">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="24579-128">Turn on recommendations</span></span>

<span data-ttu-id="24579-129">Gjør følgende for å aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="24579-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="24579-130">Gå til **Detaljhandel og handel &gt; Produktanbefalinger &gt; Anbefalingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="24579-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="24579-131">Velg **Anbefalingslister** i listen over delte parametere.</span><span class="sxs-lookup"><span data-stu-id="24579-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="24579-132">Sett alternativet **Aktiver anbefalinger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="24579-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![Aktivere anbefalinger](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="24579-134">Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="24579-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="24579-135">Det kan ta flere timer kan være nødvendig før listene er tilgjengelige og kan vises ved salgsstedet (POS) eller i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="24579-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="24579-136">Konfigurere parametere for anbefalingsliste</span><span class="sxs-lookup"><span data-stu-id="24579-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="24579-137">Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier.</span><span class="sxs-lookup"><span data-stu-id="24579-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="24579-138">Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten.</span><span class="sxs-lookup"><span data-stu-id="24579-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="24579-139">Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="24579-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="24579-140">Vis anbefalinger på salgsstedsenheter</span><span class="sxs-lookup"><span data-stu-id="24579-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="24579-141">Når du har aktivert anbefalinger i Handel-administrasjonskontoret, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen ved hjelp av oppsettverktøyet.</span><span class="sxs-lookup"><span data-stu-id="24579-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="24579-142">Hvis du vil lære om denne prosessen, kan du se [Legge til en anbefalingskontroll på transaksjonsskjermbildet på salgsstedsenheter](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="24579-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="24579-143">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="24579-143">Enable personalized recommendations</span></span>

<span data-ttu-id="24579-144">I Dynamics 365 Commerce kan forhandlere få tilpassede produktanbefalinger (også kjent som personalisering).</span><span class="sxs-lookup"><span data-stu-id="24579-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="24579-145">På denne måten kan tilpassede anbefalinger bygges inn i kundeopplevelsen på nettet og ved salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="24579-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="24579-146">Når funksjonaliteten for personalisering er aktivert, kan systemet tilknytte en brukers innkjøps- og produktinformasjon, slik at de genererer indivduelle produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="24579-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="24579-147">Hvis du vil finne ut mer om tilpassede anbefalinger, kan du se [Aktivere tilpassede anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="24579-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24579-148">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="24579-148">Additional resources</span></span>

[<span data-ttu-id="24579-149">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="24579-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="24579-150">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="24579-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="24579-151">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="24579-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="24579-152">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="24579-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="24579-153">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="24579-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="24579-154">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="24579-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="24579-155">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="24579-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="24579-156">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="24579-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="24579-157">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="24579-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="24579-158">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="24579-158">Product recommendations FAQ</span></span>](faq-recommendations.md)


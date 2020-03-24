---
title: Opprette anbefalinger med demonstrasjonsdata
description: Dette dokument gir råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2e790d78b4d5216822ffda3a3895feb674876bd8
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127842"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="23038-103">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="23038-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="23038-104">Dette dokument gir råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="23038-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="23038-105">Produktanbefalinger for omnikanal gir et sett med kuraterte eller programmatisk genererte produktlister.</span><span class="sxs-lookup"><span data-stu-id="23038-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="23038-106">Disse listene kan brukes i flere scenarier, avhengig av forretningsbehovet.</span><span class="sxs-lookup"><span data-stu-id="23038-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="23038-107">Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="23038-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="23038-108">Produktanbefalinger for Lag 2-miljøer og høyere Dynamics 365-miljøer beregnes automatisk basert på kundedata.</span><span class="sxs-lookup"><span data-stu-id="23038-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="23038-109">Bruk av demonstrasjonsdata for produktanbefalinger deaktiverer ikke produktanbefalingerløsninger som allerede er klargjort i miljøet og kostnadene som er knyttet til bruken.</span><span class="sxs-lookup"><span data-stu-id="23038-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="23038-110">Produktanbefalinger for Lag 1-miljøer er bare basert på statiske demonstrasjonsdata som er lagret i en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="23038-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="23038-111">Aktivere demonstrasjonsdata for produktanbefalinger i et miljø</span><span class="sxs-lookup"><span data-stu-id="23038-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="23038-112">For å aktivere demonstrasjonsdata for produktanbefalinger må du distribuere Dynamics 365 Commerce-forhåndsvisningens demonstrasjonsutvidelse til det aktuelle miljøet.</span><span class="sxs-lookup"><span data-stu-id="23038-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="23038-113">Når du gjør dette, aktiveres demonstrasjonsdata for produktanbefalinger automatisk.</span><span class="sxs-lookup"><span data-stu-id="23038-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="23038-114">Standard demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="23038-114">Default demo data</span></span>
<span data-ttu-id="23038-115">Alle miljøer i én boks leveres med forhåndslastede demonstrasjonsdata for produktanbefalinger som er lagret i den kommadelte filen reco_demo_data.csv, som er plassert på Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="23038-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="23038-116">Dataene er strukturert langs følgende kolonner.</span><span class="sxs-lookup"><span data-stu-id="23038-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="23038-117">Kolonnenavn</span><span class="sxs-lookup"><span data-stu-id="23038-117">Column name</span></span>         | <span data-ttu-id="23038-118">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="23038-118">Mandatory</span></span>          | <span data-ttu-id="23038-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="23038-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="23038-120">Mulige verdier</span><span class="sxs-lookup"><span data-stu-id="23038-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="23038-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="23038-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="23038-123">Den spesifikke listetypen for produktanbefaling som demonstrasjonsdatapunktet skal generere.</span><span class="sxs-lookup"><span data-stu-id="23038-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="23038-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="23038-124">RecoBestSelling</span></span></li><li><span data-ttu-id="23038-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="23038-125">RecoNew</span></span></li><li><span data-ttu-id="23038-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="23038-126">RecoTrending</span></span></li><li><span data-ttu-id="23038-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="23038-127">RecoCart</span></span></li><li><span data-ttu-id="23038-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="23038-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="23038-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="23038-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="23038-131">Det spesifikke driftsenhetsnummeret der produktanbefalinger forventes å vises.</span><span class="sxs-lookup"><span data-stu-id="23038-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="23038-132">Kategori</span><span class="sxs-lookup"><span data-stu-id="23038-132">Category</span></span>            |                    |    <span data-ttu-id="23038-133">Kategorien som den bestemte listen skal returneres for.</span><span class="sxs-lookup"><span data-stu-id="23038-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="23038-134">Hvis det ikke er angitt en kategori, er listen bare for øverste navigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="23038-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="23038-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="23038-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="23038-136">For lister som krever utgangsverdi (RecoPeopleAlsoBuy og RecoCart) må produktlistene vise flere produkter.</span><span class="sxs-lookup"><span data-stu-id="23038-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="23038-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="23038-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="23038-139">Ett eller flere produkter som skal returneres som resultat, atskilt med ';'.</span><span class="sxs-lookup"><span data-stu-id="23038-139">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="23038-140">Tilpass demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="23038-140">Customize demo data</span></span>
<span data-ttu-id="23038-141">Du kan redigere standard demonstrasjonsdata med all produkt- og kategoriinformasjon konfigurert i HK.</span><span class="sxs-lookup"><span data-stu-id="23038-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="23038-142">Når du oppdaterer CSV-filen, vil produktanbefalingene som returneres til kunder, umiddelbart gjenspeile endringene.</span><span class="sxs-lookup"><span data-stu-id="23038-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="23038-143">Utvidelsen inneholder en datafil med navnet RecoMockDataset.csv, som lar deg kontrollere datasettet som brukes for de uekte anbefalingene.</span><span class="sxs-lookup"><span data-stu-id="23038-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="23038-144">Filnavnet kan styres via konfigurasjon av utvidelsen ved hjelp av innstillingen **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="23038-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="23038-145">Dette gjør det mulig for deg å ha flere datasett tilgjengelige som enkelt kan byttes ved hjelp av konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="23038-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="23038-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="23038-146">Additional Resources</span></span>

[<span data-ttu-id="23038-147">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="23038-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="23038-148">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="23038-148">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="23038-149">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="23038-149">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="23038-150">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="23038-150">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="23038-151">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="23038-151">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="23038-152">Legge til lister over anbefalinger på et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="23038-152">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="23038-153">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="23038-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="23038-154">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="23038-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="23038-155">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="23038-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="23038-156">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="23038-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="23038-157">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="23038-157">Product recommendations FAQ</span></span>](faq-recommendations.md)

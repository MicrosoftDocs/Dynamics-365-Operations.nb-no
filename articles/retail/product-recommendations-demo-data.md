---
title: Demonstrasjonsdata for produktanbefalinger for omnikanal
description: Målet med dette dokument er å gi råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872332"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="d254d-103">Demonstrasjonsdata for produktanbefalinger for omnikanal</span><span class="sxs-lookup"><span data-stu-id="d254d-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="d254d-104">Målet med dette dokument er å gi råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="d254d-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="d254d-105">Produktanbefalinger for omnikanal gir et sett med ordnet liste over produkter som er kuratert eller programmatisk generert.</span><span class="sxs-lookup"><span data-stu-id="d254d-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="d254d-106">Disse listene kan brukes i flere scenarier, avhengig av forretningsbehovet.</span><span class="sxs-lookup"><span data-stu-id="d254d-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="d254d-107">Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="d254d-107">For more information about product recommendation lists, see [Product recommendations overview.](../commerce/product-recommendations.md)</span></span>

<span data-ttu-id="d254d-108">Produktanbefalinger for Lag 2-miljøer og høyere for Dynamics, beregnes automatisk basert på kundedata.</span><span class="sxs-lookup"><span data-stu-id="d254d-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="d254d-109">Bruk av demonstrasjonsdata for produktanbefalinger deaktiverer ikke produktanbefalingerløsninger som allerede er klargjort i miljøet og kostnadene som er knyttet til bruken.</span><span class="sxs-lookup"><span data-stu-id="d254d-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="d254d-110">Produktanbefalinger for Lag 1-miljøer er bare basert på statiske demonstrasjonsdata som er lagret i en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="d254d-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="d254d-111">Aktivere demonstrasjonsdata for produktanbefalinger i et miljø</span><span class="sxs-lookup"><span data-stu-id="d254d-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="d254d-112">Kunder må distribuere **Dynamics 365 Commerce-forhåndsvisningens demonstrasjonsutvidelse** til det aktuelle miljøet, som automatisk aktiverer demonstrasjonsdata for produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="d254d-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="d254d-113">Standard demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="d254d-113">Default demo data</span></span>
<span data-ttu-id="d254d-114">Alle miljøer i én boks leveres med forhåndslastede demonstrasjonsdata for produktanbefalinger som er lagret i den kommadelte filen **reco_demo_data.csv**, som er plassert i samme mappe som dette dokumentet på Retail Server.</span><span class="sxs-lookup"><span data-stu-id="d254d-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="d254d-115">Disse dataene er strukturert langs følgende kolonner</span><span class="sxs-lookup"><span data-stu-id="d254d-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="d254d-116">Kolonnenavn</span><span class="sxs-lookup"><span data-stu-id="d254d-116">Column name</span></span>         | <span data-ttu-id="d254d-117">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="d254d-117">Mandatory</span></span>          | <span data-ttu-id="d254d-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d254d-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="d254d-119">Mulige verdier</span><span class="sxs-lookup"><span data-stu-id="d254d-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d254d-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="d254d-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="d254d-122">Den spesifikke listetypen for produktanbefaling som demonstrasjonsdatapunktet skal generere.</span><span class="sxs-lookup"><span data-stu-id="d254d-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="d254d-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="d254d-123">RecoBestSelling</span></span></li><li><span data-ttu-id="d254d-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="d254d-124">RecoNew</span></span></li><li><span data-ttu-id="d254d-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="d254d-125">RecoTrending</span></span></li><li><span data-ttu-id="d254d-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="d254d-126">RecoCart</span></span></li><li><span data-ttu-id="d254d-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="d254d-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="d254d-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="d254d-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="d254d-130">Det spesifikke driftsenhetsnummeret der produktanbefalinger forventes å vises.</span><span class="sxs-lookup"><span data-stu-id="d254d-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="d254d-131">Kategori</span><span class="sxs-lookup"><span data-stu-id="d254d-131">Category</span></span>            |                    |    <span data-ttu-id="d254d-132">Kategorien som den bestemte listen skal returneres for.</span><span class="sxs-lookup"><span data-stu-id="d254d-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="d254d-133">Hvis det ikke er angitt en kategori, er listen bare for øverste navigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="d254d-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="d254d-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="d254d-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="d254d-135">For lister som krever utgangsverdi (RecoPeopleAlsoBuy og RecoCart) må produktlistene vise flere produkter.</span><span class="sxs-lookup"><span data-stu-id="d254d-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="d254d-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d254d-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="d254d-138">Ett eller flere produkter som skal returneres som resultat, atskilt med **";"**.</span><span class="sxs-lookup"><span data-stu-id="d254d-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="d254d-139">Tilpass demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="d254d-139">Customize demo data</span></span>
<span data-ttu-id="d254d-140">Kunder kan redigere standard demonstrasjonsdata med all produkt- og kategoriinformasjon som er konfigurert i HK.</span><span class="sxs-lookup"><span data-stu-id="d254d-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="d254d-141">Når CSV er oppdatert, vil produktanbefalingene som returneres til kunder, umiddelbart gjenspeile endringene.</span><span class="sxs-lookup"><span data-stu-id="d254d-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="d254d-142">Utvidelsen inneholder en datafil med navnet RecoMockDataset.csv, som lar kunden kontrollere datasettet som brukes til for de uekte anbefalingene.</span><span class="sxs-lookup"><span data-stu-id="d254d-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="d254d-143">Filnavnet kan styres via konfigurasjon av utvidelsen ved hjelp av innstillingen **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="d254d-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="d254d-144">Dette gjør det mulig for kundene å ha flere datasett tilgjengelige som enkelt kan byttes ved hjelp av konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d254d-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="d254d-145">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d254d-145">Additional resources</span></span>

[<span data-ttu-id="d254d-146">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="d254d-146">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="d254d-147">Miljøplanlegging</span><span class="sxs-lookup"><span data-stu-id="d254d-147">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)

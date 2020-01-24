---
title: Få produktanbefalinger ved hjelp av demonstrasjonsdata
description: Dette dokument gir råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: af8a30e69d9ed143e045950efdcece207f6da14c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697940"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="d460b-103">Få produktanbefalinger ved hjelp av demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="d460b-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="d460b-104">Dette dokument gir råd om hvordan dra nytte av produktanbefalinger for omnikanal i Lag 1-ett-miljøer i en boks, med forhåndsutfylte demonstrasjonsdata som kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="d460b-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="d460b-105">Produktanbefalinger for omnikanal gir et sett med kuraterte eller programmatisk genererte produktlister.</span><span class="sxs-lookup"><span data-stu-id="d460b-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="d460b-106">Disse listene kan brukes i flere scenarier, avhengig av forretningsbehovet.</span><span class="sxs-lookup"><span data-stu-id="d460b-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="d460b-107">Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d460b-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="d460b-108">Produktanbefalinger for Lag 2-miljøer og høyere Dynamics 365-miljøer beregnes automatisk basert på kundedata.</span><span class="sxs-lookup"><span data-stu-id="d460b-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="d460b-109">Bruk av demonstrasjonsdata for produktanbefalinger deaktiverer ikke produktanbefalingerløsninger som allerede er klargjort i miljøet og kostnadene som er knyttet til bruken.</span><span class="sxs-lookup"><span data-stu-id="d460b-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="d460b-110">Produktanbefalinger for Lag 1-miljøer er bare basert på statiske demonstrasjonsdata som er lagret i en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="d460b-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="d460b-111">Aktivere demonstrasjonsdata for produktanbefalinger i et miljø</span><span class="sxs-lookup"><span data-stu-id="d460b-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="d460b-112">For å aktivere demonstrasjonsdata for produktanbefalinger må du distribuere Dynamics 365 Commerce-forhåndsvisningens demonstrasjonsutvidelse til det aktuelle miljøet.</span><span class="sxs-lookup"><span data-stu-id="d460b-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="d460b-113">Når du gjør dette, aktiveres demonstrasjonsdata for produktanbefalinger automatisk.</span><span class="sxs-lookup"><span data-stu-id="d460b-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="d460b-114">Standard demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="d460b-114">Default demo data</span></span>
<span data-ttu-id="d460b-115">Alle miljøer i én boks leveres med forhåndslastede demonstrasjonsdata for produktanbefalinger som er lagret i den kommadelte filen reco_demo_data.csv, som er plassert på Retail Server.</span><span class="sxs-lookup"><span data-stu-id="d460b-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Retail Server.</span></span>

<span data-ttu-id="d460b-116">Dataene er strukturert langs følgende kolonner.</span><span class="sxs-lookup"><span data-stu-id="d460b-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="d460b-117">Kolonnenavn</span><span class="sxs-lookup"><span data-stu-id="d460b-117">Column name</span></span>         | <span data-ttu-id="d460b-118">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="d460b-118">Mandatory</span></span>          | <span data-ttu-id="d460b-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d460b-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="d460b-120">Mulige verdier</span><span class="sxs-lookup"><span data-stu-id="d460b-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d460b-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="d460b-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="d460b-123">Den spesifikke listetypen for produktanbefaling som demonstrasjonsdatapunktet skal generere.</span><span class="sxs-lookup"><span data-stu-id="d460b-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="d460b-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="d460b-124">RecoBestSelling</span></span></li><li><span data-ttu-id="d460b-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="d460b-125">RecoNew</span></span></li><li><span data-ttu-id="d460b-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="d460b-126">RecoTrending</span></span></li><li><span data-ttu-id="d460b-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="d460b-127">RecoCart</span></span></li><li><span data-ttu-id="d460b-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="d460b-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="d460b-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="d460b-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="d460b-131">Det spesifikke driftsenhetsnummeret der produktanbefalinger forventes å vises.</span><span class="sxs-lookup"><span data-stu-id="d460b-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="d460b-132">Kategori</span><span class="sxs-lookup"><span data-stu-id="d460b-132">Category</span></span>            |                    |    <span data-ttu-id="d460b-133">Kategorien som den bestemte listen skal returneres for.</span><span class="sxs-lookup"><span data-stu-id="d460b-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="d460b-134">Hvis det ikke er angitt en kategori, er listen bare for øverste navigasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="d460b-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="d460b-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="d460b-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="d460b-136">For lister som krever utgangsverdi (RecoPeopleAlsoBuy og RecoCart) må produktlistene vise flere produkter.</span><span class="sxs-lookup"><span data-stu-id="d460b-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="d460b-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d460b-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="d460b-139">Ett eller flere produkter som skal returneres som resultat, atskilt med ';'.</span><span class="sxs-lookup"><span data-stu-id="d460b-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="d460b-140">Tilpass demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="d460b-140">Customize demo data</span></span>
<span data-ttu-id="d460b-141">Du kan redigere standard demonstrasjonsdata med all produkt- og kategoriinformasjon konfigurert i HK.</span><span class="sxs-lookup"><span data-stu-id="d460b-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="d460b-142">Når du oppdaterer CSV-filen, vil produktanbefalingene som returneres til kunder, umiddelbart gjenspeile endringene.</span><span class="sxs-lookup"><span data-stu-id="d460b-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="d460b-143">Utvidelsen inneholder en datafil med navnet RecoMockDataset.csv, som lar deg kontrollere datasettet som brukes for de uekte anbefalingene.</span><span class="sxs-lookup"><span data-stu-id="d460b-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="d460b-144">Filnavnet kan styres via konfigurasjon av utvidelsen ved hjelp av innstillingen **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="d460b-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="d460b-145">Dette gjør det mulig for deg å ha flere datasett tilgjengelige som enkelt kan byttes ved hjelp av konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="d460b-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="d460b-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d460b-146">Additional Resources</span></span>

[<span data-ttu-id="d460b-147">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="d460b-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d460b-148">Miljøplanlegging</span><span class="sxs-lookup"><span data-stu-id="d460b-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
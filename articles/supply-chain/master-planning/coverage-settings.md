---
title: Dekningsinnstillinger
description: Dette emnet inneholder informasjon om dekningsinnstillingene som hovedplanlegging bruker til å beregne varebehov.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538900"
---
# <a name="coverage-settings"></a><span data-ttu-id="3bc8a-103">Dekningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="3bc8a-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3bc8a-104">Hovedplanlegging bruker dekningsinnstillinger til å beregne varebehov.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="3bc8a-105">Du kan angi dekningsinnstillinger på flere måter:</span><span class="sxs-lookup"><span data-stu-id="3bc8a-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="3bc8a-106">Angi dekningsinnstillinger for en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="3bc8a-107">Du kan opprette en dekningsgruppe som inneholder innstillinger for alle produkter som er koblet til dekningsgruppen.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="3bc8a-108">Hvis du vil opprette en dekningsgruppe, går du til **Hovedplanlegging &gt; Oppsett &gt; Dekning &gt; Dekningsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="3bc8a-109">Du kan koble en dekningsgruppe til et produkt.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="3bc8a-110">Hvis koblingen er spesifikk for et område, lager eller produktdimensjon, kan du bruke **Dekningsgruppe**-feltet på **Varedekning**-siden.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="3bc8a-111">Hvis koblingen er generisk, uavhengig av produktdimensjonene, bruker du **Dekningsgruppe**-feltet i **Plan**-hurtigkategorien på **Produktdetaljer**-siden.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="3bc8a-112">Hvis du ikke kobler en dekningsgruppe til et produkt, bruker hovedplanlegging som standard den generelle dekningsgruppen som er angitt på siden **Hovedplanleggingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="3bc8a-113">Angi dekningsinnstillinger for et produkt.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="3bc8a-114">Du kan opprette dekningsinnstillinger for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="3bc8a-115">Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="3bc8a-116">Velg produktet. I handlingsruten, i kategorien **Plan** i **Dekning**-gruppen, velger du **Varedekning** for å åpne **Varedekning**-siden.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="3bc8a-117">Hvis produktet allerede er koblet til en dekningsgruppe, kan du overstyre innstillingene for dekningsgruppen ved å bruke **Overstyr**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="3bc8a-118">Dekningsinnstillingene på **Varedekning**-siden har prioritet over innstillingene på **Dekningsgruppe**-siden.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="3bc8a-119">Angi dekningsinnstillinger for et produkt ved hjelp av en veiviser.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="3bc8a-120">Veiviseren fører deg gjennom prosessen med å definere de primære varedekningsparameterne.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="3bc8a-121">På **Varedekning**-siden i handlingsruten velger du **Veiviser** for å åpne **Varedekningsveiviseren**.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="3bc8a-122">Angi dekningsinnstillinger for en dimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="3bc8a-123">Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="3bc8a-124">På **Detaljer om frigitt produkt**-siden, i hurtigfanen **Generelt** i **Administrasjon**-delen, velger du koblingen i feltet **Lagringsdimensjonsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="3bc8a-125">På **Lagringsdimensjonsgrupper**-siden merker du av for **Dekningsplanlegg etter dimensjon** for å opprette dekningsinnstillinger for en dimensjon i lagringsdimensjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="3bc8a-126">Feltet **Dekningsplanlegg etter dimensjon** må være valgt for alle produktdimensjoner, for eksempel konfigurasjon, farge, størrelse og stil.</span><span class="sxs-lookup"><span data-stu-id="3bc8a-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3bc8a-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3bc8a-127">Additional resources</span></span>

[<span data-ttu-id="3bc8a-128">Hovedplaner</span><span class="sxs-lookup"><span data-stu-id="3bc8a-128">Master plans</span></span>](master-plans.md)

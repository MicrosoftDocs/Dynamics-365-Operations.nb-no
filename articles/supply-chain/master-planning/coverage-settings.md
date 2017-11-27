---
title: Dekningsinnstillinger
description: "Hovedplanlegging bruker dekningsinnstillinger til å beregne varebehov."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd85f89917659ac9c94590bace765b2123d6e556
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="8f3a5-103">Dekningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="8f3a5-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8f3a5-104">Hovedplanlegging bruker dekningsinnstillinger til å beregne varebehov.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="8f3a5-105">Du kan angi dekningsinnstillinger på flere måter:</span><span class="sxs-lookup"><span data-stu-id="8f3a5-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="8f3a5-106">Angi dekningsinnstillinger for en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="8f3a5-107">Du kan opprette en dekningsgruppe som inneholder innstillinger for alle produkter som er koblet til dekningsgruppen.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="8f3a5-108">Klikk **Hovedplanlegging &gt; Oppsett &gt; Dekning &gt; Dekningsgrupper** for å opprette en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="8f3a5-109">Du kan koble en dekningsgruppe til et produkt.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="8f3a5-110">Hvis koblingen er spesifikk for et område, lager eller produktdimensjon, kan du bruke **Dekningsgruppe**-feltet på **Varedekning**-siden.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="8f3a5-111">Hvis koblingen er generisk, uavhengig av produktdimensjonene, bruker du **Dekningsgruppe** i **Plan**-hurtigkategorien på **Produktdetaljer**-siden.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="8f3a5-112">Hvis du ikke kobler en dekningsgruppe til et produkt, bruker hovedplanlegging den **generelle dekningsgruppen** som er angitt på siden **Hovedplanleggingsparametere**, som standard.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="8f3a5-113">Angi dekningsinnstillinger for et produkt.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="8f3a5-114">Du kan opprette dekningsinnstillinger for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="8f3a5-115">Klikk **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="8f3a5-116">Velg produktet. I **handlingsruten**, i kategorien **Plan** i **Dekningsgruppen**, klikker du **Varedekning** for å åpne **Varedekning**-siden.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="8f3a5-117">Hvis produktet allerede er koblet til en dekningsgruppe, kan du overstyre innstillingene for dekningsgruppen ved å bruke **Overstyr**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="8f3a5-118">Dekningsinnstillingene på **Varedekning**-siden har prioritet over innstillingene på **Dekningsgruppe**-siden.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="8f3a5-119">Angi dekningsinnstillinger for et produkt ved hjelp av en veiviser.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="8f3a5-120">Veiviseren gir deg trinnvise instruksjoner om hvordan du definerer primære dekningsparametere.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="8f3a5-121">På **Varedekning**-siden klikker du **Veiviser** for å åpne **Varedekningsveiviseren**.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="8f3a5-122">Angi dekningsinnstillinger for en dimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="8f3a5-123">Klikk **Behandling av produktinformasjon &gt; Felles &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="8f3a5-124">På siden **Detaljer om frigitt produkt**, i kategorien **Generelt** i **Administrasjon**-gruppen, klikker du koblingen **Lagringsdimensjonsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="8f3a5-125">På **Lagringsdimensjonsgruppe**-siden velger du feltet **Dekningsplanlegg etter dimensjon** for å opprette dekningsinnstillinger for en dimensjon i lagringsdimensjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="8f3a5-126">Alle produktdimensjoner, for eksempel konfigurasjon, farge, størrelse, stil, må ha feltet **Dekningsplanlegg etter dimensjon** valgt.</span><span class="sxs-lookup"><span data-stu-id="8f3a5-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="8f3a5-127">Se også</span><span class="sxs-lookup"><span data-stu-id="8f3a5-127">See also</span></span>
--------

[<span data-ttu-id="8f3a5-128">Hovedplaner</span><span class="sxs-lookup"><span data-stu-id="8f3a5-128">Master plans</span></span>](master-plans.md)





---
title: Dekningsinnstillinger
description: Dette emnet inneholder informasjon om dekningsinnstillingene som hovedplanlegging bruker til å beregne varebehov.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1134f734f1025151a56b2a72266a6baa5763ba4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434654"
---
# <a name="coverage-settings"></a><span data-ttu-id="d0174-103">Dekningsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="d0174-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0174-104">Hovedplanlegging bruker dekningsinnstillinger til å beregne varebehov.</span><span class="sxs-lookup"><span data-stu-id="d0174-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="d0174-105">Du kan angi dekningsinnstillinger på flere måter:</span><span class="sxs-lookup"><span data-stu-id="d0174-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="d0174-106">Angi dekningsinnstillinger for en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d0174-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="d0174-107">Du kan opprette en dekningsgruppe som inneholder innstillinger for alle produkter som er koblet til dekningsgruppen.</span><span class="sxs-lookup"><span data-stu-id="d0174-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="d0174-108">Hvis du vil opprette en dekningsgruppe, går du til **Hovedplanlegging &gt; Oppsett &gt; Dekning &gt; Dekningsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="d0174-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="d0174-109">Du kan koble en dekningsgruppe til et produkt.</span><span class="sxs-lookup"><span data-stu-id="d0174-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="d0174-110">Hvis koblingen er spesifikk for et område, lager eller produktdimensjon, kan du bruke **Dekningsgruppe**-feltet på **Varedekning**-siden.</span><span class="sxs-lookup"><span data-stu-id="d0174-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="d0174-111">Hvis koblingen er generisk, uavhengig av produktdimensjonene, bruker du **Dekningsgruppe**-feltet i **Plan**-hurtigkategorien på **Produktdetaljer**-siden.</span><span class="sxs-lookup"><span data-stu-id="d0174-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="d0174-112">Hvis du ikke kobler en dekningsgruppe til et produkt, bruker hovedplanlegging som standard den generelle dekningsgruppen som er angitt på siden **Hovedplanleggingsparametere**.</span><span class="sxs-lookup"><span data-stu-id="d0174-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="d0174-113">Angi dekningsinnstillinger for et produkt.</span><span class="sxs-lookup"><span data-stu-id="d0174-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="d0174-114">Du kan opprette dekningsinnstillinger for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="d0174-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="d0174-115">Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="d0174-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="d0174-116">Velg produktet. I handlingsruten, i kategorien **Plan** i **Dekning**-gruppen, velger du **Varedekning** for å åpne **Varedekning**-siden.</span><span class="sxs-lookup"><span data-stu-id="d0174-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="d0174-117">Hvis produktet allerede er koblet til en dekningsgruppe, kan du overstyre innstillingene for dekningsgruppen ved å bruke **Overstyr**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0174-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="d0174-118">Dekningsinnstillingene på **Varedekning**-siden har prioritet over innstillingene på **Dekningsgruppe**-siden.</span><span class="sxs-lookup"><span data-stu-id="d0174-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="d0174-119">Angi dekningsinnstillinger for et produkt ved hjelp av en veiviser.</span><span class="sxs-lookup"><span data-stu-id="d0174-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="d0174-120">Veiviseren fører deg gjennom prosessen med å definere de primære varedekningsparameterne.</span><span class="sxs-lookup"><span data-stu-id="d0174-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="d0174-121">På **Varedekning**-siden i handlingsruten velger du **Veiviser** for å åpne **Varedekningsveiviseren**.</span><span class="sxs-lookup"><span data-stu-id="d0174-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="d0174-122">Angi dekningsinnstillinger for en dimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d0174-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="d0174-123">Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="d0174-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="d0174-124">På **Detaljer om frigitt produkt**-siden, i hurtigfanen **Generelt** i **Administrasjon**-delen, velger du koblingen i feltet **Lagringsdimensjonsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="d0174-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="d0174-125">På **Lagringsdimensjonsgrupper**-siden merker du av for **Dekningsplanlegg etter dimensjon** for å opprette dekningsinnstillinger for en dimensjon i lagringsdimensjonsgruppen.</span><span class="sxs-lookup"><span data-stu-id="d0174-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="d0174-126">Feltet **Dekningsplanlegg etter dimensjon** må være valgt for alle produktdimensjoner, for eksempel konfigurasjon, farge, størrelse og stil.</span><span class="sxs-lookup"><span data-stu-id="d0174-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="d0174-127">Dekningskoder</span><span class="sxs-lookup"><span data-stu-id="d0174-127">Coverage codes</span></span>

<span data-ttu-id="d0174-128">Hovedplanlegging kan konfigureres til å bruke forskjellige metoder for etterfylling.</span><span class="sxs-lookup"><span data-stu-id="d0174-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="d0174-129">Metodene for etterfylling eller justering av partistørrelse er teknikkene som brukes av systemet for å fastslå den satsvise størrelsen for kjøpte eller produserte varer.</span><span class="sxs-lookup"><span data-stu-id="d0174-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="d0174-130">Hver etterfyllingsmetode tilordnes én av følgende dekningskoder:</span><span class="sxs-lookup"><span data-stu-id="d0174-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="d0174-131">**Manuell** – Metoden for justering av partistørrelse der systemet ikke foreslår kjøps-, overførings- eller produksjonsordrer for varen.</span><span class="sxs-lookup"><span data-stu-id="d0174-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="d0174-132">Planleggeren for varen vil være ansvarlig for å opprette de nødvendige ordrene for etterfylling av varen.</span><span class="sxs-lookup"><span data-stu-id="d0174-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="d0174-133">**Per behov** – Metoden for justering av partistørrelse der systemet oppretter et bestillingsforslag, en overføring eller en produksjonsordre per behov for varen.</span><span class="sxs-lookup"><span data-stu-id="d0174-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="d0174-134">Dette brukes vanligvis for kostbare varer med periodisk etterspørsel.</span><span class="sxs-lookup"><span data-stu-id="d0174-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="d0174-135">**Per periode** – Metoden for justering av partistørrelse som kombinerer alt behov for en periode i én ordre for varen.</span><span class="sxs-lookup"><span data-stu-id="d0174-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="d0174-136">Ordren vil bli planlagt for den første dagen i perioden, og antallet vil oppfylle nettobehovet i den etablerte perioden.</span><span class="sxs-lookup"><span data-stu-id="d0174-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="d0174-137">Perioden begynner med det første behovet for varen og dekker den definerte lengden i tid.</span><span class="sxs-lookup"><span data-stu-id="d0174-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="d0174-138">Neste periode starter med de neste behovene til varen.</span><span class="sxs-lookup"><span data-stu-id="d0174-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="d0174-139">**Min/maks** – Metoden for justering av partistørrelse som inneholder etterfyllingen av lager opptil et bestemt nivå når beholdningsprognosen er under en terskel.</span><span class="sxs-lookup"><span data-stu-id="d0174-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="d0174-140">Etterfyllingsantallet vil være differansen mellom maksimumsnivået og det forhåndsberegnede nivået.</span><span class="sxs-lookup"><span data-stu-id="d0174-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="d0174-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d0174-141">Additional resources</span></span>

[<span data-ttu-id="d0174-142">Oversikt over hovedplaner</span><span class="sxs-lookup"><span data-stu-id="d0174-142">Master plans overview</span></span>](master-plans.md)

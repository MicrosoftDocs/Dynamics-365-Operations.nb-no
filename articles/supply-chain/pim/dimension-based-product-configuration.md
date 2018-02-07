---
title: Dimensjonsbasert produktkonfigurasjon
description: "Dimensjonsbasert produktkonfigurasjon representerer en enkel løsning for oppretting av mange produktvarianter fra én enkelt produktstandard og dens stykkliste."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 297e60e63b88b610d0886ad16667c4f99cc74ccb
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="3d747-103">Dimensjonsbasert produktkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3d747-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3d747-104">Dimensjonsbasert produktkonfigurasjon representerer en enkel løsning for oppretting av mange produktvarianter fra én enkelt produktstandard og dens stykkliste.</span><span class="sxs-lookup"><span data-stu-id="3d747-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="3d747-105">Dimensjonsbasert produktkonfigurasjon er én av tre innebygde teknologiene for produktkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3d747-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="3d747-106">De to andre teknologiene er forhåndsdefinerte varianter og restriksjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3d747-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="3d747-107">Alle tre teknologiene bruker en produktstandard som utgangspunkt og lar brukeren opprette mange produktvarianter for én produktstandard.</span><span class="sxs-lookup"><span data-stu-id="3d747-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="3d747-108">Nøkkelbegreper</span><span class="sxs-lookup"><span data-stu-id="3d747-108">Key concepts</span></span>
<span data-ttu-id="3d747-109">Dimensjonsbasert produktkonfigurasjon er basert på følgende nøkkelbegreper:</span><span class="sxs-lookup"><span data-stu-id="3d747-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="3d747-110">Produktstandarder</span><span class="sxs-lookup"><span data-stu-id="3d747-110">Product masters</span></span>
-   <span data-ttu-id="3d747-111">Konfigurasjonsproduktdimensjon</span><span class="sxs-lookup"><span data-stu-id="3d747-111">Configuration product dimension</span></span>
-   <span data-ttu-id="3d747-112">Konfigurasjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="3d747-112">Configuration groups</span></span>
-   <span data-ttu-id="3d747-113">Stykkliste</span><span class="sxs-lookup"><span data-stu-id="3d747-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="3d747-114">Konfigurasjonsrute</span><span class="sxs-lookup"><span data-stu-id="3d747-114">Configuration route</span></span>
-   <span data-ttu-id="3d747-115">Konfigurasjonsregler</span><span class="sxs-lookup"><span data-stu-id="3d747-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="3d747-116">Produktstandarder</span><span class="sxs-lookup"><span data-stu-id="3d747-116">Product masters</span></span>

<span data-ttu-id="3d747-117">En produktstandard utgangspunktet for produktkonfigurasjonsprosesser.</span><span class="sxs-lookup"><span data-stu-id="3d747-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="3d747-118">For den dimensjonsbaserte produktkonfigurasjonen må du ha en produktstandard med denne bestemte konfigurasjonsteknologien og en produktdimensjonsgruppe som omfatter konfigurasjonsproduktdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="3d747-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="3d747-119">Konfigurasjonsproduktdimensjon</span><span class="sxs-lookup"><span data-stu-id="3d747-119">Configuration product dimension</span></span>

<span data-ttu-id="3d747-120">Konfigurasjonsproduktdimensjonen brukes til å identifisere produktvariantene for en produktstandard med den dimensjonsbaserte konfigurasjonsteknologien.</span><span class="sxs-lookup"><span data-stu-id="3d747-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="3d747-121">Konfigurasjonsdimensjonsverdien angis av brukeren og skal bidra til å identifisere de individuelle produktvariantene.</span><span class="sxs-lookup"><span data-stu-id="3d747-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="3d747-122">Konfigurasjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="3d747-122">Configuration groups</span></span>

<span data-ttu-id="3d747-123">Konfigurasjonsgrupper defineres i et sentralt repositorium og kan brukes i forbindelse med alle produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="3d747-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="3d747-124">Konfigurasjonsgrupper er knyttet til de enkeltstående stykklistelinjene og holder sammen en gruppe med linjer som er gjensidig utelukkende.</span><span class="sxs-lookup"><span data-stu-id="3d747-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="3d747-125">Dette betyr at bare én linje i en gruppe kan velges for én produktvariant.</span><span class="sxs-lookup"><span data-stu-id="3d747-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="3d747-126">Stykkliste</span><span class="sxs-lookup"><span data-stu-id="3d747-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="3d747-127">Stykklisten representerer byggeblokker for en dimensjonsbasert produktkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3d747-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="3d747-128">Den må inneholde alle de ulike produktene som kan brukes i en hvilken som helst produktvariant.</span><span class="sxs-lookup"><span data-stu-id="3d747-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="3d747-129">Hver linje i stykklisten kan referere til en konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3d747-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="3d747-130">Hvis en linje ikke refererer til en konfigurasjonsgruppe, tas den med i alle produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="3d747-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="3d747-131">Konfigurasjonsrute</span><span class="sxs-lookup"><span data-stu-id="3d747-131">Configuration route</span></span>

<span data-ttu-id="3d747-132">Konfigurasjonsruten bestemmer rekkefølgen på konfigurasjonsgruppene, slik de vises for brukeren under produktkonfigurasjonsprosessen.</span><span class="sxs-lookup"><span data-stu-id="3d747-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="3d747-133">Konfigurasjonsregler</span><span class="sxs-lookup"><span data-stu-id="3d747-133">Configuration rules</span></span>

<span data-ttu-id="3d747-134">Konfigurasjonsreglene representerer en mekanisme for å sikre at et produkt som er inkludert i én konfigurasjonsgruppe i en stykkliste, fremtvinger en inkludering eller en utelukkelse av et produkt i en annen konfigurasjonsgruppe i samme stykklisten.</span><span class="sxs-lookup"><span data-stu-id="3d747-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="3d747-135">Produktmodelleringsprosess</span><span class="sxs-lookup"><span data-stu-id="3d747-135">Product modeling process</span></span>
<span data-ttu-id="3d747-136">Den naturlige sekvensen i utviklingen av en produktmodell for et dimensjonsbasert produkt starter med definisjonen av de relevante konfigurasjonsgruppene.</span><span class="sxs-lookup"><span data-stu-id="3d747-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="3d747-137">Det er viktig å sikre at alle produkter som skal brukes i stykklisten, er frigitt til firmaet som produktmodellen er utviklet for.</span><span class="sxs-lookup"><span data-stu-id="3d747-137">It is important to ensure that all products which will be used in the BOM have been released to the company that the product model is built for.</span></span> <span data-ttu-id="3d747-138">Med disse byggeblokkene på plass kan brukeren opprette stykklisten og tilordne konfigurasjonsgrupper til alle relevante stykklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="3d747-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="3d747-139">Når stykklisten er fullført, kan en konfigurasjonsrute defineres for å ordne konfigurasjonsgruppene i riktig rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="3d747-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="3d747-140">[![Dimensjonsbasert produktmodelleringsprosess](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Hvis det er visse produkter fra forskjellige konfigurasjonsgrupper som enten må, eller ikke må brukes sammen, kan du opprette konfigurasjonsregler som vil håndheve disse produktrelasjonene.</span><span class="sxs-lookup"><span data-stu-id="3d747-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="3d747-141">Etter at stykklisten er knyttet sammen med en dimensjonsbasert produktstandard via en stykklisteversjon og begge er godkjent og aktivert, kan du opprette produktkonfigurasjoner og skrive inn et navn for hver konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3d747-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="3d747-142">Du kan definere konfigurasjonene før eventuelle transaksjoner er generert, eller du kan gjøre det når det er behov for en bestemt konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3d747-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="3d747-143">Foreslått bruk</span><span class="sxs-lookup"><span data-stu-id="3d747-143">Suggested use</span></span>

<span data-ttu-id="3d747-144">Teknologien for dimensjonsbasert konfigurasjon passer best for produkter med begrenset varians og kombinasjonen av de standard produktdimensjonene størrelse, farge, stil, og konfigurasjon er ikke egnet til å identifisere en bestemt produktvariant.</span><span class="sxs-lookup"><span data-stu-id="3d747-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="3d747-145">Et eksempel kan være sykkel med rammehøyde, hjulstørrelse, bremstyper og ulike gir.</span><span class="sxs-lookup"><span data-stu-id="3d747-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="3d747-146">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="3d747-146">Next step</span></span> 

<span data-ttu-id="3d747-147">Følgende åtte oppgavelinjer er oppført i den rekkefølgen du skal fylle dem ut.</span><span class="sxs-lookup"><span data-stu-id="3d747-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="3d747-148">Opprette en dimensjonsbasert produktstandard (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3d747-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="3d747-149">Frigi en dimensjonsbasert produktstandard (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3d747-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="3d747-150">Fullføre grunnleggende oppsett av en frigitt produktstandard (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3d747-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="3d747-151">Definere konfigurasjonsgrupper (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3d747-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="3d747-152">Opprette en stykkliste for en dimensjonsbasert produktstandard (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3d747-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="3d747-153">Definere konfigurasjonsruter (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3d747-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="3d747-154">Opprette konfigurasjonsregler (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3d747-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="3d747-155">Opprette dimensjonsbaserte konfigurasjoner (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="3d747-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)



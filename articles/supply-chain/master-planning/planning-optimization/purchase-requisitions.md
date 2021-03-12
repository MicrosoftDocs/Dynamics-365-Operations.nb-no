---
title: Innkjøpsrekvisisjoner
description: Dette emnet beskriver hvordan innkjøpsrekvisisjoner støttes i planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8075f8d7c3868c6d6012edbce17dbbb4749209ab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992351"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="94563-103">Innkjøpsrekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="94563-103">Purchase requisitions</span></span>

<span data-ttu-id="94563-104">Hovedplanlegging kan etterfylle godkjente innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="94563-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="94563-105">Brukere trenger derfor ikke å bruke en arbeidsflyt til å opprette bestillinger for å dekke innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="94563-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="94563-106">Innkjøpsrekvisisjoner kan i stedet dekkes av hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="94563-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="94563-107">På grunn av denne funksjonaliteten kan en innkjøpsrekvisisjon produsere en bestilling, en overføringsordre eller en produksjonsordre, avhengig av verdien for **Type planlagt bestilling** som er angitt for det tilknyttede produktet.</span><span class="sxs-lookup"><span data-stu-id="94563-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="94563-108">Aktivere hovedplaner for å inkludere rekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="94563-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="94563-109">Følg denne fremgangsmåten for å inkludere rekvisisjoner under dekningsberegningen for en hovedplan.</span><span class="sxs-lookup"><span data-stu-id="94563-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="94563-110">Gå til **Hovedplanlegging** \> **Oppsett** \> **Planer** \> **Hovedplaner**.</span><span class="sxs-lookup"><span data-stu-id="94563-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="94563-111">Opprett eller velg en hovedplan.</span><span class="sxs-lookup"><span data-stu-id="94563-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="94563-112">I hurtigfanen **Generelt** angir du *Ja* for alternativet **Inkluder rekvisisjoner**.</span><span class="sxs-lookup"><span data-stu-id="94563-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="94563-113">Gjenta trinn 2 og 3 for hver ytterligere hovedplan der du vil ta med rekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="94563-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="94563-114">Horisont for godkjente rekvisisjoner</span><span class="sxs-lookup"><span data-stu-id="94563-114">Approved requisitions time fence</span></span>

<span data-ttu-id="94563-115">*Horisonten for godkjente rekvisisjoner* fastsetter hvor langt tilbake (i dager) en hovedplan skal ta med behov fra godkjente etterfyllingsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="94563-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="94563-116">Du kan angi en horisont for godkjente rekvisisjoner både på dekningsgruppenivået og hovedplannivået.</span><span class="sxs-lookup"><span data-stu-id="94563-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="94563-117">Angi horisonten for godkjente rekvisisjoner for en dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="94563-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="94563-118">Gå til **Hovedplanlegging** \> **Oppsett** \> **Dekning** \> **Dekningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="94563-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage group**.</span></span>
1. <span data-ttu-id="94563-119">Opprett eller velg en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="94563-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="94563-120">Angi antallet dager som skal tas med i horisonten, i feltet **Godkjente rekvisisjoner - horisont (dager)** i hurtigfanen **Annet**.</span><span class="sxs-lookup"><span data-stu-id="94563-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="94563-121">Gjenta trinn 2 og 3 for hver ytterligere dekningsgruppe der du vil angi en horisont for godkjente rekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="94563-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="94563-122">Angi horisonten for godkjente rekvisisjoner for individuelle hovedplaner</span><span class="sxs-lookup"><span data-stu-id="94563-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="94563-123">Når du angir en horisont for godkjente rekvisisjoner for en individuell hovedplan, overstyrer innstillingen horisontinnstillingen for enhver gjeldende dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="94563-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="94563-124">Gå til **Hovedplanlegging** \> **Oppsett** \> **Planer** \> **Hovedplaner**.</span><span class="sxs-lookup"><span data-stu-id="94563-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="94563-125">Opprett eller velg en hovedplan.</span><span class="sxs-lookup"><span data-stu-id="94563-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="94563-126">Angi antallet dager som skal tas med i horisonten, i feltet **Godkjente rekvisisjoner - horisont (dager)** i hurtigfanen **Horisonter i dager**.</span><span class="sxs-lookup"><span data-stu-id="94563-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="94563-127">Gjenta trinn 2 og 3 for hver ytterligere hovedplan der du vil angi en horisont for godkjente rekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="94563-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94563-128">**Kommer snart:** Horisonter for godkjente rekvisisjoner støttes ikke ennå for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="94563-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="94563-129">Før de støttes, ignoreres alle verdier du angir i feltet **Godkjente rekvisisjoner - horisont (dager)**.</span><span class="sxs-lookup"><span data-stu-id="94563-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="94563-130">Uavhengig forsyning, uavhengig av dekningskode</span><span class="sxs-lookup"><span data-stu-id="94563-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="94563-131">Innkjøpsrekvisisjoner dekkes alltid av uavhengige planlagte bestillinger, uavhengig av dekningskode.</span><span class="sxs-lookup"><span data-stu-id="94563-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="94563-132">Denne virkemåten sikrer klar sporbarhet og klare arbeidsflyter mellom innkjøpsrekvisisjoner og etterfyllingsordrer.</span><span class="sxs-lookup"><span data-stu-id="94563-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="94563-133">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="94563-133">Example 1</span></span>

<span data-ttu-id="94563-134">Et produkt er konfigurert slik at det har **Dekningskode**-verdien *Min./maks.* Det har følgende statuser for beholdning og rekvisisjon:</span><span class="sxs-lookup"><span data-stu-id="94563-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="94563-135">Lagerbeholdningsantall = 10.</span><span class="sxs-lookup"><span data-stu-id="94563-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="94563-136">Minimumslagerantall = 15.</span><span class="sxs-lookup"><span data-stu-id="94563-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="94563-137">Maksimumslagerantall = 20.</span><span class="sxs-lookup"><span data-stu-id="94563-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="94563-138">Det finnes en innkjøpsrekvisisjon for ett stykk.</span><span class="sxs-lookup"><span data-stu-id="94563-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="94563-139">Ønsket dato for den er i dag.</span><span class="sxs-lookup"><span data-stu-id="94563-139">It has a requested date of today.</span></span>

<span data-ttu-id="94563-140">Når hovedplanlegging kjører, opprettes det to planlagte bestillinger: én for 10 stykker for å etterfylle beholdningen til maksimumsantallet, og én for ett stykk for å etterfylle innkjøpsrekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="94563-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="94563-141">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="94563-141">Example 2</span></span>

<span data-ttu-id="94563-142">Et produkt er konfigurert slik at det har **Dekningskode**-verdien *Min./maks.* Det har følgende statuser for beholdning og rekvisisjon:</span><span class="sxs-lookup"><span data-stu-id="94563-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="94563-143">Lagerbeholdningsantall = 17.</span><span class="sxs-lookup"><span data-stu-id="94563-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="94563-144">Minimumslagerantall = 15.</span><span class="sxs-lookup"><span data-stu-id="94563-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="94563-145">Maksimumslagerantall = 20.</span><span class="sxs-lookup"><span data-stu-id="94563-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="94563-146">Det finnes en innkjøpsrekvisisjon for ett stykk.</span><span class="sxs-lookup"><span data-stu-id="94563-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="94563-147">Ønsket dato for den er i dag.</span><span class="sxs-lookup"><span data-stu-id="94563-147">It has a requested date of today.</span></span>

<span data-ttu-id="94563-148">Når hovedplanleggingen kjører, opprettes det én planlagt bestilling for ett stykk for å etterfylle innkjøpsrekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="94563-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="94563-149">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="94563-149">Example 3</span></span>

<span data-ttu-id="94563-150">Et produkt er konfigurert slik at det har **Dekningskode**-verdien *Periode* og en periodelengde på sju dager.</span><span class="sxs-lookup"><span data-stu-id="94563-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="94563-151">Det har følgende statuser for beholdning, salgsordre og rekvisisjon:</span><span class="sxs-lookup"><span data-stu-id="94563-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="94563-152">Lagerbeholdningsantall = 0.</span><span class="sxs-lookup"><span data-stu-id="94563-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="94563-153">Det finnes en salgsordre for fem stykker.</span><span class="sxs-lookup"><span data-stu-id="94563-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="94563-154">Forventet forsendelsesdato er i dag pluss én dag.</span><span class="sxs-lookup"><span data-stu-id="94563-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="94563-155">Det finnes en innkjøpsrekvisisjon for tre stykker.</span><span class="sxs-lookup"><span data-stu-id="94563-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="94563-156">Ønsket dato for den er i dag pluss tre dager.</span><span class="sxs-lookup"><span data-stu-id="94563-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="94563-157">Når hovedplanlegging kjører, opprettes det to planlagte bestillinger: én for tre stykker for å etterfylle innkjøpsrekvisisjonen, og én for fem stykker for å etterfylle salgsordrebehovet.</span><span class="sxs-lookup"><span data-stu-id="94563-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="94563-158">Når en planlagt bestilling som er utlignet mot en innkjøpsrekvisisjon, autoriseres, beholder planleggingsmotoren utligningen mot innkjøpsrekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="94563-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="94563-159">Hvis den autoriserte bestillingen senere mangler noe av antallet som kreves for å oppfylle innkjøpsrekvisisjonen, oppretter systemet en ny planlagt bestilling for differansen.</span><span class="sxs-lookup"><span data-stu-id="94563-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="94563-160">Hvis du vil ha mer informasjon om innkjøpsrekvisisjoner, kan du se [Oversikt over innkjøpsrekvisisjon](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="94563-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>

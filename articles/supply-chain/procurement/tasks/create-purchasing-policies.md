---
title: Opprette innkjøpspolicyer
description: Dette emnet viser hvordan du oppretter innkjøpspolicyer som er tilpasset forretningsprosessene for innkjøp.
author: mkirknel
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e13a9a594e8c4041a586734df53321d57b43586
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204806"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="a76ff-103">Opprette innkjøpspolicyer</span><span class="sxs-lookup"><span data-stu-id="a76ff-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a76ff-104">Dette emnet viser hvordan du oppretter innkjøpspolicyer som er tilpasset forretningsprosessene for innkjøp.</span><span class="sxs-lookup"><span data-stu-id="a76ff-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="a76ff-105">Før du kan opprette innkjøpspolicyer, må du definere parametere for innkjøpspolicy.</span><span class="sxs-lookup"><span data-stu-id="a76ff-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="a76ff-106">Det er mulig å opprette, endre og avslutte en innkjøpspolicy, men du kan ikke slette en innkjøpspolicy.</span><span class="sxs-lookup"><span data-stu-id="a76ff-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="a76ff-107">Denne fremgangsmåten utføres vanligvis av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="a76ff-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="a76ff-108">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="a76ff-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="a76ff-109">Angi policyparametere</span><span class="sxs-lookup"><span data-stu-id="a76ff-109">Set up policy parameters</span></span>
1. <span data-ttu-id="a76ff-110">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Oppsett > Policyer > Innkjøpspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="a76ff-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="a76ff-111">Velg **Parametere** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a76ff-111">In the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="a76ff-112">Regler for policyprioritet gjelder for forskjellige nivåer i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="a76ff-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="a76ff-113">Organisasjonsenheter som vises avhengig av din organisasjonshierarkiet og på hvilke nivåer i hierarkiet de er tilordnet formålet Internkontroll av innkjøp.</span><span class="sxs-lookup"><span data-stu-id="a76ff-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="a76ff-114">Organisasjonen har for eksempel kanskje juridiske enheter, kostsentre, områder og avdelinger, men det kan hende at noen av disse har hierarkiformålet Internkontroll av innkjøp.</span><span class="sxs-lookup"><span data-stu-id="a76ff-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="a76ff-115">Organiseringen av typen Firma er tilgjengelig som standard.</span><span class="sxs-lookup"><span data-stu-id="a76ff-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="a76ff-116">Velg kategorien **Parametere for policyregeltype**.</span><span class="sxs-lookup"><span data-stu-id="a76ff-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="a76ff-117">I treet går du til **Velg Innkjøpspolicy > Kontrollregel for innkjøpsrekvisisjon**.</span><span class="sxs-lookup"><span data-stu-id="a76ff-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="a76ff-118">Du definerer prioritetsrekkefølgen for policyløsning på policynivået.</span><span class="sxs-lookup"><span data-stu-id="a76ff-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="a76ff-119">For enkelte policytyper kan du imidlertid overstyre prioritetsrekkefølgen for individuelle policyregeltyper.</span><span class="sxs-lookup"><span data-stu-id="a76ff-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="a76ff-120">La oss si at du vil definere prioritetsrekkefølgen for innkjøpspolicyer slik: kostsenter, avdeling, firma.</span><span class="sxs-lookup"><span data-stu-id="a76ff-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="a76ff-121">For katalogpolicyregelen vil du imidlertid at prioritetsrekkefølgen skal være: avdeling, kostsenter, firma.</span><span class="sxs-lookup"><span data-stu-id="a76ff-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="a76ff-122">Du kan endre prioritetsrekkefølgen for katalogpolicyregelen.</span><span class="sxs-lookup"><span data-stu-id="a76ff-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="a76ff-123">Når en arbeider oppretter en rekvisisjon, vil katalogen som vises, bestemmes av policyene som er knyttet til arbeiderens avdeling, deres kostsenter og deretter firmaet.</span><span class="sxs-lookup"><span data-stu-id="a76ff-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="a76ff-124">Hvis det ikke er oppført mer enn ett organisasjonsnivå, kan du bruke pil opp eller pil ned for å angi prioritetsrekkefølgen for Kontrollregel for innkjøpsrekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="a76ff-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="a76ff-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a76ff-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="a76ff-126">Opprett en ny policy</span><span class="sxs-lookup"><span data-stu-id="a76ff-126">Create a new policy</span></span>
1. <span data-ttu-id="a76ff-127">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a76ff-127">Select **New**.</span></span>
2. <span data-ttu-id="a76ff-128">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a76ff-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="a76ff-129">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a76ff-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="a76ff-130">Én enkelt innkjøpspolicy kan bare gjelde for ett organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="a76ff-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="a76ff-131">Du kan for eksempel ha ett hierarki som kalles Geografisk og ett som kalles Avdeling, og ha en forskjellig innkjøpspolicy for hver av dem.</span><span class="sxs-lookup"><span data-stu-id="a76ff-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="a76ff-132">Velg en organisasjon som policyen skal gjelde for.</span><span class="sxs-lookup"><span data-stu-id="a76ff-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="a76ff-133">Velg pilen for å legge til den valgte organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="a76ff-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="a76ff-134">Du kan gjenta denne prosessen for å legge til flere organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="a76ff-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="a76ff-135">Legge til en policyregel</span><span class="sxs-lookup"><span data-stu-id="a76ff-135">Add a policy rule</span></span>
1. <span data-ttu-id="a76ff-136">Velg **Regel for rekvisisjonsformål** i listen **Type policyregel**.</span><span class="sxs-lookup"><span data-stu-id="a76ff-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="a76ff-137">Du oppretter en regel som setter standardformål for rekvisisjonen til Forbruk, men tillater at Etterfylling-typen velges i stedet.</span><span class="sxs-lookup"><span data-stu-id="a76ff-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="a76ff-138">Velg **Opprett policyregel**.</span><span class="sxs-lookup"><span data-stu-id="a76ff-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="a76ff-139">Velg **Ja** i feltet **Tillat manuell overstyring**.</span><span class="sxs-lookup"><span data-stu-id="a76ff-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="a76ff-140">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="a76ff-140">Select **Close**.</span></span>
- <span data-ttu-id="a76ff-141">Nå kan du definere andre policyregler for innkjøpspolicyen.</span><span class="sxs-lookup"><span data-stu-id="a76ff-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="a76ff-142">Legg merke til at en policyregeltype ikke kan ha overlappende regler som er aktive samtidig i én enkelt innkjøpspolicy.</span><span class="sxs-lookup"><span data-stu-id="a76ff-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  


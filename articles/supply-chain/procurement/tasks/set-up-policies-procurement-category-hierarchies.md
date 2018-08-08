--- 
title: "Definere policyer for innkjøpskategorihierarkier"
description: "Bruk denne fremgangsmåten for å konfigurere regler for bestilling av produkter i en kategori."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a8f21599aec191c0358d919b501834677cda30ac
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="40e63-103">Definere policyer for innkjøpskategorihierarkier</span><span class="sxs-lookup"><span data-stu-id="40e63-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40e63-104">Bruk denne fremgangsmåten for å konfigurere regler for bestilling av produkter i en kategori.</span><span class="sxs-lookup"><span data-stu-id="40e63-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="40e63-105">Reglene er definert for en bestemt innkjøpspolicy.</span><span class="sxs-lookup"><span data-stu-id="40e63-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="40e63-106">Regelen for kategoritilgang kontrollerer hvilke innkjøpskategorier ansatte har tilgang til når de oppretter en rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="40e63-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="40e63-107">Når en rekvisisjon opprettes, avgjør systemet hvilken innkjøpspolicy og regel for kategoritilgang som gjelder, basert på den juridiske enheten og driftsenheten som den ansatte tilhører.</span><span class="sxs-lookup"><span data-stu-id="40e63-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="40e63-108">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="40e63-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="40e63-109">Denne oppgaven utføres vanligvis av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="40e63-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="40e63-110">Finne innkjøpspolicyen</span><span class="sxs-lookup"><span data-stu-id="40e63-110">Find the procurement policy</span></span>
1. <span data-ttu-id="40e63-111">Gå til Innkjøp og leverandører > Oppsett > Policyer > Innkjøpspolicyer.</span><span class="sxs-lookup"><span data-stu-id="40e63-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="40e63-112">Klikk koblingen på siden Policy for innkjøpspolicy for USMF.</span><span class="sxs-lookup"><span data-stu-id="40e63-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="40e63-113">Dette er policyen som du vil legge til en regel i.</span><span class="sxs-lookup"><span data-stu-id="40e63-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="40e63-114">Det må være en aktiv policy.</span><span class="sxs-lookup"><span data-stu-id="40e63-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="40e63-115">Opprette en regel for kategoritilgang</span><span class="sxs-lookup"><span data-stu-id="40e63-115">Create a category access rule</span></span>
1. <span data-ttu-id="40e63-116">Velg policyregelen for kategoritilgang.</span><span class="sxs-lookup"><span data-stu-id="40e63-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="40e63-117">Hvis knappen Opprett policyregel er nedtonet, er det fordi det allerede finnes en aktiv policyregel for kategoritilgang.</span><span class="sxs-lookup"><span data-stu-id="40e63-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="40e63-118">Kontroller feltene Gyldighetsdato og Utløpsdato for å finne ut hvilken det er, velg den og klikk Avslutt policyregel.</span><span class="sxs-lookup"><span data-stu-id="40e63-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="40e63-119">Hvis knappen Opprett policyregel er tilgjengelig, trenger du ikke gjøre noe.</span><span class="sxs-lookup"><span data-stu-id="40e63-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="40e63-120">Klikk Opprett policyregel.</span><span class="sxs-lookup"><span data-stu-id="40e63-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="40e63-121">Angi dato og klokkeslett i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="40e63-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="40e63-122">Tidspunktet må ikke overlappe med en annen regel som allerede er aktiv.</span><span class="sxs-lookup"><span data-stu-id="40e63-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="40e63-123">Velg en kategori som regelen skal gjelde for.</span><span class="sxs-lookup"><span data-stu-id="40e63-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="40e63-124">Merk deg hvilken kategori dette er. Du trenger det senere.</span><span class="sxs-lookup"><span data-stu-id="40e63-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="40e63-125">Når du velger en kategori, legges alle overordnede kategorier også til i listen Valgte kategorier.</span><span class="sxs-lookup"><span data-stu-id="40e63-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="40e63-126">Hvis du vil at regelen skal gjelde for alle underkategorier for den valgt kategorien, merker du av for Inkluder underkategorier.</span><span class="sxs-lookup"><span data-stu-id="40e63-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="40e63-127">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="40e63-127">Click Add.</span></span>
    * <span data-ttu-id="40e63-128">Hvis du vil sette alternativet Inkluder overordnet regel til Ja, vil policyregelen du konfigurerer for en overordnet kategori, også tilordnes de underordnede kategoriene hvis ingen policyregel er konfigurert for de underordnede kategoriene.</span><span class="sxs-lookup"><span data-stu-id="40e63-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="40e63-129">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="40e63-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="40e63-130">Opprette en policyregel for kategori</span><span class="sxs-lookup"><span data-stu-id="40e63-130">Create a category policy rule</span></span>
1. <span data-ttu-id="40e63-131">Velge kategoripolicyregel</span><span class="sxs-lookup"><span data-stu-id="40e63-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="40e63-132">Velg den aktive policyregelen hvis knappen Opprett policyregel er nedtonet, og klikk deretter Avslutt policyregel.</span><span class="sxs-lookup"><span data-stu-id="40e63-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="40e63-133">Klikk Opprett policyregel.</span><span class="sxs-lookup"><span data-stu-id="40e63-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="40e63-134">Angi dato og klokkeslett i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="40e63-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="40e63-135">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="40e63-135">Click Add.</span></span>
5. <span data-ttu-id="40e63-136">Velg den samme kategorien som du brukte for kategoritilgangsregelen.</span><span class="sxs-lookup"><span data-stu-id="40e63-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="40e63-137">Velg et alternativ i Leverandør-feltet.</span><span class="sxs-lookup"><span data-stu-id="40e63-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="40e63-138">Velg en regel for å kontrollere hvilke type leverandører som kan velges for kategorien når rekvisisjoner opprettes.</span><span class="sxs-lookup"><span data-stu-id="40e63-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="40e63-139">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="40e63-139">Click Close.</span></span>
    * <span data-ttu-id="40e63-140">Policyreglene du har definert, har vært for rekvisisjoner av typen Forbruk.</span><span class="sxs-lookup"><span data-stu-id="40e63-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="40e63-141">Hvis du vil definere policyer for rekvisisjoner av typen Etterfylling, kan du opprette en regel for policyregeltypen kalt Policyregel for tilgang til etterfyllingskategori.</span><span class="sxs-lookup"><span data-stu-id="40e63-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  



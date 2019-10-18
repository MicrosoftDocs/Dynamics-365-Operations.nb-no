---
title: Bølgetrinnkoder
description: Dette emnet inneholder en oversikt over bølgetrinnkoder og hvordan de brukes.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992363"
---
# <a name="wave-step-codes"></a><span data-ttu-id="1f8df-103">Bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="1f8df-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="1f8df-104">Om bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="1f8df-104">About wave step codes</span></span>

<span data-ttu-id="1f8df-105">Bølgetrinnkoder er koder som brukere kan definere og bruke til å koble bestemte forekomster av bølgemetoder til en tilsvarende mal.</span><span class="sxs-lookup"><span data-stu-id="1f8df-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="1f8df-106">Malene omfatter maler for etterfylling, containerbruk, etikettutskrift, lastplanlegging og sortering.</span><span class="sxs-lookup"><span data-stu-id="1f8df-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="1f8df-107">Når bølgetrinnkoder ikke brukes, må brukerne angi en fritekst for å referere til en bestemt mal fra den bølgemetodeforekomsten.</span><span class="sxs-lookup"><span data-stu-id="1f8df-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="1f8df-108">Fritekst er utsatt for feil fordi brukerne må passe på at bølgestrinnteksten de legger til en bølgemal for en bestemt bølgetrinnmetode, samsvarer nøyaktig med bølgetrinnteksten i målmalen.</span><span class="sxs-lookup"><span data-stu-id="1f8df-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="1f8df-109">Bølgetrinnkoder for en bestemt bølgetrinntype konfigureres på en egen side.</span><span class="sxs-lookup"><span data-stu-id="1f8df-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="1f8df-110">For alle bølgetrinnforekomster i en bølgemal som krever en bølgetrinnkode, må du velge bølgetrinnkoden i en rullegardinliste.</span><span class="sxs-lookup"><span data-stu-id="1f8df-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="1f8df-111">Valg i en rullegardinliste erstatter fritekstoppføring og reduserer risikoen og innvirkningen av menneskelig feil.</span><span class="sxs-lookup"><span data-stu-id="1f8df-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="1f8df-112">Oppsettkoder brukes til å koble en bølgetrinnmetode i en bølgemal til en målmal for metoden.</span><span class="sxs-lookup"><span data-stu-id="1f8df-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="1f8df-113">Bruk av funksjonen for bølgetrinnkoder er valgfri, og implementering er per juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="1f8df-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="1f8df-114">Hvis en bestemt juridisk enhet bruker funksjonen, oppgraderes derfor alle eksisterende bølgetrinnkoder i den juridiske enheten til den nye strukturen.</span><span class="sxs-lookup"><span data-stu-id="1f8df-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="1f8df-115">Installere demonstrasjon</span><span class="sxs-lookup"><span data-stu-id="1f8df-115">Setup demo</span></span> 

<span data-ttu-id="1f8df-116">For denne demonstrasjonen må demonstrasjons være installert, og du må bruke demonstrasjonsdataene for firmaet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="1f8df-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="1f8df-117">Aktiver bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="1f8df-117">Enable wave step codes</span></span>

<span data-ttu-id="1f8df-118">Følg disse trinnene for å aktivere funksjonen for bølgetrinnkoder.</span><span class="sxs-lookup"><span data-stu-id="1f8df-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="1f8df-119">Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="1f8df-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="1f8df-120">I kategorien **Generelt** i hurtigfanen **Bølgebehandling** setter du alternativet **Aktiver bølgetrinnkoder** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1f8df-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="1f8df-121">Alle eksisterende bølgetrinn i fritekst oppgraderes til den nye strukturen.</span><span class="sxs-lookup"><span data-stu-id="1f8df-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="1f8df-122">Når denne oppgraderingen er fullført for en juridisk enhet, er ikke alternativet **Aktiver bølgetrinnkoder** tilgjengelig på siden **Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="1f8df-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="1f8df-123">Valideringer utføres under oppgraderingen, og hvis oppgraderingen mislykkes, får du en feil melding.</span><span class="sxs-lookup"><span data-stu-id="1f8df-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="1f8df-124">En oppgradering kan mislykkes på grunn av følgende konflikter:</span><span class="sxs-lookup"><span data-stu-id="1f8df-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="1f8df-125">Det finnes duplisert bølgetrinn i fritekst.</span><span class="sxs-lookup"><span data-stu-id="1f8df-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="1f8df-126">Det finnes tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="1f8df-126">Customizations exist.</span></span>
- <span data-ttu-id="1f8df-127">Et bølgetrinn i fritekst som er knyttet til en bølgetrinnmetodeforekomst, samsvarer ikke med den forventede maltypen.</span><span class="sxs-lookup"><span data-stu-id="1f8df-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="1f8df-128">Når du har løst eventuelle konflikter som identifiseres i løpet av valideringene, kan du kjøre oppgraderingsprosessen på nytt.</span><span class="sxs-lookup"><span data-stu-id="1f8df-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="1f8df-129">Når oppgraderingen er fullført, blir siden **Bølgetrinnkoder** (**Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**) tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="1f8df-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="1f8df-130">Denne siden viser en liste over bølgetrinnkodene som ble oppgradert da funksjonen for bølgetrinnkoder ble aktivert.</span><span class="sxs-lookup"><span data-stu-id="1f8df-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="1f8df-131">Opprette nye bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="1f8df-131">Create new wave step codes</span></span>

<span data-ttu-id="1f8df-132">Du kan bruke siden **Bølgetrinnkoder** til å opprette og slette bølgetrinnkoder.</span><span class="sxs-lookup"><span data-stu-id="1f8df-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="1f8df-133">Alle nye bølgetrinnkoder og den tilknyttede ID-en, må være unike på tvers av alle bølgetrinntyper, og de må defineres for en bestemt bølgetrinntype.</span><span class="sxs-lookup"><span data-stu-id="1f8df-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="1f8df-134">Bruke bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="1f8df-134">Apply wave step codes</span></span>

<span data-ttu-id="1f8df-135">Når du har definert de aktuelle bølgetrinnkodene, kan de brukes på bølgeprosessmetodene.</span><span class="sxs-lookup"><span data-stu-id="1f8df-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="1f8df-136">Hvis du vil bruke bølgetrinnkoder, går du til den aktuelle målmalen.</span><span class="sxs-lookup"><span data-stu-id="1f8df-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="1f8df-137">Her er målmalene som bølgetrinnkodene peker på:</span><span class="sxs-lookup"><span data-stu-id="1f8df-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="1f8df-138">**Etterfyllingsmaler**: Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler</span><span class="sxs-lookup"><span data-stu-id="1f8df-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="1f8df-139">**Maler for lastplanlegging**: Lagerstyring \> Oppsett \> Last \> Maler for lastplanlegging</span><span class="sxs-lookup"><span data-stu-id="1f8df-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="1f8df-140">**Sorter maler** : Lagerstyring \> Oppsett \> Emballasje \> Utgående sorteringsmaler</span><span class="sxs-lookup"><span data-stu-id="1f8df-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="1f8df-141">**Maler for containerbruk**: Lagerstyring \> Oppsett \> Containere \> Maler for containerbygging</span><span class="sxs-lookup"><span data-stu-id="1f8df-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="1f8df-142">**Maler for etikettutskrift**: Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter</span><span class="sxs-lookup"><span data-stu-id="1f8df-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="1f8df-143">Malene i denne listen brukes når de refereres fra en bølgeprosessmetode som er valgt i en bølgemal.</span><span class="sxs-lookup"><span data-stu-id="1f8df-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="1f8df-144">Når bølgetrinnkoden for bølgeprosessmetode i en bølgemal samsvarer med bølgetrinnkoden i én av maltypene, brukes malen.</span><span class="sxs-lookup"><span data-stu-id="1f8df-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="1f8df-145">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="1f8df-145">Sample scenario</span></span>

<span data-ttu-id="1f8df-146">Fremgangsmåten nedenfor hjelper deg med å garantere at etterfyllings malen du opprettet, brukes for bølgemalen.</span><span class="sxs-lookup"><span data-stu-id="1f8df-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="1f8df-147">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**, og opprett en bølgetrinnkode for typen **Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="1f8df-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="1f8df-148">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler**, og opprett en etterfyllingsmal.</span><span class="sxs-lookup"><span data-stu-id="1f8df-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="1f8df-149">I etterfyllingsmalen velger du bølgetrinnkoden du opprettet for typen **Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="1f8df-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="1f8df-150">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**, og velg bølgemalen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="1f8df-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="1f8df-151">I hurtigfanen **Metoder** i malen, velger du metoden **Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="1f8df-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="1f8df-152">I feltet **Bølgetrinnkode** velger du bølgetrinnkoden du valgte i etterfyllingsmalen.</span><span class="sxs-lookup"><span data-stu-id="1f8df-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

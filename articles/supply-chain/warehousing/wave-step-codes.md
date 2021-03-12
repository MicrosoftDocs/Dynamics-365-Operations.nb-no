---
title: Bølgetrinnkoder
description: Dette emnet inneholder en oversikt over bølgetrinnkoder og hvordan de brukes.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 08b40c076e288592f6a4cd628b9acd8a2eaedb7e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998409"
---
# <a name="wave-step-codes"></a><span data-ttu-id="2d186-103">Bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="2d186-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d186-104">Bølgetrinnkoder er koder som brukere kan definere og bruke til å koble bestemte forekomster av bølgemetoder til en tilsvarende mal.</span><span class="sxs-lookup"><span data-stu-id="2d186-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="2d186-105">Malene omfatter maler for etterfylling, containerbruk, etikettutskrift, lastplanlegging og sortering.</span><span class="sxs-lookup"><span data-stu-id="2d186-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="2d186-106">Når bølgetrinnkoder ikke brukes, må brukerne angi en fritekst for å referere til en bestemt mal fra den bølgemetodeforekomsten.</span><span class="sxs-lookup"><span data-stu-id="2d186-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="2d186-107">Fritekst er utsatt for feil fordi brukerne må passe på at bølgestrinnteksten de legger til en bølgemal for en bestemt bølgetrinnmetode, samsvarer nøyaktig med bølgetrinnteksten i målmalen.</span><span class="sxs-lookup"><span data-stu-id="2d186-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="2d186-108">Bølgetrinnkoder for en bestemt bølgetrinntype konfigureres på en egen side.</span><span class="sxs-lookup"><span data-stu-id="2d186-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="2d186-109">For alle bølgetrinnforekomster i en bølgemal som krever en bølgetrinnkode, må du velge bølgetrinnkoden i en rullegardinliste.</span><span class="sxs-lookup"><span data-stu-id="2d186-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="2d186-110">Valg i en rullegardinliste erstatter fritekstoppføring og reduserer risikoen og innvirkningen av menneskelig feil.</span><span class="sxs-lookup"><span data-stu-id="2d186-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="2d186-111">Oppsettkoder brukes til å koble en bølgetrinnmetode i en bølgemal til en målmal for metoden.</span><span class="sxs-lookup"><span data-stu-id="2d186-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="2d186-112">Bruk av bølgetrinnkoder-funksjonen er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="2d186-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="2d186-113">Den er aktivert i hele organisasjonen for alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="2d186-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="2d186-114">Installere demonstrasjon</span><span class="sxs-lookup"><span data-stu-id="2d186-114">Setup demo</span></span> 

<span data-ttu-id="2d186-115">For denne demonstrasjonen må demonstrasjons være installert, og du må bruke demonstrasjonsdataene for firmaet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="2d186-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="2d186-116">Aktiver bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="2d186-116">Enable wave step codes</span></span>

<span data-ttu-id="2d186-117">Følg disse trinnene for å aktivere funksjonen for bølgetrinnkoder.</span><span class="sxs-lookup"><span data-stu-id="2d186-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="2d186-118">Gå til **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="2d186-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="2d186-119">Velg dette for å aktivere funksjonen kalt **Organisasjonsomfattende bølgetrinnkode**.</span><span class="sxs-lookup"><span data-stu-id="2d186-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="2d186-120">Alle eksisterende bølgetrinn i fritekst i alle juridiske enheter oppgraderes til den nye strukturen.</span><span class="sxs-lookup"><span data-stu-id="2d186-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="2d186-121">Når denne oppgraderingen er fullført for alle juridiske enheter, er funksjonen aktivert.</span><span class="sxs-lookup"><span data-stu-id="2d186-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="2d186-122">Hvis funksjonen ikke kan aktiveres for én eller flere juridiske enheter, er ikke funksjonen aktivert for noen juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="2d186-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="2d186-123">Under aktivering utføres valideringer under dataoppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="2d186-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="2d186-124">Hvis oppgraderingen mislykkes, får du en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="2d186-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="2d186-125">En oppgradering kan mislykkes på grunn av følgende konflikter:</span><span class="sxs-lookup"><span data-stu-id="2d186-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="2d186-126">Det finnes duplisert bølgetrinn i fritekst.</span><span class="sxs-lookup"><span data-stu-id="2d186-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="2d186-127">Det finnes tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="2d186-127">Customizations exist.</span></span>
- <span data-ttu-id="2d186-128">Et bølgetrinn i fritekst som er knyttet til en bølgetrinnmetodeforekomst, samsvarer ikke med den forventede maltypen.</span><span class="sxs-lookup"><span data-stu-id="2d186-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="2d186-129">Når du har løst eventuelle konflikter som identifiseres i løpet av valideringene, kan du prøve å aktivere funksjonen på nytt.</span><span class="sxs-lookup"><span data-stu-id="2d186-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="2d186-130">Når funksjonen er aktivert, blir siden **Bølgetrinnkoder** (**Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**) tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="2d186-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="2d186-131">Denne siden viser en liste over bølgetrinnkodene som ble oppgradert da funksjonen Organisasjonsomfattende bølgetrinnkode ble aktivert.</span><span class="sxs-lookup"><span data-stu-id="2d186-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="2d186-132">Opprette nye bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="2d186-132">Create new wave step codes</span></span>

<span data-ttu-id="2d186-133">Du kan bruke siden **Bølgetrinnkoder** til å opprette og slette bølgetrinnkoder.</span><span class="sxs-lookup"><span data-stu-id="2d186-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="2d186-134">Alle nye bølgetrinnkoder og den tilknyttede ID-en, må være unike på tvers av alle bølgetrinntyper, og de må defineres for en bestemt bølgetrinntype.</span><span class="sxs-lookup"><span data-stu-id="2d186-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="2d186-135">Bruke bølgetrinnkoder</span><span class="sxs-lookup"><span data-stu-id="2d186-135">Apply wave step codes</span></span>

<span data-ttu-id="2d186-136">Når du har definert de aktuelle bølgetrinnkodene, kan de brukes på bølgeprosessmetodene.</span><span class="sxs-lookup"><span data-stu-id="2d186-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="2d186-137">Hvis du vil bruke bølgetrinnkoder, går du til den aktuelle målmalen.</span><span class="sxs-lookup"><span data-stu-id="2d186-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="2d186-138">Her er målmalene som bølgetrinnkodene peker på:</span><span class="sxs-lookup"><span data-stu-id="2d186-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="2d186-139">**Etterfyllingsmaler**: Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler</span><span class="sxs-lookup"><span data-stu-id="2d186-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="2d186-140">**Maler for lastplanlegging**: Lagerstyring \> Oppsett \> Last \> Maler for lastplanlegging</span><span class="sxs-lookup"><span data-stu-id="2d186-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="2d186-141">**Sorter maler** : Lagerstyring \> Oppsett \> Emballasje \> Utgående sorteringsmaler</span><span class="sxs-lookup"><span data-stu-id="2d186-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="2d186-142">**Maler for containerbruk**: Lagerstyring \> Oppsett \> Containere \> Maler for containerbygging</span><span class="sxs-lookup"><span data-stu-id="2d186-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="2d186-143">**Maler for etikettutskrift**: Lagerstyring \> Oppsett \> Dokumentruting \> Maler for bølgeetiketter</span><span class="sxs-lookup"><span data-stu-id="2d186-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="2d186-144">Malene i denne listen brukes når de refereres fra en bølgeprosessmetode som er valgt i en bølgemal.</span><span class="sxs-lookup"><span data-stu-id="2d186-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="2d186-145">Når bølgetrinnkoden for bølgeprosessmetode i en bølgemal samsvarer med bølgetrinnkoden i én av maltypene, brukes malen.</span><span class="sxs-lookup"><span data-stu-id="2d186-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="2d186-146">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="2d186-146">Sample scenario</span></span>

<span data-ttu-id="2d186-147">Fremgangsmåten nedenfor hjelper deg med å garantere at etterfyllings malen du opprettet, brukes for bølgemalen.</span><span class="sxs-lookup"><span data-stu-id="2d186-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="2d186-148">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**, og opprett en bølgetrinnkode for typen **Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="2d186-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="2d186-149">Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler**, og opprett en etterfyllingsmal.</span><span class="sxs-lookup"><span data-stu-id="2d186-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="2d186-150">I etterfyllingsmalen velger du bølgetrinnkoden du opprettet for typen **Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="2d186-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="2d186-151">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**, og velg bølgemalen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="2d186-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="2d186-152">I hurtigfanen **Metoder** i malen, velger du metoden **Etterfylling**.</span><span class="sxs-lookup"><span data-stu-id="2d186-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="2d186-153">I feltet **Bølgetrinnkode** velger du bølgetrinnkoden du valgte i etterfyllingsmalen.</span><span class="sxs-lookup"><span data-stu-id="2d186-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="2d186-154">Du utfører disse trinnene for hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="2d186-154">You perform these steps for each legal entity.</span></span>

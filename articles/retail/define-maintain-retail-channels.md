---
title: Definere og vedlikeholde detaljhandelskanaler
description: "Denne artikkelen inneholder en oversikt over prosessen for å definere bankens fysiske butikker, som kalles detaljhandelsbutikker i Microsoft Dynamics 365 for Retail. Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert en detaljhandelsbutikk."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a78df20ce5a9ff0aae7b2b3e93d00c46f747f07
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="e16e0-104">Definere og vedlikeholde detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="e16e0-104">Define and maintain retail channels</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e16e0-105">Denne artikkelen inneholder en oversikt over prosessen for å definere bankens fysiske butikker, som kalles detaljhandelsbutikker i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e16e0-105">This article provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="e16e0-106">Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert en detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="e16e0-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="e16e0-107">Dynamics 365 for Retail støtter flere detaljhandelskanaler, for eksempel nettbutikker, telefonsentre og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="e16e0-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="e16e0-108">En fysisk butikk kalles detaljhandelbutikk.</span><span class="sxs-lookup"><span data-stu-id="e16e0-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="e16e0-109">Hver detaljhandelsbutikk kan ha sine egne betalingsmåter, prisgrupper, salgsstedskasser, inntekts- og utgiftskontoer og ansatte.</span><span class="sxs-lookup"><span data-stu-id="e16e0-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="e16e0-110">Du må definere alle disse elementene for en detaljhandelsbutikk, før du oppretter den.</span><span class="sxs-lookup"><span data-stu-id="e16e0-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="e16e0-111">Når du har opprettet en detaljhandelsbutikk, tilordner du produktene du vil den skal føre.</span><span class="sxs-lookup"><span data-stu-id="e16e0-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="e16e0-112">Du tilordner også ansatte, kasser og kunder til butikken.</span><span class="sxs-lookup"><span data-stu-id="e16e0-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="e16e0-113">Til slutt legger du til den nye butikken i et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="e16e0-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="e16e0-114">Definere detaljhandelsbutikker</span><span class="sxs-lookup"><span data-stu-id="e16e0-114">Setting up retail stores</span></span>
<span data-ttu-id="e16e0-115">Før du kan definere en detaljhandelsbutikk i Dynamics 365 for Retail, må du fullføre noen nødvendige oppgaver.</span><span class="sxs-lookup"><span data-stu-id="e16e0-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="e16e0-116">Du kan deretter opprette detaljhandelsbutikken og legge til detaljer.</span><span class="sxs-lookup"><span data-stu-id="e16e0-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e16e0-117">Nødvendig programvare</span><span class="sxs-lookup"><span data-stu-id="e16e0-117">Prerequisites</span></span>

<span data-ttu-id="e16e0-118">Du må fullføre følgende oppgaver før du kan definere en detaljhandelsbutikk:</span><span class="sxs-lookup"><span data-stu-id="e16e0-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="e16e0-119">Konfigurer organisasjonsstrukturen, og definer organisasjonshierarkier for detaljhandelssortimenter, -etterfylling og -rapportering.</span><span class="sxs-lookup"><span data-stu-id="e16e0-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="e16e0-120">Definere et lager som representerer detaljhandelsbutikken.</span><span class="sxs-lookup"><span data-stu-id="e16e0-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="e16e0-121">Definer nummerserier for detaljhandelsbutikker, butikkutdrag og utdragsbilag.</span><span class="sxs-lookup"><span data-stu-id="e16e0-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="e16e0-122">Konfigurer parametere for Detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="e16e0-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="e16e0-123">Definer betalingsmåtene butikken godtar.</span><span class="sxs-lookup"><span data-stu-id="e16e0-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="e16e0-124">Hvis du vil behandle kredittkorttransaksjoner i kasser på salgssteder, kan du også konfigurere betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="e16e0-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="e16e0-125">Definer mva-grupper.</span><span class="sxs-lookup"><span data-stu-id="e16e0-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="e16e0-126">Definer detaljprodukter.</span><span class="sxs-lookup"><span data-stu-id="e16e0-126">Set up retail products.</span></span> <span data-ttu-id="e16e0-127">Som en del av denne oppgaven definerer du også detaljprodukthierarkier, produktvarianter og produktsortimenter.</span><span class="sxs-lookup"><span data-stu-id="e16e0-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="e16e0-128">Definer produktgrupper.</span><span class="sxs-lookup"><span data-stu-id="e16e0-128">Set up product price groups.</span></span>
10. <span data-ttu-id="e16e0-129">Definer produktpriser for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="e16e0-129">Set up retail product pricing.</span></span> <span data-ttu-id="e16e0-130">Som en del av denne oppgaven definerer du også prisjusteringer, rabatter og rabattperioder.</span><span class="sxs-lookup"><span data-stu-id="e16e0-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="e16e0-131">Definere stabsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e16e0-131">Set up staff members.</span></span> <span data-ttu-id="e16e0-132">**Obs!** Du må også tilordne aktuelle tillatelser til arbeiderne, slik at de kan logge på og utføre oppgaver ved hjelp av Dynamics 365 for Retail for Retail POS-systemet.</span><span class="sxs-lookup"><span data-stu-id="e16e0-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="e16e0-133">Konfigurer Retail POS-profilene som skal tilordnes butikken.</span><span class="sxs-lookup"><span data-stu-id="e16e0-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="e16e0-134">Denne oppgaven omfatter mange andre oppgaver, for eksempel å definere kasser, definere frakoblede profiler og definere kvitteringsformater og -profiler.</span><span class="sxs-lookup"><span data-stu-id="e16e0-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="e16e0-135">Se gjennom alle oppgavene som er inkludert i forutsetningen, og fullfør bare de oppgavene som gjelder for deg.</span><span class="sxs-lookup"><span data-stu-id="e16e0-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="e16e0-136">Angi en detaljhandelsbutikk</span><span class="sxs-lookup"><span data-stu-id="e16e0-136">Set up a retail store</span></span>

<span data-ttu-id="e16e0-137">Når du har fullført de nødvendige oppgavene, må du fullføre disse oppgavene for å definere detaljene for detaljhandelsbutikken:</span><span class="sxs-lookup"><span data-stu-id="e16e0-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="e16e0-138">Opprett en detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="e16e0-138">Create a retail store.</span></span>
2.  <span data-ttu-id="e16e0-139">Tilordne en mva-gruppe til butikken.</span><span class="sxs-lookup"><span data-stu-id="e16e0-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="e16e0-140">Tilordne de godtatte betalingsmåtene til butikken.</span><span class="sxs-lookup"><span data-stu-id="e16e0-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="e16e0-141">Legg til detaljer i produktbeskrivelsene for produkter du tilbyr i detaljhandelsbutikkene.</span><span class="sxs-lookup"><span data-stu-id="e16e0-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="e16e0-142">Du kan for eksempel legge til rik tekst og bilder.</span><span class="sxs-lookup"><span data-stu-id="e16e0-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="e16e0-143">Disse produktdetaljene vises i ulike kontekster, for eksempel på kassen på salgsstedet eller på utskrevne etiketter.</span><span class="sxs-lookup"><span data-stu-id="e16e0-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="e16e0-144">Legg til butikken som standard organisasjonshierarki som er tilordnet formålet **Detaljhandelsortiment**, **Detaljhandeletterfylling** eller **Detaljhandelsrapportering**.</span><span class="sxs-lookup"><span data-stu-id="e16e0-144">Add the store to an the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="e16e0-145">Når du har opprettet en detaljhandelsbutikk</span><span class="sxs-lookup"><span data-stu-id="e16e0-145">After you set up a retail store</span></span>

<span data-ttu-id="e16e0-146">Når du har angitt detaljene for detaljhandelsbutikken, fullfører du disse oppgavene for å sende de nye dataene for detaljhandelsbutikken til Retail POS:</span><span class="sxs-lookup"><span data-stu-id="e16e0-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="e16e0-147">Konfigurer salgsstedskassene for butikken.</span><span class="sxs-lookup"><span data-stu-id="e16e0-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="e16e0-148">Tilordne produktsortimenter til butikken.</span><span class="sxs-lookup"><span data-stu-id="e16e0-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="e16e0-149">Behandle sortimenter for å generere listen over produkter som er inkludert i sortimentet og gjøre varene tilgjengelige i detaljhandelsbutikken.</span><span class="sxs-lookup"><span data-stu-id="e16e0-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="e16e0-150">Sende data, for eksempel nummerserier, maskinvareprofiler, og skjermoppsett for salgssted til Retail POS-kassene.</span><span class="sxs-lookup"><span data-stu-id="e16e0-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="e16e0-151">Publiser detaljhandelsbutikken hvis du vil sende butikkdata til Retail POS.</span><span class="sxs-lookup"><span data-stu-id="e16e0-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="e16e0-152">Kjør jobbene for å sende butikkdataene til Retail POS.</span><span class="sxs-lookup"><span data-stu-id="e16e0-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="e16e0-153">Organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="e16e0-153">Organization hierarchies</span></span>
<span data-ttu-id="e16e0-154">Retail bruker organisasjonshierarkier til å strukturere detaljhandelskanaler.</span><span class="sxs-lookup"><span data-stu-id="e16e0-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="e16e0-155">Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.</span><span class="sxs-lookup"><span data-stu-id="e16e0-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="e16e0-156">Når du definerer butikker, kan du legge dem til i et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="e16e0-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="e16e0-157">Butikken lagrer og deler data som brukes for sortimenter, etterfylling og rapportering.</span><span class="sxs-lookup"><span data-stu-id="e16e0-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>





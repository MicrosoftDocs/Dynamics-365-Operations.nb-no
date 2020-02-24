---
title: Definere og vedlikeholde detaljhandelskanaler
description: Dette emnet inneholder en oversikt over prosessen for å definere bankens fysiske butikker, som kalles butikker i Dynamics 365 Commerce. Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert en butikk.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 63639d69af90c6aa37bbf7af7868bca71942063f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023503"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="38417-104">Definere og vedlikeholde detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="38417-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38417-105">Dette emnet inneholder en oversikt over prosessen for å definere bankens fysiske butikker, som kalles butikker i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="38417-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="38417-106">Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert en butikk.</span><span class="sxs-lookup"><span data-stu-id="38417-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="38417-107">Handel støtter flere kanaler, for eksempel nettbutikker, telefonsentre og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="38417-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="38417-108">En fysisk butikk kalles en butikk.</span><span class="sxs-lookup"><span data-stu-id="38417-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="38417-109">Hver butikk kan ha sine egne betalingsmåter, prisgrupper, salgsstedskasser, inntekts- og utgiftskontoer og ansatte.</span><span class="sxs-lookup"><span data-stu-id="38417-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="38417-110">Du må definere alle disse elementene for en butikk, før du oppretter den.</span><span class="sxs-lookup"><span data-stu-id="38417-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="38417-111">Når du har opprettet en butikk, tilordner du produktene du vil den skal føre.</span><span class="sxs-lookup"><span data-stu-id="38417-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="38417-112">Du tilordner også ansatte, kasser og kunder til butikken.</span><span class="sxs-lookup"><span data-stu-id="38417-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="38417-113">Til slutt legger du til den nye butikken i et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="38417-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="38417-114">Sette opp butikker</span><span class="sxs-lookup"><span data-stu-id="38417-114">Setting up stores</span></span>

<span data-ttu-id="38417-115">Før du kan definere en butikk i Handel, må du fullføre noen nødvendige oppgaver.</span><span class="sxs-lookup"><span data-stu-id="38417-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="38417-116">Du kan deretter opprette butikken og legge til detaljer.</span><span class="sxs-lookup"><span data-stu-id="38417-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="38417-117">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="38417-117">Prerequisites</span></span>

<span data-ttu-id="38417-118">Du må fullføre følgende oppgaver før du kan definere en butikk:</span><span class="sxs-lookup"><span data-stu-id="38417-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="38417-119">Konfigurer organisasjonsstrukturen, og definer organisasjonshierarkier for detaljhandelssortimenter, -etterfylling og -rapportering.</span><span class="sxs-lookup"><span data-stu-id="38417-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="38417-120">Definere et lager som representerer butikken.</span><span class="sxs-lookup"><span data-stu-id="38417-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="38417-121">Definer nummerserier for butikker, butikkutdrag og utdragsbilag.</span><span class="sxs-lookup"><span data-stu-id="38417-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="38417-122">Konfigurer parametere for Handel.</span><span class="sxs-lookup"><span data-stu-id="38417-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="38417-123">Definer betalingsmåtene butikken godtar.</span><span class="sxs-lookup"><span data-stu-id="38417-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="38417-124">Hvis du vil behandle kredittkorttransaksjoner i kasser på salgssteder, kan du også konfigurere betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="38417-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="38417-125">Definer mva-grupper.</span><span class="sxs-lookup"><span data-stu-id="38417-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="38417-126">Definer detaljprodukter.</span><span class="sxs-lookup"><span data-stu-id="38417-126">Set up retail products.</span></span> <span data-ttu-id="38417-127">Som en del av denne oppgaven definerer du også produkthierarkier, produktvarianter og produktsortimenter.</span><span class="sxs-lookup"><span data-stu-id="38417-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="38417-128">Definer produktgrupper.</span><span class="sxs-lookup"><span data-stu-id="38417-128">Set up product price groups.</span></span>
10. <span data-ttu-id="38417-129">Sett opp produktprising.</span><span class="sxs-lookup"><span data-stu-id="38417-129">Set up product pricing.</span></span> <span data-ttu-id="38417-130">Som en del av denne oppgaven definerer du også prisjusteringer, rabatter og rabattperioder.</span><span class="sxs-lookup"><span data-stu-id="38417-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="38417-131">Definere stabsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="38417-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="38417-132">Du må også tilordne aktuelle tillatelser til arbeiderne, slik at de kan logge på og utføre oppgaver ved hjelp av salgsstedssystemet.</span><span class="sxs-lookup"><span data-stu-id="38417-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="38417-133">Konfigurer salgsstedsprofiler som skal tilordnes butikken.</span><span class="sxs-lookup"><span data-stu-id="38417-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="38417-134">Denne oppgaven omfatter mange andre oppgaver, for eksempel å definere kasser, definere frakoblede profiler og definere kvitteringsformater og -profiler.</span><span class="sxs-lookup"><span data-stu-id="38417-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="38417-135">Se gjennom alle oppgavene som er inkludert i forutsetningene, og fullfør bare de oppgavene som gjelder for deg.</span><span class="sxs-lookup"><span data-stu-id="38417-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="38417-136">Sette opp en butikk</span><span class="sxs-lookup"><span data-stu-id="38417-136">Set up a store</span></span>

<span data-ttu-id="38417-137">Når du har fullført de nødvendige oppgavene, må du fullføre disse oppgavene for å definere detaljene for butikken:</span><span class="sxs-lookup"><span data-stu-id="38417-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="38417-138">Opprett en butikk.</span><span class="sxs-lookup"><span data-stu-id="38417-138">Create a store.</span></span>
2. <span data-ttu-id="38417-139">Tilordne en mva-gruppe til butikken.</span><span class="sxs-lookup"><span data-stu-id="38417-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="38417-140">Tilordne de godtatte betalingsmåtene til butikken.</span><span class="sxs-lookup"><span data-stu-id="38417-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="38417-141">Legg til detaljer i produktbeskrivelsene for produkter du tilbyr i butikkene.</span><span class="sxs-lookup"><span data-stu-id="38417-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="38417-142">Du kan for eksempel legge til rik tekst og bilder.</span><span class="sxs-lookup"><span data-stu-id="38417-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="38417-143">Disse produktdetaljene vises i ulike kontekster, for eksempel på kassen på salgsstedet eller på utskrevne etiketter.</span><span class="sxs-lookup"><span data-stu-id="38417-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="38417-144">Legg til butikken som standard organisasjonshierarki som er tilordnet formålet **Detaljhandelsortiment**, **Detaljhandeletterfylling** eller **Detaljhandelsrapportering**.</span><span class="sxs-lookup"><span data-stu-id="38417-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="38417-145">Etter at du har satt opp en butikk</span><span class="sxs-lookup"><span data-stu-id="38417-145">After you set up a store</span></span>

<span data-ttu-id="38417-146">Når du har angitt detaljene for butikken, fullfører du disse oppgavene for å sende dataene for den nye butikken til salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="38417-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="38417-147">Konfigurer salgsstedskassene for butikken.</span><span class="sxs-lookup"><span data-stu-id="38417-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="38417-148">Tilordne produktsortimenter til butikken.</span><span class="sxs-lookup"><span data-stu-id="38417-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="38417-149">Behandle sortimenter for å generere listen over produkter som er inkludert i sortimentet og gjøre varene tilgjengelige i butikken.</span><span class="sxs-lookup"><span data-stu-id="38417-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="38417-150">Sende data, for eksempel nummerserier, maskinvareprofiler, og skjermoppsett for salgssted til salgsstedskassene.</span><span class="sxs-lookup"><span data-stu-id="38417-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="38417-151">Publiser butikken hvis du vil sende butikkdata til salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="38417-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="38417-152">Kjør jobbene for å sende butikkdataene til salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="38417-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="38417-153">Organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="38417-153">Organization hierarchies</span></span>

<span data-ttu-id="38417-154">Handel bruker organisasjonshierarkier til å strukturere kanaler.</span><span class="sxs-lookup"><span data-stu-id="38417-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="38417-155">Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.</span><span class="sxs-lookup"><span data-stu-id="38417-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="38417-156">Når du definerer butikker, kan du legge dem til i et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="38417-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="38417-157">Butikken lagrer og deler data som brukes for sortimenter, etterfylling og rapportering.</span><span class="sxs-lookup"><span data-stu-id="38417-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="38417-158">Konfigurasjonsnøkkelen for **Flere forsendelsesadresser** må være aktivert for å bruke funksjonalitet for detaljhandelsalg.</span><span class="sxs-lookup"><span data-stu-id="38417-158">To use Retail sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="38417-159">Denne konfigurasjonsnøkkelen kan finnes i nøklene for **Handelskonfigurasjon** under **Systemadministrasjon**\> **Oppsett** \> **Lisenskonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="38417-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="38417-160">Dette er nødvendig på grunn av Retail-funksjonalitet som utfører forskjellige valideringer basert på leveringsadressen som er konfigurert på salgsordrelinjenivå.</span><span class="sxs-lookup"><span data-stu-id="38417-160">This is required due to Retail functionality that performs various validations based on the delivery address configured at the sales order line level.</span></span>


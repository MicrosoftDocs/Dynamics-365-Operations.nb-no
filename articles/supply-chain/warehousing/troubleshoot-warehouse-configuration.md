---
title: Feilsøk lagerkonfigurasjon
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du konfigurerer Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 09b5770190fea9591f422b61ce6deedb2b9fa790
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994009"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="79e74-103">Feilsøk lagerkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="79e74-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79e74-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du konfigurerer Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="79e74-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="79e74-105">Jeg får følgende feilmelding: Nummerskiltet eller lokasjonen er ugyldig.</span><span class="sxs-lookup"><span data-stu-id="79e74-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e74-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="79e74-106">Issue description</span></span>

<span data-ttu-id="79e74-107">Du får denne feilmeldingen når du skanner en nummerskilt-ID eller lokasjon.</span><span class="sxs-lookup"><span data-stu-id="79e74-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e74-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="79e74-108">Issue resolution</span></span>

<span data-ttu-id="79e74-109">Pass på at nummerskilt-ID-en ikke er reserver av noe annet.</span><span class="sxs-lookup"><span data-stu-id="79e74-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="79e74-110">Dette problemet oppstod tidligere når verdien som en bruker skannet i lagerappen, var både en gyldig lokasjon og en gyldig nummerskilt-ID.</span><span class="sxs-lookup"><span data-stu-id="79e74-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="79e74-111">Dette problemet ble imidlertid løst i versjon 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="79e74-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="79e74-112">Jeg får følgende feilmelding: Nummerskilt må angis for denne lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="79e74-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e74-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="79e74-113">Issue description</span></span>

<span data-ttu-id="79e74-114">Du får denne feilmeldingen hvis du oppretter en overføringsordre ved hjelp av et lager som er aktivert for avansert lagerstyring (WMS), og etter at arbeidet er fullført, prøver du å bekrefte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="79e74-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e74-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="79e74-115">Issue resolution</span></span>

<span data-ttu-id="79e74-116">Feltet **Standard mottakssted** er tomt for et transittlager i fra-lageret.</span><span class="sxs-lookup"><span data-stu-id="79e74-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="79e74-117">Du kan løse dette problemet ved å angi en standard mottakssted i transittlageret.</span><span class="sxs-lookup"><span data-stu-id="79e74-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="79e74-118">Kontroller at denne plasseringen er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="79e74-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="79e74-119">Jeg får følgende feilmelding: Du kan ikke opprette en arbeidsmallinje for lagerstatusendring fordi arbeidstypen ikke er gyldig.</span><span class="sxs-lookup"><span data-stu-id="79e74-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="79e74-120">Velg en annen arbeidstype.</span><span class="sxs-lookup"><span data-stu-id="79e74-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e74-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="79e74-121">Issue description</span></span>

<span data-ttu-id="79e74-122">Du kan ikke velge *Lagerstatusendring* i **Arbeidstype**-kolonnen i delen **Arbeidsmaldetaljer**.</span><span class="sxs-lookup"><span data-stu-id="79e74-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e74-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="79e74-123">Issue resolution</span></span>

<span data-ttu-id="79e74-124">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="79e74-124">This behavior is by design.</span></span> <span data-ttu-id="79e74-125">Arbeidstypen *Lagerstatusendring* brukes bare av systemprosesser.</span><span class="sxs-lookup"><span data-stu-id="79e74-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="79e74-126">Den kan ikke konfigureres.</span><span class="sxs-lookup"><span data-stu-id="79e74-126">It can't be configured.</span></span> <span data-ttu-id="79e74-127">Fordi listen over arbeidstyper er fast som en opplisting, kan ikke de ekstra postene filtreres ut fra rullegardinmenyen **Arbeidstype**.</span><span class="sxs-lookup"><span data-stu-id="79e74-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="79e74-128">Jeg får følgende feilmelding: Antallet er ikke gyldig for enhet 1%.</span><span class="sxs-lookup"><span data-stu-id="79e74-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e74-129">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="79e74-129">Issue description</span></span>

<span data-ttu-id="79e74-130">Antallet er ikke gyldig for *ea*-enheten når det er et plukkarbeid som har flere nummerskilter på ett sted.</span><span class="sxs-lookup"><span data-stu-id="79e74-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e74-131">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="79e74-131">Issue resolution</span></span>

<span data-ttu-id="79e74-132">Kontroller at feltene **Sekvensgruppe-ID for enhet** og **Enhetskonverteringer** i frigitt produkt eller produktvariant er riktig angitt.</span><span class="sxs-lookup"><span data-stu-id="79e74-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="79e74-133">Legg merke til at feilmeldingen er forbedret i versjon 10.0.15 (se [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="79e74-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="79e74-134">Den nye feilmeldingen er Antallet er ikke gyldig.</span><span class="sxs-lookup"><span data-stu-id="79e74-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="79e74-135">Forventet %1 %2.</span><span class="sxs-lookup"><span data-stu-id="79e74-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="79e74-136">I lokasjonsdirektiver for plasseringsarbeid for salgsordre evaluerer ikke alternativet flere SKU-er flere lokasjonsdirektivhandlinger.</span><span class="sxs-lookup"><span data-stu-id="79e74-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e74-137">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="79e74-137">Issue description</span></span>

<span data-ttu-id="79e74-138">Lokasjonsdirektiver for *Salgsordre*-arbeidsordretypen og *Plasser*-arbeidstypen evaluerer ikke fler lokasjonsdirektivhandlinger når det **Flere SKU-er** er valgt.</span><span class="sxs-lookup"><span data-stu-id="79e74-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="79e74-139">Bare den første lokasjonsdirektivhandlingen evalueres.</span><span class="sxs-lookup"><span data-stu-id="79e74-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e74-140">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="79e74-140">Issue resolution</span></span>

<span data-ttu-id="79e74-141">En ny funksjon, *Evaluere alle handlinger for lokasjonsdirektiver med flere SKU-er*, er lagt til i versjon 10.0.15 (se [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="79e74-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="79e74-142">Denne funksjonen evaluerer alle handlinger for lokasjonsdirektiver med flere SKU-er.</span><span class="sxs-lookup"><span data-stu-id="79e74-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="79e74-143">Hvis du trenger denne funksjonen, kan du bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere den.</span><span class="sxs-lookup"><span data-stu-id="79e74-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="79e74-144">Jeg kan ikke bruke lagerappen til delvis plukking.</span><span class="sxs-lookup"><span data-stu-id="79e74-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e74-145">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="79e74-145">Issue description</span></span>

<span data-ttu-id="79e74-146">For salgs- og overføringsordrer kan du ikke hoppe over varer og foreta delvis plukking.</span><span class="sxs-lookup"><span data-stu-id="79e74-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e74-147">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="79e74-147">Issue resolution</span></span>

<span data-ttu-id="79e74-148">På siden **Menyelementer på mobilenheten** for hvert menyelement som er konfigurert til å behandle salgsordrer eller overføringsordrer, angir du alternativet **Tillat deling av arbeid** på hurtigfanen **Generelt** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="79e74-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="79e74-149">Hvordan kan jeg utføre en lagerstatusendring for arbeid med delvis antall?</span><span class="sxs-lookup"><span data-stu-id="79e74-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e74-150">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="79e74-150">Issue description</span></span>

<span data-ttu-id="79e74-151">Du vil utføre en lagerstatusendring for et delvis antall i et parti.</span><span class="sxs-lookup"><span data-stu-id="79e74-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e74-152">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="79e74-152">Issue resolution</span></span>

<span data-ttu-id="79e74-153">Hvis du vil at arbeidere skal kunne utføre denne endringen, kan du opprette et menyelement for lagerappen.</span><span class="sxs-lookup"><span data-stu-id="79e74-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="79e74-154">Opprett (eller rediger) et menyelement som har følgende innstillinger på siden **Menyelementer på mobilenheten**:</span><span class="sxs-lookup"><span data-stu-id="79e74-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="79e74-155">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="79e74-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="79e74-156">**Bruke eksisterende arbeid:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="79e74-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="79e74-157">**Arbeidsopprettelsesprosess:** *Flytting*</span><span class="sxs-lookup"><span data-stu-id="79e74-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="79e74-158">**Vis beholdningsstatus:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="79e74-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="79e74-159">Du kan angi andre felter på siden slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="79e74-159">You can set other fields on the page as you require.</span></span>

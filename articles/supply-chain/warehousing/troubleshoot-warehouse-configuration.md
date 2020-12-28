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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646113"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="c4fa5-103">Feilsøk lagerkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="c4fa5-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4fa5-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du konfigurerer Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="c4fa5-105">Jeg får følgende feilmelding: Nummerskiltet eller lokasjonen er ugyldig.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c4fa5-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4fa5-106">Issue description</span></span>

<span data-ttu-id="c4fa5-107">Du får denne feilmeldingen når du skanner en nummerskilt-ID eller lokasjon.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c4fa5-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c4fa5-108">Issue resolution</span></span>

<span data-ttu-id="c4fa5-109">Pass på at nummerskilt-ID-en ikke er reserver av noe annet.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="c4fa5-110">Dette problemet oppstod tidligere når verdien som en bruker skannet i lagerappen, var både en gyldig lokasjon og en gyldig nummerskilt-ID.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="c4fa5-111">Dette problemet ble imidlertid løst i versjon 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="c4fa5-112">Jeg får følgende feilmelding: Nummerskilt må angis for denne lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c4fa5-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4fa5-113">Issue description</span></span>

<span data-ttu-id="c4fa5-114">Du får denne feilmeldingen hvis du oppretter en overføringsordre ved hjelp av et lager som er aktivert for avansert lagerstyring (WMS), og etter at arbeidet er fullført, prøver du å bekrefte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c4fa5-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c4fa5-115">Issue resolution</span></span>

<span data-ttu-id="c4fa5-116">Feltet **Standard mottakssted** er tomt for et transittlager i fra-lageret.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="c4fa5-117">Du kan løse dette problemet ved å angi en standard mottakssted i transittlageret.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="c4fa5-118">Kontroller at denne plasseringen er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="c4fa5-119">Jeg får følgende feilmelding: Du kan ikke opprette en arbeidsmallinje for lagerstatusendring fordi arbeidstypen ikke er gyldig.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="c4fa5-120">Velg en annen arbeidstype.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c4fa5-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4fa5-121">Issue description</span></span>

<span data-ttu-id="c4fa5-122">Du kan ikke velge *Lagerstatusendring* i **Arbeidstype**-kolonnen i delen **Arbeidsmaldetaljer**.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c4fa5-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c4fa5-123">Issue resolution</span></span>

<span data-ttu-id="c4fa5-124">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-124">This behavior is by design.</span></span> <span data-ttu-id="c4fa5-125">Arbeidstypen *Lagerstatusendring* brukes bare av systemprosesser.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="c4fa5-126">Den kan ikke konfigureres.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-126">It can't be configured.</span></span> <span data-ttu-id="c4fa5-127">Fordi listen over arbeidstyper er fast som en opplisting, kan ikke de ekstra postene filtreres ut fra rullegardinmenyen **Arbeidstype**.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="c4fa5-128">Jeg får følgende feilmelding: Antallet er ikke gyldig for enhet 1%.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c4fa5-129">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4fa5-129">Issue description</span></span>

<span data-ttu-id="c4fa5-130">Antallet er ikke gyldig for *ea*-enheten når det er et plukkarbeid som har flere nummerskilter på ett sted.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c4fa5-131">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c4fa5-131">Issue resolution</span></span>

<span data-ttu-id="c4fa5-132">Kontroller at feltene **Sekvensgruppe-ID for enhet** og **Enhetskonverteringer** i frigitt produkt eller produktvariant er riktig angitt.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="c4fa5-133">Legg merke til at feilmeldingen er forbedret i versjon 10.0.15 (se [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="c4fa5-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="c4fa5-134">Den nye feilmeldingen er Antallet er ikke gyldig.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="c4fa5-135">Forventet %1 %2.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="c4fa5-136">I lokasjonsdirektiver for plasseringsarbeid for salgsordre evaluerer ikke alternativet flere SKU-er flere lokasjonsdirektivhandlinger.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c4fa5-137">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4fa5-137">Issue description</span></span>

<span data-ttu-id="c4fa5-138">Lokasjonsdirektiver for *Salgsordre*-arbeidsordretypen og *Plasser*-arbeidstypen evaluerer ikke fler lokasjonsdirektivhandlinger når det **Flere SKU-er** er valgt.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="c4fa5-139">Bare den første lokasjonsdirektivhandlingen evalueres.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c4fa5-140">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c4fa5-140">Issue resolution</span></span>

<span data-ttu-id="c4fa5-141">En ny funksjon, *Evaluere alle handlinger for lokasjonsdirektiver med flere SKU-er*, er lagt til i versjon 10.0.15 (se [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="c4fa5-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="c4fa5-142">Denne funksjonen evaluerer alle handlinger for lokasjonsdirektiver med flere SKU-er.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="c4fa5-143">Hvis du trenger denne funksjonen, kan du bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere den.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="c4fa5-144">Jeg kan ikke bruke lagerappen til delvis plukking.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c4fa5-145">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4fa5-145">Issue description</span></span>

<span data-ttu-id="c4fa5-146">For salgs- og overføringsordrer kan du ikke hoppe over varer og foreta delvis plukking.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c4fa5-147">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c4fa5-147">Issue resolution</span></span>

<span data-ttu-id="c4fa5-148">På siden **Menyelementer på mobilenheten** for hvert menyelement som er konfigurert til å behandle salgsordrer eller overføringsordrer, angir du alternativet **Tillat deling av arbeid** på hurtigfanen **Generelt** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="c4fa5-149">Hvordan kan jeg utføre en lagerstatusendring for arbeid med delvis antall?</span><span class="sxs-lookup"><span data-stu-id="c4fa5-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="c4fa5-150">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4fa5-150">Issue description</span></span>

<span data-ttu-id="c4fa5-151">Du vil utføre en lagerstatusendring for et delvis antall i et parti.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c4fa5-152">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c4fa5-152">Issue resolution</span></span>

<span data-ttu-id="c4fa5-153">Hvis du vil at arbeidere skal kunne utføre denne endringen, kan du opprette et menyelement for lagerappen.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="c4fa5-154">Opprett (eller rediger) et menyelement som har følgende innstillinger på siden **Menyelementer på mobilenheten**:</span><span class="sxs-lookup"><span data-stu-id="c4fa5-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="c4fa5-155">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="c4fa5-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="c4fa5-156">**Bruke eksisterende arbeid:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="c4fa5-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="c4fa5-157">**Arbeidsopprettelsesprosess:** *Flytting*</span><span class="sxs-lookup"><span data-stu-id="c4fa5-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="c4fa5-158">**Vis beholdningsstatus:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="c4fa5-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="c4fa5-159">Du kan angi andre felter på siden slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-159">You can set other fields on the page as you require.</span></span>

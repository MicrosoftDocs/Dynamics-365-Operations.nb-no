---
title: "Konfigurere navn på appfelt i lagerapp"
description: "Dette emnet beskriver hvordan du definerer og konfigurerer navn på lagerappfelt og prioriteter i Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 0162014189ed6bffb17e6718a67eecfd55c334a5
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="5f5d3-103">Konfigurere navn på appfelt i lagerapp</span><span class="sxs-lookup"><span data-stu-id="5f5d3-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f5d3-104">Dette emnet beskriver hvordan du definerer og konfigurerer navn på lagerappfelt og prioriteter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="5f5d3-105">**Obs!** Dette emnet artikkelen gjelder funksjoner i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="5f5d3-106">Den gjelder ikke for funksjoner i Beholdningsstyring.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="5f5d3-107">Finance and Operations – Lager er en app som du kan bruke til å utføre lageroppgaver.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="5f5d3-108">Du kan definere og konfigurere feltnavnene som brukes i appen, samt konfigurere prioriteten som feltnavnene skal tilordnes.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="5f5d3-109">Dette emnet forklarer hvordan du definerer og konfigurerer disse navnene og prioriteringene for lagerappfelt, og hvordan de brukes i Finance and Operations – Warehousing.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="5f5d3-110">Hvis du vil ha detaljert informasjon om hvordan du konfigurerer tilkoblingen til Finance and Operations – Warehousing, kan du se opplæringen [Installere og konfigurere Finance and Operations – Warehousing](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="5f5d3-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="5f5d3-111">Konfigurere navn på lagerappfelt</span><span class="sxs-lookup"><span data-stu-id="5f5d3-111">Configure warehouse app field names</span></span>

<span data-ttu-id="5f5d3-112">Når du bruker Finance and Operations – Warehousing på den mobile enheten, kan du konfigurere hvordan metadata skal vises på enheten på siden **Navn på lagerappfelt**.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="5f5d3-113">I et nytt firma i Finance and Operations velger du **Opprett standardoppsett** for å generere alle feltnavn som skal brukes i arbeidsflyter for mobilenheter i lageret, og deretter tilordner du en foretrukket inndatamodus og inndatatype til dem.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="5f5d3-114">Når du har generert alle feltnavn, kan du velge følgende alternativer for inndata.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f5d3-115">Alternativ</span><span class="sxs-lookup"><span data-stu-id="5f5d3-115">Option</span></span></th>
<th><span data-ttu-id="5f5d3-116">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5f5d3-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f5d3-117">Foretrukket inndatamodus</span><span class="sxs-lookup"><span data-stu-id="5f5d3-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="5f5d3-118">Dette alternativet angir om et skanningsfelt eller et manuelt inndatafelt skal vises for det valgte feltnavnet.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="5f5d3-119">Dette er nyttig for å skille feltene, avhengig om strekkoder er brukt for feltet.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="5f5d3-120"><strong>Merk:</strong> For feltnavnene med foretrukket inndatamodus satt til <strong>Skanning</strong>, kan du angi informasjon manuelt hvis strekkoden er uleselig eller skadet.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f5d3-121">Inndatatype</span><span class="sxs-lookup"><span data-stu-id="5f5d3-121">Input type</span></span></td>
<td><span data-ttu-id="5f5d3-122">Dette alternativet angir hvilken inndatatype som skal brukes for det valgte feltnavnet.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="5f5d3-123">Fire alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="5f5d3-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="5f5d3-124"><strong>Utvalg</strong> - Inneholder en liste med alternativer å velge mellom.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="5f5d3-125">Feltnavn med dette alternativet kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="5f5d3-126"><strong>Dato</strong> - Feltnavn som er oppgitt som dato, viser et datoformat med etiketten.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="5f5d3-127">På denne måten kan lagermedarbeidere se hvilket format datoen skal angis i.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="5f5d3-128">Feltnavn med dette alternativet kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="5f5d3-129"><strong>Alpha</strong> - Hvis dette er valgt vil enhetens tastatur brukes ved innskriving av informasjon manuelt i appen.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="5f5d3-130">Tastaturopplevelsen kan endres avhengig av hvilken enhet som brukes.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="5f5d3-131"><strong>Numerisk</strong> - For feltnavn som bare bruker numerisk inngang, kan du velge dette alternativet for å vise et egendefinert numerisk tastatur med inntastingsfeltet, i stedet for enhetens tastatur.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="5f5d3-132">Konfigurere prioritet for lagerappfelt</span><span class="sxs-lookup"><span data-stu-id="5f5d3-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="5f5d3-133">På siden **Prioritet for lagerappfelt** kan du legge feltnavn i ulike prioritetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="5f5d3-134">Dette gjør det mulig å bestemme hvilken informasjon som skal vises på hovedoppgavesiden når lagermedarbeidere utfører oppgaver ved hjelp av appen.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="5f5d3-135">Hvis du klikker **Opprett standardoppsett**, genereres et standardsett med prioritetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="5f5d3-136">Det er mulig å opprette så mange prioritetsgrupper som nødvendig, men bare tre prioritetsgrupper vises på oppgavesiden.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="5f5d3-137">Når Finance and Operations sender metadata til appen, tilordnes hvert felt en relativ prioritet avhengig av prioritetsgruppen, og appen viser de første tre prioritetsgruppene i metadataene på oppgavesiden.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="5f5d3-138">Resten av overflytmetadataene vises på en sekundær detaljside.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="5f5d3-139">Tabellen nedenfor viser et eksempel på fem prioritetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f5d3-140">Prioritetsgruppe</span><span class="sxs-lookup"><span data-stu-id="5f5d3-140">Priority group</span></span></th>
<th><span data-ttu-id="5f5d3-141">Tilordnede felt</span><span class="sxs-lookup"><span data-stu-id="5f5d3-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="5f5d3-142">Prioritet 10</span><span class="sxs-lookup"><span data-stu-id="5f5d3-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="5f5d3-143">Vare</span><span class="sxs-lookup"><span data-stu-id="5f5d3-143">Item</span></span></li>
<li><span data-ttu-id="5f5d3-144">Antall</span><span class="sxs-lookup"><span data-stu-id="5f5d3-144">Quantity</span></span></li>
<li><span data-ttu-id="5f5d3-145">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="5f5d3-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="5f5d3-146">Prioritet 20</span><span class="sxs-lookup"><span data-stu-id="5f5d3-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="5f5d3-147">Gruppestilling</span><span class="sxs-lookup"><span data-stu-id="5f5d3-147">Cluster position</span></span></li>
<li><span data-ttu-id="5f5d3-148">Gruppe</span><span class="sxs-lookup"><span data-stu-id="5f5d3-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="5f5d3-149">Prioritet 30</span><span class="sxs-lookup"><span data-stu-id="5f5d3-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="5f5d3-150">Varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5f5d3-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="5f5d3-151">Prioritet 40</span><span class="sxs-lookup"><span data-stu-id="5f5d3-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="5f5d3-152">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="5f5d3-152">Configuration</span></span></li>
<li><span data-ttu-id="5f5d3-153">Farge</span><span class="sxs-lookup"><span data-stu-id="5f5d3-153">Color</span></span></li>
<li><span data-ttu-id="5f5d3-154">Størrelse</span><span class="sxs-lookup"><span data-stu-id="5f5d3-154">Size</span></span></li>
<li><span data-ttu-id="5f5d3-155">Stil</span><span class="sxs-lookup"><span data-stu-id="5f5d3-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="5f5d3-156">Prioritet 50</span><span class="sxs-lookup"><span data-stu-id="5f5d3-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="5f5d3-157">Plassering</span><span class="sxs-lookup"><span data-stu-id="5f5d3-157">Location</span></span></li>
<li><span data-ttu-id="5f5d3-158">Nummerskilt</span><span class="sxs-lookup"><span data-stu-id="5f5d3-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f5d3-159">Når en lagermedarbeider for eksempel utfører en oppgave på en mobil enhet, og metadataene som vises i appen, består av følgende felt:</span><span class="sxs-lookup"><span data-stu-id="5f5d3-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="5f5d3-160">Vare</span><span class="sxs-lookup"><span data-stu-id="5f5d3-160">Item</span></span>
-   <span data-ttu-id="5f5d3-161">Antall</span><span class="sxs-lookup"><span data-stu-id="5f5d3-161">Quantity</span></span>
-   <span data-ttu-id="5f5d3-162">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="5f5d3-162">Unit of measure</span></span>
-   <span data-ttu-id="5f5d3-163">Varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5f5d3-163">Item description</span></span>
-   <span data-ttu-id="5f5d3-164">Størrelse og lokasjon</span><span class="sxs-lookup"><span data-stu-id="5f5d3-164">Size and Location</span></span>

<span data-ttu-id="5f5d3-165">Basert på prioriteten for lagerappfelt som er definert i tabellen ovenfor, vises følgende 3 rader med informasjon på oppgavesiden:</span><span class="sxs-lookup"><span data-stu-id="5f5d3-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="5f5d3-166">Rad 1: vare, antall, måleenhet</span><span class="sxs-lookup"><span data-stu-id="5f5d3-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="5f5d3-167">Rad 2: varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5f5d3-167">Row 2: Item description</span></span>
-   <span data-ttu-id="5f5d3-168">Rad 3: størrelse</span><span class="sxs-lookup"><span data-stu-id="5f5d3-168">Row 3: Size</span></span>

<span data-ttu-id="5f5d3-169">Gjenstående metadata, for eksempel lokasjon, vises ikke på oppgavesiden, men vises på detaljsiden.</span><span class="sxs-lookup"><span data-stu-id="5f5d3-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="5f5d3-170">Hvis du vil vite mer og se eksempler på brukergrensesnittet, kan du se blogginnlegget [Kunngjøring av Finance and Operations – Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="5f5d3-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="5f5d3-171">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5f5d3-171">Additional resources</span></span>
--------

[<span data-ttu-id="5f5d3-172">Installere og konfigurere Microsoft Dynamics 365 for Finance and Operations – Warehousing</span><span class="sxs-lookup"><span data-stu-id="5f5d3-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)





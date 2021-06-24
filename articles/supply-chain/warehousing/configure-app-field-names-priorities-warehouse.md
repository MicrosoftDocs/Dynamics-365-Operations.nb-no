---
title: Konfigurer felter for mobilappen Lagerstyring
description: Dette emnet beskriver hvordan du definerer og konfigurerer navn på og egenskaper for felter som vises i mobilappen Lagerstyring.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc224d3fd6cf5b111f61066202090f10ba4a7e8a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189256"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="ae34a-103">Konfigurer felter for mobilappen Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ae34a-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae34a-104">Dette emnet beskriver hvordan du definerer og konfigurerer navn på og egenskaper for felter som vises i mobilappen Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="ae34a-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="ae34a-105">Dette emnet artikkelen gjelder funksjoner i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="ae34a-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="ae34a-106">Den gjelder ikke for funksjoner i Beholdningsstyring.</span><span class="sxs-lookup"><span data-stu-id="ae34a-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="ae34a-107">Mobilappen Lagerstyring er en app som du kan bruke til å utføre lageroppgaver.</span><span class="sxs-lookup"><span data-stu-id="ae34a-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="ae34a-108">Du kan definere og konfigurere feltnavnene som brukes i appen, samt konfigurere prioriteten som feltnavnene skal tilordnes.</span><span class="sxs-lookup"><span data-stu-id="ae34a-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="ae34a-109">Dette emnet forklarer hvordan du definerer og konfigurerer disse feltnavnene og -egenskapene i mobilappen LAgerstyring, og hvordan de brukes.</span><span class="sxs-lookup"><span data-stu-id="ae34a-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="ae34a-110">Konfigurere navn på lagerappfelt</span><span class="sxs-lookup"><span data-stu-id="ae34a-110">Configure warehouse app field names</span></span>

<span data-ttu-id="ae34a-111">Når du bruker Warehousing på den mobile enheten, kan du konfigurere hvordan metadata skal vises på enheten på siden **Navn på lagerappfelt**.</span><span class="sxs-lookup"><span data-stu-id="ae34a-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="ae34a-112">I et nytt firma velger du **Opprett standardoppsett** for å generere alle feltnavn som skal brukes i arbeidsflyter for mobilenheter i lageret, og deretter tilordner du en foretrukket inndatamodus og inndatatype til dem.</span><span class="sxs-lookup"><span data-stu-id="ae34a-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="ae34a-113">Når du har generert alle feltnavn, kan du velge følgende alternativer for inndata.</span><span class="sxs-lookup"><span data-stu-id="ae34a-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae34a-114">Alternativ</span><span class="sxs-lookup"><span data-stu-id="ae34a-114">Option</span></span></th>
<th><span data-ttu-id="ae34a-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ae34a-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae34a-116">Foretrukket inndatamodus</span><span class="sxs-lookup"><span data-stu-id="ae34a-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="ae34a-117">Dette alternativet angir om et skanningsfelt eller et manuelt inndatafelt skal vises for det valgte feltnavnet.</span><span class="sxs-lookup"><span data-stu-id="ae34a-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="ae34a-118">Dette er nyttig for å skille feltene, avhengig om strekkoder er brukt for feltet.</span><span class="sxs-lookup"><span data-stu-id="ae34a-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="ae34a-119"><strong>Merk:</strong> For feltnavnene med foretrukket inndatamodus satt til <strong>Skanning</strong>, kan du angi informasjon manuelt hvis strekkoden er uleselig eller skadet.</span><span class="sxs-lookup"><span data-stu-id="ae34a-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae34a-120">Inndatatype</span><span class="sxs-lookup"><span data-stu-id="ae34a-120">Input type</span></span></td>
<td><span data-ttu-id="ae34a-121">Dette alternativet angir hvilken inndatatype som skal brukes for det valgte feltnavnet.</span><span class="sxs-lookup"><span data-stu-id="ae34a-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="ae34a-122">Fire alternativer er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="ae34a-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="ae34a-123"><strong>Utvalg</strong> - Inneholder en liste med alternativer å velge mellom.</span><span class="sxs-lookup"><span data-stu-id="ae34a-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="ae34a-124">Feltnavn med dette alternativet kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="ae34a-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="ae34a-125"><strong>Dato</strong> - Feltnavn som er oppgitt som dato, viser et datoformat med etiketten.</span><span class="sxs-lookup"><span data-stu-id="ae34a-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="ae34a-126">På denne måten kan lagermedarbeidere se hvilket format datoen skal angis i.</span><span class="sxs-lookup"><span data-stu-id="ae34a-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="ae34a-127">Feltnavn med dette alternativet kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="ae34a-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="ae34a-128"><strong>Alpha</strong> - Hvis dette er valgt vil enhetens tastatur brukes ved innskriving av informasjon manuelt i appen.</span><span class="sxs-lookup"><span data-stu-id="ae34a-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="ae34a-129">Tastaturopplevelsen kan endres avhengig av hvilken enhet som brukes.</span><span class="sxs-lookup"><span data-stu-id="ae34a-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="ae34a-130"><strong>Numerisk</strong> - For feltnavn som bare bruker numerisk inngang, kan du velge dette alternativet for å vise et egendefinert numerisk tastatur med inntastingsfeltet, i stedet for enhetens tastatur.</span><span class="sxs-lookup"><span data-stu-id="ae34a-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="ae34a-131">Konfigurere prioritet for lagerappfelt</span><span class="sxs-lookup"><span data-stu-id="ae34a-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="ae34a-132">På siden **Prioritet for lagerappfelt** kan du legge feltnavn i ulike prioritetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ae34a-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="ae34a-133">Dette gjør det mulig å bestemme hvilken informasjon som skal vises på hovedoppgavesiden når lagermedarbeidere utfører oppgaver ved hjelp av appen.</span><span class="sxs-lookup"><span data-stu-id="ae34a-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="ae34a-134">Hvis du klikker **Opprett standardoppsett**, genereres et standardsett med prioritetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ae34a-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="ae34a-135">Det er mulig å opprette så mange prioritetsgrupper som nødvendig, men bare tre prioritetsgrupper vises på oppgavesiden.</span><span class="sxs-lookup"><span data-stu-id="ae34a-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="ae34a-136">Når systemet sender metadata til appen, tilordnes hvert felt en relativ prioritet avhengig av prioritetsgruppen, og appen viser de første tre prioritetsgruppene i metadataene på oppgavesiden.</span><span class="sxs-lookup"><span data-stu-id="ae34a-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="ae34a-137">Resten av overflytmetadataene vises på en sekundær detaljside.</span><span class="sxs-lookup"><span data-stu-id="ae34a-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="ae34a-138">Tabellen nedenfor viser et eksempel på fem prioritetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ae34a-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae34a-139">Prioritetsgruppe</span><span class="sxs-lookup"><span data-stu-id="ae34a-139">Priority group</span></span></th>
<th><span data-ttu-id="ae34a-140">Tilordnede felt</span><span class="sxs-lookup"><span data-stu-id="ae34a-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="ae34a-141">Prioritet 10</span><span class="sxs-lookup"><span data-stu-id="ae34a-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="ae34a-142">Vare</span><span class="sxs-lookup"><span data-stu-id="ae34a-142">Item</span></span></li>
<li><span data-ttu-id="ae34a-143">Antall</span><span class="sxs-lookup"><span data-stu-id="ae34a-143">Quantity</span></span></li>
<li><span data-ttu-id="ae34a-144">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="ae34a-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="ae34a-145">Prioritet 20</span><span class="sxs-lookup"><span data-stu-id="ae34a-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="ae34a-146">Gruppestilling</span><span class="sxs-lookup"><span data-stu-id="ae34a-146">Cluster position</span></span></li>
<li><span data-ttu-id="ae34a-147">Gruppe</span><span class="sxs-lookup"><span data-stu-id="ae34a-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="ae34a-148">Prioritet 30</span><span class="sxs-lookup"><span data-stu-id="ae34a-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="ae34a-149">Varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="ae34a-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="ae34a-150">Prioritet 40</span><span class="sxs-lookup"><span data-stu-id="ae34a-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="ae34a-151">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="ae34a-151">Configuration</span></span></li>
<li><span data-ttu-id="ae34a-152">Farge</span><span class="sxs-lookup"><span data-stu-id="ae34a-152">Color</span></span></li>
<li><span data-ttu-id="ae34a-153">Størrelse</span><span class="sxs-lookup"><span data-stu-id="ae34a-153">Size</span></span></li>
<li><span data-ttu-id="ae34a-154">Stil</span><span class="sxs-lookup"><span data-stu-id="ae34a-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="ae34a-155">Prioritet 50</span><span class="sxs-lookup"><span data-stu-id="ae34a-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="ae34a-156">Plassering</span><span class="sxs-lookup"><span data-stu-id="ae34a-156">Location</span></span></li>
<li><span data-ttu-id="ae34a-157">Nummerskilt</span><span class="sxs-lookup"><span data-stu-id="ae34a-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ae34a-158">Når en lagermedarbeider for eksempel utfører en oppgave på en mobil enhet, og metadataene som vises i appen, består av følgende felt:</span><span class="sxs-lookup"><span data-stu-id="ae34a-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="ae34a-159">Vare</span><span class="sxs-lookup"><span data-stu-id="ae34a-159">Item</span></span>
-   <span data-ttu-id="ae34a-160">Antall</span><span class="sxs-lookup"><span data-stu-id="ae34a-160">Quantity</span></span>
-   <span data-ttu-id="ae34a-161">Måleenhet</span><span class="sxs-lookup"><span data-stu-id="ae34a-161">Unit of measure</span></span>
-   <span data-ttu-id="ae34a-162">Varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="ae34a-162">Item description</span></span>
-   <span data-ttu-id="ae34a-163">Størrelse og lokasjon</span><span class="sxs-lookup"><span data-stu-id="ae34a-163">Size and Location</span></span>

<span data-ttu-id="ae34a-164">Basert på prioriteten for lagerappfelt som er definert i tabellen ovenfor, vises følgende 3 rader med informasjon på oppgavesiden:</span><span class="sxs-lookup"><span data-stu-id="ae34a-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="ae34a-165">Rad 1: vare, antall, måleenhet</span><span class="sxs-lookup"><span data-stu-id="ae34a-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="ae34a-166">Rad 2: varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="ae34a-166">Row 2: Item description</span></span>
-   <span data-ttu-id="ae34a-167">Rad 3: størrelse</span><span class="sxs-lookup"><span data-stu-id="ae34a-167">Row 3: Size</span></span>

<span data-ttu-id="ae34a-168">Gjenstående metadata, for eksempel lokasjon, vises ikke på oppgavesiden, men vises på detaljsiden.</span><span class="sxs-lookup"><span data-stu-id="ae34a-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="ae34a-169">Hvis du vil vite mer og se eksempler på brukergrensesnittet, kan du se blogginnlegget [Kunngjøring av Finance and Operations – Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="ae34a-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae34a-170">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ae34a-170">Additional resources</span></span>

[<span data-ttu-id="ae34a-171">Installere og koble til mobilappen Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ae34a-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
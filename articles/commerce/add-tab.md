---
title: Kategorimodul
description: Dette emnet dekker kategorimoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c9d897113442f14b95539efb9fec9482be96447a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414588"
---
# <a name="tab-module"></a><span data-ttu-id="cbf4b-103">Kategorimodul</span><span class="sxs-lookup"><span data-stu-id="cbf4b-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cbf4b-104">Dette emnet dekker kategorimoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cbf4b-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="cbf4b-105">Overview</span></span>

<span data-ttu-id="cbf4b-106">Kategorimoduler er beholdere-lignende moduler som brukes til å organisere informasjonen på en områdeside i kategorier.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="cbf4b-107">De kan brukes på en hvilken som helst side hvor informasjon må presenteres i kategorier.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="cbf4b-108">I hver kategorimodul kan én eller flere kategorielementmoduler legges til.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="cbf4b-109">Hver kategorielementmodul representerer én enkelt kategori. I hver kategorielementmodul kan én eller flere moduler legges til.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="cbf4b-110">Det er ingen begrensninger på hvilke modultyper som kan legges til i en kategorielementmodul.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="cbf4b-111">Bildet nedenfor viser et eksempel på en kategorimodul på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="cbf4b-112">I dette eksemplet er kategorien **Forsendelse** valgt.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-112">In this example, the **Shipping** tab selected.</span></span>

![Eksempel på en kategorimodul](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="cbf4b-114">Egenskaper for kategorimoduler</span><span class="sxs-lookup"><span data-stu-id="cbf4b-114">Tab module properties</span></span>

| <span data-ttu-id="cbf4b-115">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="cbf4b-115">Property name</span></span> | <span data-ttu-id="cbf4b-116">Verdier</span><span class="sxs-lookup"><span data-stu-id="cbf4b-116">Values</span></span> | <span data-ttu-id="cbf4b-117">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cbf4b-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="cbf4b-118">Overskrift</span><span class="sxs-lookup"><span data-stu-id="cbf4b-118">Heading</span></span> | <span data-ttu-id="cbf4b-119">Tekst</span><span class="sxs-lookup"><span data-stu-id="cbf4b-119">Text</span></span> | <span data-ttu-id="cbf4b-120">Denne egenskapen angir en valgfri tekstoverskrift for kategorimodulen.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="cbf4b-121">Aktiv kategoriindeks</span><span class="sxs-lookup"><span data-stu-id="cbf4b-121">Active Tab Index</span></span> | <span data-ttu-id="cbf4b-122">Tall</span><span class="sxs-lookup"><span data-stu-id="cbf4b-122">Number</span></span> | <span data-ttu-id="cbf4b-123">Denne egenskapen angir kategorien som skal være aktiv som standard når en side lastes inn.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="cbf4b-124">Hvis ingen verdi er angitt, er standardfunksjonen at det første kategorielementet er aktivt.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="cbf4b-125">Egenskaper for kategorielementmoduler</span><span class="sxs-lookup"><span data-stu-id="cbf4b-125">Tab item module properties</span></span>

| <span data-ttu-id="cbf4b-126">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="cbf4b-126">Property name</span></span> | <span data-ttu-id="cbf4b-127">Verdier</span><span class="sxs-lookup"><span data-stu-id="cbf4b-127">Values</span></span> | <span data-ttu-id="cbf4b-128">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cbf4b-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="cbf4b-129">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="cbf4b-129">Title</span></span> | <span data-ttu-id="cbf4b-130">Tekst</span><span class="sxs-lookup"><span data-stu-id="cbf4b-130">Text</span></span> | <span data-ttu-id="cbf4b-131">Denne egenskapen angir overskriftteksten for kategorielementmodulen.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="cbf4b-132">Legge til en kategorimodul på en side</span><span class="sxs-lookup"><span data-stu-id="cbf4b-132">Add a tab module to a page</span></span>

<span data-ttu-id="cbf4b-133">Hvis du vil legge til en kategorimodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="cbf4b-134">Bruk Fabrikam-markedsføringsmalen (eller en mal som ikke har begrensninger) for å opprette en ny side som heter **Butikkpolicy-side**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="cbf4b-135">På **Hoved**-sporet på **Standardside** velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cbf4b-136">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cbf4b-137">I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cbf4b-138">I dialogboksen **Legg til modul** velger du **Kategori**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cbf4b-139">Velg **Overskrift** ved siden av blyantsymbolet i egenskapsruten i kategorimodulen.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="cbf4b-140">I **Overskrift**-dialogboksen, under **Overskriftstekst**, angir du overskriftsteksten (f.eks. **Policyer**).</span><span class="sxs-lookup"><span data-stu-id="cbf4b-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="cbf4b-141">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-141">Then select **OK**.</span></span>
1. <span data-ttu-id="cbf4b-142">I **Kategori**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cbf4b-143">I dialogboksen **Legg til modul** velger du **Kategorielement**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cbf4b-144">I egenskapsruten for kategorielementmodulen, under **Tittel**, skriver du inn tittelteksten (f.eks. **Levering**).</span><span class="sxs-lookup"><span data-stu-id="cbf4b-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="cbf4b-145">I **Kategorielement**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cbf4b-146">I dialogboksen **Legg til modul** velger du **Tekstblokk**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cbf4b-147">I egenskapsruten for tekstblokkmodulen legger du til et avsnitt med tekst under **Rik tekst**.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="cbf4b-148">I **Kategori**-sporet legger du til et par ekstra kategorielementmoduler med overskrifter.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="cbf4b-149">Legg til en tekstblokkmodul med innhold i hver enkelt kategorielementmodul.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="cbf4b-150">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="cbf4b-151">Siden viser en kategorimodul som inneholder kategorielementmoduler med innholdet du la til.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="cbf4b-152">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="cbf4b-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cbf4b-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cbf4b-153">Additional resources</span></span>

[<span data-ttu-id="cbf4b-154">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="cbf4b-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cbf4b-155">Beholdermodul</span><span class="sxs-lookup"><span data-stu-id="cbf4b-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="cbf4b-156">Samsvarsmodul</span><span class="sxs-lookup"><span data-stu-id="cbf4b-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="cbf4b-157">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="cbf4b-157">Text block module</span></span>](add-content-rich-block.md)

---
title: Kategorimodul
description: Dette emnet dekker fanemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209233"
---
# <a name="tab-module"></a><span data-ttu-id="c1dfe-103">Kategorimodul</span><span class="sxs-lookup"><span data-stu-id="c1dfe-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c1dfe-104">Dette emnet dekker fanemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c1dfe-105">Kategorimoduler er beholdere-lignende moduler som brukes til å organisere informasjonen på en områdeside i kategorier.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="c1dfe-106">De kan brukes på en hvilken som helst side hvor informasjon må presenteres i kategorier.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="c1dfe-107">I hver kategorimodul kan én eller flere kategorielementmoduler legges til.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="c1dfe-108">Hver kategorielementmodul representerer én enkelt kategori. I hver kategorielementmodul kan én eller flere moduler legges til.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="c1dfe-109">Det er ingen begrensninger på hvilke modultyper som kan legges til i en kategorielementmodul.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="c1dfe-110">Bildet nedenfor viser et eksempel på en kategorimodul på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="c1dfe-111">I dette eksemplet er kategorien **Forsendelse** valgt.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-111">In this example, the **Shipping** tab selected.</span></span>

![Eksempel på en kategorimodul](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="c1dfe-113">Egenskaper for kategorimoduler</span><span class="sxs-lookup"><span data-stu-id="c1dfe-113">Tab module properties</span></span>

| <span data-ttu-id="c1dfe-114">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="c1dfe-114">Property name</span></span> | <span data-ttu-id="c1dfe-115">Verdier</span><span class="sxs-lookup"><span data-stu-id="c1dfe-115">Values</span></span> | <span data-ttu-id="c1dfe-116">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1dfe-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="c1dfe-117">Overskrift</span><span class="sxs-lookup"><span data-stu-id="c1dfe-117">Heading</span></span> | <span data-ttu-id="c1dfe-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="c1dfe-118">Text</span></span> | <span data-ttu-id="c1dfe-119">Denne egenskapen angir en valgfri tekstoverskrift for kategorimodulen.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="c1dfe-120">Aktiv kategoriindeks</span><span class="sxs-lookup"><span data-stu-id="c1dfe-120">Active Tab Index</span></span> | <span data-ttu-id="c1dfe-121">Tall</span><span class="sxs-lookup"><span data-stu-id="c1dfe-121">Number</span></span> | <span data-ttu-id="c1dfe-122">Denne egenskapen angir kategorien som skal være aktiv som standard når en side lastes inn.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="c1dfe-123">Hvis ingen verdi er angitt, er standardfunksjonen at det første kategorielementet er aktivt.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="c1dfe-124">Egenskaper for kategorielementmoduler</span><span class="sxs-lookup"><span data-stu-id="c1dfe-124">Tab item module properties</span></span>

| <span data-ttu-id="c1dfe-125">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="c1dfe-125">Property name</span></span> | <span data-ttu-id="c1dfe-126">Verdier</span><span class="sxs-lookup"><span data-stu-id="c1dfe-126">Values</span></span> | <span data-ttu-id="c1dfe-127">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1dfe-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="c1dfe-128">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="c1dfe-128">Title</span></span> | <span data-ttu-id="c1dfe-129">Tekst</span><span class="sxs-lookup"><span data-stu-id="c1dfe-129">Text</span></span> | <span data-ttu-id="c1dfe-130">Denne egenskapen angir overskriftteksten for kategorielementmodulen.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="c1dfe-131">Legge til en kategorimodul på en side</span><span class="sxs-lookup"><span data-stu-id="c1dfe-131">Add a tab module to a page</span></span>

<span data-ttu-id="c1dfe-132">Hvis du vil legge til en kategorimodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="c1dfe-133">Bruk Fabrikam-markedsføringsmalen (eller en mal som ikke har begrensninger) for å opprette en ny side som heter **Butikkpolicy-side**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="c1dfe-134">På **Hoved**-sporet på **Standardside** velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c1dfe-135">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c1dfe-136">I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c1dfe-137">I dialogboksen **Legg til modul** velger du **Kategori**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c1dfe-138">Velg **Overskrift** ved siden av blyantsymbolet i egenskapsruten i kategorimodulen.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="c1dfe-139">I **Overskrift**-dialogboksen, under **Overskriftstekst**, angir du overskriftsteksten (f.eks. **Policyer**).</span><span class="sxs-lookup"><span data-stu-id="c1dfe-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="c1dfe-140">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-140">Then select **OK**.</span></span>
1. <span data-ttu-id="c1dfe-141">I **Kategori**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c1dfe-142">I dialogboksen **Legg til modul** velger du **Kategorielement**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c1dfe-143">I egenskapsruten for kategorielementmodulen, under **Tittel**, skriver du inn tittelteksten (f.eks. **Levering**).</span><span class="sxs-lookup"><span data-stu-id="c1dfe-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="c1dfe-144">I **Kategorielement**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c1dfe-145">I dialogboksen **Legg til modul** velger du **Tekstblokk**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c1dfe-146">I egenskapsruten for tekstblokkmodulen legger du til et avsnitt med tekst under **Rik tekst**.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="c1dfe-147">I **Kategori**-sporet legger du til et par ekstra kategorielementmoduler med overskrifter.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="c1dfe-148">Legg til en tekstblokkmodul med innhold i hver enkelt kategorielementmodul.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="c1dfe-149">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="c1dfe-150">Siden viser en kategorimodul som inneholder kategorielementmoduler med innholdet du la til.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="c1dfe-151">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1dfe-152">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c1dfe-152">Additional resources</span></span>

[<span data-ttu-id="c1dfe-153">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="c1dfe-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c1dfe-154">Beholdermodul</span><span class="sxs-lookup"><span data-stu-id="c1dfe-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c1dfe-155">Samsvarsmodul</span><span class="sxs-lookup"><span data-stu-id="c1dfe-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="c1dfe-156">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="c1dfe-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
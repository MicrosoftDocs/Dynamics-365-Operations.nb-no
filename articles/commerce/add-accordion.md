---
title: Trekkspillmodul
description: Dette emnet dekker trekkspillmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ba973299291276fe48d82360e203ca28f02aaffb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796276"
---
# <a name="accordion-module"></a><span data-ttu-id="1cf60-103">Samsvarsmodul</span><span class="sxs-lookup"><span data-stu-id="1cf60-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1cf60-104">Dette emnet dekker trekkspillmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1cf60-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1cf60-105">Slike moduler er beholder-lignende moduler som brukes til å organisere informasjonen eller modulene på en side gjennom en skuffelignende funksjon.</span><span class="sxs-lookup"><span data-stu-id="1cf60-105">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="1cf60-106">En trekkspillmodul kan brukes på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="1cf60-106">An accordion module can be used on any page.</span></span>

<span data-ttu-id="1cf60-107">I hver trekkspillmodul kan én eller flere trekkspillelementmoduler legges til.</span><span class="sxs-lookup"><span data-stu-id="1cf60-107">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="1cf60-108">Hver trekkspillelementmodul representerer en skjulbar skuff.</span><span class="sxs-lookup"><span data-stu-id="1cf60-108">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="1cf60-109">I hver trekkspillelementmodul kan én eller flere moduler legges til.</span><span class="sxs-lookup"><span data-stu-id="1cf60-109">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="1cf60-110">Det er ingen begrensninger på hvilke modultyper som kan legges til i en trekkspillelementmodul.</span><span class="sxs-lookup"><span data-stu-id="1cf60-110">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="1cf60-111">Bildet nedenfor viser et eksempel på en trekkspillmodul som brukes til å organisere informasjon på en side med vanlige spørsmål om en butikk.</span><span class="sxs-lookup"><span data-stu-id="1cf60-111">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Eksempel på en trekkspillmodul](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="1cf60-113">Egenskaper for trekkspillmoduler</span><span class="sxs-lookup"><span data-stu-id="1cf60-113">Accordion module properties</span></span>

| <span data-ttu-id="1cf60-114">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="1cf60-114">Property name</span></span> | <span data-ttu-id="1cf60-115">Verdier</span><span class="sxs-lookup"><span data-stu-id="1cf60-115">Values</span></span> | <span data-ttu-id="1cf60-116">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cf60-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="1cf60-117">Overskrift</span><span class="sxs-lookup"><span data-stu-id="1cf60-117">Heading</span></span> | <span data-ttu-id="1cf60-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="1cf60-118">Text</span></span> | <span data-ttu-id="1cf60-119">Denne egenskapen angir en valgfri tekstoverskrift for trekkspillmodulen.</span><span class="sxs-lookup"><span data-stu-id="1cf60-119">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="1cf60-120">Vis alle</span><span class="sxs-lookup"><span data-stu-id="1cf60-120">Expand All</span></span> | <span data-ttu-id="1cf60-121">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="1cf60-121">**True** or **False**</span></span> | <span data-ttu-id="1cf60-122">Hvis verdien er satt til **Sann**, aktiveres vis/skjul-funksjonaliteten slik at alle elementene i denne modulen kan utvides og skjules.</span><span class="sxs-lookup"><span data-stu-id="1cf60-122">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="1cf60-123">Samhandlingsstil</span><span class="sxs-lookup"><span data-stu-id="1cf60-123">Interaction Style</span></span> | <span data-ttu-id="1cf60-124">**Uavhengig** eller **Bare utvid ett element**</span><span class="sxs-lookup"><span data-stu-id="1cf60-124">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="1cf60-125">Denne egenskapen angir samhandlingsstilen for trekkspillelementer.</span><span class="sxs-lookup"><span data-stu-id="1cf60-125">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="1cf60-126">Hvis verdien er satt til **Uavhengig**, kan hvert enkelt trekkspillelement utvides eller skjules uavhengig av hverandre.</span><span class="sxs-lookup"><span data-stu-id="1cf60-126">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="1cf60-127">Hvis verdien er satt til **Bare utvid ett element**, kan bare ett element utvides om gangen.</span><span class="sxs-lookup"><span data-stu-id="1cf60-127">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="1cf60-128">Når et element utvides, skjules tidligere utvidede elementer.</span><span class="sxs-lookup"><span data-stu-id="1cf60-128">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="1cf60-129">Egenskaper for trekkspillelementmoduler</span><span class="sxs-lookup"><span data-stu-id="1cf60-129">Accordion item module properties</span></span>

| <span data-ttu-id="1cf60-130">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="1cf60-130">Property name</span></span> | <span data-ttu-id="1cf60-131">Verdier</span><span class="sxs-lookup"><span data-stu-id="1cf60-131">Values</span></span> | <span data-ttu-id="1cf60-132">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1cf60-132">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="1cf60-133">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="1cf60-133">Title</span></span> | <span data-ttu-id="1cf60-134">Tekst</span><span class="sxs-lookup"><span data-stu-id="1cf60-134">Text</span></span> | <span data-ttu-id="1cf60-135">Denne egenskapen angir overskriftteksten for trekkspillelementmodulen.</span><span class="sxs-lookup"><span data-stu-id="1cf60-135">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="1cf60-136">Ved å velge tittelområdet kan brukerne vise eller skjule delen.</span><span class="sxs-lookup"><span data-stu-id="1cf60-136">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="1cf60-137">Utvid som standard</span><span class="sxs-lookup"><span data-stu-id="1cf60-137">Expand by default</span></span> | <span data-ttu-id="1cf60-138">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="1cf60-138">**True** or **False**</span></span> | <span data-ttu-id="1cf60-139">Hvis verdien er satt til **Sann**, utvides trekkspillelementet som standard når siden lastes inn.</span><span class="sxs-lookup"><span data-stu-id="1cf60-139">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="1cf60-140">Legge til en trekkspillmodul på en side med vanlige spørsmål</span><span class="sxs-lookup"><span data-stu-id="1cf60-140">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="1cf60-141">Hvis du vil legge til en trekkspillmodul på en side med vanlige spørsmål, og angi egenskapene i områdebygger, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="1cf60-141">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="1cf60-142">Gå til **Sider**, og bruk Fabrikam-markedsføringsmalen (eller en mal som ikke har begrensninger) for å opprette en ny side som heter **Vanlige spørsmål om butikken**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-142">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="1cf60-143">På **Hoved**-sporet på **Standardside** velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-143">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1cf60-144">I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-144">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1cf60-145">I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-145">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1cf60-146">I dialogboksen **Legg til modul** velger du **Trekkspill**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-146">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1cf60-147">Velg **Overskrift** ved siden av blyantsymbolet i egenskapsruten i trekkspillmodulen.</span><span class="sxs-lookup"><span data-stu-id="1cf60-147">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="1cf60-148">I **Overskrift**-dialogboksen, under **Overskriftstekst**, skriver du **Vanlige spørsmål**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-148">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="1cf60-149">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-149">Then select **OK**.</span></span>
1. <span data-ttu-id="1cf60-150">I egenskapsruten i trekkspillmodulen merker du av for **Vis alle utvidet**-ruten, og i **Samhandlingsstil**-feltet velger du **Uavhengig**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-150">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="1cf60-151">I **Trekkspill**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-151">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1cf60-152">I dialogboksen **Legg til modul** velger du **Trekkspillelement**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-152">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1cf60-153">I egenskapsruten for trekkspillelementmodulen, under **Tittel** skriver du inn tittelteksten (f.eks. **Hvordan fungerer returordningen?**).</span><span class="sxs-lookup"><span data-stu-id="1cf60-153">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="1cf60-154">I **Trekkspillelement**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-154">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1cf60-155">I dialogboksen **Legg til modul** velger du **Tekstblokk**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cf60-155">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1cf60-156">I egenskapsruten for tekstblokkmodulen skriver du inn et avsnitt med tekst (f.eks. **Returer må behandles via kundesenteret. Ring 1-800–FABRIKAM for retur av varer. Produkter har en 30-dagers returpolicy. Returer må iverksettes innenfor denne tidsrammen.**).</span><span class="sxs-lookup"><span data-stu-id="1cf60-156">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="1cf60-157">I **Trekkspill**-sporet legger du til flere trekkspillelementmoduler.</span><span class="sxs-lookup"><span data-stu-id="1cf60-157">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="1cf60-158">Legg til en tekstblokkmodul med innhold i hver enkelt trekkspillelementmodul.</span><span class="sxs-lookup"><span data-stu-id="1cf60-158">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="1cf60-159">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="1cf60-159">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="1cf60-160">Siden viser en trekkspillmodul som har innholdet du la til.</span><span class="sxs-lookup"><span data-stu-id="1cf60-160">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="1cf60-161">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="1cf60-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1cf60-162">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1cf60-162">Additional resources</span></span>

[<span data-ttu-id="1cf60-163">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="1cf60-163">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1cf60-164">Beholdermodul</span><span class="sxs-lookup"><span data-stu-id="1cf60-164">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1cf60-165">Kategorimodul</span><span class="sxs-lookup"><span data-stu-id="1cf60-165">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="1cf60-166">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="1cf60-166">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
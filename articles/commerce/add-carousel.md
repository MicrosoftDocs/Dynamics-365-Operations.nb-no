---
title: Karusellmodul
description: Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797893"
---
# <a name="carousel-module"></a><span data-ttu-id="5209f-103">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="5209f-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5209f-104">Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5209f-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5209f-105">En karusellmodul brukes til å legge flere kampanjevarer (inkludert rike bilder) i et roterende karusellbanner som kunder kan bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="5209f-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="5209f-106">En forhandler kan for eksempel bruke en karusellmodul på en startside til å vise flere nye produkter eller kampanjer.</span><span class="sxs-lookup"><span data-stu-id="5209f-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="5209f-107">Du kan legge til innholdsblokkmoduler i en karusellmodul.</span><span class="sxs-lookup"><span data-stu-id="5209f-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="5209f-108">Egenskapene for karusellmodulen definerer deretter hvordan disse modulene gjengis.</span><span class="sxs-lookup"><span data-stu-id="5209f-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="5209f-109">Eksempler på karusellmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="5209f-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="5209f-110">En karusell som har flere kampanjemoduler inni, kan brukes på en startside.</span><span class="sxs-lookup"><span data-stu-id="5209f-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="5209f-111">En karusell som har flere kampanjemoduler inni, kan brukes på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="5209f-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="5209f-112">En karusell kan brukes på en hvilken som helst markedsføringsside for å fremme flere kampanjer eller produkter.</span><span class="sxs-lookup"><span data-stu-id="5209f-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="5209f-113">Bildet nedenfor viser et eksempel på en karusellmodul som brukes på en hjemmeside.</span><span class="sxs-lookup"><span data-stu-id="5209f-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="5209f-114">Denne karusellmodulen inneholder flere innholdsblokkelementer.</span><span class="sxs-lookup"><span data-stu-id="5209f-114">This carousel module contains multiple content block items.</span></span>

![Eksempel på en karusellmodul](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="5209f-116">Egenskaper for karusellmodul</span><span class="sxs-lookup"><span data-stu-id="5209f-116">Carousel module properties</span></span>

| <span data-ttu-id="5209f-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="5209f-117">Property name</span></span>             | <span data-ttu-id="5209f-118">Verdi</span><span class="sxs-lookup"><span data-stu-id="5209f-118">Value</span></span>                 | <span data-ttu-id="5209f-119">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="5209f-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5209f-120">Autokjør</span><span class="sxs-lookup"><span data-stu-id="5209f-120">Autoplay</span></span>                  | <span data-ttu-id="5209f-121">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="5209f-121">**True** or **False**</span></span> | <span data-ttu-id="5209f-122">Hvis verdien settes til **Sann**, skjer overgangen mellom elementer i karusellen automatisk.</span><span class="sxs-lookup"><span data-stu-id="5209f-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="5209f-123">Hvis verdien settes til **Usann**, skjer ingen overgang med mindre kunden bruker tastaturet eller musen til å flytte fra ett element til neste element.</span><span class="sxs-lookup"><span data-stu-id="5209f-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="5209f-124">Intervall for lysbildeovergang</span><span class="sxs-lookup"><span data-stu-id="5209f-124">Slide transition interval</span></span> | <span data-ttu-id="5209f-125">En verdi i sekunder</span><span class="sxs-lookup"><span data-stu-id="5209f-125">A value in seconds</span></span>    | <span data-ttu-id="5209f-126">Intervallet for overganger mellom elementer.</span><span class="sxs-lookup"><span data-stu-id="5209f-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="5209f-127">Overgangstype</span><span class="sxs-lookup"><span data-stu-id="5209f-127">Transition type</span></span>           | <span data-ttu-id="5209f-128">**Lysbilde** eller **Toning**</span><span class="sxs-lookup"><span data-stu-id="5209f-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="5209f-129">Overgangseffekten mellom varer.</span><span class="sxs-lookup"><span data-stu-id="5209f-129">The transition effect between items.</span></span> |
| <span data-ttu-id="5209f-130">Skjul karusellflipper</span><span class="sxs-lookup"><span data-stu-id="5209f-130">Hide carousel flipper</span></span>     | <span data-ttu-id="5209f-131">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="5209f-131">**True** or **False**</span></span> | <span data-ttu-id="5209f-132">Hvis verdien settes til **Sann**, skjules karusellflipperen og sekvensindikatoren.</span><span class="sxs-lookup"><span data-stu-id="5209f-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="5209f-133">Tillat å forkaste karusell</span><span class="sxs-lookup"><span data-stu-id="5209f-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="5209f-134">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="5209f-134">**True** or **False**</span></span> | <span data-ttu-id="5209f-135">Hvis verdien settes til **Sann**, kan brukerne forkaste karusellen.</span><span class="sxs-lookup"><span data-stu-id="5209f-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="5209f-136">Legge til en karusellmodul på en side</span><span class="sxs-lookup"><span data-stu-id="5209f-136">Add a carousel module to a page</span></span>

<span data-ttu-id="5209f-137">Hvis du vil legge til en karusellmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="5209f-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5209f-138">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="5209f-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="5209f-139">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Karusellmal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5209f-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="5209f-140">Legg til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="5209f-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="5209f-141">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="5209f-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="5209f-142">Bruk karusellmalen du nettopp opprettet, for å opprette en side som heter **Karusellside**.</span><span class="sxs-lookup"><span data-stu-id="5209f-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="5209f-143">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="5209f-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="5209f-144">I ruten til høyre setter du **Bredde**-verdien til **Fyll skjerm**.</span><span class="sxs-lookup"><span data-stu-id="5209f-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="5209f-145">Under **Sideoppsett** legger du til en karusellmodul i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="5209f-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="5209f-146">Legg til en innholdsblokkmodul i karusellmodulen.</span><span class="sxs-lookup"><span data-stu-id="5209f-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="5209f-147">Angi egenskapene for innholdsblokkmodulen ved å angi **Overskrift**, **Kobling**, **Oppsett** og andre egenskaper.</span><span class="sxs-lookup"><span data-stu-id="5209f-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="5209f-148">Legg til og konfigurer en ny innholdsblokkmodul.</span><span class="sxs-lookup"><span data-stu-id="5209f-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="5209f-149">Angi flere egenskaper for karusellmodulen etter behov.</span><span class="sxs-lookup"><span data-stu-id="5209f-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="5209f-150">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="5209f-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="5209f-151">Siden skal vise en karusell med to moduler i (en hovedbannermodul og en funksjonsmodul).</span><span class="sxs-lookup"><span data-stu-id="5209f-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="5209f-152">Du kan endre flere egenskaper for modulene karusell, hovedbanner og funksjon for å oppnå ønsket effekt.</span><span class="sxs-lookup"><span data-stu-id="5209f-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="5209f-153">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="5209f-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5209f-154">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5209f-154">Additional resources</span></span>

[<span data-ttu-id="5209f-155">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="5209f-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5209f-156">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="5209f-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="5209f-157">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="5209f-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="5209f-158">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="5209f-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="5209f-159">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="5209f-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
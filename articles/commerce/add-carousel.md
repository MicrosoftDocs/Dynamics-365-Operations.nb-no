---
title: Karusellmodul
description: Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 0b4ce8fdb7b598e55db59ddf5a99a0ba46eb6f91
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986010"
---
# <a name="carousel-module"></a><span data-ttu-id="72b2c-103">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="72b2c-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="72b2c-104">Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="72b2c-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="72b2c-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="72b2c-105">Overview</span></span>

<span data-ttu-id="72b2c-106">En karusellmodul brukes til å legge flere kampanjevarer (inkludert rike bilder) i et roterende karusellbanner som kunder kan bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="72b2c-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="72b2c-107">En forhandler kan for eksempel bruke en karusellmodul på en startside til å vise flere nye produkter eller kampanjer.</span><span class="sxs-lookup"><span data-stu-id="72b2c-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="72b2c-108">Du kan legge til innholdsblokkmoduler i en karusellmodul.</span><span class="sxs-lookup"><span data-stu-id="72b2c-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="72b2c-109">Egenskapene for karusellmodulen definerer deretter hvordan disse modulene gjengis.</span><span class="sxs-lookup"><span data-stu-id="72b2c-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="72b2c-110">Eksempler på karusellmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="72b2c-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="72b2c-111">En karusell som har flere kampanjemoduler inni, kan brukes på en startside.</span><span class="sxs-lookup"><span data-stu-id="72b2c-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="72b2c-112">En karusell som har flere kampanjemoduler inni, kan brukes på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="72b2c-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="72b2c-113">En karusell kan brukes på en hvilken som helst markedsføringsside for å fremme flere kampanjer eller produkter.</span><span class="sxs-lookup"><span data-stu-id="72b2c-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="72b2c-114">Bildet nedenfor viser et eksempel på en karusellmodul som brukes på en hjemmeside.</span><span class="sxs-lookup"><span data-stu-id="72b2c-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="72b2c-115">Denne karusellmodulen inneholder flere innholdsblokkelementer.</span><span class="sxs-lookup"><span data-stu-id="72b2c-115">This carousel module contains multiple content block items.</span></span>

![Eksempel på en karusellmodul](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="72b2c-117">Egenskaper for karusellmodul</span><span class="sxs-lookup"><span data-stu-id="72b2c-117">Carousel module properties</span></span>

| <span data-ttu-id="72b2c-118">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="72b2c-118">Property name</span></span>             | <span data-ttu-id="72b2c-119">Verdi</span><span class="sxs-lookup"><span data-stu-id="72b2c-119">Value</span></span>                 | <span data-ttu-id="72b2c-120">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="72b2c-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="72b2c-121">Autokjør</span><span class="sxs-lookup"><span data-stu-id="72b2c-121">Autoplay</span></span>                  | <span data-ttu-id="72b2c-122">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="72b2c-122">**True** or **False**</span></span> | <span data-ttu-id="72b2c-123">Hvis verdien settes til **Sann**, skjer overgangen mellom elementer i karusellen automatisk.</span><span class="sxs-lookup"><span data-stu-id="72b2c-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="72b2c-124">Hvis verdien settes til **Usann**, skjer ingen overgang med mindre kunden bruker tastaturet eller musen til å flytte fra ett element til neste element.</span><span class="sxs-lookup"><span data-stu-id="72b2c-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="72b2c-125">Intervall for lysbildeovergang</span><span class="sxs-lookup"><span data-stu-id="72b2c-125">Slide transition interval</span></span> | <span data-ttu-id="72b2c-126">En verdi i sekunder</span><span class="sxs-lookup"><span data-stu-id="72b2c-126">A value in seconds</span></span>    | <span data-ttu-id="72b2c-127">Intervallet for overganger mellom elementer.</span><span class="sxs-lookup"><span data-stu-id="72b2c-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="72b2c-128">Overgangstype</span><span class="sxs-lookup"><span data-stu-id="72b2c-128">Transition type</span></span>           | <span data-ttu-id="72b2c-129">**Lysbilde** eller **Toning**</span><span class="sxs-lookup"><span data-stu-id="72b2c-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="72b2c-130">Overgangseffekten mellom varer.</span><span class="sxs-lookup"><span data-stu-id="72b2c-130">The transition effect between items.</span></span> |
| <span data-ttu-id="72b2c-131">Skjul karusellflipper</span><span class="sxs-lookup"><span data-stu-id="72b2c-131">Hide carousel flipper</span></span>     | <span data-ttu-id="72b2c-132">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="72b2c-132">**True** or **False**</span></span> | <span data-ttu-id="72b2c-133">Hvis verdien settes til **Sann**, skjules karusellflipperen og sekvensindikatoren.</span><span class="sxs-lookup"><span data-stu-id="72b2c-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="72b2c-134">Tillat å forkaste karusell</span><span class="sxs-lookup"><span data-stu-id="72b2c-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="72b2c-135">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="72b2c-135">**True** or **False**</span></span> | <span data-ttu-id="72b2c-136">Hvis verdien settes til **Sann**, kan brukerne forkaste karusellen.</span><span class="sxs-lookup"><span data-stu-id="72b2c-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="72b2c-137">Legge til en karusellmodul på en side</span><span class="sxs-lookup"><span data-stu-id="72b2c-137">Add a carousel module to a page</span></span>

<span data-ttu-id="72b2c-138">Hvis du vil legge til en karusellmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="72b2c-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="72b2c-139">Gå til **Maler**, og velg **Ny** for å opprette en ny mal.</span><span class="sxs-lookup"><span data-stu-id="72b2c-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="72b2c-140">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Karusellmal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="72b2c-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="72b2c-141">Legg til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="72b2c-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="72b2c-142">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="72b2c-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="72b2c-143">Bruk karusellmalen du nettopp opprettet, for å opprette en side som heter **Karusellside**.</span><span class="sxs-lookup"><span data-stu-id="72b2c-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="72b2c-144">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="72b2c-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="72b2c-145">I ruten til høyre setter du **Bredde**-verdien til **Fyll skjerm**.</span><span class="sxs-lookup"><span data-stu-id="72b2c-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="72b2c-146">Under **Sideoppsett** legger du til en karusellmodul i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="72b2c-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="72b2c-147">Legg til en innholdsblokkmodul i karusellmodulen.</span><span class="sxs-lookup"><span data-stu-id="72b2c-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="72b2c-148">Angi egenskapene for innholdsblokkmodulen ved å angi **Overskrift**, **Kobling**, **Oppsett** og andre egenskaper.</span><span class="sxs-lookup"><span data-stu-id="72b2c-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="72b2c-149">Legg til og konfigurer en ny innholdsblokkmodul.</span><span class="sxs-lookup"><span data-stu-id="72b2c-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="72b2c-150">Angi flere egenskaper for karusellmodulen etter behov.</span><span class="sxs-lookup"><span data-stu-id="72b2c-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="72b2c-151">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="72b2c-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="72b2c-152">Siden skal vise en karusell med to moduler i (en hovedbannermodul og en funksjonsmodul).</span><span class="sxs-lookup"><span data-stu-id="72b2c-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="72b2c-153">Du kan endre flere egenskaper for modulene karusell, hovedbanner og funksjon for å oppnå ønsket effekt.</span><span class="sxs-lookup"><span data-stu-id="72b2c-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="72b2c-154">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="72b2c-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72b2c-155">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="72b2c-155">Additional resources</span></span>

[<span data-ttu-id="72b2c-156">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="72b2c-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="72b2c-157">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="72b2c-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="72b2c-158">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="72b2c-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="72b2c-159">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="72b2c-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="72b2c-160">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="72b2c-160">Video player module</span></span>](add-video-player.md)

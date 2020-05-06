---
title: Karusellmodul
description: Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269734"
---
# <a name="carousel-module"></a><span data-ttu-id="60b81-103">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="60b81-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="60b81-104">Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="60b81-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="60b81-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="60b81-105">Overview</span></span>

<span data-ttu-id="60b81-106">En karusellmodul brukes til å legge flere kampanjevarer (inkludert rike bilder) i et roterende karusellbanner som kunder kan bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="60b81-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="60b81-107">En forhandler kan for eksempel bruke en karusellmodul på en startside til å vise flere nye produkter eller kampanjer.</span><span class="sxs-lookup"><span data-stu-id="60b81-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="60b81-108">Du kan legge til innholdsblokkmoduler i en karusellmodul.</span><span class="sxs-lookup"><span data-stu-id="60b81-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="60b81-109">Egenskapene for karusellmodulen definerer deretter hvordan disse modulene gjengis.</span><span class="sxs-lookup"><span data-stu-id="60b81-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="60b81-110">Eksempler på karusellmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="60b81-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="60b81-111">En karusell som har flere kampanjemoduler inni, kan brukes på en startside.</span><span class="sxs-lookup"><span data-stu-id="60b81-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="60b81-112">En karusell som har flere kampanjemoduler inni, kan brukes på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="60b81-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="60b81-113">En karusell kan brukes på en hvilken som helst markedsføringsside for å fremme flere kampanjer eller produkter.</span><span class="sxs-lookup"><span data-stu-id="60b81-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="60b81-114">Egenskaper for karusellmodul</span><span class="sxs-lookup"><span data-stu-id="60b81-114">Carousel module properties</span></span>

| <span data-ttu-id="60b81-115">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="60b81-115">Property name</span></span>             | <span data-ttu-id="60b81-116">Verdi</span><span class="sxs-lookup"><span data-stu-id="60b81-116">Value</span></span>                 | <span data-ttu-id="60b81-117">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="60b81-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="60b81-118">Autokjør</span><span class="sxs-lookup"><span data-stu-id="60b81-118">Autoplay</span></span>                  | <span data-ttu-id="60b81-119">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="60b81-119">**True** or **False**</span></span> | <span data-ttu-id="60b81-120">Hvis verdien settes til **Sann**, skjer overgangen mellom elementer i karusellen automatisk.</span><span class="sxs-lookup"><span data-stu-id="60b81-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="60b81-121">Hvis verdien settes til **Usann**, skjer ingen overgang med mindre kunden bruker tastaturet eller musen til å flytte fra ett element til neste element.</span><span class="sxs-lookup"><span data-stu-id="60b81-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="60b81-122">Intervall for lysbildeovergang</span><span class="sxs-lookup"><span data-stu-id="60b81-122">Slide transition interval</span></span> | <span data-ttu-id="60b81-123">En verdi i sekunder</span><span class="sxs-lookup"><span data-stu-id="60b81-123">A value in seconds</span></span>    | <span data-ttu-id="60b81-124">Intervallet for overganger mellom elementer.</span><span class="sxs-lookup"><span data-stu-id="60b81-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="60b81-125">Overgangstype</span><span class="sxs-lookup"><span data-stu-id="60b81-125">Transition type</span></span>           | <span data-ttu-id="60b81-126">**Lysbilde** eller **Toning**</span><span class="sxs-lookup"><span data-stu-id="60b81-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="60b81-127">Overgangseffekten mellom varer.</span><span class="sxs-lookup"><span data-stu-id="60b81-127">The transition effect between items.</span></span> |
| <span data-ttu-id="60b81-128">Skjul karusellflipper</span><span class="sxs-lookup"><span data-stu-id="60b81-128">Hide carousel flipper</span></span>     | <span data-ttu-id="60b81-129">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="60b81-129">**True** or **False**</span></span> | <span data-ttu-id="60b81-130">Hvis verdien settes til **Sann**, skjules karusellflipperen og sekvensindikatoren.</span><span class="sxs-lookup"><span data-stu-id="60b81-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="60b81-131">Tillat å forkaste karusell</span><span class="sxs-lookup"><span data-stu-id="60b81-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="60b81-132">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="60b81-132">**True** or **False**</span></span> | <span data-ttu-id="60b81-133">Hvis verdien settes til **Sann**, kan brukerne forkaste karusellen.</span><span class="sxs-lookup"><span data-stu-id="60b81-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="60b81-134">Legge til en karusellmodul på en side</span><span class="sxs-lookup"><span data-stu-id="60b81-134">Add a carousel module to a page</span></span>

<span data-ttu-id="60b81-135">Hvis du vil legge til en karusellmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="60b81-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="60b81-136">Velg **Ny** for å opprette en sidemal.</span><span class="sxs-lookup"><span data-stu-id="60b81-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="60b81-137">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Karusellmal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="60b81-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="60b81-138">Legg til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="60b81-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="60b81-139">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="60b81-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="60b81-140">Bruk karusellmalen du nettopp opprettet, for å opprette en side som heter **Karusellside**.</span><span class="sxs-lookup"><span data-stu-id="60b81-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="60b81-141">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="60b81-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="60b81-142">I ruten til høyre setter du **Bredde**-verdien til **Fyll skjerm**.</span><span class="sxs-lookup"><span data-stu-id="60b81-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="60b81-143">Under **Sideoppsett** legger du til en karusellmodul i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="60b81-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="60b81-144">Legg til en innholdsblokkmodul i karusellmodulen.</span><span class="sxs-lookup"><span data-stu-id="60b81-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="60b81-145">Angi egenskapene for innholdsblokkmodulen ved å angi **Overskrift**, **Kobling**, **Oppsett** og andre egenskaper.</span><span class="sxs-lookup"><span data-stu-id="60b81-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="60b81-146">Legg til og konfigurer en ny innholdsblokkmodul.</span><span class="sxs-lookup"><span data-stu-id="60b81-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="60b81-147">Angi flere egenskaper for karusellmodulen etter behov.</span><span class="sxs-lookup"><span data-stu-id="60b81-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="60b81-148">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="60b81-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="60b81-149">Siden skal vise en karusell med to moduler i (en hovedbannermodul og en funksjonsmodul).</span><span class="sxs-lookup"><span data-stu-id="60b81-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="60b81-150">Du kan endre flere egenskaper for modulene karusell, hovedbanner og funksjon for å oppnå ønsket effekt.</span><span class="sxs-lookup"><span data-stu-id="60b81-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="60b81-151">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="60b81-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60b81-152">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="60b81-152">Additional resources</span></span>

[<span data-ttu-id="60b81-153">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="60b81-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="60b81-154">Promobannermodul</span><span class="sxs-lookup"><span data-stu-id="60b81-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="60b81-155">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="60b81-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="60b81-156">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="60b81-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="60b81-157">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="60b81-157">Video player module</span></span>](add-video-player.md)

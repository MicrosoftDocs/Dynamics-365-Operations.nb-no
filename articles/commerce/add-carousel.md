---
title: Karusellmodul
description: Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025787"
---
# <a name="carousel-module"></a><span data-ttu-id="12d82-103">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="12d82-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="12d82-104">Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="12d82-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="12d82-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="12d82-105">Overview</span></span>

<span data-ttu-id="12d82-106">En karusellmodul brukes til å legge flere kampanjevarer (inkludert rike bilder) i et roterende karusellbanner som kunder kan bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="12d82-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="12d82-107">En forhandler kan for eksempel bruke en karusellmodul på en startside til å vise flere nye produkter eller kampanjer.</span><span class="sxs-lookup"><span data-stu-id="12d82-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="12d82-108">Du kan legge til innholdsblokkmoduler i en karusellmodul.</span><span class="sxs-lookup"><span data-stu-id="12d82-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="12d82-109">Egenskapene for karusellmodulen definerer deretter hvordan disse modulene gjengis.</span><span class="sxs-lookup"><span data-stu-id="12d82-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="12d82-110">Eksempler på karusellmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="12d82-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="12d82-111">En karusell som har flere kampanjemoduler inni, kan brukes på en startside.</span><span class="sxs-lookup"><span data-stu-id="12d82-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="12d82-112">En karusell som har flere kampanjemoduler inni, kan brukes på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="12d82-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="12d82-113">En karusell kan brukes på en hvilken som helst markedsføringsside for å fremme flere kampanjer eller produkter.</span><span class="sxs-lookup"><span data-stu-id="12d82-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="12d82-114">Egenskaper for karusellmodul</span><span class="sxs-lookup"><span data-stu-id="12d82-114">Carousel module properties</span></span>

| <span data-ttu-id="12d82-115">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="12d82-115">Property name</span></span>             | <span data-ttu-id="12d82-116">Verdi</span><span class="sxs-lookup"><span data-stu-id="12d82-116">Value</span></span>                 | <span data-ttu-id="12d82-117">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="12d82-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="12d82-118">Autokjør</span><span class="sxs-lookup"><span data-stu-id="12d82-118">Autoplay</span></span>                  | <span data-ttu-id="12d82-119">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="12d82-119">**True** or **False**</span></span> | <span data-ttu-id="12d82-120">Hvis verdien settes til **Sann**, skjer overgangen mellom elementer i karusellen automatisk.</span><span class="sxs-lookup"><span data-stu-id="12d82-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="12d82-121">Hvis verdien settes til **Usann**, skjer ingen overgang med mindre kunden bruker tastaturet eller musen til å flytte fra ett element til neste element.</span><span class="sxs-lookup"><span data-stu-id="12d82-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="12d82-122">Intervall for lysbildeovergang</span><span class="sxs-lookup"><span data-stu-id="12d82-122">Slide transition interval</span></span> | <span data-ttu-id="12d82-123">En verdi i sekunder</span><span class="sxs-lookup"><span data-stu-id="12d82-123">A value in seconds</span></span>    | <span data-ttu-id="12d82-124">Intervallet for overganger mellom elementer.</span><span class="sxs-lookup"><span data-stu-id="12d82-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="12d82-125">Overgangstype</span><span class="sxs-lookup"><span data-stu-id="12d82-125">Transition type</span></span>           | <span data-ttu-id="12d82-126">**Lysbilde** eller **Toning**</span><span class="sxs-lookup"><span data-stu-id="12d82-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="12d82-127">Overgangseffekten mellom varer.</span><span class="sxs-lookup"><span data-stu-id="12d82-127">The transition effect between items.</span></span> |
| <span data-ttu-id="12d82-128">Skjul karusellflipper</span><span class="sxs-lookup"><span data-stu-id="12d82-128">Hide carousel flipper</span></span>     | <span data-ttu-id="12d82-129">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="12d82-129">**True** or **False**</span></span> | <span data-ttu-id="12d82-130">Hvis verdien settes til **Sann**, skjules karusellflipperen og sekvensindikatoren.</span><span class="sxs-lookup"><span data-stu-id="12d82-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="12d82-131">Tillat å forkaste karusell</span><span class="sxs-lookup"><span data-stu-id="12d82-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="12d82-132">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="12d82-132">**True** or **False**</span></span> | <span data-ttu-id="12d82-133">Hvis verdien settes til **Sann**, kan brukerne forkaste karusellen.</span><span class="sxs-lookup"><span data-stu-id="12d82-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="12d82-134">Legge til en karusellmodul på en side</span><span class="sxs-lookup"><span data-stu-id="12d82-134">Add a carousel module to a page</span></span>

<span data-ttu-id="12d82-135">Hvis du vil legge til en karusellmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="12d82-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="12d82-136">Opprett en sidemal som heter **karusellmal**.</span><span class="sxs-lookup"><span data-stu-id="12d82-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="12d82-137">Legg til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="12d82-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="12d82-138">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="12d82-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="12d82-139">Bruk karusellmalen du nettopp opprettet, for å opprette en side som heter **karusellside**.</span><span class="sxs-lookup"><span data-stu-id="12d82-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="12d82-140">I **Hoved**-sporet på den nye siden legger du til en containermodul.</span><span class="sxs-lookup"><span data-stu-id="12d82-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="12d82-141">I ruten til høyre setter du **Bredde**-verdien til **Fyll skjerm**.</span><span class="sxs-lookup"><span data-stu-id="12d82-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="12d82-142">Under **Sideoppsett** legger du til en karusellmodul i containermodulen.</span><span class="sxs-lookup"><span data-stu-id="12d82-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="12d82-143">Legg til en innholdsblokkmodul i karusellmodulen.</span><span class="sxs-lookup"><span data-stu-id="12d82-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="12d82-144">Angi egenskapene for innholdsblokkmodulen ved å angi **Overskrift**, **Kobling**, **Oppsett** og andre egenskaper.</span><span class="sxs-lookup"><span data-stu-id="12d82-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="12d82-145">Legg til og konfigurer en ny innholdsblokkmodul.</span><span class="sxs-lookup"><span data-stu-id="12d82-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="12d82-146">Angi flere egenskaper for karusellmodulen etter behov.</span><span class="sxs-lookup"><span data-stu-id="12d82-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="12d82-147">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="12d82-147">Save and preview the page.</span></span> <span data-ttu-id="12d82-148">Siden skal vise en karusell med to moduler i (en hovedbannermodul og en funksjonsmodul).</span><span class="sxs-lookup"><span data-stu-id="12d82-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="12d82-149">Du kan endre flere egenskaper for modulene karusell, hovedbanner og funksjon for å oppnå ønsket effekt.</span><span class="sxs-lookup"><span data-stu-id="12d82-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="12d82-150">Fullfør redigeringen av siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="12d82-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12d82-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="12d82-151">Additional resources</span></span>

[<span data-ttu-id="12d82-152">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="12d82-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="12d82-153">Kampanjebannermodul</span><span class="sxs-lookup"><span data-stu-id="12d82-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="12d82-154">Tekstblokkmodul</span><span class="sxs-lookup"><span data-stu-id="12d82-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="12d82-155">Innholdsblokkmodul</span><span class="sxs-lookup"><span data-stu-id="12d82-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="12d82-156">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="12d82-156">Video player module</span></span>](add-video-player.md)

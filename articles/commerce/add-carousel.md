---
title: Karusellmodul
description: Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785243"
---
# <a name="carousel-module"></a><span data-ttu-id="afe91-103">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="afe91-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="afe91-104">Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="afe91-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="afe91-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="afe91-105">Overview</span></span>

<span data-ttu-id="afe91-106">En karusellmodul brukes til å legge flere kampanjevarer i en karusell som kunder kan bla gjennom.</span><span class="sxs-lookup"><span data-stu-id="afe91-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="afe91-107">Det er en spesiell containermodul som er vert for andre moduler.</span><span class="sxs-lookup"><span data-stu-id="afe91-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="afe91-108">En forhandler kan for eksempel bruke en karusellmodul på en startside til å vise flere nye produkter eller kampanjer.</span><span class="sxs-lookup"><span data-stu-id="afe91-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="afe91-109">Du kan legge til hovedbanner- og funksjonsmoduler i en karusellmodul.</span><span class="sxs-lookup"><span data-stu-id="afe91-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="afe91-110">Egenskapene for karusellmodulen definerer deretter hvordan disse modulene gjengis.</span><span class="sxs-lookup"><span data-stu-id="afe91-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="afe91-111">Eksempler på karusellmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="afe91-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="afe91-112">En karusell som har flere kampanjemoduler inni, kan brukes på en startside.</span><span class="sxs-lookup"><span data-stu-id="afe91-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="afe91-113">En karusell som har flere kampanjemoduler inni, kan brukes på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="afe91-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="afe91-114">En karusell kan brukes på en hvilken som helst markedsføringsside for å fremme flere kampanjer eller produkter.</span><span class="sxs-lookup"><span data-stu-id="afe91-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="afe91-115">Egenskaper for karusellmodul</span><span class="sxs-lookup"><span data-stu-id="afe91-115">Carousel module properties</span></span>

| <span data-ttu-id="afe91-116">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="afe91-116">Property name</span></span>             | <span data-ttu-id="afe91-117">Verdi</span><span class="sxs-lookup"><span data-stu-id="afe91-117">Value</span></span>                                | <span data-ttu-id="afe91-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="afe91-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="afe91-119">Autokjør</span><span class="sxs-lookup"><span data-stu-id="afe91-119">Autoplay</span></span>                  | <span data-ttu-id="afe91-120">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="afe91-120">**True** or **False**</span></span>                | <span data-ttu-id="afe91-121">Hvis verdien settes til **Sann**, skjer overgangen mellom elementer i karusellen automatisk.</span><span class="sxs-lookup"><span data-stu-id="afe91-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="afe91-122">Hvis verdien settes til **Usann**, skjer ingen overgang med mindre kunden bruker tastaturet eller musen til å flytte fra ett element til neste element.</span><span class="sxs-lookup"><span data-stu-id="afe91-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="afe91-123">Intervall for lysbildeovergang</span><span class="sxs-lookup"><span data-stu-id="afe91-123">Slide transition interval</span></span> | <span data-ttu-id="afe91-124">En verdi i sekunder</span><span class="sxs-lookup"><span data-stu-id="afe91-124">A value in seconds</span></span>                   | <span data-ttu-id="afe91-125">Intervallet for overganger mellom elementer.</span><span class="sxs-lookup"><span data-stu-id="afe91-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="afe91-126">Overgangsanimasjon</span><span class="sxs-lookup"><span data-stu-id="afe91-126">Transition animation</span></span>      | <span data-ttu-id="afe91-127">**Lysbilde** eller **Toning**</span><span class="sxs-lookup"><span data-stu-id="afe91-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="afe91-128">Overgangseffekten.</span><span class="sxs-lookup"><span data-stu-id="afe91-128">The transition effect.</span></span> |
| <span data-ttu-id="afe91-129">Bredde</span><span class="sxs-lookup"><span data-stu-id="afe91-129">Width</span></span>                     | <span data-ttu-id="afe91-130">**Tilpass container** eller **Fyll skjerm**</span><span class="sxs-lookup"><span data-stu-id="afe91-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="afe91-131">Hvis verdien er satt til **Tilpass container**, er elementene i karusellen begrenset til bredden på karusellen.</span><span class="sxs-lookup"><span data-stu-id="afe91-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="afe91-132">Hvis verdien er satt til **Fyll skjerm**, er ikke elementene begrenset til karusellbredden, men de kan gå i fullskjermmodus.</span><span class="sxs-lookup"><span data-stu-id="afe91-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="afe91-133">Du kan endre verdien for å oppnå det ønskede oppsettet.</span><span class="sxs-lookup"><span data-stu-id="afe91-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="afe91-134">Legge til en karusellmodul på en side</span><span class="sxs-lookup"><span data-stu-id="afe91-134">Add a carousel module to a page</span></span>

<span data-ttu-id="afe91-135">Hvis du vil legge til en karusellmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="afe91-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="afe91-136">Opprett en sidemal som heter **karusellmal**.</span><span class="sxs-lookup"><span data-stu-id="afe91-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="afe91-137">I **Hoved**-sporet på standardsiden legger du til en karusellmodul.</span><span class="sxs-lookup"><span data-stu-id="afe91-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="afe91-138">Legg til en hovedbannermodul i karusellmodulen.</span><span class="sxs-lookup"><span data-stu-id="afe91-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="afe91-139">Legg til en funksjonsmodul i karusellmodulen.</span><span class="sxs-lookup"><span data-stu-id="afe91-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="afe91-140">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="afe91-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="afe91-141">Bruk karusellmalen du nettopp opprettet, for å opprette en side som heter **karusellside**.</span><span class="sxs-lookup"><span data-stu-id="afe91-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="afe91-142">I **Hoved**-sporet på den nye siden legger du til en karusellmodul.</span><span class="sxs-lookup"><span data-stu-id="afe91-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="afe91-143">Angi egenskapen **Bredde** for karusellmodulen for å **fylle skjermen**.</span><span class="sxs-lookup"><span data-stu-id="afe91-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="afe91-144">Angi egenskapen **Overgangsanimasjon** til **Lysbilde**.</span><span class="sxs-lookup"><span data-stu-id="afe91-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="afe91-145">Legg til en hovedbannermodul i karusellmodulen.</span><span class="sxs-lookup"><span data-stu-id="afe91-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="afe91-146">Legg til et bilde og en overskrift i hovedbannermodulen, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="afe91-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="afe91-147">Legg til en funksjonsmodul i karusellmodulen.</span><span class="sxs-lookup"><span data-stu-id="afe91-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="afe91-148">I funksjonsmodulen legger du til et bilde, en overskrift og et avsnitt med tekst.</span><span class="sxs-lookup"><span data-stu-id="afe91-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="afe91-149">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="afe91-149">Save and preview the page.</span></span> <span data-ttu-id="afe91-150">Siden skal vise en karusell med to moduler i (en hovedbannermodul og en funksjonsmodul).</span><span class="sxs-lookup"><span data-stu-id="afe91-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="afe91-151">Du kan endre flere egenskaper for modulene karusell, hovedbanner og funksjon for å oppnå ønsket effekt.</span><span class="sxs-lookup"><span data-stu-id="afe91-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="afe91-152">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="afe91-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="afe91-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="afe91-153">Additional resources</span></span>

[<span data-ttu-id="afe91-154">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="afe91-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="afe91-155">Varselmodul</span><span class="sxs-lookup"><span data-stu-id="afe91-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="afe91-156">Innholdsrik blokk-modul</span><span class="sxs-lookup"><span data-stu-id="afe91-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="afe91-157">Modul for innholdsplassering</span><span class="sxs-lookup"><span data-stu-id="afe91-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="afe91-158">Funksjonsmodul</span><span class="sxs-lookup"><span data-stu-id="afe91-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="afe91-159">Hovedbannermodul</span><span class="sxs-lookup"><span data-stu-id="afe91-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="afe91-160">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="afe91-160">Video player module</span></span>](add-video-player.md)

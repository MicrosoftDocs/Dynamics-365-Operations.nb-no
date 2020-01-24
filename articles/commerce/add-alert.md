---
title: Varselmodul
description: Dette emnet dekker varselmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785358"
---
# <a name="alert-module"></a><span data-ttu-id="08f93-103">Varselmodul</span><span class="sxs-lookup"><span data-stu-id="08f93-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="08f93-104">Dette emnet dekker varselmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="08f93-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="08f93-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="08f93-105">Overview</span></span>

<span data-ttu-id="08f93-106">En varselmodul brukes til å vise meldinger med innebygd informasjon på en side.</span><span class="sxs-lookup"><span data-stu-id="08f93-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="08f93-107">Varselmoduler støtter en tekstmelding og en kobling.</span><span class="sxs-lookup"><span data-stu-id="08f93-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="08f93-108">De kan brukes til å vise kampanjer på hele området som vises på alle sider av et e-handelsområde.</span><span class="sxs-lookup"><span data-stu-id="08f93-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="08f93-109">Varselmoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="08f93-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="08f93-110">Eksempler på varselmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="08f93-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="08f93-111">Varselmoduler kan brukes på områdehodet for å angi kampanjer eller meldinger på hele området.</span><span class="sxs-lookup"><span data-stu-id="08f93-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="08f93-112">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="08f93-112">Here are some examples:</span></span>

<span data-ttu-id="08f93-113">"Årlige salg avsluttes om 10 dager"</span><span class="sxs-lookup"><span data-stu-id="08f93-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="08f93-114">"Gjør store besparelse på skolestartsalget.</span><span class="sxs-lookup"><span data-stu-id="08f93-114">"Save big with back to school sale.</span></span> <span data-ttu-id="08f93-115">Handle nå. "</span><span class="sxs-lookup"><span data-stu-id="08f93-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="08f93-116">Egenskaper for varselmodul</span><span class="sxs-lookup"><span data-stu-id="08f93-116">Alert module properties</span></span>

| <span data-ttu-id="08f93-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="08f93-117">Property name</span></span>  | <span data-ttu-id="08f93-118">Verdi</span><span class="sxs-lookup"><span data-stu-id="08f93-118">Value</span></span>                              | <span data-ttu-id="08f93-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="08f93-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="08f93-120">Tekst</span><span class="sxs-lookup"><span data-stu-id="08f93-120">Text</span></span>           | <span data-ttu-id="08f93-121">Tekst</span><span class="sxs-lookup"><span data-stu-id="08f93-121">Text</span></span>                               | <span data-ttu-id="08f93-122">Tekstmeldingen som vises i varselmodulen.</span><span class="sxs-lookup"><span data-stu-id="08f93-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="08f93-123">Tekstjustering</span><span class="sxs-lookup"><span data-stu-id="08f93-123">Text alignment</span></span> | <span data-ttu-id="08f93-124">**Høyre**, **Venstre** eller **Midtstilt**</span><span class="sxs-lookup"><span data-stu-id="08f93-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="08f93-125">En verdi som definerer hvordan tekst justeres i varselmodulen.</span><span class="sxs-lookup"><span data-stu-id="08f93-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="08f93-126">Forkast varsel</span><span class="sxs-lookup"><span data-stu-id="08f93-126">Dismiss alert</span></span>  | <span data-ttu-id="08f93-127">**Sann** eller **Usann**</span><span class="sxs-lookup"><span data-stu-id="08f93-127">**True** or **False**</span></span>              | <span data-ttu-id="08f93-128">Hvis verdien settes til **Sann**, kan kunden forkaste varselet.</span><span class="sxs-lookup"><span data-stu-id="08f93-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="08f93-129">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="08f93-129">Link</span></span>           | <span data-ttu-id="08f93-130">URL-adresse</span><span class="sxs-lookup"><span data-stu-id="08f93-130">URL</span></span>                                | <span data-ttu-id="08f93-131">URL-adresse for valgfri kobling.</span><span class="sxs-lookup"><span data-stu-id="08f93-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="08f93-132">Legg til en varselmodul på en side</span><span class="sxs-lookup"><span data-stu-id="08f93-132">Add an alert module to a page</span></span> 

<span data-ttu-id="08f93-133">Hvis du vil legge til en varselmodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="08f93-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="08f93-134">Opprett en sidemal som heter **varselmal**.</span><span class="sxs-lookup"><span data-stu-id="08f93-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="08f93-135">I **Hoved**-sporet på standardsiden legger du til en varselmodul.</span><span class="sxs-lookup"><span data-stu-id="08f93-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="08f93-136">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="08f93-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="08f93-137">Bruk varselmalen du nettopp opprettet, for å opprette en side som heter **varselside**.</span><span class="sxs-lookup"><span data-stu-id="08f93-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="08f93-138">I **Hoved**-sporet på den nye siden legger du til en varselmodul.</span><span class="sxs-lookup"><span data-stu-id="08f93-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="08f93-139">Skriv inn varselteksten i innstillingene for varselmodulen.</span><span class="sxs-lookup"><span data-stu-id="08f93-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="08f93-140">Du kan redigere de andre egenskapene hvis du vil tilpasse varselmodulen ytterligere.</span><span class="sxs-lookup"><span data-stu-id="08f93-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="08f93-141">Lagre og forhåndsvis siden.</span><span class="sxs-lookup"><span data-stu-id="08f93-141">Save and preview the page.</span></span> <span data-ttu-id="08f93-142">Øverst på siden vil du se et varsel som inneholder teksten du la til.</span><span class="sxs-lookup"><span data-stu-id="08f93-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="08f93-143">Sjekk inn siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="08f93-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="08f93-144">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="08f93-144">Additional resources</span></span>

[<span data-ttu-id="08f93-145">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="08f93-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="08f93-146">Karusellmodul</span><span class="sxs-lookup"><span data-stu-id="08f93-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="08f93-147">Innholdsrik blokk-modul</span><span class="sxs-lookup"><span data-stu-id="08f93-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="08f93-148">Modul for innholdsplassering</span><span class="sxs-lookup"><span data-stu-id="08f93-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="08f93-149">Funksjonsmodul</span><span class="sxs-lookup"><span data-stu-id="08f93-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="08f93-150">Hovedbannermodul</span><span class="sxs-lookup"><span data-stu-id="08f93-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="08f93-151">Videospillermodul</span><span class="sxs-lookup"><span data-stu-id="08f93-151">Video player module</span></span>](add-video-player.md)
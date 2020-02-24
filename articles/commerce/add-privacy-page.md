---
title: Legge til en side med personvernpolicy
description: Dette emnet beskriver hvordan du legger til en side med personvernpolicy på området ditt i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001329"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="308c5-103">Legge til en side med personvernpolicy</span><span class="sxs-lookup"><span data-stu-id="308c5-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="308c5-104">Dette emnet beskriver hvordan du legger til en side med personvernpolicy på området ditt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="308c5-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="308c5-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="308c5-105">Overview</span></span>

<span data-ttu-id="308c5-106">Overholdelse av personvern inkluderer organisatoriske tiltak som informerer brukerne om hvordan deres data samles inn og håndteres.</span><span class="sxs-lookup"><span data-stu-id="308c5-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="308c5-107">Brukere kan deretter bestemme hvordan de vil at deres personlige data skal håndteres og kan iverksette nødvendige tiltak.</span><span class="sxs-lookup"><span data-stu-id="308c5-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="308c5-108">Se gjennom Microsofts personvernerklæring i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="308c5-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="308c5-109">Hvis du vil se gjennom Microsofts personvernerklæring mens du er logget på redigeringsverktøyene i Dynamics 365 Commerce, velger du **Hjelp**-knappen (**?**) i øvre høyre hjørne, og deretter velger du **Personvern og informasjonskapsler**.</span><span class="sxs-lookup"><span data-stu-id="308c5-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="308c5-110">En ny fane åpnes med en kobling til [Microsofts personvernerklæring](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="308c5-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="308c5-111">Bygge en personvernspolicy-side for nettstedet ditt</span><span class="sxs-lookup"><span data-stu-id="308c5-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="308c5-112">I Dynamics 365 Commerce er det flere måter å gi brukerne av nettstedet ditt tilgang til personvernpolicyen.</span><span class="sxs-lookup"><span data-stu-id="308c5-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="308c5-113">Denne delen viser hvordan du bygger en personvernspolicy-side og deretter refererer til siden ved hjelp av et bunntekstfragment.</span><span class="sxs-lookup"><span data-stu-id="308c5-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="308c5-114">Veiledningen nedenfor er et eksempel som viser hvordan du bygger en generell personvernpolicy-side for et handelsområde.</span><span class="sxs-lookup"><span data-stu-id="308c5-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="308c5-115">Du er ansvarlig for å utforme og implementere en personvernpolicy-sideløsning som best dekker firmaets juridiske krav.</span><span class="sxs-lookup"><span data-stu-id="308c5-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="308c5-116">Hvis du vil starte, går du til webområdet du vil bygge en personvernspolicy-side for, i redigeringsverktøyene.</span><span class="sxs-lookup"><span data-stu-id="308c5-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="308c5-117">Opprett en mal</span><span class="sxs-lookup"><span data-stu-id="308c5-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="308c5-118">Hvis en mal som kan brukes til siden for personvernpolicy, allerede er opprettet, går du videre til delen [Bygge en personvern-side](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="308c5-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="308c5-119">Hvis du vil opprette en mal, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="308c5-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="308c5-120">Gå til **Maler \> Ny mal**.</span><span class="sxs-lookup"><span data-stu-id="308c5-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="308c5-121">Angi malnavnet, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="308c5-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="308c5-122">I malen legger du til eventuelle nødvendige moduler i de nødvendige sidesporene.</span><span class="sxs-lookup"><span data-stu-id="308c5-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="308c5-123">Hvis du vil ha veiledning, holder du pekeren over de røde utropstegnene.</span><span class="sxs-lookup"><span data-stu-id="308c5-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="308c5-124">**HTML-hode**-sporet kan for eksempel kreve en **Standard eksternt skript**-modul.</span><span class="sxs-lookup"><span data-stu-id="308c5-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="308c5-125">Legg til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="308c5-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="308c5-126">I **Standardside**-modulen i **Hoved**-sporet legger du til en **innholdsrik blokk**-modul.</span><span class="sxs-lookup"><span data-stu-id="308c5-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="308c5-127">I **Innholdsrik blokk**-modulen kan du legge til en **innholdsrik blokkelement**-modul.</span><span class="sxs-lookup"><span data-stu-id="308c5-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="308c5-128">Sjekk inn malen, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="308c5-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="308c5-129">Bygge en side med personvernpolicy</span><span class="sxs-lookup"><span data-stu-id="308c5-129">Build a privacy policy page</span></span>

<span data-ttu-id="308c5-130">Følg denne fremgangsmåten for å bygge en personvernspolicy-side.</span><span class="sxs-lookup"><span data-stu-id="308c5-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="308c5-131">Gå til **Sider \> Ny side**.</span><span class="sxs-lookup"><span data-stu-id="308c5-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="308c5-132">Velg malen for siden for personvernpolicy.</span><span class="sxs-lookup"><span data-stu-id="308c5-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="308c5-133">Angi et malnavn og en URL, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="308c5-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="308c5-134">I **Hoved**-sporet på den nye siden legger du til en **innholdsrik blokk**-modul.</span><span class="sxs-lookup"><span data-stu-id="308c5-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="308c5-135">I **Innholdsrik blokk**-modulen kan du legge til en **innholdsrik blokkelement**-modul.</span><span class="sxs-lookup"><span data-stu-id="308c5-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="308c5-136">Velg **Legg til datakilde** i egenskapsruten for **Innholdsrik blokk**-modulen, og velg deretter **Rikt tekstinnhold**.</span><span class="sxs-lookup"><span data-stu-id="308c5-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="308c5-137">I redigeringsprogrammet for rik tekst skriver du inn innholdet for siden for personvernpolicy.</span><span class="sxs-lookup"><span data-stu-id="308c5-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="308c5-138">Utvid redigeringsprogrammet for rik tekst til fullskjermmodus etter behov.</span><span class="sxs-lookup"><span data-stu-id="308c5-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="308c5-139">Når du er ferdig med å skrive inn innhold, velger du **Forhåndsvisning** for å forhåndsvise siden i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="308c5-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="308c5-140">Fyll ut eventuelle gjenværende tillegg til side- og modulegenskapene.</span><span class="sxs-lookup"><span data-stu-id="308c5-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="308c5-141">Sjekk inn personvernpolicy-siden, og publiser den.</span><span class="sxs-lookup"><span data-stu-id="308c5-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="308c5-142">Følg disse trinnene for å publisere URL-en for personvernpolicy-siden.</span><span class="sxs-lookup"><span data-stu-id="308c5-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="308c5-143">Gå til **URL-adresser**, og velg URL-adressen for personvernpolicy-siden.</span><span class="sxs-lookup"><span data-stu-id="308c5-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="308c5-144">Publiser den valgte URL-en.</span><span class="sxs-lookup"><span data-stu-id="308c5-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="308c5-145">Opprette en kobling til siden for personvernpolicy i en bunntekst</span><span class="sxs-lookup"><span data-stu-id="308c5-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="308c5-146">Du kan legge til en kobling til siden for personvernpolicy i et fragment.</span><span class="sxs-lookup"><span data-stu-id="308c5-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="308c5-147">På denne måten kan du dele koblingen og oppdatere den på tvers av flere sider på området ved å referere til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="308c5-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="308c5-148">Dette eksemplet viser hvordan du legger til en kobling til siden for personvernpolicy i et bunntekstfragment.</span><span class="sxs-lookup"><span data-stu-id="308c5-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="308c5-149">Hvis du vil legge til en kobling til et bunntekstfragment, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="308c5-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="308c5-150">Gå til **Sidefragmenter \> Nytt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="308c5-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="308c5-151">Velg **Bunntekst**-modulen, og skriv deretter inn et navn i feltet **Navn på sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="308c5-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="308c5-152">Legg til en **Bunntekstelement**-modul i **Bunntekstkategori**-sporet.</span><span class="sxs-lookup"><span data-stu-id="308c5-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="308c5-153">Velg **Koble til tekst** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="308c5-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="308c5-154">I dialogboksen **Koble til tekst** skriver du inn koblingsteksten og koblingsmålet på siden for personvernpolicy, og deretter klikker du **OK**.</span><span class="sxs-lookup"><span data-stu-id="308c5-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="308c5-155">For å få nettadressen til personvernpolicy-siden går du til **Sider**, personvernpolicy-siden, og kopierer URL-adressen fra egenskaper-ruten.</span><span class="sxs-lookup"><span data-stu-id="308c5-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="308c5-156">Lagre fragmentet, sjekk det inn, og publiser det.</span><span class="sxs-lookup"><span data-stu-id="308c5-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="308c5-157">Forhåndsvis fragmentet, og test koblingen til siden for personvernpolicy.</span><span class="sxs-lookup"><span data-stu-id="308c5-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="308c5-158">Fragmentet kan nå refereres i malen for andre områdesider.</span><span class="sxs-lookup"><span data-stu-id="308c5-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="308c5-159">Når det refereres til dette fragmentet i **Bunntekst**-modulen for en mal, vises koblingsreferansen på alle sider som er bygget ved hjelp av denne malen.</span><span class="sxs-lookup"><span data-stu-id="308c5-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="308c5-160">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="308c5-160">Additional resources</span></span>

[<span data-ttu-id="308c5-161">Oversikt over samsvar</span><span class="sxs-lookup"><span data-stu-id="308c5-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="308c5-162">Tilgjengelighetsfunksjoner og egenskaper</span><span class="sxs-lookup"><span data-stu-id="308c5-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="308c5-163">Samsvar for informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="308c5-163">Cookie compliance</span></span>](cookie-compliance.md)

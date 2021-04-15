---
title: Legge til en side med personvernpolicy
description: Dette emnet beskriver hvordan du legger til en side med personvernpolicy på området ditt i Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797533"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="7120f-103">Legge til en side for personvernpolicy</span><span class="sxs-lookup"><span data-stu-id="7120f-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7120f-104">Dette emnet beskriver hvordan du legger til en side med personvernpolicy på området ditt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7120f-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7120f-105">Overholdelse av personvern inkluderer organisatoriske tiltak som informerer brukerne om hvordan deres data samles inn og håndteres.</span><span class="sxs-lookup"><span data-stu-id="7120f-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="7120f-106">Brukere kan deretter bestemme hvordan de vil at deres personlige data skal håndteres og kan iverksette nødvendige tiltak.</span><span class="sxs-lookup"><span data-stu-id="7120f-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="7120f-107">Se gjennom Microsofts personvernerklæring i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7120f-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="7120f-108">Hvis du vil se gjennom Microsofts personvernerklæring mens du er logget på redigeringsverktøyene i Dynamics 365 Commerce, velger du **Hjelp**-knappen (**?**) i øvre høyre hjørne, og deretter velger du **Personvern og informasjonskapsler**.</span><span class="sxs-lookup"><span data-stu-id="7120f-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="7120f-109">En ny fane åpnes med en kobling til [Microsofts personvernerklæring](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="7120f-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="7120f-110">Bygge en personvernspolicy-side for nettstedet ditt</span><span class="sxs-lookup"><span data-stu-id="7120f-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="7120f-111">I Dynamics 365 Commerce er det flere måter å gi brukerne av nettstedet ditt tilgang til personvernpolicyen.</span><span class="sxs-lookup"><span data-stu-id="7120f-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="7120f-112">Denne delen viser hvordan du bygger en personvernspolicy-side og deretter refererer til siden ved hjelp av et bunntekstfragment.</span><span class="sxs-lookup"><span data-stu-id="7120f-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="7120f-113">Veiledningen nedenfor er et eksempel som viser hvordan du bygger en generell personvernpolicy-side for et handelsområde.</span><span class="sxs-lookup"><span data-stu-id="7120f-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="7120f-114">Du er ansvarlig for å utforme og implementere en personvernpolicy-sideløsning som best dekker firmaets juridiske krav.</span><span class="sxs-lookup"><span data-stu-id="7120f-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="7120f-115">Hvis du vil starte, går du til webområdet du vil bygge en personvernspolicy-side for, i redigeringsverktøyene.</span><span class="sxs-lookup"><span data-stu-id="7120f-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="7120f-116">Opprett en mal</span><span class="sxs-lookup"><span data-stu-id="7120f-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="7120f-117">Hvis en mal som kan brukes til siden for personvernpolicy, allerede er opprettet, går du videre til delen [Bygge en personvern-side](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="7120f-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="7120f-118">Hvis du vil opprette en mal, følger du trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="7120f-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="7120f-119">Gå til **Maler**, og velg deretter **Ny** for å opprette en sidemal.</span><span class="sxs-lookup"><span data-stu-id="7120f-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="7120f-120">I dialogboksen **Ny mal**, under **Malnavn**, angir du **Kampanjebannermal**, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7120f-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="7120f-121">I malen legger du til eventuelle nødvendige moduler i de nødvendige sidesporene.</span><span class="sxs-lookup"><span data-stu-id="7120f-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="7120f-122">Hvis du vil ha veiledning, holder du pekeren over de røde utropstegnene.</span><span class="sxs-lookup"><span data-stu-id="7120f-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="7120f-123">(**HTML-hode**-sporet kan for eksempel kreve en **Standard eksternt skript**-modul.)</span><span class="sxs-lookup"><span data-stu-id="7120f-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="7120f-124">Legg til en **Standardside**-modul i **Meldingstekst**-sporet.</span><span class="sxs-lookup"><span data-stu-id="7120f-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="7120f-125">I **Standardside**-modulen i **Hoved**-sporet legger du til en **innholdsrik blokk**-modul.</span><span class="sxs-lookup"><span data-stu-id="7120f-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="7120f-126">I **Innholdsrik blokk**-modulen kan du legge til en **innholdsrik blokkelement**-modul.</span><span class="sxs-lookup"><span data-stu-id="7120f-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="7120f-127">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="7120f-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="7120f-128">Bygge en side med personvernpolicy</span><span class="sxs-lookup"><span data-stu-id="7120f-128">Build a privacy policy page</span></span>

<span data-ttu-id="7120f-129">Følg denne fremgangsmåten for å bygge en personvernspolicy-side.</span><span class="sxs-lookup"><span data-stu-id="7120f-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="7120f-130">Gå til **Sider**, og velg deretter **Ny** for å opprette en side.</span><span class="sxs-lookup"><span data-stu-id="7120f-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="7120f-131">I dialogboksen **Velg en mal** velger du malen for siden for personvernpolicy.</span><span class="sxs-lookup"><span data-stu-id="7120f-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="7120f-132">Angi et sidenavn og en side-URL, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7120f-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="7120f-133">I **Hoved**-sporet på den nye siden legger du til en **innholdsrik blokk**-modul.</span><span class="sxs-lookup"><span data-stu-id="7120f-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="7120f-134">I **Innholdsrik blokk**-modulen kan du legge til en **innholdsrik blokkelement**-modul.</span><span class="sxs-lookup"><span data-stu-id="7120f-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="7120f-135">Velg **Legg til datakilde** i egenskapsruten for **Innholdsrik blokk**-modulen, og velg deretter **Rikt tekstinnhold**.</span><span class="sxs-lookup"><span data-stu-id="7120f-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="7120f-136">I redigeringsprogrammet for rik tekst skriver du inn innholdet for siden for personvernpolicy.</span><span class="sxs-lookup"><span data-stu-id="7120f-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="7120f-137">Utvid redigeringsprogrammet for rik tekst til fullskjermmodus etter behov.</span><span class="sxs-lookup"><span data-stu-id="7120f-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="7120f-138">Når du er ferdig med å skrive inn innhold, velger du **Forhåndsvisning** for å forhåndsvise siden i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="7120f-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="7120f-139">Fyll ut eventuelle gjenværende tillegg til side- og modulegenskapene.</span><span class="sxs-lookup"><span data-stu-id="7120f-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="7120f-140">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="7120f-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="7120f-141">Følg disse trinnene for å publisere URL-en for personvernpolicy-siden.</span><span class="sxs-lookup"><span data-stu-id="7120f-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="7120f-142">Gå til **URL-adresser**, og velg URL-adressen for personvernpolicy-siden.</span><span class="sxs-lookup"><span data-stu-id="7120f-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="7120f-143">Velg **Publiser** for å publisere den valgte URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="7120f-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="7120f-144">Opprette en kobling til siden for personvernpolicy i en bunntekst</span><span class="sxs-lookup"><span data-stu-id="7120f-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="7120f-145">Du kan legge til en kobling til siden for personvernpolicy i et fragment.</span><span class="sxs-lookup"><span data-stu-id="7120f-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="7120f-146">På denne måten kan du dele koblingen og oppdatere den på tvers av flere sider på området ved å referere til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="7120f-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="7120f-147">Dette eksemplet viser hvordan du legger til en kobling til siden for personvernpolicy i et bunntekstfragment.</span><span class="sxs-lookup"><span data-stu-id="7120f-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="7120f-148">Hvis du vil legge til en kobling til et bunntekstfragment, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="7120f-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="7120f-149">Gå til **Fragmenter**, og velg **Ny** for å opprette et sidefragment.</span><span class="sxs-lookup"><span data-stu-id="7120f-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="7120f-150">I dialogboksen **Nytt fragment** velger du **Bunntekst**-modulen.</span><span class="sxs-lookup"><span data-stu-id="7120f-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="7120f-151">Under **Navn på fragment** angir du et navn på fragmentet, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="7120f-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7120f-152">Legg til en **Bunntekstelement**-modul i **Bunntekstkategori**-sporet.</span><span class="sxs-lookup"><span data-stu-id="7120f-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="7120f-153">Velg **Koble til tekst** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="7120f-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="7120f-154">I dialogboksen **Koble til tekst** skriver du inn koblingsteksten og koblingsmålet på siden for personvernpolicy, og deretter klikker du **OK**.</span><span class="sxs-lookup"><span data-stu-id="7120f-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="7120f-155">For å få nettadressen til personvernpolicy-siden går du til **Sider**, personvernpolicy-siden, og kopierer URL-adressen fra egenskaper-ruten.</span><span class="sxs-lookup"><span data-stu-id="7120f-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="7120f-156">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.</span><span class="sxs-lookup"><span data-stu-id="7120f-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7120f-157">Forhåndsvis fragmentet, og test koblingen til siden for personvernpolicy.</span><span class="sxs-lookup"><span data-stu-id="7120f-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="7120f-158">Fragmentet kan nå refereres i malen for andre områdesider.</span><span class="sxs-lookup"><span data-stu-id="7120f-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="7120f-159">Når det refereres til dette fragmentet i **Bunntekst**-modulen for en mal, vises koblingsreferansen på alle sider som er bygget ved hjelp av denne malen.</span><span class="sxs-lookup"><span data-stu-id="7120f-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7120f-160">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7120f-160">Additional resources</span></span>

[<span data-ttu-id="7120f-161">Oversikt over samsvar</span><span class="sxs-lookup"><span data-stu-id="7120f-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="7120f-162">Funksjoner og egenskaper for tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="7120f-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="7120f-163">Informasjonskapselsamsvar</span><span class="sxs-lookup"><span data-stu-id="7120f-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="7120f-164">Erstatte bruker-IDer knyttet til sporede innholdsendringer</span><span class="sxs-lookup"><span data-stu-id="7120f-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

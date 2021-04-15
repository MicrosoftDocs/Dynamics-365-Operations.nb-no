---
title: Sosial deling-modul
description: Dette emnet dekker moduler for sosial deling for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795363"
---
# <a name="social-share-module"></a><span data-ttu-id="f4312-103">Modul for sosial deling</span><span class="sxs-lookup"><span data-stu-id="f4312-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f4312-104">Dette emnet dekker moduler for sosial deling for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f4312-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f4312-105">Med moduler for sosial deling kan brukere dele URL-adresser på områdesidene for e-handel på sosiale medier, for eksempel Facebook Twitter, Pinterest og LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="f4312-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="f4312-106">URL-adresser til områdesider kan også deles via e-post.</span><span class="sxs-lookup"><span data-stu-id="f4312-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="f4312-107">Moduler for sosial deling brukes vanligvis på sider for produktdetaljer (PDP-er) for å hjelpe brukere med å dele produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="f4312-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="f4312-108">Hver modul for sosialdeling er en beholder for varemoduler for sosial deling.</span><span class="sxs-lookup"><span data-stu-id="f4312-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="f4312-109">Hver varemodul for sosial deling kan konfigureres slik at den peker til et bestemt område for sosiale medier.</span><span class="sxs-lookup"><span data-stu-id="f4312-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="f4312-110">Integrering med Facebook, Twitter, Pinterest, LinkedIn og e-post støttes som standard.</span><span class="sxs-lookup"><span data-stu-id="f4312-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="f4312-111">Når en områdebruker velger et symbol for sosiale medier, startes en forekomst av HTML iFrame for det respektive området for sosialt medium.</span><span class="sxs-lookup"><span data-stu-id="f4312-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="f4312-112">I iFrame kan brukeren logge på og legge inn sideinnholdet de studerte.</span><span class="sxs-lookup"><span data-stu-id="f4312-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="f4312-113">Hver sosiale medieplattform kan spore informasjonskapsler, så denne modulen krever at områdebrukere godtar varslingen om samtykke for informasjonskapsel.</span><span class="sxs-lookup"><span data-stu-id="f4312-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="f4312-114">Når samtykke for informasjonskapsel ikke godkjennes, vil modulen være skjult på siden.</span><span class="sxs-lookup"><span data-stu-id="f4312-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="f4312-115">Hvis du vil ha mer informasjon, kan du se [Samsvar for informasjonskapsel](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="f4312-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="f4312-116">Illustrasjonen nedenfor viser et eksempel på en modul for sosial deling som brukes på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="f4312-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Eksempel på en modul for sosial deling](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="f4312-118">Egenskaper for modul for sosial deling</span><span class="sxs-lookup"><span data-stu-id="f4312-118">Social share module properties</span></span>

| <span data-ttu-id="f4312-119">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="f4312-119">Property name</span></span>             | <span data-ttu-id="f4312-120">Verdi</span><span class="sxs-lookup"><span data-stu-id="f4312-120">Value</span></span>                 | <span data-ttu-id="f4312-121">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f4312-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f4312-122">Overskrift</span><span class="sxs-lookup"><span data-stu-id="f4312-122">Caption</span></span>                  | <span data-ttu-id="f4312-123">Tekst</span><span class="sxs-lookup"><span data-stu-id="f4312-123">Text</span></span> | <span data-ttu-id="f4312-124">Denne egenskapen angir en tittel for modulen.</span><span class="sxs-lookup"><span data-stu-id="f4312-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="f4312-125">Retning</span><span class="sxs-lookup"><span data-stu-id="f4312-125">Orientation</span></span> | <span data-ttu-id="f4312-126">**Vannrett** eller **Loddrett**</span><span class="sxs-lookup"><span data-stu-id="f4312-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="f4312-127">Denne egenskapen definerer oppsettsretningen for elementene for sosiale medier.</span><span class="sxs-lookup"><span data-stu-id="f4312-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="f4312-128">Egenskaper for varemodul for sosial deling</span><span class="sxs-lookup"><span data-stu-id="f4312-128">Social share item module properties</span></span>
| <span data-ttu-id="f4312-129">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="f4312-129">Property name</span></span>             | <span data-ttu-id="f4312-130">Verdi</span><span class="sxs-lookup"><span data-stu-id="f4312-130">Value</span></span>                 | <span data-ttu-id="f4312-131">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f4312-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f4312-132">Sosiale medier</span><span class="sxs-lookup"><span data-stu-id="f4312-132">Social media</span></span>              | <span data-ttu-id="f4312-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span><span class="sxs-lookup"><span data-stu-id="f4312-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="f4312-134">En rullegardinmeny med en liste over plattformer for sosiale medier.</span><span class="sxs-lookup"><span data-stu-id="f4312-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="f4312-135">Ikon</span><span class="sxs-lookup"><span data-stu-id="f4312-135">Icon</span></span> |<span data-ttu-id="f4312-136">Bilde</span><span class="sxs-lookup"><span data-stu-id="f4312-136">Image</span></span>    | <span data-ttu-id="f4312-137">Dette vil være bildet som vil vises for de respektive sosiale mediene.</span><span class="sxs-lookup"><span data-stu-id="f4312-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="f4312-138">Den beste fremgangsmåten får du ved å se SDK for plattform for sosiale medier for det anbefalte bildet som skal brukes for hver plattform.</span><span class="sxs-lookup"><span data-stu-id="f4312-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="f4312-139">Legg til en modul for sosial deling i en kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="f4312-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="f4312-140">Hvis du vil legge til en modul for sosial deling i en kjøpsboksmodul, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="f4312-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="f4312-141">Velg **Sider** på Fabrikam-området, og velg deretter siden **DefaultPDP** for å åpne siden med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="f4312-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="f4312-142">I sporet **Kjøpsboks (obligatorisk)** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f4312-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4312-143">I dialogboksen **Legg til modul** velger du modulen **Sosial deling**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4312-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4312-144">I sporet **Sosial deling** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f4312-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4312-145">I dialogboksen **Legg til modul** velger du modulen **Sosial deling**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4312-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4312-146">I egenskapsruten for modulen **Sosial deling** velger du **Vannrett** under **Retning**.</span><span class="sxs-lookup"><span data-stu-id="f4312-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="f4312-147">Legg til en bildetekst etter behov.</span><span class="sxs-lookup"><span data-stu-id="f4312-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="f4312-148">I sporet **Sosial deling** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="f4312-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4312-149">I dialogboksen **Legg til modul** velger du modulen **SocialShareItem**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4312-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4312-150">I egenskapsruten for modulen **SocialShareItem** velger du **Facebook** under **Sosiale medier**.</span><span class="sxs-lookup"><span data-stu-id="f4312-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="f4312-151">I egenskapsruten for modulen **SocialShareItem** velger du **+ Legg til et bilde** under **Ikon**.</span><span class="sxs-lookup"><span data-stu-id="f4312-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="f4312-152">I dialogboksen **Medievelger** velger du logobildet Facebook, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4312-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="f4312-153">Hvis et logobilde for Facebook ikke finnes, velger du **Last opp nytt medieelement** for å laste opp et bilde.</span><span class="sxs-lookup"><span data-stu-id="f4312-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="f4312-154">Legg til og konfigurer flere forekomster av modulen **SocialShareItem** etter behov.</span><span class="sxs-lookup"><span data-stu-id="f4312-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="f4312-155">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="f4312-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f4312-156">Siden vil vise modulen for sodial deling.</span><span class="sxs-lookup"><span data-stu-id="f4312-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="f4312-157">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="f4312-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4312-158">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f4312-158">Additional resources</span></span>

[<span data-ttu-id="f4312-159">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="f4312-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f4312-160">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="f4312-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f4312-161">Informasjonskapselsamsvar</span><span class="sxs-lookup"><span data-stu-id="f4312-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
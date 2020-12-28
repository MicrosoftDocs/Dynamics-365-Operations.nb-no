---
title: Sosial deling-modul
description: Dette emnet dekker moduler for sosial deling for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 510ca8b14d8b5334e50aca1b15d636c65fcc9888
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4414774"
---
# <a name="social-share-module"></a><span data-ttu-id="9fc19-103">Sosial deling-modul</span><span class="sxs-lookup"><span data-stu-id="9fc19-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9fc19-104">Dette emnet dekker moduler for sosial deling for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9fc19-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9fc19-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="9fc19-105">Overview</span></span>

<span data-ttu-id="9fc19-106">Med moduler for sosial deling kan brukere dele URL-adresser på områdesidene for e-handel på sosiale medier, for eksempel Facebook Twitter, Pinterest og LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="9fc19-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="9fc19-107">URL-adresser til områdesider kan også deles via e-post.</span><span class="sxs-lookup"><span data-stu-id="9fc19-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="9fc19-108">Moduler for sosial deling brukes vanligvis på sider for produktdetaljer (PDP-er) for å hjelpe brukere med å dele produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="9fc19-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="9fc19-109">Hver modul for sosialdeling er en beholder for varemoduler for sosial deling.</span><span class="sxs-lookup"><span data-stu-id="9fc19-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="9fc19-110">Hver varemodul for sosial deling kan konfigureres slik at den peker til et bestemt område for sosiale medier.</span><span class="sxs-lookup"><span data-stu-id="9fc19-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="9fc19-111">Integrering med Facebook, Twitter, Pinterest, LinkedIn og e-post støttes som standard.</span><span class="sxs-lookup"><span data-stu-id="9fc19-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="9fc19-112">Når en områdebruker velger et symbol for sosiale medier, startes en forekomst av HTML iFrame for det respektive området for sosialt medium.</span><span class="sxs-lookup"><span data-stu-id="9fc19-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="9fc19-113">I iFrame kan brukeren logge på og legge inn sideinnholdet de studerte.</span><span class="sxs-lookup"><span data-stu-id="9fc19-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="9fc19-114">Hver sosiale medieplattform kan spore informasjonskapsler, så denne modulen krever at områdebrukere godtar varslingen om samtykke for informasjonskapsel.</span><span class="sxs-lookup"><span data-stu-id="9fc19-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="9fc19-115">Når samtykke for informasjonskapsel ikke godkjennes, vil modulen være skjult på siden.</span><span class="sxs-lookup"><span data-stu-id="9fc19-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="9fc19-116">Hvis du vil ha mer informasjon, kan du se [Samsvar for informasjonskapsel](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="9fc19-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="9fc19-117">Illustrasjonen nedenfor viser et eksempel på en modul for sosial deling som brukes på en produktdetaljside.</span><span class="sxs-lookup"><span data-stu-id="9fc19-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Eksempel på en modul for sosial deling](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="9fc19-119">Egenskaper for modul for sosial deling</span><span class="sxs-lookup"><span data-stu-id="9fc19-119">Social share module properties</span></span>

| <span data-ttu-id="9fc19-120">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="9fc19-120">Property name</span></span>             | <span data-ttu-id="9fc19-121">Verdi</span><span class="sxs-lookup"><span data-stu-id="9fc19-121">Value</span></span>                 | <span data-ttu-id="9fc19-122">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9fc19-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="9fc19-123">Overskrift</span><span class="sxs-lookup"><span data-stu-id="9fc19-123">Caption</span></span>                  | <span data-ttu-id="9fc19-124">Tekst</span><span class="sxs-lookup"><span data-stu-id="9fc19-124">Text</span></span> | <span data-ttu-id="9fc19-125">Denne egenskapen angir en tittel for modulen.</span><span class="sxs-lookup"><span data-stu-id="9fc19-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="9fc19-126">Retning</span><span class="sxs-lookup"><span data-stu-id="9fc19-126">Orientation</span></span> | <span data-ttu-id="9fc19-127">**Vannrett** eller **Loddrett**</span><span class="sxs-lookup"><span data-stu-id="9fc19-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="9fc19-128">Denne egenskapen definerer oppsettsretningen for elementene for sosiale medier.</span><span class="sxs-lookup"><span data-stu-id="9fc19-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="9fc19-129">Egenskaper for varemodul for sosial deling</span><span class="sxs-lookup"><span data-stu-id="9fc19-129">Social share item module properties</span></span>
| <span data-ttu-id="9fc19-130">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="9fc19-130">Property name</span></span>             | <span data-ttu-id="9fc19-131">Verdi</span><span class="sxs-lookup"><span data-stu-id="9fc19-131">Value</span></span>                 | <span data-ttu-id="9fc19-132">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9fc19-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="9fc19-133">Sosiale medier</span><span class="sxs-lookup"><span data-stu-id="9fc19-133">Social media</span></span>              | <span data-ttu-id="9fc19-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span><span class="sxs-lookup"><span data-stu-id="9fc19-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="9fc19-135">En rullegardinmeny med en liste over plattformer for sosiale medier.</span><span class="sxs-lookup"><span data-stu-id="9fc19-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="9fc19-136">Ikon</span><span class="sxs-lookup"><span data-stu-id="9fc19-136">Icon</span></span> |<span data-ttu-id="9fc19-137">Bilde</span><span class="sxs-lookup"><span data-stu-id="9fc19-137">Image</span></span>    | <span data-ttu-id="9fc19-138">Dette vil være bildet som vil vises for de respektive sosiale mediene.</span><span class="sxs-lookup"><span data-stu-id="9fc19-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="9fc19-139">Den beste fremgangsmåten får du ved å se SDK for plattform for sosiale medier for det anbefalte bildet som skal brukes for hver plattform.</span><span class="sxs-lookup"><span data-stu-id="9fc19-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="9fc19-140">Legg til en modul for sosial deling i en kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="9fc19-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="9fc19-141">Hvis du vil legge til en modul for sosial deling i en kjøpsboksmodul, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="9fc19-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="9fc19-142">Velg **Sider** på Fabrikam-området, og velg deretter siden **DefaultPDP** for å åpne siden med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="9fc19-142">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="9fc19-143">I sporet **Kjøpsboks (obligatorisk)** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-143">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9fc19-144">I dialogboksen **Legg til modul** velger du modulen **Sosial deling**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9fc19-145">I sporet **Sosial deling** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-145">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9fc19-146">I dialogboksen **Legg til modul** velger du modulen **Sosial deling**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9fc19-147">I egenskapsruten for modulen **Sosial deling** velger du **Vannrett** under **Retning**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-147">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="9fc19-148">Legg til en bildetekst etter behov.</span><span class="sxs-lookup"><span data-stu-id="9fc19-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="9fc19-149">I sporet **Sosial deling** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-149">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9fc19-150">I dialogboksen **Legg til modul** velger du modulen **SocialShareItem**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9fc19-151">I egenskapsruten for modulen **SocialShareItem** velger du **Facebook** under **Sosiale medier**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-151">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="9fc19-152">I egenskapsruten for modulen **SocialShareItem** velger du **+ Legg til et bilde** under **Ikon**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-152">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="9fc19-153">I dialogboksen **Medievelger** velger du logobildet Facebook, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fc19-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="9fc19-154">Hvis et logobilde for Facebook ikke finnes, velger du **Last opp nytt medieelement** for å laste opp et bilde.</span><span class="sxs-lookup"><span data-stu-id="9fc19-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="9fc19-155">Legg til og konfigurer flere forekomster av modulen **SocialShareItem** etter behov.</span><span class="sxs-lookup"><span data-stu-id="9fc19-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="9fc19-156">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="9fc19-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="9fc19-157">Siden vil vise modulen for sodial deling.</span><span class="sxs-lookup"><span data-stu-id="9fc19-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="9fc19-158">Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="9fc19-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fc19-159">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9fc19-159">Additional resources</span></span>

[<span data-ttu-id="9fc19-160">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="9fc19-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9fc19-161">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="9fc19-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9fc19-162">Informasjonskapselsamsvar</span><span class="sxs-lookup"><span data-stu-id="9fc19-162">Cookie compliance</span></span>](cookie-compliance.md)

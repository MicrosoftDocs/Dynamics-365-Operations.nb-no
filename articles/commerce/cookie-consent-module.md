---
title: Samtykkemodul for informasjonskapsel
description: Dette emnet dekker samtykkemoduler for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 2f0118b197f465113bb894e3e57b3e682e04ef36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796009"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="0d2d7-103">Samtykkemodul for informasjonskapsler</span><span class="sxs-lookup"><span data-stu-id="0d2d7-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d2d7-104">Dette emnet dekker samtykkemoduler for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0d2d7-105">Samtykkemodulen for informasjonskapsel ber områdebrukere uttrykkelig om å gi samtykke for å tillate informasjonskapsler for alle funksjoner eller moduler som sporer informasjonskapsler for nettlesere.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="0d2d7-106">Samtykke er nødvendig første gang en områdebruker blar seg frem til et område i en ny nettleserøkt.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="0d2d7-107">Når samtykke er mottatt, spores det, og områdebrukeren blir ikke spurt om samtykke på nytt.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="0d2d7-108">Hvis du vil ha mer informasjon, kan du se [Samsvar for informasjonskapsel](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d7-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="0d2d7-109">Hvis godkjenning av informasjonskapsler for område ikke er mottatt, vil ingen av funksjonene eller modulene som krever samtykke for informasjonskapsel, vises på siden.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="0d2d7-110">Betalingsmodulen, modulen for sosial deling og foretrukkede butikkfunksjon vil for eksempel kreve samtykke for informasjonskapsel, og vil ikke bli gjengitt hvis samtykke for områdebruker ikke er mottatt.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="0d2d7-111">En samtykkemodul for informasjonskapsel kan konfigureres i en sides topptekstfragment, slik at den kan håndheves når siden lastes.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="0d2d7-112">Samtykkemodulen for informasjonskapsel bør ha en tydelig melding som informerer områdebrukeren om bruk av informasjonskapsler på området, og som skal gi en kobling til områdets personvernside.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="0d2d7-113">Illustrasjonen nedenfor fremhever et eksempel på en melding fra informasjonskapselen med en kobling til områdets side for personvernpolicy som vises i toppteksten på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="0d2d7-114">![Eksempel på en samtykkemodul for informasjonskapsel](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="0d2d7-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="0d2d7-115">Egenskaper for samtykkemodul for informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="0d2d7-115">Cookie consent module properties</span></span>

| <span data-ttu-id="0d2d7-116">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="0d2d7-116">Property name</span></span>             | <span data-ttu-id="0d2d7-117">Verdi</span><span class="sxs-lookup"><span data-stu-id="0d2d7-117">Value</span></span>                 | <span data-ttu-id="0d2d7-118">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0d2d7-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="0d2d7-119">Rik tekst</span><span class="sxs-lookup"><span data-stu-id="0d2d7-119">Rich Text</span></span>                  | <span data-ttu-id="0d2d7-120">Rik tekst</span><span class="sxs-lookup"><span data-stu-id="0d2d7-120">Rich Text</span></span> | <span data-ttu-id="0d2d7-121">Angir en varsling i rik tekst til områdebrukere om at området bruker informasjonskapsler for nettleser, og at brukere bør godta bruk av informasjonskapsler for at området skal fungere optimalt.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="0d2d7-122">Koblinger</span><span class="sxs-lookup"><span data-stu-id="0d2d7-122">Links</span></span> | <span data-ttu-id="0d2d7-123">URL</span><span class="sxs-lookup"><span data-stu-id="0d2d7-123">URL</span></span> | <span data-ttu-id="0d2d7-124">Én eller flere koblinger kan legges til på områdets personvernside som beskriver typene informasjonskapsler som spores på området.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="0d2d7-125">Legg til en tillatelsesmodul for informasjonskapsler på områdesider</span><span class="sxs-lookup"><span data-stu-id="0d2d7-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="0d2d7-126">Hvis du vil legge til en samtykkemodul for informasjonskapsel på flere områdesider, kan den legges til i et delt topptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="0d2d7-127">Når topptekstfragmentet blir lagt til på alle områdesider, vil det automatisk vises en varsling om samtykke for informasjonskapsel første gang en områdebruker går til en områdeside.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="0d2d7-128">Hvis du vil ha mer informasjon om topptekstfragmenter og moduler, kan du se [Topptekstmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d7-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d2d7-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0d2d7-129">Additional resources</span></span>

[<span data-ttu-id="0d2d7-130">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="0d2d7-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0d2d7-131">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="0d2d7-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="0d2d7-132">Informasjonskapselsamsvar</span><span class="sxs-lookup"><span data-stu-id="0d2d7-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
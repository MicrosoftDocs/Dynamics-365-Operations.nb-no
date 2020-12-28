---
title: Samtykkemodul for informasjonskapsel
description: Dette emnet dekker samtykkemoduler for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414543"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="62f12-103">Samtykkemodul for informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="62f12-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62f12-104">Dette emnet dekker samtykkemoduler for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="62f12-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="62f12-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="62f12-105">Overview</span></span>

<span data-ttu-id="62f12-106">Samtykkemodulen for informasjonskapsel ber områdebrukere uttrykkelig om å gi samtykke for å tillate informasjonskapsler for alle funksjoner eller moduler som sporer informasjonskapsler for nettlesere.</span><span class="sxs-lookup"><span data-stu-id="62f12-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="62f12-107">Samtykke er nødvendig første gang en områdebruker blar seg frem til et område i en ny nettleserøkt.</span><span class="sxs-lookup"><span data-stu-id="62f12-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="62f12-108">Når samtykke er mottatt, spores det, og områdebrukeren blir ikke spurt om samtykke på nytt.</span><span class="sxs-lookup"><span data-stu-id="62f12-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="62f12-109">Hvis du vil ha mer informasjon, kan du se [Samsvar for informasjonskapsel](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="62f12-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="62f12-110">Hvis godkjenning av informasjonskapsler for område ikke er mottatt, vil ingen av funksjonene eller modulene som krever samtykke for informasjonskapsel, vises på siden.</span><span class="sxs-lookup"><span data-stu-id="62f12-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="62f12-111">Betalingsmodulen, modulen for sosial deling og foretrukkede butikkfunksjon vil for eksempel kreve samtykke for informasjonskapsel, og vil ikke bli gjengitt hvis samtykke for områdebruker ikke er mottatt.</span><span class="sxs-lookup"><span data-stu-id="62f12-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="62f12-112">En samtykkemodul for informasjonskapsel kan konfigureres i en sides topptekstfragment, slik at den kan håndheves når siden lastes.</span><span class="sxs-lookup"><span data-stu-id="62f12-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="62f12-113">Samtykkemodulen for informasjonskapsel bør ha en tydelig melding som informerer områdebrukeren om bruk av informasjonskapsler på området, og som skal gi en kobling til områdets personvernside.</span><span class="sxs-lookup"><span data-stu-id="62f12-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="62f12-114">Illustrasjonen nedenfor fremhever et eksempel på en melding fra informasjonskapselen med en kobling til områdets side for personvernpolicy som vises i toppteksten på en områdeside.</span><span class="sxs-lookup"><span data-stu-id="62f12-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="62f12-115">![Eksempel på en samtykkemodul for informasjonskapsel](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="62f12-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="62f12-116">Egenskaper for samtykkemodul for informasjonskapsel</span><span class="sxs-lookup"><span data-stu-id="62f12-116">Cookie consent module properties</span></span>

| <span data-ttu-id="62f12-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="62f12-117">Property name</span></span>             | <span data-ttu-id="62f12-118">Verdi</span><span class="sxs-lookup"><span data-stu-id="62f12-118">Value</span></span>                 | <span data-ttu-id="62f12-119">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="62f12-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="62f12-120">Rik tekst</span><span class="sxs-lookup"><span data-stu-id="62f12-120">Rich Text</span></span>                  | <span data-ttu-id="62f12-121">Rik tekst</span><span class="sxs-lookup"><span data-stu-id="62f12-121">Rich Text</span></span> | <span data-ttu-id="62f12-122">Angir en varsling i rik tekst til områdebrukere om at området bruker informasjonskapsler for nettleser, og at brukere bør godta bruk av informasjonskapsler for at området skal fungere optimalt.</span><span class="sxs-lookup"><span data-stu-id="62f12-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="62f12-123">Koblinger</span><span class="sxs-lookup"><span data-stu-id="62f12-123">Links</span></span> | <span data-ttu-id="62f12-124">URL</span><span class="sxs-lookup"><span data-stu-id="62f12-124">URL</span></span> | <span data-ttu-id="62f12-125">Én eller flere koblinger kan legges til på områdets personvernside som beskriver typene informasjonskapsler som spores på området.</span><span class="sxs-lookup"><span data-stu-id="62f12-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="62f12-126">Legg til en tillatelsesmodul for informasjonskapsler på områdesider</span><span class="sxs-lookup"><span data-stu-id="62f12-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="62f12-127">Hvis du vil legge til en samtykkemodul for informasjonskapsel på flere områdesider, kan den legges til i et delt topptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="62f12-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="62f12-128">Når topptekstfragmentet blir lagt til på alle områdesider, vil det automatisk vises en varsling om samtykke for informasjonskapsel første gang en områdebruker går til en områdeside.</span><span class="sxs-lookup"><span data-stu-id="62f12-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="62f12-129">Hvis du vil ha mer informasjon om topptekstfragmenter og moduler, kan du se [Topptekstmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="62f12-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62f12-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="62f12-130">Additional resources</span></span>

[<span data-ttu-id="62f12-131">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="62f12-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="62f12-132">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="62f12-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="62f12-133">Informasjonskapselsamsvar</span><span class="sxs-lookup"><span data-stu-id="62f12-133">Cookie compliance</span></span>](cookie-compliance.md)

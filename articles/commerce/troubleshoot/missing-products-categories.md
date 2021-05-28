---
title: Produkter og kategorier mangler etter miljøkopi
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når produkter og kategorier mangler etter at et område er kopiert mellom miljøer eller innenfor samme miljø.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022404"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="e99d9-103">Produkter og kategorier som mangler etter miljøkopi</span><span class="sxs-lookup"><span data-stu-id="e99d9-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e99d9-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når produkter og kategorier mangler etter at et område er kopiert mellom miljøer eller innenfor samme miljø.</span><span class="sxs-lookup"><span data-stu-id="e99d9-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="e99d9-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e99d9-105">Description</span></span>

<span data-ttu-id="e99d9-106">Når et område kopieres fra ett miljø til et annet eller i samme miljø, mangler produktene og kategoriene fra området.</span><span class="sxs-lookup"><span data-stu-id="e99d9-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="e99d9-107">Produktene og kategoriene mangler i e-handelbutikken og fra kategorien **Produkter** i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="e99d9-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="e99d9-108">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="e99d9-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="e99d9-109">Tilordne kanaldriftsenhetsnummeret til et nykopiert område i Commerce-områdebyggeren</span><span class="sxs-lookup"><span data-stu-id="e99d9-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="e99d9-110">Hvis du vil tilordne kanaldriftsenhetsnummeret (OUN) til et nykopiert område i Commerce-områdebyggeren, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="e99d9-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e99d9-111">Velg det nykopierte området.</span><span class="sxs-lookup"><span data-stu-id="e99d9-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="e99d9-112">Velg **Kanaler** under **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="e99d9-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="e99d9-113">Ved siden av kanalnavnet velger du ellipsen (**...**), og deretter velger du **Endre kanal for nettbutikk**.</span><span class="sxs-lookup"><span data-stu-id="e99d9-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="e99d9-114">Velg kanalen du vil tilordne til det nykopierte området, i dialogboksen **Endre kanal for nettbutikk**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e99d9-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="e99d9-115">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="e99d9-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e99d9-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e99d9-116">Additional resources</span></span>

[<span data-ttu-id="e99d9-117">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="e99d9-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)

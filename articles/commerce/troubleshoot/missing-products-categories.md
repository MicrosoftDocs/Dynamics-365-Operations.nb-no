---
title: Produkter og kategorier mangler etter miljøkopi
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når produkter og kategorier mangler etter at et område er kopiert mellom miljøer eller innenfor samme miljø.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 527fd0fa62775f65f61b538474b1d45d1a0155ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801729"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="402ec-103">Produkter og kategorier som mangler etter miljøkopi</span><span class="sxs-lookup"><span data-stu-id="402ec-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="402ec-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når produkter og kategorier mangler etter at et område er kopiert mellom miljøer eller innenfor samme miljø.</span><span class="sxs-lookup"><span data-stu-id="402ec-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="402ec-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="402ec-105">Description</span></span>

<span data-ttu-id="402ec-106">Når et område kopieres fra ett miljø til et annet eller i samme miljø, mangler produktene og kategoriene fra området.</span><span class="sxs-lookup"><span data-stu-id="402ec-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="402ec-107">Produktene og kategoriene mangler i e-handelbutikken og fra kategorien **Produkter** i Commerce-områdebyggeren.</span><span class="sxs-lookup"><span data-stu-id="402ec-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="402ec-108">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="402ec-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="402ec-109">Tilordne kanaldriftsenhetsnummeret til et nykopiert område i Commerce-områdebyggeren</span><span class="sxs-lookup"><span data-stu-id="402ec-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="402ec-110">Hvis du vil tilordne kanaldriftsenhetsnummeret (OUN) til et nykopiert område i Commerce-områdebyggeren, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="402ec-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="402ec-111">Velg det nykopierte området.</span><span class="sxs-lookup"><span data-stu-id="402ec-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="402ec-112">Velg **Kanaler** under **Områdeinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="402ec-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="402ec-113">Ved siden av kanalnavnet velger du ellipsen (**...**), og deretter velger du **Endre kanal for nettbutikk**.</span><span class="sxs-lookup"><span data-stu-id="402ec-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="402ec-114">Velg kanalen du vil tilordne til det nykopierte området, i dialogboksen **Endre kanal for nettbutikk**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="402ec-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="402ec-115">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="402ec-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="402ec-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="402ec-116">Additional resources</span></span>

[<span data-ttu-id="402ec-117">Knytte et Dynamics 365 Commerce-nettsted til en nettkanal</span><span class="sxs-lookup"><span data-stu-id="402ec-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)

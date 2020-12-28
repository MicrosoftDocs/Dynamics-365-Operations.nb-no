---
title: Definere strekkoder
description: Denne artikkelen beskriver hvordan du bruker strekkoder i Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0785f499a3e106e36b803ae61a9acbdbb072ce17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414741"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="871a5-103">Definere strekkoder</span><span class="sxs-lookup"><span data-stu-id="871a5-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="871a5-104">Denne artikkelen beskriver hvordan du bruker strekkoder i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="871a5-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="871a5-105">Du kan bruke strekkoder til å kjøpe og selge produkter, spore produktvarianter og sette opp kunder og ansatte.</span><span class="sxs-lookup"><span data-stu-id="871a5-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="871a5-106">Du kan også bruke strekkoder til å utstede og godkjenne kuponger, gavekort, og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="871a5-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="871a5-107">Du kan definere produkter slik at de har standard strekkoder eller egendefinerte, interne strekkoder.</span><span class="sxs-lookup"><span data-stu-id="871a5-107">You can set up products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="871a5-108">Produkter kan ha flere enn én strekkode.</span><span class="sxs-lookup"><span data-stu-id="871a5-108">Products can have more than one bar code.</span></span> <span data-ttu-id="871a5-109">For eksempel kan et produkt ha flere strekkoder hvis det kommer fra ulike produsenter, eller hvis det har varianter som er basert på størrelse, stil eller farge.</span><span class="sxs-lookup"><span data-stu-id="871a5-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="871a5-110">Strekkoder kan inneholde vekt eller pris for produktet.</span><span class="sxs-lookup"><span data-stu-id="871a5-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="871a5-111">Strekkodemasker er maler som brukes til å opprette strekkoder.</span><span class="sxs-lookup"><span data-stu-id="871a5-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="871a5-112">Hvis du tilordner en unik strekkode til hver variantkombinasjon kan du skanne strekkoden i kassen og la programmet bestemme hvilken variant av produktet som selges.</span><span class="sxs-lookup"><span data-stu-id="871a5-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="871a5-113">Du kan også samle inn og vise statistikk om salg etter variant.</span><span class="sxs-lookup"><span data-stu-id="871a5-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="871a5-114">Hver størrelses-, farge- og stilgruppe kan tilordnes et unikt nummer som identifiserer denne gruppen i strekkoden.</span><span class="sxs-lookup"><span data-stu-id="871a5-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="871a5-115">Commerce bruker strekkodemasken til å generere strekkoder automatisk for hver variantkombinasjon.</span><span class="sxs-lookup"><span data-stu-id="871a5-115">Commerce uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="871a5-116">Denne funksjonaliteten kan være nyttig hvis det finnes mange størrelser, farger og stiler, fordi antall kombinasjoner øker betraktelig med hver tilføyde variantkode.</span><span class="sxs-lookup"><span data-stu-id="871a5-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="871a5-117">Hvis denne funksjonaliteten ikke brukes, må strekkodene tilordnes manuelt til hver kombinasjon som representerer en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="871a5-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="871a5-118">Du kan også opprette strekkoder manuelt eller automatisk.</span><span class="sxs-lookup"><span data-stu-id="871a5-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="871a5-119">For å opprette strekkoder kan du fullføre følgende oppgaver i rekkefølgen de er oppført.</span><span class="sxs-lookup"><span data-stu-id="871a5-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="871a5-120">[Definere tegn for strekkodemaske](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="871a5-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="871a5-121">[Definere strekkodemasker](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="871a5-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="871a5-122">Konfigurere strekkodeoppsett.</span><span class="sxs-lookup"><span data-stu-id="871a5-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="871a5-123">[Opprette strekkoder for produkter](../supply-chain/pim/tasks/create-bar-code-product.md).</span><span class="sxs-lookup"><span data-stu-id="871a5-123">[Create bar codes for products](../supply-chain/pim/tasks/create-bar-code-product.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="871a5-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="871a5-124">Additional resources</span></span>

[<span data-ttu-id="871a5-125">Definere strekkodemasker</span><span class="sxs-lookup"><span data-stu-id="871a5-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)

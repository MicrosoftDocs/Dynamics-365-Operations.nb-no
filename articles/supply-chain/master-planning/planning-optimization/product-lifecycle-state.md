---
title: Utelat produkter som har spesifikke produktstatuser
description: Dette emnet forklarer hvordan du utelater produkter basert på statusen deres når planleggingsoptimaliseringsfunksjonaliteten brukes.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1e0c734db763ffa69e2d6540a07d5fa04c22ea1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227824"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="9c208-103">Utelat produkter som har spesifikke produktstatuser</span><span class="sxs-lookup"><span data-stu-id="9c208-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c208-104">Frigitte produkter og frigitte produktversjoner omfatter et felt for **produktstatus**.</span><span class="sxs-lookup"><span data-stu-id="9c208-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="9c208-105">I dette feltet kan du kontrollere, blant annet hvilke produkter som er inkludert under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="9c208-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="9c208-106">Du kan legge til, fjerne og redigere statuser etter behov ved å gå til **Produktinformasjonsbehandling \> Oppsett \> Produktstatus**.</span><span class="sxs-lookup"><span data-stu-id="9c208-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="9c208-107">For hver produktstatus setter du alternativet **Er aktiv for planlegging** til *Ja* hvis produkter som har denne statusen, skal inkluderes under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="9c208-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="9c208-108">Når alternativet er satt til *Nei*, blir tilknyttede produkter og varianter utelatt fra all hovedplanlegging og alle beregninger på stykklistenivå.</span><span class="sxs-lookup"><span data-stu-id="9c208-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="9c208-109">Frigitte produkter og varianter der feltet **Produktstatus** er tomt, behandles som om de har en produktstatus der alternativet **Er aktiv for planlegging** er satt til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="9c208-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="9c208-110">De blir med andre ord inkludert under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="9c208-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="9c208-111">For å unngå unødvendige forsyningsforslag anbefaler vi sterkt at du knytter alle foreldede, frigitte produkter og varianter til en produktstatus der alternativet **Er aktiv for planlegging** er satt til *Nei*.</span><span class="sxs-lookup"><span data-stu-id="9c208-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="9c208-112">Denne fremgangsmåten er spesielt viktig når du arbeider med produktkonfigurasjonsvarianter som ikke kan brukes på nytt, fordi det vil bidra til å forhindre avfall.</span><span class="sxs-lookup"><span data-stu-id="9c208-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9c208-113">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="9c208-113">Related resources</span></span>

<span data-ttu-id="9c208-114">Hvis du vil ha mer informasjon om produktstatuser, kan du se [Oversikt over produktstatus](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="9c208-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="9c208-115">Hvis du vil ha mer informasjon som omfatter fremgangsmåte for å bruke produktstatuser til å utelate produkter fra hovedplanlegging og stykklistenivåberegninger, kan du se [Opprette en produktstatus for å utelukke produkter fra hovedplanlegging](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="9c208-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Produksjonsutleveringssted
description: Dette emnet beskriver hierarkiet som brukes til å identifisere produksjonsutleveringsstedet.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4002bf7dddb196edf306268ecc16e1bfa5d6d1e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434589"
---
# <a name="production-output-location"></a><span data-ttu-id="ba58d-103">Produksjonsutleveringssted</span><span class="sxs-lookup"><span data-stu-id="ba58d-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba58d-104">Dette emnet beskriver hierarkiet som brukes til å identifisere produksjonsutleveringsstedet.</span><span class="sxs-lookup"><span data-stu-id="ba58d-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="ba58d-105">Produksjonsutleveringsstedet er stedet der en ferdig vare først lagres etter at den er produsert.</span><span class="sxs-lookup"><span data-stu-id="ba58d-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="ba58d-106">Dette stedet er vanligvis nær produksjonsprosessen som produserer den ferdige varen.</span><span class="sxs-lookup"><span data-stu-id="ba58d-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="ba58d-107">Produksjonsutleveringsstedet brukes som et midlertidig lager for materialet før det flyttes til forsendelsesområdet, et lagringssted, et produksjonsinnleveringssted for en produksjonsprosess nedstrøms og så videre.</span><span class="sxs-lookup"><span data-stu-id="ba58d-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="ba58d-108">Et standard produksjonsutleveringssted angis når ferdige varer rapporteres på en produksjonsordre eller partiordre.</span><span class="sxs-lookup"><span data-stu-id="ba58d-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="ba58d-109">Det følgende hierarkiet brukes til å identifisere dette utleveringsstedet:</span><span class="sxs-lookup"><span data-stu-id="ba58d-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="ba58d-110">Bruk utleveringsstedet som er definert i produksjonsordrer eller partiordrehodet.</span><span class="sxs-lookup"><span data-stu-id="ba58d-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="ba58d-111">Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert på ressursen som brukes av den siste operasjonen som er definert i produksjonsruten.</span><span class="sxs-lookup"><span data-stu-id="ba58d-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="ba58d-112">Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert på ressursgruppen som brukes av ressursen for den siste operasjonen som er definert i produksjonsruten.</span><span class="sxs-lookup"><span data-stu-id="ba58d-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="ba58d-113">Hvis det ikke finnes noe sted der, kan du bruke utleveringsstedet som er definert i lageret som er definert for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="ba58d-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="ba58d-114">Et standard produksjonsutleveringssted angis bare for produkter som er definert ved hjelp av avanserte lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="ba58d-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="ba58d-115">Når denne typen vare er rapportert som fullført, opprettes lagerarbeid av typen **Plasser ferdigvarer** eller **Plasser koprodukt og biprodukt**.</span><span class="sxs-lookup"><span data-stu-id="ba58d-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="ba58d-116">Denne typen arbeid bruker produksjonsutleveringsstedet som plukkested.</span><span class="sxs-lookup"><span data-stu-id="ba58d-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="ba58d-117">Plasseringsstedet bestemmes av instruksjonene for stedet.</span><span class="sxs-lookup"><span data-stu-id="ba58d-117">The put-away location is determined by the location directives.</span></span>

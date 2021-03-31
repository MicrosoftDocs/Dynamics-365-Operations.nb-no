---
title: Nedbryting av en stykklisteversjon
description: Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220854"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="7db1c-103">Nedbryting av en stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="7db1c-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7db1c-104">Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7db1c-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="7db1c-105">En vellykket behovsnedbrytning av en stykklisteversjon resulterer i et behov for hver stykklistelinjevare på et bestemte område eller muligens ved et bestemt lager.</span><span class="sxs-lookup"><span data-stu-id="7db1c-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="7db1c-106">For en områdespesifikk stykkliste kan det være definert et bestemt lager for hver stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="7db1c-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="7db1c-107">Varens dimensjonsinnstillinger angir dessuten om lageret er påkrevd for hver stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="7db1c-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="7db1c-108">Det resulterende behovet for hver stykklistelinje blir deretter utgangspunktet for en ytterligere behovsnedbrytning.</span><span class="sxs-lookup"><span data-stu-id="7db1c-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="7db1c-109">Dette hovedplanleggingsscenariet omfatter følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="7db1c-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="7db1c-110">Områdedimensjonen er obligatorisk, og må angis på behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="7db1c-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="7db1c-111">Områdedimensjonen er konsekvent.</span><span class="sxs-lookup"><span data-stu-id="7db1c-111">The site dimension is consistent.</span></span> <span data-ttu-id="7db1c-112">Området for behovet på lavere nivå, er derfor det samme som området på den innledende behovstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="7db1c-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="7db1c-113">Illustrasjonen nedenfor viser hvordan behovsnedbrytningen for hovedplanlegging foregår.</span><span class="sxs-lookup"><span data-stu-id="7db1c-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Behovsnedbryting ved hjelp av stykklisteversjon](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="7db1c-115">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7db1c-115">Additional resources</span></span>
--------

[<span data-ttu-id="7db1c-116">Fastslå stykklisteversjonen</span><span class="sxs-lookup"><span data-stu-id="7db1c-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="7db1c-117">Oversikt over hovedplanlegging og multisite-funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="7db1c-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
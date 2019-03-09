---
title: Lagerbrikkeopptelling
description: Denne artikkelen inneholder informasjon om brikkeopptelling, som du bruker til å sammenligne det faktiske innholdet i et lager med lagerbeholdningen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dff899d0e6d94287c0f1924fe1787189d79c09f4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "328959"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="ca8a0-103">Lagerbrikkeopptelling</span><span class="sxs-lookup"><span data-stu-id="ca8a0-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="ca8a0-104">Denne artikkelen inneholder informasjon om brikkeopptelling, som du bruker til å sammenligne det faktiske innholdet i et lager med lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="ca8a0-105">Ved å lage linjer på **Brikkeopptelling**-siden plasserer du et brikkenummer på hver lagervare, for eksempel et tall fra 1 til 500.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="ca8a0-106">Når du teller, angir du varenummeret og antallet på en tilsvarende brikke.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="ca8a0-107">Denne brikken kan deretter brukes som grunnlag for inndata i brikkeopptellingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="ca8a0-108">Når du har postert brikkeopptellingsjournalen, opprettes en ny opptellingsjournal på **Opptelling**-siden.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="ca8a0-109">Den nye journalen er basert på brikkeopptellingsjournallinjene du opprettet.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="ca8a0-110">Hvis du teller varer ved hjelp av brikker etter en bestemt lagerdimensjon, velger du dimensjonen på **Visningsdimensjoner**-siden som vises når du oppretter brikkeopptellingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="ca8a0-111">Hvis du for eksempel vil telle varer på et bestemt lager, merker du av for **Lager**.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="ca8a0-112">Hvis glidebryteren **Lås varer under opptelling** på siden **Parametere for beholdnings- og lagerstyring** er valgt, kan ikke varer oppdateres fysisk under tellingen.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="ca8a0-113">Varer i brikkeopptellingsjournaler er imidlertid ikke låst under telling.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="ca8a0-114">Lagertransaksjoner opprettes ikke før brikkeopptellingslinjene er postert og overført til en opptellingsjournal.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="ca8a0-115">Hvis brikker er angitt i tilfeldig rekkefølge og du vil vite hvilke brikker som mangler, klikker du kolonnehodet **Brikke** for å sortere linjene etter brikke.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ca8a0-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ca8a0-116">Additional resources</span></span>
--------

[<span data-ttu-id="ca8a0-117">Syklustelling</span><span class="sxs-lookup"><span data-stu-id="ca8a0-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)

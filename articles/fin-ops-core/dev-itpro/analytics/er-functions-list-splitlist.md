---
title: SPLITLIST ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLITLIST.
author: NickSelin
ms.date: 03/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745575"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="4c5e3-103">SPLITLIST ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="4c5e3-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c5e3-104">`SPLITLIST`-funksjonen deler den angitte listen i underlister (eller grupper), der hver inneholder det angitte antallet poster.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="4c5e3-105">Deretter returneres resultatet som en ny *postliste*-verdi som består av partiene.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4c5e3-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="4c5e3-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="4c5e3-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="4c5e3-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="4c5e3-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4c5e3-108">Arguments</span></span>

<span data-ttu-id="4c5e3-109">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="4c5e3-109">`list`: *Record list*</span></span>

<span data-ttu-id="4c5e3-110">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="4c5e3-111">`number`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="4c5e3-111">`number`: *Integer*</span></span>

<span data-ttu-id="4c5e3-112">Maksimalt antall poster per parti.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="4c5e3-113">`on-demand reading flag`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="4c5e3-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="4c5e3-114">En *boolsk* verdi som angir om elementer i underlister skal genereres ved behov.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="4c5e3-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="4c5e3-115">Return values</span></span>

<span data-ttu-id="4c5e3-116">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="4c5e3-116">*Record list*</span></span>

<span data-ttu-id="4c5e3-117">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4c5e3-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="4c5e3-118">Usage notes</span></span>

<span data-ttu-id="4c5e3-119">Listen over partier som returneres, inneholder følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="4c5e3-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="4c5e3-120">**Verdi:** *Liste*</span><span class="sxs-lookup"><span data-stu-id="4c5e3-120">**Value:** *List*</span></span>

    <span data-ttu-id="4c5e3-121">Listen over oppføringer som tilhører gjeldende parti.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="4c5e3-122">**BatchNumber:** *Heltall*</span><span class="sxs-lookup"><span data-stu-id="4c5e3-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="4c5e3-123">Nummeret for gjeldende parti i den returnerte listen.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="4c5e3-124">Når flagget for lesing ved behov er satt til **Sann**, genereres underlister etter forespørsel som tillater reduksjon i minneforbruk, men som kan føre til ytelsesreduksjon hvis elementer ikke brukes sekvensielt.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="4c5e3-125">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4c5e3-125">Example</span></span>

<span data-ttu-id="4c5e3-126">I følgende illustrasjon opprettes en **Linjer**-datakilde som en postliste med tre poster.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="4c5e3-127">Denne listen er delt inn i partier, der hvert inneholder opptil to poster.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="4c5e3-128">Følgende illustrasjon viser det utformede formatoppsettet.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="4c5e3-129">I dette formatoppsettet opprettes bindinger til **Linjer**-datakilden for å generere utdata i XML-format.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="4c5e3-130">Disse utdataene viser individuelle noder for hvert parti og postene i det.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="4c5e3-131">Følgende illustrasjon viser resultatet når det utformede formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="4c5e3-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="4c5e3-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4c5e3-132">Additional resources</span></span>

[<span data-ttu-id="4c5e3-133">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="4c5e3-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

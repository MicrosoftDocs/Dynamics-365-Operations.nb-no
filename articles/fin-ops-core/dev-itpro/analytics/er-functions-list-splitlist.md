---
title: SPLITLIST ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLITLIST.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56ef02e3ea0ca2207ccdc79468a9ea4c1fbe8f95
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041889"
---
# <span data-ttu-id="81586-103"><a name="SPLITLIST">SPLITLIST ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="81586-103"><a name="SPLITLIST">SPLITLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81586-104">`SPLITLIST`-funksjonen deler den angitte listen i underlister (eller grupper), der hver inneholder det angitte antallet poster.</span><span class="sxs-lookup"><span data-stu-id="81586-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="81586-105">Deretter returneres resultatet som en ny *postliste*-verdi som består av partiene.</span><span class="sxs-lookup"><span data-stu-id="81586-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="81586-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="81586-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="81586-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="81586-107">Arguments</span></span>

<span data-ttu-id="81586-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="81586-108">`list`: *Record list*</span></span>

<span data-ttu-id="81586-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="81586-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="81586-110">`number`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="81586-110">`number`: *Integer*</span></span>

<span data-ttu-id="81586-111">Maksimalt antall poster per parti.</span><span class="sxs-lookup"><span data-stu-id="81586-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="81586-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="81586-112">Return values</span></span>

<span data-ttu-id="81586-113">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="81586-113">*Record list*</span></span>

<span data-ttu-id="81586-114">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="81586-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="81586-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="81586-115">Usage notes</span></span>

<span data-ttu-id="81586-116">Listen over partier som returneres, inneholder følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="81586-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="81586-117">**Verdi:** *Liste*</span><span class="sxs-lookup"><span data-stu-id="81586-117">**Value:** *List*</span></span>

    <span data-ttu-id="81586-118">Listen over oppføringer som tilhører gjeldende parti.</span><span class="sxs-lookup"><span data-stu-id="81586-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="81586-119">**BatchNumber:** *Heltall*</span><span class="sxs-lookup"><span data-stu-id="81586-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="81586-120">Nummeret for gjeldende parti i den returnerte listen.</span><span class="sxs-lookup"><span data-stu-id="81586-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="81586-121">Eksempel</span><span class="sxs-lookup"><span data-stu-id="81586-121">Example</span></span>

<span data-ttu-id="81586-122">I følgende illustrasjon opprettes en **Linjer**-datakilde som en postliste med tre poster.</span><span class="sxs-lookup"><span data-stu-id="81586-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="81586-123">Denne listen er delt inn i partier, der hvert inneholder opptil to poster.</span><span class="sxs-lookup"><span data-stu-id="81586-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="81586-124">Følgende illustrasjon viser det utformede formatoppsettet.</span><span class="sxs-lookup"><span data-stu-id="81586-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="81586-125">I dette formatoppsettet opprettes bindinger til **Linjer**-datakilden for å generere utdata i XML-format.</span><span class="sxs-lookup"><span data-stu-id="81586-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="81586-126">Disse utdataene viser individuelle noder for hvert parti og postene i det.</span><span class="sxs-lookup"><span data-stu-id="81586-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="81586-127">Følgende illustrasjon viser resultatet når det utformede formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="81586-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="81586-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="81586-128">Additional resources</span></span>

[<span data-ttu-id="81586-129">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="81586-129">List functions</span></span>](er-functions-category-list.md)

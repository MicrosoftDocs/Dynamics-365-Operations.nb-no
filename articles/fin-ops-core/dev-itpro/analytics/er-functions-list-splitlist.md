---
title: SPLITLIST ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLITLIST.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559144"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="c15d5-103">SPLITLIST ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="c15d5-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c15d5-104">`SPLITLIST`-funksjonen deler den angitte listen i underlister (eller grupper), der hver inneholder det angitte antallet poster.</span><span class="sxs-lookup"><span data-stu-id="c15d5-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="c15d5-105">Deretter returneres resultatet som en ny *postliste*-verdi som består av partiene.</span><span class="sxs-lookup"><span data-stu-id="c15d5-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="c15d5-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c15d5-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="c15d5-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c15d5-107">Arguments</span></span>

<span data-ttu-id="c15d5-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="c15d5-108">`list`: *Record list*</span></span>

<span data-ttu-id="c15d5-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="c15d5-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="c15d5-110">`number`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="c15d5-110">`number`: *Integer*</span></span>

<span data-ttu-id="c15d5-111">Maksimalt antall poster per parti.</span><span class="sxs-lookup"><span data-stu-id="c15d5-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="c15d5-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="c15d5-112">Return values</span></span>

<span data-ttu-id="c15d5-113">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="c15d5-113">*Record list*</span></span>

<span data-ttu-id="c15d5-114">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="c15d5-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c15d5-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="c15d5-115">Usage notes</span></span>

<span data-ttu-id="c15d5-116">Listen over partier som returneres, inneholder følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="c15d5-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="c15d5-117">**Verdi:** *Liste*</span><span class="sxs-lookup"><span data-stu-id="c15d5-117">**Value:** *List*</span></span>

    <span data-ttu-id="c15d5-118">Listen over oppføringer som tilhører gjeldende parti.</span><span class="sxs-lookup"><span data-stu-id="c15d5-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="c15d5-119">**BatchNumber:** *Heltall*</span><span class="sxs-lookup"><span data-stu-id="c15d5-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="c15d5-120">Nummeret for gjeldende parti i den returnerte listen.</span><span class="sxs-lookup"><span data-stu-id="c15d5-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="c15d5-121">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c15d5-121">Example</span></span>

<span data-ttu-id="c15d5-122">I følgende illustrasjon opprettes en **Linjer**-datakilde som en postliste med tre poster.</span><span class="sxs-lookup"><span data-stu-id="c15d5-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="c15d5-123">Denne listen er delt inn i partier, der hvert inneholder opptil to poster.</span><span class="sxs-lookup"><span data-stu-id="c15d5-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="c15d5-124">Følgende illustrasjon viser det utformede formatoppsettet.</span><span class="sxs-lookup"><span data-stu-id="c15d5-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="c15d5-125">I dette formatoppsettet opprettes bindinger til **Linjer**-datakilden for å generere utdata i XML-format.</span><span class="sxs-lookup"><span data-stu-id="c15d5-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="c15d5-126">Disse utdataene viser individuelle noder for hvert parti og postene i det.</span><span class="sxs-lookup"><span data-stu-id="c15d5-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="c15d5-127">Følgende illustrasjon viser resultatet når det utformede formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="c15d5-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="c15d5-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c15d5-128">Additional resources</span></span>

[<span data-ttu-id="c15d5-129">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="c15d5-129">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: SPLITLISTBYLIMIT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLITLISTBYLIMIT.
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
ms.openlocfilehash: 5bf13b7c1e7cab7c803b352370084421a8180dee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743445"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="8c593-103">SPLITLISTBYLIMIT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="8c593-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c593-104">`SPLITLISTBYLIMIT`-funksjonen deler den angitte listen inn i en ny liste over underlister (grupper).</span><span class="sxs-lookup"><span data-stu-id="8c593-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="8c593-105">Antall poster i hvert parti beregnes dynamisk.</span><span class="sxs-lookup"><span data-stu-id="8c593-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="8c593-106">Denne funksjonen returneres resultatet som en ny *postliste*-verdi som består av partiene.</span><span class="sxs-lookup"><span data-stu-id="8c593-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c593-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8c593-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="8c593-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8c593-108">Arguments</span></span>

<span data-ttu-id="8c593-109">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="8c593-109">`list`: *Record list*</span></span>

<span data-ttu-id="8c593-110">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="8c593-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="8c593-111">`limit value`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="8c593-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="8c593-112">Maksimumsverdien for grensen som brukes til å dele den opprinnelige listen i partier.</span><span class="sxs-lookup"><span data-stu-id="8c593-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="8c593-113">`limit source`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="8c593-113">`limit source`: *Field*</span></span>

<span data-ttu-id="8c593-114">Den gyldige banen til et felt av *Heltall* eller *Reell*-typen i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="8c593-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="8c593-115">Verdien i dette feltet definerer trinnet som den totale summen økes på.</span><span class="sxs-lookup"><span data-stu-id="8c593-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c593-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="8c593-116">Return values</span></span>

<span data-ttu-id="8c593-117">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="8c593-117">*Record list*</span></span>

<span data-ttu-id="8c593-118">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="8c593-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8c593-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="8c593-119">Usage notes</span></span>

<span data-ttu-id="8c593-120">Listen over partier som returneres, inneholder følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="8c593-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="8c593-121">**Verdi**: *Liste*</span><span class="sxs-lookup"><span data-stu-id="8c593-121">**Value**: *List*</span></span>

    <span data-ttu-id="8c593-122">Listen over oppføringer som tilhører gjeldende parti.</span><span class="sxs-lookup"><span data-stu-id="8c593-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="8c593-123">**BatchNumber**: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="8c593-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="8c593-124">Nummeret for gjeldende parti i den returnerte listen.</span><span class="sxs-lookup"><span data-stu-id="8c593-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="8c593-125">Grensen brukes ikke på en enkelt vare i originallisten hvis kildegrensen overskrider den definerte grensen.</span><span class="sxs-lookup"><span data-stu-id="8c593-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="8c593-126">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8c593-126">Example</span></span>

<span data-ttu-id="8c593-127">Illustrasjonen nedenfor viser et ER-format.</span><span class="sxs-lookup"><span data-stu-id="8c593-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="8c593-128">Følgende illustrasjon viser datakildene som brukes for formatet.</span><span class="sxs-lookup"><span data-stu-id="8c593-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="8c593-129">Følgende illustrasjon viser resultatet når formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="8c593-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="8c593-130">I dette tilfellet er utdataene en flat liste over artikkelvarer.</span><span class="sxs-lookup"><span data-stu-id="8c593-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="8c593-131">I illustrasjonene nedenfor er det samme formatet justert slik at det viser listen over artikkelvarer i partier hvis et enkelt parti må inneholde artikler, og den totale vekten må ikke overskride grensen på 9.</span><span class="sxs-lookup"><span data-stu-id="8c593-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="8c593-132">Følgende illustrasjon viser resultatet når det justerte formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="8c593-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="8c593-133">Grensen gjelder ikke for det siste elementet i den originale listen siden verdien (**11**) av grensekilden (**vekt**) overskrider den definerte grensen (**9**).</span><span class="sxs-lookup"><span data-stu-id="8c593-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="8c593-134">For å ignorere underlister under rapportgenerering bruker du enten funksjonen `WHERE`- eller **Aktivert**-uttrykket for det tilsvarende formatelementet, etter behov.</span><span class="sxs-lookup"><span data-stu-id="8c593-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c593-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8c593-135">Additional resources</span></span>

[<span data-ttu-id="8c593-136">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="8c593-136">List functions</span></span>](er-functions-category-list.md)

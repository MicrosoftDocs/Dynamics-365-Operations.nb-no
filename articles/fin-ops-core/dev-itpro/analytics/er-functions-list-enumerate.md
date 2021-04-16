---
title: ENUMERATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ENUMERATE.
author: NickSelin
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746657"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="ba778-103">ENUMERATE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="ba778-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba778-104">`ENUMERATE`-funksjonen returnerer en ny *Postliste*-verdi som består av opplistede poster i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="ba778-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba778-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ba778-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="ba778-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ba778-106">Arguments</span></span>

<span data-ttu-id="ba778-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="ba778-107">`list`: *Record list*</span></span>

<span data-ttu-id="ba778-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="ba778-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ba778-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="ba778-109">Return values</span></span>

<span data-ttu-id="ba778-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="ba778-110">*Record list*</span></span>

<span data-ttu-id="ba778-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="ba778-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ba778-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="ba778-112">Usage notes</span></span>

<span data-ttu-id="ba778-113">Listen over nummererte poster som returneres, viser følgende tilleggselementer:</span><span class="sxs-lookup"><span data-stu-id="ba778-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="ba778-114">Posten med felt (**Verdi**-komponent)</span><span class="sxs-lookup"><span data-stu-id="ba778-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="ba778-115">Gjeldende postindeks (**Number**-komponent)</span><span class="sxs-lookup"><span data-stu-id="ba778-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="ba778-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ba778-116">Example</span></span>

<span data-ttu-id="ba778-117">I illustrasjonen nedenfor opprettes **Enumerated**-datakilden som en nummerert liste over leverandørposter fra **Vendors**-datakilden som refererer til VendTable-tabellen.</span><span class="sxs-lookup"><span data-stu-id="ba778-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="ba778-118">Illustrasjonen nedenfor viser ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="ba778-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="ba778-119">I dette formatet opprettes databindinger for å generere utdata i XML-format.</span><span class="sxs-lookup"><span data-stu-id="ba778-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="ba778-120">Disse utdataene viser enkeltleverandører som opplistede noder.</span><span class="sxs-lookup"><span data-stu-id="ba778-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="ba778-121">Følgende illustrasjon viser resultatet når det utformede formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="ba778-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="ba778-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ba778-122">Additional resources</span></span>

[<span data-ttu-id="ba778-123">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="ba778-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: LISTOFFIRSTITEM ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LISTOFFIRSTITEM.
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
ms.openlocfilehash: 4d985ef5015bc104a83260b64418821cc715e8cb
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917264"
---
# <span data-ttu-id="3f6a6-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="3f6a6-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f6a6-104">`LISTOFFIRSTITEM` -funksjonen returnerer en *Postliste*-verdi som består av bare den første posten i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="3f6a6-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6a6-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="3f6a6-105">Syntax</span></span>

```
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="3f6a6-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="3f6a6-106">Arguments</span></span>

<span data-ttu-id="3f6a6-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="3f6a6-107">`list`: *Record list*</span></span>

<span data-ttu-id="3f6a6-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="3f6a6-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3f6a6-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="3f6a6-109">Return values</span></span>

<span data-ttu-id="3f6a6-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="3f6a6-110">*Record list*</span></span>

<span data-ttu-id="3f6a6-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="3f6a6-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="3f6a6-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3f6a6-112">Example</span></span>

<span data-ttu-id="3f6a6-113">Uttrykket `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returnerer tekstverdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="3f6a6-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f6a6-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3f6a6-114">Additional resources</span></span>

[<span data-ttu-id="3f6a6-115">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="3f6a6-115">List functions</span></span>](er-functions-category-list.md)
